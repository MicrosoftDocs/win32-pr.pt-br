---
description: 'O método GetBuffer Recupera um exemplo de mídia que contém um buffer. Esse método implementa o método IMemAllocator:: GetBuffer.'
ms.assetid: 81694b9c-b325-47c8-94e4-f54d1329a684
title: Método CBaseAllocator. GetBuffer (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.GetBuffer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f965885d4a7a12e09c8875f71032ce2fded61bd2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752311"
---
# <a name="cbaseallocatorgetbuffer-method"></a><span data-ttu-id="f1ac0-104">Método CBaseAllocator. GetBuffer</span><span class="sxs-lookup"><span data-stu-id="f1ac0-104">CBaseAllocator.GetBuffer method</span></span>

<span data-ttu-id="f1ac0-105">O `GetBuffer` método recupera um exemplo de mídia que contém um buffer.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-105">The `GetBuffer` method retrieves a media sample that contains a buffer.</span></span> <span data-ttu-id="f1ac0-106">Esse método implementa o método [**IMemAllocator:: GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) .</span><span class="sxs-lookup"><span data-stu-id="f1ac0-106">This method implements the [**IMemAllocator::GetBuffer**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-getbuffer) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ac0-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1ac0-107">Syntax</span></span>


```C++
HRESULT GetBuffer(
   IMediaSample   **ppBuffer,
   REFERENCE_TIME *pStartTime,
   REFERENCE_TIME *pEndTime,
   DWORD          dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f1ac0-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1ac0-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ac0-109">*ppBuffer*</span><span class="sxs-lookup"><span data-stu-id="f1ac0-109">*ppBuffer*</span></span> 
</dt> <dd>

<span data-ttu-id="f1ac0-110">Recebe um ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do buffer.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-110">Receives a pointer to the buffer's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span> <span data-ttu-id="f1ac0-111">O chamador deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-111">The caller must release the interface.</span></span>

</dd> <dt>

<span data-ttu-id="f1ac0-112">*pStartTime*</span><span class="sxs-lookup"><span data-stu-id="f1ac0-112">*pStartTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f1ac0-113">Ponteiro para a hora de início do exemplo.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-113">Pointer to the start time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="f1ac0-114">*pEndTime*</span><span class="sxs-lookup"><span data-stu-id="f1ac0-114">*pEndTime*</span></span> 
</dt> <dd>

<span data-ttu-id="f1ac0-115">Ponteiro para a hora de término do exemplo.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-115">Pointer to the end time of the sample.</span></span>

</dd> <dt>

<span data-ttu-id="f1ac0-116">*dwFlags*</span><span class="sxs-lookup"><span data-stu-id="f1ac0-116">*dwFlags*</span></span> 
</dt> <dd>

<span data-ttu-id="f1ac0-117">Combinação de bits bit a zero ou mais sinalizadores.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-117">Bitwise combination of zero or more flags.</span></span> <span data-ttu-id="f1ac0-118">A classe base oferece suporte ao sinalizador a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-118">The base class supports the following flag.</span></span>



| <span data-ttu-id="f1ac0-119">Valor</span><span class="sxs-lookup"><span data-stu-id="f1ac0-119">Value</span></span>                                                                                                                                                          | <span data-ttu-id="f1ac0-120">Significado</span><span class="sxs-lookup"><span data-stu-id="f1ac0-120">Meaning</span></span>                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------|
| <span id="AM_GBF_NOWAIT"></span><span id="am_gbf_nowait"></span><dl> <span data-ttu-id="f1ac0-121"><dt>**\_gbf \_ nowait**</dt></span><span class="sxs-lookup"><span data-stu-id="f1ac0-121"><dt>**AM\_GBF\_NOWAIT**</dt></span></span> </dl> | <span data-ttu-id="f1ac0-122">Não aguarde até que um buffer fique disponível.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-122">Do not wait for a buffer to become available.</span></span> <br/> |



 

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ac0-123">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1ac0-123">Return value</span></span>

<span data-ttu-id="f1ac0-124">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-124">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="f1ac0-125">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="f1ac0-125">Return code</span></span>                                                                                           | <span data-ttu-id="f1ac0-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="f1ac0-126">Description</span></span>                             |
|-------------------------------------------------------------------------------------------------------|-----------------------------------------|
| <dl> <span data-ttu-id="f1ac0-127"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="f1ac0-127"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="f1ac0-128">Êxito.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-128">Success.</span></span><br/>                     |
| <dl> <span data-ttu-id="f1ac0-129"><dt>**VFW \_ E \_ não \_ confirmado**</dt></span><span class="sxs-lookup"><span data-stu-id="f1ac0-129"><dt>**VFW\_E\_NOT\_COMMITTED**</dt></span></span> </dl> | <span data-ttu-id="f1ac0-130">O alocador não foi confirmado.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-130">Allocator was not committed.</span></span><br/> |
| <dl> <span data-ttu-id="f1ac0-131"><dt>**\_ \_ tempo limite de VFW E**</dt></span><span class="sxs-lookup"><span data-stu-id="f1ac0-131"><dt>**VFW\_E\_TIMEOUT**</dt></span></span> </dl>        | <span data-ttu-id="f1ac0-132">Tempo limite atingido.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-132">Timed out.</span></span><br/>                   |



 

## <a name="remarks"></a><span data-ttu-id="f1ac0-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1ac0-133">Remarks</span></span>

<span data-ttu-id="f1ac0-134">A menos que o chamador especifique o sinalizador **am \_ gbf \_ nowait** no *dwFlags*, esse método será bloqueado até que a próxima amostra esteja disponível.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-134">Unless the caller specifies the **AM\_GBF\_NOWAIT** flag in *dwFlags*, this method blocks until the next sample is available.</span></span>

<span data-ttu-id="f1ac0-135">O exemplo de mídia recuperada tem um ponteiro válido para o buffer alocado.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-135">The retrieved media sample has a valid pointer to the allocated buffer.</span></span> <span data-ttu-id="f1ac0-136">O chamador é responsável por definir quaisquer outras propriedades no exemplo, como carimbos de data/hora, horários de mídia ou a propriedade de ponto de sincronização.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-136">The caller is responsible for setting any other properties on the sample, such as the time stamps, the media times, or the sync-point property.</span></span> <span data-ttu-id="f1ac0-137">Para obter mais informações, consulte [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span><span class="sxs-lookup"><span data-stu-id="f1ac0-137">For more information, see [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample).</span></span>

<span data-ttu-id="f1ac0-138">Na classe base, os parâmetros *pStartTime* e *pEndTime* são ignorados.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-138">In the base class, the *pStartTime* and *pEndTime* parameters are ignored.</span></span> <span data-ttu-id="f1ac0-139">Classes derivadas podem usar esses valores.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-139">Derived classes can use these values.</span></span> <span data-ttu-id="f1ac0-140">Por exemplo, o alocador do filtro de [processador de vídeo](video-renderer-filter.md) usa esses valores para sincronizar a alternância entre as superfícies do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-140">For example, the allocator for the [Video Renderer](video-renderer-filter.md) filter uses these values to synchronize switching between DirectDraw surfaces.</span></span>

<span data-ttu-id="f1ac0-141">Se o método precisar aguardar um exemplo, ele incrementará a contagem de objetos em espera ([**CBaseAllocator:: m \_ lCount**](cbaseallocator-m-lcount.md)) e a função calls [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) no semáforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)).</span><span class="sxs-lookup"><span data-stu-id="f1ac0-141">If the method needs to wait on a sample, it increments the count of waiting objects ([**CBaseAllocator::m\_lCount**](cbaseallocator-m-lcount.md)) and the calls [**WaitForSingleObject**](/windows/desktop/api/synchapi/nf-synchapi-waitforsingleobject) function on the semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)).</span></span> <span data-ttu-id="f1ac0-142">Quando um exemplo se torna disponível, ele chama o método [**CBaseAllocator:: ReleaseBuffer**](cbaseallocator-releasebuffer.md) no alocador, o que aumenta a contagem de semáforos por **m \_ lCount** (liberando assim os threads em espera) e define **m \_ lCount** de volta para zero.</span><span class="sxs-lookup"><span data-stu-id="f1ac0-142">When a sample becomes available, it calls the [**CBaseAllocator::ReleaseBuffer**](cbaseallocator-releasebuffer.md) method on the allocator, which increases the semaphore count by **m\_lCount** (thereby releasing the waiting threads) and sets **m\_lCount** back to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ac0-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1ac0-143">Requirements</span></span>



| <span data-ttu-id="f1ac0-144">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1ac0-144">Requirement</span></span> | <span data-ttu-id="f1ac0-145">Valor</span><span class="sxs-lookup"><span data-stu-id="f1ac0-145">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ac0-146">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1ac0-146">Header</span></span><br/>  | <dl> <span data-ttu-id="f1ac0-147"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1ac0-147"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="f1ac0-148">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1ac0-148">Library</span></span><br/> | <dl> <span data-ttu-id="f1ac0-149"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f1ac0-149"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1ac0-150">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1ac0-150">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ac0-151">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="f1ac0-151">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

