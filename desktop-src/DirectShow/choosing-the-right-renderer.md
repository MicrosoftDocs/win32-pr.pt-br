---
description: Escolhendo o processador de vídeo correto
ms.assetid: c57c4c68-ea1c-4198-94b4-e9b6e53bb625
title: Escolhendo o processador de vídeo correto
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38a334fec59f6e3631217d48df7f0e8c83d87462
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105812850"
---
# <a name="choosing-the-right-video-renderer"></a><span data-ttu-id="ccf9d-103">Escolhendo o processador de vídeo correto</span><span class="sxs-lookup"><span data-stu-id="ccf9d-103">Choosing the Right Video Renderer</span></span>

<span data-ttu-id="ccf9d-104">O DirectShow fornece vários filtros de processador de vídeo, resumidos na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-104">DirectShow provides several video renderer filters, summarized in the following table.</span></span>



| <span data-ttu-id="ccf9d-105">Filtrar</span><span class="sxs-lookup"><span data-stu-id="ccf9d-105">Filter</span></span>                                                                  | <span data-ttu-id="ccf9d-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="ccf9d-106">Remarks</span></span>                                           |
|-------------------------------------------------------------------------|---------------------------------------------------|
| <span data-ttu-id="ccf9d-107">[**Processador de vídeo avançado**](enhanced-video-renderer-filter.md) (EVR)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-107">[**Enhanced Video Renderer**](enhanced-video-renderer-filter.md) (EVR)</span></span> | <span data-ttu-id="ccf9d-108">Usa o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-108">Uses Direct3D 9.</span></span> <span data-ttu-id="ccf9d-109">Requer o Windows Vista ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-109">Requires Windows Vista or later.</span></span> |
| <span data-ttu-id="ccf9d-110">[Processador de mixagem de vídeo 9](video-mixing-renderer-filter-9.md) (VMR-9)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-110">[Video Mixing Renderer 9](video-mixing-renderer-filter-9.md) (VMR-9)</span></span>   | <span data-ttu-id="ccf9d-111">Usa o Direct3D 9.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-111">Uses Direct3D 9.</span></span> <span data-ttu-id="ccf9d-112">Requer o Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-112">Requires Windows XP or later.</span></span>    |
| <span data-ttu-id="ccf9d-113">[Filtro de mixagem de vídeo 7](video-mixing-renderer-filter-7.md) (VMR-7)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-113">[Video Mixing Filter 7](video-mixing-renderer-filter-7.md) (VMR-7)</span></span>     | <span data-ttu-id="ccf9d-114">Usa o DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-114">Uses DirectDraw.</span></span> <span data-ttu-id="ccf9d-115">Requer o Windows XP ou posterior.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-115">Requires Windows XP or later.</span></span>    |
| [<span data-ttu-id="ccf9d-116">Mixer de sobreposição</span><span class="sxs-lookup"><span data-stu-id="ccf9d-116">Overlay Mixer</span></span>](using-the-overlay-mixer-in-video-capture.md)           | <span data-ttu-id="ccf9d-117">Dá suporte a sobreposições de hardware por meio do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-117">Supports hardware overlays through DirectDraw.</span></span>    |
| <span data-ttu-id="ccf9d-118">Filtro de [renderização de vídeo](video-renderer-filter.md) herdado.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-118">Legacy [Video Renderer](video-renderer-filter.md) filter.</span></span>              | <span data-ttu-id="ccf9d-119">Usa o DirectDraw ou o GDI (raramente)</span><span class="sxs-lookup"><span data-stu-id="ccf9d-119">Uses DirectDraw or (rarely) GDI</span></span>                   |



 

<span data-ttu-id="ccf9d-120">O renderizador a ser usado depende em grande parte das versões do Windows às quais você precisa dar suporte.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-120">Which renderer to use depends largely on which versions of Windows you need to support.</span></span>

-   <span data-ttu-id="ccf9d-121">No Windows Vista e posterior, os aplicativos devem usar o EVR se o hardware der suporte a ele.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-121">In Windows Vista and later, applications should use the EVR if the hardware supports it.</span></span> <span data-ttu-id="ccf9d-122">Caso contrário, retorne para o VMR-9 ou o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-122">Otherwise, fall back to the VMR-9 or VMR-7.</span></span> <span data-ttu-id="ccf9d-123">O EVR oferece melhor desempenho e melhor qualidade de vídeo do que os renderizadores anteriores.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-123">The EVR offers better performance and better video quality than previous renderers.</span></span> <span data-ttu-id="ccf9d-124">Além disso, ele foi projetado para trabalhar com o Gerenciador de Janelas da Área de Trabalho (DWM).</span><span class="sxs-lookup"><span data-stu-id="ccf9d-124">Also, it is designed to work with the Desktop Window Manager (DWM).</span></span>
-   <span data-ttu-id="ccf9d-125">Antes do Windows Vista, use o VMR-9 se o hardware der suporte à funcionalidade de porta de vídeo e a ela não for necessária.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-125">Prior to Windows Vista, use the VMR-9 if the hardware supports it and video port functionality is not required.</span></span> <span data-ttu-id="ccf9d-126">Caso contrário, use o VMR-7.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-126">Otherwise, use the VMR-7.</span></span>
-   <span data-ttu-id="ccf9d-127">Em sistemas mais antigos, talvez seja necessário usar o mixer de sobreposição (para porta de vídeo ou suporte à sobreposição de hardware) ou o filtro de renderização de vídeo herdado.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-127">On older systems, you might need to use the Overlay Mixer (for video port or hardware overlay support) or the legacy Video Renderer filter.</span></span>

<span data-ttu-id="ccf9d-128">Os métodos [**IGraphBuilder:: render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) e [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) usam o VMR-7 por padrão.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-128">The [**IGraphBuilder::Render**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-render) and [**RenderFile**](/windows/desktop/api/Strmif/nf-strmif-igraphbuilder-renderfile) methods use the VMR-7 by default.</span></span> <span data-ttu-id="ccf9d-129">Se o hardware não oferecer suporte ao VMR-7, esses métodos retornarão ao filtro de renderização de vídeo herdado.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-129">If the hardware does not support the VMR-7, these methods fall back to the legacy Video Renderer filter.</span></span> <span data-ttu-id="ccf9d-130">O EVR e o VMR-9 nunca são os renderizadores padrão.</span><span class="sxs-lookup"><span data-stu-id="ccf9d-130">The EVR and VMR-9 are never the default renderers.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ccf9d-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ccf9d-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ccf9d-132">Renderização de vídeo</span><span class="sxs-lookup"><span data-stu-id="ccf9d-132">Video Rendering</span></span>](video-rendering.md)
</dt> </dl>

 

 



