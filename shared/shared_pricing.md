---

copyright:

  years:  2019

lastupdated: "2019-12-13"

keywords: vmware solutions shared, price for shared, pricing plan

subcollection: vmware-solutions


---

{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}
{:important: .important}

# VMware Solutions Shared pricing
{: #shared_pricing}

VMware Solutions Shared offers two pricing plans for creating VMware virtual data centers. Virtual data centers incur charges for the following virtual data center resource usages:

* Storage allocations with tiered pricing based on storage performance
* Virtual CPU usage
* Virtual memory usage
* Egress on public networking
* Commercial operating system licenses used
* Third-party VMware services

| Plans | Description |
|:---------|:----------------------------|
| VMware Solutions Shared On-Demand | - The vCPU and RAM virtual data center are allocated based on the demand. Resources are not preallocated and in cases of large regional demand there can be delays in availability. <br/> - The limits that are established for the amount of vCPU and RAM are maximums. <br/> - vCPU and RAM resource limits can be increased and decreased later as required. <br/> - The cost is calculated hourly and it is based on the resource usage in the virtual data center. <br/> - There are no limits on the amount of storage that can be allocated and used in the virtual data center. Charges are hourly based on GB of allocated storage. <br/> - There are no limits on the amount of inbound and outbound public networking. Public bandwidth is charged per GB. |
| VMware Solutions Shared Reserved | - The vCPU and RAM virtual data center reservations are pre-allocated and their availability is guaranteed. <br/> - vCPU and RAM resources can be increased and decreased later as required. <br/> - There are no limits on the amount of storage that can be allocated and used in the virtual data center. Charges are hourly based on GB of allocated storage. <br/> - There are no limits on the amount of inbound and outbound public networking. Public bandwidth is charged per GB. |

## Cost Breakdown
{: #shared_pricing-cost}

### Terms
{: #shared_pricing-cost-terms}
<dl>
  <dt>Usage</dt>
  <dd>Metering is for the full potential size of the resource for the time period the resource is used. For example, if an On-Demand virtual data center is created with a resource limit of 100 vCPU and 800 GB of RAM, but it has no VMs running on it, there is no charge for the vCPU and RAM. If an 8 vCPU with 8 GB VM is started, metering is against the size of that VM. If the VM is using fewer than the full resources assigned to it, metering is applicable to the full size of the VM.</dd>
  <dt>Allocation</dt>
  <dd>Metering is appliacable to the full potential size of the resource for the life of the resource. For example, if a reserved virtual data center is created with a resource allocation of 100 vCPU and 800 GB of RAM, but it has no VMs running or even created on it, metering is applicable to 100 vCPU and 80 GB RAM.</dd>
  <dt>Monthly peak metric usage</dt>
  <dd>The maximum amount of the metric used over the period of the full month. For example, if a reserved virtual data center is created with 100 vCPU and 800 GB of RAM, then later in the month it is reduced to 50 vCPU and 400 GB RAM, the monthly peak usage is 100 vCPU and 800 GB RAM.</dd>
  <dt>Hourly peak metric usage</dt>
  <dd>The maximum amount of the metric used over the one hour period. For example, if 100 vCPU is used for one minute of the hour with 0 vCPU used for the other 59 mins, the hourly peak metric usage is 100 vCPU.</dd>
</dl>

### VMware Shared - On-Demand virtual data center billing plan
{: #shared_pricing-cost-ondemand}

Virtual data center resources are allocated as needed. Pricing is hourly based on the resource usage in the virtual data center. The following metrics are part of this plan.

| Metric                                   | Frequency | Description |
|:-----------------------------------------|:------------|:------------|
| MAX_BASE_COST | Monthly | Instance cost including the edge gateway with five IP addresses. |
| TOTAL_VCPU_HOURS | Hourly | The peak vCPU **usage** over the period of one hour. |
| TOTAL_RAM_GB_HOURS | Hourly | The peak memory **usage** over the period of one hour. |
| TOTAL_EGRESS_GB) | Usage | The **total** outbound public traffic is charged per GB transferred over the period of one hour. This includes public outbound traffic. |
| **Storage Metrics** |  |  |  |
| TOTAL_STORAGE_POINT_TWO_FIVE_IOPS_GB_HOUR | Hourly | The peak storage **allocation** at the 0.25 IOPS/GB tier over the period of one hour. |
| TOTAL_STORAGE_TWO_IOPS_GB_HOURS | Hourly | The peak storage **allocation** at the 2 IOPS/GB tier over the period of one hour. |
| TOTAL_STORAGE_FOUR_IOPS_GB_HOURS | Hourly | The peak storage **allocation** at the 4 IOPS/GB tier over the period of one hour. |
| TOTAL_STORAGE_TEN_IOPS_GB_HOURS | Hourly | The peak storage **allocation** at the 10 IOPS/GB tier over the period of one hour. |
| **OS License Usage** |  | | |
| MAX_WINDOWS_LICENSES | Monthly | The peak number of Windows license **usage** over the period of one month measured in one hour intervals. The largest number of licenses that are used at any period of time is the amount that is charged for the full month. |
{: caption="Table 1. On Demand virtual data center billing plan" caption-side="top"}

### VMware Shared - Reserved virtual data center billing plan
{: #shared_pricing-cost-reserved}

Virtual data center resources are preallocated and guaranteed. Pricing is monthly based on the allocation size of the virtual data center.

| Metric                                   | Frequency | Description |
|:-----------------------------------------|:------------|:------------|
| MAX_VCPU | Monthly | The peak vCPU **allocation** for the virtual data center over the period of one month. The peak vCPU metric is determined by the largest vCPU reservation value that is selected by the customer over a one month period. |
| MAX_RAM_GB | Monthly | The peak memory **allocation** for the virtual data center over the period of one month. The peak vCPU metric is determined by the largest memory reservation value that is selected by the customer over a one month period. |
| TOTAL_EGRESS_GB  | Usage | The **total** outbound public traffic is charged per GB transferred over the period of one month. This includes public outbound traffic through the virtual data center ESG and public outbound hybridity traffic. |
| **Storage Metrics** |  |  |
| TOTAL_STORAGE_POINT_TWO_FIVE_IOPS_GB_HOUR) | Hourly | The peak storage **allocation**  at the 0.25 IOPS/GB tier over the period of one hour. |
| TOTAL_STORAGE_TWO_IOPS_GB_HOURS | Hourly | The peak storage **allocation**  at the 2 IOPS/GB tier over the period of one hour. |
| TOTAL_STORAGE_FOUR_IOPS_GB_HOURS | Hourly | The peak storage **allocation**  at the 4 IOPS/GB tier over the period of one hour. |
| TOTAL_STORAGE_TEN_IOPS_GB_HOURS) | Hourly | The peak storage **allocation**  at the 10 IOPS/GB tier over the period of one hour. |
| **OS Metrics** | | | |
| MAX_WINDOWS_LICENSES | Monthly | The peak number of Windows licenses **usage** over the period of 1 month measured in 1 hour intervals. The largest number of licenses used at any period of time will be the amount charged for the full month. |
{: caption="Table 2. Reserved virtual data center billing plan" caption-side="top"}