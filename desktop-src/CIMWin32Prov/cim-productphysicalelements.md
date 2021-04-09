---
description: A \_ classe CIM ProductPhysicalElements representa os elementos físicos que compõem um produto.
ms.assetid: cf23098a-f61e-4778-883e-1a5138af3da0
ms.tgt_platform: multiple
title: Classe CIM_ProductPhysicalElements
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ProductPhysicalElements
- CIM_ProductPhysicalElements.Component
- CIM_ProductPhysicalElements.Product
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a581293426c421de0dd76636a9f446f245f6ab32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089039"
---
# <a name="cim_productphysicalelements-class"></a><span data-ttu-id="9b38f-103">\_Classe CIM ProductPhysicalElements</span><span class="sxs-lookup"><span data-stu-id="9b38f-103">CIM\_ProductPhysicalElements class</span></span>

<span data-ttu-id="9b38f-104">A classe **CIM \_ ProductPhysicalElements** representa os elementos físicos que compõem um produto.</span><span class="sxs-lookup"><span data-stu-id="9b38f-104">The **CIM\_ProductPhysicalElements** class represents the physical elements that make up a product.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9b38f-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="9b38f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="9b38f-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="9b38f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="9b38f-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="9b38f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="9b38f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="9b38f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="9b38f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9b38f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{502F00A0-DB2B-11d2-85FC-0000F8102E5F}"), Aggregation, Association, AMENDMENT]
class CIM_ProductPhysicalElements
{
  CIM_PhysicalElement REF Component;
  CIM_Product         REF Product;
};
```

## <a name="members"></a><span data-ttu-id="9b38f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="9b38f-110">Members</span></span>

<span data-ttu-id="9b38f-111">A classe **CIM \_ ProductPhysicalElements** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9b38f-111">The **CIM\_ProductPhysicalElements** class has these types of members:</span></span>

-   [<span data-ttu-id="9b38f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9b38f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="9b38f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="9b38f-113">Properties</span></span>

<span data-ttu-id="9b38f-114">A classe **CIM \_ ProductPhysicalElements** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="9b38f-114">The **CIM\_ProductPhysicalElements** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="9b38f-115">**Componente**</span><span class="sxs-lookup"><span data-stu-id="9b38f-115">**Component**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b38f-116">Tipo de dados: **CIM \_ físicoelement**</span><span class="sxs-lookup"><span data-stu-id="9b38f-116">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="9b38f-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b38f-117">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="9b38f-118">Referência ao elemento físico que faz parte do produto.</span><span class="sxs-lookup"><span data-stu-id="9b38f-118">Reference to the physical element that is part of the product.</span></span>

</dd> <dt>

<span data-ttu-id="9b38f-119">**Product**</span><span class="sxs-lookup"><span data-stu-id="9b38f-119">**Product**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9b38f-120">Tipo de dados **: \_ produto CIM**</span><span class="sxs-lookup"><span data-stu-id="9b38f-120">Data type: **CIM\_Product**</span></span>
</dt> <dt>

<span data-ttu-id="9b38f-121">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="9b38f-121">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="9b38f-122">Qualificadores: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="9b38f-122">Qualifiers: [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="9b38f-123">Referência ao produto.</span><span class="sxs-lookup"><span data-stu-id="9b38f-123">Reference to the product.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="9b38f-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="9b38f-124">Remarks</span></span>

<span data-ttu-id="9b38f-125">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="9b38f-125">WMI does not implement this class.</span></span>

<span data-ttu-id="9b38f-126">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="9b38f-126">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="9b38f-127">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="9b38f-127">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="9b38f-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9b38f-128">Requirements</span></span>



| <span data-ttu-id="9b38f-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="9b38f-129">Requirement</span></span> | <span data-ttu-id="9b38f-130">Valor</span><span class="sxs-lookup"><span data-stu-id="9b38f-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="9b38f-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b38f-131">Minimum supported client</span></span><br/> | <span data-ttu-id="9b38f-132">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="9b38f-132">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="9b38f-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9b38f-133">Minimum supported server</span></span><br/> | <span data-ttu-id="9b38f-134">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="9b38f-134">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="9b38f-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="9b38f-135">Namespace</span></span><br/>                | <span data-ttu-id="9b38f-136">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="9b38f-136">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="9b38f-137">MOF</span><span class="sxs-lookup"><span data-stu-id="9b38f-137">MOF</span></span><br/>                      | <dl> <span data-ttu-id="9b38f-138"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="9b38f-138"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="9b38f-139">DLL</span><span class="sxs-lookup"><span data-stu-id="9b38f-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9b38f-140"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9b38f-140"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

