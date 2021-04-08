---
description: Filtro de codificador de vídeo DV
ms.assetid: ac57bd11-de16-4a58-9f4b-da270a57ad08
title: Filtro de codificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73b91da15fda0597e9b943c78fd5a6716021a3ae
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103919743"
---
# <a name="dv-video-encoder-filter"></a><span data-ttu-id="427d3-103">Filtro de codificador de vídeo DV</span><span class="sxs-lookup"><span data-stu-id="427d3-103">DV Video Encoder Filter</span></span>

<span data-ttu-id="427d3-104">Esse filtro codifica um fluxo de vídeo descompactado em vídeo digital (DV).</span><span class="sxs-lookup"><span data-stu-id="427d3-104">This filter encodes an uncompressed video stream into digital video (DV).</span></span> <span data-ttu-id="427d3-105">Ele fornece uma interface personalizada, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), para definir a resolução e o formato da codificação.</span><span class="sxs-lookup"><span data-stu-id="427d3-105">It provides a custom interface, [**IDVEnc**](/windows/desktop/api/Strmif/nn-strmif-idvenc), for setting the encoding resolution and format.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="427d3-106">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="427d3-106">Filter Interfaces</span></span></td>
<td><span data-ttu-id="427d3-107"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="427d3-107"><a href="/windows/desktop/api/Strmif/nn-strmif-iamvideocompression"><strong>IAMVideoCompression</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvenc"><strong>IDVEnc</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="427d3-108">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="427d3-108">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="427d3-109">Tipo principal: MEDIATYPE_VideoThe seguintes subtipos são válidos:</span><span class="sxs-lookup"><span data-stu-id="427d3-109">Major type: MEDIATYPE_VideoThe following subtypes are valid:</span></span><br/>
<ul>
<li><span data-ttu-id="427d3-110">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="427d3-110">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="427d3-111">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="427d3-111">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="427d3-112">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="427d3-112">MEDIASUBTYPE_RGB555</span></span></li>
</ul></li>
<li><span data-ttu-id="427d3-113">Tipo de formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="427d3-113">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="427d3-114">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="427d3-114">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="427d3-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="427d3-115"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="427d3-116">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="427d3-116">Output Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="427d3-117">Tipo principal: MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="427d3-117">Major type: MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="427d3-118">Subtipo: MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="427d3-118">Subtype: MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="427d3-119">Tipo de formato: FORMAT_VideoInfo</span><span class="sxs-lookup"><span data-stu-id="427d3-119">Format type: FORMAT_VideoInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="427d3-120">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="427d3-120">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="427d3-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="427d3-121"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="427d3-122">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="427d3-122">Filter CLSID</span></span></td>
<td><span data-ttu-id="427d3-123">CLSID_DVVideoEnc</span><span class="sxs-lookup"><span data-stu-id="427d3-123">CLSID_DVVideoEnc</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="427d3-124">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="427d3-124">Property Page CLSID</span></span></td>
<td><span data-ttu-id="427d3-125">CLSID_DVEncPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="427d3-125">CLSID_DVEncPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="427d3-126">Executável</span><span class="sxs-lookup"><span data-stu-id="427d3-126">Executable</span></span></td>
<td><span data-ttu-id="427d3-127">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="427d3-127">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="427d3-128"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="427d3-128"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="427d3-129">MERIT_DO_NOT_USE</span><span class="sxs-lookup"><span data-stu-id="427d3-129">MERIT_DO_NOT_USE</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="427d3-130"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="427d3-130"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="427d3-131">CLSID_VideoCompressorCategory</span><span class="sxs-lookup"><span data-stu-id="427d3-131">CLSID_VideoCompressorCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="427d3-132">Comentários</span><span class="sxs-lookup"><span data-stu-id="427d3-132">Remarks</span></span>

<span data-ttu-id="427d3-133">Para vídeo de 16 bits (MEDIASUBTYPE \_ RGB555 ou MEDIASUBTYPE \_ RGB565), a entrada deve ter 720 x 480 pixels para NTSC ou 720 x 576 pixels para PAL.</span><span class="sxs-lookup"><span data-stu-id="427d3-133">For 16-bit video (MEDIASUBTYPE\_RGB555 or MEDIASUBTYPE\_RGB565), the input must be 720 x 480 pixels for NTSC, or 720 x 576 pixels for PAL.</span></span> <span data-ttu-id="427d3-134">Para vídeo de 24 bits, não há restrições de tamanho na entrada.</span><span class="sxs-lookup"><span data-stu-id="427d3-134">For 24-bit video, there are no size constraints on the input.</span></span>

<span data-ttu-id="427d3-135">A saída é sempre 720 x 480 para NTSC ou 720 x 576 para PAL; o vídeo de 24 bits é dimensionado para se ajustar a essas dimensões.</span><span class="sxs-lookup"><span data-stu-id="427d3-135">The output is always 720 x 480 for NTSC or 720 x 576 for PAL; 24-bit video is scaled to fit these dimensions.</span></span>

## <a name="related-topics"></a><span data-ttu-id="427d3-136">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="427d3-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="427d3-137">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="427d3-137">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="427d3-138">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="427d3-138">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




