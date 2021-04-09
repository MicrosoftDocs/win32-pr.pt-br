---
description: A \_ classe CIM PhysicalCapacity é uma classe abstrata que representa os requisitos mínimos e máximos de um elemento físico e sua capacidade de dar suporte a diferentes tipos de hardware.
ms.assetid: e422aec0-1830-464e-ac52-2911652165a2
ms.tgt_platform: multiple
title: Classe CIM_PhysicalCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PhysicalCapacity
- CIM_PhysicalCapacity.Caption
- CIM_PhysicalCapacity.Description
- CIM_PhysicalCapacity.Name
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 50f928f69d34600c0f90865a4df44a5d7697fc89
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920427"
---
# <a name="cim_physicalcapacity-class"></a><span data-ttu-id="e998f-103">\_Classe CIM PhysicalCapacity</span><span class="sxs-lookup"><span data-stu-id="e998f-103">CIM\_PhysicalCapacity class</span></span>

<span data-ttu-id="e998f-104">A classe **CIM \_ PhysicalCapacity** é uma classe abstrata que representa os requisitos mínimos e máximos de um elemento físico e sua capacidade de dar suporte a diferentes tipos de hardware.</span><span class="sxs-lookup"><span data-stu-id="e998f-104">The **CIM\_PhysicalCapacity** class is an abstract class that represents a physical element's minimum and maximum requirements and its ability to support different types of hardware.</span></span> <span data-ttu-id="e998f-105">Por exemplo, os requisitos mínimos e máximos de memória podem ser modelados como uma subclasse de **\_ PhysicalCapacity CIM**.</span><span class="sxs-lookup"><span data-stu-id="e998f-105">For example, minimum and maximum memory requirements can be modeled as a subclass of **CIM\_PhysicalCapacity**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e998f-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e998f-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e998f-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e998f-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e998f-108">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e998f-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e998f-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e998f-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e998f-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e998f-110">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B69-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PhysicalCapacity
{
  string Caption;
  string Description;
  string Name;
};
```

## <a name="members"></a><span data-ttu-id="e998f-111">Membros</span><span class="sxs-lookup"><span data-stu-id="e998f-111">Members</span></span>

<span data-ttu-id="e998f-112">A classe **CIM \_ PhysicalCapacity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e998f-112">The **CIM\_PhysicalCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="e998f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e998f-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e998f-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e998f-114">Properties</span></span>

<span data-ttu-id="e998f-115">A classe **CIM \_ PhysicalCapacity** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e998f-115">The **CIM\_PhysicalCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e998f-116">**Legenda**</span><span class="sxs-lookup"><span data-stu-id="e998f-116">**Caption**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e998f-117">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e998f-117">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e998f-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e998f-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e998f-119">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span><span class="sxs-lookup"><span data-stu-id="e998f-119">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (64)</span></span>
</dt> </dl>

<span data-ttu-id="e998f-120">Breve descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e998f-120">Short textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="e998f-121">**Descrição**</span><span class="sxs-lookup"><span data-stu-id="e998f-121">**Description**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e998f-122">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e998f-122">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e998f-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e998f-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e998f-124">Descrição textual do objeto.</span><span class="sxs-lookup"><span data-stu-id="e998f-124">Textual description of the object.</span></span>

</dd> <dt>

<span data-ttu-id="e998f-125">**Nome**</span><span class="sxs-lookup"><span data-stu-id="e998f-125">**Name**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e998f-126">Tipo de dados: **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="e998f-126">Data type: **string**</span></span>
</dt> <dt>

<span data-ttu-id="e998f-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e998f-127">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e998f-128">Qualificadores: [**maxlen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span><span class="sxs-lookup"><span data-stu-id="e998f-128">Qualifiers: [**MaxLen**](/windows/desktop/WmiSdk/standard-qualifiers) (256)</span></span>
</dt> </dl>

<span data-ttu-id="e998f-129">Rótulo pelo qual o objeto é conhecido.</span><span class="sxs-lookup"><span data-stu-id="e998f-129">Label by which the object is known.</span></span> <span data-ttu-id="e998f-130">Quando em uma subclasse, essa propriedade pode ser substituída como uma propriedade de chave.</span><span class="sxs-lookup"><span data-stu-id="e998f-130">When subclassed, this property can be overridden to be a key property.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="e998f-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="e998f-131">Remarks</span></span>

<span data-ttu-id="e998f-132">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e998f-132">WMI does not implement this class.</span></span>

<span data-ttu-id="e998f-133">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e998f-133">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e998f-134">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e998f-134">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e998f-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e998f-135">Requirements</span></span>



| <span data-ttu-id="e998f-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="e998f-136">Requirement</span></span> | <span data-ttu-id="e998f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="e998f-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e998f-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e998f-138">Minimum supported client</span></span><br/> | <span data-ttu-id="e998f-139">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e998f-139">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e998f-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e998f-140">Minimum supported server</span></span><br/> | <span data-ttu-id="e998f-141">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e998f-141">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e998f-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="e998f-142">Namespace</span></span><br/>                | <span data-ttu-id="e998f-143">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e998f-143">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e998f-144">MOF</span><span class="sxs-lookup"><span data-stu-id="e998f-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e998f-145"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e998f-145"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e998f-146">DLL</span><span class="sxs-lookup"><span data-stu-id="e998f-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e998f-147"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e998f-147"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

