---
description: Uma classe de associação de modelo CIM (CIM) que estabelece relações entre um sistema e os elementos do sistema gerenciado dos quais ele é composto.
ms.assetid: 11ad6dc1-a09a-4bab-bb1d-2131a8fdb812
ms.tgt_platform: multiple
title: Classe CIM_SystemComponent (provedores WMI CIMWin32)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CIM_SystemComponent
- CIM_SystemComponent.PartComponent
- CIM_SystemComponent.GroupComponent
api_type:
- DllExport
api_location:
- CIMWin32.dll
ms.openlocfilehash: 9d9aae4e4ef916916f54bddea814844f23ed7315
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089347"
---
# <a name="cim_systemcomponent-class-cimwin32-wmi-providers"></a><span data-ttu-id="f671f-103">Classe CIM_SystemComponent (provedores WMI CIMWin32)</span><span class="sxs-lookup"><span data-stu-id="f671f-103">CIM_SystemComponent class (CIMWin32 WMI Providers)</span></span>

<span data-ttu-id="f671f-104">A classe **CIM \_ Systemcomponent** é uma classe de associação de modelo CIM (CIM) que estabelece relações entre um sistema e os elementos do sistema gerenciado dos quais ele é composto.</span><span class="sxs-lookup"><span data-stu-id="f671f-104">The **CIM\_SystemComponent** class is a Common Information Model (CIM) association class that establishes relationships between a system and the managed system elements of which it is composed.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f671f-105">As classes DMTF (Distributed Management Task Force) CIM (modelo CIM) são as classes pai nas quais as classes WMI são criadas.</span><span class="sxs-lookup"><span data-stu-id="f671f-105">The DMTF (Distributed Management Task Force) CIM (Common Information Model) classes are the parent classes upon which WMI classes are built.</span></span> <span data-ttu-id="f671f-106">Atualmente, o WMI dá suporte apenas aos [esquemas de versão do CIM 2. x](https://dmtf.org/standards/cim/schemas).</span><span class="sxs-lookup"><span data-stu-id="f671f-106">WMI currently supports only the [CIM 2.x version schemas](https://dmtf.org/standards/cim/schemas).</span></span>

 

<span data-ttu-id="f671f-107">A sintaxe a seguir é simplificada do código formato MOF (MOF) e inclui todas as suas propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f671f-107">The following syntax is simplified from Managed Object Format (MOF) code and includes all of its inherited properties.</span></span> <span data-ttu-id="f671f-108">As propriedades são listadas em ordem alfabética, não em ordem MOF.</span><span class="sxs-lookup"><span data-stu-id="f671f-108">Properties are listed in alphabetic order, not MOF order.</span></span>

## <a name="syntax"></a><span data-ttu-id="f671f-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f671f-109">Syntax</span></span>

``` syntax
[Abstract, UUID("{527BC6CE-BAFE-11d2-85E5-0000F8102E5F}"), AMENDMENT]
class CIM_SystemComponent : CIM_Component
{
  CIM_ManagedSystemElement REF PartComponent;
  CIM_System               REF GroupComponent;
};
```

## <a name="members"></a><span data-ttu-id="f671f-110">Membros</span><span class="sxs-lookup"><span data-stu-id="f671f-110">Members</span></span>

<span data-ttu-id="f671f-111">A classe **CIM \_ Systemcomponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f671f-111">The **CIM\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f671f-112">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f671f-112">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f671f-113">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f671f-113">Properties</span></span>

<span data-ttu-id="f671f-114">A classe **CIM \_ Systemcomponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f671f-114">The **CIM\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f671f-115">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f671f-115">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f671f-116">Tipo de dados **: \_ sistema CIM**</span><span class="sxs-lookup"><span data-stu-id="f671f-116">Data type: **CIM\_System**</span></span>
</dt> <dt>

