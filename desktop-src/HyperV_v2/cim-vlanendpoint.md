---
description: Um ponto de extremidade em uma estação de comutador ou de extremidade que é atribuída a uma VLAN ou aceita o tráfego de uma ou mais VLANs.
ms.assetid: 20943be3-35c3-4bf5-8f1a-d4095fa6897e
title: Classe CIM_VLANEndpoint
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpoint
- CIM_VLANEndpoint.DesiredEndpointMode
- CIM_VLANEndpoint.OtherEndpointMode
- CIM_VLANEndpoint.OperationalEndpointMode
- CIM_VLANEndpoint.DesiredVLANTrunkEncapsulation
- CIM_VLANEndpoint.OtherTrunkEncapsulation
- CIM_VLANEndpoint.OperationalVLANTrunkEncapsulation
- CIM_VLANEndpoint.GVRPStatus
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 0f7b0d1318e4c24ab7381032877d16a8ea83868b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089858"
---
# <a name="cim_vlanendpoint-class"></a><span data-ttu-id="890ad-103">\_Classe CIM VLANEndpoint</span><span class="sxs-lookup"><span data-stu-id="890ad-103">CIM\_VLANEndpoint class</span></span>

<span data-ttu-id="890ad-104">Um ponto de extremidade em uma estação de comutador ou de extremidade que é atribuída a uma VLAN ou aceita o tráfego de uma ou mais VLANs.</span><span class="sxs-lookup"><span data-stu-id="890ad-104">An endpoint on a switch or end station that is assigned to a VLAN, or accepts traffic from one or more VLANs.</span></span>

