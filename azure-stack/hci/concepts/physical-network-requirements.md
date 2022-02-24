---
title: Physical network requirements for Azure Stack HCI
description: Physical network requirements and considerations for Azure Stack HCI, including network switches.
author: jacobpedd
ms.topic: conceptual
ms.date: 11/10/2021
ms.author: jpeddicord
ms.reviewer: JasonGerend
---

# Physical network requirements for Azure Stack HCI

> Applies to: Azure Stack HCI, versions 21H2 and 20H2

This article discusses physical (fabric) network considerations and requirements for Azure Stack HCI, particularly for network switches.

> [!NOTE]
> Requirements for future Azure Stack HCI versions may change.

## Network switches for Azure Stack HCI

Microsoft tests Azure Stack HCI to the standards and protocols identified in the **Network switch requirements** section below. While Microsoft doesn't certify network switches, we do work with vendors to identify devices that support Azure Stack HCI requirements.

These requirements are also published in [Windows Hardware Compatibility Program Specifications and Policies](/windows-hardware/design/compatibility/whcp-specifications-policies).  Select **Download Specifications, Windows Server 2022**, open the ZIP file, open **Devices and Components WHCP Requirements for Windows Server 2022.pdf**, then see the **Device.Network.Switch.AzureStackHCI** section.

> [!IMPORTANT]
> While other network switches using technologies and protocols not listed here may work, Microsoft cannot guarantee they will work with Azure Stack HCI and may be unable to assist in troubleshooting issues that occur.

When purchasing network switches, contact your switch vendor and ensure that the devices meet all Azure Stack HCI requirements. The following vendors (in alphabetical order) have confirmed that their switches support Azure Stack HCI requirements:

