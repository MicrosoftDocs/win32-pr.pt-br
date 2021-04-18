---
title: Método IEnumProgressItems RemoteNext
description: Dá suporte a um cliente remoto que deseja recuperar um número especificado de itens na sequência de enumeração. | Método IEnumProgressItems RemoteNext
ms.assetid: c5f85ca3-1bad-49fd-9e67-d41135cd837d
keywords:
- Método RemoteNext IMAPi
- Método RemoteNext IMAPi, interface IEnumProgressItems
- IEnumProgressItems interface IMAPi, método RemoteNext
topic_type:
- apiref
api_name:
- IEnumProgressItems.RemoteNext
api_location:
- Imapi2fs.idl
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a088a1be640c6653a8a8ccd8b00cf21bd027ecd7
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "105791462"
---
# <a name="ienumprogressitemsremotenext-method"></a><span data-ttu-id="d706c-107">Método IEnumProgressItems:: RemoteNext</span><span class="sxs-lookup"><span data-stu-id="d706c-107">IEnumProgressItems::RemoteNext method</span></span>

<span data-ttu-id="d706c-108">Dá suporte a um cliente remoto que deseja recuperar um número especificado de itens na sequência de enumeração</span><span class="sxs-lookup"><span data-stu-id="d706c-108">Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence</span></span>

## <a name="syntax"></a><span data-ttu-id="d706c-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d706c-109">Syntax</span></span>


```C++
HRESULT RemoteNext(
  [in]  ULONG         celt,
  [out] IProgressItem **rgelt,
  [out] ULONG         *pceltFetched
);
```



## <a name="parameters"></a><span data-ttu-id="d706c-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d706c-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d706c-111">*celt* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="d706c-111">*celt* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d706c-112">Número de itens a serem recuperados.</span><span class="sxs-lookup"><span data-stu-id="d706c-112">Number of items to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d706c-113">*rgelt* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d706c-113">*rgelt* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d706c-114">Matriz de interfaces [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) .</span><span class="sxs-lookup"><span data-stu-id="d706c-114">Array of [**IProgressItem**](/windows/desktop/api/imapi2fs/nn-imapi2fs-iprogressitem) interfaces.</span></span> <span data-ttu-id="d706c-115">Você deve liberar cada interface em rgelt quando terminar.</span><span class="sxs-lookup"><span data-stu-id="d706c-115">You must release each interface in rgelt when done.</span></span>

</dd> <dt>

<span data-ttu-id="d706c-116">*pceltFetched* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="d706c-116">*pceltFetched* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d706c-117">Número de elementos retornados em rgelt.</span><span class="sxs-lookup"><span data-stu-id="d706c-117">Number of elements returned in rgelt.</span></span> <span data-ttu-id="d706c-118">Você pode definir *pceltFetched* como **NULL** se *celt* for um.</span><span class="sxs-lookup"><span data-stu-id="d706c-118">You can set *pceltFetched* to **NULL** if *celt* is one.</span></span> <span data-ttu-id="d706c-119">Caso contrário, inicialize o valor de *pceltFetched* como 0 antes de chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="d706c-119">Otherwise, initialize the value of *pceltFetched* to 0 before calling this method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d706c-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d706c-120">Return value</span></span>

<span data-ttu-id="d706c-121">S \_ OK é retornado quando o número de elementos solicitados (*celt*) é retornado com êxito ou o número de itens retornados (*pceltFetched*) é menor que o número de elementos solicitados.</span><span class="sxs-lookup"><span data-stu-id="d706c-121">S\_OK is returned when the number of requested elements (*celt*) are returned successfully or the number of returned items (*pceltFetched*) is less than the number of requested elements.</span></span>

<span data-ttu-id="d706c-122">Outros códigos de êxito podem ser retornados como resultado da implementação.</span><span class="sxs-lookup"><span data-stu-id="d706c-122">Other success codes may be returned as a result of implementation.</span></span> <span data-ttu-id="d706c-123">Os códigos de erro a seguir são normalmente retornados na falha da operação, mas não representam os únicos valores de erro possíveis:</span><span class="sxs-lookup"><span data-stu-id="d706c-123">The following error codes are commonly returned on operation failure, but do not represent the only possible error values:</span></span>