<span data-ttu-id="f671f-117">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f671f-117">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f671f-118">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span><span class="sxs-lookup"><span data-stu-id="f671f-118">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("GroupComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f671f-119">Um [**\_ sistema CIM**](cim-system.md) que descreve o sistema pai na associação.</span><span class="sxs-lookup"><span data-stu-id="f671f-119">A [**CIM\_System**](cim-system.md) that describes the parent system in the association.</span></span>

</dd> <dt>

<span data-ttu-id="f671f-120">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f671f-120">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f671f-121">Tipo de dados: **CIM \_ ManagedSystemElement**</span><span class="sxs-lookup"><span data-stu-id="f671f-121">Data type: **CIM\_ManagedSystemElement**</span></span>
</dt> <dt>

<span data-ttu-id="f671f-122">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f671f-122">Access type: Read-only</span></span>
</dt> <dt>

<span data-ttu-id="f671f-123">Qualificadores: [**override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span><span class="sxs-lookup"><span data-stu-id="f671f-123">Qualifiers: [**Override**](/windows/desktop/WmiSdk/standard-qualifiers) ("PartComponent")</span></span>
</dt> </dl>

<span data-ttu-id="f671f-124">Um [**\_ ManagedSystemElement CIM**](cim-managedsystemelement.md) que descreve o elemento filho que é um componente de um sistema.</span><span class="sxs-lookup"><span data-stu-id="f671f-124">A [**CIM\_ManagedSystemElement**](cim-managedsystemelement.md) that describes the child element that is a component of a system.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f671f-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="f671f-125">Remarks</span></span>

<span data-ttu-id="f671f-126">O WMI não implementa essa classe.</span><span class="sxs-lookup"><span data-stu-id="f671f-126">WMI does not implement this class.</span></span> <span data-ttu-id="f671f-127">Para classes WMI derivadas do **CIM \_ Systemcomponent**, consulte [classes Win32](win32-provider.md).</span><span class="sxs-lookup"><span data-stu-id="f671f-127">For WMI classes derived from **CIM\_SystemComponent**, see [Win32 Classes](win32-provider.md).</span></span>

<span data-ttu-id="f671f-128">Esta documentação é derivada das descrições da classe CIM publicadas pela DMTF.</span><span class="sxs-lookup"><span data-stu-id="f671f-128">This documentation is derived from the CIM class descriptions published by the DMTF.</span></span> <span data-ttu-id="f671f-129">A Microsoft pode ter feito alterações para corrigir erros secundários, obedecer aos padrões de documentação do Microsoft SDK ou fornecer mais informações.</span><span class="sxs-lookup"><span data-stu-id="f671f-129">Microsoft may have made changes to correct minor errors, conform to Microsoft SDK documentation standards, or provide more information.</span></span>

## <a name="requirements"></a><span data-ttu-id="f671f-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f671f-130">Requirements</span></span>



| <span data-ttu-id="f671f-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="f671f-131">Requirement</span></span> | <span data-ttu-id="f671f-132">Valor</span><span class="sxs-lookup"><span data-stu-id="f671f-132">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f671f-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f671f-133">Minimum supported client</span></span><br/> | <span data-ttu-id="f671f-134">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="f671f-134">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="f671f-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f671f-135">Minimum supported server</span></span><br/> | <span data-ttu-id="f671f-136">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="f671f-136">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="f671f-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="f671f-137">Namespace</span></span><br/>                | <span data-ttu-id="f671f-138">Raiz \\ cimv2</span><span class="sxs-lookup"><span data-stu-id="f671f-138">Root\\CIMV2</span></span><br/>                                                                  |
| <span data-ttu-id="f671f-139">MOF</span><span class="sxs-lookup"><span data-stu-id="f671f-139">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f671f-140"><dt>CIMWin32. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f671f-140"><dt>CIMWin32.mof</dt></span></span> </dl> |
| <span data-ttu-id="f671f-141">DLL</span><span class="sxs-lookup"><span data-stu-id="f671f-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f671f-142"><dt>CIMWin32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f671f-142"><dt>CIMWin32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f671f-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="f671f-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f671f-144">**\_Componente CIM**</span><span class="sxs-lookup"><span data-stu-id="f671f-144">**CIM\_Component**</span></span>](cim-component.md)
</dt> </dl>

 

