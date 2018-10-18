## Infrastructure Parameters

Parameter name | Required | Description | Default Value | Allowed Values
-------------- | -------- | ----------- | ------------- | --------------
VM Name 1 |Yes |Name of the first ASCS Virtual Machine. | None | No restrictions
VM Name 2 |Yes |Name of the second ASCS Virtual Machine. | None | No restrictions
VM Size |No |Defines the size of the Azure VM for the ASCS servers. | Standard_DS3_v2 |  "Standard_DS3_v2", "Standard_DS12_v2", "Standard_DS13-4_v2", "Standard_DS14-4_v2", "Standard_F4s", "Standard_D8s_v3", "Standard_D32-8s_v3", "Standard_E8s_v3", "Standard_F8s_v2", "Standard_DS4_v2", "Standard_DS13_v2", "Standard_DS14-8_v2", "Standard_F8s", "Standard_D16s_v3", "Standard_D32-16s_v3", "Standard_D64-16s_v3", "Standard_E16s_v3", "Standard_E32-16s_v3", "Standard_F16s_v2", "Standard_D5_v2", "Standard_DS5_v2","Standard_DS14_v2", "Standard_F16s", "Standard_D32s_v3", "Standard_D64-32s_v3", "Standard_E32s_v3","Standard_E32-8s_v3", "Standard_F32s_v2", "Standard_DS15_v2", "Standard_D40s_v3", "Standard_D64s_v3", "Standard_E64s_v3", "Standard_E64-16s_v3", "Standard_E64-32s_v3", "Standard_F64s_v2", "Standard_F72s_v2", "Standard_L8s_v2", "Standard_L16s_v2", "Standard_L32s_v2", "Standard_L64s_v2", "Standard_L96s_v2", "Standard_D4s_v3", "Standard_DS2_v2", "Standard_E4s_v3", "Standard_F2s", "Standard_F4s_v2", "Standard_DS11_v2" | Only VM sizes specified.
VNET Name |No |Name of the Azure VNET to be provisioned. Assumes existing VNET | ra-hana-vnet | No restrictions
Subnet Name |No | Name of the subnet where the ASCS server will be provisioned. Assumes existing Subnet | DataSubnet | No restrictions
VM User Name | No | Username for both the HANA server and the HANA jumpbox | testuser | No restrictions
VM Password | Yes | Password for the user defined above | None | No restrictions
Operating System | No | Linux distribution to use for the HANA server | SLES for SAP 12 SP2 | SLES for SAP 12 SP2, RHEL 7.2 for SAP HANA
Existing Network Resource Group | No | This gives you the option to deploy the VMs to an existing VNET in a different Resource Group. The value provided should match the name of the existing Resource Group. To deploy the VNET in the same Resource Group the value should be set to "no" | no | No restrictions
IP Allocation Method | no | Lets you choose between Static and Dynamic IP Allocation | Dynamic | Dynamic, Static
Static IP 1 | No | Allows you to choose the specific IP to be assgined to the first HANA server. | 10.0.0.20 | No restrictions
Static IP 2 | No | Allows you to choose the specific IP to be assgined to the second HANA server. | 10.0.0.21 | No restrictions
ISCSI IP | No | IP Address of the ISCSI server that will be used as target. | 10.0.2.6 | No restrictions
ASCS LB IP | No | IP Address of the ASCS Internal Load Balancer | 10.0.5.10 | No restrictions
ERS LB IP | No | IP Address of the ERS Internal Load Balancer | 10.0.5.11 | No restrictions
ASCS Instance | No | Instance number for the ASCS install | 00 | No restrictions
Subscription Email | No | OS subscription email for BYOS. Leave blank for pay-as-you-go OS image. |  | No restrictions
Subscription ID | No | OS ID or password for BYOS. Leave blank for pay-as-you-go OS image. |  | No restrictions
SMT Uri | No | The URI to a subscription management server if used, blank otherwise |  | No restrictions

## Software Parameters

Parameter name | Required | Description | Default Value | Allowed Values
-------------- | -------- | ----------- | ------------- | --------------
VM Name 1 |Yes |Name of the first HANA Virtual Machine. | None | No restrictions
VM Name 2 |Yes |Name of the second HANA Virtual Machine. | None | No restrictions
Custom URI | Yes | URI where the SAP bits were uploaded | None | No restrictions
VM User Name | No | Username for both the HANA server and the HANA jumpbox | testuser | No restrictions
VM Password | Yes | Password for the user defined above | None | No restrictions
Operating System | No | Linux distribution to use for the HANA server | SLES for SAP 12 SP2 | SLES for SAP 12 SP2, RHEL 7.2 for SAP HANA
HANASID | No | HANA System ID | H10 | No restrictions
HANA Number | No | SAP HANA Instance Number | 00 | No restrictions
Static IP 1 | No | Allows you to choose the specific IP to be assgined to the first HANA server. | 10.0.0.20 | No restrictions
Static IP 2 | No | Allows you to choose the specific IP to be assgined to the second HANA server. | 10.0.0.21 | No restrictions
ISCSI IP | No | IP Address of the ISCSI server that will be used as target. | 10.0.2.6 | No restrictions
IQN | No | IQN for the ISCSI server | iqn.1991-05.com.microsoft:hana-target | No restrictions
IQNClient1 | No | IQN for the first ISCSI client (first HANA VM) | iqn.1991-05.com.microsoft:hana-target:hanavm1 | No restrictions
IQNClient2 | No | IQN for the second ISCSI client (second HANA VM) | iqn.1991-05.com.microsoft:hana-target:hanavm2 | No restrictions
ILB IP | No | IP Address of the Internal Load Balancer | 10.0.0.22 | No restrictions
Subscription Email | No | OS subscription email for BYOS. Leave blank for pay-as-you-go OS image. |  | No restrictions
Subscription ID | No | OS ID or password for BYOS. Leave blank for pay-as-you-go OS image. |  | No restrictions
SMT Uri | No | The URI to a subscription management server if used, blank otherwise |  | No restrictions
NFS IP | No | IP Address of the NFS server | 10.0.1.10 | No restrictions
