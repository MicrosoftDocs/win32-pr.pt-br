---
description: A \_ associação CIM CollectionOfSensors representa os sensores binários que compõem o sensor de multiestado.
ms.assetid: d9494716-bb4e-4aa2-9e3b-e865360c740f
ms.tgt_platform: multiple
title: Classe CIM_CollectionOfSensors
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_CollectionOfSensors
- CIM_CollectionOfSensors.PartComponent
- CIM_CollectionOfSensors.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 06f33d3b55c2c35526495d492b0f063fee9c1a0c
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103920433"
---
# <a name="cim_collectionofsensors-class"></a><span data-ttu-id="7639c-103">\_Classe CIM CollectionOfSensors</span><span class="sxs-lookup"><span data-stu-id="7639c-103">CIM\_CollectionOfSensors class</span></span>

<span data-ttu-id="7639c-104">A associação **CIM \_ CollectionOfSensors** representa os sensores binários que compõem o sensor de multiestado.</span><span class="sxs-lookup"><span data-stu-id="7639c-104">The **CIM\_CollectionOfSensors** association represents the binary sensors that make up the multistate sensor.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7639c-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="7639c-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="7639c-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="7639c-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="7639c-107">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7639c-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="7639c-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="7639c-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="7639c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7639c-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{A2ABF536-DB35-11d2-85FC-0000F8102E5F}"), AMENDMENT]
class CIM_CollectionOfSensors : CIM_Component
{
  CIM_BinarySensor     REF PartComponent;
  CIM_MultiStateSensor REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="7639c-110">Membros</span><span class="sxs-lookup"><span data-stu-id="7639c-110">Members</span></span>

<span data-ttu-id="7639c-111">A classe **CIM \_ CollectionOfSensors** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7639c-111">The **CIM\_CollectionOfSensors** class has these types of members:</span></span>

-   [<span data-ttu-id="7639c-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7639c-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7639c-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7639c-113">Properties</span></span>

<span data-ttu-id="7639c-114">A classe **CIM \_ CollectionOfSensors** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7639c-114">The **CIM\_CollectionOfSensors** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7639c-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="7639c-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7639c-116">Tipo de dados: **CIM \_ MultiStateSensor**</span><span class="sxs-lookup"><span data-stu-id="7639c-116">Data type: **CIM\_MultiStateSensor**</span></span>
</dt> <dt>

<span data-ttu-id="7639c-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7639c-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7639c-118">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="7639c-118">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="7639c-119">Um [**\_ MultiStateSensor CIM**](cim-multistatesensor.md) que descreve o sensor de vários Estados.</span><span class="sxs-lookup"><span data-stu-id="7639c-119">A [**CIM\_MultiStateSensor**](cim-multistatesensor.md) that describes the multi-state sensor.</span></span>

</dd> <dt>

<span data-ttu-id="7639c-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7639c-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7639c-121">Tipo de dados: **CIM \_ BinarySensor**</span><span class="sxs-lookup"><span data-stu-id="7639c-121">Data type: **CIM\_BinarySensor**</span></span>
</dt> <dt>

<span data-ttu-id="7639c-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7639c-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="7639c-123">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="7639c-123">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (2), [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="7639c-124">Um [**\_ BinarySensor CIM**](cim-binarysensor.md) que descreve um sensor binário que faz parte do sensor de vários Estados.</span><span class="sxs-lookup"><span data-stu-id="7639c-124">A [**CIM\_BinarySensor**](cim-binarysensor.md) that describes a binary sensor that is part of the multi-state sensor.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7639c-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7639c-125">Remarks</span></span>

<span data-ttu-id="7639c-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="7639c-126">WMI does not implement this class.</span></span>

<span data-ttu-id="7639c-127">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="7639c-127">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="7639c-128">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="7639c-128">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="7639c-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7639c-129">Requirements</span></span>



| <span data-ttu-id="7639c-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="7639c-130">Requirement</span></span> | <span data-ttu-id="7639c-131">Valor</span><span class="sxs-lookup"><span data-stu-id="7639c-131">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7639c-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7639c-132">Minimum supported client</span></span><br/> | <span data-ttu-id="7639c-133">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="7639c-133">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="7639c-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7639c-134">Minimum supported server</span></span><br/> | <span data-ttu-id="7639c-135">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="7639c-135">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="7639c-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="7639c-136">Namespace</span></span><br/>                | <span data-ttu-id="7639c-137">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="7639c-137">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="7639c-138">MOF</span><span class="sxs-lookup"><span data-stu-id="7639c-138">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7639c-139"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7639c-139"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="7639c-140">DLL</span><span class="sxs-lookup"><span data-stu-id="7639c-140">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7639c-141"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7639c-141"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7639c-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="7639c-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7639c-143">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="7639c-143">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

