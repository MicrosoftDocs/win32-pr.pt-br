---
description: GetIdentityByCookie não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: c2f549ac-e13d-4198-864f-7f5fbec30c72
title: 'Método IUserIdentityManager:: GetIdentityByCookie (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentityManager.GetIdentityByCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: eb4e5ad5bda349a5b1650b090abc44a9fd1e6332
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501147"
---
# <a name="iuseridentitymanagergetidentitybycookie-method"></a><span data-ttu-id="ad173-104">Método IUserIdentityManager:: GetIdentityByCookie</span><span class="sxs-lookup"><span data-stu-id="ad173-104">IUserIdentityManager::GetIdentityByCookie method</span></span>

<span data-ttu-id="ad173-105">\[**GetIdentityByCookie** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="ad173-105">\[**GetIdentityByCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="ad173-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="ad173-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="ad173-107">Obtém uma identidade de usuário específica pelo cookie usado para identificá-la exclusivamente.</span><span class="sxs-lookup"><span data-stu-id="ad173-107">Gets a specific user identity by the cookie used to uniquely identify it.</span></span>

## <a name="syntax"></a><span data-ttu-id="ad173-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ad173-108">Syntax</span></span>


```C++
HRESULT GetIdentityByCookie(
  [in]  GUID          *uidCookie,
  [out] IUserIdentity **ppIdentity
);
```



## <a name="parameters"></a><span data-ttu-id="ad173-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ad173-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ad173-110">*uidCookie* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="ad173-110">*uidCookie* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ad173-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="ad173-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="ad173-112">O endereço de um valor _ *GUID*\* que representa o cookie para a identidade que você deseja recuperar.</span><span class="sxs-lookup"><span data-stu-id="ad173-112">The address of a _ *GUID*\* value that represents the cookie for the identity you want to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="ad173-113">*ppIdentity* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="ad173-113">*ppIdentity* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ad173-114">Tipo: **[ **IUserIdentity**](iuseridentity.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="ad173-114">Type: **[**IUserIdentity**](iuseridentity.md)\*\***</span></span>

<span data-ttu-id="ad173-115">O endereço do ponteiro que receberá o objeto de identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="ad173-115">The address of the pointer that will receive the user identity object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ad173-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ad173-116">Return value</span></span>

<span data-ttu-id="ad173-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ad173-117">Type: **HRESULT**</span></span>

<span data-ttu-id="ad173-118">O resultado da solicitação de recuperação.</span><span class="sxs-lookup"><span data-stu-id="ad173-118">The result of the retrieval request.</span></span> <span data-ttu-id="ad173-119">Se for bem-sucedido, retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ad173-119">If successful, it returns S\_OK.</span></span> <span data-ttu-id="ad173-120">Caso contrário, ele retornará um dos seguintes códigos de erro.</span><span class="sxs-lookup"><span data-stu-id="ad173-120">Otherwise it will return one of the following error codes.</span></span>



| <span data-ttu-id="ad173-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="ad173-121">Return code</span></span>                                                                                            | <span data-ttu-id="ad173-122">Description</span><span class="sxs-lookup"><span data-stu-id="ad173-122">Description</span></span>                                               |
|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <dl> <span data-ttu-id="ad173-123"><dt>**\_identidade E \_ não \_ encontrada**</dt></span><span class="sxs-lookup"><span data-stu-id="ad173-123"><dt>**E\_IDENTITY\_NOT\_FOUND**</dt></span></span> </dl> | <span data-ttu-id="ad173-124">Não foi possível encontrar a identidade solicitada.</span><span class="sxs-lookup"><span data-stu-id="ad173-124">The identity requested could not be found.</span></span><br/>     |
| <dl> <span data-ttu-id="ad173-125"><dt>**\_identidades E \_ desabilitadas**</dt></span><span class="sxs-lookup"><span data-stu-id="ad173-125"><dt>**E\_IDENTITIES\_DISABLED**</dt></span></span> </dl> | <span data-ttu-id="ad173-126">O gerenciamento de identidades está desabilitado no sistema.</span><span class="sxs-lookup"><span data-stu-id="ad173-126">Identity management is disabled on the system.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="ad173-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ad173-127">Requirements</span></span>



| <span data-ttu-id="ad173-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="ad173-128">Requirement</span></span> | <span data-ttu-id="ad173-129">Valor</span><span class="sxs-lookup"><span data-stu-id="ad173-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ad173-130">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad173-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ad173-131">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ad173-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ad173-132">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="ad173-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ad173-133">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="ad173-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ad173-134">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="ad173-134">End of client support</span></span><br/>    | <span data-ttu-id="ad173-135">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="ad173-135">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="ad173-136">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="ad173-136">End of server support</span></span><br/>    | <span data-ttu-id="ad173-137">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="ad173-137">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="ad173-138">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ad173-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="ad173-139"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="ad173-139"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="ad173-140">INSERI</span><span class="sxs-lookup"><span data-stu-id="ad173-140">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ad173-141"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="ad173-141"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="ad173-142">DLL</span><span class="sxs-lookup"><span data-stu-id="ad173-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ad173-143"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ad173-143"><dt>Msident.dll</dt></span></span> </dl> |



 

 




