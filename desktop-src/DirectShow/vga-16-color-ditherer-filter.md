---
description: Filtro de separador de cores VGA 16
ms.assetid: 0a5f4e92-e703-4487-91b0-15265744004e
title: Filtro de separador de cores VGA 16
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 11d343843b002eb205e1d0718b282546bdc19907
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908674"
---
# <a name="vga-16-color-ditherer-filter"></a><span data-ttu-id="b60ba-103">Filtro de separador de cores VGA 16</span><span class="sxs-lookup"><span data-stu-id="b60ba-103">VGA 16 Color Ditherer Filter</span></span>

<span data-ttu-id="b60ba-104">O filtro de separador de cores VGA 16 converte de um tipo de cor RGB em uma exibição de cor de 4 bits para que os fluxos de vídeo AVI e MPEG possam ser exibidos em monitores mais antigos de 16 cores.</span><span class="sxs-lookup"><span data-stu-id="b60ba-104">The VGA 16 Color Ditherer filter converts from an RGB color type to a 4-bit color display so that AVI and MPEG video streams may be displayed on older 16-color monitors.</span></span> <span data-ttu-id="b60ba-105">Esse filtro é inserido no grafo entre um filtro de descompactador e um filtro de processador de vídeo.</span><span class="sxs-lookup"><span data-stu-id="b60ba-105">This filter is inserted in the graph between a decompressor filter and a video renderer filter.</span></span>



| <span data-ttu-id="b60ba-106">Label</span><span class="sxs-lookup"><span data-stu-id="b60ba-106">Label</span></span> | <span data-ttu-id="b60ba-107">Valor</span><span class="sxs-lookup"><span data-stu-id="b60ba-107">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b60ba-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="b60ba-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="b60ba-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="b60ba-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="b60ba-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="b60ba-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="b60ba-111">\_Vídeo de MediaType, MEDIASUBTYPE \_ RGB8</span><span class="sxs-lookup"><span data-stu-id="b60ba-111">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB8</span></span>                                                                                                               |
| <span data-ttu-id="b60ba-112">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="b60ba-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="b60ba-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b60ba-113">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="b60ba-114">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="b60ba-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="b60ba-115">\_Vídeo de MediaType, MEDIASUBTYPE \_ RGB4</span><span class="sxs-lookup"><span data-stu-id="b60ba-115">MEDIATYPE\_Video, MEDIASUBTYPE\_RGB4</span></span>                                                                                                               |
| <span data-ttu-id="b60ba-116">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="b60ba-116">Output Pin Interfaces</span></span>                    | <span data-ttu-id="b60ba-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="b60ba-117">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="b60ba-118">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="b60ba-118">Filter CLSID</span></span>                             | <span data-ttu-id="b60ba-119">\_Pontilhamento de CLSID</span><span class="sxs-lookup"><span data-stu-id="b60ba-119">CLSID\_Dither</span></span>                                                                                                                                      |
| <span data-ttu-id="b60ba-120">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="b60ba-120">Property Page CLSID</span></span>                      | <span data-ttu-id="b60ba-121">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="b60ba-121">No property page.</span></span>                                                                                                                                  |
| <span data-ttu-id="b60ba-122">Executável</span><span class="sxs-lookup"><span data-stu-id="b60ba-122">Executable</span></span>                               | <span data-ttu-id="b60ba-123">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="b60ba-123">quartz.dll</span></span>                                                                                                                                         |
| [<span data-ttu-id="b60ba-124">Núcleo</span><span class="sxs-lookup"><span data-stu-id="b60ba-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="b60ba-125">MÉRITO \_ improvável</span><span class="sxs-lookup"><span data-stu-id="b60ba-125">MERIT\_UNLIKELY</span></span>                                                                                                                                    |
| [<span data-ttu-id="b60ba-126">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="b60ba-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b60ba-127">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="b60ba-127">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="b60ba-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b60ba-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b60ba-129">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="b60ba-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



