---
description: Filtro de compressor de MJPEG
ms.assetid: de30a2c4-3e51-4f2b-b3f9-ed78e2d6512d
title: Filtro de compressor de MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 02928df4d09b50c0ac152aed99ed87dc6362fb70
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910004"
---
# <a name="mjpeg-compressor-filter"></a><span data-ttu-id="4b9b7-103">Filtro de compressor de MJPEG</span><span class="sxs-lookup"><span data-stu-id="4b9b7-103">MJPEG Compressor Filter</span></span>

<span data-ttu-id="4b9b7-104">Esse filtro compacta um fluxo de vídeo descompactado, usando a compactação JPEG de movimento.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-104">This filter compresses an uncompressed video stream, using motion JPEG compression.</span></span>



| <span data-ttu-id="4b9b7-105">Label</span><span class="sxs-lookup"><span data-stu-id="4b9b7-105">Label</span></span> | <span data-ttu-id="4b9b7-106">Valor</span><span class="sxs-lookup"><span data-stu-id="4b9b7-106">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4b9b7-107">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="4b9b7-107">Filter Interfaces</span></span>                        | <span data-ttu-id="4b9b7-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span><span class="sxs-lookup"><span data-stu-id="4b9b7-108">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), **IPersistStream**</span></span>                                                                                                                                                                                             |
| <span data-ttu-id="4b9b7-109">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="4b9b7-109">Input Pin Media Types</span></span>                    | <span data-ttu-id="4b9b7-110">\_vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="4b9b7-110">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="4b9b7-111">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="4b9b7-111">Input Pin Interfaces</span></span>                     | <span data-ttu-id="4b9b7-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="4b9b7-112">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                                                                                                                             |
| <span data-ttu-id="4b9b7-113">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="4b9b7-113">Output Pin Media Types</span></span>                   | <span data-ttu-id="4b9b7-114">\_Vídeo de MediaType, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="4b9b7-114">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                                                                                                                               |
| <span data-ttu-id="4b9b7-115">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="4b9b7-115">Output Pin Interfaces</span></span>                    | <span data-ttu-id="4b9b7-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="4b9b7-116">[**IAMStreamConfig**](/windows/desktop/api/Strmif/nn-strmif-iamstreamconfig), [**IAMVideoCompression**](/windows/desktop/api/Strmif/nn-strmif-iamvideocompression), [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="4b9b7-117">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="4b9b7-117">Filter CLSID</span></span>                             | <span data-ttu-id="4b9b7-118">\_MJPGENC CLSID</span><span class="sxs-lookup"><span data-stu-id="4b9b7-118">CLSID\_MJPGEnc</span></span>                                                                                                                                                                                                                                     |
| <span data-ttu-id="4b9b7-119">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="4b9b7-119">Property Page CLSID</span></span>                      | <span data-ttu-id="4b9b7-120">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="4b9b7-120">No property page</span></span>                                                                                                                                                                                                                                   |
| <span data-ttu-id="4b9b7-121">Executável</span><span class="sxs-lookup"><span data-stu-id="4b9b7-121">Executable</span></span>                               | <span data-ttu-id="4b9b7-122">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="4b9b7-122">quartz.dll</span></span>                                                                                                                                                                                                                                         |
| [<span data-ttu-id="4b9b7-123">Núcleo</span><span class="sxs-lookup"><span data-stu-id="4b9b7-123">Merit</span></span>](merit.md)                       | <span data-ttu-id="4b9b7-124">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="4b9b7-124">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                                                                                                |
| [<span data-ttu-id="4b9b7-125">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="4b9b7-125">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="4b9b7-126">\_VIDEOCOMPRESSORCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="4b9b7-126">CLSID\_VideoCompressorCategory</span></span>                                                                                                                                                                                                                     |



 

## <a name="remarks"></a><span data-ttu-id="4b9b7-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="4b9b7-127">Remarks</span></span>

<span data-ttu-id="4b9b7-128">Esse filtro codifica usando o subtipo de mídia MEDIASUBTYPE \_ MJPG, que corresponde ao código FOURCC ' MJPG '.</span><span class="sxs-lookup"><span data-stu-id="4b9b7-128">This filter encodes using the media subtype MEDIASUBTYPE\_MJPG, which corresponds to the FOURCC code 'MJPG'.</span></span>

## <a name="related-topics"></a><span data-ttu-id="4b9b7-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="4b9b7-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="4b9b7-130">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="4b9b7-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



