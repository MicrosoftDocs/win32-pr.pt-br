---
description: Eventos de origem de mídia
ms.assetid: c7b6ea86-e919-45b8-a1f9-bd18c3aed163
title: Eventos de origem de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72c40755a32f610b33ef3a5c66d3acb448223813
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "105791589"
---
# <a name="media-source-events"></a><span data-ttu-id="70b34-103">Eventos de origem de mídia</span><span class="sxs-lookup"><span data-stu-id="70b34-103">Media Source Events</span></span>

<span data-ttu-id="70b34-104">Este tópico lista os eventos que são enviados por fontes de mídia e fluxos de mídia.</span><span class="sxs-lookup"><span data-stu-id="70b34-104">This topic lists the events that are sent by media sources and media streams.</span></span> <span data-ttu-id="70b34-105">As fontes de mídia também podem enviar eventos personalizados não listados aqui.</span><span class="sxs-lookup"><span data-stu-id="70b34-105">Media sources can also send custom events not listed here.</span></span>

## <a name="media-source-events"></a><span data-ttu-id="70b34-106">Eventos de origem de mídia</span><span class="sxs-lookup"><span data-stu-id="70b34-106">Media Source Events</span></span>



| <span data-ttu-id="70b34-107">Evento</span><span class="sxs-lookup"><span data-stu-id="70b34-107">Event</span></span>                                                                      | <span data-ttu-id="70b34-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="70b34-108">Description</span></span>                                                                                      |
|----------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70b34-109">Evento MEEndOfPresentation</span><span class="sxs-lookup"><span data-stu-id="70b34-109">MEEndOfPresentation Event</span></span>](meendofpresentation.md)                       | <span data-ttu-id="70b34-110">A apresentação terminou.</span><span class="sxs-lookup"><span data-stu-id="70b34-110">The presentation ended.</span></span> <span data-ttu-id="70b34-111">Todos os fluxos na apresentação atingiram o final do fluxo.</span><span class="sxs-lookup"><span data-stu-id="70b34-111">All streams in the presentation have reached the end of the stream.</span></span>      |
| [<span data-ttu-id="70b34-112">Evento MENewStream</span><span class="sxs-lookup"><span data-stu-id="70b34-112">MENewStream Event</span></span>](menewstream.md)                                       | <span data-ttu-id="70b34-113">Um novo fluxo foi criado.</span><span class="sxs-lookup"><span data-stu-id="70b34-113">A new stream was created.</span></span> <span data-ttu-id="70b34-114">O evento contém um ponteiro para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="70b34-114">The event contains a pointer to the stream.</span></span>                            |
| [<span data-ttu-id="70b34-115">Evento MESourceCharacteristicsChanged</span><span class="sxs-lookup"><span data-stu-id="70b34-115">MESourceCharacteristicsChanged Event</span></span>](mesourcecharacteristicschanged.md) | <span data-ttu-id="70b34-116">As características da fonte foram alteradas.</span><span class="sxs-lookup"><span data-stu-id="70b34-116">The characteristics of the source have changed.</span></span> <span data-ttu-id="70b34-117">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="70b34-117">(Optional.)</span></span>                                      |
| [<span data-ttu-id="70b34-118">Evento MESourceMetadataChanged</span><span class="sxs-lookup"><span data-stu-id="70b34-118">MESourceMetadataChanged Event</span></span>](mesourcemetadatachanged.md)               | <span data-ttu-id="70b34-119">Os metadados da origem foram alterados.</span><span class="sxs-lookup"><span data-stu-id="70b34-119">The source's metadata has changed.</span></span> <span data-ttu-id="70b34-120">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="70b34-120">(Optional.)</span></span>                                                   |
| [<span data-ttu-id="70b34-121">Evento MESourcePaused</span><span class="sxs-lookup"><span data-stu-id="70b34-121">MESourcePaused Event</span></span>](mesourcepaused.md)                                 | <span data-ttu-id="70b34-122">A origem foi pausada.</span><span class="sxs-lookup"><span data-stu-id="70b34-122">The source was paused.</span></span> <span data-ttu-id="70b34-123">Nem todas as fontes dão suporte à pausa.</span><span class="sxs-lookup"><span data-stu-id="70b34-123">Not all sources support pausing.</span></span>                                          |
| [<span data-ttu-id="70b34-124">Evento MESourceRateChanged</span><span class="sxs-lookup"><span data-stu-id="70b34-124">MESourceRateChanged Event</span></span>](mesourceratechanged.md)                       | <span data-ttu-id="70b34-125">A taxa de reprodução da origem foi alterada.</span><span class="sxs-lookup"><span data-stu-id="70b34-125">The source's playback rate has changed.</span></span> <span data-ttu-id="70b34-126">(Opcional; aplica-se se a fonte der suporte ao controle de taxa.)</span><span class="sxs-lookup"><span data-stu-id="70b34-126">(Optional; applies if the source supports rate control.)</span></span> |
| [<span data-ttu-id="70b34-127">Evento MESourceRateChangeRequested</span><span class="sxs-lookup"><span data-stu-id="70b34-127">MESourceRateChangeRequested Event</span></span>](mesourceratechangerequested.md)       | <span data-ttu-id="70b34-128">A origem está solicitando uma nova taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="70b34-128">The source is requesting a new playback rate.</span></span> <span data-ttu-id="70b34-129">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="70b34-129">(Optional.)</span></span>                                        |
| [<span data-ttu-id="70b34-130">Evento MESourceSeeked</span><span class="sxs-lookup"><span data-stu-id="70b34-130">MESourceSeeked Event</span></span>](mesourceseeked.md)                                 | <span data-ttu-id="70b34-131">A origem foi procurada.</span><span class="sxs-lookup"><span data-stu-id="70b34-131">The source was seeked.</span></span> <span data-ttu-id="70b34-132">Nem todas as fontes dão suporte à busca.</span><span class="sxs-lookup"><span data-stu-id="70b34-132">Not all sources support seeking.</span></span>                                          |
| [<span data-ttu-id="70b34-133">Evento MESourceStarted</span><span class="sxs-lookup"><span data-stu-id="70b34-133">MESourceStarted Event</span></span>](mesourcestarted.md)                               | <span data-ttu-id="70b34-134">A origem foi iniciada.</span><span class="sxs-lookup"><span data-stu-id="70b34-134">The source was started.</span></span>                                                                          |
| [<span data-ttu-id="70b34-135">Evento MESourceStopped</span><span class="sxs-lookup"><span data-stu-id="70b34-135">MESourceStopped Event</span></span>](mesourcestopped.md)                               | <span data-ttu-id="70b34-136">A origem foi parada.</span><span class="sxs-lookup"><span data-stu-id="70b34-136">The source was stopped.</span></span>                                                                          |
| [<span data-ttu-id="70b34-137">Evento MEUpdatedStream</span><span class="sxs-lookup"><span data-stu-id="70b34-137">MEUpdatedStream Event</span></span>](meupdatedstream.md)                               | <span data-ttu-id="70b34-138">Um fluxo existente foi buscado ou reiniciado.</span><span class="sxs-lookup"><span data-stu-id="70b34-138">An existing stream was seeked or re-started.</span></span> <span data-ttu-id="70b34-139">O evento contém um ponteiro para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="70b34-139">The event contains a pointer to the stream.</span></span>         |



 

