---
description: A lista a seguir lista os possíveis valores do campo Flags em uma ACE (entrada de controle de acesso) WMI.
ms.assetid: bd09691d-e285-40e0-8686-edd5a132a06e
ms.tgt_platform: multiple
title: Constantes do sinalizador ACE do namespace (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- OBJECT_INHERIT_ACE
- CONTAINER_INHERIT_ACE
- NO_PROPAGATE_INHERIT_ACE
- INHERIT_ONLY_ACE
- INHERITED_ACE
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 053d4166882b6254dec313cb10fbf10588ba0071
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750141"
---
# <a name="namespace-ace-flag-constants"></a><span data-ttu-id="9603a-103">Constantes do sinalizador ACE do namespace</span><span class="sxs-lookup"><span data-stu-id="9603a-103">Namespace ACE Flag Constants</span></span>

<span data-ttu-id="9603a-104">A lista a seguir lista os possíveis valores do campo **flags** em uma ACE (entrada de controle de acesso) WMI.</span><span class="sxs-lookup"><span data-stu-id="9603a-104">The following list lists the possible values of the **Flags** field in a WMI Access Control Entry (ACE).</span></span>

<dl> <dt>

<span data-ttu-id="9603a-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**\_ACE de herança de objeto \_**</span><span class="sxs-lookup"><span data-stu-id="9603a-105"><span id="OBJECT_INHERIT_ACE"></span><span id="object_inherit_ace"></span>**OBJECT\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9603a-106">1 (0x1)</span><span class="sxs-lookup"><span data-stu-id="9603a-106">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="9603a-107">Os objetos filho sem contêiner herdam a ACE como uma ACE efetiva.</span><span class="sxs-lookup"><span data-stu-id="9603a-107">Non-container child objects inherit the ACE as an effective ACE.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9603a-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**\_Ace herdar contêiner \_**</span><span class="sxs-lookup"><span data-stu-id="9603a-108"><span id="CONTAINER_INHERIT_ACE"></span><span id="container_inherit_ace"></span>**CONTAINER\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9603a-109">2 (0x2)</span><span class="sxs-lookup"><span data-stu-id="9603a-109">2 (0x2)</span></span>
</dt> <dt>



<span data-ttu-id="9603a-110">A ACE tem um efeito nos namespaces filho, bem como no namespace atual.</span><span class="sxs-lookup"><span data-stu-id="9603a-110">The ACE has an effect on child namespaces as well as the current namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9603a-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NENHUMA \_ ACE de \_ herança de propagação \_**</span><span class="sxs-lookup"><span data-stu-id="9603a-111"><span id="NO_PROPAGATE_INHERIT_ACE"></span><span id="no_propagate_inherit_ace"></span>**NO\_PROPAGATE\_INHERIT\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9603a-112">4 (0x4)</span><span class="sxs-lookup"><span data-stu-id="9603a-112">4 (0x4)</span></span>
</dt> <dt>



<span data-ttu-id="9603a-113">A ACE aplica-se somente ao namespace atual e aos filhos imediatos.</span><span class="sxs-lookup"><span data-stu-id="9603a-113">The ACE applies only to the current namespace and immediate children .</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9603a-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**HERDAr \_ somente \_ Ace**</span><span class="sxs-lookup"><span data-stu-id="9603a-114"><span id="INHERIT_ONLY_ACE"></span><span id="inherit_only_ace"></span>**INHERIT\_ONLY\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9603a-115">8 (0x8)</span><span class="sxs-lookup"><span data-stu-id="9603a-115">8 (0x8)</span></span>
</dt> <dt>



<span data-ttu-id="9603a-116">A ACE aplica-se somente a namespaces filho.</span><span class="sxs-lookup"><span data-stu-id="9603a-116">The ACE applies only to child namespaces.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="9603a-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**Ace HERDAdo \_**</span><span class="sxs-lookup"><span data-stu-id="9603a-117"><span id="INHERITED_ACE"></span><span id="inherited_ace"></span>**INHERITED\_ACE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="9603a-118">16 (0x10)</span><span class="sxs-lookup"><span data-stu-id="9603a-118">16 (0x10)</span></span>
</dt> <dt>



<span data-ttu-id="9603a-119">Isso não é definido pelos clientes, mas é relatado para clientes quando a origem de uma ACE é um namespace pai.</span><span class="sxs-lookup"><span data-stu-id="9603a-119">This is not set by clients, but is reported to clients when the source of an ACE is a parent namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9603a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9603a-120">Requirements</span></span>



| <span data-ttu-id="9603a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="9603a-121">Requirement</span></span> | <span data-ttu-id="9603a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="9603a-122">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="9603a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9603a-123">Header</span></span><br/> | <dl> <span data-ttu-id="9603a-124"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="9603a-124"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9603a-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="9603a-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9603a-126">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="9603a-126">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="9603a-127">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="9603a-127">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="9603a-128">Estabelecendo a herança da segurança do namespace</span><span class="sxs-lookup"><span data-stu-id="9603a-128">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="9603a-129">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="9603a-129">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




