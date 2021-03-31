---
title: add urlacl
description: Reserva a URL especificada para usuários e contas não administradores.
ms.assetid: 5d89dec3-26e6-4db8-b4cc-e9b933ac60c5
keywords:
- Adicionar HTTP urlacl
topic_type:
- apiref
api_name:
- add urlacl
api_type:
- NA
ms.topic: reference
ms.custom: snippet-project
ms.date: 07/29/2020
ms.openlocfilehash: 16f6cb64c0c784f3a5400e2c97e212edbc50936c
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/10/2021
ms.locfileid: "103930529"
---
# <a name="add-urlacl"></a><span data-ttu-id="1e181-104">add urlacl</span><span class="sxs-lookup"><span data-stu-id="1e181-104">add urlacl</span></span>

<span data-ttu-id="1e181-105">Reserva a URL especificada para usuários e contas não administradores.</span><span class="sxs-lookup"><span data-stu-id="1e181-105">Reserves the specified URL for non-administrator users and accounts.</span></span> <span data-ttu-id="1e181-106">A DACL (lista de controle de acesso discricionário) pode ser especificada usando um nome de conta com os parâmetros Listen e delegate ou usando uma cadeia de caracteres SDDL (Security Descriptor Definition Language).</span><span class="sxs-lookup"><span data-stu-id="1e181-106">The discretionary access control list (DACL) can be specified by using an account name with the listen and delegate parameters or by using a security descriptor definition language (SDDL) string.</span></span>

``` syntax
add urlacl [url=]string
           [[user=]string
           {[[listen={yes|no}] [delegate={yes|no}]] | [sddl=]string}

 
```

## <a name="parameters"></a><span data-ttu-id="1e181-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e181-107">Parameters</span></span>

<dl> <span data-ttu-id="1e181-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url =] cadeia de caracteres**
</dt> </span><span class="sxs-lookup"><span data-stu-id="1e181-108"><dt>

<span id="_url__string"></span><span id="_URL__STRING"></span>
**[url=] string**
</dt> </span></span><dd>

<span data-ttu-id="1e181-109">Especifica a URL totalmente qualificada.</span><span class="sxs-lookup"><span data-stu-id="1e181-109">Specifies the fully qualified URL.</span></span>

<span data-ttu-id="1e181-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[User =] cadeia de caracteres**
</dt> </span><span class="sxs-lookup"><span data-stu-id="1e181-110"></dd> <dt>

<span id="_user__string"></span><span id="_USER__STRING"></span>
**[user=] string**
</dt> </span></span><dd>

<span data-ttu-id="1e181-111">Especifica o nome do usuário ou grupo de usuários.</span><span class="sxs-lookup"><span data-stu-id="1e181-111">Specifies the user or user group name.</span></span>

</dd> <dt>

<span data-ttu-id="1e181-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[escutar = {sim \| não}\]**</span><span class="sxs-lookup"><span data-stu-id="1e181-112"><span id="_listen__yes_no__"></span><span id="_LISTEN__YES_NO__"></span>**\[listen={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="1e181-113">Especifica um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="1e181-113">Specifies one of the following values:</span></span>

-   <span data-ttu-id="1e181-114">Sim: permite que o usuário registre URLs.</span><span class="sxs-lookup"><span data-stu-id="1e181-114">yes: Allows the user to register URLs.</span></span> <span data-ttu-id="1e181-115">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="1e181-115">This is the default value.</span></span>
-   <span data-ttu-id="1e181-116">Não: nega o usuário de registrar URLs.</span><span class="sxs-lookup"><span data-stu-id="1e181-116">no: Denies the user from registering URLs.</span></span>

</dd> <dt>

<span data-ttu-id="1e181-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate = {sim \| não}\]**</span><span class="sxs-lookup"><span data-stu-id="1e181-117"><span id="_delegate__yes_no__"></span><span id="_DELEGATE__YES_NO__"></span>**\[delegate={yes\|no}\]**</span></span>
</dt> <dd>

<span data-ttu-id="1e181-118">Especifica um dos seguintes valores:</span><span class="sxs-lookup"><span data-stu-id="1e181-118">Specifies one of the following values:</span></span>

-   <span data-ttu-id="1e181-119">Sim: permite que o usuário delegue URLs.</span><span class="sxs-lookup"><span data-stu-id="1e181-119">yes: Allows the user to delegate URLs.</span></span>
-   <span data-ttu-id="1e181-120">Não: nega o usuário de delegar URLs.</span><span class="sxs-lookup"><span data-stu-id="1e181-120">no: Denies the user from delegating URLs.</span></span> <span data-ttu-id="1e181-121">Esse é o valor padrão.</span><span class="sxs-lookup"><span data-stu-id="1e181-121">This is the default value.</span></span>

<span data-ttu-id="1e181-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[SDDL =] cadeia de caracteres**
</dt> </span><span class="sxs-lookup"><span data-stu-id="1e181-122"></dd> <dt>

<span id="_sddl__string"></span><span id="_SDDL__STRING"></span>
**[sddl=] string**
</dt> </span></span><dd>

<span data-ttu-id="1e181-123">Especifica a cadeia de caracteres SDDL que descreve a DACL.</span><span class="sxs-lookup"><span data-stu-id="1e181-123">Specifies the SDDL string that describes the DACL.</span></span>

</dd> </dl>

## <a name="examples"></a><span data-ttu-id="1e181-124">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1e181-124">Examples</span></span>

* <span data-ttu-id="1e181-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\ user</span><span class="sxs-lookup"><span data-stu-id="1e181-125">add urlacl url=https://+:80/MyUri user=DOMAIN\\user</span></span>

* <span data-ttu-id="1e181-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span><span class="sxs-lookup"><span data-stu-id="1e181-126">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user listen=yes</span></span>

* <span data-ttu-id="1e181-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span><span class="sxs-lookup"><span data-stu-id="1e181-127">add urlacl url=https://www.contoso.com:80/MyUri user=DOMAIN\\user delegate=no</span></span>

 
## <a name="see-also"></a><span data-ttu-id="1e181-128">Consulte Também</span><span class="sxs-lookup"><span data-stu-id="1e181-128">See Also</span></span>

* [<span data-ttu-id="1e181-129">Comandos Netsh http</span><span class="sxs-lookup"><span data-stu-id="1e181-129">Netsh http commands</span></span>](/windows-server/networking/technologies/netsh/netsh-http#add-urlacl)
 