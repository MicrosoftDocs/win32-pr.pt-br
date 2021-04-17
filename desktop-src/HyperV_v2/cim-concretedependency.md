---
description: Representa uma associação genérica na qual um elemento gerenciado depende de outro. CIM \_ ConcreteDependency subclasses \_ de dependência CIM para fornecer uma versão de classe concreta da \_ dependência CIM.
ms.assetid: c0e1527d-d350-410d-9b5f-c9d4dedf7393
title: Classe CIM_ConcreteDependency
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ConcreteDependency
- CIM_ConcreteDependency.Antecedent
- CIM_ConcreteDependency.Dependent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 253f57b1fd29c3844f0e87d488974ced7bec98bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105789811"
---
# <a name="cim_concretedependency-class"></a><span data-ttu-id="f90ce-104">\_Classe CIM ConcreteDependency</span><span class="sxs-lookup"><span data-stu-id="f90ce-104">CIM\_ConcreteDependency class</span></span>

<span data-ttu-id="f90ce-105">Representa uma associação genérica na qual um elemento gerenciado depende de outro.</span><span class="sxs-lookup"><span data-stu-id="f90ce-105">Represents a generic association in which a managed element depends on another.</span></span> <span data-ttu-id="f90ce-106">**CIM \_ ConcreteDependency** subclasses de [**\_ dependência CIM**](cim-dependency.md) para fornecer uma versão de classe concreta **da \_ dependência CIM**.</span><span class="sxs-lookup"><span data-stu-id="f90ce-106">**CIM\_ConcreteDependency** subclasses [**CIM\_Dependency**](cim-dependency.md) to provide a concrete class version of **CIM\_Dependency**.</span></span>

## <a name="syntax"></a><span data-ttu-id="f90ce-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f90ce-107">Syntax</span></span>

``` syntax
[Association, Abstract, Version("2.10.0"), UMLPackagePath("CIM::Core::CoreElements"), AMENDMENT]
class CIM_ConcreteDependency : CIM_Dependency
{
  CIM_ManagedElement REF Antecedent;
  CIM_ManagedElement REF Dependent;
};
```

## <a name="members"></a><span data-ttu-id="f90ce-108">Membros</span><span class="sxs-lookup"><span data-stu-id="f90ce-108">Members</span></span>

<span data-ttu-id="f90ce-109">A classe **CIM \_ ConcreteDependency** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f90ce-109">The **CIM\_ConcreteDependency** class has these types of members:</span></span>

-   [<span data-ttu-id="f90ce-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f90ce-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f90ce-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f90ce-111">Properties</span></span>

<span data-ttu-id="f90ce-112">A classe **CIM \_ ConcreteDependency** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f90ce-112">The **CIM\_ConcreteDependency** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f90ce-113">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="f90ce-113">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f90ce-114">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="f90ce-114">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f90ce-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f90ce-115">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f90ce-116">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="f90ce-116">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="f90ce-117">O objeto independente na associação.</span><span class="sxs-lookup"><span data-stu-id="f90ce-117">The independent object in the association.</span></span>

</dd> <dt>

<span data-ttu-id="f90ce-118">**Depende**</span><span class="sxs-lookup"><span data-stu-id="f90ce-118">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f90ce-119">Tipo de dados: **CIM \_ managedelement**</span><span class="sxs-lookup"><span data-stu-id="f90ce-119">Data type: **CIM\_ManagedElement**</span></span>
</dt> <dt>

<span data-ttu-id="f90ce-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f90ce-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f90ce-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="f90ce-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="f90ce-122">O objeto dependente na associação.</span><span class="sxs-lookup"><span data-stu-id="f90ce-122">The dependent object in the association.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f90ce-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f90ce-123">Requirements</span></span>



| <span data-ttu-id="f90ce-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="f90ce-124">Requirement</span></span> | <span data-ttu-id="f90ce-125">Valor</span><span class="sxs-lookup"><span data-stu-id="f90ce-125">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f90ce-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f90ce-126">Minimum supported client</span></span><br/> | <span data-ttu-id="f90ce-127">Windows 8</span><span class="sxs-lookup"><span data-stu-id="f90ce-127">Windows 8</span></span><br/>                                                                                    |
| <span data-ttu-id="f90ce-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f90ce-128">Minimum supported server</span></span><br/> | <span data-ttu-id="f90ce-129">Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="f90ce-129">Windows Server 2012</span></span><br/>                                                                          |
| <span data-ttu-id="f90ce-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="f90ce-130">Namespace</span></span><br/>                | <span data-ttu-id="f90ce-131">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f90ce-131">Root\\virtualization\\v2</span></span><br/>                                                                     |
| <span data-ttu-id="f90ce-132">MOF</span><span class="sxs-lookup"><span data-stu-id="f90ce-132">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f90ce-133"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f90ce-133"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f90ce-134">DLL</span><span class="sxs-lookup"><span data-stu-id="f90ce-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f90ce-135"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f90ce-135"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f90ce-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="f90ce-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f90ce-137">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="f90ce-137">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

