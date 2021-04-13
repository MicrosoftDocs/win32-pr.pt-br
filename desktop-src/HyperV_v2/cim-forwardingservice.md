---
description: Representa um serviço de encaminhamento para tráfego de rede. O serviço processa os pontos de extremidade de protocolo recebidos, descartando-os ou enviando-os para outros pontos de extremidade de protocolo.
ms.assetid: 366ae2bf-a436-4ad2-b212-39958a7fbc43
title: Classe CIM_ForwardingService
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ForwardingService
- CIM_ForwardingService.ProtocolType
- CIM_ForwardingService.OtherProtocolType
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 12ebb33d6c63b637c9342bd7a869993019abb26b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370577"
---
# <a name="cim_forwardingservice-class"></a><span data-ttu-id="73ca6-104">\_Classe CIM ForwardingService</span><span class="sxs-lookup"><span data-stu-id="73ca6-104">CIM\_ForwardingService class</span></span>

<span data-ttu-id="73ca6-105">Representa um serviço de encaminhamento para tráfego de rede.</span><span class="sxs-lookup"><span data-stu-id="73ca6-105">Represents a forwarding service for network traffic.</span></span> <span data-ttu-id="73ca6-106">O serviço processa os pontos de extremidade de protocolo recebidos, descartando-os ou enviando-os para outros pontos de extremidade de protocolo.</span><span class="sxs-lookup"><span data-stu-id="73ca6-106">The service processes packets received protocol endpoints by discarding them, or sending the packets to other protocol endpoints.</span></span>

