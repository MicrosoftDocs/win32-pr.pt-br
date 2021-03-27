---
description: GetIdentityFolder não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: cd3370a2-b393-4cb9-ad9c-a46086987aaa
title: 'Método IUserIdentity:: GetIdentityFolder (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetIdentityFolder
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 9f2644570bb7ccc2ae5bee8a37d4471ffb65861a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967488"
---
# <a name="iuseridentitygetidentityfolder-method"></a><span data-ttu-id="72b0f-104">Método IUserIdentity:: GetIdentityFolder</span><span class="sxs-lookup"><span data-stu-id="72b0f-104">IUserIdentity::GetIdentityFolder method</span></span>

<span data-ttu-id="72b0f-105">\[**GetIdentityFolder** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="72b0f-105">\[**GetIdentityFolder** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="72b0f-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="72b0f-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="72b0f-107">Obtém a pasta de arquivos associada a essa identidade.</span><span class="sxs-lookup"><span data-stu-id="72b0f-107">Gets the file folder associated with this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="72b0f-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72b0f-108">Syntax</span></span>


```C++
HRESULT GetIdentityFolder(
  [in] DWORD dwFlags,
  [in] WCHAR *pszPath,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="72b0f-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="72b0f-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="72b0f-110">*dwFlags* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72b0f-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b0f-111">Tipo: **DWORD**</span><span class="sxs-lookup"><span data-stu-id="72b0f-111">Type: **DWORD**</span></span>

<span data-ttu-id="72b0f-112">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="72b0f-112">Required.</span></span> <span data-ttu-id="72b0f-113">Um valor que especifica se a pasta associada a essa identidade está em roaming.</span><span class="sxs-lookup"><span data-stu-id="72b0f-113">A value that specifies whether the folder associated with this identity is roaming.</span></span> <span data-ttu-id="72b0f-114">Deve ser um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="72b0f-114">Must be one of the following values.</span></span>

<dt>



 <span data-ttu-id="72b0f-115">(GIF \_ pasta de ROAMing \_ )</span><span class="sxs-lookup"><span data-stu-id="72b0f-115">(GIF\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="72b0f-116">A pasta está em roaming.</span><span class="sxs-lookup"><span data-stu-id="72b0f-116">The folder is roaming.</span></span>

</dd> <dt>



 <span data-ttu-id="72b0f-117">(GIF \_ \_pasta não móvel \_ )</span><span class="sxs-lookup"><span data-stu-id="72b0f-117">(GIF\_NON\_ROAMING\_FOLDER)</span></span>


</dt> <dd>

<span data-ttu-id="72b0f-118">A pasta é local.</span><span class="sxs-lookup"><span data-stu-id="72b0f-118">The folder is local.</span></span>

</dd> </dl> </dd> <dt>

<span data-ttu-id="72b0f-119">*pszPath* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="72b0f-119">*pszPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b0f-120">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="72b0f-120">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="72b0f-121">Um ponteiro para uma cadeia de caracteres largos que recebe o caminho da pasta.</span><span class="sxs-lookup"><span data-stu-id="72b0f-121">A pointer to a wide-character string that receives the folder path.</span></span>

</dd> <dt>

<span data-ttu-id="72b0f-122">_ulBuffSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="72b0f-122">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="72b0f-123">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="72b0f-123">Type: **ULONG**</span></span>

<span data-ttu-id="72b0f-124">Um valor que especifica o tamanho de *pszPath*.</span><span class="sxs-lookup"><span data-stu-id="72b0f-124">A value that specifies the size of *pszPath*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="72b0f-125">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="72b0f-125">Return value</span></span>

<span data-ttu-id="72b0f-126">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="72b0f-126">Type: **HRESULT**</span></span>

<span data-ttu-id="72b0f-127">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="72b0f-127">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="72b0f-128">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="72b0f-128">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="72b0f-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72b0f-129">Requirements</span></span>



| <span data-ttu-id="72b0f-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="72b0f-130">Requirement</span></span> | <span data-ttu-id="72b0f-131">Valor</span><span class="sxs-lookup"><span data-stu-id="72b0f-131">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="72b0f-132">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72b0f-132">Minimum supported client</span></span><br/> | <span data-ttu-id="72b0f-133">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="72b0f-133">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="72b0f-134">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="72b0f-134">Minimum supported server</span></span><br/> | <span data-ttu-id="72b0f-135">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="72b0f-135">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="72b0f-136">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="72b0f-136">End of client support</span></span><br/>    | <span data-ttu-id="72b0f-137">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="72b0f-137">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="72b0f-138">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="72b0f-138">End of server support</span></span><br/>    | <span data-ttu-id="72b0f-139">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="72b0f-139">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="72b0f-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72b0f-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="72b0f-141"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="72b0f-141"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="72b0f-142">INSERI</span><span class="sxs-lookup"><span data-stu-id="72b0f-142">IDL</span></span><br/>                      | <dl> <span data-ttu-id="72b0f-143"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="72b0f-143"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="72b0f-144">DLL</span><span class="sxs-lookup"><span data-stu-id="72b0f-144">DLL</span></span><br/>                      | <dl> <span data-ttu-id="72b0f-145"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="72b0f-145"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72b0f-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="72b0f-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72b0f-147">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="72b0f-147">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="72b0f-148">**IUserIdentity::OpenIdentityRegKey**</span><span class="sxs-lookup"><span data-stu-id="72b0f-148">**IUserIdentity::OpenIdentityRegKey**</span></span>](iuseridentity-openidentityregkey.md)
</dt> </dl>

 

 




