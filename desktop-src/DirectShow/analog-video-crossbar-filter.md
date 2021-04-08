---
description: Filtro Crossbar de vídeo analógico
ms.assetid: 668f6a8b-a4ed-4e4a-956c-a87f165225fa
title: Filtro Crossbar de vídeo analógico
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a2eb086b85859a3e1e895cd322c68c56916ac19a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919870"
---
# <a name="analog-video-crossbar-filter"></a><span data-ttu-id="f5fad-103">Filtro Crossbar de vídeo analógico</span><span class="sxs-lookup"><span data-stu-id="f5fad-103">Analog Video Crossbar Filter</span></span>

<span data-ttu-id="f5fad-104">O filtro Crossbar de vídeo analógico representa uma barra de vídeo em um dispositivo de captura de vídeo que dá suporte ao Windows Driver Model (WDM).</span><span class="sxs-lookup"><span data-stu-id="f5fad-104">The Analog Video Crossbar filter represents a video crossbar on a video capture device that supports the Windows Driver Model (WDM).</span></span>

<span data-ttu-id="f5fad-105">Esse filtro é um filtro de wrapper para Crossbars em dispositivos de streaming WDM.</span><span class="sxs-lookup"><span data-stu-id="f5fad-105">This filter is a wrapper filter for crossbars on WDM streaming devices.</span></span> <span data-ttu-id="f5fad-106">O nome amigável do filtro é obtido do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="f5fad-106">The filter's friendly name is taken from the device.</span></span> <span data-ttu-id="f5fad-107">Cada pino de saída representa um caminho de hardware para o vídeo de banda básica analógica.</span><span class="sxs-lookup"><span data-stu-id="f5fad-107">Each output pin represents a hardware path for analog baseband video.</span></span> <span data-ttu-id="f5fad-108">Um dos pinos de entrada vem de um sintonizador de TV (o [filtro de sintonizador de TV](tv-tuner-filter.md)).</span><span class="sxs-lookup"><span data-stu-id="f5fad-108">One of the input pins comes from a TV Tuner (the [TV Tuner Filter](tv-tuner-filter.md)).</span></span> <span data-ttu-id="f5fad-109">Outros Pins de entrada dão suporte a fluxos de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="f5fad-109">Other input pins support video or audio streams.</span></span> <span data-ttu-id="f5fad-110">O filtro dá suporte a quaisquer subtipos de mídia e formatos com suporte nas conexões downstream.</span><span class="sxs-lookup"><span data-stu-id="f5fad-110">The filter supports any media subtypes and formats that are supported on the downstream connections.</span></span>

<span data-ttu-id="f5fad-111">Você não pode criar esse filtro diretamente com CoCreateInstance.</span><span class="sxs-lookup"><span data-stu-id="f5fad-111">You cannot directly create this filter with CoCreateInstance.</span></span> <span data-ttu-id="f5fad-112">A interface [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) adiciona automaticamente esse filtro ao grafo, conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="f5fad-112">The [**ICaptureGraphBuilder2**](/windows/desktop/api/Strmif/nn-strmif-icapturegraphbuilder2) interface automatically adds this filter to the graph as needed.</span></span>

<span data-ttu-id="f5fad-113">Para obter mais informações sobre filtros de wrapper e dispositivos de streaming WDM, consulte [como os dispositivos de hardware participam do grafo de filtro](how-hardware-devices-participate-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="f5fad-113">For more information on wrapper filters and WDM streaming devices, see [How Hardware Devices Participate in the Filter Graph](how-hardware-devices-participate-in-the-filter-graph.md).</span></span>



|                                          |                                                                                                |
|------------------------------------------|------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f5fad-114">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="f5fad-114">Filter Interfaces</span></span>                        | <span data-ttu-id="f5fad-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span><span class="sxs-lookup"><span data-stu-id="f5fad-115">[**IAMCrossbar**](/windows/desktop/api/Strmif/nn-strmif-iamcrossbar), ISpecifyPropertyPages, IPersistPropertyBag, IPersistStream</span></span> |
| <span data-ttu-id="f5fad-116">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="f5fad-116">Input Pin Media Types</span></span>                    | <span data-ttu-id="f5fad-117">MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="f5fad-117">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="f5fad-118">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="f5fad-118">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="f5fad-119">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="f5fad-119">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="f5fad-120">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="f5fad-120">Output Pin Media Types</span></span>                   | <span data-ttu-id="f5fad-121">MEDIATYPE \_ AnalogAudio, MediaType \_ AnalogVideo</span><span class="sxs-lookup"><span data-stu-id="f5fad-121">MEDIATYPE\_AnalogAudio, MEDIATYPE\_AnalogVideo</span></span>                                                 |
| <span data-ttu-id="f5fad-122">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="f5fad-122">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="f5fad-123">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="f5fad-123">**IKsPropertySet**</span></span>](ikspropertyset.md)                                                       |
| <span data-ttu-id="f5fad-124">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="f5fad-124">Filter CLSID</span></span>                             | <span data-ttu-id="f5fad-125">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="f5fad-125">Not applicable</span></span>                                                                                 |
| <span data-ttu-id="f5fad-126">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="f5fad-126">Property Page CLSID</span></span>                      | <span data-ttu-id="f5fad-127">\_CROSSBARFILTERPROPERTYPAGE CLSID</span><span class="sxs-lookup"><span data-stu-id="f5fad-127">CLSID\_CrossbarFilterPropertyPage</span></span>                                                              |
| <span data-ttu-id="f5fad-128">Executável</span><span class="sxs-lookup"><span data-stu-id="f5fad-128">Executable</span></span>                               | <span data-ttu-id="f5fad-129">ksxbar.ax</span><span class="sxs-lookup"><span data-stu-id="f5fad-129">ksxbar.ax</span></span>                                                                                      |
| [<span data-ttu-id="f5fad-130">Núcleo</span><span class="sxs-lookup"><span data-stu-id="f5fad-130">Merit</span></span>](merit.md)                       | <span data-ttu-id="f5fad-131">Dependente de driver.</span><span class="sxs-lookup"><span data-stu-id="f5fad-131">Driver-dependent.</span></span>                                                                              |
| [<span data-ttu-id="f5fad-132">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="f5fad-132">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="f5fad-133">\_KSCATEGORY \_ CROSSBAR</span><span class="sxs-lookup"><span data-stu-id="f5fad-133">AM\_KSCATEGORY\_CROSSBAR</span></span>                                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="f5fad-134">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f5fad-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f5fad-135">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="f5fad-135">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="f5fad-136">Trabalhando com Crossbars</span><span class="sxs-lookup"><span data-stu-id="f5fad-136">Working with Crossbars</span></span>](working-with-crossbars.md)
</dt> </dl>

 

 



