---
description: Gerado por um objeto do habilitador de conteúdo quando os objetos que habilitam a ação são concluídos.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f05459a648f6b357fd483baa9fc56809540e64a1
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/30/2021
ms.locfileid: "113119441"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="12c80-103">Evento MEEnablerCompleted</span><span class="sxs-lookup"><span data-stu-id="12c80-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="12c80-104">Gerado por um objeto do habilitador de conteúdo quando a ação de habilitação do objeto é concluída.</span><span class="sxs-lookup"><span data-stu-id="12c80-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="12c80-105">Objetos que expõem a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) podem autenuá-lo.</span><span class="sxs-lookup"><span data-stu-id="12c80-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="12c80-106">O evento será gerado se um dos seguintes eventos ocorrer:</span><span class="sxs-lookup"><span data-stu-id="12c80-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="12c80-107">O [**método IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="12c80-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="12c80-108">O aplicativo chama [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)e, em seguida, o aplicativo conclui a solicitação HTTP POST, conforme descrito no **método MonitorEnable.**</span><span class="sxs-lookup"><span data-stu-id="12c80-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="12c80-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="12c80-109">Event values</span></span>

<span data-ttu-id="12c80-110">Os valores possíveis recuperados [**de IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="12c80-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="12c80-111">Vartype</span><span class="sxs-lookup"><span data-stu-id="12c80-111">VARTYPE</span></span>              | <span data-ttu-id="12c80-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="12c80-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="12c80-113">VT \_ VAZIO</span><span class="sxs-lookup"><span data-stu-id="12c80-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="12c80-114">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="12c80-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="12c80-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="12c80-115">Remarks</span></span>

<span data-ttu-id="12c80-116">O código de status do evento pode conter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="12c80-116">The status code from the event may contain one of the following values.</span></span>



| <span data-ttu-id="12c80-117">Valor</span><span class="sxs-lookup"><span data-stu-id="12c80-117">Value</span></span>                                     | <span data-ttu-id="12c80-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="12c80-118">Description</span></span>                                                                                                                                                                                |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12c80-119">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="12c80-119">**S\_OK**</span></span>                            | <span data-ttu-id="12c80-120">A operação foi realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="12c80-120">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="12c80-121">**NS \_ E \_ DRM \_ LICENSE \_ NOTACQUIRED**</span><span class="sxs-lookup"><span data-stu-id="12c80-121">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="12c80-122">A licença drm não foi adquirida.</span><span class="sxs-lookup"><span data-stu-id="12c80-122">The DRM license was not acquired.</span></span> <span data-ttu-id="12c80-123">Se a tentativa anterior tiver [**usado AutomaticEnable,**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable)o aplicativo deverá tentar a aquisição não silenciosa.</span><span class="sxs-lookup"><span data-stu-id="12c80-123">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="12c80-124">**NS \_ S \_ DRM \_ MONITOR \_ CANCELLED**</span><span class="sxs-lookup"><span data-stu-id="12c80-124">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="12c80-125">A [**operação MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="12c80-125">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="12c80-126">Para receber esse evento, consulte a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para a interface [**IMFMediaEventGenerator.**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator)</span><span class="sxs-lookup"><span data-stu-id="12c80-126">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="12c80-127">Em seguida, [**chame IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), conforme descrito no tópico [Geradores](media-event-generators.md)de Eventos de Mídia .</span><span class="sxs-lookup"><span data-stu-id="12c80-127">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="12c80-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="12c80-128">Requirements</span></span>



| <span data-ttu-id="12c80-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="12c80-129">Requirement</span></span> | <span data-ttu-id="12c80-130">Valor</span><span class="sxs-lookup"><span data-stu-id="12c80-130">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="12c80-131">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12c80-131">Minimum supported client</span></span><br/> | <span data-ttu-id="12c80-132">Somente \[ aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="12c80-132">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="12c80-133">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="12c80-133">Minimum supported server</span></span><br/> | <span data-ttu-id="12c80-134">Somente aplicativos da área de trabalho do Windows Server 2008 \[\]</span><span class="sxs-lookup"><span data-stu-id="12c80-134">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="12c80-135">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="12c80-135">Header</span></span><br/>                   | <dl> <span data-ttu-id="12c80-136"><dt>Mfobjects.h (inclua Mfidl.h)</dt></span><span class="sxs-lookup"><span data-stu-id="12c80-136"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="12c80-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="12c80-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="12c80-138">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="12c80-138">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="12c80-139">Geradores de eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="12c80-139">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="12c80-140">Media Foundation eventos</span><span class="sxs-lookup"><span data-stu-id="12c80-140">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




