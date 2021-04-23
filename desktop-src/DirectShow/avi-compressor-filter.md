---
description: Filtro de compressor AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro de compressor AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 212ab58eb3800e0ad5531ebc5c50d3b054e7866c
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909464"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="f965b-103">Filtro de compressor AVI</span><span class="sxs-lookup"><span data-stu-id="f965b-103">AVI Compressor Filter</span></span>

<span data-ttu-id="f965b-104">O filtro AVI compressor permite que os codecs do VCM (Gerenciador de compactação de vídeo) ingressem em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="f965b-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="f965b-105">Cada codec aparece como uma instância separada do filtro.</span><span class="sxs-lookup"><span data-stu-id="f965b-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="f965b-106">Você não pode criar esse filtro diretamente com CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="f965b-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="f965b-107">Em vez disso, você deve usar o enumerador de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="f965b-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="f965b-108">Para obter mais informações, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="f965b-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="f965b-109">O PIN de entrada do filtro se conecta a filtros que geram dados de vídeo não compactados, como filtros de captura de vídeo ou o [filtro de Splitter AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f965b-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="f965b-110">O pino de saída do filtro normalmente se conecta a um filtro MUX, como o [filtro AVI Mux](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="f965b-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="f965b-111">Se o codec der suporte a uma caixa de diálogo de configuração de VFW estilo antigo ou a caixa de diálogo sobre, um aplicativo poderá exibi-lo usando a interface [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .</span><span class="sxs-lookup"><span data-stu-id="f965b-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="f965b-112">Os compactadores MPEG nunca são implementados como codecs VCM, mas somente como filtros nativos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="f965b-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



| <span data-ttu-id="f965b-113">Label</span><span class="sxs-lookup"><span data-stu-id="f965b-113">Label</span></span> | <span data-ttu-id="f965b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="f965b-114">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f965b-115">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="f965b-115">Filter Interfaces</span></span>                        | <span data-ttu-id="f965b-116">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="f965b-116">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="f965b-117">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="f965b-117">Input Pin Media Types</span></span>                    | <span data-ttu-id="f965b-118">\_Vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="f965b-118">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="f965b-119">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="f965b-119">Input Pin Interfaces</span></span>                     | <span data-ttu-id="f965b-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f965b-120">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="f965b-121">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="f965b-121">Output Pin Media Types</span></span>                   | <span data-ttu-id="f965b-122">\_Vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="f965b-122">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="f965b-123">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="f965b-123">Output Pin Interfaces</span></span>                    | <span data-ttu-id="f965b-124">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="f965b-124">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="f965b-125">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="f965b-125">Filter CLSID</span></span>                             | <span data-ttu-id="f965b-126">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f965b-126">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="f965b-127">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="f965b-127">Property Page CLSID</span></span>                      | <span data-ttu-id="f965b-128">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="f965b-128">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="f965b-129">Executável</span><span class="sxs-lookup"><span data-stu-id="f965b-129">Executable</span></span>                               | <span data-ttu-id="f965b-130">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="f965b-130">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="f965b-131">Núcleo</span><span class="sxs-lookup"><span data-stu-id="f965b-131">Merit</span></span>](merit.md)                       | <span data-ttu-id="f965b-132">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="f965b-132">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="f965b-133">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="f965b-133">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f965b-134">\_VIDEOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="f965b-134">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="f965b-135">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f965b-135">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f965b-136">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f965b-136">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



