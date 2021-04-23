---
description: Filtro de decodificador de WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro de decodificador de WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eb6804f82e5d15aa324feb163261544969e3c45
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908474"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="b8e45-103">Filtro de decodificador de WST</span><span class="sxs-lookup"><span data-stu-id="b8e45-103">WST Decoder Filter</span></span>

<span data-ttu-id="b8e45-104">Este componente foi removido do Windows Vista e de sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="b8e45-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="b8e45-105">Ele está disponível para uso nos sistemas operacionais Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="b8e45-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="b8e45-106">A partir do Windows Vista, o DirectShow não fornece um filtro para decodificar o teletexto padrão do mundo (WST).</span><span class="sxs-lookup"><span data-stu-id="b8e45-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="b8e45-107">O decodificador de WST é um filtro de modo kernel que aceita dados de teletextos padrão do mundo decodificados do [codec de WST](wst-codec-filter.md) e entrega os bitmaps para o pino 2 no [mixer de sobreposição](overlay-mixer-filter.md) usando fontes fornecidas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="b8e45-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="b8e45-108">Somente os idiomas da Europa Ocidental têm suporte no momento; no momento, não há fontes Unicode fornecidas.</span><span class="sxs-lookup"><span data-stu-id="b8e45-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="b8e45-109">Esse filtro pode ser adicionado ao grafo automaticamente chamando [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), usando o pino de saída do codec de WST.</span><span class="sxs-lookup"><span data-stu-id="b8e45-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



| <span data-ttu-id="b8e45-110">Label</span><span class="sxs-lookup"><span data-stu-id="b8e45-110">Label</span></span> | <span data-ttu-id="b8e45-111">Valor</span><span class="sxs-lookup"><span data-stu-id="b8e45-111">Value</span></span> |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="b8e45-112">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="b8e45-112">Filter Interfaces</span></span>                        | <span data-ttu-id="b8e45-113">ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="b8e45-113">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="b8e45-114">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="b8e45-114">Input Pin Media Types</span></span>                    | <span data-ttu-id="b8e45-115">MEDIATYPE \_ VBI, \_ TELEtext MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b8e45-115">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="b8e45-116">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="b8e45-116">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="b8e45-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="b8e45-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="b8e45-118">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="b8e45-118">Output Pin Media Types</span></span>                   | <span data-ttu-id="b8e45-119">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="b8e45-119">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="b8e45-120">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="b8e45-120">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="b8e45-121">**IPin**</span><span class="sxs-lookup"><span data-stu-id="b8e45-121">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="b8e45-122">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="b8e45-122">Filter CLSID</span></span>                             | <span data-ttu-id="b8e45-123">\_WSTDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="b8e45-123">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="b8e45-124">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="b8e45-124">Property Page CLSID</span></span>                      | <span data-ttu-id="b8e45-125">\_WSTDECODERPROPERTYPAGE CLSID</span><span class="sxs-lookup"><span data-stu-id="b8e45-125">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="b8e45-126">Executável</span><span class="sxs-lookup"><span data-stu-id="b8e45-126">Executable</span></span>                               | <span data-ttu-id="b8e45-127">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="b8e45-127">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="b8e45-128">Núcleo</span><span class="sxs-lookup"><span data-stu-id="b8e45-128">Merit</span></span>](merit.md)                       | <span data-ttu-id="b8e45-129">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="b8e45-129">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="b8e45-130">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="b8e45-130">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="b8e45-131">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="b8e45-131">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="b8e45-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b8e45-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b8e45-133">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="b8e45-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="b8e45-134">Exibindo teletexto do mundo Standard</span><span class="sxs-lookup"><span data-stu-id="b8e45-134">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



