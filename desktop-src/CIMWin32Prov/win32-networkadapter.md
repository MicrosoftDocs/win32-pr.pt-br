---
description: A \_ classe Win32 adaptador foi preterida. \_Em vez disso, use a classe MSFT netadapter. A \_ classe Win32 NetworkAdapterWMI representa um adaptador de rede de um computador que executa um sistema operacional Windows.
ms.assetid: f79cb2a1-a249-479d-a495-37a44fdea995
ms.tgt_platform: multiple
title: Classe Win32_NetworkAdapter
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Win32_NetworkAdapter
- Win32_NetworkAdapter.Reset
- Win32_NetworkAdapter.SetPowerState
- Win32_NetworkAdapter.AdapterType
- Win32_NetworkAdapter.AdapterTypeID
- Win32_NetworkAdapter.AutoSense
- Win32_NetworkAdapter.Availability
- Win32_NetworkAdapter.Caption
- Win32_NetworkAdapter.ConfigManagerErrorCode
- Win32_NetworkAdapter.ConfigManagerUserConfig
- Win32_NetworkAdapter.CreationClassName
- Win32_NetworkAdapter.Description
- Win32_NetworkAdapter.DeviceID
- Win32_NetworkAdapter.ErrorCleared
- Win32_NetworkAdapter.ErrorDescription
- Win32_NetworkAdapter.GUID
- Win32_NetworkAdapter.Index
- Win32_NetworkAdapter.InstallDate
- Win32_NetworkAdapter.Installed
- Win32_NetworkAdapter.InterfaceIndex
- Win32_NetworkAdapter.LastErrorCode
- Win32_NetworkAdapter.MACAddress
- Win32_NetworkAdapter.Manufacturer
- Win32_NetworkAdapter.MaxNumberControlled
- Win32_NetworkAdapter.MaxSpeed
- Win32_NetworkAdapter.Name
- Win32_NetworkAdapter.NetConnectionID
- Win32_NetworkAdapter.NetConnectionStatus
- Win32_NetworkAdapter.NetEnabled
- Win32_NetworkAdapter.NetworkAddresses
- Win32_NetworkAdapter.PermanentAddress
- Win32_NetworkAdapter.PhysicalAdapter
- Win32_NetworkAdapter.PNPDeviceID
- Win32_NetworkAdapter.PowerManagementCapabilities
- Win32_NetworkAdapter.PowerManagementSupported
- Win32_NetworkAdapter.ProductName
- Win32_NetworkAdapter.ServiceName
- Win32_NetworkAdapter.Speed
- Win32_NetworkAdapter.Status
- Win32_NetworkAdapter.StatusInfo
- Win32_NetworkAdapter.SystemCreationClassName
- Win32_NetworkAdapter.SystemName
- Win32_NetworkAdapter.TimeOfLastReset
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 22718802370995cc0515e3f63e731cc86d37eb0f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457144"
---
# <a name="win32_networkadapter-class"></a><span data-ttu-id="1d195-105">\_Classe Win32 adaptador</span><span class="sxs-lookup"><span data-stu-id="1d195-105">Win32\_NetworkAdapter class</span></span>

