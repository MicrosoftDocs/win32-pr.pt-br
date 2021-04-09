---
description: Filtro de desenho AVI
ms.assetid: 86cd8e48-7cfa-46e4-b8f4-609b4d09fe80
title: Filtro de desenho AVI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0b6d6b318b7a1f7e762fc0806186114fb9256f5c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087326"
---
# <a name="avi-draw-filter"></a><span data-ttu-id="9dcfb-103">Filtro de desenho AVI</span><span class="sxs-lookup"><span data-stu-id="9dcfb-103">AVI Draw Filter</span></span>

<span data-ttu-id="9dcfb-104">O filtro de desenho AVI é puxado automaticamente para um grafo de reprodução em vez do [descompactador AVI](avi-decompressor-filter.md) quando o vídeo está sendo impresso em um monitor de televisão NTSC externo.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-104">The AVI Draw filter is pulled automatically into a playback graph instead of the [AVI Decompressor](avi-decompressor-filter.md) when video is being output to an external NTSC television monitor.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="9dcfb-105">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="9dcfb-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="9dcfb-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="9dcfb-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9dcfb-107">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="9dcfb-107">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="9dcfb-108">Tipo principal: MEDIATYPE_VideoSubtypes:</span><span class="sxs-lookup"><span data-stu-id="9dcfb-108">Major Type: MEDIATYPE_VideoSubtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="9dcfb-109">MEDIASUBTYPE_MJPG</span><span class="sxs-lookup"><span data-stu-id="9dcfb-109">MEDIASUBTYPE_MJPG</span></span></li>
<li><span data-ttu-id="9dcfb-110">MEDIASUBTYPE_TVMJ</span><span class="sxs-lookup"><span data-stu-id="9dcfb-110">MEDIASUBTYPE_TVMJ</span></span></li>
<li><span data-ttu-id="9dcfb-111">MEDIASUBTYPE_WAKE</span><span class="sxs-lookup"><span data-stu-id="9dcfb-111">MEDIASUBTYPE_WAKE</span></span></li>
<li><span data-ttu-id="9dcfb-112">MEDIASUBTYPE_CFCC</span><span class="sxs-lookup"><span data-stu-id="9dcfb-112">MEDIASUBTYPE_CFCC</span></span></li>
<li><span data-ttu-id="9dcfb-113">MEDIASUBTYPE_IJPG</span><span class="sxs-lookup"><span data-stu-id="9dcfb-113">MEDIASUBTYPE_IJPG</span></span></li>
<li><span data-ttu-id="9dcfb-114">MEDIASUBTYPE_Plum</span><span class="sxs-lookup"><span data-stu-id="9dcfb-114">MEDIASUBTYPE_Plum</span></span></li>
<li><span data-ttu-id="9dcfb-115">MEDIASUBTYPE_DVCS</span><span class="sxs-lookup"><span data-stu-id="9dcfb-115">MEDIASUBTYPE_DVCS</span></span></li>
<li><span data-ttu-id="9dcfb-116">MEDIASUBTYPE_DVSD</span><span class="sxs-lookup"><span data-stu-id="9dcfb-116">MEDIASUBTYPE_DVSD</span></span></li>
<li><span data-ttu-id="9dcfb-117">MEDIASUBTYPE_MDVF</span><span class="sxs-lookup"><span data-stu-id="9dcfb-117">MEDIASUBTYPE_MDVF</span></span></li>
<li><span data-ttu-id="9dcfb-118">Tipo de formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="9dcfb-118">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9dcfb-119">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="9dcfb-119">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="9dcfb-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="9dcfb-120"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9dcfb-121">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="9dcfb-121">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="9dcfb-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span><span class="sxs-lookup"><span data-stu-id="9dcfb-122">MEDIATYPE_Video, MEDIASUBTYPE_NULL</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9dcfb-123">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="9dcfb-123">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="9dcfb-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="9dcfb-124"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ioverlaynotify"><strong>IOverlayNotify</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9dcfb-125">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="9dcfb-125">Filter CLSID</span></span></td>
<td><span data-ttu-id="9dcfb-126">CLSID_AVIDraw</span><span class="sxs-lookup"><span data-stu-id="9dcfb-126">CLSID_AVIDraw</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9dcfb-127">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="9dcfb-127">Property Page CLSID</span></span></td>
<td><span data-ttu-id="9dcfb-128">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-128">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9dcfb-129">Executável</span><span class="sxs-lookup"><span data-stu-id="9dcfb-129">Executable</span></span></td>
<td><span data-ttu-id="9dcfb-130">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="9dcfb-130">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="9dcfb-131"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="9dcfb-131"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="9dcfb-132">MERIT_NORMAL + 100</span><span class="sxs-lookup"><span data-stu-id="9dcfb-132">MERIT_NORMAL + 100</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="9dcfb-133"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="9dcfb-133"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="9dcfb-134">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="9dcfb-134">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="9dcfb-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dcfb-135">Remarks</span></span>

<span data-ttu-id="9dcfb-136">Como o filtro de desenho do AVI e o [filtro de captura do VFW](vfw-capture-filter.md) se conectam ao mesmo hardware, eles não podem estar no mesmo grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="9dcfb-136">Since the AVI Draw filter and the [VFW Capture Filter](vfw-capture-filter.md) both connect to the same hardware, they cannot be in the same filter graph.</span></span>

## <a name="related-topics"></a><span data-ttu-id="9dcfb-137">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9dcfb-137">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9dcfb-138">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="9dcfb-138">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




