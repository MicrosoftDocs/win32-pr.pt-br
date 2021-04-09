---
description: Gerado por um objeto de habilitador de conteúdo quando a ação de habilitar objetos é concluída.
ms.assetid: 5162800c-9c55-40de-be66-a98765324f76
title: Evento MEEnablerCompleted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5a74f7379ccc2983abd2327e1250bcf1ca14e688
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104091169"
---
# <a name="meenablercompleted-event"></a><span data-ttu-id="2b8f5-103">Evento MEEnablerCompleted</span><span class="sxs-lookup"><span data-stu-id="2b8f5-103">MEEnablerCompleted event</span></span>

<span data-ttu-id="2b8f5-104">Gerado por um objeto de habilitador de conteúdo quando a ação de habilitação do objeto é concluída.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-104">Raised by a content enabler object when the object's enabling action is completed.</span></span> <span data-ttu-id="2b8f5-105">Os objetos que expõem a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) podem gerar esse evento.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-105">Objects that expose the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface can raise this event.</span></span> <span data-ttu-id="2b8f5-106">O evento será gerado se ocorrer um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="2b8f5-106">The event is raised if either of the following occurs:</span></span>

-   <span data-ttu-id="2b8f5-107">O método [**IMFContentEnabler:: AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) é concluído de forma assíncrona.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-107">The [**IMFContentEnabler::AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable) method completes asynchronously.</span></span>
-   <span data-ttu-id="2b8f5-108">O aplicativo chama [**IMFContentEnabler:: MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable)e, em seguida, o aplicativo conclui a solicitação HTTP post, conforme descrito no método **MonitorEnable** .</span><span class="sxs-lookup"><span data-stu-id="2b8f5-108">The application calls [**IMFContentEnabler::MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable), and then the application completes the HTTP POST request, as described in the **MonitorEnable** method.</span></span>

## <a name="event-values"></a><span data-ttu-id="2b8f5-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="2b8f5-109">Event values</span></span>

<span data-ttu-id="2b8f5-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="2b8f5-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="2b8f5-111">VARTYPE</span></span>              | <span data-ttu-id="2b8f5-112">Description</span><span class="sxs-lookup"><span data-stu-id="2b8f5-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="2b8f5-113">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="2b8f5-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="2b8f5-114">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-114">No event data.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="2b8f5-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="2b8f5-115">Remarks</span></span>

<span data-ttu-id="2b8f5-116">O código de status do evento pode conter um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-116">The status code from the event may contain one of the following values.</span></span>



|                                      |                                                                                                                                                                                 |
|--------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8f5-117">**S \_ OK**</span><span class="sxs-lookup"><span data-stu-id="2b8f5-117">**S\_OK**</span></span>                            | <span data-ttu-id="2b8f5-118">A operação foi realizada com êxito.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-118">The operation succeeded.</span></span>                                                                                                                                                        |
| <span data-ttu-id="2b8f5-119">**licença do NS \_ E \_ DRM não \_ \_ adquirida**</span><span class="sxs-lookup"><span data-stu-id="2b8f5-119">**NS\_E\_DRM\_LICENSE\_NOTACQUIRED**</span></span> | <span data-ttu-id="2b8f5-120">A licença de DRM não foi adquirida.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-120">The DRM license was not acquired.</span></span> <span data-ttu-id="2b8f5-121">Se a tentativa anterior usou [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), o aplicativo deve tentar uma aquisição não silenciosa.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-121">If the previous attempt used [**AutomaticEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-automaticenable), the application should try non-silent acquisition.</span></span> |
| <span data-ttu-id="2b8f5-122">**MONITOR de DRM do NS \_ S \_ \_ \_ cancelado**</span><span class="sxs-lookup"><span data-stu-id="2b8f5-122">**NS\_S\_DRM\_MONITOR\_CANCELLED**</span></span>   | <span data-ttu-id="2b8f5-123">A operação [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) foi cancelada.</span><span class="sxs-lookup"><span data-stu-id="2b8f5-123">The [**MonitorEnable**](/windows/desktop/api/mfidl/nf-mfidl-imfcontentenabler-monitorenable) operation was canceled.</span></span>                                                                                            |



 

<span data-ttu-id="2b8f5-124">Para receber esse evento, consulte a interface [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) para a interface [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) .</span><span class="sxs-lookup"><span data-stu-id="2b8f5-124">To receive this event, query the [**IMFContentEnabler**](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler) interface for the [**IMFMediaEventGenerator**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaeventgenerator) interface.</span></span> <span data-ttu-id="2b8f5-125">Em seguida, chame [**IMFMediaEventGenerator:: BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), conforme descrito no tópico [geradores de eventos de mídia](media-event-generators.md).</span><span class="sxs-lookup"><span data-stu-id="2b8f5-125">Then call [**IMFMediaEventGenerator::BeginGetEvent**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaeventgenerator-begingetevent), as described in the topic [Media Event Generators](media-event-generators.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2b8f5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b8f5-126">Requirements</span></span>



| <span data-ttu-id="2b8f5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b8f5-127">Requirement</span></span> | <span data-ttu-id="2b8f5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="2b8f5-128">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b8f5-129">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b8f5-129">Minimum supported client</span></span><br/> | <span data-ttu-id="2b8f5-130">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="2b8f5-130">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="2b8f5-131">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="2b8f5-131">Minimum supported server</span></span><br/> | <span data-ttu-id="2b8f5-132">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="2b8f5-132">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="2b8f5-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b8f5-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="2b8f5-134"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b8f5-134"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b8f5-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b8f5-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b8f5-136">**IMFContentEnabler**</span><span class="sxs-lookup"><span data-stu-id="2b8f5-136">**IMFContentEnabler**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfcontentenabler)
</dt> <dt>

[<span data-ttu-id="2b8f5-137">Geradores de eventos de mídia</span><span class="sxs-lookup"><span data-stu-id="2b8f5-137">Media Event Generators</span></span>](media-event-generators.md)
</dt> <dt>

[<span data-ttu-id="2b8f5-138">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="2b8f5-138">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




