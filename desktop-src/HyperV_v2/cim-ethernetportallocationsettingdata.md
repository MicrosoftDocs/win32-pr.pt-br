---
description: Representa as configurações para a alocação da porta Ethernet, além das configurações fornecidas pela \_ classe CIM EthernetPort. Essas configurações são usadas para fornecer informações específicas ao próprio recurso.
ms.assetid: f59ebaf1-60dd-49bd-b48e-d7a6c2650909
title: Classe CIM_EthernetPortAllocationSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_EthernetPortAllocationSettingData
- CIM_EthernetPortAllocationSettingData.DesiredVLANEndpointMode
- CIM_EthernetPortAllocationSettingData.OtherEndpointMode
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 7e77b4387f77e88ceaff273b8be72a354c989e7e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105770227"
---
# <a name="cim_ethernetportallocationsettingdata-class"></a><span data-ttu-id="642f0-104">\_Classe CIM EthernetPortAllocationSettingData</span><span class="sxs-lookup"><span data-stu-id="642f0-104">CIM\_EthernetPortAllocationSettingData class</span></span>

<span data-ttu-id="642f0-105">Representa as configurações para a alocação da porta Ethernet, além das configurações fornecidas pela classe [**CIM \_ EthernetPort**](cim-ethernetport.md) .</span><span class="sxs-lookup"><span data-stu-id="642f0-105">Represents settings for the allocation of the ethernet port, in addition to the settings provided by the [**CIM\_EthernetPort**](cim-ethernetport.md) class.</span></span> <span data-ttu-id="642f0-106">Essas configurações são usadas para fornecer informações específicas ao próprio recurso.</span><span class="sxs-lookup"><span data-stu-id="642f0-106">These settings are used to provide information specific to the resource itself.</span></span>

## <a name="syntax"></a><span data-ttu-id="642f0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="642f0-107">Syntax</span></span>

``` syntax
[Abstract, Version("2.26.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_EthernetPortAllocationSettingData : CIM_ResourceAllocationSettingData
{
  uint16 DesiredVLANEndpointMode;
  string OtherEndpointMode;
};
```

## <a name="members"></a><span data-ttu-id="642f0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="642f0-108">Members</span></span>

<span data-ttu-id="642f0-109">A classe **CIM \_ EthernetPortAllocationSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="642f0-109">The **CIM\_EthernetPortAllocationSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="642f0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="642f0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="642f0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="642f0-111">Properties</span></span>

<span data-ttu-id="642f0-112">A classe **CIM \_ EthernetPortAllocationSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="642f0-112">The **CIM\_EthernetPortAllocationSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="642f0-113">**DesiredVLANEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="642f0-113">**DesiredVLANEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="642f0-114">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="642f0-114">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="642f0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="642f0-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="642f0-116">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**","**CIM \_ VLANEndpoint**.**DesiredEndpointMode**","**CIM \_ EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="642f0-116">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**", "**CIM\_VLANEndpoint**.**DesiredEndpointMode**", "**CIM\_EthernetPortAllocationSettingData**.**OtherEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="642f0-117">O modo de VLAN solicitado.</span><span class="sxs-lookup"><span data-stu-id="642f0-117">The requested VLAN mode.</span></span> <span data-ttu-id="642f0-118">Essa propriedade é usada para definir o valor da propriedade **OperationalEndpointMode** inicial na instância do **CIM \_ VLANEndpoint** associada à porta Ethernet.</span><span class="sxs-lookup"><span data-stu-id="642f0-118">This property is used to set the initial **OperationalEndpointMode** property value in the instance of **CIM\_VLANEndpoint** associated with the ethernet port.</span></span>

<dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="642f0-119">**DMTF reservado** (0)</span><span class="sxs-lookup"><span data-stu-id="642f0-119">**DMTF Reserved** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Other"></span><span id="other"></span><span id="OTHER"></span>

<span data-ttu-id="642f0-120">**Outro** (1)</span><span class="sxs-lookup"><span data-stu-id="642f0-120">**Other** (1)</span></span>


</dt> <dd></dd> <dt>

<span id="Access"></span><span id="access"></span><span id="ACCESS"></span>

<span data-ttu-id="642f0-121">**Acesso** (2)</span><span class="sxs-lookup"><span data-stu-id="642f0-121">**Access** (2)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Auto"></span><span id="dynamic_auto"></span><span id="DYNAMIC_AUTO"></span>

