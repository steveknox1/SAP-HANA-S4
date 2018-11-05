#  Network Time Protocol server using a Marketplace image


This template takes a minimum amount of parameters and deploys an Linux NTP server.

## Infrastructure Parameters

Parameter name | Required | Description | Default Value | Allowed Values
-------------- | -------- | ----------- | ------------- | --------------
VM Name |Yes |Name of the Virtual Machine. | None | No restrictions
VNET Name |No |Name of the Azure VNET to be provisioned | ra-hana-vnet | No restrictions
Subnet Name | No | Name of the subnet where the NTP server will be provisioned | subnet | No restrictions
VM User Name | No | Username for th NTP Server | testuser | No restrictions
VM Password | Yes | Password for the user defined above | None | No restrictions
OS Type | No | Linux distribution to use for the NTP server | SLES for SAP 12 SP2 | SLES for SAP 12 SP2, RHEL 7.2 for SAP HANA
Existing Network Resource Group | No | This gives you the option to deploy the VMs to an existing VNET in a different Resource Group. The value provided should match the name of the existing Resource Group. To deploy the VNET in the same Resource Group the value should be set to "no" | no | No restrictions
Custom URI | Yes | Location of the SAP Bits | None | No restrictions
Static IP | Yes | Allows you to choose the specific IP to be assgined to the NTP server. | No  | No restrictions
artifactsLocation | No | The base URI where artifacts required by this template are located. When the template is deployed using the accompanying scripts, a private location in the subscription will be used and this value will be automatically generated. |  https://raw.githubusercontent.com/AzureCAT-GSI/SAP-HANA-S4/master/sap-nfs-service/ | No restrictions
_artifactsLocationSasToken | No | The sasToken required to access _artifactsLocation.  When the template is deployed using the accompanying scripts, a sasToken will be automatically generated. |   | No restrictions


## Software Parameters

VM Name |Yes |Name of the Virtual Machine. | None | No restrictions
VNET Name |No |Name of the Azure VNET to be provisioned | ra-hana-vnet | No restrictions
Subnet Name | No | Name of the subnet where the NTP server will be provisioned | subnet | No restrictions
VM User Name | No | Username for th NTP Server | testuser | No restrictions
VM Password | Yes | Password for the user defined above | None | No restrictions
OS Type | No | Linux distribution to use for the NTP server | SLES for SAP 12 SP2 | SLES for SAP 12 SP2, RHEL 7.2 for SAP HANA
Existing Network Resource Group | No | This gives you the option to deploy the VMs to an existing VNET in a different Resource Group. The value provided should match the name of the existing Resource Group. To deploy the VNET in the same Resource Group the value should be set to "no" | no | No restrictions
Custom URI | Yes | Location of the SAP Bits | None | No restrictions
Static IP | Yes | Allows you to choose the specific IP to be assgined to the NTP server. | No  | No restrictions
artifactsLocation | No | The base URI where artifacts required by this template are located. When the template is deployed using the accompanying scripts, a private location in the subscription will be used and this value will be automatically generated. |  https://raw.githubusercontent.com/AzureCAT-GSI/SAP-HANA-S4/master/sap-nfs-service/ | No restrictions
_artifactsLocationSasToken | No | The sasToken required to access _artifactsLocation.  When the template is deployed using the accompanying scripts, a sasToken will be automatically generated. |   | No restrictions


