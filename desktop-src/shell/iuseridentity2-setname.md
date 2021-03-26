---
description: 'IUserIdentity2:: SetName não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: 1c9c3beb-fa1c-4b4d-9cfd-656b97949036
title: 'Método IUserIdentity2:: SetName (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.SetName
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 0b0fd06ef4b582987e41c2343f2d4596db6b8528
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968022"
---
# <a name="iuseridentity2setname-method"></a><span data-ttu-id="56a23-104">Método IUserIdentity2:: SetName</span><span class="sxs-lookup"><span data-stu-id="56a23-104">IUserIdentity2::SetName method</span></span>

<span data-ttu-id="56a23-105">\[**IUserIdentity2:: SetName** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="56a23-105">\[**IUserIdentity2::SetName** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="56a23-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="56a23-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="56a23-107">Define o nome de exibição da identidade.</span><span class="sxs-lookup"><span data-stu-id="56a23-107">Sets the display name of the identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="56a23-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56a23-108">Syntax</span></span>


```C++
HRESULT SetName(
  [in] WCHAR *pszName
);
```



## <a name="parameters"></a><span data-ttu-id="56a23-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56a23-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56a23-110">*pszName* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="56a23-110">*pszName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56a23-111">Tipo: \**WCHAR \** _</span><span class="sxs-lookup"><span data-stu-id="56a23-111">Type: \**WCHAR\** _</span></span>

<span data-ttu-id="56a23-112">A cadeia de caracteres largos que contém o novo nome da identidade.</span><span class="sxs-lookup"><span data-stu-id="56a23-112">The wide-character string that contains the new name of the identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56a23-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56a23-113">Return value</span></span>

<span data-ttu-id="56a23-114">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="56a23-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="56a23-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="56a23-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="56a23-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="56a23-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="56a23-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="56a23-117">Requirements</span></span>



| <span data-ttu-id="56a23-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="56a23-118">Requirement</span></span> | <span data-ttu-id="56a23-119">Valor</span><span class="sxs-lookup"><span data-stu-id="56a23-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56a23-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56a23-120">Minimum supported client</span></span><br/> | <span data-ttu-id="56a23-121">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56a23-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="56a23-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="56a23-122">Minimum supported server</span></span><br/> | <span data-ttu-id="56a23-123">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="56a23-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="56a23-124">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="56a23-124">End of client support</span></span><br/>    | <span data-ttu-id="56a23-125">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="56a23-125">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="56a23-126">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="56a23-126">End of server support</span></span><br/>    | <span data-ttu-id="56a23-127">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="56a23-127">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="56a23-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="56a23-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="56a23-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="56a23-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="56a23-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="56a23-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="56a23-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="56a23-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="56a23-132">DLL</span><span class="sxs-lookup"><span data-stu-id="56a23-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56a23-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56a23-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="56a23-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="56a23-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56a23-135">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="56a23-135">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="56a23-136">**GetName**</span><span class="sxs-lookup"><span data-stu-id="56a23-136">**GetName**</span></span>](iuseridentity-getname.md)
</dt> </dl>

 

 




