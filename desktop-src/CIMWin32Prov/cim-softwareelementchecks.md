---
description: A \_ classe de associação CIM SoftwareElementChecks relaciona um elemento de software com informações de condição ou local que um recurso pode exigir.
ms.assetid: ff130fe9-ddb2-4e4f-86d3-53f1d8ed14aa
ms.tgt_platform: multiple
title: Classe CIM_SoftwareElementChecks
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SoftwareElementChecks
- CIM_SoftwareElementChecks.Check
- CIM_SoftwareElementChecks.Element
- CIM_SoftwareElementChecks.Phase
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: ea6fcb02794174e825994f70270745741c9b7713
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826250"
---
# <a name="cim_softwareelementchecks-class"></a><span data-ttu-id="e1290-103">\_Classe CIM SoftwareElementChecks</span><span class="sxs-lookup"><span data-stu-id="e1290-103">CIM\_SoftwareElementChecks class</span></span>

<span data-ttu-id="e1290-104">A classe de associação **CIM \_ SoftwareElementChecks** relaciona um elemento de software com informações de condição ou local que um recurso pode exigir.</span><span class="sxs-lookup"><span data-stu-id="e1290-104">The **CIM\_SoftwareElementChecks** association class relates a software element with condition or location information that a feature may require.</span></span>

<span data-ttu-id="e1290-105">Como os elementos de software em um estado pronto para execução não podem fazer a transição para outro Estado, o valor da propriedade **Phase** é restrito a estado de objetos [**CIM \_ softwareelement**](cim-softwareelement.md) em um estado pronto para execução.</span><span class="sxs-lookup"><span data-stu-id="e1290-105">Because software elements in a ready-to-run state cannot transition into another state, the value of the **Phase** property is restricted to in-state for [**CIM\_SoftwareElement**](cim-softwareelement.md) objects in a ready-to-run state.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e1290-106">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="e1290-106">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="e1290-107">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="e1290-107">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="e1290-108">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="e1290-108">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="e1290-109">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="e1290-109">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1290-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1290-110">Syntax</span></span>

``` syntax
[UUID("{24783E8A-DB31-11d2-85FC-0000F8102E5F}"), Association, Aggregation, Abstract, AMENDMENT]
class CIM_SoftwareElementChecks
{
  CIM_Check           REF Check;
  CIM_SoftwareElement REF Element;
  uint16                  Phase;
};
```

## <a name="members"></a><span data-ttu-id="e1290-111">Membros</span><span class="sxs-lookup"><span data-stu-id="e1290-111">Members</span></span>

<span data-ttu-id="e1290-112">A classe **CIM \_ SoftwareElementChecks** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="e1290-112">The **CIM\_SoftwareElementChecks** class has these types of members:</span></span>

-   [<span data-ttu-id="e1290-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1290-113">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="e1290-114">Propriedades</span><span class="sxs-lookup"><span data-stu-id="e1290-114">Properties</span></span>

<span data-ttu-id="e1290-115">A classe **CIM \_ SoftwareElementChecks** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="e1290-115">The **CIM\_SoftwareElementChecks** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="e1290-116">**Verificação**</span><span class="sxs-lookup"><span data-stu-id="e1290-116">**Check**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1290-117">Tipo de dados **: \_ verificação de CIM**</span><span class="sxs-lookup"><span data-stu-id="e1290-117">Data type: **CIM\_Check**</span></span>
</dt> <dt>

<span data-ttu-id="e1290-118">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1290-118">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1290-119">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (false), [**fraco**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e1290-119">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (FALSE), [**Weak**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e1290-120">Referência à verificação.</span><span class="sxs-lookup"><span data-stu-id="e1290-120">Reference to the check.</span></span>

</dd> <dt>

<span data-ttu-id="e1290-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="e1290-121">**Element**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1290-122">Tipo de dados: **CIM \_ softwareelement**</span><span class="sxs-lookup"><span data-stu-id="e1290-122">Data type: **CIM\_SoftwareElement**</span></span>
</dt> <dt>

<span data-ttu-id="e1290-123">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1290-123">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="e1290-124">Qualificadores: [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span><span class="sxs-lookup"><span data-stu-id="e1290-124">Qualifiers: [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Aggregate**](/windows/desktop/WmiSdk/standard-qualifiers)</span></span>
</dt> </dl>

<span data-ttu-id="e1290-125">Referência ao elemento.</span><span class="sxs-lookup"><span data-stu-id="e1290-125">Reference to the element.</span></span>

</dd> <dt>

<span data-ttu-id="e1290-126">**Fase**</span><span class="sxs-lookup"><span data-stu-id="e1290-126">**Phase**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="e1290-127">Tipo de dados: **UInt16**</span><span class="sxs-lookup"><span data-stu-id="e1290-127">Data type: **uint16**</span></span>
</dt> <dt>

<span data-ttu-id="e1290-128">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="e1290-128">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="e1290-129">Indica se a verificação referenciada é uma verificação no estado ou uma verificação de estado seguinte.</span><span class="sxs-lookup"><span data-stu-id="e1290-129">Indicates whether the referenced check is an in-state check or a next-state check.</span></span>

<dt>

<span id="In-State"></span><span id="in-state"></span><span id="IN-STATE"></span>

<span data-ttu-id="e1290-130">**Em estado** (0)</span><span class="sxs-lookup"><span data-stu-id="e1290-130">**In-State** (0)</span></span>


</dt> <dd></dd> <dt>

<span id="Next-State"></span><span id="next-state"></span><span id="NEXT-STATE"></span>

<span data-ttu-id="e1290-131">**Próximo estado** (1)</span><span class="sxs-lookup"><span data-stu-id="e1290-131">**Next-State** (1)</span></span>


<span data-ttu-id="e1290-132"></dt> <dd></dd> </dl>

</dd> </dl></span><span class="sxs-lookup"><span data-stu-id="e1290-132"></dt> <dd></dd> </dl>

</dd> </dl></span></span>

## <a name="remarks"></a><span data-ttu-id="e1290-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1290-133">Remarks</span></span>

<span data-ttu-id="e1290-134">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="e1290-134">WMI does not implement this class.</span></span> <span data-ttu-id="e1290-135">Para classes WMI derivadas do **CIM \_ SoftwareElementChecks**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="e1290-135">For WMI classes derived from **CIM\_SoftwareElementChecks**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="e1290-136">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="e1290-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="e1290-137">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="e1290-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1290-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1290-138">Requirements</span></span>



| <span data-ttu-id="e1290-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1290-139">Requirement</span></span> | <span data-ttu-id="e1290-140">Valor</span><span class="sxs-lookup"><span data-stu-id="e1290-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="e1290-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1290-141">Minimum supported client</span></span><br/> | <span data-ttu-id="e1290-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="e1290-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="e1290-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e1290-143">Minimum supported server</span></span><br/> | <span data-ttu-id="e1290-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="e1290-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="e1290-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="e1290-145">Namespace</span></span><br/>                | <span data-ttu-id="e1290-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="e1290-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="e1290-147">MOF</span><span class="sxs-lookup"><span data-stu-id="e1290-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="e1290-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="e1290-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="e1290-149">DLL</span><span class="sxs-lookup"><span data-stu-id="e1290-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e1290-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e1290-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



 