## <a name="syntax"></a><span data-ttu-id="73ca6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73ca6-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.7.0"), UMLPackagePath("CIM::Network::RoutingForwarding"), AMENDMENT]
class CIM_ForwardingService : CIM_NetworkService
{
  uint16 ProtocolType;
  string OtherProtocolType;
};
```

## <a name="members"></a><span data-ttu-id="73ca6-108">Membros</span><span class="sxs-lookup"><span data-stu-id="73ca6-108">Members</span></span>

<span data-ttu-id="73ca6-109">A classe **CIM \_ ForwardingService** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="73ca6-109">The **CIM\_ForwardingService** class has these types of members:</span></span>

-   [<span data-ttu-id="73ca6-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73ca6-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="73ca6-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="73ca6-111">Properties</span></span>

<span data-ttu-id="73ca6-112">A classe **CIM \_ ForwardingService** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="73ca6-112">The **CIM\_ForwardingService** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="73ca6-113">**OtherProtocolType**</span><span class="sxs-lookup"><span data-stu-id="73ca6-113">**OtherProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73ca6-114">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="73ca6-114">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="73ca6-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73ca6-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73ca6-116">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ForwardingService**.**ProtocolType**")</span><span class="sxs-lookup"><span data-stu-id="73ca6-116">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (32), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ForwardingService**.**ProtocolType**")</span></span>
</dt> </dl>

<span data-ttu-id="73ca6-117">Define o tipo de protocolo a ser encaminhado quando o valor da propriedade **ProtocolType** é 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="73ca6-117">Defines the type of protocol to forward when the value of the **ProtocolType** property is 1 (Other).</span></span>

</dd> <dt>

<span data-ttu-id="73ca6-118">**ProtocolType**</span><span class="sxs-lookup"><span data-stu-id="73ca6-118">**ProtocolType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="73ca6-119">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="73ca6-119">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="73ca6-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="73ca6-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="73ca6-121">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ ForwardingService**.**OtherProtocolType**")</span><span class="sxs-lookup"><span data-stu-id="73ca6-121">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_ForwardingService**.**OtherProtocolType**")</span></span>
</dt> </dl>

<span data-ttu-id="73ca6-122">O tipo de protocolo a ser encaminhado.</span><span class="sxs-lookup"><span data-stu-id="73ca6-122">The type of protocol to forward.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="73ca6-123">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="73ca6-123">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="73ca6-124">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="73ca6-124">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4"></span><span id="ipv4"></span><span id="IPV4"></span>

<span data-ttu-id="73ca6-125">**IPv4** (2)</span><span class="sxs-lookup"><span data-stu-id="73ca6-125">**IPv4** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv6"></span><span id="ipv6"></span><span id="IPV6"></span>

<span data-ttu-id="73ca6-126">**IPv6** (3)</span><span class="sxs-lookup"><span data-stu-id="73ca6-126">**IPv6** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="IPv4_IPv6"></span><span id="ipv4_ipv6"></span><span id="IPV4_IPV6"></span>

<span data-ttu-id="73ca6-127">**IPv4/IPv6** (4)</span><span class="sxs-lookup"><span data-stu-id="73ca6-127">**IPv4/IPv6** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="IPX"></span><span id="ipx"></span>

<span data-ttu-id="73ca6-128">**IPX** (5)</span><span class="sxs-lookup"><span data-stu-id="73ca6-128">**IPX** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="AppleTalk"></span><span id="appletalk"></span><span id="APPLETALK"></span>

<span data-ttu-id="73ca6-129">**AppleTalk** (6)</span><span class="sxs-lookup"><span data-stu-id="73ca6-129">**AppleTalk** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DECnet"></span><span id="decnet"></span><span id="DECNET"></span>

<span data-ttu-id="73ca6-130">**DECnet** (7)</span><span class="sxs-lookup"><span data-stu-id="73ca6-130">**DECnet** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="SNA"></span><span id="sna"></span>

<span data-ttu-id="73ca6-131">**SNA** (8)</span><span class="sxs-lookup"><span data-stu-id="73ca6-131">**SNA** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="CONP"></span><span id="conp"></span>

<span data-ttu-id="73ca6-132">**CONP** (9)</span><span class="sxs-lookup"><span data-stu-id="73ca6-132">**CONP** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="CLNP"></span><span id="clnp"></span>

<span data-ttu-id="73ca6-133">**CLNP** (10)</span><span class="sxs-lookup"><span data-stu-id="73ca6-133">**CLNP** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="VINES"></span><span id="vines"></span>

<span data-ttu-id="73ca6-134">**Vines** (11)</span><span class="sxs-lookup"><span data-stu-id="73ca6-134">**VINES** (11)</span></span>


</dt> <dd></dd> <dt>

<span id="XNS"></span><span id="xns"></span>

<span data-ttu-id="73ca6-135">**XNS** (12)</span><span class="sxs-lookup"><span data-stu-id="73ca6-135">**XNS** (12)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="73ca6-136">**ATM** (13)</span><span class="sxs-lookup"><span data-stu-id="73ca6-136">**ATM** (13)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="73ca6-137">**Frame Relay** (14)</span><span class="sxs-lookup"><span data-stu-id="73ca6-137">**Frame Relay** (14)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="73ca6-138">**Ethernet** (15)</span><span class="sxs-lookup"><span data-stu-id="73ca6-138">**Ethernet** (15)</span></span>


</dt> <dd></dd> <dt>

<span id="TokenRing"></span><span id="tokenring"></span><span id="TOKENRING"></span>

<span data-ttu-id="73ca6-139">**Tokenring** (16)</span><span class="sxs-lookup"><span data-stu-id="73ca6-139">**TokenRing** (16)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="73ca6-140">**FDDI** (17)</span><span class="sxs-lookup"><span data-stu-id="73ca6-140">**FDDI** (17)</span></span>


</dt> <dd></dd> <dt>

<span id="Infiniband"></span><span id="infiniband"></span><span id="INFINIBAND"></span>

<span data-ttu-id="73ca6-141">**InfiniBand** (18)</span><span class="sxs-lookup"><span data-stu-id="73ca6-141">**Infiniband** (18)</span></span>


</dt> <dd></dd> <dt>

<span id="Fibre_Channel"></span><span id="fibre_channel"></span><span id="FIBRE_CHANNEL"></span>

<span data-ttu-id="73ca6-142">**Fibre Channel** (19)</span><span class="sxs-lookup"><span data-stu-id="73ca6-142">**Fibre Channel** (19)</span></span>


<span data-ttu-id="73ca6-143"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="73ca6-143"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="73ca6-144">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73ca6-144">Requirements</span></span>



| <span data-ttu-id="73ca6-145">Requisito</span><span class="sxs-lookup"><span data-stu-id="73ca6-145">Requirement</span></span> | <span data-ttu-id="73ca6-146">Valor</span><span class="sxs-lookup"><span data-stu-id="73ca6-146">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73ca6-147">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73ca6-147">Minimum supported client</span></span><br/> | <span data-ttu-id="73ca6-148">Windows 8</span><span class="sxs-lookup"><span data-stu-id="73ca6-148">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="73ca6-149">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="73ca6-149">Minimum supported server</span></span><br/> | <span data-ttu-id="73ca6-150">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="73ca6-150">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="73ca6-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="73ca6-151">Namespace</span></span><br/>                | <span data-ttu-id="73ca6-152">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="73ca6-152">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="73ca6-153">MOF</span><span class="sxs-lookup"><span data-stu-id="73ca6-153">MOF</span></span><br/>                      | <dl> <span data-ttu-id="73ca6-154"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="73ca6-154"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="73ca6-155">DLL</span><span class="sxs-lookup"><span data-stu-id="73ca6-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="73ca6-156"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="73ca6-156"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="73ca6-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="73ca6-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73ca6-158">**NetworkService do CIM \_**</span><span class="sxs-lookup"><span data-stu-id="73ca6-158">**CIM\_NetworkService**</span></span>](cim-networkservice.md)
</dt> </dl>

 

