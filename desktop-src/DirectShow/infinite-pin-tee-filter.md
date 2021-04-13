---
description: Filtro de t de PIN infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro de t de PIN infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90e9a80baf047cdd5559fadaa0f13ea1352d4ed0
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370260"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="bde9c-103">Filtro de t de PIN infinito</span><span class="sxs-lookup"><span data-stu-id="bde9c-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="bde9c-104">Esse filtro fornece amostras entregues ao seu pino de entrada para um número variável de Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="bde9c-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="bde9c-105">Quando uma instância do filtro é criada, ela tem um pino de saída.</span><span class="sxs-lookup"><span data-stu-id="bde9c-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="bde9c-106">Cada vez que um pino de saída é conectado, o filtro cria outro pino de saída.</span><span class="sxs-lookup"><span data-stu-id="bde9c-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="bde9c-107">Todos os Pins de saída compartilham o mesmo tipo de mídia que o pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="bde9c-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="bde9c-108">Uma versão desse filtro também é fornecida como um exemplo de SDK.</span><span class="sxs-lookup"><span data-stu-id="bde9c-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="bde9c-109">Consulte [exemplo de filtro InfTee](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="bde9c-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



|                                          |                                                                                                                                                    |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bde9c-110">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="bde9c-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="bde9c-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="bde9c-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="bde9c-112">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="bde9c-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="bde9c-113">Qualquer tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="bde9c-113">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="bde9c-114">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="bde9c-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="bde9c-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="bde9c-115">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="bde9c-116">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="bde9c-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="bde9c-117">Qualquer tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="bde9c-117">Any media type.</span></span> <span data-ttu-id="bde9c-118">O tipo de saída sempre corresponde ao tipo de entrada, para todos os Pins de saída</span><span class="sxs-lookup"><span data-stu-id="bde9c-118">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="bde9c-119">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="bde9c-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="bde9c-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="bde9c-120">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="bde9c-121">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="bde9c-121">Filter CLSID</span></span>                             | <span data-ttu-id="bde9c-122">\_INFTEE CLSID</span><span class="sxs-lookup"><span data-stu-id="bde9c-122">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="bde9c-123">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="bde9c-123">Property Page CLSID</span></span>                      | <span data-ttu-id="bde9c-124">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="bde9c-124">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="bde9c-125">Executável</span><span class="sxs-lookup"><span data-stu-id="bde9c-125">Executable</span></span>                               | <span data-ttu-id="bde9c-126">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="bde9c-126">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="bde9c-127">Núcleo</span><span class="sxs-lookup"><span data-stu-id="bde9c-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="bde9c-128">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="bde9c-128">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="bde9c-129">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="bde9c-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="bde9c-130">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="bde9c-130">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="bde9c-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bde9c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bde9c-132">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="bde9c-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



