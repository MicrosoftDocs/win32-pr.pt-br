---
description: Gerado quando uma fonte de mídia é iniciada sem busca.
ms.assetid: a52d8ee1-cb46-487d-a744-fca6db7c2353
title: Evento MESourceStarted (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c17ba7898a8bf33df4a3508afee9b7c0c9bc81c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502392"
---
# <a name="mesourcestarted-event"></a><span data-ttu-id="0c079-103">Evento MESourceStarted</span><span class="sxs-lookup"><span data-stu-id="0c079-103">MESourceStarted event</span></span>

<span data-ttu-id="0c079-104">Gerado quando uma fonte de mídia é iniciada sem busca.</span><span class="sxs-lookup"><span data-stu-id="0c079-104">Raised when a media source starts without seeking.</span></span>

## <a name="event-values"></a><span data-ttu-id="0c079-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="0c079-105">Event values</span></span>

<span data-ttu-id="0c079-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="0c079-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="0c079-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="0c079-107">VARTYPE</span></span>              | <span data-ttu-id="0c079-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c079-108">Description</span></span>                                                                                                    |
|----------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c079-109">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="0c079-109">VT\_EMPTY</span></span><br/> | <span data-ttu-id="0c079-110">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="0c079-110">No event data.</span></span> <span data-ttu-id="0c079-111">A hora de início foi a partir da posição atual.</span><span class="sxs-lookup"><span data-stu-id="0c079-111">The start time was from the current position.</span></span><br/> <br/>                            |
| <span data-ttu-id="0c079-112">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="0c079-112">VT\_I8</span></span><br/>    | <span data-ttu-id="0c079-113">A hora de início, em unidades de 100 nanossegundos, em relação aos carimbos de data/hora nos exemplos.</span><span class="sxs-lookup"><span data-stu-id="0c079-113">The starting time, in 100-nanosecond units, relative to the time stamps on the samples.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="0c079-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="0c079-114">Attributes</span></span>

<span data-ttu-id="0c079-115">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="0c079-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="0c079-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="0c079-116">Attribute</span></span>                                                                                     | <span data-ttu-id="0c079-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0c079-117">Description</span></span>                                                                                                                           |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0c079-118">**\_ \_ início real da origem do evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c079-118">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)<br/> | <span data-ttu-id="0c079-119">Hora de início.</span><span class="sxs-lookup"><span data-stu-id="0c079-119">Start time.</span></span> <span data-ttu-id="0c079-120">A origem de mídia define esse atributo se ele for reiniciado a partir de sua posição atual.</span><span class="sxs-lookup"><span data-stu-id="0c079-120">The media source sets this attribute if it restarts from its current position.</span></span><br/> <br/>                     |
| [<span data-ttu-id="0c079-121">**\_ \_ Início falso da origem do evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="0c079-121">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)<br/>     | <span data-ttu-id="0c079-122">Especifica se a topologia de segmento atual está vazia.</span><span class="sxs-lookup"><span data-stu-id="0c079-122">Specifies whether the current segment topology is empty.</span></span> <span data-ttu-id="0c079-123">A origem do sequenciador define esse atributo.</span><span class="sxs-lookup"><span data-stu-id="0c079-123">The sequencer source sets this attribute.</span></span><br/> <br/>             |
| [<span data-ttu-id="0c079-124">**\_origem do evento MF \_ \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="0c079-124">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)<br/>  | <span data-ttu-id="0c079-125">Hora de início de um segmento, em relação ao início da apresentação.</span><span class="sxs-lookup"><span data-stu-id="0c079-125">Start time for a segment, relative to the start of the presentation.</span></span> <span data-ttu-id="0c079-126">A origem do sequenciador define esse atributo.</span><span class="sxs-lookup"><span data-stu-id="0c079-126">The sequencer source sets this attribute.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="0c079-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="0c079-127">Remarks</span></span>

<span data-ttu-id="0c079-128">Uma origem de mídia gera esse evento quando ele é iniciado a partir de um estado parado ou inicia de um estado em pausa na mesma posição na origem.</span><span class="sxs-lookup"><span data-stu-id="0c079-128">A media source raises this event when it starts from a stopped state, or starts from a paused state at the same position in the source.</span></span> <span data-ttu-id="0c079-129">O evento será gerado se o método [**IMFMediaSource:: Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) retornar S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="0c079-129">The event is raised if the [**IMFMediaSource::Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method returns S\_OK.</span></span>

<span data-ttu-id="0c079-130">Se a origem da mídia iniciar a partir da posição atual e o estado anterior da origem estiver em execução ou em pausa, os dados do evento poderão ser vazios (VT \_ vazio).</span><span class="sxs-lookup"><span data-stu-id="0c079-130">If the media source starts from the current position and the source's previous state was running or paused, the event data can empty (VT\_EMPTY).</span></span> <span data-ttu-id="0c079-131">Se os dados do evento forem VT \_ vazio, a origem da mídia poderá definir o atributo de [**\_ \_ \_ \_ início real da origem do evento MF**](mf-event-source-actual-start-attribute.md) com a hora de início real.</span><span class="sxs-lookup"><span data-stu-id="0c079-131">If the event data is VT\_EMPTY, the media source might set the [**MF\_EVENT\_SOURCE\_ACTUAL\_START**](mf-event-source-actual-start-attribute.md) attribute with the actual starting time.</span></span>

<span data-ttu-id="0c079-132">Se a origem da mídia iniciar a partir de uma nova posição ou se o estado anterior da origem tiver sido interrompido, os dados do evento deverão ser a hora de início (VT \_ i8).</span><span class="sxs-lookup"><span data-stu-id="0c079-132">If the media source starts from a new position, or the source's previous state was stopped, the event data must be the starting time (VT\_I8).</span></span>

<span data-ttu-id="0c079-133">Se o método [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) fizer uma busca, a origem da mídia enviará o evento [MESourceSeeked](mesourceseeked.md) em vez de MESourceStarted.</span><span class="sxs-lookup"><span data-stu-id="0c079-133">If the [**Start**](/windows/desktop/api/mfidl/nf-mfidl-imfmediasource-start) method causes a seek, the media source sends the [MESourceSeeked](mesourceseeked.md) event instead of MESourceStarted.</span></span>

## <a name="requirements"></a><span data-ttu-id="0c079-134">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0c079-134">Requirements</span></span>



| <span data-ttu-id="0c079-135">Requisito</span><span class="sxs-lookup"><span data-stu-id="0c079-135">Requirement</span></span> | <span data-ttu-id="0c079-136">Valor</span><span class="sxs-lookup"><span data-stu-id="0c079-136">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0c079-137">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c079-137">Minimum supported client</span></span><br/> | <span data-ttu-id="0c079-138">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="0c079-138">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="0c079-139">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="0c079-139">Minimum supported server</span></span><br/> | <span data-ttu-id="0c079-140">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="0c079-140">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="0c079-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0c079-141">Header</span></span><br/>                   | <dl> <span data-ttu-id="0c079-142"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0c079-142"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0c079-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="0c079-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0c079-144">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="0c079-144">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