<span data-ttu-id="642f0-122">**Automático dinâmico** (3)</span><span class="sxs-lookup"><span data-stu-id="642f0-122">**Dynamic Auto** (3)</span></span>


</dt> <dd></dd> <dt>

<span id="Dynamic_Desirable"></span><span id="dynamic_desirable"></span><span id="DYNAMIC_DESIRABLE"></span>

<span data-ttu-id="642f0-123">**Dinâmico desejável** (4)</span><span class="sxs-lookup"><span data-stu-id="642f0-123">**Dynamic Desirable** (4)</span></span>


</dt> <dd></dd> <dt>

<span id="Trunk"></span><span id="trunk"></span><span id="TRUNK"></span>

<span data-ttu-id="642f0-124">**Tronco** (5)</span><span class="sxs-lookup"><span data-stu-id="642f0-124">**Trunk** (5)</span></span>


</dt> <dd></dd> <dt>

<span id="Dot1Q_Tunnel"></span><span id="dot1q_tunnel"></span><span id="DOT1Q_TUNNEL"></span>

<span data-ttu-id="642f0-125">**Túnel Dot1Q** (6)</span><span class="sxs-lookup"><span data-stu-id="642f0-125">**Dot1Q Tunnel** (6)</span></span>


</dt> <dd></dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span data-ttu-id="642f0-126">**DMTF reservado** (..)</span><span class="sxs-lookup"><span data-stu-id="642f0-126">**DMTF Reserved** (..)</span></span>


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span data-ttu-id="642f0-127">**Fornecedor reservado** (0x8000.. 0xFFFF</span><span class="sxs-lookup"><span data-stu-id="642f0-127">**Vendor Reserved** (0x8000..0xFFFF)</span></span>


</dt> <dd></dd> </dl>

</dd> <dt>

<span data-ttu-id="642f0-128">**OtherEndpointMode**</span><span class="sxs-lookup"><span data-stu-id="642f0-128">**OtherEndpointMode**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="642f0-129">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="642f0-129">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="642f0-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="642f0-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="642f0-131">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM \_ EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="642f0-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("**CIM\_EthernetPortAllocationSettingData**.**DesiredVLANEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="642f0-132">O tipo de modelo de ponto de extremidade de VLAN com suporte por esse ponto de extremidade de VLAN, quando o valor da propriedade de modo é definido como "1" (outro).</span><span class="sxs-lookup"><span data-stu-id="642f0-132">The type of VLAN endpoint model that is supported by this VLAN endpoint, when the value of the mode property is set to "1" (Other).</span></span> <span data-ttu-id="642f0-133">Essa propriedade deve ser definida como **NULL** quando a propriedade Mode for qualquer valor diferente de "1".</span><span class="sxs-lookup"><span data-stu-id="642f0-133">This property should be set to **NULL** when the mode property is any value other than "1".</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="642f0-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="642f0-134">Requirements</span></span>



| <span data-ttu-id="642f0-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="642f0-135">Requirement</span></span> | <span data-ttu-id="642f0-136">Valor</span><span class="sxs-lookup"><span data-stu-id="642f0-136">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="642f0-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="642f0-137">Minimum supported client</span></span><br/> | <span data-ttu-id="642f0-138">Windows 8</span><span class="sxs-lookup"><span data-stu-id="642f0-138">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="642f0-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="642f0-139">Minimum supported server</span></span><br/> | <span data-ttu-id="642f0-140">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="642f0-140">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="642f0-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="642f0-141">Namespace</span></span><br/>                | <span data-ttu-id="642f0-142">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="642f0-142">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="642f0-143">MOF</span><span class="sxs-lookup"><span data-stu-id="642f0-143">MOF</span></span><br/>                      | <dl> <span data-ttu-id="642f0-144"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="642f0-144"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="642f0-145">DLL</span><span class="sxs-lookup"><span data-stu-id="642f0-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="642f0-146"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="642f0-146"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="642f0-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="642f0-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="642f0-148">**\_RESOURCEALLOCATIONSETTINGDATA CIM**</span><span class="sxs-lookup"><span data-stu-id="642f0-148">**CIM\_ResourceAllocationSettingData**</span></span>](cim-resourceallocationsettingdata.md)
</dt> </dl>

 

