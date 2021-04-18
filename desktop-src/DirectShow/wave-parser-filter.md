---
description: Filtro do analisador de som WAVE
ms.assetid: 53a9538d-7a79-40bb-9468-d710eb238925
title: Filtro do analisador de som WAVE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bb30465a25ab3a6eef190b5fbecd4a4878c2744
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105753304"
---
# <a name="wave-parser-filter"></a><span data-ttu-id="e7cdb-103">Filtro do analisador de som WAVE</span><span class="sxs-lookup"><span data-stu-id="e7cdb-103">WAVE Parser Filter</span></span>

<span data-ttu-id="e7cdb-104">O filtro WAVE Parser analisa dados de áudio de formato WAV de arquivos. wav,. au ou. aif.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-104">The WAVE Parser filter parses WAV-format audio data from .wav, .au, or .aif files.</span></span> <span data-ttu-id="e7cdb-105">O filtro upstream deve ser o filtro de [origem de arquivo assíncrono](file-source--async--filter.md) , o filtro de [origem de arquivo de URL](file-source--url--filter.md) ou um filtro de origem assíncrono de terceiros compatível que contenha dados de áudio WAV.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-105">The upstream filter must be the [Async File Source](file-source--async--filter.md) filter, [URL File Source](file-source--url--filter.md) filter, or a compatible third-party asynchronous source filter that contains WAV audio data.</span></span> <span data-ttu-id="e7cdb-106">O fluxo de saída são dados de áudio, que você pode conectar diretamente a um filtro de renderização de áudio ou a um filtro de transformação de áudio intermediário.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-106">The output stream is audio data, which you can connect directly to an audio rendering filter or to an intervening audio transform filter.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e7cdb-107">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="e7cdb-107">Filter Interfaces</span></span></td>
<td><span data-ttu-id="e7cdb-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span><span class="sxs-lookup"><span data-stu-id="e7cdb-108"><a href="/previous-versions/windows/desktop/api/Qnetwork/nn-qnetwork-iammediacontent"><strong>IAMMediaContent</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipersistmediapropertybag"><strong>IPersistMediaPropertyBag</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7cdb-109">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="e7cdb-109">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="e7cdb-110">Tipo principal: MEDIATYPE_StreamThe seguintes subtipos são válidos:</span><span class="sxs-lookup"><span data-stu-id="e7cdb-110">Major type: MEDIATYPE_StreamThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="e7cdb-111">MEDIASUBTYPE_AIFF</span><span class="sxs-lookup"><span data-stu-id="e7cdb-111">MEDIASUBTYPE_AIFF</span></span></li>
<li><span data-ttu-id="e7cdb-112">MEDIASUBTYPE_AU</span><span class="sxs-lookup"><span data-stu-id="e7cdb-112">MEDIASUBTYPE_AU</span></span></li>
<li><span data-ttu-id="e7cdb-113">MEDIASUBTYPE_WAVE</span><span class="sxs-lookup"><span data-stu-id="e7cdb-113">MEDIASUBTYPE_WAVE</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7cdb-114">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="e7cdb-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="e7cdb-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="e7cdb-115"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7cdb-116">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="e7cdb-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="e7cdb-117">Tipo principal: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM ou outro tipo de compactação.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-117">Major type: MEDIATYPE_AudioSubtype: MEDIASUBTYPE_PCM or other compression type.</span></span> <span data-ttu-id="e7cdb-118">(Consulte <a href="audio-subtypes.md"><strong>subtipos de áudio</strong></a>.)</span><span class="sxs-lookup"><span data-stu-id="e7cdb-118">(See <a href="audio-subtypes.md"><strong>Audio Subtypes</strong></a>.)</span></span><br/> <span data-ttu-id="e7cdb-119">Tipo de formato: FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="e7cdb-119">Format type: FORMAT_WaveFormatEx</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7cdb-120">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="e7cdb-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="e7cdb-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"> <strong>IMediaSeeking</strong></a></span><span class="sxs-lookup"><span data-stu-id="e7cdb-121"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7cdb-122">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="e7cdb-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="e7cdb-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span><span class="sxs-lookup"><span data-stu-id="e7cdb-123">{D51BD5A1-7548-11cf-A520-0080C77EF58A}</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7cdb-124">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="e7cdb-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="e7cdb-125">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-125">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7cdb-126">Executável</span><span class="sxs-lookup"><span data-stu-id="e7cdb-126">Executable</span></span></td>
<td><span data-ttu-id="e7cdb-127">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="e7cdb-127">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e7cdb-128"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="e7cdb-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="e7cdb-129">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="e7cdb-129">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e7cdb-130"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="e7cdb-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="e7cdb-131">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="e7cdb-131">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="e7cdb-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="e7cdb-132">Remarks</span></span>

<span data-ttu-id="e7cdb-133">Este filtro dá suporte aos seguintes tipos de arquivo:</span><span class="sxs-lookup"><span data-stu-id="e7cdb-133">This filter supports the following file types:</span></span>

-   <span data-ttu-id="e7cdb-134">ONDA (. wav)</span><span class="sxs-lookup"><span data-stu-id="e7cdb-134">WAVE (.wav)</span></span>
-   <span data-ttu-id="e7cdb-135">AIFF e AIFF-C (. aif)</span><span class="sxs-lookup"><span data-stu-id="e7cdb-135">AIFF and AIFF-C (.aif)</span></span>
-   <span data-ttu-id="e7cdb-136">AU (. au)</span><span class="sxs-lookup"><span data-stu-id="e7cdb-136">AU (.au)</span></span>

<span data-ttu-id="e7cdb-137">No entanto, ele tem as seguintes limitações no formato de áudio:</span><span class="sxs-lookup"><span data-stu-id="e7cdb-137">However, it has the following limitations on the audio format:</span></span>

-   <span data-ttu-id="e7cdb-138">O áudio deve ser um PCM linear de 8 bits ou 16 bits.</span><span class="sxs-lookup"><span data-stu-id="e7cdb-138">The audio must be 8-bit or 16-bit linear PCM.</span></span>
-   <span data-ttu-id="e7cdb-139">Para arquivos AIFF-C, o áudio deve ser descompactado, em ordem de byte big endian (tipo de compactação ' NONE ').</span><span class="sxs-lookup"><span data-stu-id="e7cdb-139">For AIFF-C files, the audio must be uncompressed, in big-endian byte order (compression type 'NONE').</span></span>

## <a name="related-topics"></a><span data-ttu-id="e7cdb-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e7cdb-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e7cdb-141">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="e7cdb-141">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