## <a name="media-stream-events"></a><span data-ttu-id="70b34-140">Eventos de fluxo de mídia</span><span class="sxs-lookup"><span data-stu-id="70b34-140">Media Stream Events</span></span>



| <span data-ttu-id="70b34-141">Evento</span><span class="sxs-lookup"><span data-stu-id="70b34-141">Event</span></span>                                                    | <span data-ttu-id="70b34-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="70b34-142">Description</span></span>                                                                                                                    |
|----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="70b34-143">Evento MEEndOfStream</span><span class="sxs-lookup"><span data-stu-id="70b34-143">MEEndOfStream Event</span></span>](meendofstream.md)                 | <span data-ttu-id="70b34-144">O fluxo terminou.</span><span class="sxs-lookup"><span data-stu-id="70b34-144">The stream ended.</span></span>                                                                                                              |
| [<span data-ttu-id="70b34-145">Evento MEError</span><span class="sxs-lookup"><span data-stu-id="70b34-145">MEError Event</span></span>](meerror.md)                             | <span data-ttu-id="70b34-146">Ocorreu um erro durante o streaming.</span><span class="sxs-lookup"><span data-stu-id="70b34-146">An error has occurred during streaming.</span></span> <span data-ttu-id="70b34-147">Use esse evento para erros que não estão relacionados a nenhum dos outros eventos listados aqui.</span><span class="sxs-lookup"><span data-stu-id="70b34-147">Use this event for errors that are not related to any of the other events listed here.</span></span> |
| [<span data-ttu-id="70b34-148">Evento MEMediaSample</span><span class="sxs-lookup"><span data-stu-id="70b34-148">MEMediaSample Event</span></span>](memediasample.md)                 | <span data-ttu-id="70b34-149">O fluxo gerou uma nova amostra.</span><span class="sxs-lookup"><span data-stu-id="70b34-149">The stream has generated a new sample.</span></span>                                                                                         |
| [<span data-ttu-id="70b34-150">Evento MEStreamFormatChanged</span><span class="sxs-lookup"><span data-stu-id="70b34-150">MEStreamFormatChanged Event</span></span>](mestreamformatchanged.md) | <span data-ttu-id="70b34-151">O tipo de mídia foi alterado.</span><span class="sxs-lookup"><span data-stu-id="70b34-151">The media type has changed.</span></span> <span data-ttu-id="70b34-152">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="70b34-152">(Optional.)</span></span>                                                                                        |
| [<span data-ttu-id="70b34-153">Evento MEStreamPaused</span><span class="sxs-lookup"><span data-stu-id="70b34-153">MEStreamPaused Event</span></span>](mestreampaused.md)               | <span data-ttu-id="70b34-154">O fluxo foi pausado.</span><span class="sxs-lookup"><span data-stu-id="70b34-154">The stream was paused.</span></span>                                                                                                         |
| [<span data-ttu-id="70b34-155">Evento MEStreamSeeked</span><span class="sxs-lookup"><span data-stu-id="70b34-155">MEStreamSeeked Event</span></span>](mestreamseeked.md)               | <span data-ttu-id="70b34-156">O fluxo foi buscado.</span><span class="sxs-lookup"><span data-stu-id="70b34-156">The stream was seeked.</span></span>                                                                                                         |
| [<span data-ttu-id="70b34-157">Evento MEStreamStarted</span><span class="sxs-lookup"><span data-stu-id="70b34-157">MEStreamStarted Event</span></span>](mestreamstarted.md)             | <span data-ttu-id="70b34-158">O fluxo foi iniciado.</span><span class="sxs-lookup"><span data-stu-id="70b34-158">The stream was started.</span></span>                                                                                                        |
| [<span data-ttu-id="70b34-159">Evento MEStreamStopped</span><span class="sxs-lookup"><span data-stu-id="70b34-159">MEStreamStopped Event</span></span>](mestreamstopped.md)             | <span data-ttu-id="70b34-160">O fluxo foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="70b34-160">The stream was stopped.</span></span>                                                                                                        |
| [<span data-ttu-id="70b34-161">Evento MEStreamThinMode</span><span class="sxs-lookup"><span data-stu-id="70b34-161">MEStreamThinMode Event</span></span>](mestreamthinmode.md)           | <span data-ttu-id="70b34-162">O modo de finamento foi iniciado ou interrompido.</span><span class="sxs-lookup"><span data-stu-id="70b34-162">Thinning mode has started or stopped.</span></span> <span data-ttu-id="70b34-163">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="70b34-163">(Optional.)</span></span>                                                                              |
| [<span data-ttu-id="70b34-164">Evento MEStreamTick</span><span class="sxs-lookup"><span data-stu-id="70b34-164">MEStreamTick Event</span></span>](mestreamtick.md)                   | <span data-ttu-id="70b34-165">Há uma lacuna no fluxo.</span><span class="sxs-lookup"><span data-stu-id="70b34-165">There is a gap in the stream.</span></span> <span data-ttu-id="70b34-166">(Opcional).</span><span class="sxs-lookup"><span data-stu-id="70b34-166">(Optional.)</span></span>                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="70b34-167">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="70b34-167">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="70b34-168">Fontes de mídia</span><span class="sxs-lookup"><span data-stu-id="70b34-168">Media Sources</span></span>](media-sources.md)
</dt> </dl>

 

 



