---
description: Redefine a contagem interna de interfaces recuperadas na enumeração.
ms.assetid: fd79b4be-cc0c-49b3-9874-384858e21ecf
title: 'Método IEnumUserIdentity:: Reset (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Reset
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 05b3c5d38575fa1b2957c28070d642ad15f846ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169422"
---
# <a name="ienumuseridentityreset-method"></a><span data-ttu-id="575f2-103">Método IEnumUserIdentity:: Reset</span><span class="sxs-lookup"><span data-stu-id="575f2-103">IEnumUserIdentity::Reset method</span></span>

<span data-ttu-id="575f2-104">\[**IEnumUserIdentity:: Reset** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="575f2-104">\[**IEnumUserIdentity::Reset** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="575f2-105">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="575f2-105">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="575f2-106">Redefine a contagem interna de interfaces recuperadas na enumeração.</span><span class="sxs-lookup"><span data-stu-id="575f2-106">Resets the internal count of retrieved interfaces in the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="575f2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="575f2-107">Syntax</span></span>


```C++
HRESULT Reset();
```



## <a name="parameters"></a><span data-ttu-id="575f2-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="575f2-108">Parameters</span></span>

<span data-ttu-id="575f2-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="575f2-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="575f2-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="575f2-110">Return value</span></span>

<span data-ttu-id="575f2-111">Tipo: **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="575f2-111">Type: **HRESULT**</span></span>

<span data-ttu-id="575f2-112">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="575f2-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="575f2-113">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="575f2-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="575f2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="575f2-114">Remarks</span></span>

<span data-ttu-id="575f2-115">[**IEnumUserIdentity**](ienumuseridentity.md) mantém uma contagem interna que especifica qual interface está próxima de ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="575f2-115">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="575f2-116">Chamar esse método irá redefinir o valor dessa contagem.</span><span class="sxs-lookup"><span data-stu-id="575f2-116">Calling this method will reset the value of this count.</span></span>

## <a name="requirements"></a><span data-ttu-id="575f2-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="575f2-117">Requirements</span></span>



| <span data-ttu-id="575f2-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="575f2-118">Requirement</span></span> | <span data-ttu-id="575f2-119">Valor</span><span class="sxs-lookup"><span data-stu-id="575f2-119">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="575f2-120">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="575f2-120">Minimum supported client</span></span><br/> | <span data-ttu-id="575f2-121">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="575f2-121">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="575f2-122">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="575f2-122">Minimum supported server</span></span><br/> | <span data-ttu-id="575f2-123">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="575f2-123">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="575f2-124">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="575f2-124">End of client support</span></span><br/>    | <span data-ttu-id="575f2-125">Windows XP</span><span class="sxs-lookup"><span data-stu-id="575f2-125">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="575f2-126">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="575f2-126">End of server support</span></span><br/>    | <span data-ttu-id="575f2-127">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="575f2-127">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="575f2-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="575f2-128">Header</span></span><br/>                   | <dl> <span data-ttu-id="575f2-129"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="575f2-129"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="575f2-130">INSERI</span><span class="sxs-lookup"><span data-stu-id="575f2-130">IDL</span></span><br/>                      | <dl> <span data-ttu-id="575f2-131"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="575f2-131"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="575f2-132">DLL</span><span class="sxs-lookup"><span data-stu-id="575f2-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="575f2-133"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="575f2-133"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="575f2-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="575f2-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="575f2-135">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="575f2-135">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="575f2-136">**IEnumUserIdentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="575f2-136">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="575f2-137">**IEnumUserIdentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="575f2-137">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> <dt>

[<span data-ttu-id="575f2-138">**IEnumUserIdentity:: Next**</span><span class="sxs-lookup"><span data-stu-id="575f2-138">**IEnumUserIdentity::Next**</span></span>](ienumuseridentity-next.md)
</dt> </dl>

 

 




