---
description: A \_ classe CIM ElementCapacity associa um \_ objeto CIM PhysicalCapacity a um ou mais elementos físicos. Ele associa uma descrição dos requisitos mínimos e máximos de hardware (ou recursos) aos elementos físicos descritos.
ms.assetid: 368c31e8-d56b-4b90-ba3f-20d9b0de8730
ms.tgt_platform: multiple
title: Classe CIM_ElementCapacity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ElementCapacity
- CIM_ElementCapacity.Capacity
- CIM_ElementCapacity.Element
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 7c6ecac913f6d4affcd9784a30d85fa08dfe0486
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457038"
---
# <a name="cim_elementcapacity-class"></a><span data-ttu-id="617c9-104">\_Classe CIM ElementCapacity</span><span class="sxs-lookup"><span data-stu-id="617c9-104">CIM\_ElementCapacity class</span></span>

<span data-ttu-id="617c9-105">A classe **CIM \_ ElementCapacity** associa um objeto [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) a um ou mais elementos físicos.</span><span class="sxs-lookup"><span data-stu-id="617c9-105">The **CIM\_ElementCapacity** class associates a [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) object with one or more physical elements.</span></span> <span data-ttu-id="617c9-106">Ele associa uma descrição dos requisitos mínimos e máximos de hardware (ou recursos) aos elementos físicos descritos.</span><span class="sxs-lookup"><span data-stu-id="617c9-106">It associates a description of the minimum and maximum hardware requirements (or capabilities) to the physical elements being described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="617c9-107">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="617c9-107">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="617c9-108">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="617c9-108">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="617c9-109">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="617c9-109">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="617c9-110">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="617c9-110">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="617c9-111">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="617c9-111">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B6A-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_ElementCapacity
{
  CIM_PhysicalCapacity REF Capacity;
  CIM_PhysicalElement  REF Element;
};
```

## <a name="members"></a><span data-ttu-id="617c9-112">Membros</span><span class="sxs-lookup"><span data-stu-id="617c9-112">Members</span></span>

<span data-ttu-id="617c9-113">A classe **CIM \_ ElementCapacity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="617c9-113">The **CIM\_ElementCapacity** class has these types of members:</span></span>

-   [<span data-ttu-id="617c9-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="617c9-114">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="617c9-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="617c9-115">Properties</span></span>

<span data-ttu-id="617c9-116">A classe **CIM \_ ElementCapacity** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="617c9-116">The **CIM\_ElementCapacity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="617c9-117">**Capacidade**</span><span class="sxs-lookup"><span data-stu-id="617c9-117">**Capacity**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="617c9-118">Tipo de dados: **CIM \_ PhysicalCapacity**</span><span class="sxs-lookup"><span data-stu-id="617c9-118">Data type: **CIM\_PhysicalCapacity**</span></span>
</dt> <dt>

<span data-ttu-id="617c9-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="617c9-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="617c9-120">Referência à classe [**CIM \_ PhysicalCapacity**](cim-physicalcapacity.md) que descreve os requisitos mínimo e máximo e a capacidade de dar suporte a diferentes tipos de hardware para um elemento físico.</span><span class="sxs-lookup"><span data-stu-id="617c9-120">Reference to the [**CIM\_PhysicalCapacity**](cim-physicalcapacity.md) class that describes the minimum and maximum requirements and the ability to support different types of hardware for a physical element.</span></span>

</dd> <dt>

<span data-ttu-id="617c9-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="617c9-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="617c9-122">Tipo de dados: **CIM \_ físicoelement**</span><span class="sxs-lookup"><span data-stu-id="617c9-122">Data type: **CIM\_PhysicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="617c9-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="617c9-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="617c9-124">Qualificadores: [**mín**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="617c9-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="617c9-125">Referência ao elemento físico que está sendo descrito.</span><span class="sxs-lookup"><span data-stu-id="617c9-125">Reference to the physical element being described.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="617c9-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="617c9-126">Remarks</span></span>

<span data-ttu-id="617c9-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="617c9-127">WMI does not implement this class.</span></span>

<span data-ttu-id="617c9-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="617c9-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="617c9-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="617c9-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="617c9-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="617c9-130">Requirements</span></span>



| <span data-ttu-id="617c9-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="617c9-131">Requirement</span></span> | <span data-ttu-id="617c9-132">Valor</span><span class="sxs-lookup"><span data-stu-id="617c9-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="617c9-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="617c9-133">Minimum supported client</span></span><br/> | <span data-ttu-id="617c9-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="617c9-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="617c9-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="617c9-135">Minimum supported server</span></span><br/> | <span data-ttu-id="617c9-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="617c9-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="617c9-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="617c9-137">Namespace</span></span><br/>                | <span data-ttu-id="617c9-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="617c9-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="617c9-139">MOF</span><span class="sxs-lookup"><span data-stu-id="617c9-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="617c9-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="617c9-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="617c9-141">DLL</span><span class="sxs-lookup"><span data-stu-id="617c9-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="617c9-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="617c9-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

