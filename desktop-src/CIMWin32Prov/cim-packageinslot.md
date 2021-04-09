---
description: A \_ associação CIM PackageInSlot representa a relação entre os cartões de dispositivo e o chassi no qual eles são montados.
ms.assetid: 439f28a8-24fd-4a53-9d42-48fabb58e84a
ms.tgt_platform: multiple
title: Classe CIM_PackageInSlot
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_PackageInSlot
- CIM_PackageInSlot.Dependent
- CIM_PackageInSlot.Antecedent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: a17e133f16f838d6353b6d74ee2054bd5ec52cd0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104088985"
---
# <a name="cim_packageinslot-class"></a><span data-ttu-id="c9eec-103">\_Classe CIM PackageInSlot</span><span class="sxs-lookup"><span data-stu-id="c9eec-103">CIM\_PackageInSlot class</span></span>

<span data-ttu-id="c9eec-104">A associação **CIM \_ PackageInSlot** representa a relação entre os cartões de dispositivo e o chassi no qual eles são montados.</span><span class="sxs-lookup"><span data-stu-id="c9eec-104">The **CIM\_PackageInSlot** association represents the relationship between device cards and the chassis in which they are mounted.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c9eec-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="c9eec-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="c9eec-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="c9eec-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="c9eec-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="c9eec-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="c9eec-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="c9eec-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="c9eec-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c9eec-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{FAF76B89-798C-11D2-AAD1-006008C78BC7}"), AMENDMENT]
class CIM_PackageInSlot : CIM_Dependency
{
  CIM_PhysicalPackage REF Dependent;
  CIM_Slot            REF Antecedent;
};
```

## <a name="members"></a><span data-ttu-id="c9eec-110">Membros</span><span class="sxs-lookup"><span data-stu-id="c9eec-110">Members</span></span>

<span data-ttu-id="c9eec-111">A classe **CIM \_ PackageInSlot** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="c9eec-111">The **CIM\_PackageInSlot** class has these types of members:</span></span>

-   [<span data-ttu-id="c9eec-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9eec-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="c9eec-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="c9eec-113">Properties</span></span>

<span data-ttu-id="c9eec-114">A classe **CIM \_ PackageInSlot** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="c9eec-114">The **CIM\_PackageInSlot** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="c9eec-115">**Antecedent**</span><span class="sxs-lookup"><span data-stu-id="c9eec-115">**Antecedent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9eec-116">Tipo de dados **: \_ slot CIM**</span><span class="sxs-lookup"><span data-stu-id="c9eec-116">Data type: **CIM\_Slot**</span></span>
</dt> <dt>

<span data-ttu-id="c9eec-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9eec-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9eec-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span><span class="sxs-lookup"><span data-stu-id="c9eec-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Antecedent")</span></span>
</dt> </dl>

<span data-ttu-id="c9eec-119">Um [**\_ slot CIM**](cim-slot.md) que descreve o slot no qual o pacote físico é inserido.</span><span class="sxs-lookup"><span data-stu-id="c9eec-119">A [**CIM\_Slot**](cim-slot.md) describing the slot into which the physical package is inserted.</span></span>

</dd> <dt>

<span data-ttu-id="c9eec-120">**Depende**</span><span class="sxs-lookup"><span data-stu-id="c9eec-120">**Dependent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="c9eec-121">Tipo de dados: **CIM \_ PhysicalPackage**</span><span class="sxs-lookup"><span data-stu-id="c9eec-121">Data type: **CIM\_PhysicalPackage**</span></span>
</dt> <dt>

<span data-ttu-id="c9eec-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="c9eec-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="c9eec-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("dependente"), [**máx**](/windows/desktop/WmiSdk/standard-qualifiers) . (1)</span><span class="sxs-lookup"><span data-stu-id="c9eec-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("Dependent"), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1)</span></span>
</dt> </dl>

<span data-ttu-id="c9eec-124">Um [**\_ PhysicalPackage CIM**](cim-physicalpackage.md) que descreve o pacote no slot.</span><span class="sxs-lookup"><span data-stu-id="c9eec-124">A [**CIM\_PhysicalPackage**](cim-physicalpackage.md) describing the package in the slot.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="c9eec-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="c9eec-125">Remarks</span></span>

<span data-ttu-id="c9eec-126">**CIM \_ PackageInSlot** é derivado da [**\_ dependência CIM**](cim-dependency.md).</span><span class="sxs-lookup"><span data-stu-id="c9eec-126">**CIM\_PackageInSlot** is derived from [**CIM\_Dependency**](cim-dependency.md).</span></span>

<span data-ttu-id="c9eec-127">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="c9eec-127">WMI does not implement this class.</span></span>

<span data-ttu-id="c9eec-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="c9eec-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="c9eec-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="c9eec-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="c9eec-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c9eec-130">Requirements</span></span>



| <span data-ttu-id="c9eec-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="c9eec-131">Requirement</span></span> | <span data-ttu-id="c9eec-132">Valor</span><span class="sxs-lookup"><span data-stu-id="c9eec-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c9eec-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9eec-133">Minimum supported client</span></span><br/> | <span data-ttu-id="c9eec-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="c9eec-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="c9eec-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c9eec-135">Minimum supported server</span></span><br/> | <span data-ttu-id="c9eec-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="c9eec-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="c9eec-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9eec-137">Namespace</span></span><br/>                | <span data-ttu-id="c9eec-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="c9eec-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="c9eec-139">MOF</span><span class="sxs-lookup"><span data-stu-id="c9eec-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="c9eec-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="c9eec-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="c9eec-141">DLL</span><span class="sxs-lookup"><span data-stu-id="c9eec-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c9eec-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c9eec-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c9eec-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="c9eec-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c9eec-144">**\_Dependência CIM**</span><span class="sxs-lookup"><span data-stu-id="c9eec-144">**CIM\_Dependency**</span></span>](cim-dependency.md)
</dt> </dl>

 

