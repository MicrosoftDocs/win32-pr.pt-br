---
description: Todos os dados de um fluxo específico foram renderizados.
ms.assetid: 46037d53-085d-4fd0-91a0-408702cbfce5
title: EC_COMPLETE (DShow. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7cd6d548a56173b9c6ea83426ddab3fa8556e312
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789901"
---
# <a name="ec_complete"></a><span data-ttu-id="0e632-103">EC \_ concluído</span><span class="sxs-lookup"><span data-stu-id="0e632-103">EC\_COMPLETE</span></span>

<span data-ttu-id="0e632-104">Todos os dados de um fluxo específico foram renderizados.</span><span class="sxs-lookup"><span data-stu-id="0e632-104">All data from a particular stream has been rendered.</span></span>

## <a name="parameters"></a><span data-ttu-id="0e632-105">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0e632-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0e632-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span><span class="sxs-lookup"><span data-stu-id="0e632-106"><span id="lParam1"></span><span id="lparam1"></span><span id="LPARAM1"></span>*lParam1*</span></span>
</dt> <dd>

<span data-ttu-id="0e632-107">(**HRESULT**) Status do fluxo na conclusão.</span><span class="sxs-lookup"><span data-stu-id="0e632-107">(**HRESULT**) Status of the stream on completion.</span></span> <span data-ttu-id="0e632-108">Se não ocorrerem erros durante a reprodução, o valor será S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0e632-108">If no errors occurred during playback, the value is S\_OK.</span></span>

</dd> <dt>

<span data-ttu-id="0e632-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span><span class="sxs-lookup"><span data-stu-id="0e632-109"><span id="lParam2"></span><span id="lparam2"></span><span id="LPARAM2"></span>*lParam2*</span></span>
</dt> <dd>

<span data-ttu-id="0e632-110">(**IUnknown** \* ) Zero, ou um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do processador.</span><span class="sxs-lookup"><span data-stu-id="0e632-110">(**IUnknown**\*) Zero, or a pointer to the renderer's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

</dd> </dl>

## <a name="default-action"></a><span data-ttu-id="0e632-111">Ação Padrão</span><span class="sxs-lookup"><span data-stu-id="0e632-111">Default Action</span></span>

<span data-ttu-id="0e632-112">Por padrão, o Gerenciador de gráfico de filtro não encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e632-112">By default, the filter graph manager does not forward this event to the application.</span></span> <span data-ttu-id="0e632-113">No entanto, depois que todos os fluxos no gráfico de relatório do grafo forem **\_ concluídos**, o Gerenciador de grafo de filtro posta um evento de **\_ conclusão de EC** separado para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="0e632-113">However, after all the streams in the graph report **EC\_COMPLETE**, the filter graph manager posts a separate **EC\_COMPLETE** event to the application.</span></span>

<span data-ttu-id="0e632-114">Se a ação padrão estiver desabilitada para esse evento, o aplicativo receberá todos os eventos de **\_ conclusão do EC** dos renderizadores.</span><span class="sxs-lookup"><span data-stu-id="0e632-114">If the default action is disabled for this event, the application receives all of the **EC\_COMPLETE** events from the renderers.</span></span>

## <a name="remarks"></a><span data-ttu-id="0e632-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0e632-115">Remarks</span></span>

<span data-ttu-id="0e632-116">Um filtro de renderizador envia esse evento quando recebe um aviso de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="0e632-116">A renderer filter sends this event when it receives an end-of-stream notice.</span></span> <span data-ttu-id="0e632-117">(O fim do fluxo é sinalizado por meio do método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .) O filtro envia exatamente um evento **EC \_ Complete** para cada fluxo.</span><span class="sxs-lookup"><span data-stu-id="0e632-117">(End-of-stream is signaled through the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.) The filter sends exactly one **EC\_COMPLETE** event for each stream.</span></span> <span data-ttu-id="0e632-118">O filtro deve processar quaisquer amostras pendentes antes de enviar o evento.</span><span class="sxs-lookup"><span data-stu-id="0e632-118">The filter must process any pending samples before it sends the event.</span></span> <span data-ttu-id="0e632-119">Parar um processador redefine qualquer estado de fim do fluxo que foi armazenado em cache.</span><span class="sxs-lookup"><span data-stu-id="0e632-119">Stopping a renderer resets any end-of-stream state that was cached.</span></span>

<span data-ttu-id="0e632-120">Se o renderizador estiver em pausa, ele não enviará o **EC \_ Complete** até que o método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) seja chamado.</span><span class="sxs-lookup"><span data-stu-id="0e632-120">If the renderer is paused, it does not send **EC\_COMPLETE** until the [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method is called.</span></span> <span data-ttu-id="0e632-121">Além disso, ele continua enviando eventos de **\_ conclusão do EC** para cada transição de pausa para executar, até que o filtro seja interrompido ou liberado.</span><span class="sxs-lookup"><span data-stu-id="0e632-121">Furthermore, it continues to send **EC\_COMPLETE** events for each transition from pause to run, until the filter is either stopped or flushed.</span></span>

<span data-ttu-id="0e632-122">Os filtros definem o parâmetro *lParam2* para um ponteiro [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) .</span><span class="sxs-lookup"><span data-stu-id="0e632-122">Filters set the *lParam2* parameter to an [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) pointer.</span></span> <span data-ttu-id="0e632-123">Se a ação padrão estiver habilitada, o Gerenciador de gráfico de filtro definirá esse parâmetro como zero.</span><span class="sxs-lookup"><span data-stu-id="0e632-123">If the default action is enabled, the filter graph manager sets this parameter to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="0e632-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0e632-124">Requirements</span></span>



| <span data-ttu-id="0e632-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="0e632-125">Requirement</span></span> | <span data-ttu-id="0e632-126">Valor</span><span class="sxs-lookup"><span data-stu-id="0e632-126">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="0e632-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0e632-127">Header</span></span><br/> | <dl> <span data-ttu-id="0e632-128"><dt>DShow. h</dt></span><span class="sxs-lookup"><span data-stu-id="0e632-128"><dt>Dshow.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0e632-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0e632-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0e632-130">Códigos de notificação de eventos</span><span class="sxs-lookup"><span data-stu-id="0e632-130">Event Notification Codes</span></span>](event-notification-codes.md)
</dt> <dt>

[<span data-ttu-id="0e632-131">Notificação de eventos no DirectShow</span><span class="sxs-lookup"><span data-stu-id="0e632-131">Event Notification in DirectShow</span></span>](event-notification-in-directshow.md)
</dt> <dt>

[<span data-ttu-id="0e632-132">Renderizadores de vídeo alternativos</span><span class="sxs-lookup"><span data-stu-id="0e632-132">Alternative Video Renderers</span></span>](alternative-video-renderers.md)
</dt> </dl>

 

 




