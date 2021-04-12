---
description: Filtro de conversor de espaço de cor
ms.assetid: a6765184-43ce-47b8-9eb1-e15af7e11c93
title: Filtro de conversor de espaço de cor
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f054ee03dd65cf619a697d4441b4d09279e7b912
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104456490"
---
# <a name="color-space-converter-filter"></a><span data-ttu-id="7cdcc-103">Filtro de conversor de espaço de cor</span><span class="sxs-lookup"><span data-stu-id="7cdcc-103">Color Space Converter Filter</span></span>

<span data-ttu-id="7cdcc-104">Esse filtro de transformação converte de um tipo de cor RGB em outro tipo RGB, como entre cores RGB de 24 e 8 bits.</span><span class="sxs-lookup"><span data-stu-id="7cdcc-104">This transform filter converts from one RGB color type to another RGB type, such as between 24-bit and 8-bit RGB color.</span></span> <span data-ttu-id="7cdcc-105">Como esse tipo de conversão geralmente é tratado com mais eficiência em um descompactador de vídeo, o uso principal do conversor de espaço de cor é quando a origem do fluxo consiste em quadros RGB não compactados.</span><span class="sxs-lookup"><span data-stu-id="7cdcc-105">Since this type of conversion is generally handled more efficiently within a video decompressor, the main use of the Color Space Converter is when the stream source consists of uncompressed RGB frames.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7cdcc-106">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="7cdcc-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="7cdcc-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cdcc-107"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cdcc-108">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="7cdcc-108">Input Pin Media Types</span></span></td>
<td><span data-ttu-id="7cdcc-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="7cdcc-109">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="7cdcc-110">Os seguintes subtipos são válidos:</span><span class="sxs-lookup"><span data-stu-id="7cdcc-110">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="7cdcc-111">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="7cdcc-111">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="7cdcc-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="7cdcc-112">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="7cdcc-113">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="7cdcc-113">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="7cdcc-114">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="7cdcc-114">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="7cdcc-115">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="7cdcc-115">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cdcc-116">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="7cdcc-116">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="7cdcc-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cdcc-117"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cdcc-118">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="7cdcc-118">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="7cdcc-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span><span class="sxs-lookup"><span data-stu-id="7cdcc-119">MEDIATYPE_Video, FORMAT_VideoInfo.</span></span><br/> <span data-ttu-id="7cdcc-120">Os seguintes subtipos são válidos:</span><span class="sxs-lookup"><span data-stu-id="7cdcc-120">The following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="7cdcc-121">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="7cdcc-121">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="7cdcc-122">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="7cdcc-122">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="7cdcc-123">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="7cdcc-123">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="7cdcc-124">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="7cdcc-124">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="7cdcc-125">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="7cdcc-125">MEDIASUBTYPE_RGB32</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cdcc-126">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="7cdcc-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="7cdcc-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="7cdcc-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cdcc-128">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="7cdcc-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="7cdcc-129">CLSID_Colour</span><span class="sxs-lookup"><span data-stu-id="7cdcc-129">CLSID_Colour</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cdcc-130">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="7cdcc-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="7cdcc-131">Nenhuma página de propriedades.</span><span class="sxs-lookup"><span data-stu-id="7cdcc-131">No property page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cdcc-132">Executável</span><span class="sxs-lookup"><span data-stu-id="7cdcc-132">Executable</span></span></td>
<td><span data-ttu-id="7cdcc-133">quartz.dll</span><span class="sxs-lookup"><span data-stu-id="7cdcc-133">quartz.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7cdcc-134"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="7cdcc-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="7cdcc-135">MERIT_UNLIKELY</span><span class="sxs-lookup"><span data-stu-id="7cdcc-135">MERIT_UNLIKELY</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7cdcc-136"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="7cdcc-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="7cdcc-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="7cdcc-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="7cdcc-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7cdcc-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7cdcc-139">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="7cdcc-139">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 




