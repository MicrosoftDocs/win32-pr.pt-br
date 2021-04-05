---
description: Filtro de compressor AVI
ms.assetid: addde51d-2982-4964-b16a-406fea89a0ce
title: Filtro de compressor AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58f3ef342d1ea740503d9fc1e9e9b898aadc3801
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103825481"
---
# <a name="avi-compressor-filter"></a><span data-ttu-id="a081e-103">Filtro de compressor AVI</span><span class="sxs-lookup"><span data-stu-id="a081e-103">AVI Compressor Filter</span></span>

<span data-ttu-id="a081e-104">O filtro AVI compressor permite que os codecs do VCM (Gerenciador de compactação de vídeo) ingressem em um grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="a081e-104">The AVI Compressor filter enables Video Compression Manager (VCM) codecs to join a filter graph.</span></span> <span data-ttu-id="a081e-105">Cada codec aparece como uma instância separada do filtro.</span><span class="sxs-lookup"><span data-stu-id="a081e-105">Each codec appears as a separate instance of the filter.</span></span> <span data-ttu-id="a081e-106">Você não pode criar esse filtro diretamente com CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="a081e-106">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="a081e-107">Em vez disso, você deve usar o enumerador de dispositivo do sistema.</span><span class="sxs-lookup"><span data-stu-id="a081e-107">Instead, you must use the system device enumerator.</span></span> <span data-ttu-id="a081e-108">Para obter mais informações, consulte [usando o enumerador de dispositivo do sistema](using-the-system-device-enumerator.md).</span><span class="sxs-lookup"><span data-stu-id="a081e-108">For more information, see [Using the System Device Enumerator](using-the-system-device-enumerator.md).</span></span>

<span data-ttu-id="a081e-109">O PIN de entrada do filtro se conecta a filtros que geram dados de vídeo não compactados, como filtros de captura de vídeo ou o [filtro de Splitter AVI](avi-splitter-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a081e-109">The filter's input pin connects to filters that output uncompressed video data, such as video capture filters or the [AVI Splitter Filter](avi-splitter-filter.md).</span></span> <span data-ttu-id="a081e-110">O pino de saída do filtro normalmente se conecta a um filtro MUX, como o [filtro AVI Mux](avi-mux-filter.md).</span><span class="sxs-lookup"><span data-stu-id="a081e-110">The filter's output pin typically connects to a MUX filter, such as the [AVI Mux Filter](avi-mux-filter.md).</span></span>

<span data-ttu-id="a081e-111">Se o codec der suporte a uma caixa de diálogo de configuração de VFW estilo antigo ou a caixa de diálogo sobre, um aplicativo poderá exibi-lo usando a interface [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) .</span><span class="sxs-lookup"><span data-stu-id="a081e-111">If the codec supports an old-style VFW configuration dialog box or About dialog box, an application can display it using the [**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs) interface.</span></span>

> [!Note]  
> <span data-ttu-id="a081e-112">Os compactadores MPEG nunca são implementados como codecs VCM, mas somente como filtros nativos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a081e-112">MPEG compressors are never implemented as VCM codecs, but only as native DirectShow filters.</span></span>

 



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a081e-113">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="a081e-113">Filter Interfaces</span></span>                        | <span data-ttu-id="a081e-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span><span class="sxs-lookup"><span data-stu-id="a081e-114">[**IAMVfwCompressDialogs**](/windows/desktop/api/Strmif/nn-strmif-iamvfwcompressdialogs), [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), IPersistPropertyBag, ISpecifyPropertyPages</span></span>                                                                                                             |
| <span data-ttu-id="a081e-115">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a081e-115">Input Pin Media Types</span></span>                    | <span data-ttu-id="a081e-116">\_Vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="a081e-116">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="a081e-117">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a081e-117">Input Pin Interfaces</span></span>                     | <span data-ttu-id="a081e-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a081e-118">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="a081e-119">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="a081e-119">Output Pin Media Types</span></span>                   | <span data-ttu-id="a081e-120">\_Vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="a081e-120">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="a081e-121">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="a081e-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a081e-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a081e-122">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="a081e-123">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="a081e-123">Filter CLSID</span></span>                             | <span data-ttu-id="a081e-124">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="a081e-124">Not applicable</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="a081e-125">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="a081e-125">Property Page CLSID</span></span>                      | <span data-ttu-id="a081e-126">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="a081e-126">No property page.</span></span>                                                                                                                                                                                                                                  |
| <span data-ttu-id="a081e-127">Executável</span><span class="sxs-lookup"><span data-stu-id="a081e-127">Executable</span></span>                               | <span data-ttu-id="a081e-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="a081e-128">qcap.dll</span></span>                                                                                                                                                                                                                                           |
| [<span data-ttu-id="a081e-129">Núcleo</span><span class="sxs-lookup"><span data-stu-id="a081e-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="a081e-130">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="a081e-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="a081e-131">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="a081e-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a081e-132">\_VIDEOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="a081e-132">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="related-topics"></a><span data-ttu-id="a081e-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a081e-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a081e-134">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="a081e-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



