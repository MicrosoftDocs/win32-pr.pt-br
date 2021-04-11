---
description: Divisor MPEG-2
ms.assetid: 06704a5a-e7ae-4187-ae36-32512d951aaf
title: Divisor MPEG-2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f04062660df7711a573dd17deb82f90897454a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104163836"
---
# <a name="mpeg-2-splitter"></a><span data-ttu-id="5a8da-103">Divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5a8da-103">MPEG-2 Splitter</span></span>

<span data-ttu-id="5a8da-104">A partir do Microsoft® Windows® XP, o filtro de divisão MPEG-2 é preterido.</span><span class="sxs-lookup"><span data-stu-id="5a8da-104">Starting in Microsoft® Windows® XP, the MPEG-2 Splitter filter is deprecated.</span></span> <span data-ttu-id="5a8da-105">Em vez disso, use o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md) .</span><span class="sxs-lookup"><span data-stu-id="5a8da-105">Use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md) instead.</span></span>

<span data-ttu-id="5a8da-106">Em plataformas anteriores, use o divisor MPEG-2 para fluxos de programa MPEG-2 entregues no modo de pull que contém pelo menos um dos seguintes tipos de fluxo: vídeo MPEG-2; Áudio MPEG-2; Áudio AC3 codificado conforme definido para vídeo em DVD; ou áudio PCM codificado como definido para vídeo de DVD.</span><span class="sxs-lookup"><span data-stu-id="5a8da-106">On earlier platforms, use the MPEG-2 Splitter for MPEG-2 program streams delivered in pull mode that contain at least one of the following stream types: MPEG-2 video; MPEG-2 audio; AC3 audio encoded as defined for DVD video; or PCM audio encoded as defined for DVD video.</span></span> <span data-ttu-id="5a8da-107">Esse filtro analisa os fluxos, cria um pino de saída para cada fluxo e gera os pacotes de áudio ou vídeo MPEG compactados em um filtro de decodificador MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="5a8da-107">This filter parses the streams, creates an output pin for each stream, and outputs the compressed MPEG audio or video packets to an MPEG-2 decoder filter.</span></span>

<span data-ttu-id="5a8da-108">Para fluxos de programas e transporte entregues no modo Push, use o [demultiplexador MPEG-2](mpeg-2-demultiplexer.md)em todas as plataformas.</span><span class="sxs-lookup"><span data-stu-id="5a8da-108">For program and transport streams delivered in push-mode, use the [MPEG-2 Demultiplexer](mpeg-2-demultiplexer.md), on all platforms.</span></span>

> [!Note]  
> <span data-ttu-id="5a8da-109">O divisor MPEG-2 não dá suporte à busca com precisão de quadro.</span><span class="sxs-lookup"><span data-stu-id="5a8da-109">The MPEG-2 Splitter does not support frame-accurate seeking.</span></span>

 



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="5a8da-110">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="5a8da-110">Filter Interfaces</span></span></td>
<td><span data-ttu-id="5a8da-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a8da-111"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong>, <a href="/previous-versions/windows/desktop/api/Amparse/nn-amparse-iamparse"><strong>IAMParse</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iamstreamselect"><strong>IAMStreamSelect</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a8da-112">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="5a8da-112">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="5a8da-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span><span class="sxs-lookup"><span data-stu-id="5a8da-113">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG2_PROGRAM</span></span></li>
<li><span data-ttu-id="5a8da-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span><span class="sxs-lookup"><span data-stu-id="5a8da-114">MEDIATYPE_Stream, MEDIASUBTYPE_MPEG1_Video</span></span></li>
<li><span data-ttu-id="5a8da-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="5a8da-115">MEDIATYPE_Stream, MEDIASUBTYPE_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a8da-116">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="5a8da-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="5a8da-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a8da-117"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a8da-118">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="5a8da-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="5a8da-119">Depende do tipo de fluxo.</span><span class="sxs-lookup"><span data-stu-id="5a8da-119">Depends on the stream type.</span></span> <span data-ttu-id="5a8da-120">Consulte <a href="mpeg-2-splitter-media-types.md">tipos de mídia de divisor MPEG-2</a></span><span class="sxs-lookup"><span data-stu-id="5a8da-120">See <a href="mpeg-2-splitter-media-types.md">MPEG-2 Splitter Media Types</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a8da-121">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="5a8da-121">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="5a8da-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="5a8da-122"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a8da-123">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="5a8da-123">Filter CLSID</span></span></td>
<td><span data-ttu-id="5a8da-124">CLSID_MMSPLITTER</span><span class="sxs-lookup"><span data-stu-id="5a8da-124">CLSID_MMSPLITTER</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a8da-125">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="5a8da-125">Property Page CLSID</span></span></td>
<td><span data-ttu-id="5a8da-126">Não aplicável</span><span class="sxs-lookup"><span data-stu-id="5a8da-126">Not applicable</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a8da-127">Executável</span><span class="sxs-lookup"><span data-stu-id="5a8da-127">Executable</span></span></td>
<td><span data-ttu-id="5a8da-128">mpg2splt.ax</span><span class="sxs-lookup"><span data-stu-id="5a8da-128">mpg2splt.ax</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="5a8da-129"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="5a8da-129"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="5a8da-130">MERIT_NORMAL + 1</span><span class="sxs-lookup"><span data-stu-id="5a8da-130">MERIT_NORMAL + 1</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="5a8da-131"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="5a8da-131"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="5a8da-132">CLSID_AudioInputDeviceCategory</span><span class="sxs-lookup"><span data-stu-id="5a8da-132">CLSID_AudioInputDeviceCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="5a8da-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="5a8da-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5a8da-134">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="5a8da-134">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="5a8da-135">Usando o divisor MPEG-2</span><span class="sxs-lookup"><span data-stu-id="5a8da-135">Using the MPEG-2 Splitter</span></span>](using-the-mpeg-2-splitter.md)
</dt> </dl>

 

 



