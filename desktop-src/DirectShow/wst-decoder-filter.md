---
description: Filtro de decodificador de WST
ms.assetid: 2d33ae3f-565d-4e69-8fb0-117ff582a4d0
title: Filtro de decodificador de WST
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 01f2d20873ff9a5e7c009c4a84f7a23c273d6590
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827521"
---
# <a name="wst-decoder-filter"></a><span data-ttu-id="c6df1-103">Filtro de decodificador de WST</span><span class="sxs-lookup"><span data-stu-id="c6df1-103">WST Decoder Filter</span></span>

<span data-ttu-id="c6df1-104">Este componente foi removido do Windows Vista e de sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="c6df1-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="c6df1-105">Ele está disponível para uso nos sistemas operacionais Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="c6df1-105">It is available for use in the Windows XP and Windows Server 2003 operating systems.</span></span>

> [!Note]  
> <span data-ttu-id="c6df1-106">A partir do Windows Vista, o DirectShow não fornece um filtro para decodificar o teletexto padrão do mundo (WST).</span><span class="sxs-lookup"><span data-stu-id="c6df1-106">Starting in Windows Vista, DirectShow does not provide a filter to decode World Standard Teletext (WST).</span></span>

 

<span data-ttu-id="c6df1-107">O decodificador de WST é um filtro de modo kernel que aceita dados de teletextos padrão do mundo decodificados do [codec de WST](wst-codec-filter.md) e entrega os bitmaps para o pino 2 no [mixer de sobreposição](overlay-mixer-filter.md) usando fontes fornecidas pela Microsoft.</span><span class="sxs-lookup"><span data-stu-id="c6df1-107">The WST Decoder is a kernel-mode filter that accepts decoded World Standard Teletext data from the [WST Codec](wst-codec-filter.md) and delivers the bitmaps to Pin 2 on the [Overlay Mixer](overlay-mixer-filter.md) using fonts supplied by Microsoft.</span></span> <span data-ttu-id="c6df1-108">Somente os idiomas da Europa Ocidental têm suporte no momento; no momento, não há fontes Unicode fornecidas.</span><span class="sxs-lookup"><span data-stu-id="c6df1-108">Only Western European languages are supported at this time; no Unicode fonts are currently provided.</span></span>

<span data-ttu-id="c6df1-109">Esse filtro pode ser adicionado ao grafo automaticamente chamando [**ICaptureGraphBuilder2:: RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), usando o pino de saída do codec de WST.</span><span class="sxs-lookup"><span data-stu-id="c6df1-109">This filter can be added to the graph automatically by calling [**ICaptureGraphBuilder2::RenderStream**](/windows/desktop/api/Strmif/nf-strmif-icapturegraphbuilder2-renderstream), using the output pin of the WST Codec.</span></span>



|                                          |                                                               |
|------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="c6df1-110">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="c6df1-110">Filter Interfaces</span></span>                        | <span data-ttu-id="c6df1-111">ISpecifyPropertyPages, [ **IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span><span class="sxs-lookup"><span data-stu-id="c6df1-111">ISpecifyPropertyPages, [**IAMWstDecoder**](/previous-versions/windows/desktop/api/Iwstdec/nn-iwstdec-iamwstdecoder)</span></span> |
| <span data-ttu-id="c6df1-112">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="c6df1-112">Input Pin Media Types</span></span>                    | <span data-ttu-id="c6df1-113">MEDIATYPE \_ VBI, \_ TELEtext MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="c6df1-113">MEDIATYPE\_VBI, MEDIASUBTYPE\_TELETEXT</span></span>                        |
| <span data-ttu-id="c6df1-114">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="c6df1-114">Input Pin Interfaces</span></span>                     | [<span data-ttu-id="c6df1-115">**IPin**</span><span class="sxs-lookup"><span data-stu-id="c6df1-115">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="c6df1-116">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="c6df1-116">Output Pin Media Types</span></span>                   | <span data-ttu-id="c6df1-117">Vídeo de MEDIATYPE \_</span><span class="sxs-lookup"><span data-stu-id="c6df1-117">MEDIATYPE\_Video</span></span>                                              |
| <span data-ttu-id="c6df1-118">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="c6df1-118">Output Pin Interfaces</span></span>                    | [<span data-ttu-id="c6df1-119">**IPin**</span><span class="sxs-lookup"><span data-stu-id="c6df1-119">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)                                          |
| <span data-ttu-id="c6df1-120">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="c6df1-120">Filter CLSID</span></span>                             | <span data-ttu-id="c6df1-121">\_WSTDECODER CLSID</span><span class="sxs-lookup"><span data-stu-id="c6df1-121">CLSID\_WSTDecoder</span></span>                                             |
| <span data-ttu-id="c6df1-122">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="c6df1-122">Property Page CLSID</span></span>                      | <span data-ttu-id="c6df1-123">\_WSTDECODERPROPERTYPAGE CLSID</span><span class="sxs-lookup"><span data-stu-id="c6df1-123">CLSID\_WstDecoderPropertyPage</span></span>                                 |
| <span data-ttu-id="c6df1-124">Executável</span><span class="sxs-lookup"><span data-stu-id="c6df1-124">Executable</span></span>                               | <span data-ttu-id="c6df1-125">Wstdecod.DLL</span><span class="sxs-lookup"><span data-stu-id="c6df1-125">Wstdecod.DLL</span></span>                                                  |
| [<span data-ttu-id="c6df1-126">Núcleo</span><span class="sxs-lookup"><span data-stu-id="c6df1-126">Merit</span></span>](merit.md)                       | <span data-ttu-id="c6df1-127">MÉRITO \_ normal</span><span class="sxs-lookup"><span data-stu-id="c6df1-127">MERIT\_NORMAL</span></span>                                                 |
| [<span data-ttu-id="c6df1-128">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="c6df1-128">Filter Category</span></span>](filter-categories.md) | <span data-ttu-id="c6df1-129">\_LEGACYAMFILTERCATEGORY CLSID</span><span class="sxs-lookup"><span data-stu-id="c6df1-129">CLSID\_LegacyAmFilterCategory</span></span>                                 |



 

## <a name="related-topics"></a><span data-ttu-id="c6df1-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="c6df1-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="c6df1-131">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="c6df1-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="c6df1-132">Exibindo teletexto do mundo Standard</span><span class="sxs-lookup"><span data-stu-id="c6df1-132">Viewing World Standard Teletext</span></span>](viewing-world-standard-teletext.md)
</dt> </dl>

 

 



