---
description: IUserIdentityManager não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 3d24b858-bbaf-455c-83cd-3f6f93aba2a8
title: Interface IUserIdentityManager (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: d0d00399e0ba958ef63c5e6597eb4a34387f92f9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103826721"
---
# <a name="iuseridentitymanager-interface"></a><span data-ttu-id="9395f-104">Interface IUserIdentityManager</span><span class="sxs-lookup"><span data-stu-id="9395f-104">IUserIdentityManager interface</span></span>

<span data-ttu-id="9395f-105">\[**IUserIdentityManager** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="9395f-105">\[**IUserIdentityManager** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="9395f-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="9395f-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="9395f-107">Expõe métodos que identificam, enumeram e gerenciam identidades de usuário no sistema.</span><span class="sxs-lookup"><span data-stu-id="9395f-107">Exposes methods that identify, enumerate, and manage user identities on the system.</span></span>

## <a name="members"></a><span data-ttu-id="9395f-108">Membros</span><span class="sxs-lookup"><span data-stu-id="9395f-108">Members</span></span>

<span data-ttu-id="9395f-109">A interface **IUserIdentityManager** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="9395f-109">The **IUserIdentityManager** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="9395f-110">**IUserIdentityManager** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="9395f-110">**IUserIdentityManager** also has these types of members:</span></span>

-   [<span data-ttu-id="9395f-111">Métodos</span><span class="sxs-lookup"><span data-stu-id="9395f-111">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="9395f-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="9395f-112">Methods</span></span>

<span data-ttu-id="9395f-113">A interface **IUserIdentityManager** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="9395f-113">The **IUserIdentityManager** interface has these methods.</span></span>



| <span data-ttu-id="9395f-114">Método</span><span class="sxs-lookup"><span data-stu-id="9395f-114">Method</span></span>                                                                  | <span data-ttu-id="9395f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="9395f-115">Description</span></span>                                                                                                                                                             |
|:------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="9395f-116">**EnumIdentities**</span><span class="sxs-lookup"><span data-stu-id="9395f-116">**EnumIdentities**</span></span>](iuseridentitymanager-enumidentities.md)           | <span data-ttu-id="9395f-117">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9395f-117">Deprecated.</span></span> <span data-ttu-id="9395f-118">Obtém um objeto [**IEnumUserIdentity**](ienumuseridentity.md) , que pode ser usado para enumerar as identidades de usuário presentes no sistema.</span><span class="sxs-lookup"><span data-stu-id="9395f-118">Gets an [**IEnumUserIdentity**](ienumuseridentity.md) object, which can be used to enumerate through the user identities present on the system.</span></span><br/> |
| [<span data-ttu-id="9395f-119">**GetIdentityByCookie**</span><span class="sxs-lookup"><span data-stu-id="9395f-119">**GetIdentityByCookie**</span></span>](iuseridentitymanager-getidentitybycookie.md) | <span data-ttu-id="9395f-120">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9395f-120">Deprecated.</span></span> <span data-ttu-id="9395f-121">Obtém uma identidade de usuário específica pelo cookie usado para identificá-la exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="9395f-121">Gets a specific user identity by the cookie used to uniquely identify it.</span></span><br/>                                                                        |
| [<span data-ttu-id="9395f-122">**Verbos**</span><span class="sxs-lookup"><span data-stu-id="9395f-122">**Logoff**</span></span>](iuseridentitymanager-logoff.md)                           | <span data-ttu-id="9395f-123">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9395f-123">Deprecated.</span></span> <span data-ttu-id="9395f-124">Faça logoff da identidade atual.</span><span class="sxs-lookup"><span data-stu-id="9395f-124">Log off the current identity.</span></span><br/>                                                                                                                    |
| [<span data-ttu-id="9395f-125">**Logon**</span><span class="sxs-lookup"><span data-stu-id="9395f-125">**Logon**</span></span>](iuseridentitymanager-logon.md)                             | <span data-ttu-id="9395f-126">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9395f-126">Deprecated.</span></span> <span data-ttu-id="9395f-127">Exibe uma IU para o usuário, permitindo que o usuário escolha uma identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="9395f-127">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="9395f-128">Se for bem-sucedido, a identidade do usuário será registrada e recuperada.</span><span class="sxs-lookup"><span data-stu-id="9395f-128">If successful, the user identity will be logged on and retrieved.</span></span><br/>        |
| [<span data-ttu-id="9395f-129">**ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="9395f-129">**ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)       | <span data-ttu-id="9395f-130">Preterido.</span><span class="sxs-lookup"><span data-stu-id="9395f-130">Deprecated.</span></span> <span data-ttu-id="9395f-131">Exibe uma IU para o usuário, permitindo que o usuário gerencie identidades de usuário.</span><span class="sxs-lookup"><span data-stu-id="9395f-131">Displays a UI to the user, allowing the user to manage user identities.</span></span><br/>                                                                          |



 

## <a name="requirements"></a><span data-ttu-id="9395f-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9395f-132">Requirements</span></span>



| <span data-ttu-id="9395f-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="9395f-133">Requirement</span></span> | <span data-ttu-id="9395f-134">Valor</span><span class="sxs-lookup"><span data-stu-id="9395f-134">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="9395f-135">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9395f-135">Minimum supported client</span></span><br/> | <span data-ttu-id="9395f-136">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9395f-136">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="9395f-137">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="9395f-137">Minimum supported server</span></span><br/> | <span data-ttu-id="9395f-138">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="9395f-138">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="9395f-139">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="9395f-139">End of client support</span></span><br/>    | <span data-ttu-id="9395f-140">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="9395f-140">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="9395f-141">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="9395f-141">End of server support</span></span><br/>    | <span data-ttu-id="9395f-142">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="9395f-142">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="9395f-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9395f-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="9395f-144"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="9395f-144"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="9395f-145">INSERI</span><span class="sxs-lookup"><span data-stu-id="9395f-145">IDL</span></span><br/>                      | <dl> <span data-ttu-id="9395f-146"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="9395f-146"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="9395f-147">DLL</span><span class="sxs-lookup"><span data-stu-id="9395f-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="9395f-148"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="9395f-148"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9395f-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="9395f-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9395f-150">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="9395f-150">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="9395f-151">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="9395f-151">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="9395f-152">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="9395f-152">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="9395f-153">**IIdentityChangeNotify**</span><span class="sxs-lookup"><span data-stu-id="9395f-153">**IIdentityChangeNotify**</span></span>](iidentitychangenotify.md)
</dt> </dl>

 

 
