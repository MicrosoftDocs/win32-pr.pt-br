---
description: Filtro de descompactação de MJPEG
ms.assetid: 0862fd8c-7e64-4472-9405-4d8e31e4401f
title: Filtro de descompactação de MJPEG
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 23a3e3c09d218a83f5243bf6702d3b5fc3ae1c16
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107910014"
---
# <a name="mjpeg-decompressor-filter"></a><span data-ttu-id="a4c4e-103">Filtro de descompactação de MJPEG</span><span class="sxs-lookup"><span data-stu-id="a4c4e-103">MJPEG Decompressor Filter</span></span>

<span data-ttu-id="a4c4e-104">Esse filtro decodifica um fluxo de vídeo do movimento JPEG para vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-104">This filter decodes a video stream from motion JPEG to uncompressed video.</span></span> <span data-ttu-id="a4c4e-105">Algumas câmeras de vídeo digital produzem um fluxo de vídeo JPEG de movimento.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-105">Some digital video cameras produce a motion JPEG video stream.</span></span>



| <span data-ttu-id="a4c4e-106">Label</span><span class="sxs-lookup"><span data-stu-id="a4c4e-106">Label</span></span> | <span data-ttu-id="a4c4e-107">Valor</span><span class="sxs-lookup"><span data-stu-id="a4c4e-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a4c4e-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="a4c4e-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="a4c4e-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="a4c4e-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="a4c4e-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a4c4e-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="a4c4e-111">\_Vídeo de MediaType, MEDIASUBTYPE \_ MJPG</span><span class="sxs-lookup"><span data-stu-id="a4c4e-111">MEDIATYPE\_Video, MEDIASUBTYPE\_MJPG</span></span>                                                                                                               |
| <span data-ttu-id="a4c4e-112">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a4c4e-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="a4c4e-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a4c4e-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="a4c4e-114">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="a4c4e-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="a4c4e-115">\_vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="a4c4e-115">MEDIATYPE\_VIDEO, MEDIASUBTYPE\_NULL</span></span>                                                                                                               |
| <span data-ttu-id="a4c4e-116">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="a4c4e-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="a4c4e-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="a4c4e-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="a4c4e-118">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="a4c4e-118">Filter CLSID</span></span>                             | <span data-ttu-id="a4c4e-119">\_MJPEGDEC CLSID</span><span class="sxs-lookup"><span data-stu-id="a4c4e-119">CLSID\_MjpegDec</span></span>                                                                                                                                    |
| <span data-ttu-id="a4c4e-120">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="a4c4e-120">Property Page CLSID</span></span>                      | <span data-ttu-id="a4c4e-121">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="a4c4e-121">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="a4c4e-122">Executável</span><span class="sxs-lookup"><span data-stu-id="a4c4e-122">Executable</span></span>                               | <span data-ttu-id="a4c4e-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="a4c4e-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="a4c4e-124">Núcleo</span><span class="sxs-lookup"><span data-stu-id="a4c4e-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="a4c4e-125">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="a4c4e-125">MERIT\_NORMAL</span></span>                                                                                                                                      |
| [<span data-ttu-id="a4c4e-126">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="a4c4e-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="a4c4e-127">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="a4c4e-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="remarks"></a><span data-ttu-id="a4c4e-128">Comentários</span><span class="sxs-lookup"><span data-stu-id="a4c4e-128">Remarks</span></span>

<span data-ttu-id="a4c4e-129">Esse filtro é compatível com o vídeo JPEG de movimento que usa o código FOURCC ' MJPG '.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-129">This filter is compatible with motion JPEG video that uses the FOURCC code 'MJPG'.</span></span> <span data-ttu-id="a4c4e-130">Ele não pode decodificar outras variedades de JPEG de movimento.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-130">It cannot decode other varieties of motion JPEG.</span></span> <span data-ttu-id="a4c4e-131">Para isso, será necessário usar um filtro de decodificador de terceiros.</span><span class="sxs-lookup"><span data-stu-id="a4c4e-131">For these, you will need to use a third-party decoder filter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a4c4e-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a4c4e-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a4c4e-133">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="a4c4e-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



