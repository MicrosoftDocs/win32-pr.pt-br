---
description: Filtro de sintonizador de TV
ms.assetid: a8e101dc-78ab-495f-9086-7b1d1e87c357
title: Filtro de sintonizador de TV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81dd03b965275f5e9b9405b027c8e66a7fb0f157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "104297360"
---
# <a name="tv-tuner-filter"></a><span data-ttu-id="02ec0-103">Filtro de sintonizador de TV</span><span class="sxs-lookup"><span data-stu-id="02ec0-103">TV Tuner Filter</span></span>

<span data-ttu-id="02ec0-104">O filtro de sintonizador de TV seleciona uma difusão analógica ou canal de cabo a ser exibido.</span><span class="sxs-lookup"><span data-stu-id="02ec0-104">The TV Tuner filter selects an analog broadcast or cable channel to be viewed.</span></span> <span data-ttu-id="02ec0-105">O fluxo de saída único é um caminho de hardware para o vídeo de banda básica analógica.</span><span class="sxs-lookup"><span data-stu-id="02ec0-105">The single output stream is a hardware path for analog baseband video.</span></span> <span data-ttu-id="02ec0-106">Essa saída deve se conectar ao filtro Crossbar de vídeo analógico.</span><span class="sxs-lookup"><span data-stu-id="02ec0-106">This output should connect to the Analog Video Crossbar filter.</span></span> <span data-ttu-id="02ec0-107">Os Pins de entrada incluem uma entrada para o cabo e uma entrada de antena.</span><span class="sxs-lookup"><span data-stu-id="02ec0-107">The input pins include an input for cable and an antenna input.</span></span>



|                                          |                                                                                                                                                                                   |
|------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="02ec0-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="02ec0-108">Filter Interfaces</span></span>                        | <span data-ttu-id="02ec0-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span><span class="sxs-lookup"><span data-stu-id="02ec0-109">[**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter), [**IAMTVTuner**](/windows/desktop/api/Strmif/nn-strmif-iamtvtuner), **ISpecifyPropertyPages**, **IPersistPropertyBag**, **IKsObject**, [**IKsPropertySet**](ikspropertyset.md)</span></span> |
| <span data-ttu-id="02ec0-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="02ec0-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="02ec0-111">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="02ec0-111">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="02ec0-112">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="02ec0-112">Input Pin Interfaces</span></span>                     | <span data-ttu-id="02ec0-113">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="02ec0-113">Not applicable.</span></span>                                                                                                                                                                   |
| <span data-ttu-id="02ec0-114">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="02ec0-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="02ec0-115">Vídeo: MEDIATYPE \_ AnalogVideo, \_ subtipo de KSDATAFORMAT \_ nenhum áudio: MediaType \_ AnalogAudio, MEDIASUBTYPE \_ nulo</span><span class="sxs-lookup"><span data-stu-id="02ec0-115">Video: MEDIATYPE\_AnalogVideo, KSDATAFORMAT\_SUBTYPE\_NONE Audio: MEDIATYPE\_AnalogAudio, MEDIASUBTYPE\_NULL</span></span>                                                                      |
| <span data-ttu-id="02ec0-116">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="02ec0-116">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="02ec0-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="02ec0-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                                                                                                                                              |
| <span data-ttu-id="02ec0-118">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="02ec0-118">Filter CLSID</span></span>                             | <span data-ttu-id="02ec0-119">\_TVTUNERFILTER CLSID</span><span class="sxs-lookup"><span data-stu-id="02ec0-119">CLSID\_TVTunerFilter</span></span>                                                                                                                                                              |
| <span data-ttu-id="02ec0-120">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="02ec0-120">Property Page CLSID</span></span>                      | <span data-ttu-id="02ec0-121">\_TVTUNERFILTERPROPERTYPAGE CLSID</span><span class="sxs-lookup"><span data-stu-id="02ec0-121">CLSID\_TVTunerFilterPropertyPage</span></span>                                                                                                                                                  |
| <span data-ttu-id="02ec0-122">Executável</span><span class="sxs-lookup"><span data-stu-id="02ec0-122">Executable</span></span>                               | <span data-ttu-id="02ec0-123">KSTVTune.ax</span><span class="sxs-lookup"><span data-stu-id="02ec0-123">KSTVTune.ax</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="02ec0-124">Núcleo</span><span class="sxs-lookup"><span data-stu-id="02ec0-124">Merit</span></span>](merit.md)                       | <span data-ttu-id="02ec0-125">MÉRITO \_ \_ não \_ use</span><span class="sxs-lookup"><span data-stu-id="02ec0-125">MERIT\_DO\_NOT\_USE</span></span>                                                                                                                                                               |
| [<span data-ttu-id="02ec0-126">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="02ec0-126">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="02ec0-127">\_KSCATEGORY \_ TVTUNER</span><span class="sxs-lookup"><span data-stu-id="02ec0-127">AM\_KSCATEGORY\_TVTUNER</span></span>                                                                                                                                                           |



 

## <a name="related-topics"></a><span data-ttu-id="02ec0-128">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="02ec0-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="02ec0-129">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="02ec0-129">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



