---
description: O método ScheduleSample agenda uma amostra para renderização.
ms.assetid: 08c218d1-6d0a-4c66-bbde-a39e5d31561c
title: Método CBaseRenderer. ScheduleSample (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ScheduleSample
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c340e54f35b353820b128681cfbc0c5798d38849
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748820"
---
# <a name="cbaserendererschedulesample-method"></a><span data-ttu-id="f1ed7-103">Método CBaseRenderer. ScheduleSample</span><span class="sxs-lookup"><span data-stu-id="f1ed7-103">CBaseRenderer.ScheduleSample method</span></span>

<span data-ttu-id="f1ed7-104">O `ScheduleSample` método agenda uma amostra para renderização.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-104">The `ScheduleSample` method schedules a sample for rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1ed7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="f1ed7-105">Syntax</span></span>


```C++
virtual BOOL ScheduleSample(
   IMediaSample *pMediaSample
);
```



## <a name="parameters"></a><span data-ttu-id="f1ed7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="f1ed7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1ed7-107">*pMediaSample*</span><span class="sxs-lookup"><span data-stu-id="f1ed7-107">*pMediaSample*</span></span> 
</dt> <dd>

<span data-ttu-id="f1ed7-108">Ponteiro para a interface [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) do exemplo.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-108">Pointer to the sample's [**IMediaSample**](/windows/desktop/api/Strmif/nn-strmif-imediasample) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1ed7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="f1ed7-109">Return value</span></span>

<span data-ttu-id="f1ed7-110">Retorna **true** se o exemplo foi agendado ou **false** se o exemplo foi Descartado.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-110">Returns **TRUE** if the sample was scheduled, or **FALSE** if the sample was dropped.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1ed7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="f1ed7-111">Remarks</span></span>

<span data-ttu-id="f1ed7-112">Esse método primeiro determina se o exemplo deve ser renderizado imediatamente, renderizado no futuro ou descartado.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-112">This method first determines whether the sample should be rendered immediately, rendered in the future, or dropped.</span></span> <span data-ttu-id="f1ed7-113">(Para fazer isso, ele chama o método [**CBaseRenderer:: GetSampleTimes**](cbaserenderer-getsampletimes.md) .) Se o exemplo deve ser processado imediatamente, o método sinaliza o evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="f1ed7-113">(To do so, it calls the [**CBaseRenderer::GetSampleTimes**](cbaserenderer-getsampletimes.md) method.) If the sample should be rendered immediately, the method signals the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span> <span data-ttu-id="f1ed7-114">Se o exemplo for renderizado no futuro, o método chamará o método [**IReferenceClock:: aconselhetime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) para agendamento.</span><span class="sxs-lookup"><span data-stu-id="f1ed7-114">If the sample should be rendered in the future, the method calls the [**IReferenceClock::AdviseTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-advisetime) method for scheduling.</span></span>

## <a name="requirements"></a><span data-ttu-id="f1ed7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f1ed7-115">Requirements</span></span>



| <span data-ttu-id="f1ed7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="f1ed7-116">Requirement</span></span> | <span data-ttu-id="f1ed7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="f1ed7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1ed7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f1ed7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f1ed7-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f1ed7-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f1ed7-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f1ed7-120">Library</span></span><br/> | <dl> <span data-ttu-id="f1ed7-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f1ed7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1ed7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="f1ed7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1ed7-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="f1ed7-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




