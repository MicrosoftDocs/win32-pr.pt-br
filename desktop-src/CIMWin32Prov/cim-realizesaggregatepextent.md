---
description: A \_ associação CIM RealizesAggregatePExtent representa a relação na qual a \_ classe CIM AggregatePExtent é realizada em uma mídia física.
ms.assetid: 420dde1d-daa8-4cd3-b3fd-c2aefdc1e217
ms.tgt_platform: multiple
title: Classe CIM_RealizesAggregatePExtent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_RealizesAggregatePExtent
- CIM_RealizesAggregatePExtent.Dependent
- CIM_RealizesAggregatePExtent.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: eb80414134534d09a4030e2e87003a660e69fd9f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755437"
---
# <a name="cim_realizesaggregatepextent-class"></a><span data-ttu-id="25e47-103">\_Classe CIM RealizesAggregatePExtent</span><span class="sxs-lookup"><span data-stu-id="25e47-103">CIM\_RealizesAggregatePExtent class</span></span>

<span data-ttu-id="25e47-104">A associação **CIM \_ RealizesAggregatePExtent** representa a relação na qual a classe [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) é realizada em uma mídia física.</span><span class="sxs-lookup"><span data-stu-id="25e47-104">The **CIM\_RealizesAggregatePExtent** association represents the relationship in which the [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) class is realized on a physical media.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="25e47-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="25e47-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="25e47-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="25e47-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="25e47-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="25e47-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="25e47-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="25e47-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="25e47-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25e47-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B81-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_RealizesAggregatePExtent : CIM_Realizes
{
  CIM_AggregatePExtent REF Dependent;
  CIM_PhysicalMedia    REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="25e47-110">Membros</span><span class="sxs-lookup"><span data-stu-id="25e47-110">Members</span></span>

<span data-ttu-id="25e47-111">A classe **CIM \_ RealizesAggregatePExtent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="25e47-111">The **CIM\_RealizesAggregatePExtent** class has these types of members:</span></span>

-   [<span data-ttu-id="25e47-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="25e47-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="25e47-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="25e47-113">Properties</span></span>

<span data-ttu-id="25e47-114">A classe **CIM \_ RealizesAggregatePExtent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="25e47-114">The **CIM\_RealizesAggregatePExtent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="25e47-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="25e47-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25e47-116">Tipo de dados: **CIM \_ PhysicalMedia**</span><span class="sxs-lookup"><span data-stu-id="25e47-116">Data type: **CIM\_PhysicalMedia**</span></span>
</dt> <dt>

<span data-ttu-id="25e47-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25e47-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25e47-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="25e47-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="25e47-119">Um [**\_ PhysicalMedia CIM**](cim-physicalmedia.md) que descreve a mídia física na qual a extensão é realizada.</span><span class="sxs-lookup"><span data-stu-id="25e47-119">A [**CIM\_PhysicalMedia**](cim-physicalmedia.md) that describes the physical media on which the extent is realized.</span></span>

</dd> <dt>

<span data-ttu-id="25e47-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="25e47-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="25e47-121">Tipo de dados: **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="25e47-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="25e47-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="25e47-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="25e47-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente")</span><span class="sxs-lookup"><span data-stu-id="25e47-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent")</span></span>
</dt> </dl>

<span data-ttu-id="25e47-124">O [**CIM \_ AggregatePExtent**](cim-aggregatepextent.md) que está localizado na mídia.</span><span class="sxs-lookup"><span data-stu-id="25e47-124">The [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that is located on the media.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="25e47-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="25e47-125">Remarks</span></span>

<span data-ttu-id="25e47-126">A classe **CIM \_ RealizesAggregatePExtent** é derivada do [**CIM \_**](cim-realizes.md).</span><span class="sxs-lookup"><span data-stu-id="25e47-126">The **CIM\_RealizesAggregatePExtent** class is derived from [**CIM\_Realizes**](cim-realizes.md).</span></span>

<span data-ttu-id="25e47-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="25e47-127">WMI does not implement this class.</span></span>

<span data-ttu-id="25e47-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="25e47-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="25e47-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="25e47-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="25e47-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25e47-130">Requirements</span></span>



| <span data-ttu-id="25e47-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="25e47-131">Requirement</span></span> | <span data-ttu-id="25e47-132">Valor</span><span class="sxs-lookup"><span data-stu-id="25e47-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="25e47-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25e47-133">Minimum supported client</span></span><br/> | <span data-ttu-id="25e47-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="25e47-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="25e47-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25e47-135">Minimum supported server</span></span><br/> | <span data-ttu-id="25e47-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="25e47-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="25e47-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="25e47-137">Namespace</span></span><br/>                | <span data-ttu-id="25e47-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="25e47-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="25e47-139">MOF</span><span class="sxs-lookup"><span data-stu-id="25e47-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="25e47-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="25e47-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="25e47-141">DLL</span><span class="sxs-lookup"><span data-stu-id="25e47-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25e47-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25e47-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25e47-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="25e47-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25e47-144">**O CIM \_ percebe**</span><span class="sxs-lookup"><span data-stu-id="25e47-144">**CIM\_Realizes**</span></span>](cim-realizes.md)
</dt> </dl>

 

