---
description: 'IEnumUserIdentity:: Next não tem suporte e pode ser alterado ou indisponível no futuro. Em vez disso, use contas de usuário com troca rápida de usuário e Área de Trabalho Remota.'
ms.assetid: 2c8dfe36-c1bb-49f8-8847-f355cfab2984
title: 'Método IEnumUserIdentity:: Next (Msident. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IEnumUserIdentity.Next
api_type:
- COM
api_location:
- Msident.dll
ms.openlocfilehash: 763b2b4a612596c5f02a9826ad2e9c09ab8e4b0e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988965"
---
# <a name="ienumuseridentitynext-method"></a><span data-ttu-id="b419b-104">Método IEnumUserIdentity:: Next</span><span class="sxs-lookup"><span data-stu-id="b419b-104">IEnumUserIdentity::Next method</span></span>

<span data-ttu-id="b419b-105">\[**IEnumUserIdentity:: Next** não tem suporte e pode ser alterado ou indisponível no futuro.</span><span class="sxs-lookup"><span data-stu-id="b419b-105">\[**IEnumUserIdentity::Next** is not supported and may be altered or unavailable in the future.</span></span> <span data-ttu-id="b419b-106">Em vez disso, use [contas de usuário com troca rápida de usuário e área de trabalho remota](fastuserswitching.md).\]</span><span class="sxs-lookup"><span data-stu-id="b419b-106">Instead, use [User Accounts with Fast User Switching and Remote Desktop](fastuserswitching.md).\]</span></span>

<span data-ttu-id="b419b-107">Preterido.</span><span class="sxs-lookup"><span data-stu-id="b419b-107">Deprecated.</span></span> <span data-ttu-id="b419b-108">Recupera uma matriz de interfaces de identidade do usuário da enumeração.</span><span class="sxs-lookup"><span data-stu-id="b419b-108">Retrieves an array of user identity interfaces from the enumeration.</span></span>

## <a name="syntax"></a><span data-ttu-id="b419b-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b419b-109">Syntax</span></span>


