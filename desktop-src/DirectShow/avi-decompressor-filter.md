---
description: Filtro de descompactação AVI
ms.assetid: 6a9914db-483a-429c-9b26-9451578951c9
title: Filtro de descompactação AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9b6fcff61dd867c598e793fb5aa8fbff67dc6cd
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103646005"
---
# <a name="avi-decompressor-filter"></a><span data-ttu-id="773ab-103">Filtro de descompactação AVI</span><span class="sxs-lookup"><span data-stu-id="773ab-103">AVI Decompressor Filter</span></span>

<span data-ttu-id="773ab-104">O filtro do descompactador AVI permite que os codecs VCM (Gerenciador de compactação de vídeo) ingressem em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="773ab-104">The AVI Decompressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="773ab-105">O aplicativo não precisa adicionar o filtro ao grafo de filtro; Ele é retirado automaticamente pelo Gerenciador de gráficos de filtro quando necessário.</span><span class="sxs-lookup"><span data-stu-id="773ab-105">The application does not need to add the filter to the filter graph; it is pulled in automatically by the Filter Graph Manager when needed.</span></span>

<span data-ttu-id="773ab-106">Quando o Gerenciador de gráfico de filtro está criando um grafo para renderizar um arquivo AVI, ele verifica o FOURCC no cabeçalho AVI do arquivo para determinar se o fluxo de vídeo está compactado.</span><span class="sxs-lookup"><span data-stu-id="773ab-106">When the Filter Graph Manager is building a graph to render an AVI file, it checks the FOURCC in the file's AVI header to determine whether the video stream is compressed.</span></span> <span data-ttu-id="773ab-107">Se for, o Gerenciador de gráficos de filtro adicionará o descompactador AVI, que então pesquisará o registro em busca de um descompactador instalado que possa manipular o arquivo.</span><span class="sxs-lookup"><span data-stu-id="773ab-107">If it is, the Filter Graph Manager adds the AVI Decompressor, which then searches the registry for an installed decompressor that can handle the file.</span></span>

> [!Note]  
> <span data-ttu-id="773ab-108">Os decompactadores MPEG nunca são implementados como codecs VCM, mas somente como filtros nativos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="773ab-108">MPEG decompressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 

<span data-ttu-id="773ab-109">Em seu PIN de upstream, o descompactador AVI normalmente se conecta ao [divisor AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="773ab-109">On its upstream pin the AVI Decompressor typically connects to the [AVI Splitter](avi-splitter-filter.md).</span></span> <span data-ttu-id="773ab-110">Em seu pino de saída, ele normalmente se conecta ao [processador de vídeo](video-renderer-filter.md) ou ao [filtro AVI Mux](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="773ab-110">On its output pin it typically connects to the [Video Renderer](video-renderer-filter.md) or the [AVI Mux Filter](avi-mux-filter.md).</span></span>



|                                          |                                                                                                                                                                                                                    |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="773ab-111">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="773ab-111">Filter Interfaces</span></span>                        | [<span data-ttu-id="773ab-112">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="773ab-112">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                                                                                 |
| <span data-ttu-id="773ab-113">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="773ab-113">Input Pin Media Types</span></span>                    | <span data-ttu-id="773ab-114">Tipo principal: MEDIATYPE \_ VideoSubtype: deve corresponder ao código FOURCC para o tipo de compactação.</span><span class="sxs-lookup"><span data-stu-id="773ab-114">Major type: MEDIATYPE\_VideoSubtype: Must correspond to the FOURCC code for the compression type.</span></span> <span data-ttu-id="773ab-115">Para obter mais informações, consulte [Códigos FOURCC](fourcc-codes.md).</span><span class="sxs-lookup"><span data-stu-id="773ab-115">For more information, see [FOURCC Codes](fourcc-codes.md).</span></span><br/> <span data-ttu-id="773ab-116">Tipo de formato: formato \_ VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="773ab-116">Format type: FORMAT\_VideoInfo</span></span><br/> |
| <span data-ttu-id="773ab-117">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="773ab-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="773ab-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="773ab-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                             |
| <span data-ttu-id="773ab-119">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="773ab-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="773ab-120">\_Vídeo de MediaType, MEDIASUBTYPE \_ NULL, Format \_ VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="773ab-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL, FORMAT\_VideoInfo</span></span>                                                                                                                                                            |
| <span data-ttu-id="773ab-121">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="773ab-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="773ab-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="773ab-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                 |
| <span data-ttu-id="773ab-123">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="773ab-123">Filter CLSID</span></span>                             | <span data-ttu-id="773ab-124">\_AVIDEC CLSID</span><span class="sxs-lookup"><span data-stu-id="773ab-124">CLSID\_AVIDec</span></span>                                                                                                                                                                                                      |
| <span data-ttu-id="773ab-125">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="773ab-125">Property Page CLSID</span></span>                      | <span data-ttu-id="773ab-126">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="773ab-126">No property page.</span></span>                                                                                                                                                                                                  |
| <span data-ttu-id="773ab-127">Executável</span><span class="sxs-lookup"><span data-stu-id="773ab-127">Executable</span></span>                               | <span data-ttu-id="773ab-128">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="773ab-128">quartz.dll</span></span>                                                                                                                                                                                                         |
| [<span data-ttu-id="773ab-129">Núcleo</span><span class="sxs-lookup"><span data-stu-id="773ab-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="773ab-130">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="773ab-130">MERIT\_NORMAL</span></span>                                                                                                                                                                                                      |
| [<span data-ttu-id="773ab-131">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="773ab-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="773ab-132">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="773ab-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="773ab-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="773ab-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="773ab-134">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="773ab-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




