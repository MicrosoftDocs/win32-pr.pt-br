---
description: 'IUserIdentityManager:: não há suporte para logon e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: ba146ee1-6c9c-4f97-ae90-431aa084ea16
title: 'Método IUserIdentityManager:: logon (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.Logon
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eee6e0555d45d3f52173fce085d19c14f2ccfe8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104089711"
---
# <a name="iuseridentitymanagerlogon-method"></a><span data-ttu-id="bccb9-104">Método IUserIdentityManager:: logon</span><span class="sxs-lookup"><span data-stu-id="bccb9-104">IUserIdentityManager::Logon method</span></span>

<span data-ttu-id="bccb9-105">\[**IUserIdentityManager::** não há suporte para logon e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="bccb9-105">\[**IUserIdentityManager::Logon** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="bccb9-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="bccb9-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="bccb9-107">Exibe uma IU para o usuário, permitindo que o usuário escolha uma identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="bccb9-107">Displays a UI to the user, allowing the user to choose a user identity.</span></span> <span data-ttu-id="bccb9-108">Se for bem-sucedido, a identidade do usuário será registrada e recuperada.</span><span class="sxs-lookup"><span data-stu-id="bccb9-108">If successful, the user identity will be logged on and retrieved.</span></span>

## <a name="syntax"></a><span data-ttu-id="bccb9-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bccb9-109">Syntax</span></span>


```C++
HRESULT Logon(
  [in]  HWND          hwndParent,
  [in]  DWORD         dwFlags,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="bccb9-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bccb9-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bccb9-111">*hwndParent* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bccb9-111">*hwndParent* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bccb9-112">Tipo: **HWND**</span><span class="sxs-lookup"><span data-stu-id="bccb9-112">Type: **HWND**</span></span>

<span data-ttu-id="bccb9-113">Um valor de **HWND** que identifica uma janela que será colocada em primeiro plano depois que a interface do usuário de logon for ignorada.</span><span class="sxs-lookup"><span data-stu-id="bccb9-113">An **HWND** value that identifies a window that will be brought to the foreground after the logon UI is dismissed.</span></span>

</dd> <dt>

<span data-ttu-id="bccb9-114">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="bccb9-114">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="bccb9-115">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="bccb9-115">Type: **DWORD**</span></span>

<span data-ttu-id="bccb9-116">Sinalizadores opcionais para definir como o comportamento da interface do usuário se comportará.</span><span class="sxs-lookup"><span data-stu-id="bccb9-116">Optional flags to define how the UI will behave.</span></span> <span data-ttu-id="bccb9-117">Defina como UIL \_ forçar \_ a interface do usuário para forçar a exibição da interface do usuário, mesmo que uma identidade já tenha sido escolhida.</span><span class="sxs-lookup"><span data-stu-id="bccb9-117">Set to UIL\_FORCE\_UI to force the UI to display, even if an identity has already been chosen.</span></span>

</dd> <dt>

<span data-ttu-id="bccb9-118">*ppIdentity* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="bccb9-118">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="bccb9-119">Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="bccb9-119">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="bccb9-120">O endereço do ponteiro que recebe a identidade do usuário escolhida.</span><span class="sxs-lookup"><span data-stu-id="bccb9-120">The address of the pointer that receives the chosen user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bccb9-121">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bccb9-121">Return value</span></span>

<span data-ttu-id="bccb9-122">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bccb9-122">Type: **HRESULT**</span></span>

<span data-ttu-id="bccb9-123">Resultado da operação de logon.</span><span class="sxs-lookup"><span data-stu-id="bccb9-123">Result of the logon operation.</span></span> <span data-ttu-id="bccb9-124">Se for bem-sucedido, retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="bccb9-124">If successful, it returns S\_OK.</span></span> <span data-ttu-id="bccb9-125">Caso contrário, ele retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="bccb9-125">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="bccb9-126">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bccb9-126">Return code</span></span>                                                                                            | <span data-ttu-id="bccb9-127">Description</span><span class="sxs-lookup"><span data-stu-id="bccb9-127">Description</span></span>                                                                                 |
|--------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="bccb9-128"><dt>**E \_ usuário \_ cancelados**</dt></span><span class="sxs-lookup"><span data-stu-id="bccb9-128"><dt>**E\_USER\_CANCELLED**</dt></span></span> </dl>      | <span data-ttu-id="bccb9-129">O usuário cancelou a operação de logon da IU.</span><span class="sxs-lookup"><span data-stu-id="bccb9-129">The user canceled the logon operation from the UI.</span></span><br/>                               |
| <dl> <span data-ttu-id="bccb9-130"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="bccb9-130"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>          | <span data-ttu-id="bccb9-131">Não foi possível criar a identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="bccb9-131">The user identity could not be created.</span></span><br/>                                          |
| <dl> <span data-ttu-id="bccb9-132"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="bccb9-132"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>           | <span data-ttu-id="bccb9-133">A operação falhou inesperadamente.</span><span class="sxs-lookup"><span data-stu-id="bccb9-133">The operation failed unexpectedly.</span></span><br/>                                               |
| <dl> <span data-ttu-id="bccb9-134"><dt>**\_identidades E \_ desabilitadas**</dt></span><span class="sxs-lookup"><span data-stu-id="bccb9-134"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="bccb9-135">O gerenciamento de identidades está desabilitado no sistema.</span><span class="sxs-lookup"><span data-stu-id="bccb9-135">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bccb9-136"><dt>**S \_ identidades \_ desabilitadas**</dt></span><span class="sxs-lookup"><span data-stu-id="bccb9-136"><dt>**S\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="bccb9-137">O gerenciamento de identidades está desabilitado no sistema.</span><span class="sxs-lookup"><span data-stu-id="bccb9-137">Identity management is disabled on the system.</span></span><br/>                                   |
| <dl> <span data-ttu-id="bccb9-138"><dt>**\_alteração de identidade E \_**</dt></span><span class="sxs-lookup"><span data-stu-id="bccb9-138"><dt>**E\_IDENTITY\_CHANGING**</dt></span></span> </dl>   | <span data-ttu-id="bccb9-139">O sistema está atualmente alternando identidades e não pode concluir a operação.</span><span class="sxs-lookup"><span data-stu-id="bccb9-139">The system is currently switching identities, and cannot complete the operation.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="bccb9-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bccb9-140">Requirements</span></span>



| <span data-ttu-id="bccb9-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="bccb9-141">Requirement</span></span> | <span data-ttu-id="bccb9-142">Valor</span><span class="sxs-lookup"><span data-stu-id="bccb9-142">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bccb9-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bccb9-143">Minimum supported client</span></span><br/> | <span data-ttu-id="bccb9-144">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bccb9-144">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="bccb9-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="bccb9-145">Minimum supported server</span></span><br/> | <span data-ttu-id="bccb9-146">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="bccb9-146">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="bccb9-147">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="bccb9-147">End of client support</span></span><br/>    | <span data-ttu-id="bccb9-148">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="bccb9-148">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="bccb9-149">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="bccb9-149">End of server support</span></span><br/>    | <span data-ttu-id="bccb9-150">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="bccb9-150">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="bccb9-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bccb9-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="bccb9-152"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="bccb9-152"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="bccb9-153">INSERI</span><span class="sxs-lookup"><span data-stu-id="bccb9-153">IDL</span></span><br/>                      | <dl> <span data-ttu-id="bccb9-154"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="bccb9-154"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="bccb9-155">DLL</span><span class="sxs-lookup"><span data-stu-id="bccb9-155">DLL</span></span><br/>                      | <dl> <span data-ttu-id="bccb9-156"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="bccb9-156"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bccb9-157">Confira também</span><span class="sxs-lookup"><span data-stu-id="bccb9-157">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bccb9-158">**IUserIdentityManager**</span><span class="sxs-lookup"><span data-stu-id="bccb9-158">**IUserIdentityManager**</span></span>](iuseridentitymanager.md)
</dt> <dt>

[<span data-ttu-id="bccb9-159">**IUserIdentityManager:: fazer logoff**</span><span class="sxs-lookup"><span data-stu-id="bccb9-159">**IUserIdentityManager::Logoff**</span></span>](iuseridentitymanager-logoff.md)
</dt> <dt>

[<span data-ttu-id="bccb9-160">**IUserIdentityManager::ManageIdentities**</span><span class="sxs-lookup"><span data-stu-id="bccb9-160">**IUserIdentityManager::ManageIdentities**</span></span>](iuseridentitymanager-manageidentities.md)
</dt> </dl>

 

 




