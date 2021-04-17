---
description: Gerado por um coletor de fluxo quando ele conclui uma solicitação de depuração.
ms.assetid: 451c7e09-868e-4c05-b970-d222b97223f2
title: Evento MEStreamSinkScrubSampleComplete (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 81f29d478635d5a9ba7e7c5356c49ebd8da216f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105812803"
---
# <a name="mestreamsinkscrubsamplecomplete-event"></a><span data-ttu-id="c5305-103">Evento MEStreamSinkScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="c5305-103">MEStreamSinkScrubSampleComplete event</span></span>

<span data-ttu-id="c5305-104">Gerado por um coletor de fluxo quando ele conclui uma solicitação de depuração.</span><span class="sxs-lookup"><span data-stu-id="c5305-104">Raised by a stream sink when it completes a scrubbing request.</span></span>

<span data-ttu-id="c5305-105">A depuração ocorre quando a taxa de reprodução é zero e o relógio de apresentação é iniciado com um horário de srubbing especificado.</span><span class="sxs-lookup"><span data-stu-id="c5305-105">Scrubbing occurs when the playback rate is zero and the presentation clock is started with a specified srubbing time.</span></span> <span data-ttu-id="c5305-106">Se um coletor de mídia der suporte à depuração, cada fluxo do coletor gerará esse evento sempre que o método [**IMFClockStateSink:: OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) for chamado enquanto a taxa de reprodução for zero.</span><span class="sxs-lookup"><span data-stu-id="c5305-106">If a media sink supports scrubbing, every stream on the sink raises this event whenever the [**IMFClockStateSink::OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) method is called while the playback rate is zero.</span></span>

<span data-ttu-id="c5305-107">Se o fluxo renderiza dados durante a limpeza, ele envia o evento assim que os dados são renderizados.</span><span class="sxs-lookup"><span data-stu-id="c5305-107">If the stream renders data while scrubbing, it sends the event as soon as the data is rendered.</span></span> <span data-ttu-id="c5305-108">Se o fluxo não renderizar dados, ele envia o evento imediatamente após a chamada de [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) .</span><span class="sxs-lookup"><span data-stu-id="c5305-108">If the stream does not render data, it sends the event immediately after [**OnClockStart**](/windows/desktop/api/mfidl/nf-mfidl-imfclockstatesink-onclockstart) is called.</span></span>

## <a name="event-values"></a><span data-ttu-id="c5305-109">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="c5305-109">Event values</span></span>

<span data-ttu-id="c5305-110">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="c5305-110">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="c5305-111">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="c5305-111">VARTYPE</span></span>              | <span data-ttu-id="c5305-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5305-112">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="c5305-113">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="c5305-113">VT\_EMPTY</span></span><br/> | <span data-ttu-id="c5305-114">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="c5305-114">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="c5305-115">Atributos</span><span class="sxs-lookup"><span data-stu-id="c5305-115">Attributes</span></span>

<span data-ttu-id="c5305-116">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="c5305-116">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="c5305-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="c5305-117">Attribute</span></span>                                                                              | <span data-ttu-id="c5305-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="c5305-118">Description</span></span>                                                                                                                                                   |
|----------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c5305-119">**\_tempo de \_ SCRUBSAMPLE do evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="c5305-119">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)<br/> | <span data-ttu-id="c5305-120">Tempo de apresentação para o qual os dados foram renderizados.</span><span class="sxs-lookup"><span data-stu-id="c5305-120">Presentation time for which data was rendered.</span></span> <span data-ttu-id="c5305-121">Se o coletor de mídia não renderizar dados durante a depuração, ele não definirá esse atributo.</span><span class="sxs-lookup"><span data-stu-id="c5305-121">If the media sink does not render data while scrubbing, it does not set this attribute.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="c5305-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c5305-122">Requirements</span></span>



| <span data-ttu-id="c5305-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="c5305-123">Requirement</span></span> | <span data-ttu-id="c5305-124">Valor</span><span class="sxs-lookup"><span data-stu-id="c5305-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5305-125">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5305-125">Minimum supported client</span></span><br/> | <span data-ttu-id="c5305-126">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="c5305-126">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="c5305-127">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="c5305-127">Minimum supported server</span></span><br/> | <span data-ttu-id="c5305-128">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="c5305-128">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="c5305-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c5305-129">Header</span></span><br/>                   | <dl> <span data-ttu-id="c5305-130"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c5305-130"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c5305-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="c5305-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5305-132">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="c5305-132">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="c5305-133">Coletores de mídia</span><span class="sxs-lookup"><span data-stu-id="c5305-133">Media Sinks</span></span>](media-sinks.md)
</dt> <dt>

[<span data-ttu-id="c5305-134">MESessionScrubSampleComplete</span><span class="sxs-lookup"><span data-stu-id="c5305-134">MESessionScrubSampleComplete</span></span>](mesessionscrubsamplecomplete.md)
</dt> </dl>

 

 




