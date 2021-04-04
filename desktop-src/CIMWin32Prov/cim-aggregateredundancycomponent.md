---
description: A \_ classe CIM AggregateRedundancyComponent descreve a extensão física agregada em um grupo de redundância de armazenamento.
ms.assetid: 3407e888-e17c-4f65-a33f-056002accbf7
ms.tgt_platform: multiple
title: Classe CIM_AggregateRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AggregateRedundancyComponent
- CIM_AggregateRedundancyComponent.PartComponent
- CIM_AggregateRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9a5e638730578bad8d64f35b29a5152898c23fd6
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646453"
---
# <a name="cim_aggregateredundancycomponent-class"></a><span data-ttu-id="b9c43-103">\_Classe CIM AggregateRedundancyComponent</span><span class="sxs-lookup"><span data-stu-id="b9c43-103">CIM\_AggregateRedundancyComponent class</span></span>

<span data-ttu-id="b9c43-104">A classe **CIM \_ AggregateRedundancyComponent** descreve a extensão física agregada em um grupo de redundância de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9c43-104">The **CIM\_AggregateRedundancyComponent** class describes the aggregate physical extent in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b9c43-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="b9c43-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="b9c43-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="b9c43-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="b9c43-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="b9c43-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="b9c43-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="b9c43-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="b9c43-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b9c43-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{154E66D8-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_AggregateRedundancyComponent : CIM_RedundancyComponent
{
  CIM_AggregatePExtent       REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="b9c43-110">Membros</span><span class="sxs-lookup"><span data-stu-id="b9c43-110">Members</span></span>

<span data-ttu-id="b9c43-111">A classe **CIM \_ AggregateRedundancyComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="b9c43-111">The **CIM\_AggregateRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="b9c43-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b9c43-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="b9c43-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="b9c43-113">Properties</span></span>

<span data-ttu-id="b9c43-114">A classe **CIM \_ AggregateRedundancyComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="b9c43-114">The **CIM\_AggregateRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="b9c43-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="b9c43-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c43-116">Tipo de dados: **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="b9c43-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="b9c43-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9c43-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9c43-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="b9c43-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b9c43-119">Um [**\_ StorageRedundancyGroup CIM**](cim-storageredundancygroup.md) que contém o grupo de redundância de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="b9c43-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that contains the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="b9c43-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="b9c43-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="b9c43-121">Tipo de dados: **CIM \_ AggregatePExtent**</span><span class="sxs-lookup"><span data-stu-id="b9c43-121">Data type: **CIM\_AggregatePExtent**</span></span>
</dt> <dt>

<span data-ttu-id="b9c43-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="b9c43-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="b9c43-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="b9c43-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="b9c43-124">Um [**\_ AggregatePExtent CIM**](cim-aggregatepextent.md) que contém a extensão física agregada que participa do grupo de redundância.</span><span class="sxs-lookup"><span data-stu-id="b9c43-124">A [**CIM\_AggregatePExtent**](cim-aggregatepextent.md) that contains the aggregate physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="b9c43-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="b9c43-125">Remarks</span></span>

<span data-ttu-id="b9c43-126">A classe **CIM \_ AggregateRedundancyComponent** é derivada de [**\_ RedundancyComponent CIM**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="b9c43-126">The **CIM\_AggregateRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="b9c43-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="b9c43-127">WMI does not implement this class.</span></span>

<span data-ttu-id="b9c43-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="b9c43-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="b9c43-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="b9c43-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="b9c43-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b9c43-130">Requirements</span></span>



| <span data-ttu-id="b9c43-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b9c43-131">Requirement</span></span> | <span data-ttu-id="b9c43-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b9c43-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="b9c43-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9c43-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b9c43-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="b9c43-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="b9c43-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b9c43-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b9c43-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="b9c43-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="b9c43-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="b9c43-137">Namespace</span></span><br/>                | <span data-ttu-id="b9c43-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="b9c43-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="b9c43-139">MOF</span><span class="sxs-lookup"><span data-stu-id="b9c43-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="b9c43-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="b9c43-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="b9c43-141">DLL</span><span class="sxs-lookup"><span data-stu-id="b9c43-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b9c43-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b9c43-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b9c43-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="b9c43-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b9c43-144">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="b9c43-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

