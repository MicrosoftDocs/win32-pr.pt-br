---
description: 'IUserIdentityManager:: ManageIdentities não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: 9a5a85bd-d007-4247-859b-e402ed290785
title: 'Método IUserIdentityManager:: ManageIdentities (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.ManageIdentities
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: b5b782a56324faf19dd1527d2cd363d26f0e337c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296136"
---
# <a name="iuseridentitymanagermanageidentities-method"></a><span data-ttu-id="002f5-104">Método IUserIdentityManager:: ManageIdentities</span><span class="sxs-lookup"><span data-stu-id="002f5-104">IUserIdentityManager::ManageIdentities method</span></span>

<span data-ttu-id="002f5-105">\[**IUserIdentityManager:: ManageIdentities** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="002f5-105">\[**IUserIdentityManager::ManageIdentities** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="002f5-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="002f5-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="002f5-107">Exibe uma IU para o usuário, permitindo que o usuário gerencie identidades de usuário.</span><span class="sxs-lookup"><span data-stu-id="002f5-107">Displays a UI to the user, allowing the user to manage user identities.</span></span>

## <a name="syntax"></a><span data-ttu-id="002f5-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="002f5-108">Syntax</span></span>


```C++
HRESULT ManageIdentities(
  [in] HWND  hwndParent,
  [in] DWORD dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="002f5-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="002f5-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="002f5-110">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="002f5-110">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002f5-111">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="002f5-111">Type: **HWND**</span></span>

<span data-ttu-id="002f5-112">Um valor de **HWND** que identifica uma janela que será colocada em primeiro plano depois que a interface do usuário for ignorada.</span><span class="sxs-lookup"><span data-stu-id="002f5-112">An **HWND** value that identifies a window that will be brought to the foreground after the UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="002f5-113">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="002f5-113">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="002f5-114">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="002f5-114">Type: **DWORD**</span></span>

<span data-ttu-id="002f5-115">Sinalizadores opcionais para definir como o comportamento da interface do usuário se comportará.</span><span class="sxs-lookup"><span data-stu-id="002f5-115">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="002f5-116">Defina como UIMI \_ criar \_ nova \_ identidade para solicitar que o usuário crie uma nova identidade.</span><span class="sxs-lookup"><span data-stu-id="002f5-116">Set to UIMI\_CREATE\_NEW\_IDENTITY to prompt the user to create a new identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="002f5-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="002f5-117">Return value</span></span>

<span data-ttu-id="002f5-118">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="002f5-118">Type: **HRESULT**</span></span>

<span data-ttu-id="002f5-119">O resultado da operação de gerenciamento.</span><span class="sxs-lookup"><span data-stu-id="002f5-119">The result of the management operation.</span></span> <span data-ttu-id="002f5-120">Se for bem-sucedido, retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="002f5-120">If successful, it returns S\_OK.</span></span> <span data-ttu-id="002f5-121">Caso contrário, ele retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="002f5-121">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="002f5-122">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="002f5-122">Return code</span></span>                                                                                            | <span data-ttu-id="002f5-123">Description</span><span class="sxs-lookup"><span data-stu-id="002f5-123">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="002f5-124"><dt>**\_identidades E \_ desabilitadas**</dt></span><span class="sxs-lookup"><span data-stu-id="002f5-124"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="002f5-125">O gerenciamento de identidades está desabilitado no sistema.</span><span class="sxs-lookup"><span data-stu-id="002f5-125">Identity management is disabled on the system.</span></span><br/> |
| <dl> <span data-ttu-id="002f5-126"><dt>**E \_ usuário \_ cancelados**</dt></span><span class="sxs-lookup"><span data-stu-id="002f5-126"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="002f5-127">O usuário cancelou a caixa de diálogo.</span><span class="sxs-lookup"><span data-stu-id="002f5-127">The user canceled the dialog.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="002f5-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="002f5-128">Requirements</span></span>



| <span data-ttu-id="002f5-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="002f5-129">Requirement</span></span> | <span data-ttu-id="002f5-130">Valor</span><span class="sxs-lookup"><span data-stu-id="002f5-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="002f5-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="002f5-131">Minimum supported client</span></span><br/> | <span data-ttu-id="002f5-132">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="002f5-132">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="002f5-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="002f5-133">Minimum supported server</span></span><br/> | <span data-ttu-id="002f5-134">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="002f5-134">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="002f5-135">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="002f5-135">End of client support</span></span><br/>    | <span data-ttu-id="002f5-136">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="002f5-136">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="002f5-137">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="002f5-137">End of server support</span></span><br/>    | <span data-ttu-id="002f5-138">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="002f5-138">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="002f5-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="002f5-139">Header</span></span><br/>                   | <dl> <span data-ttu-id="002f5-140"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="002f5-140"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="002f5-141">INSERI</span><span class="sxs-lookup"><span data-stu-id="002f5-141">IDL</span></span><br/>                      | <dl> <span data-ttu-id="002f5-142"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="002f5-142"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="002f5-143">DLL</span><span class="sxs-lookup"><span data-stu-id="002f5-143">DLL</span></span><br/>                      | <dl> <span data-ttu-id="002f5-144"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="002f5-144"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="002f5-145">Confira também</span><span class="sxs-lookup"><span data-stu-id="002f5-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="002f5-146">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="002f5-146">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="002f5-147">**IUserIdentityManager:: logon**</span><span class="sxs-lookup"><span data-stu-id="002f5-147">**IUserIdentityManager::Logon**</span></span>](iuseridentitymanager-logon.md)
</dt> <dt>

[<span data-ttu-id="002f5-148">**IUserIdentityManager:: fazer logoff**</span><span class="sxs-lookup"><span data-stu-id="002f5-148">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> </dl>

 

 




