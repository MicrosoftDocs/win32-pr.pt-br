---
description: A \_ classe CIM PExtentRedundancyComponent representa as extensões físicas que participam de um grupo de redundância de armazenamento.
ms.assetid: 5a4bb1e8-7b99-410a-bba5-2c63beabd00e
ms.tgt_platform: multiple
title: Classe CIM_PExtentRedundancyComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PExtentRedundancyComponent
- CIM_PExtentRedundancyComponent.PartComponent
- CIM_PExtentRedundancyComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: fb2b6a88a789e93ca45f8469e0e67449e3473ddc
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104456928"
---
# <a name="cim_pextentredundancycomponent-class"></a><span data-ttu-id="2ef91-103">\_Classe CIM PExtentRedundancyComponent</span><span class="sxs-lookup"><span data-stu-id="2ef91-103">CIM\_PExtentRedundancyComponent class</span></span>

<span data-ttu-id="2ef91-104">A classe **CIM \_ PExtentRedundancyComponent** representa as extensões físicas que participam de um grupo de redundância de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2ef91-104">The **CIM\_PExtentRedundancyComponent** class represents the physical extents that participate in a storage redundancy group.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ef91-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="2ef91-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="2ef91-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="2ef91-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="2ef91-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="2ef91-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="2ef91-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="2ef91-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ef91-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ef91-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{AD3C1FA2-DB36-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_PExtentRedundancyComponent : CIM_RedundancyComponent
{
  CIM_PhysicalExtent         REF PartComponent;
  CIM_StorageRedundancyGroup REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="2ef91-110">Membros</span><span class="sxs-lookup"><span data-stu-id="2ef91-110">Members</span></span>

<span data-ttu-id="2ef91-111">A classe **CIM \_ PExtentRedundancyComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="2ef91-111">The **CIM\_PExtentRedundancyComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="2ef91-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ef91-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="2ef91-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="2ef91-113">Properties</span></span>

<span data-ttu-id="2ef91-114">A classe **CIM \_ PExtentRedundancyComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="2ef91-114">The **CIM\_PExtentRedundancyComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="2ef91-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="2ef91-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ef91-116">Tipo de dados: **CIM \_ StorageRedundancyGroup**</span><span class="sxs-lookup"><span data-stu-id="2ef91-116">Data type: **CIM\_StorageRedundancyGroup**</span></span>
</dt> <dt>

<span data-ttu-id="2ef91-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ef91-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ef91-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="2ef91-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2ef91-119">Um [**\_ StorageRedundancyGroup CIM**](cim-storageredundancygroup.md) que descreve o grupo de redundância de armazenamento.</span><span class="sxs-lookup"><span data-stu-id="2ef91-119">A [**CIM\_StorageRedundancyGroup**](cim-storageredundancygroup.md) that describes the storage redundancy group.</span></span>

</dd> <dt>

<span data-ttu-id="2ef91-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="2ef91-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="2ef91-121">Tipo de dados: **CIM \_ PhysicalExtent**</span><span class="sxs-lookup"><span data-stu-id="2ef91-121">Data type: **CIM\_PhysicalExtent**</span></span>
</dt> <dt>

<span data-ttu-id="2ef91-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="2ef91-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="2ef91-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="2ef91-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="2ef91-124">Um [**\_ PhysicalExtent CIM**](cim-physicalextent.md) que descreve a extensão física que participa do grupo de redundância.</span><span class="sxs-lookup"><span data-stu-id="2ef91-124">A [**CIM\_PhysicalExtent**](cim-physicalextent.md) that describes the physical extent participating in the redundancy group.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="2ef91-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ef91-125">Remarks</span></span>

<span data-ttu-id="2ef91-126">A classe **CIM \_ PExtentRedundancyComponent** é derivada de [**\_ RedundancyComponent CIM**](cim-redundancycomponent.md).</span><span class="sxs-lookup"><span data-stu-id="2ef91-126">The **CIM\_PExtentRedundancyComponent** class is derived from [**CIM\_RedundancyComponent**](cim-redundancycomponent.md).</span></span>

<span data-ttu-id="2ef91-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="2ef91-127">WMI does not implement this class.</span></span>

<span data-ttu-id="2ef91-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="2ef91-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="2ef91-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="2ef91-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ef91-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ef91-130">Requirements</span></span>



| <span data-ttu-id="2ef91-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ef91-131">Requirement</span></span> | <span data-ttu-id="2ef91-132">Valor</span><span class="sxs-lookup"><span data-stu-id="2ef91-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="2ef91-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ef91-133">Minimum supported client</span></span><br/> | <span data-ttu-id="2ef91-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="2ef91-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="2ef91-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2ef91-135">Minimum supported server</span></span><br/> | <span data-ttu-id="2ef91-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="2ef91-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="2ef91-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="2ef91-137">Namespace</span></span><br/>                | <span data-ttu-id="2ef91-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="2ef91-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="2ef91-139">MOF</span><span class="sxs-lookup"><span data-stu-id="2ef91-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="2ef91-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="2ef91-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="2ef91-141">DLL</span><span class="sxs-lookup"><span data-stu-id="2ef91-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="2ef91-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="2ef91-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ef91-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ef91-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ef91-144">**\_REDUNDANCYCOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="2ef91-144">**CIM\_RedundancyComponent**</span></span>](cim-redundancycomponent.md)
</dt> </dl>

 

