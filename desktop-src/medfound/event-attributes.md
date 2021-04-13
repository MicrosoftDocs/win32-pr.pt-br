---
description: Atributos do evento
ms.assetid: 25e77ee1-cffc-4f8b-ac07-b5607a125fc7
title: Atributos de evento (Microsoft Media Foundation)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 633e8f3857582422fe4a2d65ba34e68be483e7aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501170"
---
# <a name="event-attributes-microsoft-media-foundation"></a><span data-ttu-id="12784-103">Atributos de evento (Microsoft Media Foundation)</span><span class="sxs-lookup"><span data-stu-id="12784-103">Event Attributes (Microsoft Media Foundation)</span></span>

<span data-ttu-id="12784-104">Os atributos a seguir se aplicam a eventos.</span><span class="sxs-lookup"><span data-stu-id="12784-104">The following attributes apply to events.</span></span>



| <span data-ttu-id="12784-105">Atributo</span><span class="sxs-lookup"><span data-stu-id="12784-105">Attribute</span></span>                                                                                                        | <span data-ttu-id="12784-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="12784-106">Description</span></span>                                                                                                           |
|------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="12784-107">**o \_ evento MF \_ faz a \_ finação**</span><span class="sxs-lookup"><span data-stu-id="12784-107">**MF\_EVENT\_DO\_THINNING**</span></span>](mf-event-do-thinning-attribute.md)                                                | <span data-ttu-id="12784-108">Quando uma fonte de mídia solicita uma nova taxa de reprodução, especifica se a origem também solicita a fina.</span><span class="sxs-lookup"><span data-stu-id="12784-108">When a media source requests a new playback rate, specifies whether the source also requests thinning.</span></span>                |
| [<span data-ttu-id="12784-109">**\_nó de \_ saída do evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="12784-109">**MF\_EVENT\_OUTPUT\_NODE**</span></span>](mf-event-output-node-attribute.md)                                                | <span data-ttu-id="12784-110">Identifica o nó de topologia para um coletor de fluxo.</span><span class="sxs-lookup"><span data-stu-id="12784-110">Identifies the topology node for a stream sink.</span></span>                                                                       |
| [<span data-ttu-id="12784-111">**\_deslocamento do \_ tempo de apresentação do evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12784-111">**MF\_EVENT\_PRESENTATION\_TIME\_OFFSET**</span></span>](mf-event-presentation-time-offset-attribute.md)                     | <span data-ttu-id="12784-112">Deslocamento entre o tempo de apresentação e os carimbos de data/hora da fonte de mídia.</span><span class="sxs-lookup"><span data-stu-id="12784-112">Offset between the presentation time and the media source's time stamps.</span></span>                                              |
| [<span data-ttu-id="12784-113">**\_tempo de \_ SCRUBSAMPLE do evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="12784-113">**MF\_EVENT\_SCRUBSAMPLE\_TIME**</span></span>](mf-event-scrubsample-time-attribute.md)                                      | <span data-ttu-id="12784-114">Tempo de apresentação para um exemplo que foi renderizado durante a depuração.</span><span class="sxs-lookup"><span data-stu-id="12784-114">Presentation time for a sample that was rendered while scrubbing.</span></span>                                                     |
| [<span data-ttu-id="12784-115">**\_SESSIONCAPS do evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="12784-115">**MF\_EVENT\_SESSIONCAPS**</span></span>](mf-event-sessioncaps-attribute.md)                                                 | <span data-ttu-id="12784-116">Contém sinalizadores que definem os recursos da sessão de mídia, com base na apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="12784-116">Contains flags that define the capabilities of the Media Session, based on the current presentation.</span></span>                  |
| [<span data-ttu-id="12784-117">**\_ \_ SESSIONCAPS Delta de evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="12784-117">**MF\_EVENT\_SESSIONCAPS\_DELTA**</span></span>](mf-event-sessioncaps-delta-attribute.md)                                    | <span data-ttu-id="12784-118">Contém sinalizadores que indicam quais funcionalidades foram alteradas na sessão de mídia, com base na apresentação atual.</span><span class="sxs-lookup"><span data-stu-id="12784-118">Contains flags that indicate which capabilities have changed in the Media Session, based on the current presentation.</span></span> |
| [<span data-ttu-id="12784-119">**\_ \_ início real da origem do evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12784-119">**MF\_EVENT\_SOURCE\_ACTUAL\_START**</span></span>](mf-event-source-actual-start-attribute.md)                               | <span data-ttu-id="12784-120">Contém a hora de início quando uma fonte de mídia é reiniciada a partir de sua posição atual.</span><span class="sxs-lookup"><span data-stu-id="12784-120">Contains the start time when a media source restarts from its current position.</span></span>                                       |
| [<span data-ttu-id="12784-121">**\_características de \_ origem do evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="12784-121">**MF\_EVENT\_SOURCE\_CHARACTERISTICS**</span></span>](mf-event-source-characteristics-attribute.md)                          | <span data-ttu-id="12784-122">Especifica as características atuais da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="12784-122">Specifies the current characteristics of the media source.</span></span>                                                            |
| [<span data-ttu-id="12784-123">**\_características de origem do evento MF \_ \_ \_ antigas**</span><span class="sxs-lookup"><span data-stu-id="12784-123">**MF\_EVENT\_SOURCE\_CHARACTERISTICS\_OLD**</span></span>](mf-event-source-characteristics-old-attribute.md)                 | <span data-ttu-id="12784-124">Especifica as características anteriores da origem da mídia.</span><span class="sxs-lookup"><span data-stu-id="12784-124">Specifies the previous characteristics of the media source.</span></span>                                                           |
| [<span data-ttu-id="12784-125">**\_ \_ Início falso da origem do evento MF \_ \_**</span><span class="sxs-lookup"><span data-stu-id="12784-125">**MF\_EVENT\_SOURCE\_FAKE\_START**</span></span>](mf-event-source-fake-start-attribute.md)                                   | <span data-ttu-id="12784-126">Especifica se a topologia de segmento atual está vazia.</span><span class="sxs-lookup"><span data-stu-id="12784-126">Specifies whether the current segment topology is empty.</span></span>                                                              |
| [<span data-ttu-id="12784-127">**\_origem do evento MF \_ \_ PROJECTSTART**</span><span class="sxs-lookup"><span data-stu-id="12784-127">**MF\_EVENT\_SOURCE\_PROJECTSTART**</span></span>](mf-event-source-projectstart-attribute.md)                                | <span data-ttu-id="12784-128">Especifica a hora de início para uma topologia de segmento.</span><span class="sxs-lookup"><span data-stu-id="12784-128">Specifies the start time for a segment topology.</span></span>                                                                      |
| [<span data-ttu-id="12784-129">**\_topologia de origem do evento MF \_ \_ \_ cancelada**</span><span class="sxs-lookup"><span data-stu-id="12784-129">**MF\_EVENT\_SOURCE\_TOPOLOGY\_CANCELED**</span></span>](mf-event-source-topology-canceled-attribute.md)                     | <span data-ttu-id="12784-130">Especifica se a origem do sequenciador cancelou uma topologia.</span><span class="sxs-lookup"><span data-stu-id="12784-130">Specifies whether the sequencer source canceled a topology.</span></span>                                                           |
| [<span data-ttu-id="12784-131">**\_hora de \_ início da \_ apresentação \_ do evento MF**</span><span class="sxs-lookup"><span data-stu-id="12784-131">**MF\_EVENT\_START\_PRESENTATION\_TIME**</span></span>](mf-event-start-presentation-time-attribute.md)                       | <span data-ttu-id="12784-132">A hora de início da apresentação, em unidades de 100 nanossegundos, conforme medida pelo relógio de apresentação.</span><span class="sxs-lookup"><span data-stu-id="12784-132">The starting time for the presentation, in 100-nanosecond units, as measured by the presentation clock.</span></span>               |
| [<span data-ttu-id="12784-133">**\_ \_ \_ hora de início da apresentação do evento MF \_ \_ na \_ saída**</span><span class="sxs-lookup"><span data-stu-id="12784-133">**MF\_EVENT\_START\_PRESENTATION\_TIME\_AT\_OUTPUT**</span></span>](mf-event-start-presentation-time-at-output-attribute.md) | <span data-ttu-id="12784-134">A hora da apresentação na qual os coletores de mídia processarão o primeiro exemplo da nova topologia.</span><span class="sxs-lookup"><span data-stu-id="12784-134">The presentation time at which the media sinks will render the first sample of the new topology.</span></span>                      |
| [<span data-ttu-id="12784-135">**\_status da \_ topologia de evento MF \_**</span><span class="sxs-lookup"><span data-stu-id="12784-135">**MF\_EVENT\_TOPOLOGY\_STATUS**</span></span>](mf-event-topology-status-attribute.md)                                        | <span data-ttu-id="12784-136">Especifica o status de uma topologia durante a reprodução.</span><span class="sxs-lookup"><span data-stu-id="12784-136">Specifies the status of a topology during playback.</span></span>                                                                   |
| [<span data-ttu-id="12784-137">**\_tempo de \_ \_ ocorrência de evento aprox da sessão \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="12784-137">**MF\_SESSION\_APPROX\_EVENT\_OCCURRENCE\_TIME**</span></span>](mf-session-approx-event-occurrence-time-attribute.md)        | <span data-ttu-id="12784-138">A hora aproximada em que a sessão de mídia gerou um evento.</span><span class="sxs-lookup"><span data-stu-id="12784-138">The approximate time when the Media Session raised an event.</span></span>                                                          |



 

## <a name="related-topics"></a><span data-ttu-id="12784-139">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12784-139">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12784-140">**IMFMediaEvent**</span><span class="sxs-lookup"><span data-stu-id="12784-140">**IMFMediaEvent**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediaevent)
</dt> <dt>

[<span data-ttu-id="12784-141">Eventos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12784-141">Media Foundation Events</span></span>](media-foundation-events.md)
</dt> <dt>

[<span data-ttu-id="12784-142">Atributos de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="12784-142">Media Foundation Attributes</span></span>](media-foundation-attributes.md)
</dt> </dl>

 

 



