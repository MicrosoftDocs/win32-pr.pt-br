---
description: 'O método ReleaseBuffer retorna um exemplo de mídia para a lista de amostras de mídia gratuita. Esse método implementa o método IMemAllocator:: ReleaseBuffer.'
ms.assetid: 35e4e426-044c-4e57-af13-2fddf8501db7
title: Método CBaseAllocator. ReleaseBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.ReleaseBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8e339f3a8186e845e28261633806a61b1b15c281
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779856"
---
# <a name="cbaseallocatorreleasebuffer-method"></a><span data-ttu-id="75dff-104">Método CBaseAllocator. ReleaseBuffer</span><span class="sxs-lookup"><span data-stu-id="75dff-104">CBaseAllocator.ReleaseBuffer method</span></span>

<span data-ttu-id="75dff-105">O `ReleaseBuffer` método retorna um exemplo de mídia para a lista de amostras de mídia gratuita.</span><span class="sxs-lookup"><span data-stu-id="75dff-105">The `ReleaseBuffer` method returns a media sample to the list of free media samples.</span></span> <span data-ttu-id="75dff-106">Esse método implementa o método [**IMemAllocator:: ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) .</span><span class="sxs-lookup"><span data-stu-id="75dff-106">This method implements the [**IMemAllocator::ReleaseBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-releasebuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="75dff-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="75dff-107">Syntax</span></span>


```C++
HRESULT ReleaseBuffer(
   IMediaSample *pSample
);
```



## <a name="parameters"></a><span data-ttu-id="75dff-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="75dff-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75dff-109">*pSample*</span><span class="sxs-lookup"><span data-stu-id="75dff-109">*pSample*</span></span> 
</dt> <dd>

<span data-ttu-id="75dff-110">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do objeto de exemplo de mídia.</span><span class="sxs-lookup"><span data-stu-id="75dff-110">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface of the media sample object.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75dff-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="75dff-111">Return value</span></span>

<span data-ttu-id="75dff-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="75dff-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="75dff-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="75dff-113">Remarks</span></span>

<span data-ttu-id="75dff-114">Quando a contagem de referência de um exemplo de mídia chega a zero, o exemplo chama **ReleaseBuffer** com ele mesmo como o parâmetro.</span><span class="sxs-lookup"><span data-stu-id="75dff-114">When a media sample's reference count reaches zero, the sample calls **ReleaseBuffer** with itself as the parameter.</span></span> <span data-ttu-id="75dff-115">Esse método executa as seguintes ações.</span><span class="sxs-lookup"><span data-stu-id="75dff-115">This method performs the following actions.</span></span>

-   <span data-ttu-id="75dff-116">Retorna o exemplo de mídia para a lista livre ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="75dff-116">Returns the media sample to the free list ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>
-   <span data-ttu-id="75dff-117">Chama o método [**CBaseAllocator:: NotifySample**](cbaseallocator-notifysample.md) , que libera todos os threads bloqueados em chamadas para o método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="75dff-117">Calls the [**CBaseAllocator::NotifySample**](cbaseallocator-notifysample.md) method, which releases any threads that are blocked on calls to the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>
-   <span data-ttu-id="75dff-118">Se o método [**CBaseAllocator:: Setnotificar**](cbaseallocator-setnotify.md) foi chamado anteriormente, chama o método **IMemAllocatorNotifyCallbackTemp:: NotifyRelease** .</span><span class="sxs-lookup"><span data-stu-id="75dff-118">If the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method was called previously, calls the **IMemAllocatorNotifyCallbackTemp::NotifyRelease** method.</span></span>
-   <span data-ttu-id="75dff-119">Quando a última amostra for liberada, se houver uma [**CBaseAllocator pendente::D ecommit**](cbaseallocator-decommit.md) chamada, chamará o método [**CBaseAllocator:: Free**](cbaseallocator-free.md) para liberar a memória do buffer.</span><span class="sxs-lookup"><span data-stu-id="75dff-119">When the last sample is released, if there is a pending [**CBaseAllocator::Decommit**](cbaseallocator-decommit.md) call, calls the [**CBaseAllocator::Free**](cbaseallocator-free.md) method to release the buffer memory.</span></span> <span data-ttu-id="75dff-120">(Na classe base, **Free** é um método virtual puro.)</span><span class="sxs-lookup"><span data-stu-id="75dff-120">(In the base class, **Free** is a pure virtual method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="75dff-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75dff-121">Requirements</span></span>



| <span data-ttu-id="75dff-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="75dff-122">Requirement</span></span> | <span data-ttu-id="75dff-123">Valor</span><span class="sxs-lookup"><span data-stu-id="75dff-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75dff-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75dff-124">Header</span></span><br/>  | <dl> <span data-ttu-id="75dff-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75dff-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="75dff-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75dff-126">Library</span></span><br/> | <dl> <span data-ttu-id="75dff-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="75dff-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="75dff-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="75dff-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75dff-129">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="75dff-129">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




