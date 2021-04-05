---
description: Sinaliza um evento de um coletor de mídia que renderiza dados de mídia.
ms.assetid: bb7db7c9-c39f-4bf4-9412-42525c4f2ea3
title: Evento MERendererEvent (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c52e15bfbe97743e8af10a79cf3ef1d94626a877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104165043"
---
# <a name="merendererevent-event"></a><span data-ttu-id="3f006-103">Evento MERendererEvent</span><span class="sxs-lookup"><span data-stu-id="3f006-103">MERendererEvent event</span></span>

<span data-ttu-id="3f006-104">Sinaliza um evento de um coletor de mídia que renderiza dados de mídia.</span><span class="sxs-lookup"><span data-stu-id="3f006-104">Signals an event from a media sink that renders media data.</span></span>

<span data-ttu-id="3f006-105">O [processador de vídeo avançado](enhanced-video-renderer.md) (EVR) envia esse evento quando recebe um evento de usuário do apresentador EVR.</span><span class="sxs-lookup"><span data-stu-id="3f006-105">The [Enhanced Video Renderer](enhanced-video-renderer.md) (EVR) sends this event when it receives a user event from the EVR presenter.</span></span>

## <a name="event-values"></a><span data-ttu-id="3f006-106">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="3f006-106">Event values</span></span>

<span data-ttu-id="3f006-107">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="3f006-107">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="3f006-108">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="3f006-108">VARTYPE</span></span>           | <span data-ttu-id="3f006-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3f006-109">Description</span></span>                        |
|-------------------|------------------------------------|
| <span data-ttu-id="3f006-110">\_I4 VT</span><span class="sxs-lookup"><span data-stu-id="3f006-110">VT\_I4</span></span><br/> | <span data-ttu-id="3f006-111">Código do evento.</span><span class="sxs-lookup"><span data-stu-id="3f006-111">Event code.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="3f006-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="3f006-112">Remarks</span></span>

<span data-ttu-id="3f006-113">Se o apresentador chama o método **IMediaEventSink:: Notify** do EVR com um código de evento no intervalo do usuário do EC \_ ou superior, o EVR envia esse evento.</span><span class="sxs-lookup"><span data-stu-id="3f006-113">If the presenter calls the EVR's **IMediaEventSink::Notify** method with an event code in the range EC\_USER or higher, the EVR sends this event.</span></span> <span data-ttu-id="3f006-114">Os dados do evento são o código do evento que foi passado para o método **Notify** .</span><span class="sxs-lookup"><span data-stu-id="3f006-114">The event data is the event code that was passed to the **Notify** method.</span></span>

<span data-ttu-id="3f006-115">Os parâmetros de evento original (*EventParam1* e *EventParam2* no método **IMediaEventSink:: Notify** ) são ignorados, portanto, o apresentador deve definir esses valores como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="3f006-115">The original event parameters (*EventParam1* and *EventParam2* in the **IMediaEventSink::Notify** method) are ignored, so the presenter should set these values to **NULL**.</span></span>

## <a name="requirements"></a><span data-ttu-id="3f006-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3f006-116">Requirements</span></span>



| <span data-ttu-id="3f006-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="3f006-117">Requirement</span></span> | <span data-ttu-id="3f006-118">Valor</span><span class="sxs-lookup"><span data-stu-id="3f006-118">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3f006-119">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f006-119">Minimum supported client</span></span><br/> | <span data-ttu-id="3f006-120">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="3f006-120">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="3f006-121">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3f006-121">Minimum supported server</span></span><br/> | <span data-ttu-id="3f006-122">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="3f006-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="3f006-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3f006-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="3f006-124"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3f006-124"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3f006-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="3f006-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3f006-126">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="3f006-126">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