| Vendor | 10 GbE | 25 GbE | 100 GbE | 400 GbE |
| -----  | -----  | -----  | -----   | -----   |
| Arista Networks <br><br>*EOS version of 4.26.2F or later is required* |[7050X3 series](https://www.arista.com/assets/data/pdf/Datasheets/7050X3-Datasheet.pdf), [7060X series](https://www.arista.com/assets/data/pdf/Datasheets/7060X_7260X_DS.pdf), [7260X3 series](https://www.arista.com/assets/data/pdf/Datasheets/7260X3_Datasheet.pdf), [7280R series](https://www.arista.com/assets/data/pdf/Datasheets/7280R-DataSheet.pdf), [7280R3 series](https://www.arista.com/assets/data/pdf/Datasheets/7280R3-Data-Sheet.pdf) | [7050X3 series](https://www.arista.com/assets/data/pdf/Datasheets/7050X3-Datasheet.pdf), [7060X series](https://www.arista.com/assets/data/pdf/Datasheets/7060X_7260X_DS.pdf), [7260X3 series](https://www.arista.com/assets/data/pdf/Datasheets/7260X3_Datasheet.pdf), [7280R series](https://www.arista.com/assets/data/pdf/Datasheets/7280R-DataSheet.pdf), [7280R3 series](https://www.arista.com/assets/data/pdf/Datasheets/7280R3-Data-Sheet.pdf) | [7050X3 series](https://www.arista.com/assets/data/pdf/Datasheets/7050X3-Datasheet.pdf), [7060X series](https://www.arista.com/assets/data/pdf/Datasheets/7060X_7260X_DS.pdf), [7260X3 series](https://www.arista.com/assets/data/pdf/Datasheets/7260X3_Datasheet.pdf), [7060X4 series](https://www.arista.com/assets/data/pdf/Datasheets/7060X4-Datasheet.pdf), [7280R series](https://www.arista.com/assets/data/pdf/Datasheets/7280R-DataSheet.pdf), [7280R3 series](https://www.arista.com/assets/data/pdf/Datasheets/7280R3-Data-Sheet.pdf) | [7050X3 series](https://www.arista.com/assets/data/pdf/Datasheets/7050X3-Datasheet.pdf), [7060X4 series](https://www.arista.com/assets/data/pdf/Datasheets/7060X4-Datasheet.pdf), [7280R3 series](https://www.arista.com/assets/data/pdf/Datasheets/7280R3-Data-Sheet.pdf) ||
| Dell   | [S41xx series](https://www.dell.com/learn/us/en/45/shared-content~data-sheets~en/documents~dell-emc-networking-s4100-series-spec-sheet.pdf) |[S52xx series](https://www.delltechnologies.com/resources/en-us/asset/data-sheets/products/networking/dell_emc_networking-s5200_on_spec_sheet.pdf) | [S52xx series](https://www.delltechnologies.com/resources/en-us/asset/data-sheets/products/networking/dell_emc_networking-s5200_on_spec_sheet.pdf) ||
| Juniper Networks <br><br>*Junos Software Service Release version 20.2R3-S2 or later is required* | [QFX5110 series](https://www.juniper.net/assets/es/es/local/pdf/datasheets/1000605-en.pdf), [QFX5120 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5120-ethernet-switch-datasheet.pdf), [QFX5200 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5200-switch-datasheet.pdf) | [QFX5120 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5120-ethernet-switch-datasheet.pdf), [QFX5200 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5200-switch-datasheet.pdf)  | [QFX5120 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5120-ethernet-switch-datasheet.pdf), [QFX5200 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5200-switch-datasheet.pdf), [QFX5210 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5210-switch-datasheet.pdf), [QFX5220 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5220-switch-datasheet.pdf)  | [QFX5130 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5130-switch.pdf), [QFX5220 series](https://www.juniper.net/content/dam/www/assets/datasheets/us/en/switches/qfx5220-switch-datasheet.pdf) ||
| Lenovo | [G8272](https://lenovopress.com/tips1267-lenovo-rackswitch-g8272), [NE1032](https://lenovopress.com/lp0605-thinksystem-ne1032-rackswitch)|[NE2572](https://lenovopress.com/lp0608-lenovo-thinksystem-ne2572-rackswitch) |[NE10032](https://lenovopress.com/lp0609-lenovo-thinksystem-ne10032-rackswitch) |

> [!IMPORTANT]
> We update this list as we're informed of changes by network switch vendors.

If your switch isn't included, contact your switch vendor to ensure that your switch model and the version of the switch's operating system supports the requirements in the next section.

## Network switch requirements

This section lists industry standards that are mandatory for network switches used in all Azure Stack HCI deployments. These standards help ensure reliable communications between nodes in Azure Stack HCI cluster deployments.

> [!NOTE]
> Network adapters used for compute, storage, and management traffic require Ethernet. For more information, see [Host network requirements](host-network-requirements.md).

Here are the mandatory IEEE standards and specifications:

### Standard: IEEE 802.1Q

Ethernet switches must comply with the IEEE 802.1Q specification that defines VLANs. VLANs are required for several aspects of Azure Stack HCI and are required in all scenarios.

### Standard: IEEE 802.1Qbb

Ethernet switches must comply with the IEEE 802.1Qbb specification that defines Priority Flow Control (PFC). PFC is required where Data Center Bridging (DCB) is used. Since DCB can be used in both RoCE and iWARP RDMA scenarios, 802.1Qbb is required in all scenarios. A minimum of three Class of Service (CoS) priorities are required without downgrading the switch capabilities or port speeds. At least one of these traffic classes must provide lossless communication.

### Standard: IEEE 802.1Qaz

Ethernet switches must comply with the IEEE 802.1Qaz specification that defines Enhanced Transmission Select (ETS). ETS is required where DCB is used. Since DCB can be used in both RoCE and iWARP RDMA scenarios, 802.1Qaz is required in all scenarios.

A minimum of three CoS priorities are required without downgrading the switch capabilities or port speed. Additionally, if your device allows ingress QoS rates to be defined, we recommend that you do not configure ingress rates or configure them to the exact same value as the egress (ETS) rates.

> [!NOTE]
> Hyper-converged infrastructure has a high reliance on East-West Layer-2 communication within the same rack and therefore requires ETS. Microsoft doesn't test Azure Stack HCI with Differentiated Services Code Point (DSCP).


### Standard: IEEE 802.1AB

Ethernet switches must comply with the IEEE 802.1AB specification that defines the Link Layer Discovery Protocol (LLDP). LLDP is required for Azure Stack HCI and enables troubleshooting of physical networking configurations.

Configuration of the LLDP Type-Length-Values (TLVs) must be dynamically enabled. Switches must not require additional configuration beyond enablement of a specific TLV. For example, enabling 802.1 Subtype 3 should automatically advertise all VLANs available on switch ports.

### Custom TLV requirements

LLDP allows organizations to define and encode their own custom TLVs. These are called Organizationally Specific TLVs. All Organizationally Specific TLVs start with an LLDP TLV Type value of 127. The following table shows which Organizationally Specific Custom TLV (TLV Type 127) subtypes are required:

|Version required|Organization|TLV Subtype|
|-----|-----|-----|
|20H2 and later|IEEE 802.1|VLAN Name (Subtype = 3)|
|20H2 and later|IEEE 802.3|Maximum Frame Size (Subtype = 4)|

## Network traffic and architecture

This section is predominantly for network administrators.

Azure Stack HCI can function in various data center architectures including 2-tier (Spine-Leaf) and 3-tier (Core-Aggregation-Access). This section refers more to concepts from the Spine-Leaf topology that is commonly used with workloads in hyper-converged infrastructure such as Azure Stack HCI.

## Network models

Network traffic can be classified by its direction. Traditional Storage Area Network (SAN) environments are heavily North-South where traffic flows from a compute tier to a storage tier across a Layer-3 (IP) boundary. Hyperconverged infrastructure is more heavily East-West where a substantial portion of traffic stays within a Layer-2 (VLAN) boundary.

> [!IMPORTANT]
> Between nodes within an Azure Stack HCI a high-performance and low latency connection is exspected. Which means that the latency between nodes must be beneath one millisecond and a minimum connection bandwidth of 25 Gbit/s or larger is required. It is also require to provide synchronous latency between als cluster nodes. We still highly recommend that all cluster nodes in a site are physically located in the same rack and connected to the same top-of-rack (ToR) switches.

### North-South traffic for Azure Stack HCI

North-South traffic has the following characteristics:

- Traffic flows out of a ToR switch to the spine or in from the spine to a ToR switch
- Traffic leaves the physical rack or crosses a Layer-3 boundary (IP)
- Includes management (PowerShell, Windows Admin Center), compute (VM), and inter-site stretched cluster traffic
- Uses an Ethernet switch for connectivity to the physical network

### East-West traffic for Azure Stack HCI

East-West traffic has the following characteristics:

- Traffic remains within the ToR switches and Layer-2 boundary (VLAN)
- Includes storage traffic or Live Migration traffic between nodes in the same cluster and (if using a stretched cluster) within the same site
- May use an Ethernet switch (switched) or a direct (switchless) connection, as described in the next two sections.

## Using switches

North-South traffic requires the use of switches. Besides using an Ethernet switch that supports the required protocols for Azure Stack HCI, the most important aspect is the proper sizing of the network fabric.

It is imperative to understand the "non-blocking" fabric bandwidth that your Ethernet switches can support and that you minimize (or preferably eliminate) oversubscription of the network.

Common congestion points and oversubscription, such as the [Multi-Chassis Link Aggregation Group](https://en.wikipedia.org/wiki/Multi-chassis_link_aggregation_group) used for path redundancy, can be eliminated through proper use of subnets and VLANs. Also see [Host network requirements](host-network-requirements.md).

Work with your network vendor or network support team to ensure your network switches have been properly sized for the workload you are intending to run.

## Using switchless

Azure Stack HCI supports switchless (direct) connections for East-West traffic for all cluster sizes so long as each node in the cluster has a redundant connection to every node in the cluster. This is called a "full-mesh" connection.

:::image type="content" source="media/plan-networking/switchless-connectivity.png" alt-text="Diagram showing full-mesh switchless connectivity" lightbox="media/plan-networking/switchless-connectivity.png":::

|Interface pair|Subnet|VLAN|
|---|---|---|
|Mgmt host vNIC|Customer-specific|Customer-specific|
|SMB01|192.168.71.x/24|711|
|SMB02|192.168.72.x/24|712|
|SMB03|192.168.73.x/24|713|

> [!NOTE]
>The benefits of switchless deployments diminish with clusters larger than three-nodes due to the number of network adapters required.

### Advantages of switchless connections

- No switch purchase is necessary for East-West traffic. A switch is required for North-South traffic. This may result in lower capital expenditure (CAPEX) costs but is dependent on the number of nodes in the cluster.
- Because there is no switch, configuration is limited to the host, which may reduce the potential number of configuration steps needed. This value diminishes as the cluster size increases.

### Disadvantages of switchless connections

- More planning is required for IP and subnet addressing schemes.
- Provides only local storage access. Management traffic, VM traffic, and other traffic requiring North-South access cannot use these adapters.
- As the number of nodes in the cluster grows, the cost of network adapters could exceed the cost of using network switches.
- Doesn't scale well beyond three-node clusters. More nodes incur additional cabling and configuration that can surpass the complexity of using a switch.
- Cluster expansion is complex requiring hardware and software configuration changes.

## Next steps

- Learn about network adapter and host requirements. See [Host network requirements](host-network-requirements.md).
- Brush up on failover clustering basics. See [Failover Clustering Networking Basics](https://techcommunity.microsoft.com/t5/failover-clustering/.failover-clustering-networking-basics-and-fundamentals/ba-p/1706005?s=09).
- Brush up on using SET. See [Remote Direct Memory Access (RDMA) and Switch Embedded Teaming (SET)](/windows-server/virtualization/hyper-v-virtual-switch/rdma-and-switch-embedded-teaming).
- For deployment, see [Create a cluster using Windows Admin Center](../deploy/create-cluster.md).
- For deployment, see [Create a cluster using Windows PowerShell](../deploy/create-cluster-powershell.md).
