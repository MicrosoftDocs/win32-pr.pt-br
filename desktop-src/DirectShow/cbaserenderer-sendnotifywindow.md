---
description: O método SendNotifyWindow notifica o filtro upstream do identificador da janela de vídeo.
ms.assetid: f46390b1-d03a-4520-8c1d-b3f870d3bb0b
title: Método CBaseRenderer. SendNotifyWindow (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SendNotifyWindow
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 727ab16604df5b908085208e1d127e5dffad92fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752298"
---
# <a name="cbaserenderersendnotifywindow-method"></a><span data-ttu-id="e0f02-103">Método CBaseRenderer. SendNotifyWindow</span><span class="sxs-lookup"><span data-stu-id="e0f02-103">CBaseRenderer.SendNotifyWindow method</span></span>

<span data-ttu-id="e0f02-104">O `SendNotifyWindow` método notifica o filtro upstream do identificador da janela de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e0f02-104">The `SendNotifyWindow` method notifies the upstream filter of the video window handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="e0f02-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e0f02-105">Syntax</span></span>


```C++
void SendNotifyWindow(
   IPin *pPin,
   HWND hwnd
);
```



## <a name="parameters"></a><span data-ttu-id="e0f02-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e0f02-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e0f02-107">*pPin*</span><span class="sxs-lookup"><span data-stu-id="e0f02-107">*pPin*</span></span> 
</dt> <dd>

<span data-ttu-id="e0f02-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída do filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="e0f02-108">Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the upstream filter's output pin.</span></span>

</dd> <dt>

<span data-ttu-id="e0f02-109">*HWND*</span><span class="sxs-lookup"><span data-stu-id="e0f02-109">*hwnd*</span></span> 
</dt> <dd>

<span data-ttu-id="e0f02-110">Manipular para a janela de vídeo ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e0f02-110">Handle to the video window, or **NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e0f02-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e0f02-111">Return value</span></span>

<span data-ttu-id="e0f02-112">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e0f02-112">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e0f02-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="e0f02-113">Remarks</span></span>

<span data-ttu-id="e0f02-114">Se o pino de saída do filtro upstream der suporte à interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) , esse método enviará a ele o código de evento da [**janela de \_ notificação \_ do EC**](ec-notify-window.md) junto com o identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="e0f02-114">If the output pin of the upstream filter supports the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface, this method sends it the [**EC\_NOTIFY\_WINDOW**](ec-notify-window.md) event code along with the window handle.</span></span>

<span data-ttu-id="e0f02-115">Os renderizadores de vídeo podem substituir seus métodos [**CBaseRenderer:: CompleteConnect**](cbaserenderer-completeconnect.md) para chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="e0f02-115">Video renderers can override their [**CBaseRenderer::CompleteConnect**](cbaserenderer-completeconnect.md) methods to call this method.</span></span> <span data-ttu-id="e0f02-116">Ele fornece um mecanismo para informar o filtro upstream do identificador de janela.</span><span class="sxs-lookup"><span data-stu-id="e0f02-116">It provides a mechanism for informing the upstream filter of the window handle.</span></span> <span data-ttu-id="e0f02-117">Se você fizer isso, substitua o método [**CBaseRenderer:: BreakConnect**](cbaserenderer-breakconnect.md) também e chame `SendNotifyWindow` um identificador **nulo** .</span><span class="sxs-lookup"><span data-stu-id="e0f02-117">If you do this, override the [**CBaseRenderer::BreakConnect**](cbaserenderer-breakconnect.md) method as well, and call `SendNotifyWindow` with a **NULL** handle.</span></span>

## <a name="requirements"></a><span data-ttu-id="e0f02-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e0f02-118">Requirements</span></span>



| <span data-ttu-id="e0f02-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e0f02-119">Requirement</span></span> | <span data-ttu-id="e0f02-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e0f02-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e0f02-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e0f02-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e0f02-122"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e0f02-122"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e0f02-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e0f02-123">Library</span></span><br/> | <dl> <span data-ttu-id="e0f02-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e0f02-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e0f02-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e0f02-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e0f02-126">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="e0f02-126">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




