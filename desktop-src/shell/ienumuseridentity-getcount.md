---
description: GetCount não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.
ms.assetid: 1fe39f2d-f95e-4436-a780-40fe8bd41b74
title: 'Método IEnumUserIdentity:: GetCount (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.GetCount
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 43355a9585fc4099c8649f7df506ff3495a53944
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104296726"
---
# <a name="ienumuseridentitygetcount-method"></a><span data-ttu-id="1fa9b-104">Método IEnumUserIdentity:: GetCount</span><span class="sxs-lookup"><span data-stu-id="1fa9b-104">IEnumUserIdentity::GetCount method</span></span>

<span data-ttu-id="1fa9b-105">\[**GetCount** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="1fa9b-105">\[**GetCount** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="1fa9b-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="1fa9b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="1fa9b-107">Obtém a contagem de identidades de usuário atualmente no sistema.</span><span class="sxs-lookup"><span data-stu-id="1fa9b-107">Gets the count of user identities currently on the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fa9b-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1fa9b-108">Syntax</span></span>


```C++
HRESULT GetCount(
  [out] ULONG *pnCount
);
```



## <a name="parameters"></a><span data-ttu-id="1fa9b-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1fa9b-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1fa9b-110">*pnCount* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="1fa9b-110">*pnCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1fa9b-111">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="1fa9b-111">Type: \**ULONG\** _</span></span>

<span data-ttu-id="1fa9b-112">Ponteiro para um _ *ULONG*\* que recebe a contagem.</span><span class="sxs-lookup"><span data-stu-id="1fa9b-112">Pointer to a _ *ULONG*\* that receives the count.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1fa9b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1fa9b-113">Return value</span></span>

<span data-ttu-id="1fa9b-114">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="1fa9b-114">Type: **HRESULT**</span></span>

<span data-ttu-id="1fa9b-115">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="1fa9b-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="1fa9b-116">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1fa9b-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="1fa9b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="1fa9b-117">Remarks</span></span>

<span data-ttu-id="1fa9b-118">Se o suporte para várias identidades de usuário estiver desabilitado, o *pnCount* receberá um valor de 1.</span><span class="sxs-lookup"><span data-stu-id="1fa9b-118">If support for multiple user identities is disabled, *pnCount* will receive a value of 1.</span></span>

## <a name="requirements"></a><span data-ttu-id="1fa9b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1fa9b-119">Requirements</span></span>



| <span data-ttu-id="1fa9b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1fa9b-120">Requirement</span></span> | <span data-ttu-id="1fa9b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1fa9b-121">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="1fa9b-122">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fa9b-122">Minimum supported client</span></span><br/> | <span data-ttu-id="1fa9b-123">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="1fa9b-123">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="1fa9b-124">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="1fa9b-124">Minimum supported server</span></span><br/> | <span data-ttu-id="1fa9b-125">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="1fa9b-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="1fa9b-126">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="1fa9b-126">End of client support</span></span><br/>    | <span data-ttu-id="1fa9b-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="1fa9b-127">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="1fa9b-128">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="1fa9b-128">End of server support</span></span><br/>    | <span data-ttu-id="1fa9b-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="1fa9b-129">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="1fa9b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1fa9b-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="1fa9b-131"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="1fa9b-131"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="1fa9b-132">INSERI</span><span class="sxs-lookup"><span data-stu-id="1fa9b-132">IDL</span></span><br/>                      | <dl> <span data-ttu-id="1fa9b-133"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="1fa9b-133"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="1fa9b-134">DLL</span><span class="sxs-lookup"><span data-stu-id="1fa9b-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="1fa9b-135"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="1fa9b-135"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1fa9b-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="1fa9b-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1fa9b-137">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="1fa9b-137">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="1fa9b-138">**IEnumUserIdentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="1fa9b-138">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="1fa9b-139">**IEnumUserIdentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="1fa9b-139">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="1fa9b-140">**IEnumUserIdentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="1fa9b-140">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




