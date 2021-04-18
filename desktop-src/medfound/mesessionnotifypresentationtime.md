---
description: Gerado pela sessão de mídia quando uma nova apresentação é iniciada. Esse evento indica quando a apresentação será iniciada e o deslocamento entre a hora da apresentação e a hora da origem.
ms.assetid: 67c7d5f3-ffaf-4359-a59c-bb26b992b6cd
title: Evento MESessionNotifyPresentationTime (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a7b0cd8811d98094ab58ddcf844ec73e1470d120
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105752589"
---
# <a name="mesessionnotifypresentationtime-event"></a><span data-ttu-id="455da-104">Evento MESessionNotifyPresentationTime</span><span class="sxs-lookup"><span data-stu-id="455da-104">MESessionNotifyPresentationTime event</span></span>

<span data-ttu-id="455da-105">Gerado pela sessão de mídia quando uma nova apresentação é iniciada.</span><span class="sxs-lookup"><span data-stu-id="455da-105">Raised by the Media Session when a new presentation starts.</span></span> <span data-ttu-id="455da-106">Esse evento indica quando a apresentação será iniciada e o deslocamento entre a hora da apresentação e a hora da origem.</span><span class="sxs-lookup"><span data-stu-id="455da-106">This event indicates when the presentation will start and the offset between the presentation time and the source time.</span></span>

## <a name="event-values"></a><span data-ttu-id="455da-107">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="455da-107">Event values</span></span>

<span data-ttu-id="455da-108">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="455da-108">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="455da-109">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="455da-109">VARTYPE</span></span>              | <span data-ttu-id="455da-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="455da-110">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="455da-111">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="455da-111">VT\_EMPTY</span></span><br/> | <span data-ttu-id="455da-112">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="455da-112">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="455da-113">Atributos</span><span class="sxs-lookup"><span data-stu-id="455da-113">Attributes</span></span>

<span data-ttu-id="455da-114">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="455da-114">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="455da-115">Atributo</span><span class="sxs-lookup"><span data-stu-id="455da-115">Attribute</span></span>                                                                                                                   | <span data-ttu-id="455da-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="455da-116">Description</span></span>                                                                                                     |
|-----------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="455da-117">**\_hora de \_ início da \_ apresentação \_ do evento MF**</span><span class="sxs-lookup"><span data-stu-id="455da-117">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)<br/>                       | <span data-ttu-id="455da-118">Hora de início da apresentação.</span><span class="sxs-lookup"><span data-stu-id="455da-118">Starting time for the presentation.</span></span><br/> <br/>                                                      |
| [<span data-ttu-id="455da-119">**\_deslocamento do \_ tempo de apresentação do evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="455da-119">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)<br/>                     | <span data-ttu-id="455da-120">Deslocamento entre o tempo de apresentação e os carimbos de data/hora da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="455da-120">Offset between the presentation time and the media source's time stamps.</span></span><br/> <br/>                 |
| [<span data-ttu-id="455da-121">**\_ \_ \_ hora de início da apresentação do evento MF \_ \_ na \_ saída**</span><span class="sxs-lookup"><span data-stu-id="455da-121">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md)<br/> | <span data-ttu-id="455da-122">Hora da apresentação quando os coletores de mídia processarão o primeiro exemplo da nova topologia.</span><span class="sxs-lookup"><span data-stu-id="455da-122">Presentation time when the media sinks will render the first sample of the new topology.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="455da-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="455da-123">Requirements</span></span>



| <span data-ttu-id="455da-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="455da-124">Requirement</span></span> | <span data-ttu-id="455da-125">Valor</span><span class="sxs-lookup"><span data-stu-id="455da-125">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="455da-126">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="455da-126">Minimum supported client</span></span><br/> | <span data-ttu-id="455da-127">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="455da-127">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="455da-128">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="455da-128">Minimum supported server</span></span><br/> | <span data-ttu-id="455da-129">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="455da-129">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="455da-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="455da-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="455da-131"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="455da-131"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="455da-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="455da-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="455da-133">**IMFMediaSession**</span><span class="sxs-lookup"><span data-stu-id="455da-133">**IMFMediaSession**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfmediasession)
</dt> <dt>

[<span data-ttu-id="455da-134">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="455da-134">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




