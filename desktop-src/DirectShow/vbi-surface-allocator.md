---
description: Alocador de superfície VBI
ms.assetid: 51c73a25-1112-4fb4-a45f-967c6a1b5c55
title: Alocador de superfície VBI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d4edd698ed37c7b180bee27d0a99e95096080d8e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "103662547"
---
# <a name="vbi-surface-allocator"></a><span data-ttu-id="0e209-103">Alocador de superfície VBI</span><span class="sxs-lookup"><span data-stu-id="0e209-103">VBI Surface Allocator</span></span>

<span data-ttu-id="0e209-104">O alocador de superfície VBI controla a alocação de buffers VBI em gráficos de televisão analógicas com cenários de captura de porta de vídeo de hardware.</span><span class="sxs-lookup"><span data-stu-id="0e209-104">The VBI Surface Allocator controls the allocation of VBI buffers in analog television graphs with hardware video port capture scenarios.</span></span> <span data-ttu-id="0e209-105">Com dispositivos como o decodificador Bt829, o buffer de quadro pode conter vários buffers de captura VBI que são acessados por meio de um mecanismo de hardware proprietário conhecido genericamente como uma porta de vídeo.</span><span class="sxs-lookup"><span data-stu-id="0e209-105">With devices such as the Bt829 decoder, the frame buffer may contain multiple VBI capture buffers that are accessed via a proprietary hardware-based mechanism known generically as a Video Port.</span></span> <span data-ttu-id="0e209-106">O filtro de alocador de superfície VBI conecta downstream do filtro de captura e não tem nenhum pino de saída.</span><span class="sxs-lookup"><span data-stu-id="0e209-106">The VBI Surface Allocator filter connects downstream from the capture filter and has no output pin.</span></span> <span data-ttu-id="0e209-107">O filtro funciona junto com o [mixer de sobreposição](overlay-mixer-filter.md) (via DirectDraw) para executar operações coordenadas na porta de vídeo de hardware, utilizando a mesma memória de buffer de quadro SVGA limitada.</span><span class="sxs-lookup"><span data-stu-id="0e209-107">The filter works closely with the [Overlay Mixer](overlay-mixer-filter.md) (via DirectDraw) to perform coordinated operations on the hardware video port, utilizing the same limited SVGA frame buffer memory.</span></span>



|                                          |                                                                                     |
|------------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0e209-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="0e209-108">Filter Interfaces</span></span>                        | [<span data-ttu-id="0e209-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="0e209-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)                                                  |
| <span data-ttu-id="0e209-110">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="0e209-110">Input Pin Media Types</span></span>                    | <span data-ttu-id="0e209-111">\_Vídeo de MediaType, MEDIASUBTYPE \_ VPVBI</span><span class="sxs-lookup"><span data-stu-id="0e209-111">MEDIATYPE\_Video, MEDIASUBTYPE\_VPVBI</span></span>                                               |
| <span data-ttu-id="0e209-112">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="0e209-112">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="0e209-113">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="0e209-113">**IKsPropertySet**</span></span>](ikspropertyset.md)                                            |
| <span data-ttu-id="0e209-114">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="0e209-114">Output Pin Media Types</span></span>                   | <span data-ttu-id="0e209-115">MEDIATYPE \_ nulo, MEDIASUBTYPE \_ nulo.</span><span class="sxs-lookup"><span data-stu-id="0e209-115">MEDIATYPE\_NULL, MEDIASUBTYPE\_NULL.</span></span> <span data-ttu-id="0e209-116">(Nada está sempre conectado ao pino de saída.)</span><span class="sxs-lookup"><span data-stu-id="0e209-116">(Nothing is ever connected to the output pin.)</span></span> |
| <span data-ttu-id="0e209-117">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="0e209-117">Output Pin Interfaces</span></span>                    | <span data-ttu-id="0e209-118">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="0e209-118">Not applicable.</span></span>                                                                     |
| <span data-ttu-id="0e209-119">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="0e209-119">Filter CLSID</span></span>                             | <span data-ttu-id="0e209-120">\_VBISURFACES CLSID</span><span class="sxs-lookup"><span data-stu-id="0e209-120">CLSID\_VBISurfaces</span></span>                                                                  |
| <span data-ttu-id="0e209-121">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="0e209-121">Property Page CLSID</span></span>                      | <span data-ttu-id="0e209-122">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="0e209-122">No property page.</span></span>                                                                   |
| <span data-ttu-id="0e209-123">Executável</span><span class="sxs-lookup"><span data-stu-id="0e209-123">Executable</span></span>                               | <span data-ttu-id="0e209-124">vbisurf.ax</span><span class="sxs-lookup"><span data-stu-id="0e209-124">vbisurf.ax</span></span>                                                                          |
| [<span data-ttu-id="0e209-125">Núcleo</span><span class="sxs-lookup"><span data-stu-id="0e209-125">Merit</span></span>](merit.md)                       | <span data-ttu-id="0e209-126">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="0e209-126">MERIT\_NORMAL</span></span>                                                                       |
| [<span data-ttu-id="0e209-127">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="0e209-127">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="0e209-128">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="0e209-128">CLSID\_LegacyAmFilterCategory</span></span>                                                       |



 

## <a name="related-topics"></a><span data-ttu-id="0e209-129">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0e209-129">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0e209-130">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="0e209-130">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



