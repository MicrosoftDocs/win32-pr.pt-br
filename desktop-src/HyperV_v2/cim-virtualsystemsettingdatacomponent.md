---
description: Representa uma parte de uma relação entre uma \_ instância de VirtualSystemSettingData do CIM e um conjunto de instâncias de ResourceAllocationSettingData do CIM \_ .
ms.assetid: 4f167517-079e-4b5f-885a-741ac1d1dc71
title: Classe CIM_VirtualSystemSettingDataComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_VirtualSystemSettingDataComponent
- CIM_VirtualSystemSettingDataComponent.GroupComponent
- CIM_VirtualSystemSettingDataComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: afbd7ab192c65e99f4479e5380e57dc78c8a0a9c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104091796"
---
# <a name="cim_virtualsystemsettingdatacomponent-class"></a><span data-ttu-id="d1939-103">\_Classe CIM VirtualSystemSettingDataComponent</span><span class="sxs-lookup"><span data-stu-id="d1939-103">CIM\_VirtualSystemSettingDataComponent class</span></span>

<span data-ttu-id="d1939-104">Representa uma parte de uma relação entre uma instância de [**\_ VirtualSystemSettingData do CIM**](cim-virtualsystemsettingdata.md) e um conjunto de instâncias de [**\_ ResourceAllocationSettingData do CIM**](cim-resourceallocationsettingdata.md) .</span><span class="sxs-lookup"><span data-stu-id="d1939-104">Represents a portion of a relationship between a [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) instance and a set of [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) instances.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1939-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d1939-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Abstract, Version("2.22.0"), UMLPackagePath("CIM::System::SystemElements"), AMENDMENT]
class CIM_VirtualSystemSettingDataComponent : CIM_Component
{
  CIM_VirtualSystemSettingData      REF GroupComponent;
  CIM_ResourceAllocationSettingData REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="d1939-106">Membros</span><span class="sxs-lookup"><span data-stu-id="d1939-106">Members</span></span>

<span data-ttu-id="d1939-107">A classe **CIM \_ VirtualSystemSettingDataComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d1939-107">The **CIM\_VirtualSystemSettingDataComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="d1939-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1939-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d1939-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d1939-109">Properties</span></span>

<span data-ttu-id="d1939-110">A classe **CIM \_ VirtualSystemSettingDataComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d1939-110">The **CIM\_VirtualSystemSettingDataComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d1939-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="d1939-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1939-112">Tipo de dados: **CIM \_ VirtualSystemSettingData**</span><span class="sxs-lookup"><span data-stu-id="d1939-112">Data type: **CIM\_VirtualSystemSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="d1939-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1939-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1939-114">Qualificadores: [**agregação**](/windows/desktop/WmiSdk/standard-qualifiers), [**substituição**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="d1939-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d1939-115">Uma referência ao objeto [**CIM \_ VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) de nível superior da configuração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="d1939-115">A reference to the top-level [**CIM\_VirtualSystemSettingData**](cim-virtualsystemsettingdata.md) object of the virtual system configuration.</span></span>

</dd> <dt>

<span data-ttu-id="d1939-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="d1939-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d1939-117">Tipo de dados: **CIM \_ ResourceAllocationSettingData**</span><span class="sxs-lookup"><span data-stu-id="d1939-117">Data type: **CIM\_ResourceAllocationSettingData**</span></span>
</dt> <dt>

<span data-ttu-id="d1939-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d1939-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d1939-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="d1939-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="d1939-120">Uma referência ao objeto [**CIM \_ ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) que representa uma parte da configuração do sistema virtual.</span><span class="sxs-lookup"><span data-stu-id="d1939-120">A reference the [**CIM\_ResourceAllocationSettingData**](cim-resourceallocationsettingdata.md) object that represents a part of the virtual system configuration.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d1939-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1939-121">Requirements</span></span>



| <span data-ttu-id="d1939-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1939-122">Requirement</span></span> | <span data-ttu-id="d1939-123">Valor</span><span class="sxs-lookup"><span data-stu-id="d1939-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1939-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1939-124">Minimum supported client</span></span><br/> | <span data-ttu-id="d1939-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="d1939-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="d1939-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1939-126">Minimum supported server</span></span><br/> | <span data-ttu-id="d1939-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="d1939-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="d1939-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1939-128">Namespace</span></span><br/>                | <span data-ttu-id="d1939-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="d1939-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="d1939-130">MOF</span><span class="sxs-lookup"><span data-stu-id="d1939-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d1939-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d1939-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="d1939-132">DLL</span><span class="sxs-lookup"><span data-stu-id="d1939-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d1939-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="d1939-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="d1939-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1939-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1939-135">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="d1939-135">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

