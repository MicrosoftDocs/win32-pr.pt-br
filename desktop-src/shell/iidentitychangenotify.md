---
description: Preterido. Fornece notificação de modificações para identidades de usuário no sistema, bem como solicitações de usuário para alternar a identidade do usuário atual.
ms.assetid: 09903aa6-62bf-4820-9a09-79956d775441
title: Interface IIdentityChangeNotify (Msident. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IIdentityChangeNotify
api_type:
- COM
api_location:
- Msoe.dll
ms.openlocfilehash: 4a217b2cfb046bfb9ae5546e015264f74d00b1d0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169419"
---
# <a name="iidentitychangenotify-interface"></a><span data-ttu-id="0f8d2-104">Interface IIdentityChangeNotify</span><span class="sxs-lookup"><span data-stu-id="0f8d2-104">IIdentityChangeNotify interface</span></span>

<span data-ttu-id="0f8d2-105">\[A interface **IIdentityChangeNotify** está disponível para uso no Windows 2000.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-105">\[The **IIdentityChangeNotify** interface is available for use in Windows 2000.</span></span> <span data-ttu-id="0f8d2-106">No Windows XP, essa funcionalidade foi substituída por [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md)e pode ser alterada ou indisponível nas versões subsequentes.\]</span><span class="sxs-lookup"><span data-stu-id="0f8d2-106">In Windows XP, this functionality has been superseded by [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md), and might be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="0f8d2-107">Preterido.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-107">Deprecated.</span></span> <span data-ttu-id="0f8d2-108">Fornece notificação de modificações para identidades de usuário no sistema, bem como solicitações de usuário para alternar a identidade do usuário atual.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-108">Provides notification of modifications to user identities on the system, as well as user requests to switch the current user identity.</span></span>

## <a name="members"></a><span data-ttu-id="0f8d2-109">Membros</span><span class="sxs-lookup"><span data-stu-id="0f8d2-109">Members</span></span>

<span data-ttu-id="0f8d2-110">A interface **IIdentityChangeNotify** herda da interface [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="0f8d2-110">The **IIdentityChangeNotify** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="0f8d2-111">**IIdentityChangeNotify** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="0f8d2-111">**IIdentityChangeNotify** also has these types of members:</span></span>

-   [<span data-ttu-id="0f8d2-112">Métodos</span><span class="sxs-lookup"><span data-stu-id="0f8d2-112">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="0f8d2-113">Métodos</span><span class="sxs-lookup"><span data-stu-id="0f8d2-113">Methods</span></span>

<span data-ttu-id="0f8d2-114">A interface **IIdentityChangeNotify** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-114">The **IIdentityChangeNotify** interface has these methods.</span></span>



| <span data-ttu-id="0f8d2-115">Método</span><span class="sxs-lookup"><span data-stu-id="0f8d2-115">Method</span></span>                                                                                 | <span data-ttu-id="0f8d2-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="0f8d2-116">Description</span></span>                                                                                                                           |
|:---------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0f8d2-117">**IdentityInformationChanged**</span><span class="sxs-lookup"><span data-stu-id="0f8d2-117">**IdentityInformationChanged**</span></span>](iidentitychangenotify-identityinformationchanged.md) | <span data-ttu-id="0f8d2-118">Preterido.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-118">Deprecated.</span></span> <span data-ttu-id="0f8d2-119">Chamado quando informações sobre uma identidade de usuário são alteradas ou quando uma identidade de usuário é adicionada ou excluída.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-119">Called when information about a user identity has changed, or when a user identity has been added or deleted.</span></span><br/>  |
| [<span data-ttu-id="0f8d2-120">**QuerySwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="0f8d2-120">**QuerySwitchIdentities**</span></span>](iidentitychangenotify-queryswitchidentities.md)           | <span data-ttu-id="0f8d2-121">Preterido.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-121">Deprecated.</span></span> <span data-ttu-id="0f8d2-122">Chamado quando o usuário atual solicitou que a identidade do usuário fosse alternada, mas antes do comutador ocorrer.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-122">Called when the current user has requested that their user identity be switched, but before the switch occurs.</span></span><br/> |
| [<span data-ttu-id="0f8d2-123">**SwitchIdentities**</span><span class="sxs-lookup"><span data-stu-id="0f8d2-123">**SwitchIdentities**</span></span>](iidentitychangenotify-switchidentities.md)                     | <span data-ttu-id="0f8d2-124">Preterido.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-124">Deprecated.</span></span> <span data-ttu-id="0f8d2-125">Chamado quando as identidades de usuário são alternadas.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-125">Called when user identities are switched.</span></span><br/>                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="0f8d2-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="0f8d2-126">Remarks</span></span>

<span data-ttu-id="0f8d2-127">Para implementar notificações, uma interface derivada deve se conectar ao [**IUserIdentityManager**](iuseridentitymanager.md) chamando [**IConnectionPoint:: Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) e passando um ponteiro para a interface.</span><span class="sxs-lookup"><span data-stu-id="0f8d2-127">To implement notifications, a derived interface must connect to the [**IUserIdentityManager**](iuseridentitymanager.md) by calling [**IConnectionPoint::Advise**](/windows/win32/api/ocidl/nf-ocidl-iconnectionpoint-advise) and by passing a pointer to the interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="0f8d2-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0f8d2-128">Requirements</span></span>



| <span data-ttu-id="0f8d2-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="0f8d2-129">Requirement</span></span> | <span data-ttu-id="0f8d2-130">Valor</span><span class="sxs-lookup"><span data-stu-id="0f8d2-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="0f8d2-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f8d2-131">Minimum supported client</span></span><br/> | <span data-ttu-id="0f8d2-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0f8d2-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="0f8d2-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0f8d2-133">Minimum supported server</span></span><br/> | <span data-ttu-id="0f8d2-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="0f8d2-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="0f8d2-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="0f8d2-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f8d2-136"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="0f8d2-136"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f8d2-137">INSERI</span><span class="sxs-lookup"><span data-stu-id="0f8d2-137">IDL</span></span><br/>                      | <dl> <span data-ttu-id="0f8d2-138"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="0f8d2-138"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="0f8d2-139">DLL</span><span class="sxs-lookup"><span data-stu-id="0f8d2-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f8d2-140"><dt>Msoe.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f8d2-140"><dt>Msoe.dll</dt></span></span> </dl>    |



## <a name="see-also"></a><span data-ttu-id="0f8d2-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="0f8d2-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f8d2-142">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="0f8d2-142">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="0f8d2-143">**IConnectionPoint**</span><span class="sxs-lookup"><span data-stu-id="0f8d2-143">**IConnectionPoint**</span></span>](/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint)
</dt> </dl>

 

 