```C++
HRESULT Next(
  [in]  ULONG    celt,
  [out] IUnknown **rgelt,
  [out] ULONG    *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="b419b-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b419b-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b419b-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="b419b-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b419b-112">Tipo: **ULONG**</span><span class="sxs-lookup"><span data-stu-id="b419b-112">Type: **ULONG**</span></span>

<span data-ttu-id="b419b-113">Um valor **ULONG** que representa o número de interfaces a serem recuperadas.</span><span class="sxs-lookup"><span data-stu-id="b419b-113">A **ULONG** value that represents the number of interfaces to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="b419b-114">*rgelt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b419b-114">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b419b-115">Tipo: **[ **IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span><span class="sxs-lookup"><span data-stu-id="b419b-115">Type: **[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\*\***</span></span>

<span data-ttu-id="b419b-116">O endereço de um ponteiro que recebe as interfaces.</span><span class="sxs-lookup"><span data-stu-id="b419b-116">The address of a pointer that receives the interfaces.</span></span>

</dd> <dt>

<span data-ttu-id="b419b-117">*pceltFetched* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b419b-117">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b419b-118">Tipo: \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="b419b-118">Type: \**ULONG\** _</span></span>

<span data-ttu-id="b419b-119">O endereço de um ponteiro que recebe o número de interfaces recuperadas com êxito.</span><span class="sxs-lookup"><span data-stu-id="b419b-119">The address of a pointer that receives the number of interfaces successfully retrieved.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b419b-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b419b-120">Return value</span></span>

<span data-ttu-id="b419b-121">Tipo: _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="b419b-121">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="b419b-122">Se esse método for bem sucedido, ele retornará **S \_ OK**.</span><span class="sxs-lookup"><span data-stu-id="b419b-122">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="b419b-123">Caso contrário, ele retorna um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="b419b-123">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="b419b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="b419b-124">Remarks</span></span>

<span data-ttu-id="b419b-125">[**IEnumUserIdentity**](ienumuseridentity.md) mantém uma contagem interna que especifica qual interface está próxima de ser recuperada.</span><span class="sxs-lookup"><span data-stu-id="b419b-125">[**IEnumUserIdentity**](ienumuseridentity.md) keeps an internal count that specifies which interface is next to be retrieved.</span></span> <span data-ttu-id="b419b-126">Várias chamadas para este método não redefinirão essa contagem.</span><span class="sxs-lookup"><span data-stu-id="b419b-126">Multiple calls to this method will not reset this count.</span></span> <span data-ttu-id="b419b-127">Para redefinir a contagem, chame [**IEnumUserIdentity:: Reset**](ienumuseridentity-reset.md).</span><span class="sxs-lookup"><span data-stu-id="b419b-127">To reset the count, call [**IEnumUserIdentity::Reset**](ienumuseridentity-reset.md).</span></span> <span data-ttu-id="b419b-128">Para incrementar a contagem sem recuperar interfaces, chame [**IEnumUserIdentity:: Skip**](ienumuseridentity-skip.md).</span><span class="sxs-lookup"><span data-stu-id="b419b-128">To increment the count without retrieving interfaces, call [**IEnumUserIdentity::Skip**](ienumuseridentity-skip.md).</span></span>

<span data-ttu-id="b419b-129">O valor de *celt* não deve exceder o valor retornado por [**IEnumUserIdentity:: GetCount**](ienumuseridentity-getcount.md).</span><span class="sxs-lookup"><span data-stu-id="b419b-129">The value of *celt* should not exceed the value returned by [**IEnumUserIdentity::GetCount**](ienumuseridentity-getcount.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="b419b-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b419b-130">Requirements</span></span>



| <span data-ttu-id="b419b-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="b419b-131">Requirement</span></span> | <span data-ttu-id="b419b-132">Valor</span><span class="sxs-lookup"><span data-stu-id="b419b-132">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b419b-133">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b419b-133">Minimum supported client</span></span><br/> | <span data-ttu-id="b419b-134">\[Somente aplicativos da área de trabalho do Windows XP\]</span><span class="sxs-lookup"><span data-stu-id="b419b-134">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="b419b-135">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="b419b-135">Minimum supported server</span></span><br/> | <span data-ttu-id="b419b-136">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="b419b-136">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="b419b-137">Fim do suporte do cliente</span><span class="sxs-lookup"><span data-stu-id="b419b-137">End of client support</span></span><br/>    | <span data-ttu-id="b419b-138">Windows XP</span><span class="sxs-lookup"><span data-stu-id="b419b-138">Windows XP</span></span><br/>                                                                  |
| <span data-ttu-id="b419b-139">Fim do suporte do servidor</span><span class="sxs-lookup"><span data-stu-id="b419b-139">End of server support</span></span><br/>    | <span data-ttu-id="b419b-140">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="b419b-140">Windows Server 2003</span></span><br/>                                                         |
| <span data-ttu-id="b419b-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b419b-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="b419b-142"><dt>Msident. h</dt></span><span class="sxs-lookup"><span data-stu-id="b419b-142"><dt>Msident.h</dt></span></span> </dl>   |
| <span data-ttu-id="b419b-143">INSERI</span><span class="sxs-lookup"><span data-stu-id="b419b-143">IDL</span></span><br/>                      | <dl> <span data-ttu-id="b419b-144"><dt>Msident. idl</dt></span><span class="sxs-lookup"><span data-stu-id="b419b-144"><dt>Msident.idl</dt></span></span> </dl> |
| <span data-ttu-id="b419b-145">DLL</span><span class="sxs-lookup"><span data-stu-id="b419b-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="b419b-146"><dt>Msident.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b419b-146"><dt>Msident.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b419b-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="b419b-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b419b-148">**IEnumUserIdentity**</span><span class="sxs-lookup"><span data-stu-id="b419b-148">**IEnumUserIdentity**</span></span>](ienumuseridentity.md)
</dt> <dt>

[<span data-ttu-id="b419b-149">**IEnumUserIdentity:: Skip**</span><span class="sxs-lookup"><span data-stu-id="b419b-149">**IEnumUserIdentity::Skip**</span></span>](ienumuseridentity-skip.md)
</dt> <dt>

[<span data-ttu-id="b419b-150">**IEnumUserIdentity:: Reset**</span><span class="sxs-lookup"><span data-stu-id="b419b-150">**IEnumUserIdentity::Reset**</span></span>](ienumuseridentity-reset.md)
</dt> <dt>

[<span data-ttu-id="b419b-151">**IEnumUserIdentity:: GetCount**</span><span class="sxs-lookup"><span data-stu-id="b419b-151">**IEnumUserIdentity::GetCount**</span></span>](ienumuseridentity-getcount.md)
</dt> </dl>

 

 
