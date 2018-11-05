## Infrastructure Parameters

Parameter name | Required | Description | Default Value | Allowed Values
-------------- | -------- | ----------- | ------------- | --------------
VM Name |Yes |Name of the first Netweaver Virtual Machine. | nwVm | No restrictions
VM Size |No |Defines the size of the Azure VM for the ASCS servers. | Standard_DS2_v2 |  "Standard_DS13_v2", "Standard_DS14_v2" | Only VM sizes specified.
VNET Name |No |Name of the Azure VNET to be provisioned. Assumes existing VNET | ra-hana-vnet | No restrictions
Subnet Name |No | Name of the subnet where the ASCS server will be provisioned. Assumes existing Subnet | appsubnet | No restrictions
VM User Name | No | Username for both the Netweaver servers | testuser | No restrictions
VM Password | Yes | Password for the user defined above | None | No restrictions
Operating System | No | Linux distribution to use for the Netweaver server | SLES 12 SP3 | Windows Server 2016 Datacenter, SLES 12 SP3, SLES 12 SP3 BYOS, SLES 12 SP2, SLES 12 SP2 BYOS
Existing Network Resource Group | No | This gives you the option to deploy the VMs to an existing VNET in a different Resource Group. The value provided should match the name of the existing Resource Group. To deploy the VNET in the same Resource Group the value should be set to "no" | no | No restrictions
Fault Domain Max | No | Number of fault domains for the availability set | 2 | 1, 2, 3
App Avail Set Name | No | Availability Set Name for the VMs | avset-nw | No
Static IP | No | Allows you to choose the specific IP to be assgined to the Netweaver server. | 10.0.1.49 | No restrictions
_artifactsLocation | No | The base URI where artifacts required by this template are located. When the template is deployed using the accompanying scripts, a private location in the subscription will be used and this value will be automatically generated. |  https://raw.githubusercontent.com/AzureCAT-GSI/SAP-HANA-S4/master/sap-netweaver-server/ | No restrictions
_artifactsLocationSasToken | No | The sasToken required to access _artifactsLocation.  When the template is deployed using the accompanying scripts, a sasToken will be automatically generated. |   | No restrictions

## Software Parameters

Parameter name | Required | Description | Default Value | Allowed Values
-------------- | -------- | ----------- | ------------- | --------------
VM Name |Yes |Name of the first Netweaver Virtual Machine. | None | No restrictions
Static IP | No | Allows you to choose the specific IP to be assgined to the Netweaver server. | 10.0.1.49 | No restrictions
OS Type| No | Type of OS you want to deploy| SLES 12 SP3 | Windows Server 2016 Datacenter, SLES 12 SP3, SLES 12 SP3 BYOS, SLES 12 SP2, SLES 12 SP2 BYOS
Is Primary | No | Establishes whether the deployment is for the primary application server | Yes | Yes, No
Custom URI| Yes | URI where SAP bits are uploaded | None | No restrictions
NFS ILB IP | No | IP Address for the NFS internal load balancer | 10.0.1.10 | No restrictions
ASCS VM 1 | No | VM name of ASCS VM 1 | ascs1 | No restrictions
ASCS IP 1 | No | IP Address of ASCS VM 1 | 10.0.1.17 | No restrictions
ASCS VM 2 | No | VM name of ASCS VM 2 | ascs2 | No restrictions
ASCS VM 2 | No | IP Addressof ASCS VM 2 | 10.0.1.18 | No restrictions
_artifactsLocation | No | The base URI where artifacts required by this template are located. When the template is deployed using the accompanying scripts, a private location in the subscription will be used and this value will be automatically generated. |  https://raw.githubusercontent.com/AzureCAT-GSI/SAP-HANA-S4/master/sap-netweaver-server/ | No restrictions
_artifactsLocationSasToken | No | The sasToken required to access _artifactsLocation.  When the template is deployed using the accompanying scripts, a sasToken will be automatically generated. |   | No restrictions
Master Password | No | SAP Master Password | SecureString | No restrictions
SAP ADM UID | No | User ID for sapadm | 1040 | No restrictions
SAPSYS GID | No | Group ID for sapsys| 1001 | No restrictions
SID ADM UID | No | User ID for sidadm | 1050 | No restrictions
DB HOST | No | Host name for the database | hanailb | No restrictions
DB Instance | No | Instance number for the database | 03 | 2 characters
DB SID | No | Database System ID | 00 | 2 characters
ASCS SID | No | SAP ASCS ID | 04 | No restrictions
ASCS Host | No | VM name of ASCS VM 1 | ascs1 | No restrictions
NW Instance | No | SAP NW Instance | 05 | 2 characters
