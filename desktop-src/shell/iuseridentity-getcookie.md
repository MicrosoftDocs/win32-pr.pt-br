---
description: O GetCookie não tem suporte e pode ser alterado ou não estar disponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 4a743d64-9af3-43cf-9a9f-d808676ab337
title: 'Método IUserIdentity:: GetCookie (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetCookie
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 96cafb13f2c90c41e4aa6dcaaa72cf052757d0ad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967491"
---
# <a name="iuseridentitygetcookie-method"></a><span data-ttu-id="7046d-104">Método IUserIdentity:: GetCookie</span><span class="sxs-lookup"><span data-stu-id="7046d-104">IUserIdentity::GetCookie method</span></span>

<span data-ttu-id="7046d-105">\[O **GetCookie** não tem suporte e pode ser alterado ou não estar disponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="7046d-105">\[**GetCookie** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="7046d-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="7046d-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="7046d-107">Obtém o cookie usado para identificar exclusivamente essa identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="7046d-107">Gets the cookie used to uniquely identify this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="7046d-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7046d-108">Syntax</span></span>


```C++
HRESULT GetCookie(
  [out] GUID *puidCookie
);
```



## <a name="parameters"></a><span data-ttu-id="7046d-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7046d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7046d-110">*puidCookie* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="7046d-110">*puidCookie* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7046d-111">Tipo: \**GUID \** _</span><span class="sxs-lookup"><span data-stu-id="7046d-111">Type: \**GUID\** _</span></span>

<span data-ttu-id="7046d-112">Um ponteiro para um valor _ *GUID*\* que recebe o cookie usado para identificar exclusivamente essa identidade do usuário.</span><span class="sxs-lookup"><span data-stu-id="7046d-112">A pointer to a _ *GUID*\* value that receives the cookie used to uniquely identify this user identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7046d-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7046d-113">Return value</span></span>

<span data-ttu-id="7046d-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="7046d-114">Type: **HRESULT**</span></span>

<span data-ttu-id="7046d-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="7046d-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="7046d-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7046d-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="7046d-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7046d-117">Requirements</span></span>



| <span data-ttu-id="7046d-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="7046d-118">Requirement</span></span> | <span data-ttu-id="7046d-119">Valor</span><span class="sxs-lookup"><span data-stu-id="7046d-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="7046d-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7046d-120">Minimum supported client</span></span><br/> | <span data-ttu-id="7046d-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7046d-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="7046d-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7046d-122">Minimum supported server</span></span><br/> | <span data-ttu-id="7046d-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="7046d-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="7046d-124">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="7046d-124">End of client support</span></span><br/>    | <span data-ttu-id="7046d-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="7046d-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="7046d-126">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="7046d-126">End of server support</span></span><br/>    | <span data-ttu-id="7046d-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="7046d-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="7046d-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7046d-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="7046d-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="7046d-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="7046d-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="7046d-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="7046d-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="7046d-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="7046d-132">DLL</span><span class="sxs-lookup"><span data-stu-id="7046d-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7046d-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7046d-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7046d-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="7046d-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7046d-135">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="7046d-135">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="7046d-136">**GetOrdinal**</span><span class="sxs-lookup"><span data-stu-id="7046d-136">**GetOrdinal**</span></span>](iuseridentity2-getordinal.md)
</dt> </dl>

 

 




