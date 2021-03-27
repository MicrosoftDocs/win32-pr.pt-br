---
description: O logoff não tem suporte e pode ser alterado ou não estar disponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: e03fb15c-47d3-40ba-ae70-b7b0ba010004
title: 'Método IUserIdentityManager:: logoff (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logoff
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 4266e6116e43b7b792c3040d7c86a60037ca4c44
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967260"
---
# <a name="iuseridentitymanagerlogoff-method"></a><span data-ttu-id="e4f58-104">Método IUserIdentityManager:: logoff</span><span class="sxs-lookup"><span data-stu-id="e4f58-104">IUserIdentityManager::Logoff method</span></span>

<span data-ttu-id="e4f58-105">\[O **logoff** não tem suporte e pode ser alterado ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="e4f58-105">\[**Logoff** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="e4f58-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="e4f58-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="e4f58-107">Preterido.</span><span class="sxs-lookup"><span data-stu-id="e4f58-107">Deprecated.</span></span> <span data-ttu-id="e4f58-108">Faça logoff da identidade atual.</span><span class="sxs-lookup"><span data-stu-id="e4f58-108">Log off the current identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4f58-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4f58-109">Syntax</span></span>


```C++
HRESULT Logoff(
  [in] HWND hwndParent
);
```



## <a name="parameters"></a><span data-ttu-id="e4f58-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4f58-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e4f58-111">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="e4f58-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e4f58-112">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="e4f58-112">Type: **HWND**</span></span>

<span data-ttu-id="e4f58-113">Um valor de **HWND** que identifica uma janela que será colocada em primeiro plano quando o logoff for concluído.</span><span class="sxs-lookup"><span data-stu-id="e4f58-113">An **HWND** value that identifies a window that will be brought into the foreground when the logoff is complete.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e4f58-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4f58-114">Return value</span></span>

<span data-ttu-id="e4f58-115">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="e4f58-115">Type: **HRESULT**</span></span>

<span data-ttu-id="e4f58-116">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="e4f58-116">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="e4f58-117">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e4f58-117">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4f58-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4f58-118">Requirements</span></span>



| <span data-ttu-id="e4f58-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4f58-119">Requirement</span></span> | <span data-ttu-id="e4f58-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e4f58-120">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e4f58-121">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4f58-121">Minimum supported client</span></span><br/> | <span data-ttu-id="e4f58-122">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4f58-122">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="e4f58-123">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="e4f58-123">Minimum supported server</span></span><br/> | <span data-ttu-id="e4f58-124">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="e4f58-124">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="e4f58-125">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="e4f58-125">End of client support</span></span><br/>    | <span data-ttu-id="e4f58-126">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="e4f58-126">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="e4f58-127">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="e4f58-127">End of server support</span></span><br/>    | <span data-ttu-id="e4f58-128">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="e4f58-128">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="e4f58-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4f58-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="e4f58-130"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="e4f58-130"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="e4f58-131">INSERI</span><span class="sxs-lookup"><span data-stu-id="e4f58-131">IDL</span></span><br/>                      | <dl> <span data-ttu-id="e4f58-132"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="e4f58-132"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="e4f58-133">DLL</span><span class="sxs-lookup"><span data-stu-id="e4f58-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="e4f58-134"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="e4f58-134"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4f58-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4f58-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4f58-136">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="e4f58-136">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="e4f58-137">**IUserIdentityManager:: logon**</span><span class="sxs-lookup"><span data-stu-id="e4f58-137">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="e4f58-138">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="e4f58-138">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




