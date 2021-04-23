---
description: Filtro de origem do arquivo (URL)
ms.assetid: 405fd6ea-aa17-4d11-8f07-067468cb090b
title: Filtro de origem do arquivo (URL)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a0ddfa7282adbf5117bd2c52465c6eb30efbd69e
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909234"
---
# <a name="file-source-url-filter"></a><span data-ttu-id="9d72a-103">Filtro de origem do arquivo (URL)</span><span class="sxs-lookup"><span data-stu-id="9d72a-103">File Source (URL) Filter</span></span>

<span data-ttu-id="9d72a-104">O filtro de origem do arquivo de URL é um filtro de origem assíncrono genérico que funciona com qualquer arquivo de origem que pode ser identificado por um Uniform Resource Locator (URL) e cujo tipo principal de mídia é Stream.</span><span class="sxs-lookup"><span data-stu-id="9d72a-104">The URL File Source filter is a generic asynchronous source filter that works with any source file that can be identified by a Uniform Resource Locator (URL) and whose media major type is stream.</span></span> <span data-ttu-id="9d72a-105">Isso inclui arquivos AVI, MOV, MPEG e WAV.</span><span class="sxs-lookup"><span data-stu-id="9d72a-105">This includes AVI, MOV, MPEG, and WAV files.</span></span> <span data-ttu-id="9d72a-106">Ele requer que o filtro downstream seja um analisador, como o [divisor de fluxo MPEG-1](mpeg-1-stream-splitter-filter.md), o [divisor AVI](avi-splitter-filter.md)ou o [analisador de filmes do QuickTime](quicktime-movie-parser-filter.md).</span><span class="sxs-lookup"><span data-stu-id="9d72a-106">It requires the downstream filter to be a parser, such as the [MPEG-1 Stream Splitter](mpeg-1-stream-splitter-filter.md), the [AVI Splitter](avi-splitter-filter.md), or the [QuickTime Movie Parser](quicktime-movie-parser-filter.md).</span></span>



| <span data-ttu-id="9d72a-107">Label</span><span class="sxs-lookup"><span data-stu-id="9d72a-107">Label</span></span> | <span data-ttu-id="9d72a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="9d72a-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9d72a-109">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="9d72a-109">Filter Interfaces</span></span>                        | <span data-ttu-id="9d72a-110">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="9d72a-110">[**IAMOpenProgress**](/windows/desktop/api/Strmif/nn-strmif-iamopenprogress), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>       |
| <span data-ttu-id="9d72a-111">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="9d72a-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="9d72a-112">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9d72a-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="9d72a-113">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="9d72a-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="9d72a-114">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="9d72a-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="9d72a-115">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="9d72a-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="9d72a-116">Fluxo de MEDIATYPE \_ .</span><span class="sxs-lookup"><span data-stu-id="9d72a-116">MEDIATYPE\_Stream.</span></span> <span data-ttu-id="9d72a-117">O subtipo depende do formato de mídia.</span><span class="sxs-lookup"><span data-stu-id="9d72a-117">The subtype depends on the media format.</span></span> <span data-ttu-id="9d72a-118">(MEDIASUBTYPE \_ NULL se o filtro não reconhecer o formato.)</span><span class="sxs-lookup"><span data-stu-id="9d72a-118">(MEDIASUBTYPE\_NULL if the filter doesn't recognize the format.)</span></span>         |
| <span data-ttu-id="9d72a-119">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="9d72a-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="9d72a-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="9d72a-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="9d72a-121">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="9d72a-121">Filter CLSID</span></span>                             | <span data-ttu-id="9d72a-122">\_URLREADER CLSID</span><span class="sxs-lookup"><span data-stu-id="9d72a-122">CLSID\_URLReader</span></span>                                                                                                                     |
| <span data-ttu-id="9d72a-123">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="9d72a-123">Property Page CLSID</span></span>                      | <span data-ttu-id="9d72a-124">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="9d72a-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="9d72a-125">Executável</span><span class="sxs-lookup"><span data-stu-id="9d72a-125">Executable</span></span>                               | <span data-ttu-id="9d72a-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="9d72a-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="9d72a-127">Núcleo</span><span class="sxs-lookup"><span data-stu-id="9d72a-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="9d72a-128">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="9d72a-128">MERIT\_UNLIKELY</span></span>                                                                                                                      |
| [<span data-ttu-id="9d72a-129">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="9d72a-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="9d72a-130">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="9d72a-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="9d72a-131">Comentários</span><span class="sxs-lookup"><span data-stu-id="9d72a-131">Remarks</span></span>

<span data-ttu-id="9d72a-132">Esse filtro usa URLMon e oferece suporte a páginas de código.</span><span class="sxs-lookup"><span data-stu-id="9d72a-132">This filter uses URLMon and supports code pages.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9d72a-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9d72a-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9d72a-134">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="9d72a-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



