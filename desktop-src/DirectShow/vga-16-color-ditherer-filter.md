---
description: Filtro de separador de cores VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro de separador de cores VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85db9d8fad706c96f19bb5bea6b0476b0ddec735
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104011315"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="3c97c-103">Filtro de separador de cores VGA 16</span><span class="sxs-lookup"><span data-stu-id="3c97c-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="3c97c-104">O filtro de separador de cores VGA 16 converte de um tipo de cor RGB em uma exibição de cor de 4 bits para que os fluxos de vídeo AVI e MPEG possam ser exibidos em monitores mais antigos de 16 cores.</span><span class="sxs-lookup"><span data-stu-id="3c97c-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="3c97c-105">Esse filtro é inserido no grafo entre um filtro de descompactador e um filtro de processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="3c97c-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3c97c-106">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="3c97c-106">Filter Interfaces</span></span>                        | [<span data-ttu-id="3c97c-107">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="3c97c-107">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="3c97c-108">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="3c97c-108">Input Pin Media Types</span></span>                    | <span data-ttu-id="3c97c-109">\_Vídeo de MediaType, MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="3c97c-109">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="3c97c-110">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="3c97c-110">Input Pin Interfaces</span></span>                     | <span data-ttu-id="3c97c-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3c97c-111">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="3c97c-112">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="3c97c-112">Output Pin Media Types</span></span>                   | <span data-ttu-id="3c97c-113">\_Vídeo de MediaType, MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="3c97c-113">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="3c97c-114">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="3c97c-114">Output Pin Interfaces</span></span>                    | <span data-ttu-id="3c97c-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="3c97c-115">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="3c97c-116">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="3c97c-116">Filter CLSID</span></span>                             | <span data-ttu-id="3c97c-117">\_Pontilhamento de CLSID</span><span class="sxs-lookup"><span data-stu-id="3c97c-117">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="3c97c-118">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="3c97c-118">Property Page CLSID</span></span>                      | <span data-ttu-id="3c97c-119">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="3c97c-119">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="3c97c-120">Executável</span><span class="sxs-lookup"><span data-stu-id="3c97c-120">Executable</span></span>                               | <span data-ttu-id="3c97c-121">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="3c97c-121">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="3c97c-122">Núcleo</span><span class="sxs-lookup"><span data-stu-id="3c97c-122">Merit</span></span>](merit.md)                       | <span data-ttu-id="3c97c-123">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="3c97c-123">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="3c97c-124">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="3c97c-124">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="3c97c-125">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="3c97c-125">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="3c97c-126">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="3c97c-126">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3c97c-127">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="3c97c-127">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



