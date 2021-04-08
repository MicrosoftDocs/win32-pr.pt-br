---
description: Filtro de analisador de MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro de analisador de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b741b2c82eda224a24ffee8a56f8977cbb510f3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919714"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="cf03a-103">Filtro de analisador de MIDI</span><span class="sxs-lookup"><span data-stu-id="cf03a-103">MIDI Parser Filter</span></span>

<span data-ttu-id="cf03a-104">O filtro analisador de MIDI lê dados MIDI encontrados no. MID e. Arquivos RMI.</span><span class="sxs-lookup"><span data-stu-id="cf03a-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="cf03a-105">O filtro aceita um fluxo da [origem do arquivo assíncrono](file-source--async--filter.md) ou dos filtros de [origem do arquivo de URL](file-source--url--filter.md) e gera amostras de MIDI para o [**renderizador de Midi**](midi-renderer-filter.md) para reprodução.</span><span class="sxs-lookup"><span data-stu-id="cf03a-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



|                                          |                                                                                                          |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf03a-106">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="cf03a-106">Filter Interfaces</span></span>                        | <span data-ttu-id="cf03a-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="cf03a-107">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="cf03a-108">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="cf03a-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="cf03a-109">\_Fluxo de MediaType, \_ MIDI MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="cf03a-109">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="cf03a-110">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="cf03a-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="cf03a-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="cf03a-111">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="cf03a-112">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="cf03a-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="cf03a-113">\_MEDIASUBTYPE de mídia MIDI, \_ nulo</span><span class="sxs-lookup"><span data-stu-id="cf03a-113">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="cf03a-114">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="cf03a-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="cf03a-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="cf03a-115">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="cf03a-116">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="cf03a-116">Filter CLSID</span></span>                             | <span data-ttu-id="cf03a-117">\_MIDIPARSER CLSID</span><span class="sxs-lookup"><span data-stu-id="cf03a-117">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="cf03a-118">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="cf03a-118">Property Page CLSID</span></span>                      | <span data-ttu-id="cf03a-119">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="cf03a-119">No property page</span></span>                                                                                         |
| <span data-ttu-id="cf03a-120">Executável</span><span class="sxs-lookup"><span data-stu-id="cf03a-120">Executable</span></span>                               | <span data-ttu-id="cf03a-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="cf03a-121">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="cf03a-122">Núcleo</span><span class="sxs-lookup"><span data-stu-id="cf03a-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="cf03a-123">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="cf03a-123">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="cf03a-124">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="cf03a-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="cf03a-125">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="cf03a-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="cf03a-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf03a-126">Remarks</span></span>

<span data-ttu-id="cf03a-127">Para obter mais informações, consulte [**processador de Midi**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="cf03a-127">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="cf03a-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf03a-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf03a-129">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="cf03a-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



