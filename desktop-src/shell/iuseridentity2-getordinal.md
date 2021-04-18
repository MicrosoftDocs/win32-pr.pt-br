---
description: Não há suporte para GetOrdinal e ele pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 20b1c1d0-b09f-43a8-9026-9cdbac28c108
title: 'Método IUserIdentity2:: GetOrdinal (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IUserIdentity2.GetOrdinal
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: f5a7e875e92342363722858b3ac714171cb547b6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104968024"
---
# <a name="iuseridentity2getordinal-method"></a><span data-ttu-id="1e031-104">Método IUserIdentity2:: GetOrdinal</span><span class="sxs-lookup"><span data-stu-id="1e031-104">IUserIdentity2::GetOrdinal method</span></span>

<span data-ttu-id="1e031-105">\[Não há suporte para **GetOrdinal** e ele pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="1e031-105">\[**GetOrdinal** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="1e031-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="1e031-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="1e031-107">Obtém o número ordinal desta identidade.</span><span class="sxs-lookup"><span data-stu-id="1e031-107">Gets the ordinal number for this identity.</span></span>

## <a name="syntax"></a><span data-ttu-id="1e031-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1e031-108">Syntax</span></span>


```C++
HRESULT GetOrdinal(
  [out] DWORD *dwOrdinal
);
```



## <a name="parameters"></a><span data-ttu-id="1e031-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1e031-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1e031-110">*dwOrdinal* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1e031-110">*dwOrdinal* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1e031-111">Tipo: \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="1e031-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="1e031-112">Um ponteiro para um valor _ *DWORD*\* que recebe o número ordinal para essa identidade.</span><span class="sxs-lookup"><span data-stu-id="1e031-112">A pointer to a _ *DWORD*\* value that receives the ordinal number for this identity.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1e031-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1e031-113">Return value</span></span>

<span data-ttu-id="1e031-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1e031-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1e031-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1e031-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1e031-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1e031-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1e031-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1e031-117">Remarks</span></span>

<span data-ttu-id="1e031-118">O ordinal determina a ordem das identidades na lista de identidades, mas pode não persistir em operações nas identidades.</span><span class="sxs-lookup"><span data-stu-id="1e031-118">The ordinal determines the order of the identities in the identity list, but may not persist throughout operations on the identities.</span></span> <span data-ttu-id="1e031-119">Para obter um valor exclusivo para uma identidade, chame [**GetCookie**](iuseridentity-getcookie.md).</span><span class="sxs-lookup"><span data-stu-id="1e031-119">To get a unique value for an identity, call [**GetCookie**](iuseridentity-getcookie.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1e031-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1e031-120">Requirements</span></span>



| <span data-ttu-id="1e031-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="1e031-121">Requirement</span></span> | <span data-ttu-id="1e031-122">Valor</span><span class="sxs-lookup"><span data-stu-id="1e031-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1e031-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e031-123">Minimum supported client</span></span><br/> | <span data-ttu-id="1e031-124">Windows 2000 Professional \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1e031-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="1e031-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1e031-125">Minimum supported server</span></span><br/> | <span data-ttu-id="1e031-126">Windows 2000 Server \[somente aplicativos da área de trabalho\]</span><span class="sxs-lookup"><span data-stu-id="1e031-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1e031-127">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1e031-127">End of client support</span></span><br/>    | <span data-ttu-id="1e031-128">Windows 2000 Professional</span><span class="sxs-lookup"><span data-stu-id="1e031-128">Windows 2000 Professional</span></span><br/>                                                   |
| <span data-ttu-id="1e031-129">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1e031-129">End of server support</span></span><br/>    | <span data-ttu-id="1e031-130">Windows 2000 Server</span><span class="sxs-lookup"><span data-stu-id="1e031-130">Windows 2000 Server</span></span><br/>                                                         |
| <span data-ttu-id="1e031-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1e031-131">Header</span></span><br/>                   | <dl> <span data-ttu-id="1e031-132"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="1e031-132"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="1e031-133">INSERI</span><span class="sxs-lookup"><span data-stu-id="1e031-133">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1e031-134"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1e031-134"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="1e031-135">DLL</span><span class="sxs-lookup"><span data-stu-id="1e031-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1e031-136"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1e031-136"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1e031-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="1e031-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1e031-138">**IUserIdentity2**</span><span class="sxs-lookup"><span data-stu-id="1e031-138">**IUserIdentity2**</span></span>](iuseridentity2.md)
</dt> <dt>

[<span data-ttu-id="1e031-139">**GetCookie**</span><span class="sxs-lookup"><span data-stu-id="1e031-139">**GetCookie**</span></span>](iuseridentity-getcookie.md)
</dt> </dl>

 

 




