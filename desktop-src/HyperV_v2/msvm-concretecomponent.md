---
description: Uma associação genérica usada para estabelecer parte de relações entre elementos gerenciados.
ms.assetid: 4D237D68-0A63-4A19-B6AD-E3C781090994
title: Classe Msvm_ConcreteComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_ConcreteComponent
- Msvm_ConcreteComponent.GroupComponent
- Msvm_ConcreteComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 2ef9e286f4c7ca296ee6b3638ffb9511ccea4115
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105754670"
---
# <a name="msvm_concretecomponent-class"></a><span data-ttu-id="7efab-103">\_Classe Msvm ConcreteComponent</span><span class="sxs-lookup"><span data-stu-id="7efab-103">Msvm\_ConcreteComponent class</span></span>

<span data-ttu-id="7efab-104">Uma associação genérica usada para estabelecer a "parte de" relações entre elementos gerenciados.</span><span class="sxs-lookup"><span data-stu-id="7efab-104">A generic association used to establish 'part of' relationships between managed elements.</span></span> <span data-ttu-id="7efab-105">[**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) é definido como uma subclasse concreta da classe abstrata de [**\_ componente CIM**](/windows/desktop/CIMWin32Prov/cim-component) , a ser usada em vez de muitas subclasses específicas de componente que não adicionam nenhuma semântica (ou seja, as subclasses que não esclarecem o tipo de composição, atualizam cardinalidade ou adicionam ou removem qualificadores.)</span><span class="sxs-lookup"><span data-stu-id="7efab-105">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)) is defined as a concrete subclass of the abstract [**CIM\_Component**](/windows/desktop/CIMWin32Prov/cim-component) class, to be used in place of many specific subclasses of component that add no semantics (that is subclasses that do not clarify the type of composition, update cardinalities, or add or remove qualifiers.)</span></span>

<span data-ttu-id="7efab-106">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="7efab-106">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="7efab-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7efab-107">Syntax</span></span>

``` syntax
[Association, Aggregation, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_ConcreteComponent : CIM_ConcreteComponent
{
  CIM_ManagedElement REF GroupComponent;
  CIM_ManagedElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="7efab-108">Membros</span><span class="sxs-lookup"><span data-stu-id="7efab-108">Members</span></span>

<span data-ttu-id="7efab-109">A classe **Msvm \_ ConcreteComponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="7efab-109">The **Msvm\_ConcreteComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="7efab-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7efab-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="7efab-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="7efab-111">Properties</span></span>

<span data-ttu-id="7efab-112">A classe **Msvm \_ ConcreteComponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="7efab-112">The **Msvm\_ConcreteComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="7efab-113">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="7efab-113">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efab-114">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="7efab-114">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="7efab-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7efab-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7efab-116">O elemento pai na associação.</span><span class="sxs-lookup"><span data-stu-id="7efab-116">The parent element in the association.</span></span> <span data-ttu-id="7efab-117">Essa propriedade é herdada do [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7efab-117">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> <dt>

<span data-ttu-id="7efab-118">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="7efab-118">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="7efab-119">Tipo de dados: **[ **CIM \_ managedelement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span><span class="sxs-lookup"><span data-stu-id="7efab-119">Data type: **[**CIM\_ManagedElement**](/previous-versions/windows/desktop/iscsitarg/cim-managedelement)**</span></span>
</dt> <dt>

<span data-ttu-id="7efab-120">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="7efab-120">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="7efab-121">O elemento filho na associação.</span><span class="sxs-lookup"><span data-stu-id="7efab-121">The child element in the association.</span></span> <span data-ttu-id="7efab-122">Essa propriedade é herdada do [**CIM \_ ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span><span class="sxs-lookup"><span data-stu-id="7efab-122">This property is inherited from [**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85)).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="7efab-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="7efab-123">Remarks</span></span>

<span data-ttu-id="7efab-124">O acesso à classe **Msvm \_ ConcreteComponent** pode ser restringido pela filtragem do UAC.</span><span class="sxs-lookup"><span data-stu-id="7efab-124">Access to the **Msvm\_ConcreteComponent** class might be restricted by UAC Filtering.</span></span> <span data-ttu-id="7efab-125">Para obter mais informações, consulte [controle de conta de usuário e WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span><span class="sxs-lookup"><span data-stu-id="7efab-125">For more information, see [User Account Control and WMI](/windows/desktop/WmiSdk/user-account-control-and-wmi).</span></span>

## <a name="requirements"></a><span data-ttu-id="7efab-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7efab-126">Requirements</span></span>



| <span data-ttu-id="7efab-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7efab-127">Requirement</span></span> | <span data-ttu-id="7efab-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7efab-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7efab-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7efab-129">Minimum supported client</span></span><br/> | <span data-ttu-id="7efab-130">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="7efab-130">Windows 8 \[desktop apps only\]</span></span><br/>                                                              |
| <span data-ttu-id="7efab-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7efab-131">Minimum supported server</span></span><br/> | <span data-ttu-id="7efab-132">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="7efab-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                    |
| <span data-ttu-id="7efab-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="7efab-133">Namespace</span></span><br/>                | <span data-ttu-id="7efab-134">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="7efab-134">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="7efab-135">MOF</span><span class="sxs-lookup"><span data-stu-id="7efab-135">MOF</span></span><br/>                      | <dl> <span data-ttu-id="7efab-136"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="7efab-136"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="7efab-137">DLL</span><span class="sxs-lookup"><span data-stu-id="7efab-137">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7efab-138"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="7efab-138"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="7efab-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="7efab-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7efab-140">**\_CONCRETECOMPONENT CIM**</span><span class="sxs-lookup"><span data-stu-id="7efab-140">**CIM\_ConcreteComponent**</span></span>](cim-concretecomponent.md)
</dt> <dt>

<span data-ttu-id="7efab-141">[**\_CONCRETECOMPONENT CIM**](/previous-versions//cc150665(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="7efab-141">[**CIM\_ConcreteComponent**](/previous-versions//cc150665(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="7efab-142">Classes de sistema virtual</span><span class="sxs-lookup"><span data-stu-id="7efab-142">Virtual System Classes</span></span>](virtual-system-classes.md)
</dt> </dl>

 

