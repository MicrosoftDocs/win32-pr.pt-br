---
description: Filtro de origem do arquivo (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro de origem do arquivo (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: caea04b74a6880452210f1a43d5dfb29f8753dd3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087801"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="13ba7-103">Filtro de origem do arquivo (URL)</span><span class="sxs-lookup"><span data-stu-id="13ba7-103">File Source (URL) Filter</span></span>

<span data-ttu-id="13ba7-104">O filtro de origem do arquivo de URL é um filtro de origem assíncrono genérico que funciona com qualquer arquivo de origem que pode ser identificado por um Uniform Resource Locator (URL) e cujo tipo principal de mídia é Stream.</span><span class="sxs-lookup"><span data-stu-id="13ba7-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="13ba7-105">Isso inclui arquivos AVI, MOV, MPEG e WAV.</span><span class="sxs-lookup"><span data-stu-id="13ba7-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="13ba7-106">Ele requer que o filtro downstream seja um analisador, como o [divisor de fluxo MPEG-1](mpeg-1-stream-splitter-filter.md), o [divisor AVI](avi-splitter-filter.md)ou o [analisador de filmes do QuickTime](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="13ba7-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13ba7-107">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="13ba7-107">Filter Interfaces</span></span>                        | <span data-ttu-id="13ba7-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="13ba7-108">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="13ba7-109">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="13ba7-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="13ba7-110">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="13ba7-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="13ba7-111">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="13ba7-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="13ba7-112">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="13ba7-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="13ba7-113">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="13ba7-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="13ba7-114">Fluxo de MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="13ba7-114">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="13ba7-115">O subtipo depende do formato de mídia.</span><span class="sxs-lookup"><span data-stu-id="13ba7-115">The subtype depends on the media format.</span></span> <span data-ttu-id="13ba7-116">(MEDIASUBTYPE \_ NULL se o filtro não reconhecer o formato.)</span><span class="sxs-lookup"><span data-stu-id="13ba7-116">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="13ba7-117">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="13ba7-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="13ba7-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="13ba7-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="13ba7-119">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="13ba7-119">Filter CLSID</span></span>                             | <span data-ttu-id="13ba7-120">\_URLREADER CLSID</span><span class="sxs-lookup"><span data-stu-id="13ba7-120">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="13ba7-121">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="13ba7-121">Property Page CLSID</span></span>                      | <span data-ttu-id="13ba7-122">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="13ba7-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="13ba7-123">Executável</span><span class="sxs-lookup"><span data-stu-id="13ba7-123">Executable</span></span>                               | <span data-ttu-id="13ba7-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="13ba7-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="13ba7-125">Núcleo</span><span class="sxs-lookup"><span data-stu-id="13ba7-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="13ba7-126">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="13ba7-126">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="13ba7-127">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="13ba7-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="13ba7-128">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="13ba7-128">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="13ba7-129">Comentários</span><span class="sxs-lookup"><span data-stu-id="13ba7-129">Remarks</span></span>

<span data-ttu-id="13ba7-130">Esse filtro usa URLMon e oferece suporte a páginas de código.</span><span class="sxs-lookup"><span data-stu-id="13ba7-130">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13ba7-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="13ba7-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13ba7-132">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="13ba7-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