| <span data-ttu-id="d706c-124">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d706c-124">Return code</span></span>                                                                                   | <span data-ttu-id="d706c-125">Description</span><span class="sxs-lookup"><span data-stu-id="d706c-125">Description</span></span>                                                                     |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="d706c-126"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d706c-126"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="d706c-127">O ponteiro não é válido.</span><span class="sxs-lookup"><span data-stu-id="d706c-127">Pointer is not valid.</span></span><br/> <span data-ttu-id="d706c-128">Valor: 0x80004003</span><span class="sxs-lookup"><span data-stu-id="d706c-128">Value: 0x80004003</span></span><br/>                   |
| <dl> <span data-ttu-id="d706c-129"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="d706c-129"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="d706c-130">Falha ao alocar a memória necessária.</span><span class="sxs-lookup"><span data-stu-id="d706c-130">Failed to allocate the required memory.</span></span><br/> <span data-ttu-id="d706c-131">Valor: 0x8007000E</span><span class="sxs-lookup"><span data-stu-id="d706c-131">Value: 0x8007000E</span></span><br/> |
| <dl> <span data-ttu-id="d706c-132"><dt>**E \_ INVALIDARG**</dt></span><span class="sxs-lookup"><span data-stu-id="d706c-132"><dt>**E\_INVALIDARG**</dt></span></span> </dl>  | <span data-ttu-id="d706c-133">Um ou mais argumentos não são válidos.</span><span class="sxs-lookup"><span data-stu-id="d706c-133">One or more arguments are not valid.</span></span><br/> <span data-ttu-id="d706c-134">Valor: 0x80070057</span><span class="sxs-lookup"><span data-stu-id="d706c-134">Value: 0x80070057</span></span><br/>    |
| <dl> <span data-ttu-id="d706c-135"><dt>**E \_ Inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="d706c-135"><dt> **E\_UNEXPECTED**</dt></span></span> </dl> | <span data-ttu-id="d706c-136">Ocorreu uma falha inesperada.</span><span class="sxs-lookup"><span data-stu-id="d706c-136">An unexpected failure occurred.</span></span><br/> <span data-ttu-id="d706c-137">Valor: 0x8000FFFF</span><span class="sxs-lookup"><span data-stu-id="d706c-137">Value: 0x8000FFFF</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="d706c-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="d706c-138">Remarks</span></span>

<span data-ttu-id="d706c-139">Se houver menos do que o número solicitado de elementos restantes na sequência, ele recuperará os elementos restantes.</span><span class="sxs-lookup"><span data-stu-id="d706c-139">If there are fewer than the requested number of elements left in the sequence, it retrieves the remaining elements.</span></span>

## <a name="requirements"></a><span data-ttu-id="d706c-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d706c-140">Requirements</span></span>



| <span data-ttu-id="d706c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="d706c-141">Requirement</span></span> | <span data-ttu-id="d706c-142">Valor</span><span class="sxs-lookup"><span data-stu-id="d706c-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d706c-143">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d706c-143">Minimum supported client</span></span><br/> | <span data-ttu-id="d706c-144">Somente Windows Vista, Windows XP com \[ aplicativos de área de trabalho do SP2\]</span><span class="sxs-lookup"><span data-stu-id="d706c-144">Windows Vista, Windows XP with SP2 \[desktop apps only\]</span></span><br/>                     |
| <span data-ttu-id="d706c-145">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d706c-145">Minimum supported server</span></span><br/> | <span data-ttu-id="d706c-146">\[Somente aplicativos da área de trabalho do Windows Server 2003\]</span><span class="sxs-lookup"><span data-stu-id="d706c-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d706c-147">INSERI</span><span class="sxs-lookup"><span data-stu-id="d706c-147">IDL</span></span><br/>                      | <dl> <span data-ttu-id="d706c-148"><dt>Imapi2fs. idl</dt></span><span class="sxs-lookup"><span data-stu-id="d706c-148"><dt>Imapi2fs.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d706c-149">Confira também</span><span class="sxs-lookup"><span data-stu-id="d706c-149">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d706c-150">**IEnumProgressItems**</span><span class="sxs-lookup"><span data-stu-id="d706c-150">**IEnumProgressItems**</span></span>](/windows/desktop/api/imapi2fs/nn-imapi2fs-ienumprogressitems)
</dt> <dt>

[<span data-ttu-id="d706c-151">IEnumProgressItems:: Next</span><span class="sxs-lookup"><span data-stu-id="d706c-151">IEnumProgressItems::Next</span></span>](/windows/desktop/api/imapi2fs/nf-imapi2fs-ienumprogressitems-next)
</dt> </dl>

 

 





