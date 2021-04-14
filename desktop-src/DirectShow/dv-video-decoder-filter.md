---
description: Filtro de decodificador de vídeo DV
ms.assetid: aa47010e-8510-475d-836a-cb63deeb3a7b
title: Filtro de decodificador de vídeo DV
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6baab43d4a369cb16d92974a0e6e469c914961bb
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104500153"
---
# <a name="dv-video-decoder-filter"></a><span data-ttu-id="a1506-103">Filtro de decodificador de vídeo DV</span><span class="sxs-lookup"><span data-stu-id="a1506-103">DV Video Decoder Filter</span></span>

<span data-ttu-id="a1506-104">Esse filtro decodifica um fluxo de vídeo digital (DV) em vídeo descompactado.</span><span class="sxs-lookup"><span data-stu-id="a1506-104">This filter decodes a digital video (DV) stream into uncompressed video.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a1506-105">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="a1506-105">Filter Interfaces</span></span></td>
<td><span data-ttu-id="a1506-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span><span class="sxs-lookup"><span data-stu-id="a1506-106"><a href="/windows/desktop/api/Strmif/nn-strmif-ibasefilter"><strong>IBaseFilter</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-idvrgb219"><strong>IDVRGB219</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iipdvdec"><strong>IIPDVDec</strong></a>, <strong>IPersistStream</strong>, <strong>ISpecifyPropertyPages</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1506-107">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a1506-107">Input Pin Media Types</span></span></td>
<td><ul>
<li><span data-ttu-id="a1506-108">MEDIATYPE_Video</span><span class="sxs-lookup"><span data-stu-id="a1506-108">MEDIATYPE_Video</span></span></li>
<li><span data-ttu-id="a1506-109">MEDIASUBTYPE_dvsd</span><span class="sxs-lookup"><span data-stu-id="a1506-109">MEDIASUBTYPE_dvsd</span></span></li>
<li><span data-ttu-id="a1506-110">FORMAT_VideoInfo, FORMAT_DvInfo</span><span class="sxs-lookup"><span data-stu-id="a1506-110">FORMAT_VideoInfo, FORMAT_DvInfo</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1506-111">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="a1506-111">Input Pin Interfaces</span></span></td>
<td><span data-ttu-id="a1506-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a1506-112"><a href="/windows/desktop/api/Strmif/nn-strmif-imeminputpin"><strong>IMemInputPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1506-113">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="a1506-113">Output Pin Media Types</span></span></td>
<td><span data-ttu-id="a1506-114"><strong>Tipo principal</strong>: MEDIATYPE_Video<strong>subtipos</strong>:</span><span class="sxs-lookup"><span data-stu-id="a1506-114"><strong>Major type</strong>: MEDIATYPE_Video<strong>Subtypes</strong>:</span></span><br/>
<ul>
<li><span data-ttu-id="a1506-115">MEDIASUBTYPE_YUY2</span><span class="sxs-lookup"><span data-stu-id="a1506-115">MEDIASUBTYPE_YUY2</span></span></li>
<li><span data-ttu-id="a1506-116">MEDIASUBTYPE_UYVY</span><span class="sxs-lookup"><span data-stu-id="a1506-116">MEDIASUBTYPE_UYVY</span></span></li>
<li><span data-ttu-id="a1506-117">MEDIASUBTYPE_RGB24</span><span class="sxs-lookup"><span data-stu-id="a1506-117">MEDIASUBTYPE_RGB24</span></span></li>
<li><span data-ttu-id="a1506-118">MEDIASUBTYPE_RGB32</span><span class="sxs-lookup"><span data-stu-id="a1506-118">MEDIASUBTYPE_RGB32</span></span></li>
<li><span data-ttu-id="a1506-119">MEDIASUBTYPE_ARGB32</span><span class="sxs-lookup"><span data-stu-id="a1506-119">MEDIASUBTYPE_ARGB32</span></span></li>
<li><span data-ttu-id="a1506-120">MEDIASUBTYPE_RGB565</span><span class="sxs-lookup"><span data-stu-id="a1506-120">MEDIASUBTYPE_RGB565</span></span></li>
<li><span data-ttu-id="a1506-121">MEDIASUBTYPE_RGB555</span><span class="sxs-lookup"><span data-stu-id="a1506-121">MEDIASUBTYPE_RGB555</span></span></li>
<li><span data-ttu-id="a1506-122">MEDIASUBTYPE_RGB8</span><span class="sxs-lookup"><span data-stu-id="a1506-122">MEDIASUBTYPE_RGB8</span></span></li>
<li><span data-ttu-id="a1506-123">MEDIASUBTYPE_Y41P</span><span class="sxs-lookup"><span data-stu-id="a1506-123">MEDIASUBTYPE_Y41P</span></span></li>
</ul><span data-ttu-id="a1506-124">
<strong>Tipos de formato</strong>:</span><span class="sxs-lookup"><span data-stu-id="a1506-124">
<strong>Format types</strong>:</span></span><br/> <span data-ttu-id="a1506-125">Format_VideoInfo, Format_VideoInfo2</span><span class="sxs-lookup"><span data-stu-id="a1506-125">Format_VideoInfo, Format_VideoInfo2</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1506-126">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="a1506-126">Output Pin Interfaces</span></span></td>
<td><span data-ttu-id="a1506-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span><span class="sxs-lookup"><span data-stu-id="a1506-127"><a href="/windows/desktop/api/Control/nn-control-imediaposition"><strong>IMediaPosition</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-imediaseeking"><strong>IMediaSeeking</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-ipin"><strong>IPin</strong></a>, <a href="/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol"><strong>IQualityControl</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1506-128">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="a1506-128">Filter CLSID</span></span></td>
<td><span data-ttu-id="a1506-129">CLSID_DVVideoCodec</span><span class="sxs-lookup"><span data-stu-id="a1506-129">CLSID_DVVideoCodec</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1506-130">CLSID de página de propriedades</span><span class="sxs-lookup"><span data-stu-id="a1506-130">Property Page CLSID</span></span></td>
<td><span data-ttu-id="a1506-131">CLSID_DVDecPropertiesPage</span><span class="sxs-lookup"><span data-stu-id="a1506-131">CLSID_DVDecPropertiesPage</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1506-132">Executável</span><span class="sxs-lookup"><span data-stu-id="a1506-132">Executable</span></span></td>
<td><span data-ttu-id="a1506-133">qdv.dll</span><span class="sxs-lookup"><span data-stu-id="a1506-133">qdv.dll</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a1506-134"><a href="merit.md">Núcleo</a></span><span class="sxs-lookup"><span data-stu-id="a1506-134"><a href="merit.md">Merit</a></span></span></td>
<td><span data-ttu-id="a1506-135">MERIT_NORMAL</span><span class="sxs-lookup"><span data-stu-id="a1506-135">MERIT_NORMAL</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a1506-136"><a href="filter-categories.md">Categoria do filtro</a></span><span class="sxs-lookup"><span data-stu-id="a1506-136"><a href="filter-categories.md">Filter Category</a></span></span></td>
<td><span data-ttu-id="a1506-137">CLSID_LegacyAmFilterCategory</span><span class="sxs-lookup"><span data-stu-id="a1506-137">CLSID_LegacyAmFilterCategory</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="a1506-138">Comentários</span><span class="sxs-lookup"><span data-stu-id="a1506-138">Remarks</span></span>

