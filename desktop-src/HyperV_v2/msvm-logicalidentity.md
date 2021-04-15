---
description: Associa dois elementos gerenciados que representam diferentes aspectos da mesma entidade subjacente.
ms.assetid: 107A2B15-09F2-490A-8AB2-F9FE5F6FEE60
title: Classe Msvm_LogicalIdentity
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_LogicalIdentity
- Msvm_LogicalIdentity.SameElement
- Msvm_LogicalIdentity.SystemElement
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: c2f8d2ee522fde3769c08bcbb78611b99eed8e16
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104505859"
---
# <a name="msvm_logicalidentity-class"></a><span data-ttu-id="376f0-103">\_Classe Msvm LogicalIdentity</span><span class="sxs-lookup"><span data-stu-id="376f0-103">Msvm\_LogicalIdentity class</span></span>

<span data-ttu-id="376f0-104">Associa dois elementos gerenciados que representam diferentes aspectos da mesma entidade subjacente.</span><span class="sxs-lookup"><span data-stu-id="376f0-104">Associates two managed elements that represent different aspects of the same underlying entity.</span></span> <span data-ttu-id="376f0-105">Essa classe deriva do [**CIM \_ LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span><span class="sxs-lookup"><span data-stu-id="376f0-105">This class derives from [**CIM\_LogicalIdentity**](/windows/desktop/CIMWin32Prov/cim-logicalidentity).</span></span>

<span data-ttu-id="376f0-106">A sintaxe a seguir é simplificada do código MOF e inclui todas as propriedades herdadas.</span><span class="sxs-lookup"><span data-stu-id="376f0-106">The following syntax is simplified from MOF code and includes all inherited properties.</span></span>

## <a name="syntax"></a><span data-ttu-id="376f0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="376f0-107">Syntax</span></span>

``` syntax
[Association, Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_LogicalIdentity : CIM_LogicalIdentity
{
  CIM_LogicalElement REF SameElement;
  CIM_LogicalElement REF SystemElement;
};
```

## <a name="members"></a><span data-ttu-id="376f0-108">Membros</span><span class="sxs-lookup"><span data-stu-id="376f0-108">Members</span></span>

<span data-ttu-id="376f0-109">A classe **Msvm \_ LogicalIdentity** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="376f0-109">The **Msvm\_LogicalIdentity** class has these types of members:</span></span>

-   [<span data-ttu-id="376f0-110">Propriedades</span><span class="sxs-lookup"><span data-stu-id="376f0-110">Properties</span></span>](#properties)

### <a name="properties"></a><span data-ttu-id="376f0-111">Propriedades</span><span class="sxs-lookup"><span data-stu-id="376f0-111">Properties</span></span>

<span data-ttu-id="376f0-112">A classe **Msvm \_ LogicalIdentity** tem essas propriedades.</span><span class="sxs-lookup"><span data-stu-id="376f0-112">The **Msvm\_LogicalIdentity** class has these properties.</span></span>

<dl> <dt>

<span data-ttu-id="376f0-113">**Mesmoelement**</span><span class="sxs-lookup"><span data-stu-id="376f0-113">**SameElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="376f0-114">Tipo de dados: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="376f0-114">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="376f0-115">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="376f0-115">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="376f0-116">Referência a um aspecto alternativo da entidade do sistema.</span><span class="sxs-lookup"><span data-stu-id="376f0-116">Reference to an alternate aspect of the system entity.</span></span>

</dd> <dt>

<span data-ttu-id="376f0-117">**Sistema de**</span><span class="sxs-lookup"><span data-stu-id="376f0-117">**SystemElement**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="376f0-118">Tipo de dados: **CIM \_ LogicalElement**</span><span class="sxs-lookup"><span data-stu-id="376f0-118">Data type: **CIM\_LogicalElement**</span></span>
</dt> <dt>

<span data-ttu-id="376f0-119">Tipo de acesso: Somente leitura</span><span class="sxs-lookup"><span data-stu-id="376f0-119">Access type: Read-only</span></span>
</dt> </dl>

<span data-ttu-id="376f0-120">Referência a um aspecto do elemento lógico.</span><span class="sxs-lookup"><span data-stu-id="376f0-120">Reference to one aspect of the logical element.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="376f0-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="376f0-121">Requirements</span></span>



| <span data-ttu-id="376f0-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="376f0-122">Requirement</span></span> | <span data-ttu-id="376f0-123">Valor</span><span class="sxs-lookup"><span data-stu-id="376f0-123">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="376f0-124">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="376f0-124">Minimum supported client</span></span><br/> | <span data-ttu-id="376f0-125">Windows 8.1 \[ apenas aplicativos de área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="376f0-125">Windows 8.1 \[desktop apps only\]</span></span><br/>                                                            |
| <span data-ttu-id="376f0-126">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="376f0-126">Minimum supported server</span></span><br/> | <span data-ttu-id="376f0-127">\[Somente aplicativos da área de trabalho do Windows Server 2012 R2\]</span><span class="sxs-lookup"><span data-stu-id="376f0-127">Windows Server 2012 R2 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="376f0-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="376f0-128">Namespace</span></span><br/>                | <span data-ttu-id="376f0-129">\\Virtualização \\ v2 de raiz</span><span class="sxs-lookup"><span data-stu-id="376f0-129">Root\\Virtualization\\V2</span></span><br/>                                                                     |
| <span data-ttu-id="376f0-130">MOF</span><span class="sxs-lookup"><span data-stu-id="376f0-130">MOF</span></span><br/>                      | <dl> <span data-ttu-id="376f0-131"><dt>WindowsVirtualization. v2. mof</dt></span><span class="sxs-lookup"><span data-stu-id="376f0-131"><dt>WindowsVirtualization.V2.mof</dt></span></span> </dl> |
| <span data-ttu-id="376f0-132">DLL</span><span class="sxs-lookup"><span data-stu-id="376f0-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="376f0-133"><dt>Vmms.exe</dt></span><span class="sxs-lookup"><span data-stu-id="376f0-133"><dt>Vmms.exe</dt></span></span> </dl>                     |



## <a name="see-also"></a><span data-ttu-id="376f0-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="376f0-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="376f0-135">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="376f0-135">**CIM\_LogicalIdentity**</span></span>](cim-logicalidentity.md)
</dt> <dt>

[<span data-ttu-id="376f0-136">**\_LOGICALIDENTITY CIM**</span><span class="sxs-lookup"><span data-stu-id="376f0-136">**CIM\_LogicalIdentity**</span></span>](/windows/desktop/CIMWin32Prov/cim-logicalidentity)
</dt> </dl>

 

