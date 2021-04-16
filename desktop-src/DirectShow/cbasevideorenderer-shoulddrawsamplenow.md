---
description: O método ShouldDrawSampleNow determina se o vídeo deve ser desenhado sem definir um link de aviso de temporizador com o relógio.
ms.assetid: 2cbefc66-0d99-4559-b210-3163cd413dbf
title: Método CBaseVideoRenderer. ShouldDrawSampleNow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseVideoRenderer.ShouldDrawSampleNow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8c96b7453eb6009121fd6782030f7988663f5e8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758553"
---
# <a name="cbasevideorenderershoulddrawsamplenow-method"></a><span data-ttu-id="c84e5-103">Método CBaseVideoRenderer. ShouldDrawSampleNow</span><span class="sxs-lookup"><span data-stu-id="c84e5-103">CBaseVideoRenderer.ShouldDrawSampleNow method</span></span>

<span data-ttu-id="c84e5-104">O `ShouldDrawSampleNow` método determina se o vídeo deve ser desenhado sem definir um link de aviso de temporizador com o relógio.</span><span class="sxs-lookup"><span data-stu-id="c84e5-104">The `ShouldDrawSampleNow` method determines if the video should be drawn without setting a timer advise link with the clock.</span></span>

## <a name="syntax"></a><span data-ttu-id="c84e5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c84e5-105">Syntax</span></span>


```C++
virtual HRESULT ShouldDrawSampleNow(
   IMediaSample   *pMediaSample,
   REFERENCE_TIME *ptrStart,
   REFERENCE_TIME *ptrEnd
);
```



## <a name="parameters"></a><span data-ttu-id="c84e5-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c84e5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c84e5-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="c84e5-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="c84e5-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) para o exemplo.</span><span class="sxs-lookup"><span data-stu-id="c84e5-108">Pointer to the [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface for the sample.</span></span>

</dd> <dt>

<span data-ttu-id="c84e5-109">*ptrStart*</span><span class="sxs-lookup"><span data-stu-id="c84e5-109">*ptrStart*</span></span> 
</dt> <dd>

<span data-ttu-id="c84e5-110">Ponteiro para o tempo para começar a renderização.</span><span class="sxs-lookup"><span data-stu-id="c84e5-110">Pointer to the time to begin rendering.</span></span>

</dd> <dt>

<span data-ttu-id="c84e5-111">*ptrEnd*</span><span class="sxs-lookup"><span data-stu-id="c84e5-111">*ptrEnd*</span></span> 
</dt> <dd>

<span data-ttu-id="c84e5-112">Ponteiro para a hora para parar a renderização.</span><span class="sxs-lookup"><span data-stu-id="c84e5-112">Pointer to the time to stop rendering.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c84e5-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c84e5-113">Return value</span></span>

<span data-ttu-id="c84e5-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c84e5-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c84e5-115">Retorna S \_ OK para a média desenhar ao mesmo tempo sem espera, S \_ false para significar Draw no time *ptrStart* ou um erro para significar não desenhar o exemplo; ou seja, ignorá-lo para economizar tempo.</span><span class="sxs-lookup"><span data-stu-id="c84e5-115">Returns S\_OK to mean draw at once without waiting, S\_FALSE to mean draw at time *ptrStart*, or an error to mean do not draw the sample; that is, skip it to save time.</span></span>

## <a name="remarks"></a><span data-ttu-id="c84e5-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="c84e5-116">Remarks</span></span>

<span data-ttu-id="c84e5-117">Essa função de membro substitui [**CBaseRenderer:: ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span><span class="sxs-lookup"><span data-stu-id="c84e5-117">This member function overrides [**CBaseRenderer::ShouldDrawSampleNow**](cbaserenderer-shoulddrawsamplenow.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="c84e5-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c84e5-118">Requirements</span></span>



| <span data-ttu-id="c84e5-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="c84e5-119">Requirement</span></span> | <span data-ttu-id="c84e5-120">Valor</span><span class="sxs-lookup"><span data-stu-id="c84e5-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c84e5-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c84e5-121">Header</span></span><br/>  | <dl> <span data-ttu-id="c84e5-122"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c84e5-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c84e5-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c84e5-123">Library</span></span><br/> | <dl> <span data-ttu-id="c84e5-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c84e5-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c84e5-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="c84e5-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c84e5-126">**Classe CBaseVideoRenderer**</span><span class="sxs-lookup"><span data-stu-id="c84e5-126">**CBaseVideoRenderer Class**</span></span>](cbasevideorenderer.md)
</dt> </dl>

 

 




