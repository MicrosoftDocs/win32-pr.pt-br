---
description: 'O método NotifyAllocator especifica um alocador para a conexão. Esse método implementa o método IMemInputPin:: NotifyAllocator.'
ms.assetid: adc1c5b6-99da-4140-b644-7b98f6b8bad4
title: Método CTransInPlaceInputPin. NotifyAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.NotifyAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74578243ce780e09d7435f9dd4b70bd9497e1e97
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751477"
---
# <a name="ctransinplaceinputpinnotifyallocator-method"></a><span data-ttu-id="d8491-104">Método CTransInPlaceInputPin. NotifyAllocator</span><span class="sxs-lookup"><span data-stu-id="d8491-104">CTransInPlaceInputPin.NotifyAllocator method</span></span>

<span data-ttu-id="d8491-105">O `NotifyAllocator` método especifica um alocador para a conexão.</span><span class="sxs-lookup"><span data-stu-id="d8491-105">The `NotifyAllocator` method specifies an allocator for the connection.</span></span> <span data-ttu-id="d8491-106">Esse método implementa o método [**IMemInputPin:: NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) .</span><span class="sxs-lookup"><span data-stu-id="d8491-106">This method implements the [**IMemInputPin::NotifyAllocator**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-notifyallocator) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8491-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8491-107">Syntax</span></span>


```C++
HRESULT NotifyAllocator(
   IMemAllocator *pAllocator,
   BOOL          bReadOnly
);
```



## <a name="parameters"></a><span data-ttu-id="d8491-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8491-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8491-109">*pAllocator*</span><span class="sxs-lookup"><span data-stu-id="d8491-109">*pAllocator*</span></span> 
</dt> <dd>

<span data-ttu-id="d8491-110">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="d8491-110">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="d8491-111">*bReadOnly*</span><span class="sxs-lookup"><span data-stu-id="d8491-111">*bReadOnly*</span></span> 
</dt> <dd>

<span data-ttu-id="d8491-112">Sinalizador que especifica se os exemplos deste alocador são somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d8491-112">Flag that specifies whether samples from this allocator are read-only.</span></span> <span data-ttu-id="d8491-113">Se **for true**, os exemplos serão somente leitura.</span><span class="sxs-lookup"><span data-stu-id="d8491-113">If **TRUE**, samples are read-only.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8491-114">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8491-114">Return value</span></span>

<span data-ttu-id="d8491-115">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8491-115">Returns an **HRESULT** value.</span></span> <span data-ttu-id="d8491-116">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="d8491-116">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="d8491-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="d8491-117">Return code</span></span>                                                                               | <span data-ttu-id="d8491-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d8491-118">Description</span></span>                          |
|-------------------------------------------------------------------------------------------|--------------------------------------|
| <dl> <span data-ttu-id="d8491-119"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="d8491-119"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="d8491-120">Êxito</span><span class="sxs-lookup"><span data-stu-id="d8491-120">Success</span></span><br/>                   |
| <dl> <span data-ttu-id="d8491-121"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="d8491-121"><dt>**E\_FAIL**</dt></span></span> </dl>    | <span data-ttu-id="d8491-122">Falha</span><span class="sxs-lookup"><span data-stu-id="d8491-122">Failure</span></span><br/>                   |
| <dl> <span data-ttu-id="d8491-123"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="d8491-123"><dt>**E\_POINTER**</dt></span></span> </dl> | <span data-ttu-id="d8491-124">Argumento de ponteiro **nulo**</span><span class="sxs-lookup"><span data-stu-id="d8491-124">**NULL** pointer argument</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d8491-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8491-125">Remarks</span></span>

<span data-ttu-id="d8491-126">O filtro tenta usar o mesmo alocador para ambas as conexões de PIN.</span><span class="sxs-lookup"><span data-stu-id="d8491-126">The filter attempts to use the same allocator for both pin connections.</span></span>

-   <span data-ttu-id="d8491-127">Se o pino de saída não estiver conectado, o PIN de entrada aceitará automaticamente o alocador.</span><span class="sxs-lookup"><span data-stu-id="d8491-127">If the output pin is not connected, the input pin automatically accepts the allocator.</span></span> <span data-ttu-id="d8491-128">Quando o pino de saída estiver conectado, o filtro reconectará o PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="d8491-128">When the output pin is connected, the filter will reconnect the input pin.</span></span> <span data-ttu-id="d8491-129">Nesse ponto, o filtro tentará novamente usar um único alocador.</span><span class="sxs-lookup"><span data-stu-id="d8491-129">At that point, the filter will try again to use a single allocator.</span></span>
-   <span data-ttu-id="d8491-130">Se o pino de saída estiver conectado, o PIN de entrada aceitará o alocador.</span><span class="sxs-lookup"><span data-stu-id="d8491-130">If the output pin is connected, the input pin accepts the allocator.</span></span> <span data-ttu-id="d8491-131">O PIN de saída também usa o mesmo alocador.</span><span class="sxs-lookup"><span data-stu-id="d8491-131">The output pin also uses the same allocator.</span></span> <span data-ttu-id="d8491-132">Ele chama `NotifyAllocator` o pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="d8491-132">It calls `NotifyAllocator` on the downstream input pin.</span></span>

<span data-ttu-id="d8491-133">O caso anterior tem a seguinte exceção:</span><span class="sxs-lookup"><span data-stu-id="d8491-133">The previous case has the following exception:</span></span>

-   <span data-ttu-id="d8491-134">Se o alocador proposto for somente leitura (ou seja, o parâmetro *bReadOnly* for **true**) e o filtro precisar modificar os exemplos, o filtro deverá usar dois alocadores diferentes.</span><span class="sxs-lookup"><span data-stu-id="d8491-134">If the proposed allocator is read-only (that is, the *bReadOnly* parameter is **TRUE**) and the filter needs to modify the samples, then the filter must use two different allocators.</span></span> <span data-ttu-id="d8491-135">Nesse caso, se o filtro upstream estiver propondo para usar o alocador do filtro downstream, o método retornará E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="d8491-135">In this case, if the upstream filter is proposing to use the downstream filter's allocator, the method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8491-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8491-136">Requirements</span></span>



| <span data-ttu-id="d8491-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8491-137">Requirement</span></span> | <span data-ttu-id="d8491-138">Valor</span><span class="sxs-lookup"><span data-stu-id="d8491-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8491-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8491-139">Header</span></span><br/>  | <dl> <span data-ttu-id="d8491-140"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8491-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d8491-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8491-141">Library</span></span><br/> | <dl> <span data-ttu-id="d8491-142"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d8491-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d8491-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="d8491-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d8491-144">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="d8491-144">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




