---
description: Filtro de origem do arquivo (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro de origem do arquivo (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 403564b751e53f160ab140ac89bfda4fd9576f00
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456606"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="0e591-103">Filtro de origem do arquivo (Async)</span><span class="sxs-lookup"><span data-stu-id="0e591-103">File Source (Async) Filter</span></span>

<span data-ttu-id="0e591-104">O filtro de origem de arquivo assíncrono é aberto e lê os arquivos locais de vários formatos de dados diferentes e passa os dados para um filtro de analisador.</span><span class="sxs-lookup"><span data-stu-id="0e591-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="0e591-105">Para baixar arquivos de mídia da Web por meio de HTTP, use o filtro de [origem do arquivo (URL)](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0e591-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="0e591-106">Para ler arquivos ASF, use o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="0e591-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



|                                          |                                                                                                                                      |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0e591-107">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="0e591-107">Filter Interfaces</span></span>                        | <span data-ttu-id="0e591-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="0e591-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="0e591-109">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="0e591-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="0e591-110">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="0e591-110">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="0e591-111">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="0e591-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="0e591-112">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="0e591-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="0e591-113">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="0e591-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="0e591-114">**MediaType \_ Fluxo**.</span><span class="sxs-lookup"><span data-stu-id="0e591-114">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="0e591-115">O subtipo depende do formato de mídia.</span><span class="sxs-lookup"><span data-stu-id="0e591-115">The subtype depends on the media format.</span></span> <span data-ttu-id="0e591-116">(**MEDIASUBTYPE \_ NULL** se o filtro não reconhecer o formato.)</span><span class="sxs-lookup"><span data-stu-id="0e591-116">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="0e591-117">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="0e591-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="0e591-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="0e591-118">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="0e591-119">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="0e591-119">Filter CLSID</span></span>                             | <span data-ttu-id="0e591-120">**\_ASYNCREADER CLSID**</span><span class="sxs-lookup"><span data-stu-id="0e591-120">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="0e591-121">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="0e591-121">Property Page CLSID</span></span>                      | <span data-ttu-id="0e591-122">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="0e591-122">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="0e591-123">Executável</span><span class="sxs-lookup"><span data-stu-id="0e591-123">Executable</span></span>                               | <span data-ttu-id="0e591-124">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="0e591-124">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="0e591-125">Núcleo</span><span class="sxs-lookup"><span data-stu-id="0e591-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="0e591-126">**MÉRITO \_ improvável**</span><span class="sxs-lookup"><span data-stu-id="0e591-126">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="0e591-127">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="0e591-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0e591-128">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="0e591-128">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="0e591-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e591-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e591-130">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0e591-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



