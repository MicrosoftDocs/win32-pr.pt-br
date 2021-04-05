---
description: Representa uma associação na qual um \_ objeto LogicalElement do CIM representa um recurso alocado de um \_ objeto CIM ResourcePool.
ms.assetid: 5e3c95c5-1cbb-40de-b285-0bf9b34a5ca8
title: Classe CIM_ElementAllocatedFromPool
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementAllocatedFromPool
- CIM_ElementAllocatedFromPool.Antecedent
- CIM_ElementAllocatedFromPool.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 5fc6d58f5ebf82013f38b39027e0cd02e0e3595a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827388"
---
# <a name="cim_elementallocatedfrompool-class"></a><span data-ttu-id="0f66f-103">\_Classe CIM ElementAllocatedFromPool</span><span class="sxs-lookup"><span data-stu-id="0f66f-103">CIM\_ElementAllocatedFromPool class</span></span>

<span data-ttu-id="0f66f-104">Representa uma associação na qual um [**objeto \_ LogicalElement do CIM**](cim-logicalelement.md) representa um recurso alocado de um objeto [**CIM \_ ResourcePool**](cim-resourcepool.md) .</span><span class="sxs-lookup"><span data-stu-id="0f66f-104">Represents an association in which a [**CIM\_LogicalElement**](cim-logicalelement.md) object represents a resource allocated from a [**CIM\_ResourcePool**](cim-resourcepool.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f66f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0f66f-105">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.22.0"), UMLPackagePath("CIM::Core::Resource"), AMENDMENT]
class CIM_ElementAllocatedFromPool : CIM_Dependency
{
  CIM_ResourcePool   REF Antecedent;
  CIM_LogicalElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="0f66f-106">Membros</span><span class="sxs-lookup"><span data-stu-id="0f66f-106">Members</span></span>

<span data-ttu-id="0f66f-107">A classe **CIM \_ ElementAllocatedFromPool** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0f66f-107">The **CIM\_ElementAllocatedFromPool** class has these types of members:</span></span>

-   [<span data-ttu-id="0f66f-108">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0f66f-108">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="0f66f-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="0f66f-109">Properties</span></span>

<span data-ttu-id="0f66f-110">A classe **CIM \_ ElementAllocatedFromPool** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="0f66f-110">The **CIM\_ElementAllocatedFromPool** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="0f66f-111">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="0f66f-111">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f66f-112">Tipo de dados: **CIM \_ ResourcePool**</span><span class="sxs-lookup"><span data-stu-id="0f66f-112">Data type: **CIM\_ResourcePool**</span></span>
</dt> <dt>

<span data-ttu-id="0f66f-113">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f66f-113">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f66f-114">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="0f66f-114">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="0f66f-115">O pool de recursos.</span><span class="sxs-lookup"><span data-stu-id="0f66f-115">The resource pool.</span></span>

</dd> <dt>

<span data-ttu-id="0f66f-116">**Depende**</span><span class="sxs-lookup"><span data-stu-id="0f66f-116">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="0f66f-117">Tipo de dados: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="0f66f-117">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="0f66f-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="0f66f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="0f66f-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="0f66f-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="0f66f-120">O recurso alocado.</span><span class="sxs-lookup"><span data-stu-id="0f66f-120">The allocated resource.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0f66f-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f66f-121">Requirements</span></span>



| <span data-ttu-id="0f66f-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f66f-122">Requirement</span></span> | <span data-ttu-id="0f66f-123">Valor</span><span class="sxs-lookup"><span data-stu-id="0f66f-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f66f-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f66f-124">Minimum supported client</span></span><br/> | <span data-ttu-id="0f66f-125">Windows 8</span><span class="sxs-lookup"><span data-stu-id="0f66f-125">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="0f66f-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f66f-126">Minimum supported server</span></span><br/> | <span data-ttu-id="0f66f-127">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="0f66f-127">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="0f66f-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="0f66f-128">Namespace</span></span><br/>                | <span data-ttu-id="0f66f-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="0f66f-129">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="0f66f-130">MOF</span><span class="sxs-lookup"><span data-stu-id="0f66f-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="0f66f-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="0f66f-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="0f66f-132">DLL</span><span class="sxs-lookup"><span data-stu-id="0f66f-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f66f-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="0f66f-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="0f66f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f66f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f66f-135">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="0f66f-135">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

