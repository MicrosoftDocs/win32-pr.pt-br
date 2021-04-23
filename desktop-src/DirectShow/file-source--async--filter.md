---
description: Filtro de origem do arquivo (Async)
ms.assetid: 0cf6e7ab-b1fe-42f9-b682-c5484ef48c71
title: Filtro de origem do arquivo (Async)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1ddeea7398ce332a8b1db444b6b74fe3841f9053
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909694"
---
# <a name="file-source-async-filter"></a><span data-ttu-id="3db5f-103">Filtro de origem do arquivo (Async)</span><span class="sxs-lookup"><span data-stu-id="3db5f-103">File Source (Async) Filter</span></span>

<span data-ttu-id="3db5f-104">O filtro de origem de arquivo assíncrono é aberto e lê os arquivos locais de vários formatos de dados diferentes e passa os dados para um filtro de analisador.</span><span class="sxs-lookup"><span data-stu-id="3db5f-104">The Async File Source filter opens and reads local files of many different data formats and passes the data to a parser filter.</span></span>

<span data-ttu-id="3db5f-105">Para baixar arquivos de mídia da Web por meio de HTTP, use o filtro de [origem do arquivo (URL)](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3db5f-105">To download media files from the web through HTTP, use the [File Source (URL)](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="3db5f-106">Para ler arquivos ASF, use o filtro de [leitor ASF do WM](wm-asf-reader-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="3db5f-106">To read ASF files, use the [WM ASF Reader](wm-asf-reader-filter.md) filter.</span></span>



| <span data-ttu-id="3db5f-107">Label</span><span class="sxs-lookup"><span data-stu-id="3db5f-107">Label</span></span> | <span data-ttu-id="3db5f-108">Valor</span><span class="sxs-lookup"><span data-stu-id="3db5f-108">Value</span></span> |
|------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3db5f-109">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="3db5f-109">Filter Interfaces</span></span>                        | <span data-ttu-id="3db5f-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [ **IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span><span class="sxs-lookup"><span data-stu-id="3db5f-110">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IFileSourceFilter**](/windows/desktop/api/Strmif/nn-strmif-ifilesourcefilter)</span></span>                                                   |
| <span data-ttu-id="3db5f-111">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="3db5f-111">Input Pin Media Types</span></span>                    | <span data-ttu-id="3db5f-112">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3db5f-112">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="3db5f-113">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="3db5f-113">Input Pin Interfaces</span></span>                     | <span data-ttu-id="3db5f-114">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="3db5f-114">Not applicable</span></span>                                                                                                                       |
| <span data-ttu-id="3db5f-115">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="3db5f-115">Output Pin Media Types</span></span>                   | <span data-ttu-id="3db5f-116">**MediaType \_ Fluxo**.</span><span class="sxs-lookup"><span data-stu-id="3db5f-116">**MEDIATYPE\_Stream**.</span></span> <span data-ttu-id="3db5f-117">O subtipo depende do formato de mídia.</span><span class="sxs-lookup"><span data-stu-id="3db5f-117">The subtype depends on the media format.</span></span> <span data-ttu-id="3db5f-118">(**MEDIASUBTYPE \_ NULL** se o filtro não reconhecer o formato.)</span><span class="sxs-lookup"><span data-stu-id="3db5f-118">(**MEDIASUBTYPE\_NULL** if the filter doesn't recognize the format.)</span></span> |
| <span data-ttu-id="3db5f-119">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="3db5f-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="3db5f-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span><span class="sxs-lookup"><span data-stu-id="3db5f-120">[**IAMAsyncReaderTimestampScaling**](/windows/desktop/api/Strmif/nn-strmif-iamasyncreadertimestampscaling), [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin)</span></span> |
| <span data-ttu-id="3db5f-121">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="3db5f-121">Filter CLSID</span></span>                             | <span data-ttu-id="3db5f-122">**\_ASYNCREADER CLSID**</span><span class="sxs-lookup"><span data-stu-id="3db5f-122">**CLSID\_AsyncReader**</span></span>                                                                                                               |
| <span data-ttu-id="3db5f-123">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="3db5f-123">Property Page CLSID</span></span>                      | <span data-ttu-id="3db5f-124">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="3db5f-124">No property page</span></span>                                                                                                                     |
| <span data-ttu-id="3db5f-125">Executável</span><span class="sxs-lookup"><span data-stu-id="3db5f-125">Executable</span></span>                               | <span data-ttu-id="3db5f-126">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="3db5f-126">quartz.dll</span></span>                                                                                                                           |
| [<span data-ttu-id="3db5f-127">Núcleo</span><span class="sxs-lookup"><span data-stu-id="3db5f-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="3db5f-128">**MÉRITO \_ improvável**</span><span class="sxs-lookup"><span data-stu-id="3db5f-128">**MERIT\_UNLIKELY**</span></span>                                                                                                                  |
| [<span data-ttu-id="3db5f-129">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="3db5f-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="3db5f-130">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="3db5f-130">**CLSID\_LegacyAmFilterCategory**</span></span>                                                                                                    |



 

## <a name="related-topics"></a><span data-ttu-id="3db5f-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3db5f-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3db5f-132">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="3db5f-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



