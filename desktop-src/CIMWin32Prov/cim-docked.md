---
description: A \_ Associação de encaixe CIM representa a relação entre dois chassis. Por exemplo, um laptop (um tipo de chassi) pode ser encaixado em uma estação de encaixe (outro tipo de chassi). Essa relação típica é descrita explicitamente.
ms.assetid: 72cb36bb-f79e-4d1a-a859-4024031e4ebc
ms.tgt_platform: multiple
title: Classe CIM_Docked
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_Docked
- CIM_Docked.Dependent
- CIM_Docked.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 899b85d63293861f0a36df3d3c30610f8cff05ac
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646397"
---
# <a name="cim_docked-class"></a><span data-ttu-id="d74a8-105">\_Classe encaixada CIM</span><span class="sxs-lookup"><span data-stu-id="d74a8-105">CIM\_Docked class</span></span>

<span data-ttu-id="d74a8-106">A associação de **\_ encaixe CIM** representa a relação entre dois chassis.</span><span class="sxs-lookup"><span data-stu-id="d74a8-106">The **CIM\_Docked** association represents the relationship between two chassis.</span></span> <span data-ttu-id="d74a8-107">Por exemplo, um laptop (um tipo de chassi) pode ser encaixado em uma estação de encaixe (outro tipo de chassi).</span><span class="sxs-lookup"><span data-stu-id="d74a8-107">For example, a laptop (a type of chassis) can be docked in a docking station (another type of chassis).</span></span> <span data-ttu-id="d74a8-108">Essa relação típica é descrita explicitamente.</span><span class="sxs-lookup"><span data-stu-id="d74a8-108">This typical relationship is explicitly described.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d74a8-109">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="d74a8-109">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="d74a8-110">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="d74a8-110">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="d74a8-111">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="d74a8-111">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="d74a8-112">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d74a8-112">Syntax</span></span>

``` syntax
[Abstract, MappingStrings("MIF.DMTF|Dynamic States|001.2"), UUID("{FAF76B75-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_Docked : CIM_Dependency
{
  CIM_Chassis REF Dependent;
  CIM_Chassis REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="d74a8-113">Membros</span><span class="sxs-lookup"><span data-stu-id="d74a8-113">Members</span></span>

<span data-ttu-id="d74a8-114">A **classe \_ encaixada CIM** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="d74a8-114">The **CIM\_Docked** class has these types of members:</span></span>

-   [<span data-ttu-id="d74a8-115">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d74a8-115">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="d74a8-116">Propriedades</span><span class="sxs-lookup"><span data-stu-id="d74a8-116">Properties</span></span>

<span data-ttu-id="d74a8-117">A **classe \_ encaixada CIM** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="d74a8-117">The **CIM\_Docked** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="d74a8-118">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="d74a8-118">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d74a8-119">Tipo de dados **: \_ chassi CIM**</span><span class="sxs-lookup"><span data-stu-id="d74a8-119">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="d74a8-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d74a8-120">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d74a8-121">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span><span class="sxs-lookup"><span data-stu-id="d74a8-121">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d74a8-122">Um [**\_ chassi CIM**](cim-chassis.md) que descreve a estação de encaixe.</span><span class="sxs-lookup"><span data-stu-id="d74a8-122">A [**CIM\_Chassis**](cim-chassis.md) describing the docking station.</span></span>

</dd> <dt>

<span data-ttu-id="d74a8-123">**Depende**</span><span class="sxs-lookup"><span data-stu-id="d74a8-123">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="d74a8-124">Tipo de dados **: \_ chassi CIM**</span><span class="sxs-lookup"><span data-stu-id="d74a8-124">Data type: **CIM\_Chassis**</span></span>
</dt> <dt>

<span data-ttu-id="d74a8-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="d74a8-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="d74a8-126">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="d74a8-126">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="d74a8-127">Um [**\_ chassi CIM**](cim-chassis.md) que descreve o laptop encaixado.</span><span class="sxs-lookup"><span data-stu-id="d74a8-127">A [**CIM\_Chassis**](cim-chassis.md) describing the docked laptop.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="d74a8-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="d74a8-128">Remarks</span></span>

<span data-ttu-id="d74a8-129">A **classe \_ encaixada CIM** é derivada [**da \_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="d74a8-129">The **CIM\_Docked** class is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="d74a8-130">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="d74a8-130">WMI does not implement this class.</span></span>

<span data-ttu-id="d74a8-131">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="d74a8-131">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="d74a8-132">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="d74a8-132">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="d74a8-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d74a8-133">Requirements</span></span>



| <span data-ttu-id="d74a8-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="d74a8-134">Requirement</span></span> | <span data-ttu-id="d74a8-135">Valor</span><span class="sxs-lookup"><span data-stu-id="d74a8-135">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d74a8-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d74a8-136">Minimum supported client</span></span><br/> | <span data-ttu-id="d74a8-137">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d74a8-137">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="d74a8-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d74a8-138">Minimum supported server</span></span><br/> | <span data-ttu-id="d74a8-139">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d74a8-139">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="d74a8-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="d74a8-140">Namespace</span></span><br/>                | <span data-ttu-id="d74a8-141">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="d74a8-141">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="d74a8-142">MOF</span><span class="sxs-lookup"><span data-stu-id="d74a8-142">MOF</span></span><br/>                      | <dl> <span data-ttu-id="d74a8-143"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="d74a8-143"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="d74a8-144">DLL</span><span class="sxs-lookup"><span data-stu-id="d74a8-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d74a8-145"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d74a8-145"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d74a8-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="d74a8-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d74a8-147">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="d74a8-147">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

