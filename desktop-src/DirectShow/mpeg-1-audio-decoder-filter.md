---
description: Filtro de decodificador de áudio MPEG-1
ms.assetid: 2f695ac6-7d4b-41a8-b4c5-83fb9d20ab9d
title: Filtro de decodificador de áudio MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0f2c68243544a8c6a77cbd8101c85d68f393c3d
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105787137"
---
# <a name="mpeg-1-audio-decoder-filter"></a><span data-ttu-id="85a1a-103">Filtro de decodificador de áudio MPEG-1</span><span class="sxs-lookup"><span data-stu-id="85a1a-103">MPEG-1 Audio Decoder Filter</span></span>

<span data-ttu-id="85a1a-104">Decodifica o áudio de camada I e camada II MPEG-1 para PCM.</span><span class="sxs-lookup"><span data-stu-id="85a1a-104">Decodes MPEG-1 Layer I and Layer II audio to PCM.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="85a1a-105">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="85a1a-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="85a1a-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="85a1a-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85a1a-107">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="85a1a-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="85a1a-108">MEDIATYPE_Audio, FORMAT_WaveFormatEx</span><span class="sxs-lookup"><span data-stu-id="85a1a-108">MEDIATYPE_Audio, FORMAT_WaveFormatEx</span></span><br/> <span data-ttu-id="85a1a-109">Os seguintes subtipos são válidos:</span><span class="sxs-lookup"><span data-stu-id="85a1a-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="85a1a-110">MEDIASUBTYPE_MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="85a1a-110">MEDIASUBTYPE_MPEG1Packet</span></span></li>
<li><span data-ttu-id="85a1a-111">MEDIASUBTYPE_MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="85a1a-111">MEDIASUBTYPE_MPEG1Payload</span></span></li>
<li><span data-ttu-id="85a1a-112">MEDIASUBTYPE_MPEG1AudioPayload</span><span class="sxs-lookup"><span data-stu-id="85a1a-112">MEDIASUBTYPE_MPEG1AudioPayload</span></span></li>
<li><span data-ttu-id="85a1a-113">GUID_NULL</span><span class="sxs-lookup"><span data-stu-id="85a1a-113">GUID_NULL</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85a1a-114">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="85a1a-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="85a1a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="85a1a-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85a1a-116">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="85a1a-116">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="85a1a-117">MEDIATYPE_Audio, MEDIASUBTYPE_PCM</span><span class="sxs-lookup"><span data-stu-id="85a1a-117">MEDIATYPE_Audio, MEDIASUBTYPE_PCM</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85a1a-118">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="85a1a-118">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="85a1a-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="85a1a-119"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85a1a-120">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="85a1a-120">Filter CLSID</span></span></td>
<td><span data-ttu-id="85a1a-121">CLSID_CMpegAudioCodec</span><span class="sxs-lookup"><span data-stu-id="85a1a-121">CLSID_CMpegAudioCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85a1a-122">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="85a1a-122">Property Page CLSID</span></span></td>
<td><span data-ttu-id="85a1a-123">CLSID_MpegAudioDecoderPropertyPage</span><span class="sxs-lookup"><span data-stu-id="85a1a-123">CLSID_MpegAudioDecoderPropertyPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85a1a-124">Executável</span><span class="sxs-lookup"><span data-stu-id="85a1a-124">Executable</span></span></td>
<td><span data-ttu-id="85a1a-125">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="85a1a-125">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="85a1a-126"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="85a1a-126"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="85a1a-127">0x03680001</span><span class="sxs-lookup"><span data-stu-id="85a1a-127">0x03680001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="85a1a-128"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="85a1a-128"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="85a1a-129">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="85a1a-129">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="85a1a-130">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="85a1a-130">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="85a1a-131">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="85a1a-131">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




