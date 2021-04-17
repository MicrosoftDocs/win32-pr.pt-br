---
description: Filtro de compressor de MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro de compressor de MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a20c559bb889750959a4868fa08c03b3eb12dfb5
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812770"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="7f439-103">Filtro de compressor de MJPEG</span><span class="sxs-lookup"><span data-stu-id="7f439-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="7f439-104">Esse filtro compacta um fluxo de vídeo descompactado, usando a compactação JPEG de movimento.</span><span class="sxs-lookup"><span data-stu-id="7f439-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



|                                          |                                                                                                                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f439-105">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="7f439-105">Filter Interfaces</span></span>                        | <span data-ttu-id="7f439-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="7f439-106">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="7f439-107">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="7f439-107">Input Pin Media Types</span></span>                    | <span data-ttu-id="7f439-108">\_vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="7f439-108">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="7f439-109">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="7f439-109">Input Pin Interfaces</span></span>                     | <span data-ttu-id="7f439-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="7f439-110">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="7f439-111">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="7f439-111">Output Pin Media Types</span></span>                   | <span data-ttu-id="7f439-112">\_Vídeo de MediaType, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="7f439-112">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="7f439-113">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="7f439-113">Output Pin Interfaces</span></span>                    | <span data-ttu-id="7f439-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="7f439-114">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="7f439-115">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="7f439-115">Filter CLSID</span></span>                             | <span data-ttu-id="7f439-116">\_MJPGENC CLSID</span><span class="sxs-lookup"><span data-stu-id="7f439-116">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="7f439-117">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="7f439-117">Property Page CLSID</span></span>                      | <span data-ttu-id="7f439-118">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="7f439-118">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="7f439-119">Executável</span><span class="sxs-lookup"><span data-stu-id="7f439-119">Executable</span></span>                               | <span data-ttu-id="7f439-120">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7f439-120">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="7f439-121">Núcleo</span><span class="sxs-lookup"><span data-stu-id="7f439-121">Merit</span></span>](merit.md)                       | <span data-ttu-id="7f439-122">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="7f439-122">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="7f439-123">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="7f439-123">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="7f439-124">\_VIDEOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="7f439-124">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="7f439-125">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f439-125">Remarks</span></span>

<span data-ttu-id="7f439-126">Esse filtro codifica usando o subtipo de mídia MEDIASUBTYPE \_ MJPG, que corresponde ao código FOURCC ' MJPG '.</span><span class="sxs-lookup"><span data-stu-id="7f439-126">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7f439-127">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7f439-127">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7f439-128">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7f439-128">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



