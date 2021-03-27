---
description: IUserIdentity2 não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 85238574-f6bf-43d7-a41b-3ea086c45e07
title: Interface IUserIdentity2 (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88142e462566a6afaf299096744a0b8f9ea83dfa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501148"
---
# <a name="iuseridentity2-interface"></a><span data-ttu-id="25136-104">Interface IUserIdentity2</span><span class="sxs-lookup"><span data-stu-id="25136-104">IUserIdentity2 interface</span></span>

<span data-ttu-id="25136-105">\[**IUserIdentity2** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="25136-105">\[**IUserIdentity2** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="25136-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="25136-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="25136-107">Expõe métodos que fornecem nomenclatura, senha e controle ordinal para uma identidade de usuário específica.</span><span class="sxs-lookup"><span data-stu-id="25136-107">Exposes methods that provide naming, password, and ordinal control for a specific user identity.</span></span>

## <a name="members"></a><span data-ttu-id="25136-108">Membros</span><span class="sxs-lookup"><span data-stu-id="25136-108">Members</span></span>

<span data-ttu-id="25136-109">A interface **IUserIdentity2** herda de [**IUserIdentity**](iuseridentity.md).</span><span class="sxs-lookup"><span data-stu-id="25136-109">The **IUserIdentity2** interface inherits from [**IUserIdentity**](iuseridentity.md).</span></span> <span data-ttu-id="25136-110">**IUserIdentity2** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="25136-110">**IUserIdentity2** also has these types of members:</span></span>

-   [<span data-ttu-id="25136-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="25136-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="25136-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="25136-112">Methods</span></span>

<span data-ttu-id="25136-113">A interface **IUserIdentity2** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="25136-113">The **IUserIdentity2** interface has these methods.</span></span>



| <span data-ttu-id="25136-114">Método</span><span class="sxs-lookup"><span data-stu-id="25136-114">Method</span></span>                                                  | <span data-ttu-id="25136-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="25136-115">Description</span></span>                                                       |
|:--------------------------------------------------------|:------------------------------------------------------------------|
| [<span data-ttu-id="25136-116">**ChangePassword**</span><span class="sxs-lookup"><span data-stu-id="25136-116">**ChangePassword**</span></span>](iuseridentity2-changepassword.md) | <span data-ttu-id="25136-117">Preterido.</span><span class="sxs-lookup"><span data-stu-id="25136-117">Deprecated.</span></span> <span data-ttu-id="25136-118">Define uma nova senha para a identidade.</span><span class="sxs-lookup"><span data-stu-id="25136-118">Sets a new password for the identity.</span></span><br/>      |
| [<span data-ttu-id="25136-119">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="25136-119">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)         | <span data-ttu-id="25136-120">Preterido.</span><span class="sxs-lookup"><span data-stu-id="25136-120">Deprecated.</span></span> <span data-ttu-id="25136-121">Obtém o número ordinal desta identidade.</span><span class="sxs-lookup"><span data-stu-id="25136-121">Gets the ordinal number for this identity.</span></span><br/> |
| [<span data-ttu-id="25136-122">**SetName**</span><span class="sxs-lookup"><span data-stu-id="25136-122">**SetName**</span></span>](iuseridentity2-setname.md)               | <span data-ttu-id="25136-123">Preterido.</span><span class="sxs-lookup"><span data-stu-id="25136-123">Deprecated.</span></span> <span data-ttu-id="25136-124">Define o nome de exibição da identidade.</span><span class="sxs-lookup"><span data-stu-id="25136-124">Sets the display name of the identity.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="25136-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="25136-125">Remarks</span></span>

<span data-ttu-id="25136-126">Essa interface também fornece os métodos da interface [**IUserIdentity**](iuseridentity.md) , da qual ela é herdada.</span><span class="sxs-lookup"><span data-stu-id="25136-126">This interface also provides the methods of the [**IUserIdentity**](iuseridentity.md) interface, from which it inherits.</span></span>

## <a name="requirements"></a><span data-ttu-id="25136-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25136-127">Requirements</span></span>



| <span data-ttu-id="25136-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="25136-128">Requirement</span></span> | <span data-ttu-id="25136-129">Valor</span><span class="sxs-lookup"><span data-stu-id="25136-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="25136-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25136-130">Minimum supported client</span></span><br/> | <span data-ttu-id="25136-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="25136-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="25136-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="25136-132">Minimum supported server</span></span><br/> | <span data-ttu-id="25136-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="25136-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="25136-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="25136-134">End of client support</span></span><br/>    | <span data-ttu-id="25136-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="25136-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="25136-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="25136-136">End of server support</span></span><br/>    | <span data-ttu-id="25136-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="25136-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="25136-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25136-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="25136-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="25136-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="25136-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="25136-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="25136-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="25136-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="25136-142">DLL</span><span class="sxs-lookup"><span data-stu-id="25136-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="25136-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="25136-143"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25136-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="25136-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25136-145">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="25136-145">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> </dl>

 

 




