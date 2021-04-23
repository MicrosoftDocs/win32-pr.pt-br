---
description: Filtro de t de PIN infinito
ms.assetid: 5f3e06ec-adee-4bc7-8ea8-cce3030d3baa
title: Filtro de t de PIN infinito
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3433a0c2f5fe55fa59c42ed6e02d34f6e2cf0e6d
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909224"
---
# <a name="infinite-pin-tee-filter"></a><span data-ttu-id="1abba-103">Filtro de t de PIN infinito</span><span class="sxs-lookup"><span data-stu-id="1abba-103">Infinite Pin Tee Filter</span></span>

<span data-ttu-id="1abba-104">Esse filtro fornece amostras entregues ao seu pino de entrada para um número variável de Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="1abba-104">This filter delivers samples delivered to its input pin to a variable number of output pins.</span></span> <span data-ttu-id="1abba-105">Quando uma instância do filtro é criada, ela tem um pino de saída.</span><span class="sxs-lookup"><span data-stu-id="1abba-105">When an instance of the filter is created, it has one output pin.</span></span> <span data-ttu-id="1abba-106">Cada vez que um pino de saída é conectado, o filtro cria outro pino de saída.</span><span class="sxs-lookup"><span data-stu-id="1abba-106">Each time an output pin is connected, the filter creates another output pin.</span></span> <span data-ttu-id="1abba-107">Todos os Pins de saída compartilham o mesmo tipo de mídia que o pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="1abba-107">All output pins share the same media type as the input pin.</span></span>

<span data-ttu-id="1abba-108">Uma versão desse filtro também é fornecida como um exemplo de SDK.</span><span class="sxs-lookup"><span data-stu-id="1abba-108">A version of this filter is also provided as an SDK sample.</span></span> <span data-ttu-id="1abba-109">Consulte [exemplo de filtro InfTee](inftee-filter-sample.md).</span><span class="sxs-lookup"><span data-stu-id="1abba-109">See [InfTee Filter Sample](inftee-filter-sample.md).</span></span>



| <span data-ttu-id="1abba-110">Label</span><span class="sxs-lookup"><span data-stu-id="1abba-110">Label</span></span> | <span data-ttu-id="1abba-111">Valor</span><span class="sxs-lookup"><span data-stu-id="1abba-111">Value</span></span> |
|------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1abba-112">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="1abba-112">Filter Interfaces</span></span>                        | [<span data-ttu-id="1abba-113">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="1abba-113">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                                                                                 |
| <span data-ttu-id="1abba-114">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="1abba-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="1abba-115">Qualquer tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="1abba-115">Any media type</span></span>                                                                                                                                     |
| <span data-ttu-id="1abba-116">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="1abba-116">Input Pin Interfaces</span></span>                     | <span data-ttu-id="1abba-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1abba-117">[**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span>                                             |
| <span data-ttu-id="1abba-118">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="1abba-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="1abba-119">Qualquer tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="1abba-119">Any media type.</span></span> <span data-ttu-id="1abba-120">O tipo de saída sempre corresponde ao tipo de entrada, para todos os Pins de saída</span><span class="sxs-lookup"><span data-stu-id="1abba-120">The output type always matches the input type, for all output pins</span></span>                                                                 |
| <span data-ttu-id="1abba-121">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="1abba-121">Output Pin Interfaces</span></span>                    | <span data-ttu-id="1abba-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span><span class="sxs-lookup"><span data-stu-id="1abba-122">[**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking), [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin), [**IQualityControl**](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)</span></span> |
| <span data-ttu-id="1abba-123">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="1abba-123">Filter CLSID</span></span>                             | <span data-ttu-id="1abba-124">\_INFTEE CLSID</span><span class="sxs-lookup"><span data-stu-id="1abba-124">CLSID\_InfTee</span></span>                                                                                                                                      |
| <span data-ttu-id="1abba-125">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="1abba-125">Property Page CLSID</span></span>                      | <span data-ttu-id="1abba-126">Nenhuma página de propriedades</span><span class="sxs-lookup"><span data-stu-id="1abba-126">No property page</span></span>                                                                                                                                   |
| <span data-ttu-id="1abba-127">Executável</span><span class="sxs-lookup"><span data-stu-id="1abba-127">Executable</span></span>                               | <span data-ttu-id="1abba-128">qcap.dll</span><span class="sxs-lookup"><span data-stu-id="1abba-128">qcap.dll</span></span>                                                                                                                                           |
| [<span data-ttu-id="1abba-129">Núcleo</span><span class="sxs-lookup"><span data-stu-id="1abba-129">Merit</span></span>](merit.md)                       | <span data-ttu-id="1abba-130">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="1abba-130">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                |
| [<span data-ttu-id="1abba-131">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="1abba-131">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="1abba-132">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="1abba-132">CLSID\_LegacyAmFilterCategory</span></span>                                                                                                                      |



 

## <a name="related-topics"></a><span data-ttu-id="1abba-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1abba-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1abba-134">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="1abba-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



