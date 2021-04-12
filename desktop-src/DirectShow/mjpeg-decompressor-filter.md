---
description: Filtro de descompactação de MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro de descompactação de MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ebe8f5f19cb94d75c1ce01cd94dc723100560de
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500651"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="199e1-103">Filtro de descompactação de MJPEG</span><span class="sxs-lookup"><span data-stu-id="199e1-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="199e1-104">Esse filtro decodifica um fluxo de vídeo do movimento JPEG para vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="199e1-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="199e1-105">Algumas câmeras de vídeo digital produzem um fluxo de vídeo JPEG de movimento.</span><span class="sxs-lookup"><span data-stu-id="199e1-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="199e1-106">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="199e1-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="199e1-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="199e1-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="199e1-108">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="199e1-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="199e1-109">\_Vídeo de MediaType, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="199e1-109">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="199e1-110">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="199e1-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="199e1-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="199e1-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="199e1-112">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="199e1-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="199e1-113">\_vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="199e1-113">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="199e1-114">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="199e1-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="199e1-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="199e1-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="199e1-116">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="199e1-116">Filter CLSID</span></span>                             | <span data-ttu-id="199e1-117">\_MJPEGDEC CLSID</span><span class="sxs-lookup"><span data-stu-id="199e1-117">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="199e1-118">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="199e1-118">Property Page CLSID</span></span>                      | <span data-ttu-id="199e1-119">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="199e1-119">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="199e1-120">Executável</span><span class="sxs-lookup"><span data-stu-id="199e1-120">Executable</span></span>                               | <span data-ttu-id="199e1-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="199e1-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="199e1-122">Núcleo</span><span class="sxs-lookup"><span data-stu-id="199e1-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="199e1-123">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="199e1-123">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="199e1-124">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="199e1-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="199e1-125">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="199e1-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="199e1-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="199e1-126">Remarks</span></span>

<span data-ttu-id="199e1-127">Esse filtro é compatível com o vídeo JPEG de movimento que usa o código FOURCC ' MJPG '.</span><span class="sxs-lookup"><span data-stu-id="199e1-127">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="199e1-128">Ele não pode decodificar outras variedades de JPEG de movimento.</span><span class="sxs-lookup"><span data-stu-id="199e1-128">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="199e1-129">Para isso, será necessário usar um filtro de decodificador de terceiros.</span><span class="sxs-lookup"><span data-stu-id="199e1-129">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="199e1-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="199e1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="199e1-131">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="199e1-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