## <a name="syntax"></a><span data-ttu-id="890ad-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="890ad-105">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Network::VLAN"), AMENDMENT]
class CIM_VLANEndpoint : CIM_ProtocolEndpoint
{
  uint16 DesiredEndpointMode;
  string OtherEndpointMode;
  uint16 OperationalEndpointMode;
  uint16 DesiredVLANTrunkEncapsulation;
  string OtherTrunkEncapsulation;
  uint16 OperationalVLANTrunkEncapsulation;
  uint16 GVRPStatus;
};
```

## <a name="members"></a><span data-ttu-id="890ad-106">Membros</span><span class="sxs-lookup"><span data-stu-id="890ad-106">Members</span></span>

<span data-ttu-id="890ad-107">A classe **CIM \_ VLANEndpoint** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="890ad-107">The **CIM\_VLANEndpoint** class has these types of members:</span></span>

-   [<span data-ttu-id="890ad-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="890ad-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="890ad-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="890ad-109">Properties</span></span>

<span data-ttu-id="890ad-110">A classe **CIM \_ VLANEndpoint** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="890ad-110">The **CIM\_VLANEndpoint** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="890ad-111">**DesiredEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="890ad-111">**DesiredEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="890ad-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="890ad-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="890ad-113">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="890ad-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="890ad-114">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**","**CIM \_ VLANEndpoint**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="890ad-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="890ad-115">O modo de VLAN solicitado para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="890ad-115">The requested VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="890ad-116">**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="890ad-116">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="890ad-117">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="890ad-117">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="890ad-118">**Acesso** (2)</span><span class="sxs-lookup"><span data-stu-id="890ad-118">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="890ad-119">**Automático dinâmico** (3)</span><span class="sxs-lookup"><span data-stu-id="890ad-119">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="890ad-120">**Dinâmico desejável** (4)</span><span class="sxs-lookup"><span data-stu-id="890ad-120">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="890ad-121">**Tronco** (5)</span><span class="sxs-lookup"><span data-stu-id="890ad-121">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="890ad-122">**Túnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="890ad-122">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="890ad-123">**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="890ad-123">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="890ad-124">**Fornecedor reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="890ad-124">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="890ad-125">**DesiredVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="890ad-125">**DesiredVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="890ad-126">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="890ad-126">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="890ad-127">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="890ad-127">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="890ad-128">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM \_ VLANEndpointCapabilities. SupportsTrunkEncapsulationNegotiation", "**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="890ad-128">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("CIM\_VLANEndpointCapabilities.SupportsTrunkEncapsulationNegotiation", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="890ad-129">O tipo de encapsulamento de VLAN solicitado.</span><span class="sxs-lookup"><span data-stu-id="890ad-129">The requested VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="890ad-130">Essa propriedade só é usada quando o ponto de extremidade de VLAN está no modo de entroncamento.</span><span class="sxs-lookup"><span data-stu-id="890ad-130">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="890ad-131">**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="890ad-131">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="890ad-132">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="890ad-132">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="890ad-133">**Não aplicável** (2)</span><span class="sxs-lookup"><span data-stu-id="890ad-133">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="890ad-134">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="890ad-134">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="890ad-135">**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="890ad-135">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiate"></span><span id="negotiate"></span><span id="NEGOTIATE"></span>

<span data-ttu-id="890ad-136">**Negociar** (5)</span><span class="sxs-lookup"><span data-stu-id="890ad-136">**Negotiate** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="890ad-137">**DMTF reservado** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="890ad-137">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="890ad-138">**Fornecedor reservado** (32768..)</span><span class="sxs-lookup"><span data-stu-id="890ad-138">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="890ad-139">**GVRPStatus**</span><span class="sxs-lookup"><span data-stu-id="890ad-139">**GVRPStatus**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="890ad-140">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="890ad-140">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="890ad-141">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="890ad-141">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="890ad-142">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OperationalEndpointMode**, CIM \_ VLANEndpointCapabilities. Dot1QTagging ")</span><span class="sxs-lookup"><span data-stu-id="890ad-142">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OperationalEndpointMode**, CIM\_VLANEndpointCapabilities.Dot1QTagging")</span></span>
</dt> </dl>

<span data-ttu-id="890ad-143">Indica se o GVRP (protocolo de registro de VLAN GARP) está habilitado ou desabilitado no ponto de extremidade do tronco.</span><span class="sxs-lookup"><span data-stu-id="890ad-143">Indicates whether GARP VLAN Registration Protocol (GVRP) is enabled or disabled on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="890ad-144">Essa propriedade só é usada quando o ponto de extremidade oferece suporte a GVRP e o modo de entroncamento está habilitado.</span><span class="sxs-lookup"><span data-stu-id="890ad-144">This property is only used when GVRP is supported by the endpoint, and trunking mode is enabled.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="890ad-145">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="890ad-145">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="890ad-146">**Não aplicável** (2)</span><span class="sxs-lookup"><span data-stu-id="890ad-146">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Enabled"></span><span id="enabled"></span><span id="ENABLED"></span>

<span data-ttu-id="890ad-147">**Habilitado** (3)</span><span class="sxs-lookup"><span data-stu-id="890ad-147">**Enabled** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Disabled"></span><span id="disabled"></span><span id="DISABLED"></span>

<span data-ttu-id="890ad-148">**Desabilitado** (4)</span><span class="sxs-lookup"><span data-stu-id="890ad-148">**Disabled** (4)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="890ad-149">**OperationalEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="890ad-149">**OperationalEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="890ad-150">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="890ad-150">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="890ad-151">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="890ad-151">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="890ad-152">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ VLANEndpoint**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="890ad-152">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="890ad-153">O modo de VLAN atual para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="890ad-153">The current VLAN mode for the endpoint.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="890ad-154">**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="890ad-154">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="890ad-155">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="890ad-155">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="890ad-156">**Acesso** (2)</span><span class="sxs-lookup"><span data-stu-id="890ad-156">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="890ad-157">**Automático dinâmico** (3)</span><span class="sxs-lookup"><span data-stu-id="890ad-157">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="890ad-158">**Dinâmico desejável** (4)</span><span class="sxs-lookup"><span data-stu-id="890ad-158">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="890ad-159">**Tronco** (5)</span><span class="sxs-lookup"><span data-stu-id="890ad-159">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="890ad-160">**Túnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="890ad-160">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="890ad-161">**DMTF reservado** (7.. 32767)</span><span class="sxs-lookup"><span data-stu-id="890ad-161">**DMTF Reserved** (7..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="890ad-162">**Fornecedor reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="890ad-162">**Vendor Reserved** (..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="890ad-163">**OperationalVLANTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="890ad-163">**OperationalVLANTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="890ad-164">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="890ad-164">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="890ad-165">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="890ad-165">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="890ad-166">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**OtherTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="890ad-166">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**OtherTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="890ad-167">O tipo de encapsulamento de VLAN atual.</span><span class="sxs-lookup"><span data-stu-id="890ad-167">The current VLAN encapsulation type.</span></span>

> [!Note]  
> <span data-ttu-id="890ad-168">Essa propriedade só é usada quando o ponto de extremidade de VLAN está no modo de entroncamento.</span><span class="sxs-lookup"><span data-stu-id="890ad-168">This property is only used when the VLAN endpoint is in trunking mode.</span></span>

 

<dt>

<span id="Unknown"></span><span id="unknown"></span><span id="UNKNOWN"></span>

<span data-ttu-id="890ad-169">**Desconhecido** (0)</span><span class="sxs-lookup"><span data-stu-id="890ad-169">**Unknown** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="890ad-170">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="890ad-170">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Not_Applicable"></span><span id="not_applicable"></span><span id="NOT_APPLICABLE"></span>

<span data-ttu-id="890ad-171">**Não aplicável** (2)</span><span class="sxs-lookup"><span data-stu-id="890ad-171">**Not Applicable** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="802.1q"></span><span id="802.1Q"></span>

<span data-ttu-id="890ad-172">**802.1 q** (3)</span><span class="sxs-lookup"><span data-stu-id="890ad-172">**802.1q** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Cisco_ISL"></span><span id="cisco_isl"></span><span id="CISCO_ISL"></span>

<span data-ttu-id="890ad-173">**Cisco ISL** (4)</span><span class="sxs-lookup"><span data-stu-id="890ad-173">**Cisco ISL** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Negotiating"></span><span id="negotiating"></span><span id="NEGOTIATING"></span>

<span data-ttu-id="890ad-174">**Negociando** (5)</span><span class="sxs-lookup"><span data-stu-id="890ad-174">**Negotiating** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="890ad-175">**DMTF reservado** (6.. 32767)</span><span class="sxs-lookup"><span data-stu-id="890ad-175">**DMTF Reserved** (6..32767)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="890ad-176">**Fornecedor reservado** (32768..)</span><span class="sxs-lookup"><span data-stu-id="890ad-176">**Vendor Reserved** (32768..)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="890ad-177">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="890ad-177">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="890ad-178">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="890ad-178">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="890ad-179">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="890ad-179">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="890ad-180">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ VLANEndpoint**.**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="890ad-180">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_VLANEndpoint**.**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="890ad-181">O tipo de modelo de ponto de extremidade de VLAN com suporte do VLANEndpoint quando o valor de **DesiredEndpointMode** é definido como "1" (outro); caso contrário, **NULL**.</span><span class="sxs-lookup"><span data-stu-id="890ad-181">The type of VLAN endpoint model that is supported by the VLANEndpoint when the value of **DesiredEndpointMode** is set to "1" (other); otherwise, **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="890ad-182">**OtherTrunkEncapsulation**</span><span class="sxs-lookup"><span data-stu-id="890ad-182">**OtherTrunkEncapsulation**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="890ad-183">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="890ad-183">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="890ad-184">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="890ad-184">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="890ad-185">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ VLANEndpoint**.**DesiredVLANTrunkEncapsulation**","**CIM \_ VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span><span class="sxs-lookup"><span data-stu-id="890ad-185">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_VLANEndpoint**.**DesiredVLANTrunkEncapsulation**", "**CIM\_VLANEndpoint**.**OperationalVLANTrunkEncapsulation**")</span></span>
</dt> </dl>

<span data-ttu-id="890ad-186">O tipo de encapsulamento de VLAN que é suportado pelo ponto de extremidade de VLAN quando o valor da propriedade **DesiredVLANTrunkEncapsulation** é definido como 1 (outro); caso contrário, **NULL**.</span><span class="sxs-lookup"><span data-stu-id="890ad-186">The type of VLAN encapsulation that is supported by the VLAN endpoint when the value of the **DesiredVLANTrunkEncapsulation** property is set to 1 (other); otherwise, **NULL**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="890ad-187">Requisitos</span><span class="sxs-lookup"><span data-stu-id="890ad-187">Requirements</span></span>



| <span data-ttu-id="890ad-188">Requisito</span><span class="sxs-lookup"><span data-stu-id="890ad-188">Requirement</span></span> | <span data-ttu-id="890ad-189">Valor</span><span class="sxs-lookup"><span data-stu-id="890ad-189">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="890ad-190">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="890ad-190">Minimum supported client</span></span><br/> | <span data-ttu-id="890ad-191">Windows 8</span><span class="sxs-lookup"><span data-stu-id="890ad-191">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="890ad-192">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="890ad-192">Minimum supported server</span></span><br/> | <span data-ttu-id="890ad-193">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="890ad-193">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="890ad-194">Namespace</span><span class="sxs-lookup"><span data-stu-id="890ad-194">Namespace</span></span><br/>                | <span data-ttu-id="890ad-195">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="890ad-195">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="890ad-196">MOF</span><span class="sxs-lookup"><span data-stu-id="890ad-196">MOF</span></span><br/>                      | <dl> <span data-ttu-id="890ad-197"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="890ad-197"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="890ad-198">DLL</span><span class="sxs-lookup"><span data-stu-id="890ad-198">DLL</span></span><br/>                      | <dl> <span data-ttu-id="890ad-199"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="890ad-199"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="890ad-200">Confira também</span><span class="sxs-lookup"><span data-stu-id="890ad-200">See also</span></span>

<dl> <dt>

[<span data-ttu-id="890ad-201">**CIM \_ ProtocolEndpoint**</span><span class="sxs-lookup"><span data-stu-id="890ad-201">**CIM\_ProtocolEndpoint**</span></span>](cim-protocolendpoint.md)
</dt> </dl>

 

