---
description: Uma representação lógica de uma porta de rede em um dispositivo de rede.
ms.assetid: afcfc93d-174e-43b5-a16f-28937b4bf81a
title: Classe CIM_NetworkPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_NetworkPort
- CIM_NetworkPort.Speed
- CIM_NetworkPort.OtherNetworkPortType
- CIM_NetworkPort.PortNumber
- CIM_NetworkPort.LinkTechnology
- CIM_NetworkPort.OtherLinkTechnology
- CIM_NetworkPort.PermanentAddress
- CIM_NetworkPort.NetworkAddresses
- CIM_NetworkPort.FullDuplex
- CIM_NetworkPort.AutoSense
- CIM_NetworkPort.SupportedMaximumTransmissionUnit
- CIM_NetworkPort.ActiveMaximumTransmissionUnit
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 9e3ac64b55e17d0526527ebbaca168c3f7b289f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104171303"
---
# <a name="cim_networkport-class"></a><span data-ttu-id="55b01-103">\_Classe CIM NetworkPort</span><span class="sxs-lookup"><span data-stu-id="55b01-103">CIM\_NetworkPort class</span></span>

<span data-ttu-id="55b01-104">Uma representação lógica de uma porta de rede em um dispositivo de rede.</span><span class="sxs-lookup"><span data-stu-id="55b01-104">A logical representation of a network port on a network device.</span></span>

