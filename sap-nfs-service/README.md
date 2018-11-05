# ISCSI Server
## Machine Info
This template will deploy an NFS cluster into your environment.  

#### Storage Configuration

This VM doesn't require any additional data disks.

## Deploy the Solution
### Deploy from the Portal

To deploy  the infrastructre from the portal using a graphic interface you can use the [![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzureCAT-GSI%2FSAP-HANA-S4%2Fmaster%2Fsap-hana-cluster%2Fazuredeploy-hsr-infra.json)

To deploy the Custom Script Extension to install and configure the software,  from the portal using a graphic interface you can use [![Deploy to Azure](http://azuredeploy.net/deploybutton.png)](https://portal.azure.com/#create/Microsoft.Template/uri/https%3A%2F%2Fraw.githubusercontent.com%2FAzureCAT-GSI%2FSAP-HANA-S4%2Fmaster%2Fsap-hana-cluster%2Fazuredeploy-hsr-sw.json)


## Infrastructure Parameters

Parameter name | Required | Description | Default Value | Allowed Values
-------------- | -------- | ----------- | ------------- | --------------
VM Name |Yes |Name of the NFS Server | None | No restrictions
Existing Network Resource Group | No | This gives you the option to deploy the VMs to an existing VNET in a different Resource Group. The value provided should match the name of the existing Resource Group. To deploy the VNET in the same Resource Group the value should be set to "no" | no | No restrictions
VNET Name |No |Name of the Azure VNET which will be used for the VM | vnet | No restrictions
Subnet Name |No | Name of the subnet where the ISCSI server will be provisioned | mgtsubnet | No restrictions
VM User Name | No | Username for both NFS servers | No restrictions
VM Password | Yes | Password for the user defined above | None | No restrictions
OS Type | No | OS to use for the ISCSI Server | SLES 12 SP3 | "Windows Server 2016 Datacenter", "SLES 12 SP3",  "SLES 12 SP3 BYOS",  "SLES 12 SP2", "SLES 12 SP2 BYOS"
Static IP 1 | No | Allows you to choose the specific IP to be assgined to the first NFS server. | 10.0.1.7 | No restrictions
Static IP 2 | No | Allows you to choose the specific IP to be assgined to the second NFS server. | 10.0.1.8 | No restrictions
iSCSI IP | No | IP Address for the iSCSI server | 10.0.2.6 | No restrictions
ILB IP | No | IP Address for the internal load balancer | 10.0.5.10 | No restrictions
_artifactsLocation | No | The base URI where artifacts required by this template are located. When the template is deployed using the accompanying scripts, a private location in the subscription will be used and this value will be automatically generated. |  https://raw.githubusercontent.com/AzureCAT-GSI/SAP-HANA-S4/master/sap-nfs-service/ | No restrictions
_artifactsLocationSasToken | No | The sasToken required to access _artifactsLocation.  When the template is deployed using the accompanying scripts, a sasToken will be automatically generated. |   | No restrictions
HANA SID | No | SAP HANA System ID | H10 | No restrictions
Subscription Email | No | OS subscription email for BYOS. Leave blank for pay-as-you-go OS image. |  | No restrictions
Subscription ID | No | OS ID or password for BYOS. Leave blank for pay-as-you-go OS image. |  | No restrictions
SMT Uri | No | The URI to a subscription management server if used, blank otherwise |  | No restrictions

## Software Parameters

Parameter name | Required | Description | Default Value | Allowed Values
-------------- | -------- | ----------- | ------------- | --------------
VM Name 1 |Yes |Name of the first NFS Virtual Machine. | None | No restrictions
VM Name 2 |Yes |Name of the second NFS Virtual Machine. | None | No restrictions
VM User Name | No | Username for both the NFS servers  | testuser | No restrictions
VM Password | Yes | Password for the user defined above | None | No restrictions
tatic IP 1 | No | Allows you to choose the specific IP to be assgined to the first NFS server. | 10.0.0.20 | No restrictions
Static IP 2 | No | Allows you to choose the specific IP to be assgined to the second NFS server. | 10.0.0.21 | No restrictions
iSCSI IP | No | IP Address for the iSCSI server | 10.0.2.6 | No restrictions
IQN  | Yes | IQN for the  ISCSI target | No | No restrictions
IQN  Client 1 | Yes | IQN for the first client connecting to the  ISCSI target | No | No restrictions
IQN Client 2 | Yes | IQN for the second client connecting to the ISCSI target | No | No restrictions
ILB IP | No | IP Address for the internal load balancer | 10.0.5.10 | No restrictions
_artifactsLocation | No | The base URI where artifacts required by this template are located. When the template is deployed using the accompanying scripts, a private location in the subscription will be used and this value will be automatically generated. | https://raw.githubusercontent.com/AzureCAT-GSI/Hana-Test-Deploy/master/ | No restrictions
_artifactsLocationSasToken | No | The sasToken required to access _artifactsLocation.  When the template is deployed using the accompanying scripts, a sasToken will be automatically generated | | No restrictions
