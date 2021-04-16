---
description: O método SourceThreadCanWait mantém ou libera o thread de streaming.
ms.assetid: f68f5f0b-ef5b-49a9-a768-c4cc065c0cb3
title: Método CBaseRenderer. SourceThreadCanWait (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SourceThreadCanWait
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f01be304ec2b5f845ea61c9609808c6e2f39fca9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750668"
---
# <a name="cbaserenderersourcethreadcanwait-method"></a><span data-ttu-id="43994-103">Método CBaseRenderer. SourceThreadCanWait</span><span class="sxs-lookup"><span data-stu-id="43994-103">CBaseRenderer.SourceThreadCanWait method</span></span>

<span data-ttu-id="43994-104">O `SourceThreadCanWait` método mantém ou libera o thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="43994-104">The `SourceThreadCanWait` method holds or releases the streaming thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="43994-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="43994-105">Syntax</span></span>


```C++
virtual HRESULT SourceThreadCanWait(
   BOOL bCanWait
);
```



## <a name="parameters"></a><span data-ttu-id="43994-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="43994-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43994-107">*bCanWait*</span><span class="sxs-lookup"><span data-stu-id="43994-107">*bCanWait*</span></span> 
</dt> <dd>

<span data-ttu-id="43994-108">Valor booliano que indica se o thread de streaming deve ser mantido.</span><span class="sxs-lookup"><span data-stu-id="43994-108">Boolean value indicating whether to hold the streaming thread.</span></span> <span data-ttu-id="43994-109">Se **for true**, o thread de streaming será bloqueado enquanto o filtro aguardar para renderizar os próximos exemplos.</span><span class="sxs-lookup"><span data-stu-id="43994-109">If **TRUE**, the streaming thread is blocked while the filter waits to render the next samples.</span></span> <span data-ttu-id="43994-110">Se for **false**, o thread de streaming será liberado.</span><span class="sxs-lookup"><span data-stu-id="43994-110">If **FALSE**, the streaming thread is released.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43994-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="43994-111">Return value</span></span>

<span data-ttu-id="43994-112">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="43994-112">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="43994-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="43994-113">Remarks</span></span>

<span data-ttu-id="43994-114">Chamar o `SourceThreadCanWait` método com o valor **false** força o filtro a retornar de uma chamada [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) bloqueada.</span><span class="sxs-lookup"><span data-stu-id="43994-114">Calling the `SourceThreadCanWait` method with the value **FALSE** forces the filter to return from a blocked [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) call.</span></span> <span data-ttu-id="43994-115">Quando o filtro está em execução, ele bloqueia as chamadas de **recebimento** até o tempo de apresentação do exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="43994-115">When the filter is running, it blocks **Receive** calls until the current sample's presentation time.</span></span> <span data-ttu-id="43994-116">Quando o filtro é pausado, ele bloqueia o **recebimento** de chamadas indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="43994-116">When the filter is paused, it blocks **Receive** calls indefinitely.</span></span> <span data-ttu-id="43994-117">Esse comportamento regula o fluxo de dados no fluxo.</span><span class="sxs-lookup"><span data-stu-id="43994-117">This behavior regulates the flow of data in the stream.</span></span> <span data-ttu-id="43994-118">No entanto, quando o filtro é interrompido ou liberado, ele não deve bloquear.</span><span class="sxs-lookup"><span data-stu-id="43994-118">When the filter is stopped or flushing, however, it should not block.</span></span>

<span data-ttu-id="43994-119">O bloqueio é controlado pelo método [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md) , que aguarda dois eventos: [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) e [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md).</span><span class="sxs-lookup"><span data-stu-id="43994-119">The blocking is controlled by the [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md) method, which waits on two events: [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) and [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md).</span></span> <span data-ttu-id="43994-120">O evento **m \_ RenderEvent** é sinalizado quando o tempo de apresentação chega.</span><span class="sxs-lookup"><span data-stu-id="43994-120">The **m\_RenderEvent** event is signaled when the presentation time arrives.</span></span> <span data-ttu-id="43994-121">O evento **m \_ ThreadSignal** é sinalizado quando `SourceThreadCanWait` é chamado com o valor **false**.</span><span class="sxs-lookup"><span data-stu-id="43994-121">The **m\_ThreadSignal** event is signaled when `SourceThreadCanWait` is called with the value **FALSE**.</span></span> <span data-ttu-id="43994-122">Chamar `SourceThreadCanWait` com o valor **true** redefine o evento.</span><span class="sxs-lookup"><span data-stu-id="43994-122">Calling `SourceThreadCanWait` with the value **TRUE** resets the event.</span></span>

<span data-ttu-id="43994-123">Os métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chamam `SourceThreadCanWait` com o valor **false** (liberando o thread de streaming).</span><span class="sxs-lookup"><span data-stu-id="43994-123">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call `SourceThreadCanWait` with the value **FALSE** (releasing the streaming thread).</span></span> <span data-ttu-id="43994-124">Os métodos [**CBaseRenderer::P ause**](cbaserenderer-pause.md), [**CBaseRenderer:: Run**](cbaserenderer-run.md)e [**CBaseRenderer:: EndFlush**](cbaserenderer-endflush.md) chamam `SourceThreadCanWait` com o valor **true**.</span><span class="sxs-lookup"><span data-stu-id="43994-124">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md), [**CBaseRenderer::Run**](cbaserenderer-run.md), and [**CBaseRenderer::EndFlush**](cbaserenderer-endflush.md) methods call `SourceThreadCanWait` with the value **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="43994-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="43994-125">Requirements</span></span>



| <span data-ttu-id="43994-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="43994-126">Requirement</span></span> | <span data-ttu-id="43994-127">Valor</span><span class="sxs-lookup"><span data-stu-id="43994-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="43994-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="43994-128">Header</span></span><br/>  | <dl> <span data-ttu-id="43994-129"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="43994-129"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="43994-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="43994-130">Library</span></span><br/> | <dl> <span data-ttu-id="43994-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="43994-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="43994-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="43994-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43994-133">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="43994-133">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




