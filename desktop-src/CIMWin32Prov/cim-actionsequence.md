---
description: A \_ associação CIM ActionSequence define uma série de operações que fazem a transição do elemento software (referenciado pela \_ Associação SOFTWAREELEMENTACTIONS do CIM) para seu próximo estado ou remove o elemento software de seu estado atual.
ms.assetid: b539c424-bc2a-414b-b56c-72550004720f
ms.tgt_platform: multiple
title: Classe CIM_ActionSequence
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_ActionSequence
- CIM_ActionSequence.Next
- CIM_ActionSequence.Prior
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 71150d1ad9785d81579d8f305fe46bc6b7e57d00
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105755876"
---
# <a name="cim_actionsequence-class"></a><span data-ttu-id="cba43-103">\_Classe CIM ActionSequence</span><span class="sxs-lookup"><span data-stu-id="cba43-103">CIM\_ActionSequence class</span></span>

<span data-ttu-id="cba43-104">A associação **CIM \_ ActionSequence** define uma série de operações que fazem a transição do elemento software (referenciado pela Associação [**\_ SoftwareElementActions do CIM**](cim-softwareelementactions.md) ) para seu próximo estado ou remove o elemento software de seu estado atual.</span><span class="sxs-lookup"><span data-stu-id="cba43-104">The **CIM\_ActionSequence** association defines a series of operations that transition the software element (referenced by the [**CIM\_SoftwareElementActions**](cim-softwareelementactions.md) association) to its next state, or removes the software element from its current state.</span></span>

<span data-ttu-id="cba43-105">As ações de estado seguinte e as ações de desinstalação associadas a um elemento de software específico devem ser uma sequência contínua.</span><span class="sxs-lookup"><span data-stu-id="cba43-105">The next-state actions and uninstall actions associated with a particular software element must be a continuous sequence.</span></span> <span data-ttu-id="cba43-106">Como o **CIM \_ ActionSequence** é uma associação, o loops na classe de [**\_ ação CIM**](cim-action.md) , com funções para a ação "anterior" e a ação "Avançar", formam uma sequência.</span><span class="sxs-lookup"><span data-stu-id="cba43-106">Since **CIM\_ActionSequence** is an association, the loops on the [**CIM\_Action**](cim-action.md) class, with roles for the "prior" action and "next" action, form a sequence.</span></span>

<span data-ttu-id="cba43-107">A necessidade de uma sequência contínua implica:</span><span class="sxs-lookup"><span data-stu-id="cba43-107">The need for a continuous sequence implies:</span></span>

-   <span data-ttu-id="cba43-108">Dentro do conjunto de ações de próximo estado ou de desinstalação, há apenas uma ação que não tem uma instância da Associação **\_ ActionSequence do CIM** que a referencia na função "Next".</span><span class="sxs-lookup"><span data-stu-id="cba43-108">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "next" role.</span></span> <span data-ttu-id="cba43-109">Essa é a primeira ação na sequência.</span><span class="sxs-lookup"><span data-stu-id="cba43-109">This is the first action in the sequence.</span></span>
-   <span data-ttu-id="cba43-110">Dentro do conjunto de ações de próximo estado ou de desinstalação, há apenas uma ação que não tem uma instância da Associação **\_ ActionSequence do CIM** fazendo referência a ela na função "anterior".</span><span class="sxs-lookup"><span data-stu-id="cba43-110">Within the set of next-state or uninstall actions, there is only one action that does not have an instance of the **CIM\_ActionSequence** association referencing it in the "prior" role.</span></span> <span data-ttu-id="cba43-111">Esta é a última ação na sequência.</span><span class="sxs-lookup"><span data-stu-id="cba43-111">This is the last action in the sequence.</span></span>
-   <span data-ttu-id="cba43-112">Todas as outras ações dentro do conjunto de ações de próximo estado e desinstalação devem participar de duas instâncias da Associação de **\_ ActionSequence do CIM** , uma em uma função "anterior" e outra na função "Next".</span><span class="sxs-lookup"><span data-stu-id="cba43-112">All other actions within the set of next-state and uninstall actions must participate in two instances of the **CIM\_ActionSequence** association, one in a "prior" role and one in the "next" role.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cba43-113">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="cba43-113">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="cba43-114">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="cba43-114">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="cba43-115">A sintaxe a seguir é simplificada do código MOF (Managed Object Format) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="cba43-115">The following syntax is simplified from Managed Object Format (MOF) code and includes all inherited properties.</span></span> <span data-ttu-id="cba43-116">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="cba43-116">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="cba43-117">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cba43-117">Syntax</span></span>

