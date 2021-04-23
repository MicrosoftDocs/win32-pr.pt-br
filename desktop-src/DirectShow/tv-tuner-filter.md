---
description: Filtro de sintonizador de TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro de sintonizador de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90f1fa68d7fc2723839882dd232e630dbe128634
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909024"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="e55a2-103">Filtro de sintonizador de TV</span><span class="sxs-lookup"><span data-stu-id="e55a2-103">TV Tuner Filter</span></span>

<span data-ttu-id="e55a2-104">O filtro de sintonizador de TV seleciona uma difusão analógica ou canal de cabo a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="e55a2-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="e55a2-105">O fluxo de saída único é um caminho de hardware para o vídeo de banda básica analógica.</span><span class="sxs-lookup"><span data-stu-id="e55a2-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="e55a2-106">Essa saída deve se conectar ao filtro Crossbar de vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="e55a2-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="e55a2-107">Os Pins de entrada incluem uma entrada para o cabo e uma entrada de antena.</span><span class="sxs-lookup"><span data-stu-id="e55a2-107">The input pins include an input for cable and an antenna input.</span></span>



| <span data-ttu-id="e55a2-108">Label</span><span class="sxs-lookup"><span data-stu-id="e55a2-108">Label</span></span> | <span data-ttu-id="e55a2-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e55a2-109">Value</span></span> |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e55a2-110">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="e55a2-110">Filter Interfaces</span></span>                        | <span data-ttu-id="e55a2-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="e55a2-111">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="e55a2-112">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="e55a2-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="e55a2-113">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="e55a2-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="e55a2-114">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="e55a2-114">Input Pin Interfaces</span></span>                     | <span data-ttu-id="e55a2-115">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="e55a2-115">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="e55a2-116">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="e55a2-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="e55a2-117">Vídeo: MEDIATYPE \_ AnalogVideo, \_ subtipo de KSDATAFORMAT \_ nenhum áudio: MediaType \_ AnalogAudio, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="e55a2-117">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="e55a2-118">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="e55a2-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="e55a2-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="e55a2-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="e55a2-120">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="e55a2-120">Filter CLSID</span></span>                             | <span data-ttu-id="e55a2-121">\_TVTUNERFILTER CLSID</span><span class="sxs-lookup"><span data-stu-id="e55a2-121">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="e55a2-122">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="e55a2-122">Property Page CLSID</span></span>                      | <span data-ttu-id="e55a2-123">\_TVTUNERFILTERPROPERTYPAGE CLSID</span><span class="sxs-lookup"><span data-stu-id="e55a2-123">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="e55a2-124">Executável</span><span class="sxs-lookup"><span data-stu-id="e55a2-124">Executable</span></span>                               | <span data-ttu-id="e55a2-125">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="e55a2-125">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="e55a2-126">Núcleo</span><span class="sxs-lookup"><span data-stu-id="e55a2-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="e55a2-127">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="e55a2-127">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="e55a2-128">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="e55a2-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="e55a2-129">\_KSCATEGORY \_ TVTUNER</span><span class="sxs-lookup"><span data-stu-id="e55a2-129">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="e55a2-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e55a2-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e55a2-131">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="e55a2-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