<span data-ttu-id="a1506-139">Use a interface [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) para definir a resolução de decodificação como Full, meia-size, tamanho de trimestre ou um oitavo tamanho.</span><span class="sxs-lookup"><span data-stu-id="a1506-139">Use the [**IIPDVDec**](/windows/desktop/api/Strmif/nn-strmif-iipdvdec) interface to set the decoding resolution to full, half size, quarter size, or one-eighth size.</span></span>

<span data-ttu-id="a1506-140">**Entrelaçamento**: as versões anteriores do decodificador sempre desentrelaçam o vídeo.</span><span class="sxs-lookup"><span data-stu-id="a1506-140">**Interlacing**: Earlier versions of the decoder always deinterlace the video.</span></span> <span data-ttu-id="a1506-141">A partir do DirectX 9,0, o decodificador de vídeo DV pode preservar o entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="a1506-141">As of DirectX 9.0, the DV Video Decoder can preserve the interlacing.</span></span> <span data-ttu-id="a1506-142">Isso permite que o vídeo entrelaçado seja desentrelaçado pelo VMR (Video Misturation Renderer), para melhor qualidade de renderização.</span><span class="sxs-lookup"><span data-stu-id="a1506-142">This enables the interlaced video to be deinterlaced by the Video Mixing Renderer (VMR), for improved rendering quality.</span></span> <span data-ttu-id="a1506-143">Para usar esse recurso, o filtro downstream deve dar suporte a formatos [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , indicados pelo formato de valor \_ VideoInfo2 no membro **formatType** da estrutura do [**\_ \_ tipo de mídia am**](/windows/win32/api/strmif/ns-strmif-am_media_type) .</span><span class="sxs-lookup"><span data-stu-id="a1506-143">To use this feature, the downstream filter must support [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) formats, indicated by that value Format\_VideoInfo2 in the **formattype** member of the [**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type) structure.</span></span> <span data-ttu-id="a1506-144">Na saída de resolução completa, os sinalizadores de desentrelaçamento (**dwInterlace**) na estrutura **VIDEOINFOHEADER2** são definidos como `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave` , indicando campos entrelaçados.</span><span class="sxs-lookup"><span data-stu-id="a1506-144">At full resolution output, the deinterlacing flags (**dwInterlace**) in the **VIDEOINFOHEADER2** structure are set to `AMINTERLACE_IsInterlaced | AMINTERLACE_DisplayModeBobOrWeave`, indicating interlaced fields.</span></span> <span data-ttu-id="a1506-145">Na metade da resolução ou inferior, **dwInterlace** é definido como zero, indicando quadros progressivos.</span><span class="sxs-lookup"><span data-stu-id="a1506-145">At half resolution or lower, **dwInterlace** is set to zero, indicating progressive frames.</span></span>

## <a name="related-topics"></a><span data-ttu-id="a1506-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="a1506-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a1506-147">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1506-147">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="a1506-148">Vídeo digital no DirectShow</span><span class="sxs-lookup"><span data-stu-id="a1506-148">Digital Video in DirectShow</span></span>](digital-video-in-directshow.md)
</dt> </dl>

 

 




