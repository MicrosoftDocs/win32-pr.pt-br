---
description: A \_ classe CIM AssociateMemory associa a memória instalada ou associada, como memória de cache com um dispositivo lógico.
ms.assetid: b108d0cc-9353-4940-a5f6-34bb93330a62
ms.tgt_platform: multiple
title: Classe CIM_AssociatedMemory
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AssociatedMemory
- CIM_AssociatedMemory.Dependent
- CIM_AssociatedMemory.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 3cb1443f54ab273ef6c114b8645e5322c24785f8
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457104"
---
# <a name="cim_associatedmemory-class"></a><span data-ttu-id="a20fa-103">\_Classe CIM AssociatedMemory</span><span class="sxs-lookup"><span data-stu-id="a20fa-103">CIM\_AssociatedMemory class</span></span>

<span data-ttu-id="a20fa-104">A classe **CIM \_ AssociateMemory** associa a memória instalada ou associada, como memória de cache com um dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a20fa-104">The **CIM\_AssociateMemory** class associates installed or associated memory, such as cache memory with a logical device.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a20fa-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="a20fa-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="a20fa-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="a20fa-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="a20fa-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="a20fa-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="a20fa-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="a20fa-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="a20fa-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a20fa-109">Syntax</span></span>

``` syntax
[abstract, UUID("{464FFAB0-946F-11d2-AAE2-006008C78BC7}"), AMENDMENT]
class CIM_AssociatedMemory : CIM_Dependency
{
  CIM_LogicalDevice REF Dependent;
  CIM_Memory        REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="a20fa-110">Membros</span><span class="sxs-lookup"><span data-stu-id="a20fa-110">Members</span></span>

<span data-ttu-id="a20fa-111">A classe **CIM \_ AssociatedMemory** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="a20fa-111">The **CIM\_AssociatedMemory** class has these types of members:</span></span>

-   [<span data-ttu-id="a20fa-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a20fa-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="a20fa-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="a20fa-113">Properties</span></span>

<span data-ttu-id="a20fa-114">A classe **CIM \_ AssociatedMemory** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="a20fa-114">The **CIM\_AssociatedMemory** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="a20fa-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="a20fa-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a20fa-116">Tipo de dados **: \_ memória CIM**</span><span class="sxs-lookup"><span data-stu-id="a20fa-116">Data type: **CIM\_Memory**</span></span>
</dt> <dt>

<span data-ttu-id="a20fa-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a20fa-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a20fa-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="a20fa-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="a20fa-119">Uma [**\_ memória CIM**](cim-memory.md) que descreve a memória instalada ou associada a um dispositivo.</span><span class="sxs-lookup"><span data-stu-id="a20fa-119">A [**CIM\_Memory**](cim-memory.md) that describes the memory installed on or associated with a device.</span></span>

</dd> <dt>

<span data-ttu-id="a20fa-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="a20fa-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="a20fa-121">Tipo de dados **: \_ LogicalDevice CIM**</span><span class="sxs-lookup"><span data-stu-id="a20fa-121">Data type: **CIM\_LogicalDevice**</span></span>
</dt> <dt>

<span data-ttu-id="a20fa-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="a20fa-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="a20fa-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="a20fa-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="a20fa-124">Um [**\_ LogicalDevice CIM**](cim-logicaldevice.md) que descreve o dispositivo lógico.</span><span class="sxs-lookup"><span data-stu-id="a20fa-124">A [**CIM\_LogicalDevice**](cim-logicaldevice.md) that describes the logical device.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a20fa-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="a20fa-125">Remarks</span></span>

<span data-ttu-id="a20fa-126">A classe **CIM \_ AssociatedMemory** é derivada da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="a20fa-126">The **CIM\_AssociatedMemory** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="a20fa-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="a20fa-127">WMI does not implement this class.</span></span>

<span data-ttu-id="a20fa-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="a20fa-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="a20fa-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="a20fa-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="a20fa-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a20fa-130">Requirements</span></span>



| <span data-ttu-id="a20fa-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="a20fa-131">Requirement</span></span> | <span data-ttu-id="a20fa-132">Valor</span><span class="sxs-lookup"><span data-stu-id="a20fa-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a20fa-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a20fa-133">Minimum supported client</span></span><br/> | <span data-ttu-id="a20fa-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="a20fa-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="a20fa-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a20fa-135">Minimum supported server</span></span><br/> | <span data-ttu-id="a20fa-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="a20fa-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="a20fa-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="a20fa-137">Namespace</span></span><br/>                | <span data-ttu-id="a20fa-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="a20fa-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="a20fa-139">MOF</span><span class="sxs-lookup"><span data-stu-id="a20fa-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="a20fa-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="a20fa-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="a20fa-141">DLL</span><span class="sxs-lookup"><span data-stu-id="a20fa-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a20fa-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a20fa-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a20fa-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="a20fa-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a20fa-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="a20fa-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

