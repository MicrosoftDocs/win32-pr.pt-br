---
description: A \_ classe CIM RedundancyComponent associa um grupo de redundância composto por elementos do sistema gerenciado e indica que, juntos, os elementos fornecem redundância.
ms.assetid: 2511ae26-011a-4e0d-ad34-d5fe9c78f0ff
ms.tgt_platform: multiple
title: Classe CIM_RedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RedundancyComponent
- CIM_RedundancyComponent.GroupComponent
- CIM_RedundancyComponent.PartComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 5bcd1c16417ba0c02e13579f9e471076d4c61818
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826153"
---
# <a name="cim_redundancycomponent-class"></a><span data-ttu-id="e623a-103">\_Classe CIM RedundancyComponent</span><span class="sxs-lookup"><span data-stu-id="e623a-103">CIM\_RedundancyComponent class</span></span>

<span data-ttu-id="e623a-104">A classe **CIM \_ RedundancyComponent** associa um grupo de redundância composto por elementos do sistema gerenciado e indica que, juntos, os elementos fornecem redundância.</span><span class="sxs-lookup"><span data-stu-id="e623a-104">The **CIM\_RedundancyComponent** class associates a redundancy group composed of managed system elements and indicates that, together, the elements provide redundancy.</span></span> <span data-ttu-id="e623a-105">Todos os elementos agregados em um grupo de redundância devem ser instanciações da mesma classe de objeto.</span><span class="sxs-lookup"><span data-stu-id="e623a-105">All elements aggregated in a redundancy group should be instantiations of the same object class.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e623a-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e623a-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e623a-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e623a-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e623a-108">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e623a-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e623a-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e623a-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e623a-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e623a-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FB9D6E62-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_RedundancyComponent : CIM_Component
{
  CIM_RedundancyGroup      REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="e623a-111">Membros</span><span class="sxs-lookup"><span data-stu-id="e623a-111">Members</span></span>

<span data-ttu-id="e623a-112">A classe **CIM \_ RedundancyComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e623a-112">The **CIM\_RedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="e623a-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e623a-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e623a-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e623a-114">Properties</span></span>

<span data-ttu-id="e623a-115">A classe **CIM \_ RedundancyComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e623a-115">The **CIM\_RedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e623a-116">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="e623a-116">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e623a-117">Tipo de dados: **CIM \_ RedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="e623a-117">Data type: **CIM\_RedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="e623a-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e623a-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e623a-119">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="e623a-119">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="e623a-120">A associação **CIM \_ RedundancyComponent** indica que o "este conjunto de fãs" ou "essas extensões físicas" participam de um único grupo de redundância.</span><span class="sxs-lookup"><span data-stu-id="e623a-120">The **CIM\_RedundancyComponent** association indicates that 'this set of fans' or 'these physical extents' participate in a single redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="e623a-121">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="e623a-121">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e623a-122">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="e623a-122">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="e623a-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e623a-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e623a-124">Um [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) que descreve o elemento filho na associação.</span><span class="sxs-lookup"><span data-stu-id="e623a-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element in the association.</span></span>

<span data-ttu-id="e623a-125">Esta propriedade é herdada [**do \_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="e623a-125">This property is inherited from [**CIM\_Component**](cim-component.md).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e623a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="e623a-126">Remarks</span></span>

<span data-ttu-id="e623a-127">**CIM \_ RedundancyComponent** é derivado do [**\_ componente CIM**](cim-component.md).</span><span class="sxs-lookup"><span data-stu-id="e623a-127">**CIM\_RedundancyComponent** is derived from [**CIM\_Component**](cim-component.md).</span></span>

<span data-ttu-id="e623a-128">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e623a-128">WMI does not implement this class.</span></span>

<span data-ttu-id="e623a-129">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e623a-129">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e623a-130">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e623a-130">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e623a-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e623a-131">Requirements</span></span>



| <span data-ttu-id="e623a-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="e623a-132">Requirement</span></span> | <span data-ttu-id="e623a-133">Valor</span><span class="sxs-lookup"><span data-stu-id="e623a-133">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e623a-134">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e623a-134">Minimum supported client</span></span><br/> | <span data-ttu-id="e623a-135">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e623a-135">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e623a-136">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e623a-136">Minimum supported server</span></span><br/> | <span data-ttu-id="e623a-137">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e623a-137">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e623a-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="e623a-138">Namespace</span></span><br/>                | <span data-ttu-id="e623a-139">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e623a-139">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e623a-140">MOF</span><span class="sxs-lookup"><span data-stu-id="e623a-140">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e623a-141"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e623a-141"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e623a-142">DLL</span><span class="sxs-lookup"><span data-stu-id="e623a-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e623a-143"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e623a-143"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e623a-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="e623a-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e623a-145">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="e623a-145">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

