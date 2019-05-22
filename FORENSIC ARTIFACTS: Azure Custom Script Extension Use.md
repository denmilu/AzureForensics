# FORENSIC ARTIFACTS: Azure Custom Script Extension Use

## Azure Portal Artifacts
Audit logs from the Azure platform itself can be found in the VM's "Activity Logs" in the Azure Portal. The events you're looking for are named "Create or Update Virtual Machine Extension". The JSON details contain details on when the job was executed, who did it, what the payload was, and other useful bits.

The "Create or Update Virtual Machine Extension" events can be alerted on via Health Alerts config or by using Azure Security Center.


## Windows VM Artifacts
When a Custom Script Extension (CSE) run is submitted via the Azure front door (Portal / API / PowerShell) to run on a Windows machine several things happen:

1. The script is uploaded to an Azure Storage account associated with Azure Compute.
2. The Azure Guest Agent on the VM installs the CSE application and supporting files to:
    C:\Packages\Plugins\Microsoft.Compute.CustomScriptExtension\
3. The script uploaded to Storage is downloaded to the VM by the Guest Agent.
4. CustomScriptHandler.exe executes the instructions passed to it (i.e. the PowerShell script and any supplied arguments.)

The script in step 4 can be found in:
    C:\Packages\Plugins\Microsoft.Compute.CustomScriptExtension\version_number\Downloads\\#\

In fact, this same folder is where any files and folders created as part of the script execution will be found.

NOTE: If the script contains instructions to delete the files then only the script itself will still be found on disk. However, the script will still contain the deletion commands so you can at least know what was deleted.

NOTE: CustomScriptHandler.exe runs as SYSTEM and so the PowerShell script and any processes created by it will also be run as SYSTEM.

If the CSE is deleted from the VM via the Azure front door then the Guest Agent will delete the entire Microsoft.Compute.CustomScriptExtension folder from C:\Packages\Plugins\ and all its contents. Since TRIM is in use on Windows VMs in Azure, there is risk that no file data itself will be left behind on disk.

If you have 4688 command line and PowerShell script audit logging enabled then you should be able to pull the script and other details about the run from it.

