---
description: Representa uma porta Ethernet.
ms.assetid: c9a148c2-cf02-466f-b8ca-b1bf616d75dc
title: Classe CIM_EthernetPort
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPort
- CIM_EthernetPort.PortType
- CIM_EthernetPort.NetworkAddresses
- CIM_EthernetPort.MaxDataSize
- CIM_EthernetPort.Capabilities
- CIM_EthernetPort.CapabilityDescriptions
- CIM_EthernetPort.EnabledCapabilities
- CIM_EthernetPort.OtherEnabledCapabilities
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a44e93f84178fa2714d3c823735b3d90922e04be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501279"
---
# <a name="cim_ethernetport-class"></a><span data-ttu-id="6691d-103">\_Classe CIM EthernetPort</span><span class="sxs-lookup"><span data-stu-id="6691d-103">CIM\_EthernetPort class</span></span>

<span data-ttu-id="6691d-104">Representa uma porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="6691d-104">Represents an ethernet port.</span></span>

## <a name="syntax"></a><span data-ttu-id="6691d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6691d-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.10.0"), UMLPackagePath("CIM::Device::Ports"), AMENDMENT]
class CIM_EthernetPort : CIM_NetworkPort
{
  uint16 PortType;
  string NetworkAddresses[];
  uint32 MaxDataSize;
  uint16 Capabilities[];
  string CapabilityDescriptions[];
  uint16 EnabledCapabilities[];
  string OtherEnabledCapabilities[];
};
```

## <a name="members"></a><span data-ttu-id="6691d-106">Membros</span><span class="sxs-lookup"><span data-stu-id="6691d-106">Members</span></span>

<span data-ttu-id="6691d-107">A classe **CIM \_ EthernetPort** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="6691d-107">The **CIM\_EthernetPort** class has these types of members:</span></span>

-   [<span data-ttu-id="6691d-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6691d-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="6691d-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="6691d-109">Properties</span></span>

<span data-ttu-id="6691d-110">A classe **CIM \_ EthernetPort** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="6691d-110">The **CIM\_EthernetPort** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="6691d-111">**Funcionalidades**</span><span class="sxs-lookup"><span data-stu-id="6691d-111">**Capabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6691d-112">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6691d-112">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6691d-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6691d-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6691d-114">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM EthernetPort**.**CapabilityDescriptions**")</span><span class="sxs-lookup"><span data-stu-id="6691d-114">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**CapabilityDescriptions**")</span></span>
</dt> </dl>

<span data-ttu-id="6691d-115">Os recursos da porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="6691d-115">The capabilities of the ethernet port.</span></span>

> [!Note]  
> <span data-ttu-id="6691d-116">Se os recursos de failover ou balanceamento de carga estiverem habilitados, um objeto de [**\_ reserva**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) CIM ou [**CIM \_ ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (balanceamento de carga) também deverá ser definido para descrever completamente o recurso.</span><span class="sxs-lookup"><span data-stu-id="6691d-116">If failover or load balancing capabilities are enabled, a [**CIM\_SpareGroup**](/windows/desktop/CIMWin32Prov/cim-sparegroup) (failover) or [**CIM\_ExtraCapacityGroup**](/windows/desktop/CIMWin32Prov/cim-extracapacitygroup) (load balancing) object should also be defined to completely describe the capability.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6691d-117">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="6691d-117">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6691d-118">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6691d-118">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="6691d-119">**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="6691d-119">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="6691d-120">**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="6691d-120">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="6691d-121">**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="6691d-121">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="6691d-122">**Balanceamento de carga** (5)</span><span class="sxs-lookup"><span data-stu-id="6691d-122">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6691d-123">**CapabilityDescriptions**</span><span class="sxs-lookup"><span data-stu-id="6691d-123">**CapabilityDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6691d-124">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6691d-124">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6691d-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6691d-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6691d-126">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM EthernetPort**.**Recursos**")</span><span class="sxs-lookup"><span data-stu-id="6691d-126">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="6691d-127">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos recursos indicados na matriz Capabilities.</span><span class="sxs-lookup"><span data-stu-id="6691d-127">An array of free-form strings that provides more detailed explanations for any of the features that are indicated in the Capabilities array.</span></span> <span data-ttu-id="6691d-128">Os itens nessa matriz correspondem aos itens na matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="6691d-128">The items in this array correspond to the items in the Capabilities array.</span></span>

</dd> <dt>

<span data-ttu-id="6691d-129">**EnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6691d-129">**EnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6691d-130">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6691d-130">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="6691d-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6691d-131">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6691d-132">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM EthernetPort**.**Recursos**","**CIM \_ EthernetPort**.**OtherEnabledCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="6691d-132">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**Capabilities**", "**CIM\_EthernetPort**.**OtherEnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="6691d-133">Indica quais funcionalidades estão habilitadas na matriz Capabilities.</span><span class="sxs-lookup"><span data-stu-id="6691d-133">Indicates which capabilities are enabled in the Capabilities array.</span></span> <span data-ttu-id="6691d-134">Os itens nessa matriz correspondem aos itens na matriz de recursos.</span><span class="sxs-lookup"><span data-stu-id="6691d-134">The items in this array correspond to the items in the Capabilities array.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6691d-135">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="6691d-135">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6691d-136">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6691d-136">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="AlertOnLan"></span><span id="alertonlan"></span><span id="ALERTONLAN"></span>

<span data-ttu-id="6691d-137">**AlertOnLan** (2)</span><span class="sxs-lookup"><span data-stu-id="6691d-137">**AlertOnLan** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="WakeOnLan"></span><span id="wakeonlan"></span><span id="WAKEONLAN"></span>

<span data-ttu-id="6691d-138">**WakeOnLan** (3)</span><span class="sxs-lookup"><span data-stu-id="6691d-138">**WakeOnLan** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="FailOver"></span><span id="failover"></span><span id="FAILOVER"></span>

<span data-ttu-id="6691d-139">**Failover** (4)</span><span class="sxs-lookup"><span data-stu-id="6691d-139">**FailOver** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="LoadBalancing"></span><span id="loadbalancing"></span><span id="LOADBALANCING"></span>

<span data-ttu-id="6691d-140">**Balanceamento de carga** (5)</span><span class="sxs-lookup"><span data-stu-id="6691d-140">**LoadBalancing** (5)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="6691d-141">**MaxDataSize**</span><span class="sxs-lookup"><span data-stu-id="6691d-141">**MaxDataSize**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6691d-142">Tipo de dados: **UInt32**</span><span class="sxs-lookup"><span data-stu-id="6691d-142">Data type: **uint32**</span></span>
</dt> <dt>

<span data-ttu-id="6691d-143">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6691d-143">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6691d-144">Qualificadores: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB. IETF \| Bridge-MIB. dot1dTpPortMaxInfo ")</span><span class="sxs-lookup"><span data-stu-id="6691d-144">Qualifiers: [**MappingStrings**](/windows/desktop/WmiSdk/standard-qualifiers) ("MIB.IETF\|BRIDGE-MIB.dot1dTpPortMaxInfo")</span></span>
</dt> </dl>

<span data-ttu-id="6691d-145">O tamanho máximo do campo de informações (não MAC) que será recebido ou transmitido.</span><span class="sxs-lookup"><span data-stu-id="6691d-145">The maximum size of the INFO (non-MAC) field that will be received or transmitted.</span></span>

</dd> <dt>

<span data-ttu-id="6691d-146">**NetworkAddresses**</span><span class="sxs-lookup"><span data-stu-id="6691d-146">**NetworkAddresses**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6691d-147">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6691d-147">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6691d-148">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6691d-148">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6691d-149">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span><span class="sxs-lookup"><span data-stu-id="6691d-149">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("NetworkAddresses")</span></span>
</dt> </dl>

<span data-ttu-id="6691d-150">Os endereços de rede atribuídos à porta.</span><span class="sxs-lookup"><span data-stu-id="6691d-150">The network addresses assigned to the port.</span></span> <span data-ttu-id="6691d-151">O endereço é um MAC 802,3 que é formatado como doze dígitos hexadecimais (por exemplo, "010203040506"), onde cada par de dígitos representa um dos seis octetos do endereço MAC na ordem de bits canônica.</span><span class="sxs-lookup"><span data-stu-id="6691d-151">The address is a 802.3 MAC that is formatted as twelve hexadecimal digits (for example, "010203040506"), where each pair of digits represents one of the six octets of the MAC address in canonical bit order.</span></span>

</dd> <dt>

<span data-ttu-id="6691d-152">**OtherEnabledCapabilities**</span><span class="sxs-lookup"><span data-stu-id="6691d-152">**OtherEnabledCapabilities**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6691d-153">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="6691d-153">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="6691d-154">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6691d-154">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6691d-155">Qualificadores: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("indexado"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) (**" \_ CIM EthernetPort**.**EnabledCapabilities**")</span><span class="sxs-lookup"><span data-stu-id="6691d-155">Qualifiers: [**ArrayType**](/windows/desktop/WmiSdk/standard-qualifiers) ("Indexed"), [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPort**.**EnabledCapabilities**")</span></span>
</dt> </dl>

<span data-ttu-id="6691d-156">Uma matriz de cadeias de caracteres de forma livre que fornece explicações mais detalhadas para qualquer um dos itens de matriz **EnabledCapabilities** que são definidos como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="6691d-156">An array of free-form strings that provide more detailed explanations for any of the **EnabledCapabilities** array items that are set to 1 (Other).</span></span> <span data-ttu-id="6691d-157">Os itens nessa matriz correspondem aos itens na matriz **EnabledCapabilities** .</span><span class="sxs-lookup"><span data-stu-id="6691d-157">The items in this array correspond to the items in the **EnabledCapabilities** array.</span></span>

</dd> <dt>

<span data-ttu-id="6691d-158">**PortType**</span><span class="sxs-lookup"><span data-stu-id="6691d-158">**PortType**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="6691d-159">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="6691d-159">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="6691d-160">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="6691d-160">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="6691d-161">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span><span class="sxs-lookup"><span data-stu-id="6691d-161">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PortType")</span></span>
</dt> </dl>

<span data-ttu-id="6691d-162">O modo que está habilitado na porta.</span><span class="sxs-lookup"><span data-stu-id="6691d-162">The mode that is enabled on the port.</span></span> <span data-ttu-id="6691d-163">Quando definido como 1 (outro), a propriedade **OtherPortType** descreve o modo.</span><span class="sxs-lookup"><span data-stu-id="6691d-163">When set to 1 (Other), the **OtherPortType** property describes the mode.</span></span>

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="6691d-164">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="6691d-164">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="6691d-165">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="6691d-165">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="10BaseT"></span><span id="10baset"></span><span id="10BASET"></span>

<span data-ttu-id="6691d-166">**10BaseT** (50)</span><span class="sxs-lookup"><span data-stu-id="6691d-166">**10BaseT** (50)</span></span>


</dt> <dd></dd> <dt>

<span id="10-100BaseT"></span><span id="10-100baset"></span><span id="10-100BASET"></span>

<span data-ttu-id="6691d-167">**10-100BaseT** (51)</span><span class="sxs-lookup"><span data-stu-id="6691d-167">**10-100BaseT** (51)</span></span>


</dt> <dd></dd> <dt>

<span id="100BaseT"></span><span id="100baset"></span><span id="100BASET"></span>

<span data-ttu-id="6691d-168">**100BaseT** (52)</span><span class="sxs-lookup"><span data-stu-id="6691d-168">**100BaseT** (52)</span></span>


</dt> <dd></dd> <dt>

<span id="1000BaseT"></span><span id="1000baset"></span><span id="1000BASET"></span>

<span data-ttu-id="6691d-169">**1000baseT** (53)</span><span class="sxs-lookup"><span data-stu-id="6691d-169">**1000BaseT** (53)</span></span>


</dt> <dd></dd> <dt>

<span id="2500BaseT"></span><span id="2500baset"></span><span id="2500BASET"></span>

<span data-ttu-id="6691d-170">**2500BaseT** (54)</span><span class="sxs-lookup"><span data-stu-id="6691d-170">**2500BaseT** (54)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBaseT"></span><span id="10gbaset"></span><span id="10GBASET"></span>

<span data-ttu-id="6691d-171">**10GBaseT** (55)</span><span class="sxs-lookup"><span data-stu-id="6691d-171">**10GBaseT** (55)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-CX4"></span><span id="10gbase-cx4"></span><span id="10GBASE-CX4"></span>

<span data-ttu-id="6691d-172">**10GBASE-CX4** (56)</span><span class="sxs-lookup"><span data-stu-id="6691d-172">**10GBase-CX4** (56)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-FX"></span><span id="100base-fx"></span><span id="100BASE-FX"></span>

<span data-ttu-id="6691d-173">**100BASE-FX** (100)</span><span class="sxs-lookup"><span data-stu-id="6691d-173">**100Base-FX** (100)</span></span>


</dt> <dd></dd> <dt>

<span id="100Base-SX"></span><span id="100base-sx"></span><span id="100BASE-SX"></span>

<span data-ttu-id="6691d-174">**100BASE-SX** (101)</span><span class="sxs-lookup"><span data-stu-id="6691d-174">**100Base-SX** (101)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-SX"></span><span id="1000base-sx"></span><span id="1000BASE-SX"></span>

<span data-ttu-id="6691d-175">**1000BASE-SX** (102)</span><span class="sxs-lookup"><span data-stu-id="6691d-175">**1000Base-SX** (102)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-LX"></span><span id="1000base-lx"></span><span id="1000BASE-LX"></span>

<span data-ttu-id="6691d-176">**1000BASE-LX** (103)</span><span class="sxs-lookup"><span data-stu-id="6691d-176">**1000Base-LX** (103)</span></span>


</dt> <dd></dd> <dt>

<span id="1000Base-CX"></span><span id="1000base-cx"></span><span id="1000BASE-CX"></span>

<span data-ttu-id="6691d-177">**1000BASE-CX** (104)</span><span class="sxs-lookup"><span data-stu-id="6691d-177">**1000Base-CX** (104)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SR"></span><span id="10gbase-sr"></span><span id="10GBASE-SR"></span>

<span data-ttu-id="6691d-178">**10GBASE-Sr** (105)</span><span class="sxs-lookup"><span data-stu-id="6691d-178">**10GBase-SR** (105)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-SW"></span><span id="10gbase-sw"></span><span id="10GBASE-SW"></span>

<span data-ttu-id="6691d-179">**10GBASE-SW** (106)</span><span class="sxs-lookup"><span data-stu-id="6691d-179">**10GBase-SW** (106)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LX4"></span><span id="10gbase-lx4"></span><span id="10GBASE-LX4"></span>

<span data-ttu-id="6691d-180">**10GBASE-LX4** (107)</span><span class="sxs-lookup"><span data-stu-id="6691d-180">**10GBase-LX4** (107)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LR"></span><span id="10gbase-lr"></span><span id="10GBASE-LR"></span>

<span data-ttu-id="6691d-181">**10GBASE-LR** (108)</span><span class="sxs-lookup"><span data-stu-id="6691d-181">**10GBase-LR** (108)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-LW"></span><span id="10gbase-lw"></span><span id="10GBASE-LW"></span>

<span data-ttu-id="6691d-182">**10GBASE-LW** (109)</span><span class="sxs-lookup"><span data-stu-id="6691d-182">**10GBase-LW** (109)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-ER"></span><span id="10gbase-er"></span><span id="10GBASE-ER"></span>

<span data-ttu-id="6691d-183">**10GBASE-ER** (110)</span><span class="sxs-lookup"><span data-stu-id="6691d-183">**10GBase-ER** (110)</span></span>


</dt> <dd></dd> <dt>

<span id="10GBase-EW"></span><span id="10gbase-ew"></span><span id="10GBASE-EW"></span>

<span data-ttu-id="6691d-184">**10GBASE-ovo** (111)</span><span class="sxs-lookup"><span data-stu-id="6691d-184">**10GBase-EW** (111)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="6691d-185">**Fornecedor reservado** (16000.. 65535)</span><span class="sxs-lookup"><span data-stu-id="6691d-185">**Vendor Reserved** (16000..65535)</span></span>


<span data-ttu-id="6691d-186"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="6691d-186"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="requirements"></a><span data-ttu-id="6691d-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6691d-187">Requirements</span></span>



| <span data-ttu-id="6691d-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="6691d-188">Requirement</span></span> | <span data-ttu-id="6691d-189">Valor</span><span class="sxs-lookup"><span data-stu-id="6691d-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6691d-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6691d-190">Minimum supported client</span></span><br/> | <span data-ttu-id="6691d-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="6691d-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="6691d-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6691d-192">Minimum supported server</span></span><br/> | <span data-ttu-id="6691d-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="6691d-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="6691d-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="6691d-194">Namespace</span></span><br/>                | <span data-ttu-id="6691d-195">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="6691d-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="6691d-196">MOF</span><span class="sxs-lookup"><span data-stu-id="6691d-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="6691d-197"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="6691d-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="6691d-198">DLL</span><span class="sxs-lookup"><span data-stu-id="6691d-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6691d-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="6691d-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="6691d-200">Confira também</span><span class="sxs-lookup"><span data-stu-id="6691d-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6691d-201">**\_NETWORKPORT CIM**</span><span class="sxs-lookup"><span data-stu-id="6691d-201">**CIM\_NetworkPort**</span></span>](cim-networkport.md)
</dt> </dl>

 

