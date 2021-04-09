---
description: Representa dados de configuração para um ponto de extremidade de VLAN.
ms.assetid: 5ef3cc55-cf27-40b4-9e94-2e2b42ca41c5
title: Classe CIM_VLANEndpointSettingData
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VLANEndpointSettingData
- CIM_VLANEndpointSettingData.PruneEligibleVLANList
- CIM_VLANEndpointSettingData.NativeVLAN
- CIM_VLANEndpointSettingData.DefaultVLAN
- CIM_VLANEndpointSettingData.TrunkedVLANList
- CIM_VLANEndpointSettingData.AccessVLAN
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: a510c4195c538ab9735e7544acec2c88beeaa1de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103837520"
---
# <a name="cim_vlanendpointsettingdata-class"></a><span data-ttu-id="fb930-103">\_Classe CIM VLANEndpointSettingData</span><span class="sxs-lookup"><span data-stu-id="fb930-103">CIM\_VLANEndpointSettingData class</span></span>

<span data-ttu-id="fb930-104">Representa dados de configuração para um ponto de extremidade de VLAN.</span><span class="sxs-lookup"><span data-stu-id="fb930-104">Represents configuration data for a VLAN endpoint.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb930-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fb930-105">Syntax</span></span>

``` syntax
[Experimental, Abstract, Version("2.11.0"), UMLPackagePath("CIM::Network::VLAN")]
class CIM_VLANEndpointSettingData : CIM_SettingData
{
  uint16 PruneEligibleVLANList[];
  uint16 NativeVLAN;
  uint16 DefaultVLAN;
  uint16 TrunkedVLANList[];
  uint16 AccessVLAN;
};
```

## <a name="members"></a><span data-ttu-id="fb930-106">Membros</span><span class="sxs-lookup"><span data-stu-id="fb930-106">Members</span></span>

<span data-ttu-id="fb930-107">A classe **CIM \_ VLANEndpointSettingData** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="fb930-107">The **CIM\_VLANEndpointSettingData** class has these types of members:</span></span>

-   [<span data-ttu-id="fb930-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fb930-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="fb930-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="fb930-109">Properties</span></span>

<span data-ttu-id="fb930-110">A classe **CIM \_ VLANEndpointSettingData** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="fb930-110">The **CIM\_VLANEndpointSettingData** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="fb930-111">**AccessVLAN**</span><span class="sxs-lookup"><span data-stu-id="fb930-111">**AccessVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb930-112">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb930-112">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb930-113">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fb930-113">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fb930-114">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="fb930-114">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="fb930-115">A VLAN de acesso para o ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="fb930-115">The access VLAN for the endpoint.</span></span>

</dd> <dt>

<span data-ttu-id="fb930-116">**Defaultvlan**</span><span class="sxs-lookup"><span data-stu-id="fb930-116">**DefaultVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb930-117">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb930-117">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb930-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="fb930-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="fb930-119">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="fb930-119">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="fb930-120">O valor padrão para a VLAN nativa no ponto de extremidade do tronco.</span><span class="sxs-lookup"><span data-stu-id="fb930-120">The default value for the native VLAN on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="fb930-121">Essa propriedade só é usada quando o ponto de extremidade de VLAN está operando no modo de entroncamento, que é especificado na propriedade **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="fb930-121">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="fb930-122">**NativeVLAN**</span><span class="sxs-lookup"><span data-stu-id="fb930-122">**NativeVLAN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb930-123">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb930-123">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="fb930-124">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fb930-124">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fb930-125">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="fb930-125">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="fb930-126">A ID de VLAN usada para marcar o tráfego não marcado recebido no ponto de extremidade do tronco.</span><span class="sxs-lookup"><span data-stu-id="fb930-126">The VLAN ID that is used to tag untagged traffic received on the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="fb930-127">Essa propriedade só é usada quando o ponto de extremidade de VLAN está operando no modo de entroncamento, que é especificado na propriedade **SwitchEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="fb930-127">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **SwitchEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="fb930-128">**PruneEligibleVLANList**</span><span class="sxs-lookup"><span data-stu-id="fb930-128">**PruneEligibleVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb930-129">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb930-129">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fb930-130">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fb930-130">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fb930-131">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="fb930-131">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="fb930-132">Uma matriz que contém IDs de VLANs que o sistema pode remover do ponto de extremidade do tronco.</span><span class="sxs-lookup"><span data-stu-id="fb930-132">An array that contains IDs of VLANs that the system may remove from the trunk endpoint.</span></span>

> [!Note]  
> <span data-ttu-id="fb930-133">Essa propriedade só é usada quando o ponto de extremidade de VLAN está operando no modo de entroncamento, que é especificado na propriedade **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="fb930-133">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> <dt>

<span data-ttu-id="fb930-134">**TrunkedVLANList**</span><span class="sxs-lookup"><span data-stu-id="fb930-134">**TrunkedVLANList**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="fb930-135">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="fb930-135">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="fb930-136">Tipo de acesso: leitura/gravação</span><span class="sxs-lookup"><span data-stu-id="fb930-136">Access type: Read/write</span></span>
</dt> <dt>

<span data-ttu-id="fb930-137">Qualificadores: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM \_ VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span><span class="sxs-lookup"><span data-stu-id="fb930-137">Qualifiers: [**ModelCorrespondence**](/windows/desktop/WmiSdk/standard-qualifiers) ("[**CIM\_VLANEndpoint**](cim-vlanendpoint.md).**OperationalEndpointMode**")</span></span>
</dt> </dl>

<span data-ttu-id="fb930-138">Uma matriz que contém IDs de pontos de extremidade de VLAN com entroncamento habilitado.</span><span class="sxs-lookup"><span data-stu-id="fb930-138">An array that contains IDs of VLAN endpoints with trunking enabled.</span></span>

> [!Note]  
> <span data-ttu-id="fb930-139">Essa propriedade só é usada quando o ponto de extremidade de VLAN está operando no modo de entroncamento, que é especificado na propriedade **OperationalEndpointMode** .</span><span class="sxs-lookup"><span data-stu-id="fb930-139">This property is only used when the VLAN endpoint is operating in trunking mode, which is specified in the **OperationalEndpointMode** property.</span></span>

 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="fb930-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fb930-140">Requirements</span></span>



| <span data-ttu-id="fb930-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="fb930-141">Requirement</span></span> | <span data-ttu-id="fb930-142">Valor</span><span class="sxs-lookup"><span data-stu-id="fb930-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb930-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb930-143">Minimum supported client</span></span><br/> | <span data-ttu-id="fb930-144">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="fb930-144">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="fb930-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="fb930-145">Minimum supported server</span></span><br/> | <span data-ttu-id="fb930-146">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="fb930-146">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="fb930-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="fb930-147">Namespace</span></span><br/>                | <span data-ttu-id="fb930-148">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="fb930-148">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="fb930-149">MOF</span><span class="sxs-lookup"><span data-stu-id="fb930-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="fb930-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="fb930-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="fb930-151">DLL</span><span class="sxs-lookup"><span data-stu-id="fb930-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="fb930-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="fb930-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="fb930-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="fb930-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb930-154">**CIM \_ SettingData**</span><span class="sxs-lookup"><span data-stu-id="fb930-154">**CIM\_SettingData**</span></span>](cim-settingdata.md)
</dt> </dl>

 

