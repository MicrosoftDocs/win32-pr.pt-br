---
description: A \_ associação CIM AdjacentSlots descreve o layout dos slots em uma placa de adaptador ou placa de hospedagem.
ms.assetid: d604647f-7b2f-4f99-8d98-adf115ae9dfb
ms.tgt_platform: multiple
title: Classe CIM_AdjacentSlots
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_AdjacentSlots
- CIM_AdjacentSlots.DistanceBetweenSlots
- CIM_AdjacentSlots.SharedSlots
- CIM_AdjacentSlots.SlotA
- CIM_AdjacentSlots.SlotB
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 695f9c668d6f75864e46026deac9a969993596ff
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089407"
---
# <a name="cim_adjacentslots-class"></a><span data-ttu-id="aa00b-103">\_Classe CIM AdjacentSlots</span><span class="sxs-lookup"><span data-stu-id="aa00b-103">CIM\_AdjacentSlots class</span></span>

<span data-ttu-id="aa00b-104">A associação **CIM \_ AdjacentSlots** descreve o layout dos slots em uma placa de adaptador ou placa de hospedagem.</span><span class="sxs-lookup"><span data-stu-id="aa00b-104">The **CIM\_AdjacentSlots** association describes the layout of slots on a hosting board or adapter card.</span></span> <span data-ttu-id="aa00b-105">Informações, como a distância entre os slots e se elas são "compartilhadas" (se uma for populada, o outro slot não poderá ser usado), será transmitido como propriedades de associação.</span><span class="sxs-lookup"><span data-stu-id="aa00b-105">Information, such as the distance between the slots and whether they are "shared" (if one is populated, then the other slot cannot be used), is conveyed as association properties.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="aa00b-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="aa00b-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="aa00b-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="aa00b-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="aa00b-108">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="aa00b-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="aa00b-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="aa00b-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa00b-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa00b-110">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{FAF76B88-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_AdjacentSlots
{
  real32       DistanceBetweenSlots;
  boolean      SharedSlots;
  CIM_Slot REF SlotA;
  CIM_Slot REF SlotB;
};
```

## <a name="members"></a><span data-ttu-id="aa00b-111">Membros</span><span class="sxs-lookup"><span data-stu-id="aa00b-111">Members</span></span>

<span data-ttu-id="aa00b-112">A classe **CIM \_ AdjacentSlots** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="aa00b-112">The **CIM\_AdjacentSlots** class has these types of members:</span></span>

-   [<span data-ttu-id="aa00b-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aa00b-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="aa00b-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="aa00b-114">Properties</span></span>

<span data-ttu-id="aa00b-115">A classe **CIM \_ AdjacentSlots** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="aa00b-115">The **CIM\_AdjacentSlots** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="aa00b-116">**DistanceBetweenSlots**</span><span class="sxs-lookup"><span data-stu-id="aa00b-116">**DistanceBetweenSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa00b-117">Tipo de dados: **real32**</span><span class="sxs-lookup"><span data-stu-id="aa00b-117">Data type: **real32**</span></span>
</dt> <dt>

<span data-ttu-id="aa00b-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa00b-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="aa00b-119">Qualificadores: [**unidades**](/windows/desktop/WmiSdk/standard-qualifiers) ("polegadas")</span><span class="sxs-lookup"><span data-stu-id="aa00b-119">Qualifiers: [**Units**](/windows/desktop/WmiSdk/standard-qualifiers) ("inches")</span></span>
</dt> </dl>

<span data-ttu-id="aa00b-120">Distância, em polegadas, entre os slots adjacentes.</span><span class="sxs-lookup"><span data-stu-id="aa00b-120">Distance, in inches, between adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="aa00b-121">**SharedSlots**</span><span class="sxs-lookup"><span data-stu-id="aa00b-121">**SharedSlots**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa00b-122">Tipo de dados: **booliano**</span><span class="sxs-lookup"><span data-stu-id="aa00b-122">Data type: **boolean**</span></span>
</dt> <dt>

<span data-ttu-id="aa00b-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa00b-123">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa00b-124">Se for **true**, um dos slots será preenchido por uma placa de adaptador; o outro slot deve ser deixado vazio.</span><span class="sxs-lookup"><span data-stu-id="aa00b-124">If **TRUE**, one of the slots is populated by an adapter card; the other slot must be left empty.</span></span>

</dd> <dt>

<span data-ttu-id="aa00b-125">**Slota**</span><span class="sxs-lookup"><span data-stu-id="aa00b-125">**SlotA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa00b-126">Tipo de dados **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="aa00b-126">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="aa00b-127">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa00b-127">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa00b-128">Referência a um dos slots adjacentes.</span><span class="sxs-lookup"><span data-stu-id="aa00b-128">Reference to one of the adjacent slots.</span></span>

</dd> <dt>

<span data-ttu-id="aa00b-129">**SlotB**</span><span class="sxs-lookup"><span data-stu-id="aa00b-129">**SlotB**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="aa00b-130">Tipo de dados **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="aa00b-130">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="aa00b-131">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="aa00b-131">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="aa00b-132">Referência ao slot adjacente "other".</span><span class="sxs-lookup"><span data-stu-id="aa00b-132">Reference to the "other" adjacent slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aa00b-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa00b-133">Remarks</span></span>

<span data-ttu-id="aa00b-134">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="aa00b-134">WMI does not implement this class.</span></span>

<span data-ttu-id="aa00b-135">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="aa00b-135">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="aa00b-136">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="aa00b-136">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa00b-137">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa00b-137">Requirements</span></span>



| <span data-ttu-id="aa00b-138">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa00b-138">Requirement</span></span> | <span data-ttu-id="aa00b-139">Valor</span><span class="sxs-lookup"><span data-stu-id="aa00b-139">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="aa00b-140">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa00b-140">Minimum supported client</span></span><br/> | <span data-ttu-id="aa00b-141">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="aa00b-141">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="aa00b-142">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="aa00b-142">Minimum supported server</span></span><br/> | <span data-ttu-id="aa00b-143">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="aa00b-143">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="aa00b-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="aa00b-144">Namespace</span></span><br/>                | <span data-ttu-id="aa00b-145">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="aa00b-145">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="aa00b-146">MOF</span><span class="sxs-lookup"><span data-stu-id="aa00b-146">MOF</span></span><br/>                      | <dl> <span data-ttu-id="aa00b-147"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="aa00b-147"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="aa00b-148">DLL</span><span class="sxs-lookup"><span data-stu-id="aa00b-148">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aa00b-149"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aa00b-149"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa00b-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa00b-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa00b-151">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="aa00b-151">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

