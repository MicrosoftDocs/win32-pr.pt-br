---
description: Associa uma instância de máquina virtual ao serviço de gerenciamento que controla seu estado.
ms.assetid: 12EB3951-74D4-477F-8B55-69FAA3B14631
title: Classe Msvm_ServiceAffectsElement
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ServiceAffectsElement
- Msvm_ServiceAffectsElement.AffectedElement
- Msvm_ServiceAffectsElement.AffectingElement
- Msvm_ServiceAffectsElement.ElementEffects
- Msvm_ServiceAffectsElement.OtherElementEffectsDescriptions
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: eadb9f33015091999776b73c83d792ccd29396b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104090796"
---
# <a name="msvm_serviceaffectselement-class"></a><span data-ttu-id="43e26-103">Classe Msvm não \_ afetaelement</span><span class="sxs-lookup"><span data-stu-id="43e26-103">Msvm\_ServiceAffectsElement class</span></span>

<span data-ttu-id="43e26-104">Associa uma instância de máquina virtual ao serviço de gerenciamento que controla seu estado.</span><span class="sxs-lookup"><span data-stu-id="43e26-104">Associates a virtual machine instance with the management service that controls its state.</span></span>

<span data-ttu-id="43e26-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="43e26-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="43e26-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43e26-106">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ServiceAffectsElement : CIM_ServiceAffectsElement
{
  CIM_ManagedElement REF AffectedElement;
  CIM_Service        REF AffectingElement;
  uint16                 ElementEffects[] = 5;
  string                 OtherElementEffectsDescriptions[];
};
```

## <a name="members"></a><span data-ttu-id="43e26-107">Membros</span><span class="sxs-lookup"><span data-stu-id="43e26-107">Members</span></span>

<span data-ttu-id="43e26-108">A classe **Msvm não \_ afetaelement** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="43e26-108">The **Msvm\_ServiceAffectsElement** class has these types of members:</span></span>

-   [<span data-ttu-id="43e26-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43e26-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="43e26-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="43e26-110">Properties</span></span>

<span data-ttu-id="43e26-111">A classe **Msvm não \_ afetaelement** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="43e26-111">The **Msvm\_ServiceAffectsElement** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="43e26-112">**Afetadoselement**</span><span class="sxs-lookup"><span data-stu-id="43e26-112">**AffectedElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43e26-113">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="43e26-113">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="43e26-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43e26-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43e26-115">Uma referência à máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43e26-115">A reference to the virtual machine.</span></span> <span data-ttu-id="43e26-116">Essa propriedade é herdada de [**CIM \_ imafetaelement**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="43e26-116">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="43e26-117">**Afetando**</span><span class="sxs-lookup"><span data-stu-id="43e26-117">**AffectingElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43e26-118">Tipo de dados: **[ **\_ serviço CIM**](/windows/desktop/CIMWin32Prov/cim-service)**</span><span class="sxs-lookup"><span data-stu-id="43e26-118">Data type: **[**CIM\_Service**](/windows/desktop/CIMWin32Prov/cim-service)**</span></span>
</dt> <dt>

<span data-ttu-id="43e26-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43e26-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43e26-120">Uma referência ao serviço que controla a máquina virtual.</span><span class="sxs-lookup"><span data-stu-id="43e26-120">A reference to the service that controls the virtual machine.</span></span> <span data-ttu-id="43e26-121">Essa propriedade é herdada de [**CIM \_ imafetaelement**](/previous-versions//cc136907(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="43e26-121">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="43e26-122">**ElementEffects**</span><span class="sxs-lookup"><span data-stu-id="43e26-122">**ElementEffects**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43e26-123">Tipo de dados: a matriz **UInt16**</span><span class="sxs-lookup"><span data-stu-id="43e26-123">Data type: **uint16** array</span></span>
</dt> <dt>

<span data-ttu-id="43e26-124">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43e26-124">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43e26-125">Especifica o tipo de controle que a associação representa.</span><span class="sxs-lookup"><span data-stu-id="43e26-125">Specifies the type of control that the association represents.</span></span> <span data-ttu-id="43e26-126">Essa propriedade é herdada de [**CIM \_ imafetaelement**](/previous-versions//cc136907(v=vs.85))e é sempre definida como o valor a seguir.</span><span class="sxs-lookup"><span data-stu-id="43e26-126">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to the following value.</span></span>



| <span data-ttu-id="43e26-127">Valor</span><span class="sxs-lookup"><span data-stu-id="43e26-127">Value</span></span>                                                                        | <span data-ttu-id="43e26-128">Significado</span><span class="sxs-lookup"><span data-stu-id="43e26-128">Meaning</span></span>            |
|------------------------------------------------------------------------------|--------------------|
| <dl> <span data-ttu-id="43e26-129"><dt>5</dt></span><span class="sxs-lookup"><span data-stu-id="43e26-129"><dt>5</dt></span></span> </dl> | <span data-ttu-id="43e26-130">Gerencia</span><span class="sxs-lookup"><span data-stu-id="43e26-130">Manages</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="43e26-131">**OtherElementEffectsDescriptions**</span><span class="sxs-lookup"><span data-stu-id="43e26-131">**OtherElementEffectsDescriptions**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="43e26-132">Tipo de dados: matriz de **cadeia de caracteres**</span><span class="sxs-lookup"><span data-stu-id="43e26-132">Data type: **string** array</span></span>
</dt> <dt>

<span data-ttu-id="43e26-133">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="43e26-133">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="43e26-134">Os detalhes do tipo de associação na posição da matriz correspondente na matriz da propriedade **ElementAffects** .</span><span class="sxs-lookup"><span data-stu-id="43e26-134">The details for the type of association at the corresponding array position in the **ElementAffects** property array.</span></span> <span data-ttu-id="43e26-135">Essas informações serão necessárias se **ElementAffects** estiver definido como 1 (outro).</span><span class="sxs-lookup"><span data-stu-id="43e26-135">This information is required if **ElementAffects** is set to 1 (Other).</span></span> <span data-ttu-id="43e26-136">Essa propriedade é herdada de [**CIM \_ imafetaelement**](/previous-versions//cc136907(v=vs.85))e é sempre definida como **nula**.</span><span class="sxs-lookup"><span data-stu-id="43e26-136">This property is inherited from [**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85)), and it is always set to **Null**.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="43e26-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="43e26-137">Remarks</span></span>

<span data-ttu-id="43e26-138">O acesso à classe **Msvm de \_ paraafetaelement** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="43e26-138">Access to the **Msvm\_ServiceAffectsElement** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="43e26-139">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="43e26-139">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="43e26-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43e26-140">Requirements</span></span>



| <span data-ttu-id="43e26-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="43e26-141">Requirement</span></span> | <span data-ttu-id="43e26-142">Valor</span><span class="sxs-lookup"><span data-stu-id="43e26-142">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43e26-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43e26-143">Minimum supported client</span></span><br/> | <span data-ttu-id="43e26-144">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="43e26-144">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="43e26-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="43e26-145">Minimum supported server</span></span><br/> | <span data-ttu-id="43e26-146">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="43e26-146">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="43e26-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="43e26-147">Namespace</span></span><br/>                | <span data-ttu-id="43e26-148">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="43e26-148">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="43e26-149">MOF</span><span class="sxs-lookup"><span data-stu-id="43e26-149">MOF</span></span><br/>                      | <dl> <span data-ttu-id="43e26-150"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="43e26-150"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="43e26-151">DLL</span><span class="sxs-lookup"><span data-stu-id="43e26-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="43e26-152"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="43e26-152"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="43e26-153">Confira também</span><span class="sxs-lookup"><span data-stu-id="43e26-153">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43e26-154">**CIM \_ Imafetaelement**</span><span class="sxs-lookup"><span data-stu-id="43e26-154">**CIM\_ServiceAffectsElement**</span></span>](cim-serviceaffectselement.md)
</dt> <dt>

<span data-ttu-id="43e26-155">[**CIM \_ Imafetaelement**](/previous-versions//cc136907(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="43e26-155">[**CIM\_ServiceAffectsElement**](/previous-versions//cc136907(v=vs.85))</span></span>
</dt> </dl>

 

