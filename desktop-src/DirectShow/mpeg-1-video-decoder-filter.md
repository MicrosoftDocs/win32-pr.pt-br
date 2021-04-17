---
description: Filtro de decodificador de vídeo MPEG-1
ms.assetid: 272d2f31-6e57-4ce5-ac86-b4d47f661fea
title: Filtro de decodificador de vídeo MPEG-1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ec7f48e441226dee33ef949219e8008e15c9d711
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105780141"
---
# <a name="mpeg-1-video-decoder-filter"></a><span data-ttu-id="03ef9-103">Filtro de decodificador de vídeo MPEG-1</span><span class="sxs-lookup"><span data-stu-id="03ef9-103">MPEG-1 Video Decoder Filter</span></span>

<span data-ttu-id="03ef9-104">Decodifica vídeo MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="03ef9-104">Decodes MPEG-1 video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="03ef9-105">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="03ef9-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="03ef9-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ef9-107">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="03ef9-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="03ef9-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span><span class="sxs-lookup"><span data-stu-id="03ef9-108">MEDIATYPE_Video, FORMAT_MPEGVideo</span></span><br/> <span data-ttu-id="03ef9-109">Os seguintes subtipos são válidos:</span><span class="sxs-lookup"><span data-stu-id="03ef9-109">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="03ef9-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-110"><strong>MEDIASUBTYPE_MPEG1Packet</strong></span></span></li>
<li><span data-ttu-id="03ef9-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-111"><strong>MEDIASUBTYPE_MPEG1Payload</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ef9-112">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="03ef9-112">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="03ef9-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"> <strong>IMemInputPin</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ef9-113"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ef9-114">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="03ef9-114">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="03ef9-115">Tipo principal: <strong>MEDIATYPE_Video</strong>,</span><span class="sxs-lookup"><span data-stu-id="03ef9-115">Major type: <strong>MEDIATYPE_Video</strong>,</span></span><br/> <span data-ttu-id="03ef9-116">Tipo de formato: <strong>FORMAT_VideoInfo</strong> ou <strong>FORMAT_VideoInfo2</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-116">Format type: <strong>FORMAT_VideoInfo</strong> or <strong>FORMAT_VideoInfo2</strong></span></span><br/> <span data-ttu-id="03ef9-117">Subtipos</span><span class="sxs-lookup"><span data-stu-id="03ef9-117">Subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="03ef9-118"><strong>MEDIASUBTYPE_RGB24</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-118"><strong>MEDIASUBTYPE_RGB24</strong></span></span></li>
<li><span data-ttu-id="03ef9-119"><strong>MEDIASUBTYPE_RGB32</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-119"><strong>MEDIASUBTYPE_RGB32</strong></span></span></li>
<li><span data-ttu-id="03ef9-120"><strong>MEDIASUBTYPE_RGB8</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-120"><strong>MEDIASUBTYPE_RGB8</strong></span></span></li>
<li><span data-ttu-id="03ef9-121"><strong>MEDIASUBTYPE_RGB555</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-121"><strong>MEDIASUBTYPE_RGB555</strong></span></span></li>
<li><span data-ttu-id="03ef9-122"><strong>MEDIASUBTYPE_RGB565</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-122"><strong>MEDIASUBTYPE_RGB565</strong></span></span></li>
<li><span data-ttu-id="03ef9-123"><strong>MEDIASUBTYPE_UYVY</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-123"><strong>MEDIASUBTYPE_UYVY</strong></span></span></li>
<li><span data-ttu-id="03ef9-124"><strong>MEDIASUBTYPE_Y41P</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-124"><strong>MEDIASUBTYPE_Y41P</strong></span></span></li>
<li><span data-ttu-id="03ef9-125"><strong>MEDIASUBTYPE_YUY2</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-125"><strong>MEDIASUBTYPE_YUY2</strong></span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ef9-126">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="03ef9-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="03ef9-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"> <strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="03ef9-127"><a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ef9-128">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="03ef9-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="03ef9-129"><strong>CLSID_CMpegVideoCodec</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-129"><strong>CLSID_CMpegVideoCodec</strong></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ef9-130">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="03ef9-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="03ef9-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span><span class="sxs-lookup"><span data-stu-id="03ef9-131"><strong>CLSID_MpegVideoDecodePropertyPage</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ef9-132">Executável</span><span class="sxs-lookup"><span data-stu-id="03ef9-132">Executable</span></span></td>
<td><span data-ttu-id="03ef9-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="03ef9-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="03ef9-134"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="03ef9-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="03ef9-135">0x40000001</span><span class="sxs-lookup"><span data-stu-id="03ef9-135">0x40000001</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03ef9-136"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="03ef9-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="03ef9-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="03ef9-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="03ef9-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="03ef9-138">Remarks</span></span>

<span data-ttu-id="03ef9-139">Esse filtro pode decodificar em uma superfície do DirectDraw.</span><span class="sxs-lookup"><span data-stu-id="03ef9-139">This filter can decode into a DirectDraw Surface.</span></span> <span data-ttu-id="03ef9-140">O filtro usará a tecnologia MMX se o computador oferecer suporte à tecnologia MMX.</span><span class="sxs-lookup"><span data-stu-id="03ef9-140">The filter uses MMX if the machine supports MMX.</span></span>

## <a name="related-topics"></a><span data-ttu-id="03ef9-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="03ef9-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="03ef9-142">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="03ef9-142">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




