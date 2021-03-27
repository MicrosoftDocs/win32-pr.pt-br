---
description: 'IUserIdentity:: GetName não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: 4db24dd2-d2b8-4a58-9c16-0e721bc195da
title: 'Método IUserIdentity:: GetName (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity.GetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 88c0a3d08ff917c2cc9fd59f15e4c23fc22fc79d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104967884"
---
# <a name="iuseridentitygetname-method"></a><span data-ttu-id="87970-104">Método IUserIdentity:: GetName</span><span class="sxs-lookup"><span data-stu-id="87970-104">IUserIdentity::GetName method</span></span>

<span data-ttu-id="87970-105">\[**IUserIdentity:: GetName** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="87970-105">\[**IUserIdentity::GetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="87970-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="87970-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="87970-107">Obtém o nome associado a esta identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="87970-107">Gets the name associated with this user identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="87970-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="87970-108">Syntax</span></span>


```C++
HRESULT GetName(
  [in] WCHAR *pszName,
  [in] ULONG ulBuffSize
);
```



## <a name="parameters"></a><span data-ttu-id="87970-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="87970-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="87970-110">*pszName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="87970-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87970-111">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="87970-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="87970-112">Um ponteiro para uma cadeia de caracteres largos que recebe o nome desta identidade de usuário.</span><span class="sxs-lookup"><span data-stu-id="87970-112">A pointer to a wide-character string that receives the name of this user identity.</span></span>

</dd> <dt>

<span data-ttu-id="87970-113">_ulBuffSize \* \[ in\]</span><span class="sxs-lookup"><span data-stu-id="87970-113">_ulBuffSize\* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="87970-114">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="87970-114">Type: **ULONG**</span></span>

<span data-ttu-id="87970-115">Um valor que especifica o tamanho de *pszName*.</span><span class="sxs-lookup"><span data-stu-id="87970-115">A value that specifies the size of *pszName*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="87970-116">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="87970-116">Return value</span></span>

<span data-ttu-id="87970-117">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="87970-117">Type: **HRESULT**</span></span>

<span data-ttu-id="87970-118">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="87970-118">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="87970-119">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="87970-119">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="87970-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="87970-120">Requirements</span></span>



| <span data-ttu-id="87970-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="87970-121">Requirement</span></span> | <span data-ttu-id="87970-122">Valor</span><span class="sxs-lookup"><span data-stu-id="87970-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="87970-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87970-123">Minimum supported client</span></span><br/> | <span data-ttu-id="87970-124">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="87970-124">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="87970-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="87970-125">Minimum supported server</span></span><br/> | <span data-ttu-id="87970-126">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="87970-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="87970-127">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="87970-127">End of client support</span></span><br/>    | <span data-ttu-id="87970-128">Windows XP</span><span class="sxs-lookup"><span data-stu-id="87970-128">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="87970-129">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="87970-129">End of server support</span></span><br/>    | <span data-ttu-id="87970-130">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="87970-130">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="87970-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="87970-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="87970-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="87970-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="87970-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="87970-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="87970-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="87970-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="87970-135">DLL</span><span class="sxs-lookup"><span data-stu-id="87970-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="87970-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="87970-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="87970-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="87970-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="87970-138">**IUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="87970-138">**IUserIdentity**</span></span>](iuseridentity.md)
</dt> <dt>

[<span data-ttu-id="87970-139">**SetName**</span><span class="sxs-lookup"><span data-stu-id="87970-139">**SetName**</span></span>](iuseridentity2-setname.md)
</dt> </dl>

 

 




