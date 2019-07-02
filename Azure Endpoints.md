Azure maintains many FQDNs which serve as service endpoints for other things on the internet to talk to. The list is enormous and I've never seen a consolidated one before, so here one is. It'll be maintained on a best-effort basis.

These may come in handy for forensic analysis, phishing investigations, malware reverse engineering, red teaming / pentesting, and many other use cases.

For all these endpoints Microsoft maintains publicly-signed SSL certificates in the root which cascade down to all subdomains, so they will all appear to be trusted sites, even when the customer is hosting malicious content.

## Endpoint Lists

### Access Control Service

This service has been shut down as of November 7, 2018. 
* [How to: Migrate from the Azure Access Control Service](https://docs.microsoft.com/en-us/azure/active-directory/develop/active-directory-acs-migration)

| Cloud | Type | Domain |
| --- | --- | --- |
| Public | Shut Down | *.accesscontrol.windows.net |
| Public | Still Active | accounts.accesscontrol.windows.net |
| Government | Shut Down | *.accesscontrol.windows.net |
| Germany | Shut Down | *.microsoftonline.de |
| China | Shut Down | *.accesscontrol.chinacloudapi.cn |

### API / Classic Deployment Model

| Cloud | Type | Domain |
| --- | --- | --- |
| Public | ARM | *.management.azure.com |
| Public | Classic | *.management.core.windows.net |
| Government |  | *.management.usgovcloudapi.net |
| Germany |  | *.management.core.cloudapi.de |
| China |  | *.management.core.chinacloudapi.cn |

### API Management

| Cloud | Type | Domain |
| --- | --- | --- |
| Public | API Management Gateway | *.azure-api.net |
| Public | API Management ... Management | *.management.azure-api.net |
| Public | API Management Portal | *.portal.azure-api.net |
| Government | API Management Gateway | *.azure-api.us |
| Government | API Management ... Management | *.management.azure-api.us |
| Government | API Management Portal | *.portal.azure-api.us |
| Germany |  |  |
| China |  | *.chinacloudapi.cn |

### Azure Active Directory Endpoint and Authority

| Cloud | Type | Domain |
| --- | --- | --- |
| Public | Primary | *.login.windows.net |
| Public | Alternate | *.login.microsoftonline.com |
| Government | New | *.login.microsoftonline.us |
| Government | Old | *.login-us.microsoftonline.com |
| Germany |  | *.login.microsoftonline.de |
| China | Primary | *.login.chinacloudapi.cn |
| China | Alternate | *.login.partner.microsoftonline.cn |

### Azure Active Directory Tenant Names

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.onmicrosoft.com |
| Government |  | *.onmicrosoft.com |
| Germany |  |  |
| China |  | *.partner.onmschina.cn |

### CDN

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.azureedge.net |
| Government |  |  |
| Germany |  |  |
| China |  |  |

### Cognitive Services

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | api.projectoxford.ai/face/v1.0 |
| Government |  |  |
| Germany |  |  |
| China |  | api.cognitive.azure.cn/face/v1.0 |

### Compute

| Cloud | Type | Domain |
| --- | --- | --- |
| Public | Classic (Cloud Service) | *.cloudapp.net |
| Public | ARM | *.cloudapp.azure.com |
| Government |  | *.cloudapp.usgovcloudapi.net |
| Germany |  |  |
| China |  | *.chinacloudapp.cn |

### Container Registry

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.azurecr.io |
| Government |  | *.azurecr.us |
| Germany |  |  |
| China |  |  |

### Cosmos DB

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.documents.azure.com |
| Government |  |  |
| Germany |  |  |
| China |  |  |

### Database

| Cloud | Type | Domain |
| --- | --- | --- |
| Public | Microsoft SQL | *.database.windows.net |
| Public | MySQL | *.mysql.database.azure.com |
| Government | Microsoft SQL | *.database.usgovcloudapi.net |
| Germany | Microsoft SQL | *.database.cloudapi.de |
| China | Microsoft SQL | *.database.chinacloudapi.cn |
| China | MySQL | *.mysqldb.chinacloudapi.cn |

### Database Import/Export Service

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  |  |
| Government |  |  |
| Germany |  |  |
| China | East | https://sh1prod-dacsvc.chinacloudapp.cn/dacwebservice.svc |
| China | North | https://bj1prod-dacsvc.chinacloudapp.cn/dacwebservice.svc |

### Database Management

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.management.database.windows.net |
| Government |  |  |
| Germany |  |  |
| China |  | *.management.database.chinacloudapi.cn |

### Gallery

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.gallery.azure.com |
| Government |  | *.gallery.azure.us |
| Germany |  | *.gallery.cloudapi.de |
| China |  |  |

### Graph API

[National Cloud Deployments](https://docs.microsoft.com/en-us/graph/deployments)

| Cloud | Type | Domain |
| --- | --- | --- |
| Global |  | *.graph.microsoft.com |
| Public |  | *.graph.windows.net |
| Government | L4 | *.graph.microsoft.us |
| Government | L5 (DOD) | *.dod-graph.microsoft.us |
| Germany | Primary | *.graph.cloudapi.de |
| Germany | Alternate | *.graph.microsoft.de |
| China | Primary | *.graph.chinacloudapi.cn |
| China | Alternate | *.microsoftgraph.chinacloudapi.cn |

### HDInsight

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  |  |
| Government |  |  |
| Germany |  |  |
| China |  | *.azurehdinsight.cn |

### Key Vault

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.vault.azure.net |
| Government |  | *.vault.usgovcloudapi.net |
| Germany |  | *.vault.microsoftazure.de |
| China |  | *.vault.azure.cn |

### Kusto / Data Explorer

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.kusto.windows.net |
| Government |  |  |
| Germany |  |  |
| China |  |  |

### LUIS Portal

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | luis.ai |
| Government |  | luis.azure.us |
| Germany |  |  |
| China |  |  |

### Media Services

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.streaming.media.azure.net |
| Government |  |  |
| Germany |  |  |
| China |  |  |

### Portal

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.portal.azure.com |
| Government |  | *.portal.azure.us |
| Germany |  | *.portal.microsoftazure.de |
| China |  | *.portal.azure.cn |

### Publish Settings File

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | portal.azure.com/#blade/Microsoft_Azure_ClassicResources/PublishingProfileBlade |
| Government |  | portal.azure.us#blade/Microsoft_Azure_ClassicResources/PublishingProfileBlade |
| Germany |  | manage.microsoftazure.de/publishsettings/index |
| China |  |  |

### Resource Manager

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  |  |
| Government |  | *.management.usgovcloudapi.net |
| Germany |  | *.management.microsoftazure.de |
| China |  | *.management.chinacloudapi.cn |

### Service Bus / Notification Hub

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.servicebus.windows.net |
| Government |  | *.servicebus.usgovcloudapi.net |
| Germany |  | *.servicebus.cloudapi.de |
| China |  | *.servicebus.chinacloudapi.cn |

### Service Fabric Cluster

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.cloudapp.azure.com |
| Government |  | *.cloudapp.usgovcloudapi.net |
| Germany |  |  |
| China |  | *.chinaeast.chinacloudapp.cn |

### Storage

| Cloud | Type | Domain |
| --- | --- | --- |
| Public | Blob | *.blob.core.windows.net |
| Public | File | *.file.core.windows.net |
| Public | Table | *.table.core.windows.net |
| Public | Queue | *.queue.core.windows.net |
| Public | Static Website | *.web.core.windows.net |
| Government | Blob | *.blob.core.usgovcloudapi.net |
| Government | File | *.file.core.usgovcloudapi.net |
| Government | Table | *.table.core.usgovcloudapi.net |
| Government | Queue | *.queue.core.usgovcloudapi.net |
| Germany | Blob | *.blob.core.cloudapi.de |
| Germany | File | *.file.core.cloudapi.de |
| Germany | Table | *.table.core.cloudapi.de |
| Germany | Queue | *.queue.core.cloudapi.de |
| China | Blob | *.blob.chinacloudapi.cn |
| China | File | *.file.chinacloudapi.cn |
| China | Table | *.table.chinacloudapi.cn |
| China | Queue | *.queue.chinacloudapi.cn |

### Traffic Manager

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  | *.trafficmanager.net |
| Government |  | *.usgovtrafficmanager.net |
| Germany |  | *.azuretrafficmanager.de |
| China |  |  |

### Web Apps

| Cloud | Type | Domain |
| --- | --- | --- |
| Public | Website | *.azurewebsites.net |
| Public | FTP(S) | *.azurewebsites.windows.net |
| Government |  | *.azurewebsites.us |
| Germany |  |  |
| China |  |  |

## Source Material
* [Azure Government Developer Guide](https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-developer-guide)
* [Azure China Developer Guide](https://docs.microsoft.com/en-us/azure/china/resources-developer-guide)
* [Azure Germany Developer Guide](https://docs.microsoft.com/en-us/azure/germany/germany-developer-guide)
* [Identity in National Clouds](https://docs.microsoft.com/en-us/azure/active-directory/develop/authentication-national-cloud)
* [Authorization considerations for tenants hosted in the Germany, China or US Government environments](https://docs.microsoft.com/en-us/sharepoint/dev/solution-guidance/extending-sharepoint-online-for-germany-china-usgovernment-environments)
* [Azure Government Web + Mobile](https://docs.microsoft.com/en-us/azure/azure-government/documentation-government-services-webandmobile)
* [API Management REST](https://docs.microsoft.com/en-us/rest/api/apimanagement/apimanagementrest/api-management-rest)

## Table Template

| Cloud | Type | Domain |
| --- | --- | --- |
| Public |  |  |
| Government |  |  |
| Germany |  |  |
| China |  |  |
