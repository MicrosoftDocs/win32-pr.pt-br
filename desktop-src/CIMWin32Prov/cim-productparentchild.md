---
description: A \_ associação CIM ProductParentChild define uma hierarquia pai-filho entre os produtos. Por exemplo, um produto pode ser agrupado com outros produtos.
ms.assetid: 244576fd-8dae-4554-b80b-0cac58c93037
ms.tgt_platform: multiple
title: Classe CIM_ProductParentChild
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductParentChild
- CIM_ProductParentChild.Child
- CIM_ProductParentChild.Parent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3a5fd34cc3dffc6d5c8df7f7a76d9cada7856d57
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104500840"
---
# <a name="cim_productparentchild-class"></a><span data-ttu-id="408e5-104">\_Classe CIM ProductParentChild</span><span class="sxs-lookup"><span data-stu-id="408e5-104">CIM\_ProductParentChild class</span></span>

<span data-ttu-id="408e5-105">A associação **CIM \_ ProductParentChild** define uma hierarquia pai-filho entre os produtos.</span><span class="sxs-lookup"><span data-stu-id="408e5-105">The **CIM\_ProductParentChild** association defines a parent-child hierarchy among products.</span></span> <span data-ttu-id="408e5-106">Por exemplo, um produto pode ser agrupado com outros produtos.</span><span class="sxs-lookup"><span data-stu-id="408e5-106">For example, a product can come bundled with other products.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="408e5-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="408e5-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="408e5-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="408e5-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="408e5-109">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="408e5-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="408e5-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="408e5-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="408e5-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="408e5-111">Syntax</span></span>

``` syntax
[Abstract, UUID("{3E24D5A6-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductParentChild
{
  CIM_Product REF Child;
  CIM_Product REF Parent;
};
```

## <a name="members"></a><span data-ttu-id="408e5-112">Membros</span><span class="sxs-lookup"><span data-stu-id="408e5-112">Members</span></span>

<span data-ttu-id="408e5-113">A classe **CIM \_ ProductParentChild** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="408e5-113">The **CIM\_ProductParentChild** class has these types of members:</span></span>

-   [<span data-ttu-id="408e5-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="408e5-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="408e5-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="408e5-115">Properties</span></span>

<span data-ttu-id="408e5-116">A classe **CIM \_ ProductParentChild** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="408e5-116">The **CIM\_ProductParentChild** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="408e5-117">**Filho**</span><span class="sxs-lookup"><span data-stu-id="408e5-117">**Child**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="408e5-118">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="408e5-118">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="408e5-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="408e5-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="408e5-120">Referência ao produto filho na associação.</span><span class="sxs-lookup"><span data-stu-id="408e5-120">Reference to the child product in the association.</span></span>

</dd> <dt>

<span data-ttu-id="408e5-121">**Pai**</span><span class="sxs-lookup"><span data-stu-id="408e5-121">**Parent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="408e5-122">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="408e5-122">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="408e5-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="408e5-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="408e5-124">Qualificadores: [ **agregação**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="408e5-124">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="408e5-125">Referência ao produto pai na associação.</span><span class="sxs-lookup"><span data-stu-id="408e5-125">Reference to the parent product in the association.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="408e5-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="408e5-126">Remarks</span></span>

<span data-ttu-id="408e5-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="408e5-127">WMI does not implement this class.</span></span>

<span data-ttu-id="408e5-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="408e5-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="408e5-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="408e5-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="408e5-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="408e5-130">Requirements</span></span>



| <span data-ttu-id="408e5-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="408e5-131">Requirement</span></span> | <span data-ttu-id="408e5-132">Valor</span><span class="sxs-lookup"><span data-stu-id="408e5-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="408e5-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="408e5-133">Minimum supported client</span></span><br/> | <span data-ttu-id="408e5-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="408e5-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="408e5-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="408e5-135">Minimum supported server</span></span><br/> | <span data-ttu-id="408e5-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="408e5-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="408e5-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="408e5-137">Namespace</span></span><br/>                | <span data-ttu-id="408e5-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="408e5-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="408e5-139">MOF</span><span class="sxs-lookup"><span data-stu-id="408e5-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="408e5-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="408e5-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="408e5-141">DLL</span><span class="sxs-lookup"><span data-stu-id="408e5-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="408e5-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="408e5-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

