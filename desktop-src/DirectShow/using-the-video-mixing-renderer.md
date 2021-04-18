---
description: Usando o processador de mixagem de vídeo
ms.assetid: 3d0fdfac-ec7e-4e02-886b-2039c607dac7
title: Usando o processador de mixagem de vídeo
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5baf7d559eed0d3111876924520952b55c6da2e6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105778780"
---
# <a name="using-the-video-mixing-renderer"></a><span data-ttu-id="e0f01-103">Usando o processador de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="e0f01-103">Using the Video Mixing Renderer</span></span>

<span data-ttu-id="e0f01-104">Em termos de desempenho e amplitude de recursos, o filtro de processador de mixagem de vídeo (VMR) representa a próxima geração na renderização de vídeo na plataforma Windows.</span><span class="sxs-lookup"><span data-stu-id="e0f01-104">In terms of both performance and breadth of features, the Video Mixing Renderer (VMR) filter represents the next generation in video rendering on the Windows platform.</span></span> <span data-ttu-id="e0f01-105">O VMR substitui o [mixer de sobreposição](overlay-mixer-filter.md) e o [processador de vídeo](video-renderer-filter.md), além de adicionar muitos novos recursos de mixagem.</span><span class="sxs-lookup"><span data-stu-id="e0f01-105">The VMR replaces the [Overlay Mixer](overlay-mixer-filter.md) and [Video Renderer](video-renderer-filter.md), and adds many new mixing features.</span></span>

<span data-ttu-id="e0f01-106">Há duas versões do VMR:</span><span class="sxs-lookup"><span data-stu-id="e0f01-106">There are two versions of the VMR:</span></span>

-   <span data-ttu-id="e0f01-107">O VMR-7, que usa o DirectDraw 7 para renderização.</span><span class="sxs-lookup"><span data-stu-id="e0f01-107">The VMR-7, which uses DirectDraw 7 for rendering.</span></span>
-   <span data-ttu-id="e0f01-108">O VMR-9, que usa o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e0f01-108">The VMR-9, which uses Direct3D 9.</span></span>

<span data-ttu-id="e0f01-109">O VMR-7 está disponível no Windows XP e posterior, mas não está disponível para redistribuição.</span><span class="sxs-lookup"><span data-stu-id="e0f01-109">The VMR-7 is available on Windows XP and later, but is not available for redistribution.</span></span> <span data-ttu-id="e0f01-110">O VMR-9 está disponível para redistribuição em todas as plataformas com suporte no DirectX 9.</span><span class="sxs-lookup"><span data-stu-id="e0f01-110">The VMR-9 is available for redistribution on all platforms supported by DirectX 9.</span></span> <span data-ttu-id="e0f01-111">Os dois filtros do VMR são muito semelhantes em sua implementação e nas interfaces que eles expõem.</span><span class="sxs-lookup"><span data-stu-id="e0f01-111">The two VMR filters are very similar in their implementation and the interfaces that they expose.</span></span>

<span data-ttu-id="e0f01-112">O VMR-9 tem seu próprio CLSID e seu próprio conjunto de interfaces, estruturas e tipos de enumeração que nem sempre são idênticos aos tipos de dados correspondentes para o VMR-7, devido às diferenças subjacentes entre o DirectDraw 7 e o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="e0f01-112">The VMR-9 has its own CLSID and its own set of interfaces, structures and enumeration types which are not always identical to the corresponding data types for the VMR-7, due to the underlying differences between DirectDraw 7 and Direct3D 9.</span></span> <span data-ttu-id="e0f01-113">Todas as interfaces do VMR-9 terminam com "9", por exemplo, **IVMRStreamConfig9**, e as estruturas e os tipos de enumeração têm "VMR9" em seu nome para diferenciá-las dos tipos de dados usados com o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="e0f01-113">The VMR-9 interfaces all end with "9", for example **IVMRStreamConfig9**, and the structures and enumeration types all have "VMR9" in their name to distinguish them from the data types used with the VMR-7.</span></span>