<span data-ttu-id="1d195-106">A classe **Win32 \_ adaptador** foi preterida.</span><span class="sxs-lookup"><span data-stu-id="1d195-106">The **Win32\_NetworkAdapter** class is deprecated.</span></span> <span data-ttu-id="1d195-107">Em vez disso, use a classe [**MSFT \_ netadapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1d195-107">Use the [**MSFT\_NetAdapter**](/previous-versions/windows/desktop/legacy/hh968170(v=vs.85)) class instead.</span></span> <span data-ttu-id="1d195-108">A [classe WMI](../wmisdk/retrieving-a-class.md) **\_ adaptador do Win32** representa um adaptador de rede de um computador que executa um sistema operacional Windows.</span><span class="sxs-lookup"><span data-stu-id="1d195-108">The **Win32\_NetworkAdapter**[WMI class](../wmisdk/retrieving-a-class.md) represents a network adapter of a computer running a Windows operating system.</span></span>

<span data-ttu-id="1d195-109">**Win32 \_ Adaptador** fornece apenas dados IPv4.</span><span class="sxs-lookup"><span data-stu-id="1d195-109">**Win32\_NetworkAdapter** only supplies IPv4 data.</span></span> <span data-ttu-id="1d195-110">Para obter mais informações, consulte [suporte a IPv6 e IPv4 no WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-110">For more information, see [IPv6 and IPv4 Support in WMI](../wmisdk/ipv6-and-ipv4-support-in-wmi.md).</span></span>

<span data-ttu-id="1d195-111">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="1d195-111">The following syntax is simplified from Managed Object Format (MOF) code and includes all of the inherited properties.</span></span> <span data-ttu-id="1d195-112">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="1d195-112">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d195-113">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d195-113">Syntax</span></span>

``` syntax
[Dynamic, Provider("CIMWin32"), UUID("{8502C4C0-5FBB-11D2-AAC1-006008C78BC7}"), AMENDMENT]
class Win32_NetworkAdapter : CIM_NetworkAdapter
{
  string   AdapterType;
  uint16   AdapterTypeID;
  boolean  AutoSense;
  uint16   Availability;
  string   Caption;
  uint32   ConfigManagerErrorCode;
  boolean  ConfigManagerUserConfig;
  string   CreationClassName;
  string   Description;
  string   DeviceID;
  boolean  ErrorCleared;
  string   ErrorDescription;
  string   GUID;
  uint32   Index;
  datetime InstallDate;
  boolean  Installed;
  uint32   InterfaceIndex;
  uint32   LastErrorCode;
  string   MACAddress;
  string   Manufacturer;
  uint32   MaxNumberControlled;
  uint64   MaxSpeed;
  string   Name;
  string   NetConnectionID;
  uint16   NetConnectionStatus;
  boolean  NetEnabled;
  string   NetworkAddresses[];
  string   PermanentAddress;
  boolean  PhysicalAdapter;
  string   PNPDeviceID;
  uint16   PowerManagementCapabilities[];
  boolean  PowerManagementSupported;
  string   ProductName;
  string   ServiceName;
  uint64   Speed;
  string   Status;
  uint16   StatusInfo;
  string   SystemCreationClassName;
  string   SystemName;
  datetime TimeOfLastReset;
};
```

## <a name="members"></a><span data-ttu-id="1d195-114">Membros</span><span class="sxs-lookup"><span data-stu-id="1d195-114">Members</span></span>

<span data-ttu-id="1d195-115">A classe **Win32 \_ adaptador** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="1d195-115">The **Win32\_NetworkAdapter** class has these types of members:</span></span>

-   [<span data-ttu-id="1d195-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d195-116">Methods</span></span>](#methods)
-   [<span data-ttu-id="1d195-117">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1d195-117">Properties</span></span>](#properties)

### <a name="methods"></a><span data-ttu-id="1d195-118">Métodos</span><span class="sxs-lookup"><span data-stu-id="1d195-118">Methods</span></span>

<span data-ttu-id="1d195-119">A classe **Win32 \_ adaptador** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="1d195-119">The **Win32\_NetworkAdapter** class has these methods.</span></span>



| <span data-ttu-id="1d195-120">Método</span><span class="sxs-lookup"><span data-stu-id="1d195-120">Method</span></span>                                                          | <span data-ttu-id="1d195-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d195-121">Description</span></span>                                                                                                                                                                                                                     |
|:----------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1d195-122">**Desabilitar**</span><span class="sxs-lookup"><span data-stu-id="1d195-122">**Disable**</span></span>](disable-method-in-class-win32-networkadapter.md) | <span data-ttu-id="1d195-123">Desabilita o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-123">Disables the network adapter.</span></span><br/>                                                                                                                                                                                        |
| [<span data-ttu-id="1d195-124">**Habilitar**</span><span class="sxs-lookup"><span data-stu-id="1d195-124">**Enable**</span></span>](enable-method-in-class-win32-networkadapter.md)   | <span data-ttu-id="1d195-125">Habilita o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-125">Enables the network adapter.</span></span><br/>                                                                                                                                                                                         |
| <span data-ttu-id="1d195-126">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="1d195-126">**Reset**</span></span>                                                       | <span data-ttu-id="1d195-127">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="1d195-127">Not implemented.</span></span> <span data-ttu-id="1d195-128">Para obter mais informações sobre como implementar esse método, consulte o método [**Reset**](reset-method-in-class-cim-controller.md) no [**CIM \_ adaptador**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-128">For more information about how to implement this method, see the [**Reset**](reset-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/>                 |
| <span data-ttu-id="1d195-129">**SetPowerState**</span><span class="sxs-lookup"><span data-stu-id="1d195-129">**SetPowerState**</span></span>                                               | <span data-ttu-id="1d195-130">Não implementado.</span><span class="sxs-lookup"><span data-stu-id="1d195-130">Not implemented.</span></span> <span data-ttu-id="1d195-131">Para obter mais informações sobre como implementar esse método, consulte o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) no [**CIM \_ adaptador**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-131">For more information about how to implement this method, see the [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method in [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span><br/> |



 

### <a name="properties"></a><span data-ttu-id="1d195-132">Propriedades</span><span class="sxs-lookup"><span data-stu-id="1d195-132">Properties</span></span>

<span data-ttu-id="1d195-133">A classe **Win32 \_ adaptador** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="1d195-133">The **Win32\_NetworkAdapter** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="1d195-134">**AdapterType**</span><span class="sxs-lookup"><span data-stu-id="1d195-134">**AdapterType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-135">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-135">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-136">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-136">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-137">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ Gen \_ Media \_ em \_ uso](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="1d195-137">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-138">Mídia de rede em uso.</span><span class="sxs-lookup"><span data-stu-id="1d195-138">Network medium in use.</span></span> <span data-ttu-id="1d195-139">Os adaptadores de rede são os seguintes:</span><span class="sxs-lookup"><span data-stu-id="1d195-139">The network adapters are as follows:</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="1d195-140">**Ethernet 802,3** ("Ethernet 802,3")</span><span class="sxs-lookup"><span data-stu-id="1d195-140">**Ethernet 802.3** ("Ethernet 802.3")</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="1d195-141">**Token ring 802,5** ("token ring 802,5")</span><span class="sxs-lookup"><span data-stu-id="1d195-141">**Token Ring 802.5** ("Token Ring 802.5")</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="1d195-142">**Fiber Distributed data interface (FDDI)** ("Fiber Distributed data interface (FDDI)")</span><span class="sxs-lookup"><span data-stu-id="1d195-142">**Fiber Distributed Data Interface (FDDI)** ("Fiber Distributed Data Interface (FDDI)")</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="1d195-143">**Rede de longa distância (WAN)** ("rede de longa distância (WAN)")</span><span class="sxs-lookup"><span data-stu-id="1d195-143">**Wide Area Network (WAN)** ("Wide Area Network (WAN)")</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="1d195-144">**LocalTalk** ("LocalTalk")</span><span class="sxs-lookup"><span data-stu-id="1d195-144">**LocalTalk** ("LocalTalk")</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="1d195-145">**Ethernet usando o formato de cabeçalho Dix** ("Ethernet usando o formato de cabeçalho Dix")</span><span class="sxs-lookup"><span data-stu-id="1d195-145">**Ethernet using DIX header format** ("Ethernet using DIX header format")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="1d195-146">**ARCnet** ("ARCnet")</span><span class="sxs-lookup"><span data-stu-id="1d195-146">**ARCNET** ("ARCNET")</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="1d195-147">**ARCnet (878,2)** ("ARCNET (878,2)")</span><span class="sxs-lookup"><span data-stu-id="1d195-147">**ARCNET (878.2)** ("ARCNET (878.2)")</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="1d195-148">**ATM** ("ATM")</span><span class="sxs-lookup"><span data-stu-id="1d195-148">**ATM** ("ATM")</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="1d195-149">**Sem fio** ("sem fio")</span><span class="sxs-lookup"><span data-stu-id="1d195-149">**Wireless** ("Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="1d195-150">**Infravermelho sem fio** ("infravermelho sem fio")</span><span class="sxs-lookup"><span data-stu-id="1d195-150">**Infrared Wireless** ("Infrared Wireless")</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="1d195-151">**BPC** ("BPC")</span><span class="sxs-lookup"><span data-stu-id="1d195-151">**Bpc** ("Bpc")</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="1d195-152">**CoWan** ("CoWan")</span><span class="sxs-lookup"><span data-stu-id="1d195-152">**CoWan** ("CoWan")</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="1d195-153">**1394** ("1394")</span><span class="sxs-lookup"><span data-stu-id="1d195-153">**1394** ("1394")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d195-154">**AdapterTypeID**</span><span class="sxs-lookup"><span data-stu-id="1d195-154">**AdapterTypeID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-155">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d195-155">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-156">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-156">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-157">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID \_ Gen \_ Media \_ em \_ uso](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span><span class="sxs-lookup"><span data-stu-id="1d195-157">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)::[OID\_GEN\_MEDIA\_IN\_USE](/windows-hardware/drivers/network/oid-gen-media-in-use)")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-158">Mídia de rede em uso.</span><span class="sxs-lookup"><span data-stu-id="1d195-158">Network medium in use.</span></span> <span data-ttu-id="1d195-159">Retorna as mesmas informações que a propriedade **AdapterType** , exceto que as informações estão na forma de um inteiro.</span><span class="sxs-lookup"><span data-stu-id="1d195-159">Returns the same information as the **AdapterType** property, except that the information is in the form of an integer.</span></span>

<dt>

<span id="Ethernet_802.3"></span><span id="ethernet_802.3"></span><span id="ETHERNET_802.3"></span>

<span data-ttu-id="1d195-160">**Ethernet 802,3** (0)</span><span class="sxs-lookup"><span data-stu-id="1d195-160">**Ethernet 802.3** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring_802.5"></span><span id="token_ring_802.5"></span><span id="TOKEN_RING_802.5"></span>

<span data-ttu-id="1d195-161">**Token Ring 802,5** (1)</span><span class="sxs-lookup"><span data-stu-id="1d195-161">**Token Ring 802.5** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Fiber_Distributed_Data_Interface__FDDI_"></span><span id="fiber_distributed_data_interface__fddi_"></span><span id="FIBER_DISTRIBUTED_DATA_INTERFACE__FDDI_"></span>

<span data-ttu-id="1d195-162">**Fiber Distributed data interface (FDDI)** (2)</span><span class="sxs-lookup"><span data-stu-id="1d195-162">**Fiber Distributed Data Interface (FDDI)** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Wide_Area_Network__WAN_"></span><span id="wide_area_network__wan_"></span><span id="WIDE_AREA_NETWORK__WAN_"></span>

<span data-ttu-id="1d195-163">**WAN (rede de longa distância)** (3)</span><span class="sxs-lookup"><span data-stu-id="1d195-163">**Wide Area Network (WAN)** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="LocalTalk"></span><span id="localtalk"></span><span id="LOCALTALK"></span>

<span data-ttu-id="1d195-164">**LocalTalk** (4)</span><span class="sxs-lookup"><span data-stu-id="1d195-164">**LocalTalk** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet_using_DIX_header_format"></span><span id="ethernet_using_dix_header_format"></span><span id="ETHERNET_USING_DIX_HEADER_FORMAT"></span>

<span data-ttu-id="1d195-165">**Ethernet usando o formato de cabeçalho Dix** (5)</span><span class="sxs-lookup"><span data-stu-id="1d195-165">**Ethernet using DIX header format** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET"></span><span id="arcnet"></span>

<span data-ttu-id="1d195-166">**ARCnet** (6)</span><span class="sxs-lookup"><span data-stu-id="1d195-166">**ARCNET** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="ARCNET__878.2_"></span><span id="arcnet__878.2_"></span>

<span data-ttu-id="1d195-167">**ARCnet (878,2)** (7)</span><span class="sxs-lookup"><span data-stu-id="1d195-167">**ARCNET (878.2)** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="1d195-168">**ATM** (8)</span><span class="sxs-lookup"><span data-stu-id="1d195-168">**ATM** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless"></span><span id="wireless"></span><span id="WIRELESS"></span>

<span data-ttu-id="1d195-169">**Sem fio** (9)</span><span class="sxs-lookup"><span data-stu-id="1d195-169">**Wireless** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared_Wireless"></span><span id="infrared_wireless"></span><span id="INFRARED_WIRELESS"></span>

<span data-ttu-id="1d195-170">**Infravermelho sem fio** (10)</span><span class="sxs-lookup"><span data-stu-id="1d195-170">**Infrared Wireless** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Bpc"></span><span id="bpc"></span><span id="BPC"></span>

<span data-ttu-id="1d195-171">**BPC** (11)</span><span class="sxs-lookup"><span data-stu-id="1d195-171">**Bpc** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="CoWan"></span><span id="cowan"></span><span id="COWAN"></span>

<span data-ttu-id="1d195-172">**CoWan** (12)</span><span class="sxs-lookup"><span data-stu-id="1d195-172">**CoWan** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="1394"></span>

<span data-ttu-id="1d195-173">**1394** (13)</span><span class="sxs-lookup"><span data-stu-id="1d195-173">**1394** (13)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d195-174">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="1d195-174">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-175">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d195-175">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-176">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-176">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-177">Se **for true**, o adaptador de rede poderá determinar automaticamente a velocidade da mídia de rede ou conectada.</span><span class="sxs-lookup"><span data-stu-id="1d195-177">If **True**, the network adapter can automatically determine the speed of the attached or network media.</span></span>

<span data-ttu-id="1d195-178">Essa propriedade é herdada do [**CIM \_ adaptador**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-178">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="1d195-179">Esta propriedade ainda não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="1d195-179">This property has not been implemented yet.</span></span> <span data-ttu-id="1d195-180">Ele retorna um valor **nulo** por padrão.</span><span class="sxs-lookup"><span data-stu-id="1d195-180">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-181">**Disponibilidade**</span><span class="sxs-lookup"><span data-stu-id="1d195-181">**Availability**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-182">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d195-182">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-183">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-183">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-184">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,5 "," MIB. IETF \| host-REsources-MIB. hrDeviceStatus ")</span><span class="sxs-lookup"><span data-stu-id="1d195-184">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.5", "MIB.IETF\|HOST-RESOURCES-MIB.hrDeviceStatus")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-185">Disponibilidade e status do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d195-185">Availability and status of the device.</span></span>

<span data-ttu-id="1d195-186">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-186">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d195-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d195-187"><span id="Other"></span><span id="other"></span><span id="OTHER"></span>**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d195-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d195-188"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>

<span data-ttu-id="1d195-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Execução/energia completa** (3)</span><span class="sxs-lookup"><span data-stu-id="1d195-189"><span id="Running_Full_Power"></span><span id="running_full_power"></span><span id="RUNNING_FULL_POWER"></span>**Running/Full Power** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-190">Energia completa ou em execução</span><span class="sxs-lookup"><span data-stu-id="1d195-190">Running or Full Power</span></span>

</dd> <dt>

<span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>

<span data-ttu-id="1d195-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Aviso** (4)</span><span class="sxs-lookup"><span data-stu-id="1d195-191"><span id="Warning"></span><span id="warning"></span><span id="WARNING"></span>**Warning** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>

<span data-ttu-id="1d195-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**Em teste** (5)</span><span class="sxs-lookup"><span data-stu-id="1d195-192"><span id="In_Test"></span><span id="in_test"></span><span id="IN_TEST"></span>**In Test** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1d195-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Não aplicável** (6)</span><span class="sxs-lookup"><span data-stu-id="1d195-193"><span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>**Not Applicable** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>

<span data-ttu-id="1d195-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Desligar (7** )</span><span class="sxs-lookup"><span data-stu-id="1d195-194"><span id="Power_Off"></span><span id="power_off"></span><span id="POWER_OFF"></span>**Power Off** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>

<span data-ttu-id="1d195-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off line** (8)</span><span class="sxs-lookup"><span data-stu-id="1d195-195"><span id="Off_Line"></span><span id="off_line"></span><span id="OFF_LINE"></span>**Off Line** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>

<span data-ttu-id="1d195-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Fora do imposto** (9)</span><span class="sxs-lookup"><span data-stu-id="1d195-196"><span id="Off_Duty"></span><span id="off_duty"></span><span id="OFF_DUTY"></span>**Off Duty** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d195-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degradado** (10)</span><span class="sxs-lookup"><span data-stu-id="1d195-197"><span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>**Degraded** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>

<span data-ttu-id="1d195-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Não instalado** (11)</span><span class="sxs-lookup"><span data-stu-id="1d195-198"><span id="Not_Installed"></span><span id="not_installed"></span><span id="NOT_INSTALLED"></span>**Not Installed** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>

<span data-ttu-id="1d195-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Erro de instalação** (12)</span><span class="sxs-lookup"><span data-stu-id="1d195-199"><span id="Install_Error"></span><span id="install_error"></span><span id="INSTALL_ERROR"></span>**Install Error** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>

<span data-ttu-id="1d195-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>Economia **de energia-desconhecido** (13)</span><span class="sxs-lookup"><span data-stu-id="1d195-200"><span id="Power_Save_-_Unknown"></span><span id="power_save_-_unknown"></span><span id="POWER_SAVE_-_UNKNOWN"></span>**Power Save - Unknown** (13)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-201">O dispositivo é conhecido por estar em um estado de economia de energia, mas seu status exato é desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1d195-201">The device is known to be in a power save state, but its exact status is unknown.</span></span>

</dd> <dt>

<span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>

<span data-ttu-id="1d195-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>Economia **de energia-modo de baixa energia** (14)</span><span class="sxs-lookup"><span data-stu-id="1d195-202"><span id="Power_Save_-_Low_Power_Mode"></span><span id="power_save_-_low_power_mode"></span><span id="POWER_SAVE_-_LOW_POWER_MODE"></span>**Power Save - Low Power Mode** (14)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-203">O dispositivo está em um estado de economia de energia, mas ainda está funcionando e pode exibir o desempenho degradado.</span><span class="sxs-lookup"><span data-stu-id="1d195-203">The device is in a power save state, but still functioning, and may exhibit degraded performance.</span></span>

</dd> <dt>

<span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>

<span data-ttu-id="1d195-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save-em espera** (15)</span><span class="sxs-lookup"><span data-stu-id="1d195-204"><span id="Power_Save_-_Standby"></span><span id="power_save_-_standby"></span><span id="POWER_SAVE_-_STANDBY"></span>**Power Save - Standby** (15)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-205">O dispositivo não está funcionando, mas pode ser levado a uma potência completa rapidamente.</span><span class="sxs-lookup"><span data-stu-id="1d195-205">The device is not functioning, but could be brought to full power quickly.</span></span>

</dd> <dt>

<span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>

<span data-ttu-id="1d195-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Ciclo de energia** (16)</span><span class="sxs-lookup"><span data-stu-id="1d195-206"><span id="Power_Cycle"></span><span id="power_cycle"></span><span id="POWER_CYCLE"></span>**Power Cycle** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>

<span data-ttu-id="1d195-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>Economia **de energia-aviso** (17)</span><span class="sxs-lookup"><span data-stu-id="1d195-207"><span id="Power_Save_-_Warning"></span><span id="power_save_-_warning"></span><span id="POWER_SAVE_-_WARNING"></span>**Power Save - Warning** (17)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-208">O dispositivo está em um estado de aviso, embora também esteja em um estado de economia de energia.</span><span class="sxs-lookup"><span data-stu-id="1d195-208">The device is in a warning state, though also in a power save state.</span></span>

</dd> <dt>

<span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>

<span data-ttu-id="1d195-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>Em **pausa** (18)</span><span class="sxs-lookup"><span data-stu-id="1d195-209"><span id="Paused"></span><span id="paused"></span><span id="PAUSED"></span>**Paused** (18)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-210">O dispositivo está em pausa.</span><span class="sxs-lookup"><span data-stu-id="1d195-210">The device is paused.</span></span>

</dd> <dt>

<span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>

<span data-ttu-id="1d195-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Não pronto** (19)</span><span class="sxs-lookup"><span data-stu-id="1d195-211"><span id="Not_Ready"></span><span id="not_ready"></span><span id="NOT_READY"></span>**Not Ready** (19)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-212">O dispositivo não está pronto.</span><span class="sxs-lookup"><span data-stu-id="1d195-212">The device is not ready.</span></span>

</dd> <dt>

<span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>

<span data-ttu-id="1d195-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Não configurado** (20)</span><span class="sxs-lookup"><span data-stu-id="1d195-213"><span id="Not_Configured"></span><span id="not_configured"></span><span id="NOT_CONFIGURED"></span>**Not Configured** (20)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-214">O dispositivo não está configurado.</span><span class="sxs-lookup"><span data-stu-id="1d195-214">The device is not configured.</span></span>

</dd> <dt>

<span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>

<span data-ttu-id="1d195-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Desativado** (21)</span><span class="sxs-lookup"><span data-stu-id="1d195-215"><span id="Quiesced"></span><span id="quiesced"></span><span id="QUIESCED"></span>**Quiesced** (21)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-216">O dispositivo está silencioso.</span><span class="sxs-lookup"><span data-stu-id="1d195-216">The device is quiet.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d195-217">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="1d195-217">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-218">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-218">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-219">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-219">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-220">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span><span class="sxs-lookup"><span data-stu-id="1d195-220">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Caption")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-221">Breve descrição do objeto — uma cadeia de caracteres de uma linha.</span><span class="sxs-lookup"><span data-stu-id="1d195-221">Short description of the object—a one-line string.</span></span>

<span data-ttu-id="1d195-222">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-222">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-223">**ConfigManagerErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1d195-223">**ConfigManagerErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-224">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d195-224">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-225">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-225">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-226">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d195-226">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-227">Código de erro do Windows Configuration Manager.</span><span class="sxs-lookup"><span data-stu-id="1d195-227">Windows Configuration Manager error code.</span></span>

<span data-ttu-id="1d195-228">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-228">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="This_device_is_working_properly."></span><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>

<span data-ttu-id="1d195-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**Este dispositivo está funcionando corretamente.**</span><span class="sxs-lookup"><span data-stu-id="1d195-229"><span id="this_device_is_working_properly."></span><span id="THIS_DEVICE_IS_WORKING_PROPERLY."></span>**This device is working properly.**</span></span> <span data-ttu-id="1d195-230"> acima (0)</span><span class="sxs-lookup"><span data-stu-id="1d195-230">(0)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-231">O dispositivo está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d195-231">Device is working properly.</span></span>

</dd> <dt>

<span id="This_device_is_not_configured_correctly."></span><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>

<span data-ttu-id="1d195-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**Este dispositivo não está configurado corretamente.**</span><span class="sxs-lookup"><span data-stu-id="1d195-232"><span id="this_device_is_not_configured_correctly."></span><span id="THIS_DEVICE_IS_NOT_CONFIGURED_CORRECTLY."></span>**This device is not configured correctly.**</span></span> <span data-ttu-id="1d195-233">(1)</span><span class="sxs-lookup"><span data-stu-id="1d195-233">(1)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-234">O dispositivo não está configurado corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d195-234">Device is not configured correctly.</span></span>

</dd> <dt>

<span id="Windows_cannot_load_the_driver_for_this_device."></span><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d195-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**O Windows não pode carregar o driver para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d195-235"><span id="windows_cannot_load_the_driver_for_this_device."></span><span id="WINDOWS_CANNOT_LOAD_THE_DRIVER_FOR_THIS_DEVICE."></span>**Windows cannot load the driver for this device.**</span></span> <span data-ttu-id="1d195-236">(2)</span><span class="sxs-lookup"><span data-stu-id="1d195-236">(2)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>

<span data-ttu-id="1d195-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.**</span><span class="sxs-lookup"><span data-stu-id="1d195-237"><span id="the_driver_for_this_device_might_be_corrupted__or_your_system_may_be_running_low_on_memory_or_other_resources."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_MIGHT_BE_CORRUPTED__OR_YOUR_SYSTEM_MAY_BE_RUNNING_LOW_ON_MEMORY_OR_OTHER_RESOURCES."></span>**The driver for this device might be corrupted, or your system may be running low on memory or other resources.**</span></span> <span data-ttu-id="1d195-238">(3)</span><span class="sxs-lookup"><span data-stu-id="1d195-238">(3)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-239">O driver para este dispositivo pode estar corrompido ou o sistema pode estar com pouca memória ou outros recursos.</span><span class="sxs-lookup"><span data-stu-id="1d195-239">Driver for this device might be corrupted, or the system may be low on memory or other resources.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1d195-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Este dispositivo não está funcionando corretamente. Um de seus drivers ou seu registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="1d195-240"><span id="This_device_is_not_working_properly._One_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="this_device_is_not_working_properly._one_of_its_drivers_or_your_registry_might_be_corrupted."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY._ONE_OF_ITS_DRIVERS_OR_YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**This device is not working properly. One of its drivers or your registry might be corrupted.**</span></span> <span data-ttu-id="1d195-241">(4)</span><span class="sxs-lookup"><span data-stu-id="1d195-241">(4)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-242">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d195-242">Device is not working properly.</span></span> <span data-ttu-id="1d195-243">Um de seus drivers ou o registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="1d195-243">One of its drivers or the registry might be corrupted.</span></span>

</dd> <dt>

<span id="The_driver_for_this_device_needs_a_resource_that_Windows_cannot_manage."></span><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>

<span data-ttu-id="1d195-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**O driver para este dispositivo precisa de um recurso que o Windows não possa gerenciar.**</span><span class="sxs-lookup"><span data-stu-id="1d195-244"><span id="the_driver_for_this_device_needs_a_resource_that_windows_cannot_manage."></span><span id="THE_DRIVER_FOR_THIS_DEVICE_NEEDS_A_RESOURCE_THAT_WINDOWS_CANNOT_MANAGE."></span>**The driver for this device needs a resource that Windows cannot manage.**</span></span> <span data-ttu-id="1d195-245">(5)</span><span class="sxs-lookup"><span data-stu-id="1d195-245">(5)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-246">O driver para o dispositivo requer um recurso que o Windows não pode gerenciar.</span><span class="sxs-lookup"><span data-stu-id="1d195-246">Driver for the device requires a resource that Windows cannot manage.</span></span>

</dd> <dt>

<span id="The_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>

<span data-ttu-id="1d195-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**A configuração de inicialização para este dispositivo está em conflito com outros dispositivos.**</span><span class="sxs-lookup"><span data-stu-id="1d195-247"><span id="the_boot_configuration_for_this_device_conflicts_with_other_devices."></span><span id="THE_BOOT_CONFIGURATION_FOR_THIS_DEVICE_CONFLICTS_WITH_OTHER_DEVICES."></span>**The boot configuration for this device conflicts with other devices.**</span></span> <span data-ttu-id="1d195-248"> (6)</span><span class="sxs-lookup"><span data-stu-id="1d195-248">(6)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-249">A configuração de inicialização para o dispositivo está em conflito com outros dispositivos.</span><span class="sxs-lookup"><span data-stu-id="1d195-249">Boot configuration for the device conflicts with other devices.</span></span>

</dd> <dt>

<span id="Cannot_filter."></span><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>

<span data-ttu-id="1d195-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Não é possível filtrar.**</span><span class="sxs-lookup"><span data-stu-id="1d195-250"><span id="cannot_filter."></span><span id="CANNOT_FILTER."></span>**Cannot filter.**</span></span> <span data-ttu-id="1d195-251">(7)</span><span class="sxs-lookup"><span data-stu-id="1d195-251">(7)</span></span>


</dt> <dd></dd> <dt>

<span id="The_driver_loader_for_the_device_is_missing."></span><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>

<span data-ttu-id="1d195-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**O carregador de driver para o dispositivo está ausente.**</span><span class="sxs-lookup"><span data-stu-id="1d195-252"><span id="the_driver_loader_for_the_device_is_missing."></span><span id="THE_DRIVER_LOADER_FOR_THE_DEVICE_IS_MISSING."></span>**The driver loader for the device is missing.**</span></span> <span data-ttu-id="1d195-253">(8)</span><span class="sxs-lookup"><span data-stu-id="1d195-253">(8)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-254">O carregador de driver para o dispositivo está ausente.</span><span class="sxs-lookup"><span data-stu-id="1d195-254">Driver loader for the device is missing.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>

<span data-ttu-id="1d195-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**Este dispositivo não está funcionando corretamente porque o firmware de controle está relatando os recursos para o dispositivo incorretamente.**</span><span class="sxs-lookup"><span data-stu-id="1d195-255"><span id="this_device_is_not_working_properly_because_the_controlling_firmware_is_reporting_the_resources_for_the_device_incorrectly."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THE_CONTROLLING_FIRMWARE_IS_REPORTING_THE_RESOURCES_FOR_THE_DEVICE_INCORRECTLY."></span>**This device is not working properly because the controlling firmware is reporting the resources for the device incorrectly.**</span></span> <span data-ttu-id="1d195-256">(9)</span><span class="sxs-lookup"><span data-stu-id="1d195-256">(9)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-257">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d195-257">Device is not working properly.</span></span> <span data-ttu-id="1d195-258">O firmware de controle está relatando incorretamente os recursos para o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d195-258">The controlling firmware is incorrectly reporting the resources for the device.</span></span>

</dd> <dt>

<span id="This_device_cannot_start."></span><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>

<span data-ttu-id="1d195-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**Este dispositivo não pode ser iniciado.**</span><span class="sxs-lookup"><span data-stu-id="1d195-259"><span id="this_device_cannot_start."></span><span id="THIS_DEVICE_CANNOT_START."></span>**This device cannot start.**</span></span> <span data-ttu-id="1d195-260">(10)</span><span class="sxs-lookup"><span data-stu-id="1d195-260">(10)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-261">Não é possível iniciar o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d195-261">Device cannot start.</span></span>

</dd> <dt>

<span id="This_device_failed."></span><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>

<span data-ttu-id="1d195-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**Este dispositivo falhou.**</span><span class="sxs-lookup"><span data-stu-id="1d195-262"><span id="this_device_failed."></span><span id="THIS_DEVICE_FAILED."></span>**This device failed.**</span></span> <span data-ttu-id="1d195-263">(11)</span><span class="sxs-lookup"><span data-stu-id="1d195-263">(11)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-264">Falha no dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d195-264">Device failed.</span></span>

</dd> <dt>

<span id="This_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>

<span data-ttu-id="1d195-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**Este dispositivo não pode encontrar recursos livres suficientes que podem ser usados.**</span><span class="sxs-lookup"><span data-stu-id="1d195-265"><span id="this_device_cannot_find_enough_free_resources_that_it_can_use."></span><span id="THIS_DEVICE_CANNOT_FIND_ENOUGH_FREE_RESOURCES_THAT_IT_CAN_USE."></span>**This device cannot find enough free resources that it can use.**</span></span> <span data-ttu-id="1d195-266">12</span><span class="sxs-lookup"><span data-stu-id="1d195-266">(12)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-267">O dispositivo não pode encontrar recursos livres suficientes para usar.</span><span class="sxs-lookup"><span data-stu-id="1d195-267">Device cannot find enough free resources to use.</span></span>

</dd> <dt>

<span id="Windows_cannot_verify_this_device_s_resources."></span><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>

<span data-ttu-id="1d195-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**O Windows não pode verificar os recursos deste dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d195-268"><span id="windows_cannot_verify_this_device_s_resources."></span><span id="WINDOWS_CANNOT_VERIFY_THIS_DEVICE_S_RESOURCES."></span>**Windows cannot verify this device's resources.**</span></span> <span data-ttu-id="1d195-269">(13)</span><span class="sxs-lookup"><span data-stu-id="1d195-269">(13)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-270">O Windows não pode verificar os recursos do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d195-270">Windows cannot verify the device's resources.</span></span>

</dd> <dt>

<span id="This_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>

<span data-ttu-id="1d195-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**Este dispositivo não funcionará corretamente até que você reinicie o computador.**</span><span class="sxs-lookup"><span data-stu-id="1d195-271"><span id="this_device_cannot_work_properly_until_you_restart_your_computer."></span><span id="THIS_DEVICE_CANNOT_WORK_PROPERLY_UNTIL_YOU_RESTART_YOUR_COMPUTER."></span>**This device cannot work properly until you restart your computer.**</span></span> <span data-ttu-id="1d195-272">(14)</span><span class="sxs-lookup"><span data-stu-id="1d195-272">(14)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-273">O dispositivo não funcionará corretamente até que o computador seja reiniciado.</span><span class="sxs-lookup"><span data-stu-id="1d195-273">Device cannot work properly until the computer is restarted.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>

<span data-ttu-id="1d195-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**Este dispositivo não está funcionando corretamente porque provavelmente há um problema de nova enumeração.**</span><span class="sxs-lookup"><span data-stu-id="1d195-274"><span id="This_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="this_device_is_not_working_properly_because_there_is_probably_a_re-enumeration_problem."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_THERE_IS_PROBABLY_A_RE-ENUMERATION_PROBLEM."></span>**This device is not working properly because there is probably a re-enumeration problem.**</span></span> <span data-ttu-id="1d195-275">(15)</span><span class="sxs-lookup"><span data-stu-id="1d195-275">(15)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-276">O dispositivo não está funcionando corretamente devido a um possível problema de reenumeração.</span><span class="sxs-lookup"><span data-stu-id="1d195-276">Device is not working properly due to a possible re-enumeration problem.</span></span>

</dd> <dt>

<span id="Windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>

<span data-ttu-id="1d195-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**O Windows não pode identificar todos os recursos que este dispositivo usa.**</span><span class="sxs-lookup"><span data-stu-id="1d195-277"><span id="windows_cannot_identify_all_the_resources_this_device_uses."></span><span id="WINDOWS_CANNOT_IDENTIFY_ALL_THE_RESOURCES_THIS_DEVICE_USES."></span>**Windows cannot identify all the resources this device uses.**</span></span> <span data-ttu-id="1d195-278">(16)</span><span class="sxs-lookup"><span data-stu-id="1d195-278">(16)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-279">O Windows não pode identificar todos os recursos que o dispositivo usa.</span><span class="sxs-lookup"><span data-stu-id="1d195-279">Windows cannot identify all of the resources that the device uses.</span></span>

</dd> <dt>

<span id="This_device_is_asking_for_an_unknown_resource_type."></span><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>

<span data-ttu-id="1d195-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**Este dispositivo está solicitando um tipo de recurso desconhecido.**</span><span class="sxs-lookup"><span data-stu-id="1d195-280"><span id="this_device_is_asking_for_an_unknown_resource_type."></span><span id="THIS_DEVICE_IS_ASKING_FOR_AN_UNKNOWN_RESOURCE_TYPE."></span>**This device is asking for an unknown resource type.**</span></span> <span data-ttu-id="1d195-281">(17)</span><span class="sxs-lookup"><span data-stu-id="1d195-281">(17)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-282">O dispositivo está solicitando um tipo de recurso desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1d195-282">Device is requesting an unknown resource type.</span></span>

</dd> <dt>

<span id="Reinstall_the_drivers_for_this_device."></span><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d195-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstale os drivers para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d195-283"><span id="reinstall_the_drivers_for_this_device."></span><span id="REINSTALL_THE_DRIVERS_FOR_THIS_DEVICE."></span>**Reinstall the drivers for this device.**</span></span> <span data-ttu-id="1d195-284">(18)</span><span class="sxs-lookup"><span data-stu-id="1d195-284">(18)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-285">Os drivers de dispositivo devem ser reinstalados.</span><span class="sxs-lookup"><span data-stu-id="1d195-285">Device drivers must be reinstalled.</span></span>

</dd> <dt>

<span id="Failure_using_the_VxD_loader."></span><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>

<span data-ttu-id="1d195-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Falha ao usar o carregador VxD.**</span><span class="sxs-lookup"><span data-stu-id="1d195-286"><span id="failure_using_the_vxd_loader."></span><span id="FAILURE_USING_THE_VXD_LOADER."></span>**Failure using the VxD loader.**</span></span> <span data-ttu-id="1d195-287">(19)</span><span class="sxs-lookup"><span data-stu-id="1d195-287">(19)</span></span>


</dt> <dd></dd> <dt>

<span id="Your_registry_might_be_corrupted."></span><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>

<span data-ttu-id="1d195-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**O registro pode estar corrompido.**</span><span class="sxs-lookup"><span data-stu-id="1d195-288"><span id="your_registry_might_be_corrupted."></span><span id="YOUR_REGISTRY_MIGHT_BE_CORRUPTED."></span>**Your registry might be corrupted.**</span></span> <span data-ttu-id="1d195-289">(20)</span><span class="sxs-lookup"><span data-stu-id="1d195-289">(20)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-290">O registro pode estar corrompido.</span><span class="sxs-lookup"><span data-stu-id="1d195-290">Registry might be corrupted.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>

<span data-ttu-id="1d195-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware. O Windows está removendo este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d195-291"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_does_not_work__see_your_hardware_documentation._Windows_is_removing_this_device."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_does_not_work__see_your_hardware_documentation._windows_is_removing_this_device."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOES_NOT_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION._WINDOWS_IS_REMOVING_THIS_DEVICE."></span>**System failure: Try changing the driver for this device. If that does not work, see your hardware documentation. Windows is removing this device.**</span></span> <span data-ttu-id="1d195-292">(21)</span><span class="sxs-lookup"><span data-stu-id="1d195-292">(21)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-293">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="1d195-293">System failure.</span></span> <span data-ttu-id="1d195-294">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="1d195-294">If changing the device driver is ineffective, see the hardware documentation.</span></span> <span data-ttu-id="1d195-295">O Windows está removendo o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d195-295">Windows is removing the device.</span></span>

</dd> <dt>

<span id="This_device_is_disabled."></span><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>

<span data-ttu-id="1d195-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**Este dispositivo está desabilitado.**</span><span class="sxs-lookup"><span data-stu-id="1d195-296"><span id="this_device_is_disabled."></span><span id="THIS_DEVICE_IS_DISABLED."></span>**This device is disabled.**</span></span> <span data-ttu-id="1d195-297">(22)</span><span class="sxs-lookup"><span data-stu-id="1d195-297">(22)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-298">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1d195-298">Device is disabled.</span></span>

</dd> <dt>

<span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>

<span data-ttu-id="1d195-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**Falha do sistema: Tente alterar o driver deste dispositivo. Se isso não funcionar, consulte a documentação do hardware.**</span><span class="sxs-lookup"><span data-stu-id="1d195-299"><span id="System_failure__Try_changing_the_driver_for_this_device._If_that_doesn_t_work__see_your_hardware_documentation."></span><span id="system_failure__try_changing_the_driver_for_this_device._if_that_doesn_t_work__see_your_hardware_documentation."></span><span id="SYSTEM_FAILURE__TRY_CHANGING_THE_DRIVER_FOR_THIS_DEVICE._IF_THAT_DOESN_T_WORK__SEE_YOUR_HARDWARE_DOCUMENTATION."></span>**System failure: Try changing the driver for this device. If that doesn't work, see your hardware documentation.**</span></span> <span data-ttu-id="1d195-300">(23)</span><span class="sxs-lookup"><span data-stu-id="1d195-300">(23)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-301">Falha do sistema.</span><span class="sxs-lookup"><span data-stu-id="1d195-301">System failure.</span></span> <span data-ttu-id="1d195-302">Se a alteração do driver de dispositivo não for eficaz, consulte a documentação do hardware.</span><span class="sxs-lookup"><span data-stu-id="1d195-302">If changing the device driver is ineffective, see the hardware documentation.</span></span>

</dd> <dt>

<span id="This_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>

<span data-ttu-id="1d195-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**Este dispositivo não está presente, não está funcionando corretamente ou não tem todos os drivers instalados.**</span><span class="sxs-lookup"><span data-stu-id="1d195-303"><span id="this_device_is_not_present__is_not_working_properly__or_does_not_have_all_its_drivers_installed."></span><span id="THIS_DEVICE_IS_NOT_PRESENT__IS_NOT_WORKING_PROPERLY__OR_DOES_NOT_HAVE_ALL_ITS_DRIVERS_INSTALLED."></span>**This device is not present, is not working properly, or does not have all its drivers installed.**</span></span> <span data-ttu-id="1d195-304">(24)</span><span class="sxs-lookup"><span data-stu-id="1d195-304">(24)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-305">O dispositivo não está presente, não está funcionando corretamente ou não tem todos os seus drivers instalados.</span><span class="sxs-lookup"><span data-stu-id="1d195-305">Device is not present, not working properly, or does not have all of its drivers installed.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1d195-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d195-306"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1d195-307">(25)</span><span class="sxs-lookup"><span data-stu-id="1d195-307">(25)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-308">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d195-308">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="Windows_is_still_setting_up_this_device."></span><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>

<span data-ttu-id="1d195-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**O Windows ainda está configurando este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d195-309"><span id="windows_is_still_setting_up_this_device."></span><span id="WINDOWS_IS_STILL_SETTING_UP_THIS_DEVICE."></span>**Windows is still setting up this device.**</span></span> <span data-ttu-id="1d195-310">(26)</span><span class="sxs-lookup"><span data-stu-id="1d195-310">(26)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-311">O Windows ainda está configurando o dispositivo.</span><span class="sxs-lookup"><span data-stu-id="1d195-311">Windows is still setting up the device.</span></span>

</dd> <dt>

<span id="This_device_does_not_have_valid_log_configuration."></span><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>

<span data-ttu-id="1d195-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**Este dispositivo não tem uma configuração de log válida.**</span><span class="sxs-lookup"><span data-stu-id="1d195-312"><span id="this_device_does_not_have_valid_log_configuration."></span><span id="THIS_DEVICE_DOES_NOT_HAVE_VALID_LOG_CONFIGURATION."></span>**This device does not have valid log configuration.**</span></span> <span data-ttu-id="1d195-313">(27)</span><span class="sxs-lookup"><span data-stu-id="1d195-313">(27)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-314">O dispositivo não tem uma configuração de log válida.</span><span class="sxs-lookup"><span data-stu-id="1d195-314">Device does not have valid log configuration.</span></span>

</dd> <dt>

<span id="The_drivers_for_this_device_are_not_installed."></span><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>

<span data-ttu-id="1d195-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**Os drivers para este dispositivo não estão instalados.**</span><span class="sxs-lookup"><span data-stu-id="1d195-315"><span id="the_drivers_for_this_device_are_not_installed."></span><span id="THE_DRIVERS_FOR_THIS_DEVICE_ARE_NOT_INSTALLED."></span>**The drivers for this device are not installed.**</span></span> <span data-ttu-id="1d195-316">(28)</span><span class="sxs-lookup"><span data-stu-id="1d195-316">(28)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-317">Os drivers de dispositivo não estão instalados.</span><span class="sxs-lookup"><span data-stu-id="1d195-317">Device drivers are not installed.</span></span>

</dd> <dt>

<span id="This_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>

<span data-ttu-id="1d195-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**Este dispositivo está desabilitado porque o firmware do dispositivo não forneceu os recursos necessários.**</span><span class="sxs-lookup"><span data-stu-id="1d195-318"><span id="this_device_is_disabled_because_the_firmware_of_the_device_did_not_give_it_the_required_resources."></span><span id="THIS_DEVICE_IS_DISABLED_BECAUSE_THE_FIRMWARE_OF_THE_DEVICE_DID_NOT_GIVE_IT_THE_REQUIRED_RESOURCES."></span>**This device is disabled because the firmware of the device did not give it the required resources.**</span></span> <span data-ttu-id="1d195-319">(29)</span><span class="sxs-lookup"><span data-stu-id="1d195-319">(29)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-320">O dispositivo está desabilitado.</span><span class="sxs-lookup"><span data-stu-id="1d195-320">Device is disabled.</span></span> <span data-ttu-id="1d195-321">O firmware do dispositivo não forneceu os recursos necessários.</span><span class="sxs-lookup"><span data-stu-id="1d195-321">The device firmware did not provide the required resources.</span></span>

</dd> <dt>

<span id="This_device_is_using_an_Interrupt_Request__IRQ__resource_that_another_device_is_using."></span><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>

<span data-ttu-id="1d195-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**Este dispositivo está usando um recurso de IRQ (solicitação de interrupção) que outro dispositivo está usando.**</span><span class="sxs-lookup"><span data-stu-id="1d195-322"><span id="this_device_is_using_an_interrupt_request__irq__resource_that_another_device_is_using."></span><span id="THIS_DEVICE_IS_USING_AN_INTERRUPT_REQUEST__IRQ__RESOURCE_THAT_ANOTHER_DEVICE_IS_USING."></span>**This device is using an Interrupt Request (IRQ) resource that another device is using.**</span></span> <span data-ttu-id="1d195-323">(30)</span><span class="sxs-lookup"><span data-stu-id="1d195-323">(30)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-324">O dispositivo está usando um recurso de IRQ que outro dispositivo está usando.</span><span class="sxs-lookup"><span data-stu-id="1d195-324">Device is using an IRQ resource that another device is using.</span></span>

</dd> <dt>

<span id="This_device_is_not_working_properly_because_Windows_cannot_load_the_drivers_required_for_this_device."></span><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>

<span data-ttu-id="1d195-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**Este dispositivo não está funcionando corretamente porque o Windows não pode carregar os drivers necessários para este dispositivo.**</span><span class="sxs-lookup"><span data-stu-id="1d195-325"><span id="this_device_is_not_working_properly_because_windows_cannot_load_the_drivers_required_for_this_device."></span><span id="THIS_DEVICE_IS_NOT_WORKING_PROPERLY_BECAUSE_WINDOWS_CANNOT_LOAD_THE_DRIVERS_REQUIRED_FOR_THIS_DEVICE."></span>**This device is not working properly because Windows cannot load the drivers required for this device.**</span></span> <span data-ttu-id="1d195-326">(31)</span><span class="sxs-lookup"><span data-stu-id="1d195-326">(31)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-327">O dispositivo não está funcionando corretamente.</span><span class="sxs-lookup"><span data-stu-id="1d195-327">Device is not working properly.</span></span> <span data-ttu-id="1d195-328">O Windows não pode carregar os drivers de dispositivo necessários.</span><span class="sxs-lookup"><span data-stu-id="1d195-328">Windows cannot load the required device drivers.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d195-329">**ConfigManagerUserConfig**</span><span class="sxs-lookup"><span data-stu-id="1d195-329">**ConfigManagerUserConfig**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-330">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d195-330">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-331">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-331">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-332">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d195-332">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-333">Se for **true**, o dispositivo estará usando uma configuração definida pelo usuário.</span><span class="sxs-lookup"><span data-stu-id="1d195-333">If **True**, the device is using a user-defined configuration.</span></span>

<span data-ttu-id="1d195-334">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-334">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-335">**CreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d195-335">**CreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-336">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-336">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-337">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-337">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-338">Qualificadores: [ **\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1d195-338">Qualifiers: [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1d195-339">Nome da primeira classe concreta a ser exibida na cadeia de herança usada na criação de uma instância.</span><span class="sxs-lookup"><span data-stu-id="1d195-339">Name of the first concrete class to appear in the inheritance chain used in the creation of an instance.</span></span> <span data-ttu-id="1d195-340">Quando usado com as outras propriedades de chave da classe, a propriedade permite que todas as instâncias dessa classe e suas subclasses sejam identificadas exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="1d195-340">When used with the other key properties of the class, the property allows all instances of this class and its subclasses to be uniquely identified.</span></span>

<span data-ttu-id="1d195-341">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-341">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-342">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="1d195-342">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-343">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-343">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-344">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-344">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-345">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Descrição")</span><span class="sxs-lookup"><span data-stu-id="1d195-345">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Description")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-346">Descrição do objeto.</span><span class="sxs-lookup"><span data-stu-id="1d195-346">Description of the object.</span></span>

<span data-ttu-id="1d195-347">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-347">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-348">**DeviceID**</span><span class="sxs-lookup"><span data-stu-id="1d195-348">**DeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-349">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-349">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-350">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-350">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-351">Qualificadores: [**chave**](../wmisdk/key-qualifier.md), [**substituição**](../wmisdk/standard-qualifiers.md) ("DeviceID"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry do \| sistema \\ \\ CurrentControlSet \\ \\ Control \\ \\ Class \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="1d195-351">Qualifiers: [**Key**](../wmisdk/key-qualifier.md), [**Override**](../wmisdk/standard-qualifiers.md) ("DeviceId"), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-352">Identificador exclusivo do adaptador de rede de outros dispositivos no sistema.</span><span class="sxs-lookup"><span data-stu-id="1d195-352">Unique identifier of the network adapter from other devices on the system.</span></span>

<span data-ttu-id="1d195-353">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-353">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-354">**ErrorCleared**</span><span class="sxs-lookup"><span data-stu-id="1d195-354">**ErrorCleared**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-355">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d195-355">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-356">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-356">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-357">Se **for true**, o erro relatado em **LastErrorCode** agora será limpo.</span><span class="sxs-lookup"><span data-stu-id="1d195-357">If **True**, the error reported in **LastErrorCode** is now cleared.</span></span>

<span data-ttu-id="1d195-358">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-358">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-359">**ErrorDescription**</span><span class="sxs-lookup"><span data-stu-id="1d195-359">**ErrorDescription**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-360">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-360">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-361">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-361">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-362">Mais informações sobre o erro registrado em **LastErrorCode** e informações sobre as ações corretivas que podem ser executadas.</span><span class="sxs-lookup"><span data-stu-id="1d195-362">More information about the error recorded in **LastErrorCode**, and information about any corrective actions that may be taken.</span></span>

<span data-ttu-id="1d195-363">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-363">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-364">**GUID**</span><span class="sxs-lookup"><span data-stu-id="1d195-364">**GUID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-365">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-365">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-366">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-366">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-367">Identificador global exclusivo para a conexão.</span><span class="sxs-lookup"><span data-stu-id="1d195-367">Globally unique identifier for the connection.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-368">**Index**</span><span class="sxs-lookup"><span data-stu-id="1d195-368">**Index**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-369">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d195-369">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-370">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-370">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-371">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| classe de controle CurrentControlSet do sistema Win32Registry \\ \\ \\ \\ \\ \\ \\ \\ {4D36E972-E325-11CE-BFC1-08002BE10318}")</span><span class="sxs-lookup"><span data-stu-id="1d195-371">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|System\\\\CurrentControlSet\\\\Control\\\\Class\\\\{4D36E972-E325-11CE-BFC1-08002BE10318}")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-372">Número de índice do adaptador de rede, armazenado no registro do sistema.</span><span class="sxs-lookup"><span data-stu-id="1d195-372">Index number of the network adapter, stored in the system registry.</span></span>

<span data-ttu-id="1d195-373">Exemplo: 0</span><span class="sxs-lookup"><span data-stu-id="1d195-373">Example: 0</span></span>

</dd> <dt>

<span data-ttu-id="1d195-374">**InstallDate**</span><span class="sxs-lookup"><span data-stu-id="1d195-374">**InstallDate**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-375">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d195-375">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-376">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-376">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-377">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Componente DMTF \| 1,5 "), [**DisplayName**](../wmisdk/standard-qualifiers.md) (" data de instalação ")</span><span class="sxs-lookup"><span data-stu-id="1d195-377">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|ComponentID\|001.5"), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Install Date")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-378">Data e hora em que o objeto foi instalado.</span><span class="sxs-lookup"><span data-stu-id="1d195-378">Date and time the object was installed.</span></span> <span data-ttu-id="1d195-379">Essa propriedade não precisa de um valor para indicar que o objeto está instalado.</span><span class="sxs-lookup"><span data-stu-id="1d195-379">This property does not need a value to indicate that the object is installed.</span></span>

<span data-ttu-id="1d195-380">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-380">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1d195-381">Esta propriedade ainda não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="1d195-381">This property has not been implemented yet.</span></span> <span data-ttu-id="1d195-382">Ele retorna um valor **nulo** por padrão.</span><span class="sxs-lookup"><span data-stu-id="1d195-382">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-383">**Instalado**</span><span class="sxs-lookup"><span data-stu-id="1d195-383">**Installed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-384">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d195-384">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-385">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-385">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-386">Qualificadores: [**preteridos**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("WIN32REGISTRY \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| DriverDate")</span><span class="sxs-lookup"><span data-stu-id="1d195-386">Qualifiers: [**DEPRECATED**](../wmisdk/standard-wmi-qualifiers.md), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|DriverDate")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-387">Se for **true**, o adaptador de rede será instalado no sistema.</span><span class="sxs-lookup"><span data-stu-id="1d195-387">If **True**, the network adapter is installed in the system.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-388">**InterfaceIndex**</span><span class="sxs-lookup"><span data-stu-id="1d195-388">**InterfaceIndex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-389">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d195-389">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-390">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-390">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-391">Valor de índice que identifica exclusivamente a interface de rede local.</span><span class="sxs-lookup"><span data-stu-id="1d195-391">Index value that uniquely identifies the local network interface.</span></span> <span data-ttu-id="1d195-392">O valor nessa propriedade é o mesmo que o valor na propriedade **InterfaceIndex** na instância do [**Win32 \_ IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) que representa a interface de rede na tabela de rotas.</span><span class="sxs-lookup"><span data-stu-id="1d195-392">The value in this property is the same as the value in the **InterfaceIndex** property in the instance of [**Win32\_IP4RouteTable**](/previous-versions/windows/desktop/wmiiprouteprov/win32-ip4routetable) that represents the network interface in the route table.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-393">**LastErrorCode**</span><span class="sxs-lookup"><span data-stu-id="1d195-393">**LastErrorCode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-394">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d195-394">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-395">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-395">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-396">Código do último erro relatado pelo dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d195-396">Last error code reported by the logical device.</span></span>

<span data-ttu-id="1d195-397">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-397">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-398">**MACAddress**</span><span class="sxs-lookup"><span data-stu-id="1d195-398">**MACAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-399">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-399">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-400">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-400">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-401">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) (" \| funções de entrada e saída de dispositivo do win32api \| [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span><span class="sxs-lookup"><span data-stu-id="1d195-401">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32API\|Device Input and Output Functions\|[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-402">Endereço de controle de acesso à mídia para este adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-402">Media access control address for this network adapter.</span></span> <span data-ttu-id="1d195-403">Um endereço MAC é um número de 48 bits exclusivo atribuído ao adaptador de rede pelo fabricante.</span><span class="sxs-lookup"><span data-stu-id="1d195-403">A MAC address is a unique 48-bit number assigned to the network adapter by the manufacturer.</span></span> <span data-ttu-id="1d195-404">Ele identifica exclusivamente esse adaptador de rede e é usado para mapear comunicações de rede TCP/IP.</span><span class="sxs-lookup"><span data-stu-id="1d195-404">It uniquely identifies this network adapter and is used for mapping TCP/IP network communications.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-405">**Manufacturer**</span><span class="sxs-lookup"><span data-stu-id="1d195-405">**Manufacturer**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-406">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-406">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-407">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-407">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-408">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| manufacturer")</span><span class="sxs-lookup"><span data-stu-id="1d195-408">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|Manufacturer")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-409">Nome do fabricante do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-409">Name of the network adapter's manufacturer.</span></span>

<span data-ttu-id="1d195-410">Exemplo: "3COM"</span><span class="sxs-lookup"><span data-stu-id="1d195-410">Example: "3COM"</span></span>

</dd> <dt>

<span data-ttu-id="1d195-411">**MaxNumberControlled**</span><span class="sxs-lookup"><span data-stu-id="1d195-411">**MaxNumberControlled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-412">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="1d195-412">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-413">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-413">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-414">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Porta do barramento DMTF \| 1,9 \| número máximo de anexos ")</span><span class="sxs-lookup"><span data-stu-id="1d195-414">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Bus Port\|001.9\|Maximum Number of Attachments")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-415">Número máximo de portas diretamente endereçáveis com suporte por este adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-415">Maximum number of directly addressable ports supported by this network adapter.</span></span> <span data-ttu-id="1d195-416">Um valor de 0 (zero) deve ser usado se o número for desconhecido.</span><span class="sxs-lookup"><span data-stu-id="1d195-416">A value of 0 (zero) should be used if the number is unknown.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-417">**MaxSpeed**</span><span class="sxs-lookup"><span data-stu-id="1d195-417">**MaxSpeed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-418">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d195-418">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-419">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-419">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-420">Qualificadores: [**unidades**](../wmisdk/standard-qualifiers.md) ("bits por segundo")</span><span class="sxs-lookup"><span data-stu-id="1d195-420">Qualifiers: [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-421">Velocidade máxima, em bits por segundo, para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-421">Maximum speed, in bits per second, for the network adapter.</span></span>

<span data-ttu-id="1d195-422">Essa propriedade é herdada do [**CIM \_ adaptador**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-422">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="1d195-423">Esta propriedade ainda não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="1d195-423">This property has not been implemented yet.</span></span> <span data-ttu-id="1d195-424">Ele retorna um valor **nulo** por padrão.</span><span class="sxs-lookup"><span data-stu-id="1d195-424">It returns a **NULL** value by default.</span></span>

<span data-ttu-id="1d195-425">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d195-425">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-426">**Nome**</span><span class="sxs-lookup"><span data-stu-id="1d195-426">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-427">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-427">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-428">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-428">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-429">Qualificadores: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span><span class="sxs-lookup"><span data-stu-id="1d195-429">Qualifiers: [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Name")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-430">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="1d195-430">Label by which the object is known.</span></span> <span data-ttu-id="1d195-431">Quando em uma subclasse, a propriedade pode ser substituída para ser uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="1d195-431">When subclassed, the property can be overridden to be a key property.</span></span>

<span data-ttu-id="1d195-432">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-432">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-433">**NetConnectionID**</span><span class="sxs-lookup"><span data-stu-id="1d195-433">**NetConnectionID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-434">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-434">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-435">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="1d195-435">Access type: Read/write</span></span>
</dt> </dl>

<span data-ttu-id="1d195-436">Nome da conexão de rede que aparece no programa do painel de controle de **conexões de rede** .</span><span class="sxs-lookup"><span data-stu-id="1d195-436">Name of the network connection as it appears in the **Network Connections** Control Panel program.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-437">**NetConnectionStatus**</span><span class="sxs-lookup"><span data-stu-id="1d195-437">**NetConnectionStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-438">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d195-438">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-439">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-439">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-440">Estado da conexão do adaptador de rede com a rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-440">State of the network adapter connection to the network.</span></span>

<dt>

<span id="Disconnected"></span><span id="disconnected"></span><span id="DISCONNECTED"></span>

<span data-ttu-id="1d195-441">**Desconectado** (0)</span><span class="sxs-lookup"><span data-stu-id="1d195-441">**Disconnected** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Connecting"></span><span id="connecting"></span><span id="CONNECTING"></span>

<span data-ttu-id="1d195-442">**Conectando** (1)</span><span class="sxs-lookup"><span data-stu-id="1d195-442">**Connecting** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Connected"></span><span id="connected"></span><span id="CONNECTED"></span>

<span data-ttu-id="1d195-443">**Conectado** (2)</span><span class="sxs-lookup"><span data-stu-id="1d195-443">**Connected** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Disconnecting"></span><span id="disconnecting"></span><span id="DISCONNECTING"></span>

<span data-ttu-id="1d195-444">**Desconectando** (3)</span><span class="sxs-lookup"><span data-stu-id="1d195-444">**Disconnecting** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Not_Present"></span><span id="hardware_not_present"></span><span id="HARDWARE_NOT_PRESENT"></span>

<span data-ttu-id="1d195-445">**Hardware não presente** (4)</span><span class="sxs-lookup"><span data-stu-id="1d195-445">**Hardware Not Present** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Disabled"></span><span id="hardware_disabled"></span><span id="HARDWARE_DISABLED"></span>

<span data-ttu-id="1d195-446">**Hardware desabilitado** (5)</span><span class="sxs-lookup"><span data-stu-id="1d195-446">**Hardware Disabled** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Hardware_Malfunction"></span><span id="hardware_malfunction"></span><span id="HARDWARE_MALFUNCTION"></span>

<span data-ttu-id="1d195-447">**Mau funcionamento do hardware** (6)</span><span class="sxs-lookup"><span data-stu-id="1d195-447">**Hardware Malfunction** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Media_Disconnected"></span><span id="media_disconnected"></span><span id="MEDIA_DISCONNECTED"></span>

<span data-ttu-id="1d195-448">**Mídia desconectada** (7)</span><span class="sxs-lookup"><span data-stu-id="1d195-448">**Media Disconnected** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Authenticating"></span><span id="authenticating"></span><span id="AUTHENTICATING"></span>

<span data-ttu-id="1d195-449">**Autenticando** (8)</span><span class="sxs-lookup"><span data-stu-id="1d195-449">**Authenticating** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Succeeded"></span><span id="authentication_succeeded"></span><span id="AUTHENTICATION_SUCCEEDED"></span>

<span data-ttu-id="1d195-450">**Autenticação bem-sucedida** (9)</span><span class="sxs-lookup"><span data-stu-id="1d195-450">**Authentication Succeeded** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="Authentication_Failed"></span><span id="authentication_failed"></span><span id="AUTHENTICATION_FAILED"></span>

<span data-ttu-id="1d195-451">**Falha na autenticação** (10)</span><span class="sxs-lookup"><span data-stu-id="1d195-451">**Authentication Failed** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Invalid_Address"></span><span id="invalid_address"></span><span id="INVALID_ADDRESS"></span>

<span data-ttu-id="1d195-452">**Endereço inválido** (11)</span><span class="sxs-lookup"><span data-stu-id="1d195-452">**Invalid Address** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="Credentials_Required"></span><span id="credentials_required"></span><span id="CREDENTIALS_REQUIRED"></span>

<span data-ttu-id="1d195-453">**Credenciais necessárias** (12)</span><span class="sxs-lookup"><span data-stu-id="1d195-453">**Credentials Required** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d195-454">**Outras**</span><span class="sxs-lookup"><span data-stu-id="1d195-454">**Other**</span></span>


</dt> <dd><span data-ttu-id="1d195-455">13 a 65535</span><span class="sxs-lookup"><span data-stu-id="1d195-455">13–65535</span></span></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d195-456">**NetEnabled**</span><span class="sxs-lookup"><span data-stu-id="1d195-456">**NetEnabled**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-457">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d195-457">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-458">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-458">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-459">Indica se o adaptador está habilitado ou não.</span><span class="sxs-lookup"><span data-stu-id="1d195-459">Indicates whether the adapter is enabled or not.</span></span> <span data-ttu-id="1d195-460">Se for **true**, o adaptador será habilitado.</span><span class="sxs-lookup"><span data-stu-id="1d195-460">If **True**, the adapter is enabled.</span></span> <span data-ttu-id="1d195-461">Você pode habilitar ou desabilitar a NIC usando os métodos [**Enable**](enable-method-in-class-win32-networkadapter.md) e [**Disable**](disable-method-in-class-win32-networkadapter.md) .</span><span class="sxs-lookup"><span data-stu-id="1d195-461">You can enable or disable the NIC by using the [**Enable**](enable-method-in-class-win32-networkadapter.md) and [**Disable**](disable-method-in-class-win32-networkadapter.md) methods.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-462">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="1d195-462">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-463">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-463">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="1d195-464">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-464">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-465">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Adaptador de rede DMTF 802 porta \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="1d195-465">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-466">Matriz de endereços de rede para um adaptador.</span><span class="sxs-lookup"><span data-stu-id="1d195-466">Array of network addresses for an adapter.</span></span>

<span data-ttu-id="1d195-467">Essa propriedade é herdada do [**CIM \_ adaptador**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-467">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="1d195-468">Esta propriedade ainda não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="1d195-468">This property has not been implemented yet.</span></span> <span data-ttu-id="1d195-469">Ele retorna um valor **nulo** por padrão.</span><span class="sxs-lookup"><span data-stu-id="1d195-469">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-470">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="1d195-470">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-471">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-471">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-472">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-472">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-473">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Adaptador de rede DMTF 802 porta \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="1d195-473">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (64), [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-474">Endereço de rede embutido em código em um adaptador.</span><span class="sxs-lookup"><span data-stu-id="1d195-474">Network address hard-coded into an adapter.</span></span> <span data-ttu-id="1d195-475">Esse endereço embutido em código pode ser alterado por atualização de firmware ou configuração de software.</span><span class="sxs-lookup"><span data-stu-id="1d195-475">This hard-coded address may be changed by firmware upgrade or software configuration.</span></span> <span data-ttu-id="1d195-476">Nesse caso, esse campo deve ser atualizado quando a alteração é feita.</span><span class="sxs-lookup"><span data-stu-id="1d195-476">If so, this field should be updated when the change is made.</span></span> <span data-ttu-id="1d195-477">A propriedade deve ser deixada em branco se não existir nenhum endereço embutido no código para o adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-477">The property should be left blank if no hard-coded address exists for the network adapter.</span></span>

<span data-ttu-id="1d195-478">Essa propriedade é herdada do [**CIM \_ adaptador**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-478">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="1d195-479">Esta propriedade ainda não foi implementada.</span><span class="sxs-lookup"><span data-stu-id="1d195-479">This property has not been implemented yet.</span></span> <span data-ttu-id="1d195-480">Ele retorna um valor **nulo** por padrão.</span><span class="sxs-lookup"><span data-stu-id="1d195-480">It returns a **NULL** value by default.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-481">**PhysicalAdapter**</span><span class="sxs-lookup"><span data-stu-id="1d195-481">**PhysicalAdapter**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-482">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d195-482">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-483">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-483">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-484">Indica se o adaptador é um adaptador físico ou lógico.</span><span class="sxs-lookup"><span data-stu-id="1d195-484">Indicates whether the adapter is a physical or a logical adapter.</span></span> <span data-ttu-id="1d195-485">Se for **true**, o adaptador será físico.</span><span class="sxs-lookup"><span data-stu-id="1d195-485">If **True**, the adapter is physical.</span></span>

</dd> <dt>

<span data-ttu-id="1d195-486">**PNPDeviceID**</span><span class="sxs-lookup"><span data-stu-id="1d195-486">**PNPDeviceID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-487">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-487">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-488">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-488">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-489">Qualificadores: [**esquema**](../wmisdk/standard-qualifiers.md) ("Win32")</span><span class="sxs-lookup"><span data-stu-id="1d195-489">Qualifiers: [**Schema**](../wmisdk/standard-qualifiers.md) ("Win32")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-490">Identificador de dispositivo do Windows Plug and Play do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d195-490">Windows Plug and Play device identifier of the logical device.</span></span>

<span data-ttu-id="1d195-491">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-491">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<span data-ttu-id="1d195-492">Exemplo: " \* PNP030b"</span><span class="sxs-lookup"><span data-stu-id="1d195-492">Example: "\*PNP030b"</span></span>

</dd> <dt>

<span data-ttu-id="1d195-493">**PowerManagementCapabilities**</span><span class="sxs-lookup"><span data-stu-id="1d195-493">**PowerManagementCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-494">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d195-494">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="1d195-495">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-495">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-496">Matriz de recursos específicos relacionados à energia de um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d195-496">Array of the specific power-related capabilities of a logical device.</span></span>

<span data-ttu-id="1d195-497">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-497">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d195-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="1d195-498"><span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>

<span data-ttu-id="1d195-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Sem suporte** (1)</span><span class="sxs-lookup"><span data-stu-id="1d195-499"><span id="Not_Supported"></span><span id="not_supported"></span><span id="NOT_SUPPORTED"></span>**Not Supported** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1d195-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Desabilitado** (2)</span><span class="sxs-lookup"><span data-stu-id="1d195-500"><span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>**Disabled** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1d195-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1d195-501"><span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>**Enabled** (3)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-502">Os recursos de gerenciamento de energia estão habilitados no momento, mas o conjunto de recursos exato é desconhecido ou as informações não estão disponíveis.</span><span class="sxs-lookup"><span data-stu-id="1d195-502">The power management features are currently enabled but the exact feature set is unknown or the information is unavailable.</span></span>

</dd> <dt>

<span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>

<span data-ttu-id="1d195-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Modos de economia de energia inseridos automaticamente** (4)</span><span class="sxs-lookup"><span data-stu-id="1d195-503"><span id="Power_Saving_Modes_Entered_Automatically"></span><span id="power_saving_modes_entered_automatically"></span><span id="POWER_SAVING_MODES_ENTERED_AUTOMATICALLY"></span>**Power Saving Modes Entered Automatically** (4)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-504">O dispositivo pode alterar seu estado de energia com base no uso ou em outros critérios.</span><span class="sxs-lookup"><span data-stu-id="1d195-504">The device can change its power state based on usage or other criteria.</span></span>

</dd> <dt>

<span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>

<span data-ttu-id="1d195-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Estado de energia configurável** (5)</span><span class="sxs-lookup"><span data-stu-id="1d195-505"><span id="Power_State_Settable"></span><span id="power_state_settable"></span><span id="POWER_STATE_SETTABLE"></span>**Power State Settable** (5)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-506">Há suporte para o método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) .</span><span class="sxs-lookup"><span data-stu-id="1d195-506">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method is supported.</span></span> <span data-ttu-id="1d195-507">Esse método é encontrado na classe pai [**de \_ LogicalDevice CIM**](cim-logicaldevice.md) e pode ser implementado.</span><span class="sxs-lookup"><span data-stu-id="1d195-507">This method is found on the parent [**CIM\_LogicalDevice**](cim-logicaldevice.md) class and can be implemented.</span></span> <span data-ttu-id="1d195-508">Para obter mais informações, consulte [Designing formato MOF (MOF) classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-508">For more information, see [Designing Managed Object Format (MOF) Classes](../wmisdk/designing-managed-object-format--mof--classes.md).</span></span>

</dd> <dt>

<span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>

<span data-ttu-id="1d195-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Ciclo de energia com suporte** (6)</span><span class="sxs-lookup"><span data-stu-id="1d195-509"><span id="Power_Cycling_Supported"></span><span id="power_cycling_supported"></span><span id="POWER_CYCLING_SUPPORTED"></span>**Power Cycling Supported** (6)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-510">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia).</span><span class="sxs-lookup"><span data-stu-id="1d195-510">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle).</span></span>

</dd> <dt>

<span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>

<span data-ttu-id="1d195-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Energia cronometrada com suporte** (7)</span><span class="sxs-lookup"><span data-stu-id="1d195-511"><span id="Timed_Power_On_Supported"></span><span id="timed_power_on_supported"></span><span id="TIMED_POWER_ON_SUPPORTED"></span>**Timed Power On Supported** (7)</span></span>


</dt> <dd>

<span data-ttu-id="1d195-512">Tempo Power-On com suporte</span><span class="sxs-lookup"><span data-stu-id="1d195-512">Timed Power-On Supported</span></span>

<span data-ttu-id="1d195-513">O método [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) pode ser invocado com o parâmetro *PowerState* definido como 5 (ciclo de energia) e o *tempo* definido como uma data e hora e um intervalo específicos para o Power-on.</span><span class="sxs-lookup"><span data-stu-id="1d195-513">The [**SetPowerState**](setpowerstate-method-in-class-cim-controller.md) method can be invoked with the *PowerState* parameter set to 5 (Power Cycle) and *Time* set to a specific date and time, or interval, for power-on.</span></span>

</dd> </dl>

</dd> <dt>

<span data-ttu-id="1d195-514">**PowerManagementSupported**</span><span class="sxs-lookup"><span data-stu-id="1d195-514">**PowerManagementSupported**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-515">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="1d195-515">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-516">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-516">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="1d195-517">Se **for true**, o dispositivo poderá ser gerenciado por energia (pode ser colocado no modo de suspensão e assim por diante).</span><span class="sxs-lookup"><span data-stu-id="1d195-517">If **True**, the device can be power-managed (can be put into suspend mode, and so on).</span></span> <span data-ttu-id="1d195-518">A propriedade não indica que os recursos de gerenciamento de energia estão habilitados no momento, apenas que o dispositivo lógico é capaz de gerenciamento de energia.</span><span class="sxs-lookup"><span data-stu-id="1d195-518">The property does not indicate that power management features are currently enabled, only that the logical device is capable of power management.</span></span>

<span data-ttu-id="1d195-519">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-519">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-520">**ProductName**</span><span class="sxs-lookup"><span data-stu-id="1d195-520">**ProductName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-521">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-521">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-522">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-522">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-523">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ServiceName")</span><span class="sxs-lookup"><span data-stu-id="1d195-523">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ServiceName")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-524">Nome do produto do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-524">Product name of the network adapter.</span></span>

<span data-ttu-id="1d195-525">Exemplo: "Fast EtherLink XL"</span><span class="sxs-lookup"><span data-stu-id="1d195-525">Example: "Fast EtherLink XL"</span></span>

</dd> <dt>

<span data-ttu-id="1d195-526">**ServiceName**</span><span class="sxs-lookup"><span data-stu-id="1d195-526">**ServiceName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-527">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-527">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-528">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-528">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-529">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry \| software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ NetworkCards \| ProductName")</span><span class="sxs-lookup"><span data-stu-id="1d195-529">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("Win32Registry\|Software\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\NetworkCards\|ProductName")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-530">Nome do serviço do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-530">Service name of the network adapter.</span></span> <span data-ttu-id="1d195-531">Esse nome é geralmente mais curto do que o nome completo do produto.</span><span class="sxs-lookup"><span data-stu-id="1d195-531">This name is usually shorter than the full product name.</span></span>

<span data-ttu-id="1d195-532">Exemplo: "Elnkii"</span><span class="sxs-lookup"><span data-stu-id="1d195-532">Example: "Elnkii"</span></span>

</dd> <dt>

<span data-ttu-id="1d195-533">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="1d195-533">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-534">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="1d195-534">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-535">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-535">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-536">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB. IETF \| RFC1213-MIB. ifSpeed "," MIF. \|Adaptador de rede DMTF 802 porta \| 1,5 "), [**unidades**](../wmisdk/standard-qualifiers.md) (" bits por segundo ")</span><span class="sxs-lookup"><span data-stu-id="1d195-536">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIB.IETF\|RFC1213-MIB.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), [**Units**](../wmisdk/standard-qualifiers.md) ("bits per second")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-537">Estimativa da largura de banda atual em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="1d195-537">Estimate of the current bandwidth in bits per second.</span></span> <span data-ttu-id="1d195-538">Para pontos de extremidade que variam na largura de banda ou para aqueles em que não é possível fazer nenhuma estimativa precisa, essa propriedade deve conter a largura de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="1d195-538">For endpoints which vary in bandwidth or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

<span data-ttu-id="1d195-539">Essa propriedade é herdada do [**CIM \_ adaptador**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-539">This property is inherited from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="1d195-540">Para obter mais informações sobre como usar valores de **UInt64** em scripts, consulte [scripts no WMI](/previous-versions//aa393262(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="1d195-540">For more information about using **uint64** values in scripts, see [Scripting in WMI](/previous-versions//aa393262(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-541">**Status**</span><span class="sxs-lookup"><span data-stu-id="1d195-541">**Status**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-542">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-542">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-543">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-543">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-544">Qualificadores: [**maxlen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("status")</span><span class="sxs-lookup"><span data-stu-id="1d195-544">Qualifiers: [**MaxLen**](../wmisdk/standard-qualifiers.md) (10), [**DisplayName**](../wmisdk/standard-qualifiers.md) ("Status")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-545">Status atual do objeto.</span><span class="sxs-lookup"><span data-stu-id="1d195-545">Current status of the object.</span></span> <span data-ttu-id="1d195-546">Essa propriedade é herdada do [**CIM \_ ManagedSystemElement**](cim-managedsystemelement.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-546">This property is inherited from [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md).</span></span>

<span data-ttu-id="1d195-547">Os valores incluem o seguinte:</span><span class="sxs-lookup"><span data-stu-id="1d195-547">Values include the following:</span></span>

<dt>

<span id="OK"></span><span id="ok"></span>

<span data-ttu-id="1d195-548">**OK** ("OK")</span><span class="sxs-lookup"><span data-stu-id="1d195-548">**OK** ("OK")</span></span>


</dt> <dd></dd> <dt>

<span id="Error"></span><span id="error"></span><span id="ERROR"></span>

<span data-ttu-id="1d195-549">**Erro** ("erro")</span><span class="sxs-lookup"><span data-stu-id="1d195-549">**Error** ("Error")</span></span>


</dt> <dd></dd> <dt>

<span id="Degraded"></span><span id="degraded"></span><span id="DEGRADED"></span>

<span data-ttu-id="1d195-550">**Degradado** ("degradado")</span><span class="sxs-lookup"><span data-stu-id="1d195-550">**Degraded** ("Degraded")</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d195-551">**Desconhecido** ("desconhecido")</span><span class="sxs-lookup"><span data-stu-id="1d195-551">**Unknown** ("Unknown")</span></span>


</dt> <dd></dd> <dt>

<span id="Pred_Fail"></span><span id="pred_fail"></span><span id="PRED_FAIL"></span>

<span data-ttu-id="1d195-552">**Falha de Pred** ("Pred Fail")</span><span class="sxs-lookup"><span data-stu-id="1d195-552">**Pred Fail** ("Pred Fail")</span></span>


</dt> <dd></dd> <dt>

<span id="Starting"></span><span id="starting"></span><span id="STARTING"></span>

<span data-ttu-id="1d195-553">**Iniciando** ("Iniciando")</span><span class="sxs-lookup"><span data-stu-id="1d195-553">**Starting** ("Starting")</span></span>


</dt> <dd></dd> <dt>

<span id="Stopping"></span><span id="stopping"></span><span id="STOPPING"></span>

<span data-ttu-id="1d195-554">**Parando** ("parando")</span><span class="sxs-lookup"><span data-stu-id="1d195-554">**Stopping** ("Stopping")</span></span>


</dt> <dd></dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span data-ttu-id="1d195-555">**Serviço** ("serviço")</span><span class="sxs-lookup"><span data-stu-id="1d195-555">**Service** ("Service")</span></span>


</dt> <dd></dd> <dt>

<span id="Stressed"></span><span id="stressed"></span><span id="STRESSED"></span>

<span data-ttu-id="1d195-556">**Sob estresse** ("sob estresse")</span><span class="sxs-lookup"><span data-stu-id="1d195-556">**Stressed** ("Stressed")</span></span>


</dt> <dd></dd> <dt>

<span id="NonRecover"></span><span id="nonrecover"></span><span id="NONRECOVER"></span>

<span data-ttu-id="1d195-557">Não **recuperar** ("Recover")</span><span class="sxs-lookup"><span data-stu-id="1d195-557">**NonRecover** ("NonRecover")</span></span>


</dt> <dd></dd> <dt>

<span id="No_Contact"></span><span id="no_contact"></span><span id="NO_CONTACT"></span>

<span data-ttu-id="1d195-558">**Sem contato** ("sem contato")</span><span class="sxs-lookup"><span data-stu-id="1d195-558">**No Contact** ("No Contact")</span></span>


</dt> <dd></dd> <dt>

<span id="Lost_Comm"></span><span id="lost_comm"></span><span id="LOST_COMM"></span>

<span data-ttu-id="1d195-559">**Perda de comunicação** ("perda de comunicação")</span><span class="sxs-lookup"><span data-stu-id="1d195-559">**Lost Comm** ("Lost Comm")</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d195-560">**StatusInfo**</span><span class="sxs-lookup"><span data-stu-id="1d195-560">**StatusInfo**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-561">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="1d195-561">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-562">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-562">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-563">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF. \|Estado operacional da DMTF \| 3,3 ")</span><span class="sxs-lookup"><span data-stu-id="1d195-563">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("MIF.DMTF\|Operational State\|003.3")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-564">Estado do dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="1d195-564">State of the logical device.</span></span> <span data-ttu-id="1d195-565">Se essa propriedade não se aplicar ao dispositivo lógico, o valor 5 (não aplicável) deverá ser usado.</span><span class="sxs-lookup"><span data-stu-id="1d195-565">If this property does not apply to the logical device, the value 5 (Not Applicable) should be used.</span></span>

<span data-ttu-id="1d195-566">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-566">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

<dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="1d195-567">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="1d195-567">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="1d195-568">**Desconhecido** (2)</span><span class="sxs-lookup"><span data-stu-id="1d195-568">**Unknown** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="1d195-569">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="1d195-569">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="1d195-570">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="1d195-570">**Disabled** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="1d195-571">**Não aplicável** (5)</span><span class="sxs-lookup"><span data-stu-id="1d195-571">**Not Applicable** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="1d195-572">**SystemCreationClassName**</span><span class="sxs-lookup"><span data-stu-id="1d195-572">**SystemCreationClassName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-573">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-573">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-574">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-574">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-575">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**CreationClassName**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1d195-575">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**CreationClassName**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1d195-576">Valor da propriedade **CreationClassName** do computador de escopo.</span><span class="sxs-lookup"><span data-stu-id="1d195-576">Value of the scoping computer's **CreationClassName** property.</span></span>

<span data-ttu-id="1d195-577">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-577">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-578">**SystemName**</span><span class="sxs-lookup"><span data-stu-id="1d195-578">**SystemName**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-579">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="1d195-579">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-580">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-580">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-581">Qualificadores: [**propagados**](../wmisdk/standard-qualifiers.md) ([**" \_ sistema CIM**](cim-system.md).**Name**"), [**\_ chave CIM**](../wmisdk/standard-wmi-qualifiers.md)</span><span class="sxs-lookup"><span data-stu-id="1d195-581">Qualifiers: [**Propagated**](../wmisdk/standard-qualifiers.md) ("[**CIM\_System**](cim-system.md).**Name**"), [**CIM\_Key**](../wmisdk/standard-wmi-qualifiers.md)</span></span>
</dt> </dl>

<span data-ttu-id="1d195-582">Nome do sistema de escopo.</span><span class="sxs-lookup"><span data-stu-id="1d195-582">Name of the scoping system.</span></span>

<span data-ttu-id="1d195-583">Essa propriedade é herdada [**de \_ LogicalDevice CIM**](cim-logicaldevice.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-583">This property is inherited from [**CIM\_LogicalDevice**](cim-logicaldevice.md).</span></span>

</dd> <dt>

<span data-ttu-id="1d195-584">**TimeOfLastReset**</span><span class="sxs-lookup"><span data-stu-id="1d195-584">**TimeOfLastReset**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="1d195-585">Tipo de dados: **DateTime**</span><span class="sxs-lookup"><span data-stu-id="1d195-585">Data type: **datetime**</span></span>
</dt> <dt>

<span data-ttu-id="1d195-586">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="1d195-586">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="1d195-587">Qualificadores: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("software \\ \\ Microsoft \\ \\ Windows NT \\ \\ CurrentVersion \\ \\ Perflib \\ \\ 009 \| System up time")</span><span class="sxs-lookup"><span data-stu-id="1d195-587">Qualifiers: [**MappingStrings**](../wmisdk/standard-qualifiers.md) ("SOFTWARE\\\\Microsoft\\\\Windows NT\\\\CurrentVersion\\\\Perflib\\\\009\|System Up Time")</span></span>
</dt> </dl>

<span data-ttu-id="1d195-588">Data e hora da última redefinição do adaptador de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-588">Date and time the network adapter was last reset.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="1d195-589">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d195-589">Remarks</span></span>

<span data-ttu-id="1d195-590">A classe **Win32 \_ adaptador** é derivada de [**CIM \_ adaptador**](cim-networkadapter.md).</span><span class="sxs-lookup"><span data-stu-id="1d195-590">The **Win32\_NetworkAdapter** class is derived from [**CIM\_NetworkAdapter**](cim-networkadapter.md).</span></span>

<span data-ttu-id="1d195-591">A lista a seguir descreve as classes de associador do **Win32 \_ adaptador**:</span><span class="sxs-lookup"><span data-stu-id="1d195-591">The following list describes the Associator classes for **Win32\_NetworkAdapter**:</span></span>

-   [<span data-ttu-id="1d195-592">**\_PnPEntity Win32**</span><span class="sxs-lookup"><span data-stu-id="1d195-592">**Win32\_PnPEntity**</span></span>](win32-pnpentity.md)
-   [<span data-ttu-id="1d195-593">**\_Sistema de ComputerSystem Win32**</span><span class="sxs-lookup"><span data-stu-id="1d195-593">**Win32\_ComputerSystem**</span></span>](win32-computersystem.md)
-   [<span data-ttu-id="1d195-594">**\_NetworkAdapterConfiguration Win32**</span><span class="sxs-lookup"><span data-stu-id="1d195-594">**Win32\_NetworkAdapterConfiguration**</span></span>](win32-networkadapterconfiguration.md)
-   [<span data-ttu-id="1d195-595">**\_IRQResource Win32**</span><span class="sxs-lookup"><span data-stu-id="1d195-595">**Win32\_IRQResource**</span></span>](win32-irqresource.md)
-   [<span data-ttu-id="1d195-596">**\_DeviceMemoryAddress Win32**</span><span class="sxs-lookup"><span data-stu-id="1d195-596">**Win32\_DeviceMemoryAddress**</span></span>](win32-devicememoryaddress.md)
-   [<span data-ttu-id="1d195-597">**\_PortResource Win32**</span><span class="sxs-lookup"><span data-stu-id="1d195-597">**Win32\_PortResource**</span></span>](win32-portresource.md)
-   [<span data-ttu-id="1d195-598">**\_NetworkProtocol Win32**</span><span class="sxs-lookup"><span data-stu-id="1d195-598">**Win32\_NetworkProtocol**</span></span>](win32-networkprotocol.md)
-   [<span data-ttu-id="1d195-599">**Systemdrive do Win32 \_**</span><span class="sxs-lookup"><span data-stu-id="1d195-599">**Win32\_SystemDriver**</span></span>](win32-systemdriver.md)

<span data-ttu-id="1d195-600">Muitos sistemas têm vários adaptadores de rede.</span><span class="sxs-lookup"><span data-stu-id="1d195-600">Many systems have a number of network adapters on them.</span></span> <span data-ttu-id="1d195-601">Considere o uso do seguinte como referência para localizar os adaptadores atuais:</span><span class="sxs-lookup"><span data-stu-id="1d195-601">Consider using the following as a reference to find the current adapters:</span></span>

``` syntax
AdapterType: "Ethernet 802.3"
MACAddress: String Length > 16
Availability: 3
PNPDeviceID: InStr ( PNPDeviceID, "PCI") = 1
Installed: vbTrue
ConfigManagerErrorCode: 0
: <keep this as an index to Win32_NetworkAdapterConfiguration>
```

<span data-ttu-id="1d195-602">Mesmo usando os qualificadores acima, você provavelmente recuperará mais de um adaptador de rede válido.</span><span class="sxs-lookup"><span data-stu-id="1d195-602">Even using the above qualifiers, you will likely retrieve more than one valid network adapter.</span></span> <span data-ttu-id="1d195-603">Se esse for o caso, você poderá usar as informações a seguir para qualificar ainda mais sua pesquisa do Win32 \_ NetworkAdapterConfiguration:</span><span class="sxs-lookup"><span data-stu-id="1d195-603">If that is the case, Then you can use the following information to further qualify your search of the Win32\_NetworkAdapterConfiguration:</span></span>

``` syntax
Index: <match to DeviceID above>
MACAddress: Length > 16
DefaultIPGateway: String Length > 6
DNSServerSearchOrder: Array of strings with length > 6
IPEnabled: vbTrue
IPAddress: Array of strings with length > 6
```

<span data-ttu-id="1d195-604">Depois de fazer isso, você provavelmente terá reduzido sua lista para um ou dois adaptadores configurados.</span><span class="sxs-lookup"><span data-stu-id="1d195-604">Once you have done so, you will likely have reduced your list to one or two configured adapters.</span></span>

<span data-ttu-id="1d195-605">Você também pode usar o procedimento a seguir para localizar o adaptador padrão:</span><span class="sxs-lookup"><span data-stu-id="1d195-605">You can also use the following procedure to find the default adapter:</span></span>

1.  <span data-ttu-id="1d195-606">Execute a seguinte consulta:</span><span class="sxs-lookup"><span data-stu-id="1d195-606">Run the following query:</span></span>

    `"SELECT InterfaceIndex, Destination FROM Win32_IP4RouteTable WHERE Destination='0.0.0.0'"`

    <span data-ttu-id="1d195-607">Você deve ter apenas um destino de rede padrão 0.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="1d195-607">You should only have one default network destination 0.0.0.0.</span></span>

2.  <span data-ttu-id="1d195-608">Use o **InterfaceIndex** para recuperar o adaptador de rede desejado.</span><span class="sxs-lookup"><span data-stu-id="1d195-608">Use the **InterfaceIndex** to retrieve the Network Adapter you want.</span></span>

    `"SELECT * FROM Win32_NetworkAdapter WHERE InterfaceIndex=" + insertVariableHere`

## <a name="examples"></a><span data-ttu-id="1d195-609">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1d195-609">Examples</span></span>

<span data-ttu-id="1d195-610">O exemplo de código do PowerShell de [duas funções do WMI](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) na galeria do TechNet usa o **Win32 \_ adaptador** para recriar o cmdlet [Get-netadapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) do Windows.</span><span class="sxs-lookup"><span data-stu-id="1d195-610">The [Two WMI Functions](https://Gallery.TechNet.Microsoft.Com/Two-WMI-Functions-94c31b5f) PowerShell code example in the TechNet Gallery uses **Win32\_NetworkAdapter** to re-create the Windows [Get-NetAdapter](/powershell/module/netadapter/get-netadapter?view=win10-ps) cmdlet.</span></span>

<span data-ttu-id="1d195-611">As [informações do computador get-ComputerInfo-Query de computadores locais/remotos-(WMI) exemplo do](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell na galeria do TechNet usam várias chamadas para hardware e software, incluindo **Win32 \_ adaptador**, para exibir informações sobre um sistema local ou remoto.</span><span class="sxs-lookup"><span data-stu-id="1d195-611">The [Get-ComputerInfo - Query Computer Info From Local/Remote Computers - (WMI)](https://Gallery.TechNet.Microsoft.Com/Get-ComputerInfo-Query-23dd6042) PowerShell sample on TechNet Gallery uses a number of calls to hardware and software, including **Win32\_NetworkAdapter**, to display information about a local or remote system.</span></span>

<span data-ttu-id="1d195-612">O exemplo de código C a seguir \# usa o namespace [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) para recuperar os adaptadores de rede atuais no computador local.</span><span class="sxs-lookup"><span data-stu-id="1d195-612">The following C\# code sample uses [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) namespace to retrieve the current network adapters on the local machine.</span></span>


```CSharp
using Microsoft.Management.Infrastructure;
...
static void QueryInstanceFunc()
        {
 
            CimSession session = CimSession.Create("localHost");
            IEnumerable<CimInstance> queryInstance = session.QueryInstances(@"root\cimv2", "WQL", "SELECT * FROM Win32_NetworkAdapter");

            foreach (CimInstance cimObj in queryInstance)
            {
                Console.WriteLine(cimObj.CimInstanceProperties["Name"].ToString());
                Console.WriteLine(cimObj.CimInstanceProperties["Description"].ToString());
                Console.WriteLine();
            }

            Console.ReadLine();
        }
```



<span data-ttu-id="1d195-613">O exemplo de código C a seguir \# usa https://msdn.microsoft.com/library/system.management.aspx o namespace para recuperar os adaptadores de rede atuais no computador local.</span><span class="sxs-lookup"><span data-stu-id="1d195-613">The following C\# code sample uses https://msdn.microsoft.com/library/system.management.aspx namespace to retrieve the current network adapters on the local machine.</span></span>

> [!Note]  
> <span data-ttu-id="1d195-614"> https://msdn.microsoft.com/library/system.management.aspx contém as classes originais usadas para acessar o WMI; no entanto, eles são considerados mais lentos e geralmente não são dimensionados, bem como seus equivalentes de [Microsoft. Management. Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1d195-614">https://msdn.microsoft.com/library/system.management.aspx contains the original classes used to access WMI; however, they are considered slower and generally do not scale as well as their [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958(v=vs.85)) counterparts.</span></span>

 


```CSharp
using System.Management;
...
        static void oldSchoolQueryInstanceFunc()
        {

            ObjectQuery query = new ObjectQuery("SELECT * FROM Win32_NetworkAdapter");
            ManagementObjectSearcher searcher = new ManagementObjectSearcher(query);


            ManagementObjectCollection queryCollection = searcher.Get();
            foreach (ManagementObject m in queryCollection)
            {
                Console.WriteLine("ServiceName : {0}", m["Name"]);
                Console.WriteLine("MACAddress : {0}", m["Description"]);
                Console.WriteLine();
            }
            Console.ReadLine();

        }
```



<span data-ttu-id="1d195-615">O exemplo de código VBScript a seguir descreve como recuperar os adaptadores de rede atuais no computador local.</span><span class="sxs-lookup"><span data-stu-id="1d195-615">The following VBScript code sample describes how to retrieve the current network adapters on the local machine.</span></span>


```VB
strComputer = "." 
Set objWMIService = GetObject("winmgmts:\\" & strComputer & "\root\CIMV2") 
Set colItems = objWMIService.ExecQuery("SELECT * FROM Win32_NetworkAdapter")

For Each objItem in colItems 
    Wscript.Echo "Name: " & objItem.Name
    Wscript.Echo "Description: " & objItem.Description
    Wscript.Echo
Next
```



## <a name="requirements"></a><span data-ttu-id="1d195-616">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d195-616">Requirements</span></span>



| <span data-ttu-id="1d195-617">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d195-617">Requirement</span></span> | <span data-ttu-id="1d195-618">Valor</span><span class="sxs-lookup"><span data-stu-id="1d195-618">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="1d195-619">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d195-619">Minimum supported client</span></span><br/> | <span data-ttu-id="1d195-620">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="1d195-620">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="1d195-621">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1d195-621">Minimum supported server</span></span><br/> | <span data-ttu-id="1d195-622">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="1d195-622">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="1d195-623">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d195-623">Namespace</span></span><br/>                | <span data-ttu-id="1d195-624">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="1d195-624">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="1d195-625">MOF</span><span class="sxs-lookup"><span data-stu-id="1d195-625">MOF</span></span><br/>                      | <dl> <span data-ttu-id="1d195-626"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="1d195-626"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="1d195-627">DLL</span><span class="sxs-lookup"><span data-stu-id="1d195-627">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1d195-628"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1d195-628"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d195-629">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d195-629">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d195-630">**\_Adaptador CIM**</span><span class="sxs-lookup"><span data-stu-id="1d195-630">**CIM\_NetworkAdapter**</span></span>](cim-networkadapter.md)
</dt> <dt>

[<span data-ttu-id="1d195-631">Classes de hardware do sistema de computador</span><span class="sxs-lookup"><span data-stu-id="1d195-631">Computer System Hardware Classes</span></span>](computer-system-hardware-classes.md)
</dt> <dt>

[<span data-ttu-id="1d195-632">Tarefas do WMI: rede</span><span class="sxs-lookup"><span data-stu-id="1d195-632">WMI Tasks: Networking</span></span>](../wmisdk/wmi-tasks--networking.md)
</dt> <dt>

[<span data-ttu-id="1d195-633">Suporte a IPv6 e IPv4 no WMI</span><span class="sxs-lookup"><span data-stu-id="1d195-633">IPv6 and IPv4 Support in WMI</span></span>](../wmisdk/ipv6-and-ipv4-support-in-wmi.md)
</dt> </dl>

 

 
