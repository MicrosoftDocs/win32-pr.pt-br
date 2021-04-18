---
description: A \_ associação CIM ElementsLinked representa os elementos físicos que são cabeados juntos por um link físico.
ms.assetid: b9e1d11e-6f89-4d7a-9b5c-01161e7c1bdf
ms.tgt_platform: multiple
title: Classe CIM_ElementsLinked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementsLinked
- CIM_ElementsLinked.Dependent
- CIM_ElementsLinked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 353809056d1ca3bae710272b02c2636a3f02eef1
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105756444"
---
# <a name="cim_elementslinked-class"></a><span data-ttu-id="3edcf-103">\_Classe CIM ElementsLinked</span><span class="sxs-lookup"><span data-stu-id="3edcf-103">CIM\_ElementsLinked class</span></span>

<span data-ttu-id="3edcf-104">A associação **CIM \_ ElementsLinked** representa os elementos físicos que são cabeados juntos por um link físico.</span><span class="sxs-lookup"><span data-stu-id="3edcf-104">The **CIM\_ElementsLinked** association represents physical elements that are cabled together by a physical link.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3edcf-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="3edcf-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="3edcf-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="3edcf-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="3edcf-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="3edcf-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="3edcf-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="3edcf-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="3edcf-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3edcf-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B83-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementsLinked : CIM_Dependency
{
  CIM_PhysicalElement REF Dependent;
  CIM_PhysicalLink    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="3edcf-110">Membros</span><span class="sxs-lookup"><span data-stu-id="3edcf-110">Members</span></span>

<span data-ttu-id="3edcf-111">A classe **CIM \_ ElementsLinked** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="3edcf-111">The **CIM\_ElementsLinked** class has these types of members:</span></span>

-   [<span data-ttu-id="3edcf-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3edcf-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="3edcf-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="3edcf-113">Properties</span></span>

<span data-ttu-id="3edcf-114">A classe **CIM \_ ElementsLinked** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="3edcf-114">The **CIM\_ElementsLinked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="3edcf-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="3edcf-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3edcf-116">Tipo de dados: **CIM \_ PhysicalLink**</span><span class="sxs-lookup"><span data-stu-id="3edcf-116">Data type: **CIM\_PhysicalLink**</span></span>
</dt> <dt>

<span data-ttu-id="3edcf-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3edcf-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3edcf-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="3edcf-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="3edcf-119">Um [**\_ PhysicalLink CIM**](cim-physicallink.md) que descreve o link físico.</span><span class="sxs-lookup"><span data-stu-id="3edcf-119">A [**CIM\_PhysicalLink**](cim-physicallink.md) that describes the physical link.</span></span>

</dd> <dt>

<span data-ttu-id="3edcf-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="3edcf-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3edcf-121">Tipo de dados: **CIM \_ físicoelement**</span><span class="sxs-lookup"><span data-stu-id="3edcf-121">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="3edcf-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="3edcf-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="3edcf-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="3edcf-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="3edcf-124">Um [**\_ físicoelement do CIM**](cim-physicalelement.md) que descreve o elemento físico que está vinculado.</span><span class="sxs-lookup"><span data-stu-id="3edcf-124">A [**CIM\_PhysicalElement**](cim-physicalelement.md) that describes the physical element that is linked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3edcf-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="3edcf-125">Remarks</span></span>

<span data-ttu-id="3edcf-126">A classe **CIM \_ ElementsLinked** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="3edcf-126">The **CIM\_ElementsLinked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="3edcf-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="3edcf-127">WMI does not implement this class.</span></span>

<span data-ttu-id="3edcf-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="3edcf-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="3edcf-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="3edcf-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="3edcf-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3edcf-130">Requirements</span></span>



| <span data-ttu-id="3edcf-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="3edcf-131">Requirement</span></span> | <span data-ttu-id="3edcf-132">Valor</span><span class="sxs-lookup"><span data-stu-id="3edcf-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3edcf-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3edcf-133">Minimum supported client</span></span><br/> | <span data-ttu-id="3edcf-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3edcf-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3edcf-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3edcf-135">Minimum supported server</span></span><br/> | <span data-ttu-id="3edcf-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3edcf-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3edcf-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="3edcf-137">Namespace</span></span><br/>                | <span data-ttu-id="3edcf-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="3edcf-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="3edcf-139">MOF</span><span class="sxs-lookup"><span data-stu-id="3edcf-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="3edcf-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="3edcf-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="3edcf-141">DLL</span><span class="sxs-lookup"><span data-stu-id="3edcf-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3edcf-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3edcf-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3edcf-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="3edcf-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3edcf-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="3edcf-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

