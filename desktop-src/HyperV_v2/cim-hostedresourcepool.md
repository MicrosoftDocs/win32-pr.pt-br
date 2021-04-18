---
description: Representa uma associação entre um sistema e um pool de recursos que é um componente do sistema.
ms.assetid: 0ac60dbd-0498-4978-b2d6-f4c9926a83a8
title: Classe CIM_HostedResourcePool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_HostedResourcePool
- CIM_HostedResourcePool.GroupComponent
- CIM_HostedResourcePool.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: dbb6d523b533d6e8b2f5bc1e21de93962cfd860f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105766906"
---
# <a name="cim_hostedresourcepool-class"></a><span data-ttu-id="cb659-103">\_Classe CIM HostedResourcePool</span><span class="sxs-lookup"><span data-stu-id="cb659-103">CIM\_HostedResourcePool class</span></span>

<span data-ttu-id="cb659-104">Representa uma associação entre um sistema e um pool de recursos que é um componente do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb659-104">Represents an association between a system and a resource pool that is a component of the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="cb659-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cb659-105">Syntax</span></span>

``` syntax
[Association, Aggregation, Composition, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource")]
class CIM_HostedResourcePool : CIM_SystemComponent
{
  CIM_System       REF GroupComponent;
  CIM_ResourcePool REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="cb659-106">Membros</span><span class="sxs-lookup"><span data-stu-id="cb659-106">Members</span></span>

<span data-ttu-id="cb659-107">A classe **CIM \_ HostedResourcePool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cb659-107">The **CIM\_HostedResourcePool** class has these types of members:</span></span>

-   [<span data-ttu-id="cb659-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cb659-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cb659-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cb659-109">Properties</span></span>

<span data-ttu-id="cb659-110">A classe **CIM \_ HostedResourcePool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cb659-110">The **CIM\_HostedResourcePool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cb659-111">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="cb659-111">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb659-112">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="cb659-112">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="cb659-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb659-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb659-114">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="cb659-114">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent"), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="cb659-115">O sistema pai na associação.</span><span class="sxs-lookup"><span data-stu-id="cb659-115">The parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="cb659-116">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="cb659-116">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cb659-117">Tipo de dados: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="cb659-117">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="cb659-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cb659-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cb659-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="cb659-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="cb659-120">O pool de recursos que é um componente do sistema.</span><span class="sxs-lookup"><span data-stu-id="cb659-120">The resource pool that is a component of the system.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="cb659-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cb659-121">Requirements</span></span>



| <span data-ttu-id="cb659-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="cb659-122">Requirement</span></span> | <span data-ttu-id="cb659-123">Valor</span><span class="sxs-lookup"><span data-stu-id="cb659-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cb659-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb659-124">Minimum supported client</span></span><br/> | <span data-ttu-id="cb659-125">Windows 8.1</span><span class="sxs-lookup"><span data-stu-id="cb659-125">Windows 8.1</span></span><br/>                                                                                  |
| <span data-ttu-id="cb659-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cb659-126">Minimum supported server</span></span><br/> | <span data-ttu-id="cb659-127">Windows Server 2012 R2</span><span class="sxs-lookup"><span data-stu-id="cb659-127">Windows Server 2012 R2</span></span><br/>                                                                       |
| <span data-ttu-id="cb659-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb659-128">Namespace</span></span><br/>                | <span data-ttu-id="cb659-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="cb659-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="cb659-130">MOF</span><span class="sxs-lookup"><span data-stu-id="cb659-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cb659-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cb659-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="cb659-132">DLL</span><span class="sxs-lookup"><span data-stu-id="cb659-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cb659-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="cb659-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="cb659-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="cb659-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cb659-135">**\_SYSTEMCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="cb659-135">**CIM\_SystemComponent**</span></span>](cim-systemcomponent.md)
</dt> </dl>

 

