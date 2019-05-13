---

copyright:
  years: 2016, 2019
lastupdated: "2019-05-03"

subcollection: vmware-solutions


---

{:tip: .tip}
{:note: .note}
{:important: .important}

# Instance history messages
{: #audit_messages}

All operations that {{site.data.keyword.cloud_notm}} performs for your VMware instance are logged in the instance history. You can use the instance history as a reference to review these operations. For more information about reviewing your instance history, see [Procedure to view the deployment history for vCenter Server instances](/docs/services/vmwaresolutions?topic=vmware-solutions-vc_viewinginstances#vc_viewinginstances-procedure-view-deploy-history).

The following sections provide all of the possible messages that can be issued to your instance history.

## General instance history messages
{: #audit_messages-general}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for general actions:

* ``Starting to create the instance user and required services...``
* ``The instance user and required services creation is complete.``
* ``Ordering the vCenter Server license...``
* ``Ordering VMware licenses...``
* ``Completed the order for VMware licenses.``
* ``Ordering <quantity> upcharges...``
* ``Starting the <environment> installation and configuration...``
* ``The <environment> installation and configuration is complete.``
* ``Starting VMware components...``
* ``Starting to deploy the instance...``
* ``The <instance_name> instance is ready to use.``
* ``Starting upgrade to <version>...``
* ``The upgrade to <version> is complete.``
* ``VMware component upgrade is complete.``
* ``Starting the <instance_name> instance deletion...``
* ``The <instance_name> instance is successfully deleted.``
* ``The secure wipe of the instance is complete.``
* ``Cancelling the vCenter license...``
* ``Cancelling the instance user and required services...``
* ``Cancelling <environment> upcharges...``
* ``VMware license cancellation in progress...``
* ``VMware license cancellation is complete.``
* ``The SoftLayer order failed or timed out.``

## Instance error messages
{: #audit_messages-error}

{{site.data.keyword.vmwaresolutions_short}} issues the following instance history error messages:

* ``Error ordering VMware licenses. Open a service ticket for assistance.``
* ``Error ordering subnets. Open a service ticket for assistance.``
* ``Error: The SoftLayer API key is not valid. Open a service ticket for assistance.``
* ``Error: The SoftLayer data center is not valid. Open a service ticket for assistance.``
* ``Error using a shared image in the provided SoftLayer account. Open a service ticket for assistance.``
* ``Error ordering service entries. Open a service ticket for assistance.``
* ``Error ordering subnets. Open a service ticket for assistance.``
* ``Error ordering licenses. Open a service ticket for assistance.``
* ``Error ordering services. Open a service ticket for assistance.``

## Cluster history messages
{: #audit_messages-cluster}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for vCenter Server clusters:

* ``Starting the cluster configuration...``
* ``Starting the cluster configuration for <cluster_name>...``
* ``The cluster configuration is complete.``
* ``The <cluster_name> cluster is ready to use.``
* ``Adding the new cluster into vCenter...``
* ``The new cluster is added to vCenter.``
* ``Starting the cluster deletion for <cluster_name>...``
* ``Deleting the <cluster_name> cluster from vCenter...``
* ``The <cluster_name> cluster is deleted from vCenter.``
* ``The <cluster_name> cluster is deleted.``

## ESXi server history messages
{: #audit_messages-esxi}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for ESXi servers:

* ``Starting the order for <quantity> ESXi servers...``
* ``Verifying the ESXi server order...``
* ``The ESXi servers with the <ip_addresses> Private IP address are ready.``
* ``All ESXi servers are reclaimed.``
* ``Adding ESXi servers to the vCenter Server instance...``
* ``The ESXi servers are successfully updated.``
* ``Starting to order ESXi servers for cluster...``
* ``Starting to order <quantity> ESXi servers for the <Cluster Name> cluster...``
* ``The ESXi servers for the cluster are ready.``
* ``ESXi servers with the <ip_addresses> Private IP address are ready for the cluster.``
* ``The ESXi server is ready.``
* ``The ESXi server configuration is complete.``
* ``The ESXi server is successfully added with the property.``
* ``All requests for adding ESXi servers are successfully completed.``
* ``Adding the ESXi server...``
* ``Ordering a Bare Metal Server for the ESXi server...``
* ``New ESXi servers are added to vCenter.``
* ``Starting to add services to the new ESXi servers...``
* ``The selected ESXi servers are successfully cancelled.``
* ``New ESXi servers are provisioned.``
* ``New ESXi servers are verified and ready.``
* ``Starting to order <quantity> new ESXi servers for the <cluster_name> cluster...``
* ``The selected ESXi servers are removed from vCenter Server.``
* ``Starting to remove services to remove ESXi servers...``
* ``Verifying ESXi servers for the <cluster_name> cluster...``
* ``The new cluster ESXi servers successfully passed verification.``
* ``Verifying new ESXi server order...``
* ``The verification of the ESXi servers order failed.``
* ``Splitting batch add ESXi servers request.``
* ``Successfully completed all requests for removing ESXi servers.``
* ``The host is successfully added.``
* ``The host(s) are successfully removed.``
* ``Bare Metal Server cancellation in progress...``
* ``Bare Metal Server cancellation is complete.``
* ``Removing ESXi servers from the vCenter Server instance...``
* ``Removing the ESXi server.``
* ``Removing the <server_id> ESXi server.``
* ``Removing selected ESXi servers from vCenter Server...``
* ``Cancelling the ESXi servers...``
* ``Cancelling the selected ESXi servers...``

## Networking history messages
{: #audit_messages-network}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for network settings:

* ``Starting the public VLAN order...``
* ``Successfully completed the VLAN configuration.``
* ``Ordering additional private VLAN...``
* ``Additional private VLAN is provisioned.``
* ``An additional private VLAN Virtual Server Instance is provisioned.``
* ``Trunking additional private VLAN to Bare Metal Servers...``
* ``Successfully trunked the additional private VLAN to Bare Metal Servers.``
* ``Cancelling the additional private VLAN Virtual Server Instance...``
* ``Cancelling VLANs...``
* ``VLAN cancellation in progress...``
* ``VLAN cancellation is complete.``
* ``Ordering a two socket <type> NSX license...``
* ``NSX configuration for the new cluster is complete.``
* ``Cancelling  the two socket NSX license...``
* ``The NSX license has been successfully cancelled.``
* ``Starting the order for subnets...``
* ``The subnet is ready.``
* ``The portable private subnet is ready.``
* ``Granting new subnet access to NFS storage...``
* ``Cancelling subnets...``
* ``Subnet cancellation in progress...``
* ``Cancelling the customer portable private subnet...``
* ``Canceling the customer portable public subnet...``
* ``Cancelling the Endurance Storage private subnet...``
* ``Cancelling the portable public subnet...``
* ``The portable public subnet is ready.``
* ``Starting the portable public subnet order...``
* ``Subnet cancellation is complete.``
* ``Cancelling network storage...``

## Virtual Server Instance history messages
{: #audit_messages-vsi}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for Virtual Server Instances (VSIs):

* ``Ordering a new virtual server instance for the IBM CloudDriver...``
* ``The <ip_address> IBM CloudDriver virtual server instance is provisioned.``
* ``Cancelling the <ip_address> IBM CloudDriver virtual server instance...``
* ``Starting the order for the Microsoft Windows virtual server instance for Microsoft Active Directory/DNS...``
* ``Verifying the Microsoft Windows virtual server instance order for Active Directory/DNS...``
* ``The Microsoft Windows virtual server instance for Active Directory/DNS is ready.``
* ``Virtual server instance cancellation in progress...``
* ``Cancelling associated virtual server instances...``
* ``Virtual server instance cancellation is complete.``

## IBM CloudBuilder history messages
{: #audit_messages-cloudbuilder}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for IBM CloudBuilder:

* ``Verifying the IBM CloudBuilder Virtual Server Instance order...``
* ``Starting the order for the IBM CloudBuilder Virtual Server Instance...``
* ``The IBM CloudBuilder Virtual Server Instance is ready.``
* ``The IBM CloudBuilder is ready for service.``
* ``Dismissing the IBM CloudBuilder Virtual Server Instance...``

## IBM CloudDriver history messages
{: #audit_messages-clouddriver}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for IBM CloudDriver:

* ``Preparing the IBM CloudDriver...``
* ``The IBM CloudDriver is ready.``
* ``The <ip_address> IBM CloudDriver is ready to use.``
* ``Checking the IBM CloudDriver status...``
* ``Reusing the existing <ip_address> IBM CloudDriver...``
* ``Reusing the existing IBM CloudDriver (In Provisioning)...``
* ``Releasing the IBM CloudDriver...``
* ``Releasing the <ip_address> IBM CloudDriver...``
* ``Starting the IBM CloudDriver deletion...``
* ``Completed the IBM CloudDriver deletion.``

## Storage history messages
{: #audit_messages-storage}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for storage settings:

* ``Ordering the vSAN license...``
* ``Cancelling the vSAN license...``
* ``The VSAN license cancellation is complete.``
* ``Ordering <quantity> NFS storage(s) for the <cluster_name> cluster.``
* ``The new NFS storage is added and ready to use.``
* ``Cancelling Management NFS share storage...``
* ``The selected NFS storage is deleted.``
* ``Starting the order for Endurance Storage...``
* ``Cancelling Endurance Storage...``

## Service history messages
{: #audit_messages-services}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for services:

* ``Starting the management services setup...``
* ``Ordering service entries...``
* ``Completed the order for service entries.``
* ``IBM operation services are running.``
* ``Enabling the default services...``
* ``The default services are successfully enabled.``
* ``Service entry cancellation in progress...``
* ``Service entry cancellation is complete.``

## vCenter Server with Hybridity Bundle history messages
{: #audit_messages-hybridity}

{{site.data.keyword.vmwaresolutions_short}} issues the following messages for the vCenter Server with Hybridity Bundle instances:

* ``Ordering vCenter Server with Hybridity Bundle licenses...``
* ``Starting the vCenter Server with Hybridity Bundle conversion...``
* ``The vCenter Server with Hybridity Bundle conversion is complete.``
* ``Removing the vCenter Server with Hybridity Bundle...``
* ``The vCenter Server with Hybridity Bundle is successfully removed.``
* ``Cancelling the vCenter Server with Hybridity Bundle conversion...``

## Related links
{: #ibm_use-related}

* [Considerations about changing vCenter Server artifacts](/docs/services/vmwaresolutions?topic=vmware-solutions-vcenter_chg_impact#vcenter_chg_impact-automation-id)
* [Activity Tracker events](/docs/services/vmwaresolutions?topic=vmware-solutions-at-events#at-events)