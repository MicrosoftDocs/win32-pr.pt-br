---
description: Conversões de tipo de mídia
ms.assetid: 6aee18b8-79b1-47fb-816f-d1c2c77b3a03
title: Conversões de tipo de mídia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee3a72e74439251f9661e0ff27166c504e47c238
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103663811"
---
# <a name="media-type-conversions"></a><span data-ttu-id="1f8cc-103">Conversões de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="1f8cc-103">Media Type Conversions</span></span>

<span data-ttu-id="1f8cc-104">Ocasionalmente, é necessário converter entre Media Foundation tipos de mídia e as estruturas de tipo de mídia mais antigas do DirectShow ou do Windows Media Format SDK.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-104">Occasionally it is necessary to convert between Media Foundation media types and the older media type structures from DirectShow or the Windows Media Format SDK.</span></span>

### <a name="from-a-format-structure-to-a-media-foundation-type"></a><span data-ttu-id="1f8cc-105">De uma estrutura de formato para um tipo de Media Foundation</span><span class="sxs-lookup"><span data-stu-id="1f8cc-105">From a Format Structure to a Media Foundation Type</span></span>

<span data-ttu-id="1f8cc-106">As funções a seguir inicializam um tipo de mídia Media Foundation de uma estrutura de formato.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-106">The following functions initialize a Media Foundation media type from a format structure.</span></span> <span data-ttu-id="1f8cc-107">Essas funções também serão úteis se um fluxo de dados ou um cabeçalho de arquivo contiver uma estrutura de formato.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-107">These functions are also useful if a data stream or a file header contains a format structure.</span></span> <span data-ttu-id="1f8cc-108">Por exemplo, o cabeçalho de arquivo para arquivos de áudio de som WAVE contém uma estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="1f8cc-108">For example, the file header for WAVE audio files contains a [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f8cc-109">Estrutura a ser convertida</span><span class="sxs-lookup"><span data-stu-id="1f8cc-109">Structure to Convert</span></span></th>
<th><span data-ttu-id="1f8cc-110">Função</span><span class="sxs-lookup"><span data-stu-id="1f8cc-110">Function</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1f8cc-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span><span class="sxs-lookup"><span data-stu-id="1f8cc-111"><a href="/windows/win32/api/strmif/ns-strmif-am_media_type"><strong>AM_MEDIA_TYPE</strong></a> (DirectShow)</span></span><br/> <span data-ttu-id="1f8cc-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (objetos de mídia do DirectX)</span><span class="sxs-lookup"><span data-stu-id="1f8cc-112"><a href="/previous-versions/windows/desktop/api/mediaobj/ns-mediaobj-dmo_media_type"><strong>DMO_MEDIA_TYPE</strong></a> (DirectX Media Objects)</span></span> <br/> <span data-ttu-id="1f8cc-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (SDK do Windows Media Format)</span><span class="sxs-lookup"><span data-stu-id="1f8cc-113"><a href="/previous-versions/windows/desktop/api/wmsdkidl/ns-wmsdkidl-wm_media_type"><strong>WM_MEDIA_TYPE</strong></a> (Windows Media Format SDK)</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="1f8cc-114">Essas estruturas são equivalentes.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-114">These structures are equivalent.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="1f8cc-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-115"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromammediatype"><strong>MFInitMediaTypeFromAMMediaType</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8cc-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-116"><a href="/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader"><strong>BITMAPINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="1f8cc-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-117"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfcreatevideomediatypefrombitmapinfoheaderex"><strong>MFCreateVideoMediaTypeFromBitMapInfoHeaderEx</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8cc-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-118"><a href="/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat"><strong>MFVIDEOFORMAT</strong></a></span></span></td>
<td><span data-ttu-id="1f8cc-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-119"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommfvideoformat"><strong>MFInitMediaTypeFromMFVideoFormat</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8cc-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-120"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-mpeg1videoinfo"><strong>MPEG1VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="1f8cc-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-121"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg1videoinfo"><strong>MFInitMediaTypeFromMPEG1VideoInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8cc-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-122"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-mpeg2videoinfo"><strong>MPEG2VIDEOINFO</strong></a></span></span></td>
<td><span data-ttu-id="1f8cc-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-123"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefrommpeg2videoinfo"><strong>MFInitMediaTypeFromMPEG2VideoInfo</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8cc-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-124"><a href="/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2"><strong>VIDEOINFOHEADER2</strong></a></span></span></td>
<td><span data-ttu-id="1f8cc-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-125"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader2"><strong>MFInitMediaTypeFromVideoInfoHeader2</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1f8cc-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-126"><a href="/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader"><strong>VIDEOINFOHEADER</strong></a></span></span></td>
<td><span data-ttu-id="1f8cc-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-127"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromvideoinfoheader"><strong>MFInitMediaTypeFromVideoInfoHeader</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1f8cc-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> ou <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"> <strong>WAVEFORMATEXTENSIBLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-128"><a href="/previous-versions/dd757713(v=vs.85)"><strong>WAVEFORMATEX</strong></a> or <a href="/previous-versions/windows/desktop/legacy/dd390971(v=vs.85)"><strong>WAVEFORMATEXTENSIBLE</strong></a></span></span></td>
<td><span data-ttu-id="1f8cc-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span><span class="sxs-lookup"><span data-stu-id="1f8cc-129"><a href="/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex"><strong>MFInitMediaTypeFromWaveFormatEx</strong></a></span></span></td>
</tr>
</tbody>
</table>



 

### <a name="from-a-media-foundation-type-to-a-format-structure"></a><span data-ttu-id="1f8cc-130">De um tipo de Media Foundation para uma estrutura de formato</span><span class="sxs-lookup"><span data-stu-id="1f8cc-130">From a Media Foundation Type to a Format Structure</span></span>

<span data-ttu-id="1f8cc-131">As funções a seguir criam ou inicializam uma estrutura de formato de um tipo de mídia Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-131">The following functions create or initialize a format structure from a Media Foundation media type.</span></span>



| <span data-ttu-id="1f8cc-132">Função</span><span class="sxs-lookup"><span data-stu-id="1f8cc-132">Function</span></span>                                                                             | <span data-ttu-id="1f8cc-133">Estrutura de Destino</span><span class="sxs-lookup"><span data-stu-id="1f8cc-133">Target Structure</span></span>                                                                                                                                                                    |
|--------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1f8cc-134">**IMFMediaType:: getrepresentation**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-134">**IMFMediaType::GetRepresentation**</span></span>](/windows/desktop/api/mfobjects/nf-mfobjects-imfmediatype-getrepresentation)            | <span data-ttu-id="1f8cc-135">[**Am \_ \_Tipo de mídia**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader)ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span><span class="sxs-lookup"><span data-stu-id="1f8cc-135">[**AM\_MEDIA\_TYPE**](/windows/win32/api/strmif/ns-strmif-am_media_type), [**MFVIDEOFORMAT**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat), [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader), or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2)</span></span> |
| [<span data-ttu-id="1f8cc-136">**MFCreateAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-136">**MFCreateAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreateammediatypefrommfmediatype)     | [<span data-ttu-id="1f8cc-137">**\_tipo de mídia am \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-137">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |
| [<span data-ttu-id="1f8cc-138">**MFCreateMFVideoFormatFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-138">**MFCreateMFVideoFormatFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatemfvideoformatfrommfmediatype) | [<span data-ttu-id="1f8cc-139">**MFVIDEOFORMAT**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-139">**MFVIDEOFORMAT**</span></span>](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoformat)                                                                                                                                              |
| [<span data-ttu-id="1f8cc-140">**MFCreateWaveFormatExFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-140">**MFCreateWaveFormatExFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfcreatewaveformatexfrommfmediatype)   | <span data-ttu-id="1f8cc-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) ou [ **WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="1f8cc-141">[**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) or [**WAVEFORMATEXTENSIBLE**](/previous-versions/windows/desktop/legacy/dd390971(v=vs.85))</span></span>                                                                                    |
| [<span data-ttu-id="1f8cc-142">**MFInitAMMediaTypeFromMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-142">**MFInitAMMediaTypeFromMFMediaType**</span></span>](/windows/desktop/api/mfapi/nf-mfapi-mfinitammediatypefrommfmediatype)         | [<span data-ttu-id="1f8cc-143">**\_tipo de mídia am \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-143">**AM\_MEDIA\_TYPE**</span></span>](/windows/win32/api/strmif/ns-strmif-am_media_type)                                                                                                                                          |



 

## <a name="format-mappings"></a><span data-ttu-id="1f8cc-144">Mapeamentos de formato</span><span class="sxs-lookup"><span data-stu-id="1f8cc-144">Format Mappings</span></span>

<span data-ttu-id="1f8cc-145">As tabelas a seguir listam os atributos de Media Foundation que correspondem a várias estruturas de formato.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-145">The following tables list the Media Foundation attributes that correspond to various format structures.</span></span> <span data-ttu-id="1f8cc-146">Nem todos esses atributos podem ser convertidos diretamente.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-146">Not all of these attributes can be translated directly.</span></span> <span data-ttu-id="1f8cc-147">Para executar conversões, você deve usar as funções listadas na seção anterior; essas tabelas são fornecidas principalmente para referência.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-147">To perform conversions, you should use the functions listed in the previous section; these tables are provided mainly for reference.</span></span>

### <a name="am_media_type"></a><span data-ttu-id="1f8cc-148">\_tipo de mídia am \_</span><span class="sxs-lookup"><span data-stu-id="1f8cc-148">AM\_MEDIA\_TYPE</span></span>



| <span data-ttu-id="1f8cc-149">Membro</span><span class="sxs-lookup"><span data-stu-id="1f8cc-149">Member</span></span>                   | <span data-ttu-id="1f8cc-150">Atributo</span><span class="sxs-lookup"><span data-stu-id="1f8cc-150">Attribute</span></span>                                                                            |
|--------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8cc-151">**bTemporalCompression**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-151">**bTemporalCompression**</span></span> | [<span data-ttu-id="1f8cc-152">**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-152">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md) |
| <span data-ttu-id="1f8cc-153">**bFixedSizeSamples**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-153">**bFixedSizeSamples**</span></span>    | [<span data-ttu-id="1f8cc-154">**\_amostras de \_ \_ tamanho fixo MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-154">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)           |
| <span data-ttu-id="1f8cc-155">**lSampleSize**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-155">**lSampleSize**</span></span>          | [<span data-ttu-id="1f8cc-156">**tamanho de amostra do MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-156">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                          |



 

### <a name="waveformatex-waveformatextensible"></a><span data-ttu-id="1f8cc-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span><span class="sxs-lookup"><span data-stu-id="1f8cc-157">WAVEFORMATEX, WAVEFORMATEXTENSIBLE</span></span>



| <span data-ttu-id="1f8cc-158">Membro</span><span class="sxs-lookup"><span data-stu-id="1f8cc-158">Member</span></span>                  | <span data-ttu-id="1f8cc-159">Atributo</span><span class="sxs-lookup"><span data-stu-id="1f8cc-159">Attribute</span></span>                                                                                                                                                                 |
|-------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8cc-160">**wFormatTag**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-160">**wFormatTag**</span></span>          | [<span data-ttu-id="1f8cc-161">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-161">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)<br/> <span data-ttu-id="1f8cc-162">Se **wFormatTag** for \_ \_ extensível de formato Wave, o subtipo será encontrado no membro **subformate** .</span><span class="sxs-lookup"><span data-stu-id="1f8cc-162">If **wFormatTag** is WAVE\_FORMAT\_EXTENSIBLE, the subtype is found in the **SubFormat** member.</span></span><br/> |
| <span data-ttu-id="1f8cc-163">**nChannels**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-163">**nChannels**</span></span>           | [<span data-ttu-id="1f8cc-164">**\_canais de \_ número de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-164">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                                                                                                |
| <span data-ttu-id="1f8cc-165">**nSamplesPerSec**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-165">**nSamplesPerSec**</span></span>      | [<span data-ttu-id="1f8cc-166">**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-166">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)                                                                                   |
| <span data-ttu-id="1f8cc-167">**nAvgBytesPerSec**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-167">**nAvgBytesPerSec**</span></span>     | [<span data-ttu-id="1f8cc-168">**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-168">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)                                                                              |
| <span data-ttu-id="1f8cc-169">**nBlockAlign**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-169">**nBlockAlign**</span></span>         | [<span data-ttu-id="1f8cc-170">**\_alinhamento de \_ bloco de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-170">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)                                                                                          |
| <span data-ttu-id="1f8cc-171">**wBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-171">**wBitsPerSample**</span></span>      | [<span data-ttu-id="1f8cc-172">**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-172">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)                                                                                         |
| <span data-ttu-id="1f8cc-173">**wValidBitsPerSample**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-173">**wValidBitsPerSample**</span></span> | [<span data-ttu-id="1f8cc-174">**\_áudio MF \_ MT \_ \_ bits válidos \_ por \_ amostra**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-174">**MF\_MT\_AUDIO\_VALID\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-valid-bits-per-sample-attribute.md)                                                                            |
| <span data-ttu-id="1f8cc-175">**wSamplesPerBlock**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-175">**wSamplesPerBlock**</span></span>    | [<span data-ttu-id="1f8cc-176">**\_amostras de áudio MF MT \_ \_ \_ por \_ bloco**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-176">**MF\_MT\_AUDIO\_SAMPLES\_PER\_BLOCK**</span></span>](mf-mt-audio-samples-per-block-attribute.md)                                                                                     |
| <span data-ttu-id="1f8cc-177">**dwChannelMask**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-177">**dwChannelMask**</span></span>       | [<span data-ttu-id="1f8cc-178">**\_máscara de \_ canal de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-178">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                                                                                                |
| <span data-ttu-id="1f8cc-179">**SubFormat**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-179">**SubFormat**</span></span>           | [<span data-ttu-id="1f8cc-180">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-180">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                                                                                                        |
| <span data-ttu-id="1f8cc-181">Dados extras</span><span class="sxs-lookup"><span data-stu-id="1f8cc-181">Extra data</span></span>              | [<span data-ttu-id="1f8cc-182">**dados de usuário do MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-182">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                                                                                                   |



 

### <a name="videoinfoheader-videoinfoheader2"></a><span data-ttu-id="1f8cc-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span><span class="sxs-lookup"><span data-stu-id="1f8cc-183">VIDEOINFOHEADER, VIDEOINFOHEADER2</span></span>



| <span data-ttu-id="1f8cc-184">Membro</span><span class="sxs-lookup"><span data-stu-id="1f8cc-184">Member</span></span>                                         | <span data-ttu-id="1f8cc-185">Atributo</span><span class="sxs-lookup"><span data-stu-id="1f8cc-185">Attribute</span></span>                                                                                                                                                                                                                                        |
|------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1f8cc-186">**dwBitRate**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-186">**dwBitRate**</span></span>                                  | [<span data-ttu-id="1f8cc-187">**\_taxa de \_ \_ bits média de MF MT**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-187">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="1f8cc-188">**dwBitErrorRate**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-188">**dwBitErrorRate**</span></span>                             | [<span data-ttu-id="1f8cc-189">**\_taxa de \_ \_ erros de \_ bit \_ do MF MT**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-189">**MF\_MT\_AVG\_BIT\_ERROR\_RATE**</span></span>](mf-mt-avg-bit-error-rate-attribute.md)                                                                                                                                                                      |
| <span data-ttu-id="1f8cc-190">**AvgTimePerFrame**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-190">**AvgTimePerFrame**</span></span>                            | <span data-ttu-id="1f8cc-191">[**MF \_ \_ \_ Taxa de quadros MT**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) para calcular esse valor.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-191">[**MF\_MT\_FRAME\_RATE**](mf-mt-frame-rate-attribute.md); use [**MFAverageTimePerFrameToFrameRate**](/windows/desktop/api/mfapi/nf-mfapi-mfaveragetimeperframetoframerate) to calculate this value.</span></span>                                                                             |
| <span data-ttu-id="1f8cc-192">**dwInterlaceFlags**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-192">**dwInterlaceFlags**</span></span>                           | [<span data-ttu-id="1f8cc-193">**\_modo de \_ entrelaçamento do MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-193">**MF\_MT\_INTERLACE\_MODE**</span></span>](mf-mt-interlace-mode-attribute.md)                                                                                                                                                                                |
| <span data-ttu-id="1f8cc-194">**dwCopyProtectFlags**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-194">**dwCopyProtectFlags**</span></span>                         | <span data-ttu-id="1f8cc-195">Nenhum equivalente definido</span><span class="sxs-lookup"><span data-stu-id="1f8cc-195">No defined equivalent</span></span>                                                                                                                                                                                                                            |
| <span data-ttu-id="1f8cc-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-196">**dwPictAspectRatioX**, **dwPictAspectRatioY**</span></span> | <span data-ttu-id="1f8cc-197">[**MF \_ \_ \_ \_ Taxa**](mf-mt-pixel-aspect-ratio-attribute.md)de proporção de pixel MT; deve converter da taxa de proporção da imagem para a taxa de proporção da imagem.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-197">[**MF\_MT\_PIXEL\_ASPECT\_RATIO**](mf-mt-pixel-aspect-ratio-attribute.md); must convert from picture aspect ratio to picture aspect ratio.</span></span>                                                                                                      |
| <span data-ttu-id="1f8cc-198">**dwControlFlags**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-198">**dwControlFlags**</span></span>                             | <span data-ttu-id="1f8cc-199">[**MF \_ \_sinalizadores de \_ controle \_ do pad MT**](mf-mt-pad-control-flags-attribute.md).</span><span class="sxs-lookup"><span data-stu-id="1f8cc-199">[**MF\_MT\_PAD\_CONTROL\_FLAGS**](mf-mt-pad-control-flags-attribute.md).</span></span> <span data-ttu-id="1f8cc-200">Se o sinalizador **AMCONTROL \_ COLORINFO \_ presente** estiver presente, defina os atributos de cores estendidos descritos em [informações de cores estendidas](extended-color-information.md).</span><span class="sxs-lookup"><span data-stu-id="1f8cc-200">If the **AMCONTROL\_COLORINFO\_PRESENT** flag is present, set the extended color attributes described in [Extended Color Information](extended-color-information.md).</span></span> |
| <span data-ttu-id="1f8cc-201">**bmiHeader. bilargura**, **BmiHeader. biHeight**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-201">**bmiHeader.biWidth**, **bmiHeader.biHeight**</span></span>  | [<span data-ttu-id="1f8cc-202">**\_tamanho do \_ quadro MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-202">**MF\_MT\_FRAME\_SIZE**</span></span>](mf-mt-frame-size-attribute.md)                                                                                                                                                                                        |
| <span data-ttu-id="1f8cc-203">**bmiHeader.biBitCount**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-203">**bmiHeader.biBitCount**</span></span>                       | <span data-ttu-id="1f8cc-204">Implícito no subtipo ([**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md)).</span><span class="sxs-lookup"><span data-stu-id="1f8cc-204">Implicit in the subtype ([**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md)).</span></span>                                                                                                                                                                    |
| <span data-ttu-id="1f8cc-205">**bmiHeader. biCompression**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-205">**bmiHeader.biCompression**</span></span>                    | <span data-ttu-id="1f8cc-206">Implícito no subtipo.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-206">Implicit in the subtype.</span></span>                                                                                                                                                                                                                         |
| <span data-ttu-id="1f8cc-207">**bmiHeader.biSizeImage**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-207">**bmiHeader.biSizeImage**</span></span>                      | [<span data-ttu-id="1f8cc-208">**tamanho de amostra do MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-208">**MF\_MT\_SAMPLE\_SIZE**</span></span>](mf-mt-sample-size-attribute.md)                                                                                                                                                                                      |
| <span data-ttu-id="1f8cc-209">Informações da paleta</span><span class="sxs-lookup"><span data-stu-id="1f8cc-209">Palette information</span></span>                            | [<span data-ttu-id="1f8cc-210">**\_paleta MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-210">**MF\_MT\_PALETTE**</span></span>](mf-mt-palette-attribute.md)                                                                                                                                                                                               |



 

<span data-ttu-id="1f8cc-211">Os atributos a seguir podem ser inferidos da estrutura [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) ou [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) , mas também exigem algum conhecimento dos detalhes do formato.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-211">The following attributes can be inferred from the [**VIDEOINFOHEADER**](/previous-versions/windows/desktop/api/amvideo/ns-amvideo-videoinfoheader) or [**VIDEOINFOHEADER2**](/previous-versions/windows/desktop/api/dvdmedia/ns-dvdmedia-videoinfoheader2) structure but also require some knowledge of the format details.</span></span> <span data-ttu-id="1f8cc-212">Por exemplo, diferentes formatos YUV têm requisitos de Stride diferentes.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-212">For example, different YUV formats have different stride requirements.</span></span>

-   [<span data-ttu-id="1f8cc-213">**\_ \_ Stride padrão MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-213">**MF\_MT\_DEFAULT\_STRIDE**</span></span>](mf-mt-default-stride-attribute.md)
-   [<span data-ttu-id="1f8cc-214">**\_abertura de \_ \_ exibição mínima \_ de MF MT**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-214">**MF\_MT\_MINIMUM\_DISPLAY\_APERTURE**</span></span>](mf-mt-minimum-display-aperture-attribute.md)
-   [<span data-ttu-id="1f8cc-215">**\_abertura de \_ digitalização de Pan MT \_ MF \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-215">**MF\_MT\_PAN\_SCAN\_APERTURE**</span></span>](mf-mt-pan-scan-aperture-attribute.md)

### <a name="mpeg1videoinfo"></a><span data-ttu-id="1f8cc-216">MPEG1VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="1f8cc-216">MPEG1VIDEOINFO</span></span>



| <span data-ttu-id="1f8cc-217">Membro</span><span class="sxs-lookup"><span data-stu-id="1f8cc-217">Member</span></span>                                   | <span data-ttu-id="1f8cc-218">Atributo</span><span class="sxs-lookup"><span data-stu-id="1f8cc-218">Attribute</span></span>                                                                       |
|------------------------------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="1f8cc-219">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-219">**dwStartTimeCode**</span></span>                      | [<span data-ttu-id="1f8cc-220">**código de hora de início do MF \_ MT \_ MPEG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-220">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="1f8cc-221">**bSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-221">**bSequenceHeader**</span></span>                      | [<span data-ttu-id="1f8cc-222">**cabeçalho de sequência do MF \_ MT \_ MPEG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-222">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="1f8cc-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-223">**biXPelsPerMeter**, **biYPelsPerMeter**</span></span> | [<span data-ttu-id="1f8cc-224">**taxa de proporção de pixel do MF \_ MT \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-224">**MF\_MT\_PIXEL\_ASPECT\_RATIO**</span></span>](mf-mt-pixel-aspect-ratio-attribute.md)      |



 

### <a name="mpeg2videoinfo"></a><span data-ttu-id="1f8cc-225">MPEG2VIDEOINFO</span><span class="sxs-lookup"><span data-stu-id="1f8cc-225">MPEG2VIDEOINFO</span></span>



| <span data-ttu-id="1f8cc-226">Membro</span><span class="sxs-lookup"><span data-stu-id="1f8cc-226">Member</span></span>               | <span data-ttu-id="1f8cc-227">Atributo</span><span class="sxs-lookup"><span data-stu-id="1f8cc-227">Attribute</span></span>                                                                       |
|----------------------|---------------------------------------------------------------------------------|
| <span data-ttu-id="1f8cc-228">**dwStartTimeCode**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-228">**dwStartTimeCode**</span></span>  | [<span data-ttu-id="1f8cc-229">**código de hora de início do MF \_ MT \_ MPEG \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-229">**MF\_MT\_MPEG\_START\_TIME\_CODE**</span></span>](mf-mt-mpeg-start-time-code-attribute.md) |
| <span data-ttu-id="1f8cc-230">**dwSequenceHeader**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-230">**dwSequenceHeader**</span></span> | [<span data-ttu-id="1f8cc-231">**cabeçalho de sequência do MF \_ MT \_ MPEG \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-231">**MF\_MT\_MPEG\_SEQUENCE\_HEADER**</span></span>](mf-mt-mpeg-sequence-header-attribute.md)  |
| <span data-ttu-id="1f8cc-232">**dwProfile**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-232">**dwProfile**</span></span>        | [<span data-ttu-id="1f8cc-233">**\_Perfil MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-233">**MF\_MT\_MPEG2\_PROFILE**</span></span>](mf-mt-mpeg2-profile-attribute.md)                 |
| <span data-ttu-id="1f8cc-234">**dwLevel**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-234">**dwLevel**</span></span>          | [<span data-ttu-id="1f8cc-235">**Nível de MPEG2 do MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-235">**MF\_MT\_MPEG2\_LEVEL**</span></span>](mf-mt-mpeg2-level-attribute.md)                     |
| <span data-ttu-id="1f8cc-236">**dwFlags**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-236">**dwFlags**</span></span>          | [<span data-ttu-id="1f8cc-237">**Sinalizadores de MPEG2 do MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="1f8cc-237">**MF\_MT\_MPEG2\_FLAGS**</span></span>](mf-mt-mpeg2-flags-attribute.md)                     |



 

## <a name="examples"></a><span data-ttu-id="1f8cc-238">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1f8cc-238">Examples</span></span>

<span data-ttu-id="1f8cc-239">O código a seguir preenche uma estrutura [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) de um tipo de mídia de vídeo.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-239">The following code fills in a [**BITMAPINFOHEADER**](/windows/win32/api/wingdi/ns-wingdi-bitmapinfoheader) structure from a video media type.</span></span> <span data-ttu-id="1f8cc-240">Observe que essas conversões perdem algumas das informações de formato (entrelaçamento, taxa de quadros, dados de cores estendidos).</span><span class="sxs-lookup"><span data-stu-id="1f8cc-240">Note that this conversions loses some of the format information (interlacing, frame rate, extended color data).</span></span> <span data-ttu-id="1f8cc-241">No entanto, pode ser útil ao salvar um bitmap de um quadro de vídeo, por exemplo.</span><span class="sxs-lookup"><span data-stu-id="1f8cc-241">However, it might be useful when saving a bitmap from a video frame, for example.</span></span>


```C++
#include <dshow.h>
#include <dvdmedia.h>

// Converts a video type to a BITMAPINFO structure.
// The caller must free the structure by calling CoTaskMemFree.

// Note that this conversion loses some format information, including 
// interlacing, and frame rate.

HRESULT GetBitmapInfoHeaderFromMFMediaType(
    IMFMediaType *pType,            // Pointer to the media type.
    BITMAPINFOHEADER **ppBmih,      // Receives a pointer to the structure. 
    DWORD *pcbSize)                 // Receives the size of the structure.
{
    *ppBmih = NULL;
    *pcbSize = 0;

    GUID majorType = GUID_NULL;
    AM_MEDIA_TYPE *pmt = NULL;
    DWORD cbSize = 0;
    DWORD cbOffset = 0;
    BITMAPINFOHEADER *pBMIH = NULL;

    // Verify that this is a video type.
    HRESULT hr = pType->GetMajorType(&majorType);
    if (FAILED(hr))
    {
        goto done;
    }

    if (majorType != MFMediaType_Video)
    {
        hr = MF_E_INVALIDMEDIATYPE;
        goto done;
    }

    hr = pType->GetRepresentation(AM_MEDIA_TYPE_REPRESENTATION, (void**)&pmt);
    if (FAILED(hr))
    {
        goto done;
    }

    if (pmt->formattype == FORMAT_VideoInfo)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER,bmiHeader));
    }
    else if (pmt->formattype == FORMAT_VideoInfo2)
    {
        cbOffset = (FIELD_OFFSET(VIDEOINFOHEADER2,bmiHeader));
    }
    else
    {
        hr = MF_E_INVALIDMEDIATYPE; // Unsupported format type.
        goto done;
    }

    if (pmt->cbFormat - cbOffset < sizeof(BITMAPINFOHEADER))
    {
        hr = E_UNEXPECTED; // Bad format size. 
        goto done;
    }

    cbSize = pmt->cbFormat - cbOffset;

    pBMIH = (BITMAPINFOHEADER*)CoTaskMemAlloc(cbSize);
    if (pBMIH == NULL)
    {
        hr = E_OUTOFMEMORY;
        goto done;
    }
    
    CopyMemory(pBMIH, pmt->pbFormat + cbOffset, cbSize);
    
    *ppBmih = pBMIH;
    *pcbSize = cbSize;

done:
    if (pmt)
    {
        pType->FreeRepresentation(AM_MEDIA_TYPE_REPRESENTATION, pmt);
    }
    return hr;
}
```



## <a name="related-topics"></a><span data-ttu-id="1f8cc-242">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1f8cc-242">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1f8cc-243">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="1f8cc-243">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 
