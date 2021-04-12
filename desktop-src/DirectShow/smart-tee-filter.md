---
description: Filtro de "t" inteligente
ms.assetid: 25bfbd62-b6be-4d1f-aa4c-77798bbb9fc9
title: Filtro de "t" inteligente
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 647e04ef2a24bde43c9d02b7986fd8a645a6b60c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456769"
---
# <a name="smart-tee-filter"></a><span data-ttu-id="9e40f-103">Filtro de "t" inteligente</span><span class="sxs-lookup"><span data-stu-id="9e40f-103">Smart Tee Filter</span></span>

<span data-ttu-id="9e40f-104">O filtro de monitoração inteligente é usado em gráficos de captura de vídeo para dividir o fluxo de vídeo em um fluxo de visualização e em um fluxo de captura.</span><span class="sxs-lookup"><span data-stu-id="9e40f-104">The Smart Tee filter is used in video capture graphs to split the video stream into a preview stream and a capture stream.</span></span> <span data-ttu-id="9e40f-105">Isso é feito sem qualquer cópia de dados adicional.</span><span class="sxs-lookup"><span data-stu-id="9e40f-105">This is done without any additional data copying.</span></span> <span data-ttu-id="9e40f-106">Os Pins de saída dão suporte a qualquer tipo de mídia com suporte na conexão de downstream.</span><span class="sxs-lookup"><span data-stu-id="9e40f-106">The output pins support whatever media types are supported on the downstream connection.</span></span>

<span data-ttu-id="9e40f-107">O filtro de monitoração inteligente é útil quando um filtro de captura de vídeo não fornece Pins separados para captura e visualização.</span><span class="sxs-lookup"><span data-stu-id="9e40f-107">The Smart Tee filter is useful when a video capture filter does not provide separate pins for capture and preview.</span></span> <span data-ttu-id="9e40f-108">O filtro de desempenho inteligente só fornecerá dados de visualização se isso não prejudicar o desempenho da captura.</span><span class="sxs-lookup"><span data-stu-id="9e40f-108">The Smart Tee filter delivers preview data only if doing so does not hurt capture performance.</span></span> <span data-ttu-id="9e40f-109">Ele também remove os carimbos de data/hora do fluxo de visualização.</span><span class="sxs-lookup"><span data-stu-id="9e40f-109">It also removes the time stamps from the preview stream.</span></span> <span data-ttu-id="9e40f-110">O construtor de grafo de captura insere automaticamente o filtro de "t inteligente" quando necessário.</span><span class="sxs-lookup"><span data-stu-id="9e40f-110">The capture graph builder automatically inserts the Smart Tee filter when needed.</span></span> <span data-ttu-id="9e40f-111">Para obter mais informações, consulte [combinando captura de vídeo e visualização](combining-video-capture-and-preview.md).</span><span class="sxs-lookup"><span data-stu-id="9e40f-111">For more information, see [Combining Video Capture and Preview](combining-video-capture-and-preview.md).</span></span>

<span data-ttu-id="9e40f-112">A ilustração a seguir mostra um grafo de captura típico que usa o filtro de "t" inteligente.</span><span class="sxs-lookup"><span data-stu-id="9e40f-112">The following illustration shows a typical capture graph that uses the Smart Tee filter.</span></span>

![usando o filtro de "t inteligente"](images/smarttee.png)



|                                          |                                                                                                                |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9e40f-114">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="9e40f-114">Filter Interfaces</span></span>                        | [<span data-ttu-id="9e40f-115">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="9e40f-115">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                             |
| <span data-ttu-id="9e40f-116">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="9e40f-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="9e40f-117">\_Vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="9e40f-117">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="9e40f-118">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="9e40f-118">Input Pin Interfaces</span></span>                     | <span data-ttu-id="9e40f-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="9e40f-119">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>         |
| <span data-ttu-id="9e40f-120">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="9e40f-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="9e40f-121">\_Vídeo de MediaType, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="9e40f-121">MEDIATYPE\_Video, MEDIASUBTYPE\_NULL</span></span>                                                                           |
| <span data-ttu-id="9e40f-122">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="9e40f-122">Output Pin Interfaces</span></span>                    | <span data-ttu-id="9e40f-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="9e40f-123">[**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="9e40f-124">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="9e40f-124">Filter CLSID</span></span>                             | <span data-ttu-id="9e40f-125">\_SMARTTEE CLSID</span><span class="sxs-lookup"><span data-stu-id="9e40f-125">CLSID\_SmartTee</span></span>                                                                                                |
| <span data-ttu-id="9e40f-126">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="9e40f-126">Property Page CLSID</span></span>                      | <span data-ttu-id="9e40f-127">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9e40f-127">No property page.</span></span>                                                                                              |
| <span data-ttu-id="9e40f-128">Executável</span><span class="sxs-lookup"><span data-stu-id="9e40f-128">Executable</span></span>                               | <span data-ttu-id="9e40f-129">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="9e40f-129">qcap.dll</span></span>                                                                                                       |
| [<span data-ttu-id="9e40f-130">Núcleo</span><span class="sxs-lookup"><span data-stu-id="9e40f-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="9e40f-131">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="9e40f-131">MERIT\_DO\_NOT\_USE</span></span>                                                                                            |
| [<span data-ttu-id="9e40f-132">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="9e40f-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="9e40f-133">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="9e40f-133">CLSID\_LegacyAmFilterCategory</span></span>                                                                                  |



 

## <a name="remarks"></a><span data-ttu-id="9e40f-134">Comentários</span><span class="sxs-lookup"><span data-stu-id="9e40f-134">Remarks</span></span>

<span data-ttu-id="9e40f-135">O pino de captura é o pino de saída 0 e o pino de visualização é o pino de saída 1.</span><span class="sxs-lookup"><span data-stu-id="9e40f-135">The capture pin is output pin 0, and the preview pin is output pin 1.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9e40f-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9e40f-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9e40f-137">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="9e40f-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



