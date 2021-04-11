---
description: Filtro do analisador de filmes QuickTime
ms.assetid: 9537dd7b-9aeb-4e73-a31d-86053874ef13
title: Filtro do analisador de filmes QuickTime
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a046e143487a1455aeeb125910bbf4452b4f947
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104296039"
---
# <a name="quicktime-movie-parser-filter"></a><span data-ttu-id="bf7d3-103">Filtro do analisador de filmes QuickTime</span><span class="sxs-lookup"><span data-stu-id="bf7d3-103">QuickTime Movie Parser Filter</span></span>

<span data-ttu-id="bf7d3-104">Este componente foi removido do Windows Vista e de sistemas operacionais posteriores.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-104">This component has been removed from Windows Vista and later operating systems.</span></span> <span data-ttu-id="bf7d3-105">Ele está disponível para uso nos sistemas operacionais Microsoft Windows 2000, Windows XP e Windows Server 2003.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-105">It is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span>

<span data-ttu-id="bf7d3-106">O filtro QuickTime Movie Parser divide os dados do Apple® QuickTime® em fluxos de áudio e vídeo.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-106">The QuickTime Movie Parser filter splits Apple® QuickTime® data into audio and video streams.</span></span> <span data-ttu-id="bf7d3-107">Ele dá suporte ao QuickTime 2,0 e anterior.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-107">It supports QuickTime 2.0 and earlier.</span></span> <span data-ttu-id="bf7d3-108">O PIN de entrada se conecta a um filtro de origem, como o filtro de [origem de arquivo assíncrono](file-source--async--filter.md) ou o filtro de [origem de arquivo de URL](file-source--url--filter.md) .</span><span class="sxs-lookup"><span data-stu-id="bf7d3-108">The input pin connects to a source filter such as the [Async File Source](file-source--async--filter.md) filter or the [URL File Source](file-source--url--filter.md) filter.</span></span> <span data-ttu-id="bf7d3-109">O analisador usa o filtro [AVI descompactador](avi-decompressor-filter.md) ou [Qt descompactador](qt-decompressor-filter.md) para descompactar arquivos QuickTime.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-109">The Parser uses the [AVI Decompressor](avi-decompressor-filter.md) or [QT Decompressor](qt-decompressor-filter.md) filter to decompress QuickTime files.</span></span> <span data-ttu-id="bf7d3-110">O filtro cria um pino de saída para o fluxo de vídeo e um PIN de saída para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-110">The filter creates one output pin for the video stream and one output pin for the audio stream.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="bf7d3-111">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="bf7d3-111">Filter Interfaces</span></span></td>
<td><span data-ttu-id="bf7d3-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"> <strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf7d3-112"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf7d3-113">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="bf7d3-113">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="bf7d3-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span><span class="sxs-lookup"><span data-stu-id="bf7d3-114">MEDIATYPE_Stream, MEDIASUBTYPE_QTMovie;</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf7d3-115">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="bf7d3-115">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="bf7d3-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf7d3-116"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf7d3-117">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="bf7d3-117">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="bf7d3-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="bf7d3-118">MEDIATYPE_Video, MEDIASUBTYPE_NULL, FORMAT_VideoInfo</span></span></li>
<li><span data-ttu-id="bf7d3-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="bf7d3-119">MEDIATYPE_Audio, MEDIASUBTYPE_NULL, FORMAT_WaveFormatEx</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf7d3-120">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="bf7d3-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="bf7d3-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="bf7d3-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf7d3-122">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="bf7d3-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="bf7d3-123">CLSID_QuickTimeParser</span><span class="sxs-lookup"><span data-stu-id="bf7d3-123">CLSID_QuickTimeParser</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf7d3-124">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="bf7d3-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="bf7d3-125">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="bf7d3-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf7d3-126">Executável</span><span class="sxs-lookup"><span data-stu-id="bf7d3-126">Executable</span></span></td>
<td><span data-ttu-id="bf7d3-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="bf7d3-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="bf7d3-128"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="bf7d3-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="bf7d3-129">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="bf7d3-129">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="bf7d3-130"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="bf7d3-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="bf7d3-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="bf7d3-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="bf7d3-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="bf7d3-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bf7d3-133">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="bf7d3-133">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 



