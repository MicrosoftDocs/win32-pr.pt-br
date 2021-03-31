---
description: Gerado pela origem do sequenciador quando um segmento é concluído e é seguido por outro segmento. Quando o segmento final é concluído, a origem do sequenciador gera um evento MEEndOfPresentation.
ms.assetid: 1be13c9a-d454-4642-b26b-556f2461b705
title: Evento MEEndOfPresentationSegment (Mfobjects. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d3608f51f3ff66e21261cc40d1f8cf690c92c4e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827640"
---
# <a name="meendofpresentationsegment-event"></a><span data-ttu-id="d1ae3-104">Evento MEEndOfPresentationSegment</span><span class="sxs-lookup"><span data-stu-id="d1ae3-104">MEEndOfPresentationSegment event</span></span>

<span data-ttu-id="d1ae3-105">Gerado pela origem do sequenciador quando um segmento é concluído e é seguido por outro segmento.</span><span class="sxs-lookup"><span data-stu-id="d1ae3-105">Raised by the sequencer source when a segment is completed and is followed by another segment.</span></span> <span data-ttu-id="d1ae3-106">Quando o segmento final é concluído, a origem do sequenciador gera um evento [MEEndOfPresentation](meendofpresentation.md) .</span><span class="sxs-lookup"><span data-stu-id="d1ae3-106">When the final segment is completed, the sequencer source raises an [MEEndOfPresentation](meendofpresentation.md) event.</span></span>

<span data-ttu-id="d1ae3-107">A sessão de mídia encaminha esse evento para o aplicativo.</span><span class="sxs-lookup"><span data-stu-id="d1ae3-107">The Media Session forwards this event to the application.</span></span>

## <a name="event-values"></a><span data-ttu-id="d1ae3-108">Valores de evento</span><span class="sxs-lookup"><span data-stu-id="d1ae3-108">Event values</span></span>

<span data-ttu-id="d1ae3-109">Os valores possíveis recuperados de [**IMFMediaEvent:: GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) incluem o seguinte.</span><span class="sxs-lookup"><span data-stu-id="d1ae3-109">Possible values retrieved from [**IMFMediaEvent::GetValue**](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediaevent-getvalue) include the following.</span></span>



| <span data-ttu-id="d1ae3-110">VARTYPE</span><span class="sxs-lookup"><span data-stu-id="d1ae3-110">VARTYPE</span></span>              | <span data-ttu-id="d1ae3-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1ae3-111">Description</span></span>                           |
|----------------------|---------------------------------------|
| <span data-ttu-id="d1ae3-112">VT \_ vazio</span><span class="sxs-lookup"><span data-stu-id="d1ae3-112">VT\_EMPTY</span></span><br/> | <span data-ttu-id="d1ae3-113">Nenhum dado do evento.</span><span class="sxs-lookup"><span data-stu-id="d1ae3-113">No event data.</span></span><br/> <br/> |



## <a name="attributes"></a><span data-ttu-id="d1ae3-114">Atributos</span><span class="sxs-lookup"><span data-stu-id="d1ae3-114">Attributes</span></span>

<span data-ttu-id="d1ae3-115">Os atributos a seguir são definidos para este evento.</span><span class="sxs-lookup"><span data-stu-id="d1ae3-115">The following attributes are defined for this event.</span></span>



| <span data-ttu-id="d1ae3-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="d1ae3-116">Attribute</span></span>                                                                                               | <span data-ttu-id="d1ae3-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="d1ae3-117">Description</span></span>                                                                          |
|---------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="d1ae3-118">**\_topologia de origem do evento MF \_ \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="d1ae3-118">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)<br/> | <span data-ttu-id="d1ae3-119">Especifica se a origem do sequenciador cancelou esse segmento.</span><span class="sxs-lookup"><span data-stu-id="d1ae3-119">Specifies whether the sequencer source canceled this segment.</span></span><br/> <br/> |



## <a name="requirements"></a><span data-ttu-id="d1ae3-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d1ae3-120">Requirements</span></span>



| <span data-ttu-id="d1ae3-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d1ae3-121">Requirement</span></span> | <span data-ttu-id="d1ae3-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d1ae3-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1ae3-123">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1ae3-123">Minimum supported client</span></span><br/> | <span data-ttu-id="d1ae3-124">\[Somente aplicativos da área de trabalho do Windows Vista\]</span><span class="sxs-lookup"><span data-stu-id="d1ae3-124">Windows Vista \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d1ae3-125">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d1ae3-125">Minimum supported server</span></span><br/> | <span data-ttu-id="d1ae3-126">\[Somente aplicativos da área de trabalho do Windows Server 2008\]</span><span class="sxs-lookup"><span data-stu-id="d1ae3-126">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d1ae3-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d1ae3-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="d1ae3-128"><dt>Mfobjects. h (incluir Mfidl. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d1ae3-128"><dt>Mfobjects.h (include Mfidl.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d1ae3-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="d1ae3-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1ae3-130">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="d1ae3-130">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="d1ae3-131">Sobre a origem do sequenciador</span><span class="sxs-lookup"><span data-stu-id="d1ae3-131">About the Sequencer Source</span></span>](about-the-sequencer-source.md)
</dt> <dt>

[<span data-ttu-id="d1ae3-132">Eventos de origem do Sequencer</span><span class="sxs-lookup"><span data-stu-id="d1ae3-132">Sequencer Source Events</span></span>](sequencer-source-events.md)
</dt> </dl>

 

 




