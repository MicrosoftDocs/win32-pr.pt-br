---
description: Filtro de analisador de MIDI
ms.assetid: a56576ad-f949-48fa-85e0-3e9898d2970d
title: Filtro de analisador de MIDI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 60ce659559852497b8ec55709e77f9510a1deaf2
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908424"
---
# <a name="midi-parser-filter"></a><span data-ttu-id="96705-103">Filtro de analisador de MIDI</span><span class="sxs-lookup"><span data-stu-id="96705-103">MIDI Parser Filter</span></span>

<span data-ttu-id="96705-104">O filtro analisador de MIDI lê dados MIDI encontrados no. MID e. Arquivos RMI.</span><span class="sxs-lookup"><span data-stu-id="96705-104">The MIDI Parser filter reads MIDI data that is found in .MID and .RMI files.</span></span> <span data-ttu-id="96705-105">O filtro aceita um fluxo da [origem do arquivo assíncrono](file-source--async--filter.md) ou dos filtros de [origem do arquivo de URL](file-source--url--filter.md) e gera amostras de MIDI para o [**renderizador de Midi**](midi-renderer-filter.md) para reprodução.</span><span class="sxs-lookup"><span data-stu-id="96705-105">The filter accepts a stream from the [Async File Source](file-source--async--filter.md) or [URL File Source](file-source--url--filter.md) filters and outputs MIDI samples to the [**MIDI Renderer**](midi-renderer-filter.md) for playback.</span></span>



| <span data-ttu-id="96705-106">Label</span><span class="sxs-lookup"><span data-stu-id="96705-106">Label</span></span> | <span data-ttu-id="96705-107">Valor</span><span class="sxs-lookup"><span data-stu-id="96705-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96705-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="96705-108">Filter Interfaces</span></span>                        | <span data-ttu-id="96705-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [ **IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span><span class="sxs-lookup"><span data-stu-id="96705-109">[**IAMMediaContent**](/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)</span></span>                           |
| <span data-ttu-id="96705-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="96705-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="96705-111">\_Fluxo de MediaType, \_ MIDI MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="96705-111">MEDIATYPE\_Stream, MEDIASUBTYPE\_Midi</span></span>                                                                    |
| <span data-ttu-id="96705-112">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="96705-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="96705-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [ **IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="96705-113">[**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                         |
| <span data-ttu-id="96705-114">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="96705-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="96705-115">\_MEDIASUBTYPE de mídia MIDI, \_ nulo</span><span class="sxs-lookup"><span data-stu-id="96705-115">MEDIATYPE\_Midi, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="96705-116">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="96705-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="96705-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="96705-117">[**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="96705-118">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="96705-118">Filter CLSID</span></span>                             | <span data-ttu-id="96705-119">\_MIDIPARSER CLSID</span><span class="sxs-lookup"><span data-stu-id="96705-119">CLSID\_MIDIParser</span></span>                                                                                        |
| <span data-ttu-id="96705-120">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="96705-120">Property Page CLSID</span></span>                      | <span data-ttu-id="96705-121">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="96705-121">No property page</span></span>                                                                                         |
| <span data-ttu-id="96705-122">Executável</span><span class="sxs-lookup"><span data-stu-id="96705-122">Executable</span></span>                               | <span data-ttu-id="96705-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="96705-123">quartz.dll</span></span>                                                                                               |
| [<span data-ttu-id="96705-124">Núcleo</span><span class="sxs-lookup"><span data-stu-id="96705-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="96705-125">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="96705-125">MERIT\_UNLIKELY</span></span>                                                                                          |
| [<span data-ttu-id="96705-126">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="96705-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="96705-127">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="96705-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                            |



 

## <a name="remarks"></a><span data-ttu-id="96705-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="96705-128">Remarks</span></span>

<span data-ttu-id="96705-129">Para obter mais informações, consulte [**processador de Midi**](midi-renderer-filter.md).</span><span class="sxs-lookup"><span data-stu-id="96705-129">For more information, see [**MIDI Renderer**](midi-renderer-filter.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="96705-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96705-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96705-131">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="96705-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



