---

copyright:

  years:  2016

lastupdated: "2016-12-12"

subcollection: vmware-solutions


---

{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:deprecated: .deprecated}

# Release notes for V1.2
{: #relnotes_v12}

This release includes new features, usability enhancements, and bug fixes.

## Component updates
{: #relnotes_v12-comp}

The new version of VMware ESXi is vSphere 6.0 u2 p03, updated from ESXi 6.0 u2 in the previous release.

## IBMid and Bluemix accounts association
{: #relnotes_v12-ibm-id}

{{site.data.keyword.vmwaresolutions_full}} is provided as an infrastructure solution in the IBM Bluemix® catalog. You must associate the **IBMid** account with a Bluemix account to use your **IBMid** account to log in to the {{site.data.keyword.vmwaresolutions_short}} console.

## Zerto disaster recovery
{: #relnotes_v12-zerto}

You can order both VMware Cloud Foundation instances and VMware vCenter Server instances with Zerto disaster recovery included when you order your instance. You can also add Zerto disaster recovery to your existing Cloud Foundation instances and vCenter Server instances in the instance details page.

## Pricing information
{: #relnotes_v12-price}

You can now see and review the estimated cost of your ordered instance before you decide to place an order. After you select your components when you order your instance, the total cost and the detailed pricing of all components are displayed on the **Summary** page.

## Enhancements to the instance order process
{: #relnotes_v12-inst-order}

The instance order process is greatly improved through the following enhancements:
* For both Cloud Foundation instances and vCenter Server instances, new validation checks are in place to ensure that the SoftLayer® user account that you are using has the required user permissions, that VLAN spanning is enabled, and that the correct API key is provided. If any requirements are not met, you get instructions right on the user interface to fix the problems.
*  For vCenter Server instances, the order in which you select the instance components is optimized so that only the data centers that have the available hardware and ESXi servers that you need are displayed. This change minimizes the possibility of errors later on.

## Additional email notifications
{: #relnotes_v12-email}

You now receive a notification by email when new ESXi servers are added to your instances and when the existing ESXi servers are removed. In addition, you get notified by email when an instance is deleted. The notification settings are enabled by default. Based on your preferences, you can set what notifications you want to receive on the **Settings** page.
