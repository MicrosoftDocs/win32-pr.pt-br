---
description: Sinaliza que um fluxo de mídia não tem dados disponíveis em um horário especificado.
ms.assetid: 1a00fff1-c3ab-4965-a663-3c15bb48ea98
title: Evento MEStreamTick (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 27123569e991043a534883964ba94e4955d60a40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105793395"
---
# <a name="mestreamtick-event"></a><span data-ttu-id="48680-103">Evento MEStreamTick</span><span class="sxs-lookup"><span data-stu-id="48680-103">MEStreamTick event</span></span>

<span data-ttu-id="48680-104">Sinaliza que um fluxo de mídia não tem dados disponíveis em um horário especificado.</span><span class="sxs-lookup"><span data-stu-id="48680-104">Signals that a media stream does not have data available at a specified time.</span></span>

## <a name="event-values"></a><span data-ttu-id="48680-105">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="48680-105">Event values</span></span>

<span data-ttu-id="48680-106">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="48680-106">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="48680-107">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="48680-107">VARTYPE</span></span>           | <span data-ttu-id="48680-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="48680-108">Description</span></span>                                                                   |
|-------------------|-------------------------------------------------------------------------------|
| <span data-ttu-id="48680-109">VT \_ i8</span><span class="sxs-lookup"><span data-stu-id="48680-109">VT\_I8</span></span><br/> | <span data-ttu-id="48680-110">Hora em que a lacuna ocorre, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="48680-110">Time at which the gap occurs, in 100-nanosecond units.</span></span><br/> <br/> |



## <a name="remarks"></a><span data-ttu-id="48680-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="48680-111">Remarks</span></span>

<span data-ttu-id="48680-112">Esse evento sinaliza uma lacuna nos dados.</span><span class="sxs-lookup"><span data-stu-id="48680-112">This event signals a gap in the data.</span></span> <span data-ttu-id="48680-113">O evento notifica os componentes downstream para não esperar nenhum dado no tempo especificado.</span><span class="sxs-lookup"><span data-stu-id="48680-113">The event notifies downstream components not to expect any data at the specified time.</span></span>

<span data-ttu-id="48680-114">O evento deve ser enviado por qualquer objeto que gere os carimbos de data/hora para os exemplos de mídia no fluxo.</span><span class="sxs-lookup"><span data-stu-id="48680-114">The event should be sent by whichever object generates the time stamps for the media samples in the stream.</span></span> <span data-ttu-id="48680-115">Dependendo do formato dos dados, isso é o seguinte:</span><span class="sxs-lookup"><span data-stu-id="48680-115">Depending on the format of the data, this is either:</span></span>

-   <span data-ttu-id="48680-116">O fluxo de mídia na origem da mídia (interface [**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) ) ou</span><span class="sxs-lookup"><span data-stu-id="48680-116">The media stream on the media source ([**IMFMediaStream**](/windows/desktop/api/mfidl/nn-mfidl-imfmediastream) interface), or</span></span>
-   <span data-ttu-id="48680-117">A transformação do decodificador (interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) ).</span><span class="sxs-lookup"><span data-stu-id="48680-117">The decoder transform ([**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface).</span></span>

<span data-ttu-id="48680-118">Durante a lacuna, o objeto deve enviar o evento, com a frequência em que normalmente produziria amostras.</span><span class="sxs-lookup"><span data-stu-id="48680-118">During the gap, the object should send the event about as often as it would normally produce samples.</span></span> <span data-ttu-id="48680-119">Para vídeo, envie um evento para cada quadro ausente.</span><span class="sxs-lookup"><span data-stu-id="48680-119">For video, send one event for each missing frame.</span></span> <span data-ttu-id="48680-120">Para áudio, envie o evento pelo menos uma vez por segundo durante o intervalo.</span><span class="sxs-lookup"><span data-stu-id="48680-120">For audio, send the event at least once per second during the gap.</span></span> <span data-ttu-id="48680-121">O valor do evento é o carimbo de data/hora do exemplo ausente.</span><span class="sxs-lookup"><span data-stu-id="48680-121">The value of the event is the time stamp of the missing sample.</span></span> <span data-ttu-id="48680-122">Envie quantos eventos MEStreamTick forem necessários para preencher a lacuna nos dados.</span><span class="sxs-lookup"><span data-stu-id="48680-122">Send as many MEStreamTick events as needed to fill the gap in the data.</span></span>

<span data-ttu-id="48680-123">Se uma fonte de mídia tiver vários fluxos e houver um intervalo em mais de um fluxo, cada fluxo deverá enviar eventos MEStreamTick.</span><span class="sxs-lookup"><span data-stu-id="48680-123">If a media source has several streams and there is a gap in more than one stream, each stream should send MEStreamTick events.</span></span> <span data-ttu-id="48680-124">Por exemplo, se houver uma lacuna nos dados de áudio e de vídeo, ambos os fluxos enviarão o evento.</span><span class="sxs-lookup"><span data-stu-id="48680-124">For example, if there is a gap in both audio and video data, then both streams send the event.</span></span>

<span data-ttu-id="48680-125">O evento MEStreamTick não conclui uma solicitação [**IMFMediaStream:: RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) .</span><span class="sxs-lookup"><span data-stu-id="48680-125">The MEStreamTick event does not complete an [**IMFMediaStream::RequestSample**](/windows/desktop/api/mfidl/nf-mfidl-imfmediastream-requestsample) request.</span></span> <span data-ttu-id="48680-126">A origem da mídia ainda deve enviar um evento [MEMediaSample](memediasample.md) para cada chamada para **RequestSample**.</span><span class="sxs-lookup"><span data-stu-id="48680-126">The media source must still send an [MEMediaSample](memediasample.md) event for each call to **RequestSample**.</span></span>

<span data-ttu-id="48680-127">Os coletores de mídia não podem consumir esse evento diretamente.</span><span class="sxs-lookup"><span data-stu-id="48680-127">Media sinks cannot consume this event directly.</span></span> <span data-ttu-id="48680-128">Para sinalizar uma lacuna no fluxo para um coletor de mídia, chame [**IMFStreamSink::P lacemarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) com um marcador de **\_ \_ tique MFSTREAMSINK** .</span><span class="sxs-lookup"><span data-stu-id="48680-128">To signal a gap in the stream to a media sink, call [**IMFStreamSink::PlaceMarker**](/windows/desktop/api/mfidl/nf-mfidl-imfstreamsink-placemarker) with an **MFSTREAMSINK\_MARKER\_TICK** marker.</span></span> <span data-ttu-id="48680-129">O pipeline de Media Foundation converte eventos MEStreamTick em marcadores de **\_ \_ tique de marcador MFSTREAMSINK** quando necessário.</span><span class="sxs-lookup"><span data-stu-id="48680-129">The Media Foundation pipeline converts MEStreamTick events to **MFSTREAMSINK\_MARKER\_TICK** markers when needed.</span></span>

<span data-ttu-id="48680-130">Não defina o atributo [**de \_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) no próximo exemplo de mídia após um evento MEStreamTick.</span><span class="sxs-lookup"><span data-stu-id="48680-130">Do not set the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute on the next media sample after an MEStreamTick event.</span></span> <span data-ttu-id="48680-131">O atributo de **\_ descontinuidade MFSampleExtension** implica que o carimbo de data/hora é descontínuo com carimbos de data/hora anteriores, enquanto MEStreamTick implica que os carimbos de hora são contínuos, mas alguns dados estão ausentes</span><span class="sxs-lookup"><span data-stu-id="48680-131">The **MFSampleExtension\_Discontinuity** attribute implies that the time stamp is discontinuous with previous time stamps, whereas MEStreamTick implies that time stamps are continuous but some data is missing.</span></span>

> [!Note]  
> <span data-ttu-id="48680-132">Uma versão anterior da documentação incorretamente afirmou que o exemplo depois de um evento MEStreamTick deve ter o atributo [**de \_ descontinuidade MFSampleExtension**](mfsampleextension-discontinuity-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="48680-132">An earlier version of the documentation incorrectly stated that the sample after an MEStreamTick event should have the [**MFSampleExtension\_Discontinuity**](mfsampleextension-discontinuity-attribute.md) attribute.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="48680-133">Requisitos</span><span class="sxs-lookup"><span data-stu-id="48680-133">Requirements</span></span>



| <span data-ttu-id="48680-134">Requisito</span><span class="sxs-lookup"><span data-stu-id="48680-134">Requirement</span></span> | <span data-ttu-id="48680-135">Valor</span><span class="sxs-lookup"><span data-stu-id="48680-135">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="48680-136">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48680-136">Minimum supported client</span></span><br/> | <span data-ttu-id="48680-137">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="48680-137">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="48680-138">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="48680-138">Minimum supported server</span></span><br/> | <span data-ttu-id="48680-139">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="48680-139">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="48680-140">parâmetro</span><span class="sxs-lookup"><span data-stu-id="48680-140">Header</span></span><br/>                   | <dl> <span data-ttu-id="48680-141"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="48680-141"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="48680-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="48680-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="48680-143">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="48680-143">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> </dl>

 

 