``` syntax
[Abstract, Association, UUID("{F127E50E-E3E0-11d2-8601-0000F8102E5F}"), AMENDMENT]
class CIM_ActionSequence
{
  CIM_Action REF Next;
  CIM_Action REF Prior;
};
```

## <a name="members"></a><span data-ttu-id="cba43-118">Membros</span><span class="sxs-lookup"><span data-stu-id="cba43-118">Members</span></span>

<span data-ttu-id="cba43-119">A classe **CIM \_ ActionSequence** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="cba43-119">The **CIM\_ActionSequence** class has these types of members:</span></span>

-   [<span data-ttu-id="cba43-120">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cba43-120">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="cba43-121">Propriedades</span><span class="sxs-lookup"><span data-stu-id="cba43-121">Properties</span></span>

<span data-ttu-id="cba43-122">A classe **CIM \_ ActionSequence** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="cba43-122">The **CIM\_ActionSequence** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="cba43-123">**Próximo**</span><span class="sxs-lookup"><span data-stu-id="cba43-123">**Next**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cba43-124">Tipo de dados **: \_ ação CIM**</span><span class="sxs-lookup"><span data-stu-id="cba43-124">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="cba43-125">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cba43-125">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cba43-126">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="cba43-126">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="cba43-127">Referência à próxima ação.</span><span class="sxs-lookup"><span data-stu-id="cba43-127">Reference to the next action.</span></span>

</dd> <dt>

<span data-ttu-id="cba43-128">**Prior**</span><span class="sxs-lookup"><span data-stu-id="cba43-128">**Prior**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="cba43-129">Tipo de dados **: \_ ação CIM**</span><span class="sxs-lookup"><span data-stu-id="cba43-129">Data type: **CIM\_Action**</span></span>
</dt> <dt>

<span data-ttu-id="cba43-130">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="cba43-130">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="cba43-131">Qualificadores: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span><span class="sxs-lookup"><span data-stu-id="cba43-131">Qualifiers: [**Max**](/windows/desktop/WmiSdk/standard-qualifiers) (1), [**Min**](/windows/desktop/WmiSdk/standard-qualifiers) (0)</span></span>
</dt> </dl>

<span data-ttu-id="cba43-132">Referência à ação anterior.</span><span class="sxs-lookup"><span data-stu-id="cba43-132">Reference to the prior action.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="cba43-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="cba43-133">Remarks</span></span>

<span data-ttu-id="cba43-134">As classes de [**\_ ação CIM**](cim-action.md) que participam dessa associação devem ter o mesmo valor para a propriedade **Direction** .</span><span class="sxs-lookup"><span data-stu-id="cba43-134">The [**CIM\_Action**](cim-action.md) classes participating in this association must have the same value for the **Direction** property.</span></span>

<span data-ttu-id="cba43-135">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="cba43-135">WMI does not implement this class.</span></span>

<span data-ttu-id="cba43-136">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="cba43-136">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="cba43-137">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="cba43-137">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="cba43-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cba43-138">Requirements</span></span>



| <span data-ttu-id="cba43-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="cba43-139">Requirement</span></span> | <span data-ttu-id="cba43-140">Valor</span><span class="sxs-lookup"><span data-stu-id="cba43-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="cba43-141">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cba43-141">Minimum supported client</span></span><br/> | <span data-ttu-id="cba43-142">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="cba43-142">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="cba43-143">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cba43-143">Minimum supported server</span></span><br/> | <span data-ttu-id="cba43-144">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="cba43-144">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="cba43-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="cba43-145">Namespace</span></span><br/>                | <span data-ttu-id="cba43-146">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="cba43-146">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="cba43-147">MOF</span><span class="sxs-lookup"><span data-stu-id="cba43-147">MOF</span></span><br/>                      | <dl> <span data-ttu-id="cba43-148"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="cba43-148"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="cba43-149">DLL</span><span class="sxs-lookup"><span data-stu-id="cba43-149">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cba43-150"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cba43-150"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cba43-151">Confira também</span><span class="sxs-lookup"><span data-stu-id="cba43-151">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cba43-152">Classes CIM</span><span class="sxs-lookup"><span data-stu-id="cba43-152">CIM Classes</span></span>](/windows/desktop/WmiSdk/cimclas)
</dt> </dl>

 

