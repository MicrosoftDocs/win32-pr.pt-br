---
description: Alocador de superfície VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Alocador de superfície VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5849b23b8f21a7b49e477060386628ba4c19b2e5
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909004"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="e5da0-103">Alocador de superfície VBI</span><span class="sxs-lookup"><span data-stu-id="e5da0-103">VBI Surface Allocator</span></span>

<span data-ttu-id="e5da0-104">O alocador de superfície VBI controla a alocação de buffers VBI em gráficos de televisão analógicas com cenários de captura de porta de vídeo de hardware.</span><span class="sxs-lookup"><span data-stu-id="e5da0-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="e5da0-105">Com dispositivos como o decodificador Bt829, o buffer de quadro pode conter vários buffers de captura VBI que são acessados por meio de um mecanismo de hardware proprietário conhecido genericamente como uma porta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="e5da0-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="e5da0-106">O filtro de alocador de superfície VBI conecta downstream do filtro de captura e não tem nenhum pino de saída.</span><span class="sxs-lookup"><span data-stu-id="e5da0-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="e5da0-107">O filtro funciona junto com o [mixer de sobreposição](overlay-mixer-filter.md) (via DirectDraw) para executar operações coordenadas na porta de vídeo de hardware, utilizando a mesma memória de buffer de quadro SVGA limitada.</span><span class="sxs-lookup"><span data-stu-id="e5da0-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



| <span data-ttu-id="e5da0-108">Label</span><span class="sxs-lookup"><span data-stu-id="e5da0-108">Label</span></span> | <span data-ttu-id="e5da0-109">Valor</span><span class="sxs-lookup"><span data-stu-id="e5da0-109">Value</span></span> |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e5da0-110">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="e5da0-110">Filter Interfaces</span></span>                        | [<span data-ttu-id="e5da0-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="e5da0-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="e5da0-112">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="e5da0-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="e5da0-113">\_Vídeo de MediaType, MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="e5da0-113">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="e5da0-114">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="e5da0-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="e5da0-115">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="e5da0-115">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="e5da0-116">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="e5da0-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="e5da0-117">MEDIATYPE \_ nulo, MEDIASUBTYPE \_ nulo.</span><span class="sxs-lookup"><span data-stu-id="e5da0-117">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="e5da0-118">(Nada está sempre conectado ao pino de saída.)</span><span class="sxs-lookup"><span data-stu-id="e5da0-118">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="e5da0-119">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="e5da0-119">Output Pin Interfaces</span></span>                    | <span data-ttu-id="e5da0-120">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="e5da0-120">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="e5da0-121">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="e5da0-121">Filter CLSID</span></span>                             | <span data-ttu-id="e5da0-122">\_VBISURFACES CLSID</span><span class="sxs-lookup"><span data-stu-id="e5da0-122">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="e5da0-123">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="e5da0-123">Property Page CLSID</span></span>                      | <span data-ttu-id="e5da0-124">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e5da0-124">No property page.</span></span>                                                                   |
| <span data-ttu-id="e5da0-125">Executável</span><span class="sxs-lookup"><span data-stu-id="e5da0-125">Executable</span></span>                               | <span data-ttu-id="e5da0-126">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="e5da0-126">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="e5da0-127">Núcleo</span><span class="sxs-lookup"><span data-stu-id="e5da0-127">Merit</span></span>](merit.md)                       | <span data-ttu-id="e5da0-128">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="e5da0-128">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="e5da0-129">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="e5da0-129">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="e5da0-130">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="e5da0-130">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="e5da0-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e5da0-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e5da0-132">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="e5da0-132">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