<span data-ttu-id="e0f01-114">Para garantir a compatibilidade com versões anteriores, o VMR-9 não é o renderizador padrão em nenhum sistema.</span><span class="sxs-lookup"><span data-stu-id="e0f01-114">To ensure backward-compatibility, the VMR-9 is not the default renderer on any system.</span></span> <span data-ttu-id="e0f01-115">Para usar o VMR-9, você deve adicioná-lo explicitamente ao grafo de filtro usando o método [**IFilterGraph:: addfiltro**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) e configurá-lo antes de conectá-lo a qualquer filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="e0f01-115">To use the VMR-9, you must explicitly add it to the filter graph using the [**IFilterGraph::AddFilter**](/windows/desktop/api/Strmif/nf-strmif-ifiltergraph-addfilter) method, and configure it before connecting it to any upstream filters.</span></span>

<span data-ttu-id="e0f01-116">Este artigo inclui as seções a seguir.</span><span class="sxs-lookup"><span data-stu-id="e0f01-116">This article contains the following sections.</span></span> <span data-ttu-id="e0f01-117">Exceto quando indicado, as informações nessas seções se aplicam aos filtros VMR-7 e VMR-9.</span><span class="sxs-lookup"><span data-stu-id="e0f01-117">Except where noted, the information in these sections applies to both the VMR-7 and the VMR-9 filters.</span></span>

-   [<span data-ttu-id="e0f01-118">Sobre o processamento de mixagem de vídeo</span><span class="sxs-lookup"><span data-stu-id="e0f01-118">About the Video Mixing Render</span></span>](about-the-video-mixing-render.md)
-   [<span data-ttu-id="e0f01-119">Modos de operação do VMR</span><span class="sxs-lookup"><span data-stu-id="e0f01-119">VMR Modes of Operation</span></span>](vmr-modes-of-operation.md)
-   [<span data-ttu-id="e0f01-120">Criando um grafo de filtro do VMR-9</span><span class="sxs-lookup"><span data-stu-id="e0f01-120">Building a VMR-9 Filter Graph</span></span>](building-a-vmr-9-filter-graph.md)
-   [<span data-ttu-id="e0f01-121">Usando o modo de mixagem do VMR</span><span class="sxs-lookup"><span data-stu-id="e0f01-121">Using VMR Mixing Mode</span></span>](using-vmr-mixing-mode.md)
-   [<span data-ttu-id="e0f01-122">Definindo preferências de desentrelaçamento</span><span class="sxs-lookup"><span data-stu-id="e0f01-122">Setting Deinterlace Preferences</span></span>](setting-deinterlace-preferences.md)
-   [<span data-ttu-id="e0f01-123">Usando o VMR para desenvolvedores de filtro do DirectShow</span><span class="sxs-lookup"><span data-stu-id="e0f01-123">Using the VMR for DirectShow Filter Developers</span></span>](using-the-vmr-for-directshow-filter-developers.md)
-   [<span data-ttu-id="e0f01-124">Usando o protocolo COPP (certificado de proteção de saída)</span><span class="sxs-lookup"><span data-stu-id="e0f01-124">Using Certified Output Protection Protocol (COPP)</span></span>](using-certified-output-protection-protocol--copp.md)

## <a name="related-topics"></a><span data-ttu-id="e0f01-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e0f01-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e0f01-126">Filtro de processador de mixagem de vídeo 7</span><span class="sxs-lookup"><span data-stu-id="e0f01-126">Video Mixing Renderer Filter 7</span></span>](video-mixing-renderer-filter-7.md)
</dt> <dt>

[<span data-ttu-id="e0f01-127">Filtro de processador de mixagem de vídeo 9</span><span class="sxs-lookup"><span data-stu-id="e0f01-127">Video Mixing Renderer Filter 9</span></span>](video-mixing-renderer-filter-9.md)
</dt> </dl>

 

 



