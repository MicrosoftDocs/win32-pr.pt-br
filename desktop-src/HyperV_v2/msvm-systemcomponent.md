---
description: Estabelece um &\# 0034; parte do&\# 0034; relação entre um sistema e qualquer elemento do sistema gerenciado do qual ele é composto.
ms.assetid: 6BF72E36-9B6C-4853-A553-DDAF65991C86
title: Classe Msvm_SystemComponent
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SystemComponent
- Msvm_SystemComponent.GroupComponent
- Msvm_SystemComponent.PartComponent
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: ee150793143b549c90d280eef287ee6a5afb66b9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104370604"
---
# <a name="msvm_systemcomponent-class"></a><span data-ttu-id="f3721-103">\_Classe Msvm Systemcomponent</span><span class="sxs-lookup"><span data-stu-id="f3721-103">Msvm\_SystemComponent class</span></span>

<span data-ttu-id="f3721-104">Estabelece uma relação "parte de" entre um sistema e qualquer elemento do sistema gerenciado do qual ele é composto.</span><span class="sxs-lookup"><span data-stu-id="f3721-104">Establishes a "part of" relationship between a system and any managed system element of which it is composed.</span></span>

<span data-ttu-id="f3721-105">A sintaxe a seguir é simplificada formato MOF código (MOF) e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="f3721-105">The following syntax is simplified Managed Object Format (MOF) code, and it includes all of the inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="f3721-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f3721-106">Syntax</span></span>

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), Association, Aggregation]
class Msvm_SystemComponent : CIM_SystemComponent
{
  CIM_System               REF GroupComponent;
  CIM_ManagedSystemElement REF PartComponent;
};
```

## <a name="members"></a><span data-ttu-id="f3721-107">Membros</span><span class="sxs-lookup"><span data-stu-id="f3721-107">Members</span></span>

<span data-ttu-id="f3721-108">A classe **Msvm \_ Systemcomponent** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="f3721-108">The **Msvm\_SystemComponent** class has these types of members:</span></span>

-   [<span data-ttu-id="f3721-109">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3721-109">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="f3721-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="f3721-110">Properties</span></span>

<span data-ttu-id="f3721-111">A classe **Msvm \_ Systemcomponent** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="f3721-111">The **Msvm\_SystemComponent** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="f3721-112">**GroupComponent**</span><span class="sxs-lookup"><span data-stu-id="f3721-112">**GroupComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3721-113">Tipo de dados: **[ **\_ sistema CIM**](/windows/desktop/CIMWin32Prov/cim-system)**</span><span class="sxs-lookup"><span data-stu-id="f3721-113">Data type: **[**CIM\_System**](/windows/desktop/CIMWin32Prov/cim-system)**</span></span>
</dt> <dt>

<span data-ttu-id="f3721-114">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f3721-114">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3721-115">O elemento pai na associação.</span><span class="sxs-lookup"><span data-stu-id="f3721-115">The parent element in the association.</span></span> <span data-ttu-id="f3721-116">Essa propriedade é herdada do [**CIM \_ Systemcomponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="f3721-116">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> <dt>

<span data-ttu-id="f3721-117">**PartComponent**</span><span class="sxs-lookup"><span data-stu-id="f3721-117">**PartComponent**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="f3721-118">Tipo de dados: **[ **CIM \_ ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span><span class="sxs-lookup"><span data-stu-id="f3721-118">Data type: **[**CIM\_ManagedSystemElement**](/windows/desktop/CIMWin32Prov/cim-managedsystemelement)**</span></span>
</dt> <dt>

<span data-ttu-id="f3721-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="f3721-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="f3721-120">O elemento filho na associação.</span><span class="sxs-lookup"><span data-stu-id="f3721-120">The child element in the association.</span></span> <span data-ttu-id="f3721-121">Essa propriedade é herdada do [**CIM \_ Systemcomponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span><span class="sxs-lookup"><span data-stu-id="f3721-121">This property is inherited from [**CIM\_SystemComponent**](/windows/desktop/CIMWin32Prov/cim-systemcomponent).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f3721-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f3721-122">Requirements</span></span>



| <span data-ttu-id="f3721-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="f3721-123">Requirement</span></span> | <span data-ttu-id="f3721-124">Valor</span><span class="sxs-lookup"><span data-stu-id="f3721-124">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f3721-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3721-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f3721-126">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="f3721-126">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="f3721-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="f3721-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f3721-128">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="f3721-128">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="f3721-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="f3721-129">Namespace</span></span><br/>                | <span data-ttu-id="f3721-130">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="f3721-130">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="f3721-131">MOF</span><span class="sxs-lookup"><span data-stu-id="f3721-131">MOF</span></span><br/>                      | <dl> <span data-ttu-id="f3721-132"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="f3721-132"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="f3721-133">DLL</span><span class="sxs-lookup"><span data-stu-id="f3721-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f3721-134"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="f3721-134"><dt>Vmms.exe</dt></span></span> </dl>                     |



 

