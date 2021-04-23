---
description: Filtro de "t" inteligente
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro de "t" inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c52077066f69e50fbb5218012a402a8d556c15c1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909294"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="96ad9-103">Filtro de "t" inteligente</span><span class="sxs-lookup"><span data-stu-id="96ad9-103">Smart Tee Filter</span></span>

<span data-ttu-id="96ad9-104">O filtro de monitoração inteligente é usado em gráficos de captura de vídeo para dividir o fluxo de vídeo em um fluxo de visualização e em um fluxo de captura.</span><span class="sxs-lookup"><span data-stu-id="96ad9-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="96ad9-105">Isso é feito sem qualquer cópia de dados adicional.</span><span class="sxs-lookup"><span data-stu-id="96ad9-105">This is done without any additional data copying.</span></span> <span data-ttu-id="96ad9-106">Os Pins de saída dão suporte a qualquer tipo de mídia com suporte na conexão de downstream.</span><span class="sxs-lookup"><span data-stu-id="96ad9-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="96ad9-107">O filtro de monitoração inteligente é útil quando um filtro de captura de vídeo não fornece Pins separados para captura e visualização.</span><span class="sxs-lookup"><span data-stu-id="96ad9-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="96ad9-108">O filtro de desempenho inteligente só fornecerá dados de visualização se isso não prejudicar o desempenho da captura.</span><span class="sxs-lookup"><span data-stu-id="96ad9-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="96ad9-109">Ele também remove os carimbos de data/hora do fluxo de visualização.</span><span class="sxs-lookup"><span data-stu-id="96ad9-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="96ad9-110">O construtor de grafo de captura insere automaticamente o filtro de "t inteligente" quando necessário.</span><span class="sxs-lookup"><span data-stu-id="96ad9-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="96ad9-111">Para obter mais informações, consulte [combinando captura de vídeo e visualização](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="96ad9-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="96ad9-112">A ilustração a seguir mostra um grafo de captura típico que usa o filtro de "t" inteligente.</span><span class="sxs-lookup"><span data-stu-id="96ad9-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![usando o filtro de "t inteligente"](images/smarttee.png)



| <span data-ttu-id="96ad9-114">Label</span><span class="sxs-lookup"><span data-stu-id="96ad9-114">Label</span></span> | <span data-ttu-id="96ad9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="96ad9-115">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96ad9-116">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="96ad9-116">Filter Interfaces</span></span>                        | [<span data-ttu-id="96ad9-117">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="96ad9-117">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="96ad9-118">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="96ad9-118">Input Pin Media Types</span></span>                    | <span data-ttu-id="96ad9-119">\_Vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="96ad9-119">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="96ad9-120">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="96ad9-120">Input Pin Interfaces</span></span>                     | <span data-ttu-id="96ad9-121">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="96ad9-121">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="96ad9-122">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="96ad9-122">Output Pin Media Types</span></span>                   | <span data-ttu-id="96ad9-123">\_Vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="96ad9-123">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="96ad9-124">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="96ad9-124">Output Pin Interfaces</span></span>                    | <span data-ttu-id="96ad9-125">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="96ad9-125">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="96ad9-126">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="96ad9-126">Filter CLSID</span></span>                             | <span data-ttu-id="96ad9-127">\_SMARTTEE CLSID</span><span class="sxs-lookup"><span data-stu-id="96ad9-127">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="96ad9-128">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="96ad9-128">Property Page CLSID</span></span>                      | <span data-ttu-id="96ad9-129">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="96ad9-129">No property page.</span></span>                                                                                              |
| <span data-ttu-id="96ad9-130">Executável</span><span class="sxs-lookup"><span data-stu-id="96ad9-130">Executable</span></span>                               | <span data-ttu-id="96ad9-131">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="96ad9-131">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="96ad9-132">Núcleo</span><span class="sxs-lookup"><span data-stu-id="96ad9-132">Merit</span></span>](merit.md)                       | <span data-ttu-id="96ad9-133">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="96ad9-133">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="96ad9-134">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="96ad9-134">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="96ad9-135">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="96ad9-135">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="96ad9-136">Comentários</span><span class="sxs-lookup"><span data-stu-id="96ad9-136">Remarks</span></span>

<span data-ttu-id="96ad9-137">O pino de captura é o pino de saída 0 e o pino de visualização é o pino de saída 1.</span><span class="sxs-lookup"><span data-stu-id="96ad9-137">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="96ad9-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="96ad9-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="96ad9-139">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="96ad9-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



