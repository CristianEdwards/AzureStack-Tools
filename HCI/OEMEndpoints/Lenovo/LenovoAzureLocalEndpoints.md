# Lenovo required endpoints for Azure Local deployments

This page provides a comprehensive overview of the necessary endpoints for deploying Azure Local using Lenovo solutions. These URLs are maintained by the OEM hardware vendor. Please contact with your OEM provider if these URLs need to be updated.

Each hardware vendor provided [Solution Builder Extension (SBE)](https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension) will require some minimal endpoints to allow for discovery and download of [SBE](https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension) updates for your solution.

Refer to the table in the following document to determine if your solution supports an SBE as well is to review SBE release notes or and other documentation: https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension?view=azloc-24113#identify-a-solution-builder-extension-update-for-your-hardware

In addition to [SBE](https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension) endpoints, some OEM hardware vendors will require additional endpoints for there specific use cases as noted below.

**Last updated on March 19, 2025**

| Id | Endpoint Description | Endpoint URL                                                           | Port | Notes                                                    | Arc gateway support | Required for                 |
|----|---------------------|------------------------------------------------------------------------|------|----------------------------------------------------------|---------------------|------------------------------|
| 1  | SBE Manifest endpoint    | thinkagile.lenovo.com/MX/SBE/SBE_Discovery_Lenovo.xml  | 443  | Enables discovery and confirmation of validity for SBE updates from OEM | No                  | Deployment & Post deployment |
| 2  | SBE Manifest redirection link     | aka.ms/AzureStackSBEUpdate/Lenovo                                      | 443  | Microsoft redirection to the explicit OEM SBE manifest endpoint. | No                 | Deployment & Post deployment |
| 3  | SBE Download list     | https://thinkagile.lenovo.com/MX/SBE/Lenovo_DownloadConnector_Matrix.xml                                   | 443  | online list of SBE download endpoints. Required for Azure Local to be able to download SBE files to avoid "AdditionalContentRequired" state (see "Download" in [Avanced SBE capabilities](https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension?view=azloc-24113#advanced-solution-builder-extension-capabilities)).<br><br>**Tip:** Review the contents of this file for the full list of endpoints, by SBE version.   | No                 | Deployment & Post deployment |
| 4  | SBE Download list redirection link     | aka.ms/LenovoSBEDownloadMatrix                                   | 443  | Microsoft redirection to online list of SBE download endpoints. Required for Azure Local to be able to download SBE files to avoid "AdditionalContentRequired" state (see "Download" in [Avanced SBE capabilities](https://learn.microsoft.com/en-us/azure/azure-local/update/solution-builder-extension?view=azloc-24113#advanced-solution-builder-extension-capabilities)). | No                 | Deployment & Post deployment |


