---
description: O campo de tipo em uma ACE (entrada de controle de acesso) que determina se a ACE é uma ACE que permite o acesso ou nega o acesso.
ms.assetid: a78c72f7-0bc0-4bda-9012-4abe45342d8d
ms.tgt_platform: multiple
title: Constantes de tipo de ACE de namespace (WinNT. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Allow
- Deny
api_type:
- HeaderDef
api_location:
- Winnt.h
ms.openlocfilehash: 0c9f1f7e05f663782c0d748ddb296ca36ecbe29c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751764"
---
# <a name="namespace-ace-type-constants"></a><span data-ttu-id="11544-103">Constantes de tipo de ACE de namespace</span><span class="sxs-lookup"><span data-stu-id="11544-103">Namespace ACE Type Constants</span></span>

<span data-ttu-id="11544-104">O campo de **tipo** em uma ACE (entrada de controle de acesso) que determina se a ACE é uma ACE que permite o acesso ou nega o acesso.</span><span class="sxs-lookup"><span data-stu-id="11544-104">The **Type** field in an access control entry (ACE) that determines whether the ACE is an ACE that allows access or denies access.</span></span>

<dl> <dt>

<span data-ttu-id="11544-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Permitir**</span><span class="sxs-lookup"><span data-stu-id="11544-105"><span id="Allow"></span><span id="allow"></span><span id="ALLOW"></span>**Allow**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11544-106">0</span><span class="sxs-lookup"><span data-stu-id="11544-106">0</span></span>
</dt> <dt>



<span data-ttu-id="11544-107">A ACE permite o acesso ao namespace.</span><span class="sxs-lookup"><span data-stu-id="11544-107">The ACE allows access to the namespace.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="11544-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Negar**</span><span class="sxs-lookup"><span data-stu-id="11544-108"><span id="Deny"></span><span id="deny"></span><span id="DENY"></span>**Deny**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="11544-109">1</span><span class="sxs-lookup"><span data-stu-id="11544-109">1</span></span>
</dt> <dt>



<span data-ttu-id="11544-110">A ACE nega o acesso ao namespace.</span><span class="sxs-lookup"><span data-stu-id="11544-110">The ACE denies access to the namespace.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="11544-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="11544-111">Requirements</span></span>



| <span data-ttu-id="11544-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="11544-112">Requirement</span></span> | <span data-ttu-id="11544-113">Valor</span><span class="sxs-lookup"><span data-stu-id="11544-113">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="11544-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="11544-114">Header</span></span><br/> | <dl> <span data-ttu-id="11544-115"><dt>Winnt. h</dt></span><span class="sxs-lookup"><span data-stu-id="11544-115"><dt>Winnt.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="11544-116">Confira também</span><span class="sxs-lookup"><span data-stu-id="11544-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="11544-117">Constantes de segurança do WMI</span><span class="sxs-lookup"><span data-stu-id="11544-117">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="11544-118">Configurando descritores de segurança namepace</span><span class="sxs-lookup"><span data-stu-id="11544-118">Setting Namepace Security Descriptors</span></span>](setting-namespace-security-descriptors.md)
</dt> <dt>

[<span data-ttu-id="11544-119">Estabelecendo a herança da segurança do namespace</span><span class="sxs-lookup"><span data-stu-id="11544-119">Establishing Inheritance of Namespace Security</span></span>](establishing-inheritance-of-namespace-security.md)
</dt> <dt>

[<span data-ttu-id="11544-120">**\_\_SystemSecurity**</span><span class="sxs-lookup"><span data-stu-id="11544-120">**\_\_SystemSecurity**</span></span>](--systemsecurity.md)
</dt> </dl>

 

 




