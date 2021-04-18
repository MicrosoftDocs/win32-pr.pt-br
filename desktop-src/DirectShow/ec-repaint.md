---
description: Um processador de vídeo requer um redesenho.
ms.assetid: 2e756dea-366c-4024-8fc8-6feabaef1954
title: EC_REPAINT (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ba86b54d6d465330ec1635ed7301ce774ef7cb27
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760095"
---
# <a name="ec_repaint"></a><span data-ttu-id="69a68-103">redesenho de EC \_</span><span class="sxs-lookup"><span data-stu-id="69a68-103">EC\_REPAINT</span></span>

<span data-ttu-id="69a68-104">Um processador de vídeo requer um redesenho.</span><span class="sxs-lookup"><span data-stu-id="69a68-104">A video renderer requires a repaint.</span></span>

## <a name="parameters"></a><span data-ttu-id="69a68-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="69a68-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="69a68-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="69a68-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="69a68-107">(**IUnknown** \* ) Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada do processador de vídeo ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="69a68-107">(**IUnknown**\*) Pointer to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface of the video renderer's input pin, or **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="69a68-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="69a68-108"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="69a68-109">Zero.</span><span class="sxs-lookup"><span data-stu-id="69a68-109">Zero.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="69a68-110">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="69a68-110">Default Action</span></span>

<span data-ttu-id="69a68-111">O parâmetro *lParam1* pode especificar o pino de entrada do processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="69a68-111">The *lParam1* parameter might specify the video renderer's input pin.</span></span> <span data-ttu-id="69a68-112">Nesse caso, o Gerenciador do grafo de filtro localiza o pino de saída conectado a esse PIN e o consulta para a interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="69a68-112">If so, the filter graph manager finds the output pin connected to that pin and queries it for the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span> <span data-ttu-id="69a68-113">Se o pino de saída der suporte a **IMediaEventSink**, o Gerenciador de gráfico de filtro chamará [**IMediaEventSink:: Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) com o código de evento do EC \_ Repaint.</span><span class="sxs-lookup"><span data-stu-id="69a68-113">If the output pin supports **IMediaEventSink**, the filter graph manager calls [**IMediaEventSink::Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) with the EC\_REPAINT event code.</span></span> <span data-ttu-id="69a68-114">Isso dá ao filtro upstream a oportunidade de enviar novamente o último exemplo.</span><span class="sxs-lookup"><span data-stu-id="69a68-114">This gives the upstream filter the opportunity to re-send the last sample.</span></span>

<span data-ttu-id="69a68-115">Se *lParam1* for **nulo** ou se o PIN não oferecer suporte a [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), ou se o método [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) falhar, o Gerenciador do grafo de filtro tratará o \_ evento Repaint do EC por si só.</span><span class="sxs-lookup"><span data-stu-id="69a68-115">If *lParam1* is **NULL**, or if the pin does not support [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink), or if the [**Notify**](/windows/desktop/api/Strmif/nf-strmif-imediaeventsink-notify) method fails, the filter graph manager handles the EC\_REPAINT event by itself.</span></span> <span data-ttu-id="69a68-116">Seu comportamento depende do estado do grafo:</span><span class="sxs-lookup"><span data-stu-id="69a68-116">Its behavior depends on the state of the graph:</span></span>

-   <span data-ttu-id="69a68-117">Em execução: ignora o evento.</span><span class="sxs-lookup"><span data-stu-id="69a68-117">Running: Ignores the event.</span></span> <span data-ttu-id="69a68-118">(O renderizador receberá o próximo exemplo no fluxo.)</span><span class="sxs-lookup"><span data-stu-id="69a68-118">(The renderer will receive the next sample in the stream.)</span></span>
-   <span data-ttu-id="69a68-119">Em pausa: procura o grafo em seu local atual, liberando, assim, o filtro e colocando os dados em fila novamente.</span><span class="sxs-lookup"><span data-stu-id="69a68-119">Paused: Seeks the graph to its current location, thereby flushing the filter and re-queuing the data.</span></span>
-   <span data-ttu-id="69a68-120">Parado: pausa e para o grafo, assim, colocando novamente os dados em fila.</span><span class="sxs-lookup"><span data-stu-id="69a68-120">Stopped: Pauses and stops the graph, thereby re-queuing the data.</span></span>

<span data-ttu-id="69a68-121">Por padrão, o Gerenciador de gráfico de filtro não passa esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="69a68-121">By default, the filter graph manager does not pass this event to the application.</span></span>

## <a name="remarks"></a><span data-ttu-id="69a68-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="69a68-122">Remarks</span></span>

<span data-ttu-id="69a68-123">Os renderizadores de vídeo enviam essa mensagem quando recebem uma mensagem do [**WM \_ Paint**](/windows/desktop/gdi/wm-paint) e não têm dados a serem exibidos.</span><span class="sxs-lookup"><span data-stu-id="69a68-123">Video renderers send this message when they receive a [**WM\_PAINT**](/windows/desktop/gdi/wm-paint) message and have no data to display.</span></span>

## <a name="requirements"></a><span data-ttu-id="69a68-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="69a68-124">Requirements</span></span>



| <span data-ttu-id="69a68-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="69a68-125">Requirement</span></span> | <span data-ttu-id="69a68-126">Valor</span><span class="sxs-lookup"><span data-stu-id="69a68-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="69a68-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="69a68-127">Header</span></span><br/> | <dl> <span data-ttu-id="69a68-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="69a68-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="69a68-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="69a68-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="69a68-130">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="69a68-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="69a68-131">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="69a68-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> </dl>

 