## <a name="syntax"></a><span data-ttu-id="55b01-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55b01-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_NetworkPort : CIM_LogicalPort
{
  uint64  Speed;
  string  OtherNetworkPortType;
  uint16  PortNumber;
  uint16  LinkTechnology;
  string  OtherLinkTechnology;
  string  PermanentAddress;
  string  NetworkAddresses[];
  boolean FullDuplex;
  boolean AutoSense;
  uint64  SupportedMaximumTransmissionUnit;
  uint64  ActiveMaximumTransmissionUnit;
};
```

## <a name="members"></a><span data-ttu-id="55b01-106">Membros</span><span class="sxs-lookup"><span data-stu-id="55b01-106">Members</span></span>

<span data-ttu-id="55b01-107">A classe **CIM \_ NetworkPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="55b01-107">The **CIM\_NetworkPort** class has these types of members:</span></span>

-   [<span data-ttu-id="55b01-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55b01-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="55b01-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="55b01-109">Properties</span></span>

<span data-ttu-id="55b01-110">A classe **CIM \_ NetworkPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="55b01-110">The **CIM\_NetworkPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="55b01-111">**ActiveMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="55b01-111">**ActiveMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-112">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55b01-112">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b01-114">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")</span><span class="sxs-lookup"><span data-stu-id="55b01-114">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="55b01-115">A unidade de transmissão máxima (MTU) negociada ou ativa que é suportada pela porta.</span><span class="sxs-lookup"><span data-stu-id="55b01-115">The active or negotiated maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> <dt>

<span data-ttu-id="55b01-116">**Autodetecção**</span><span class="sxs-lookup"><span data-stu-id="55b01-116">**AutoSense**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-117">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="55b01-117">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-118">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55b01-119">**true** se a porta puder determinar automaticamente a velocidade ou outras características de comunicação da mídia de rede anexada; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="55b01-119">**true** if the port can automatically determine the speed or other communications characteristic of the attached network media; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="55b01-120">**FullDuplex**</span><span class="sxs-lookup"><span data-stu-id="55b01-120">**FullDuplex**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-121">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="55b01-121">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-122">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55b01-123">**true** se a porta estiver operando no modo full duplex; caso contrário, **false**.</span><span class="sxs-lookup"><span data-stu-id="55b01-123">**true** if the port is operating in full duplex mode; otherwise, **false**.</span></span>

</dd> <dt>

<span data-ttu-id="55b01-124">**LinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="55b01-124">**LinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-125">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55b01-125">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-126">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-126">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b01-127">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**OtherLinkTechnology**")</span><span class="sxs-lookup"><span data-stu-id="55b01-127">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**OtherLinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="55b01-128">A tecnologia de link usada pela porta.</span><span class="sxs-lookup"><span data-stu-id="55b01-128">The link technology used by the port.</span></span> <span data-ttu-id="55b01-129">Quando definido como "1" (outro), a propriedade **OtherLinkTechnology** contém uma descrição do tipo de link.</span><span class="sxs-lookup"><span data-stu-id="55b01-129">When set to "1" (other), the **OtherLinkTechnology** property contains a description of the link type.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="55b01-130">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="55b01-130">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="55b01-131">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="55b01-131">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Ethernet"></span><span id="ethernet"></span><span id="ETHERNET"></span>

<span data-ttu-id="55b01-132">**Ethernet** (2)</span><span class="sxs-lookup"><span data-stu-id="55b01-132">**Ethernet** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="IB"></span><span id="ib"></span>

<span data-ttu-id="55b01-133">**IB** (3)</span><span class="sxs-lookup"><span data-stu-id="55b01-133">**IB** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FC"></span><span id="fc"></span>

<span data-ttu-id="55b01-134">**FC** (4)</span><span class="sxs-lookup"><span data-stu-id="55b01-134">**FC** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="FDDI"></span><span id="fddi"></span>

<span data-ttu-id="55b01-135">**FDDI** (5)</span><span class="sxs-lookup"><span data-stu-id="55b01-135">**FDDI** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="ATM"></span><span id="atm"></span>

<span data-ttu-id="55b01-136">**ATM** (6)</span><span class="sxs-lookup"><span data-stu-id="55b01-136">**ATM** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="Token_Ring"></span><span id="token_ring"></span><span id="TOKEN_RING"></span>

<span data-ttu-id="55b01-137">**Token ring** (7)</span><span class="sxs-lookup"><span data-stu-id="55b01-137">**Token Ring** (7)</span></span>


</dt> <dd></dd> <dt>

<span id="Frame_Relay"></span><span id="frame_relay"></span><span id="FRAME_RELAY"></span>

<span data-ttu-id="55b01-138">**Frame Relay** (8)</span><span class="sxs-lookup"><span data-stu-id="55b01-138">**Frame Relay** (8)</span></span>


</dt> <dd></dd> <dt>

<span id="Infrared"></span><span id="infrared"></span><span id="INFRARED"></span>

<span data-ttu-id="55b01-139">**Infravermelho** (9)</span><span class="sxs-lookup"><span data-stu-id="55b01-139">**Infrared** (9)</span></span>


</dt> <dd></dd> <dt>

<span id="BlueTooth"></span><span id="bluetooth"></span><span id="BLUETOOTH"></span>

<span data-ttu-id="55b01-140">**Bluetooth** (10)</span><span class="sxs-lookup"><span data-stu-id="55b01-140">**BlueTooth** (10)</span></span>


</dt> <dd></dd> <dt>

<span id="Wireless_LAN"></span><span id="wireless_lan"></span><span id="WIRELESS_LAN"></span>

<span data-ttu-id="55b01-141">**LAN sem fio** (11)</span><span class="sxs-lookup"><span data-stu-id="55b01-141">**Wireless LAN** (11)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="55b01-142">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="55b01-142">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-143">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55b01-143">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="55b01-144">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-144">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b01-145">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adaptador de rede DMTF 802 porta \| 1,3 ")</span><span class="sxs-lookup"><span data-stu-id="55b01-145">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.3")</span></span>
</dt> </dl>

<span data-ttu-id="55b01-146">Uma matriz que contém os endereços de rede para a porta.</span><span class="sxs-lookup"><span data-stu-id="55b01-146">An array that contains the network addresses for the port.</span></span>

</dd> <dt>

<span data-ttu-id="55b01-147">**OtherLinkTechnology**</span><span class="sxs-lookup"><span data-stu-id="55b01-147">**OtherLinkTechnology**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-148">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55b01-148">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-149">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-149">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b01-150">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ NetworkPort**.**LinkTechnology**")</span><span class="sxs-lookup"><span data-stu-id="55b01-150">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_NetworkPort**.**LinkTechnology**")</span></span>
</dt> </dl>

<span data-ttu-id="55b01-151">A tecnologia de link quando **LinkTechnology** é definido como "1", (outro).</span><span class="sxs-lookup"><span data-stu-id="55b01-151">The link technology when **LinkTechnology** is set to "1", (other).</span></span>

</dd> <dt>

<span data-ttu-id="55b01-152">**OtherNetworkPortType**</span><span class="sxs-lookup"><span data-stu-id="55b01-152">**OtherNetworkPortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-153">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55b01-153">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b01-155">Qualificadores: [**preteridos**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM \_ NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ LogicalPort**](cim-logicalport.md).**PortType**")</span><span class="sxs-lookup"><span data-stu-id="55b01-155">Qualifiers: [**Deprecated**](/windows/desktop/WmiSdk/standard-wmi-qualifiers) ("**CIM\_NetworkPort**.**OtherPortType**"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_LogicalPort**](cim-logicalport.md).**PortType**")</span></span>
</dt> </dl>

> [!Note]  
> <span data-ttu-id="55b01-156">Descrição preterida: o tipo de módulo da porta, quando a propriedade **PortType** contém 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="55b01-156">Deprecated description: The module type of the port, when the **PortType** property contains 1 (other).</span></span>

 

<span data-ttu-id="55b01-157">Essa propriedade é preterida.</span><span class="sxs-lookup"><span data-stu-id="55b01-157">This property is deprecated.</span></span> <span data-ttu-id="55b01-158">Em vez disso, recomendamos a propriedade **PortType** na classe [**CIM \_ LogicalPort**](cim-logicalport.md) .</span><span class="sxs-lookup"><span data-stu-id="55b01-158">Instead, we recommend the **PortType** property in the [**CIM\_LogicalPort**](cim-logicalport.md) class.</span></span>

</dd> <dt>

<span data-ttu-id="55b01-159">**PermanentAddress**</span><span class="sxs-lookup"><span data-stu-id="55b01-159">**PermanentAddress**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-160">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="55b01-160">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-161">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-161">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b01-162">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF. \|Adaptador de rede DMTF 802 porta \| 1,2 ")</span><span class="sxs-lookup"><span data-stu-id="55b01-162">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIF.DMTF\|Network Adapter 802 Port\|001.2")</span></span>
</dt> </dl>

<span data-ttu-id="55b01-163">O endereço de rede embutido em uma porta.</span><span class="sxs-lookup"><span data-stu-id="55b01-163">The network address that is hardcoded into a port.</span></span> <span data-ttu-id="55b01-164">O endereço codificado pode ser alterado usando uma atualização de firmware ou uma configuração de software.</span><span class="sxs-lookup"><span data-stu-id="55b01-164">The hardcoded address can be changed using a firmware upgrade or a software configuration.</span></span> <span data-ttu-id="55b01-165">Quando essa alteração é feita, essa propriedade deve ser atualizada ao mesmo tempo.</span><span class="sxs-lookup"><span data-stu-id="55b01-165">When this change is made, this property should be updated at the same time.</span></span> <span data-ttu-id="55b01-166">**PermanentAddress** deverá ser deixado em branco se o endereço não existir.</span><span class="sxs-lookup"><span data-stu-id="55b01-166">**PermanentAddress** should be left blank if the address doesn't exist.</span></span>

</dd> <dt>

<span data-ttu-id="55b01-167">**PortNumber**</span><span class="sxs-lookup"><span data-stu-id="55b01-167">**PortNumber**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-168">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="55b01-168">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-169">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-169">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="55b01-170">O número da porta da porta de rede.</span><span class="sxs-lookup"><span data-stu-id="55b01-170">The port number of the network port.</span></span> <span data-ttu-id="55b01-171">As portas de rede geralmente são numeradas em relação a um módulo lógico ou um elemento de rede.</span><span class="sxs-lookup"><span data-stu-id="55b01-171">Network ports are often numbered relative to either a logical module or a network element.</span></span>

</dd> <dt>

<span data-ttu-id="55b01-172">**Velocidade**</span><span class="sxs-lookup"><span data-stu-id="55b01-172">**Speed**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-173">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55b01-173">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-174">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-174">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b01-175">Qualificadores: [**substituir**](/windows/desktop/WmiSdk/standard-qualifiers) ("velocidade"), [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bits por segundo"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| MIB-II. ifSpeed "," MIF. \|Adaptador de rede DMTF 802 porta \| 1,5 "), **PUnit** (" bit/segundo ")</span><span class="sxs-lookup"><span data-stu-id="55b01-175">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Speed"), [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bits per Second"), [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|MIB-II.ifSpeed", "MIF.DMTF\|Network Adapter 802 Port\|001.5"), **PUnit** ("bit / second")</span></span>
</dt> </dl>

<span data-ttu-id="55b01-176">A largura de banda atual da porta em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="55b01-176">The current bandwidth of the port in bits per second.</span></span> <span data-ttu-id="55b01-177">Para portas que variam de largura de banda ou para aquelas em que não é possível fazer nenhuma estimativa precisa, essa propriedade deve conter a largura de banda nominal.</span><span class="sxs-lookup"><span data-stu-id="55b01-177">For ports that vary in bandwidth, or for those where no accurate estimation can be made, this property should contain the nominal bandwidth.</span></span>

</dd> <dt>

<span data-ttu-id="55b01-178">**SupportedMaximumTransmissionUnit**</span><span class="sxs-lookup"><span data-stu-id="55b01-178">**SupportedMaximumTransmissionUnit**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="55b01-179">Tipo de dados: **UInt64**</span><span class="sxs-lookup"><span data-stu-id="55b01-179">Data type: **uint64**</span></span>
</dt> <dt>

<span data-ttu-id="55b01-180">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="55b01-180">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="55b01-181">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("bytes"), **PUnit** ("byte")</span><span class="sxs-lookup"><span data-stu-id="55b01-181">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("Bytes"), **PUnit** ("byte")</span></span>
</dt> </dl>

<span data-ttu-id="55b01-182">A unidade máxima de transmissão (MTU) que é suportada pela porta.</span><span class="sxs-lookup"><span data-stu-id="55b01-182">The maximum transmission unit (MTU) that is supported by the port.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="55b01-183">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55b01-183">Requirements</span></span>



| <span data-ttu-id="55b01-184">Requisito</span><span class="sxs-lookup"><span data-stu-id="55b01-184">Requirement</span></span> | <span data-ttu-id="55b01-185">Valor</span><span class="sxs-lookup"><span data-stu-id="55b01-185">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55b01-186">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55b01-186">Minimum supported client</span></span><br/> | <span data-ttu-id="55b01-187">Windows 8</span><span class="sxs-lookup"><span data-stu-id="55b01-187">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="55b01-188">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="55b01-188">Minimum supported server</span></span><br/> | <span data-ttu-id="55b01-189">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="55b01-189">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="55b01-190">Namespace</span><span class="sxs-lookup"><span data-stu-id="55b01-190">Namespace</span></span><br/>                | <span data-ttu-id="55b01-191">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="55b01-191">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="55b01-192">MOF</span><span class="sxs-lookup"><span data-stu-id="55b01-192">MOF</span></span><br/>                      | <dl> <span data-ttu-id="55b01-193"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="55b01-193"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="55b01-194">DLL</span><span class="sxs-lookup"><span data-stu-id="55b01-194">DLL</span></span><br/>                      | <dl> <span data-ttu-id="55b01-195"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="55b01-195"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="55b01-196">Confira também</span><span class="sxs-lookup"><span data-stu-id="55b01-196">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55b01-197">**\_LOGICALPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="55b01-197">**CIM\_LogicalPort**</span></span>](cim-logicalport.md)
</dt> </dl>

 

