---
description: Representa uma associação entre um trabalho e o elemento gerenciado que pode ser afetado pela sua execução.
ms.assetid: 125A4976-A4E3-4D7A-A43B-86045C3B00AE
title: Classe Msvm_AffectedJobElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_AffectedJobElement
- Msvm_AffectedJobElement.AffectedElement
- Msvm_AffectedJobElement.AffectingElement
- Msvm_AffectedJobElement.ElementEffects
- Msvm_AffectedJobElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: bef667872a7afa4c726ee1b2c77a36c29649114d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105767643"
---
# <a name="msvm_affectedjobelement-class"></a><span data-ttu-id="f2642-103">\_Classe Msvm AffectedJobElement</span><span class="sxs-lookup"><span data-stu-id="f2642-103">Msvm\_AffectedJobElement class</span></span>

<span data-ttu-id="f2642-104">Representa uma associação entre um trabalho e o elemento gerenciado que pode ser afetado pela sua execução.</span><span class="sxs-lookup"><span data-stu-id="f2642-104">Represents an association between a job and the managed element that may be affected by its execution.</span></span>

<span data-ttu-id="f2642-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f2642-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f2642-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f2642-106">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_AffectedJobElement : CIM_AffectedJobElement
{
  CIM_ManagedElement REF AffectedElement;
  Msvm_ConcreteJob   REF AffectingElement;
  uint16                 ElementEffects[];
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="f2642-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f2642-107">Members</span></span>

<span data-ttu-id="f2642-108">A classe **Msvm \_ AffectedJobElement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f2642-108">The **Msvm\_AffectedJobElement** class has these types of members:</span></span>

-   [<span data-ttu-id="f2642-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f2642-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f2642-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f2642-110">Properties</span></span>

<span data-ttu-id="f2642-111">A classe **Msvm \_ AffectedJobElement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f2642-111">The **Msvm\_AffectedJobElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f2642-112">**Afetadoselement**</span><span class="sxs-lookup"><span data-stu-id="f2642-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2642-113">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="f2642-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="f2642-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2642-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2642-115">O elemento gerenciado afetado pela execução do trabalho.</span><span class="sxs-lookup"><span data-stu-id="f2642-115">The managed element affected by the execution of the job.</span></span> <span data-ttu-id="f2642-116">Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f2642-116">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f2642-117">**Afetando**</span><span class="sxs-lookup"><span data-stu-id="f2642-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2642-118">Tipo de dados: **[ **Msvm \_ ConcreteJob**](msvm-concretejob.md)**</span><span class="sxs-lookup"><span data-stu-id="f2642-118">Data type: **[**Msvm\_ConcreteJob**](msvm-concretejob.md)**</span></span>
</dt> <dt>

<span data-ttu-id="f2642-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2642-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2642-120">O trabalho que está afetando o elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2642-120">The job that is affecting the managed element.</span></span> <span data-ttu-id="f2642-121">Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f2642-121">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f2642-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="f2642-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2642-123">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="f2642-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="f2642-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2642-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2642-125">Uma enumeração que descreve o efeito sobre o elemento gerenciado.</span><span class="sxs-lookup"><span data-stu-id="f2642-125">An enumeration that describes the effect on the managed element.</span></span> <span data-ttu-id="f2642-126">Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f2642-126">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="f2642-127">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="f2642-127">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f2642-128">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="f2642-128">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="f2642-129">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f2642-129">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f2642-130">Fornece detalhes para o efeito na posição da matriz correspondente em **ElementEffects**.</span><span class="sxs-lookup"><span data-stu-id="f2642-130">Provides details for the effect at the corresponding array position in **ElementEffects**.</span></span> <span data-ttu-id="f2642-131">Essa propriedade é herdada do [**CIM \_ AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="f2642-131">This property is inherited from [**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f2642-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="f2642-132">Remarks</span></span>

<span data-ttu-id="f2642-133">O acesso à classe **Msvm \_ AffectedJobElement** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="f2642-133">Access to the **Msvm\_AffectedJobElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="f2642-134">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="f2642-134">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="f2642-135">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f2642-135">Requirements</span></span>



| <span data-ttu-id="f2642-136">Requisito</span><span class="sxs-lookup"><span data-stu-id="f2642-136">Requirement</span></span> | <span data-ttu-id="f2642-137">Valor</span><span class="sxs-lookup"><span data-stu-id="f2642-137">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f2642-138">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2642-138">Minimum supported client</span></span><br/> | <span data-ttu-id="f2642-139">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="f2642-139">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="f2642-140">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f2642-140">Minimum supported server</span></span><br/> | <span data-ttu-id="f2642-141">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="f2642-141">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="f2642-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2642-142">Namespace</span></span><br/>                | <span data-ttu-id="f2642-143">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f2642-143">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f2642-144">MOF</span><span class="sxs-lookup"><span data-stu-id="f2642-144">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f2642-145"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f2642-145"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f2642-146">DLL</span><span class="sxs-lookup"><span data-stu-id="f2642-146">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f2642-147"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f2642-147"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="f2642-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="f2642-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f2642-149">**\_AFFECTEDJOBELEMENT CIM**</span><span class="sxs-lookup"><span data-stu-id="f2642-149">**CIM\_AffectedJobElement**</span></span>](cim-affectedjobelement.md)
</dt> <dt>

<span data-ttu-id="f2642-150">[**\_AFFECTEDJOBELEMENT CIM**](/previous-versions//cc150663(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="f2642-150">[**CIM\_AffectedJobElement**](/previous-versions//cc150663(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="f2642-151">Classes de gerenciamento do sistema virtual</span><span class="sxs-lookup"><span data-stu-id="f2642-151">Virtual System Management Classes</span></span>](virtual-system-management-classes.md)
</dt> </dl>

 

