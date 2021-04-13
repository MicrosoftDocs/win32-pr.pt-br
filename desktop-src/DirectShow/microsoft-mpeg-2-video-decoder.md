---
description: Esse filtro decodifica o vídeo MPEG-1, MPEG-2, H. 264.
ms.assetid: d8195c3a-97ac-4ad1-a097-18878c8fda6f
title: Decodificador de vídeo do Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8460b5b554fffc8f0dd8679810e5ef3f42bcb004
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104370105"
---
# <a name="microsoft-mpeg-2-video-decoder"></a><span data-ttu-id="052a3-103">Decodificador de vídeo do Microsoft MPEG-2</span><span class="sxs-lookup"><span data-stu-id="052a3-103">Microsoft MPEG-2 Video Decoder</span></span>

<span data-ttu-id="052a3-104">Esse filtro decodifica o vídeo MPEG-1, MPEG-2, H. 264.</span><span class="sxs-lookup"><span data-stu-id="052a3-104">This filter decodes MPEG-1, MPEG-2, H.264 video.</span></span>

> [!Note]  
> <span data-ttu-id="052a3-105">A decodificação do vídeo H. 264 requer o Windows 7.</span><span class="sxs-lookup"><span data-stu-id="052a3-105">Decoding of H.264 video requires Windows 7.</span></span>

 

> [!Note]  
> <span data-ttu-id="052a3-106">Não há suporte para esse filtro em plataformas baseadas em IA-64.</span><span class="sxs-lookup"><span data-stu-id="052a3-106">This filter is not supported on IA-64-based platforms.</span></span>

 

<span data-ttu-id="052a3-107">No registro, o nome amigável desse filtro é "decodificador de vídeo Microsoft DTV-DVD".</span><span class="sxs-lookup"><span data-stu-id="052a3-107">In the registry, the friendly name of this filter is "Microsoft DTV-DVD Video Decoder".</span></span>



<span data-ttu-id="052a3-108">Informações de filtro</span><span class="sxs-lookup"><span data-stu-id="052a3-108">Filter Information</span></span>

<span data-ttu-id="052a3-109">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="052a3-109">Filter Interfaces</span></span>

[<span data-ttu-id="052a3-110">**IAMDecoderCaps**</span><span class="sxs-lookup"><span data-stu-id="052a3-110">**IAMDecoderCaps**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iamdecodercaps)<br/> [<span data-ttu-id="052a3-111">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="052a3-111">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="052a3-112">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="052a3-112">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/>

<span data-ttu-id="052a3-113">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="052a3-113">Input Pin Media Types</span></span>

<span data-ttu-id="052a3-114">Pino de entrada de vídeo:</span><span class="sxs-lookup"><span data-stu-id="052a3-114">Video input pin:</span></span>

-   <span data-ttu-id="052a3-115">\_ \_ Pacote de DVD criptografado \_ de MediaType, vídeo do MEDIASUBTYPE \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="052a3-115">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="052a3-116">\_ \_ Vídeo de MediaType MPEG2 PES, MEDIASUBTYPE \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="052a3-116">MEDIATYPE\_MPEG2\_PES, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>
-   <span data-ttu-id="052a3-117">\_Vídeo de MediaType, MEDIASUBTYPE \_ MPEG1Packet</span><span class="sxs-lookup"><span data-stu-id="052a3-117">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Packet</span></span>
-   <span data-ttu-id="052a3-118">\_Vídeo de MediaType, MEDIASUBTYPE \_ MPEG1Payload</span><span class="sxs-lookup"><span data-stu-id="052a3-118">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG1Payload</span></span>
-   <span data-ttu-id="052a3-119">\_Vídeo de MediaType, vídeo do MEDIASUBTYPE \_ MPEG2 \_</span><span class="sxs-lookup"><span data-stu-id="052a3-119">MEDIATYPE\_Video, MEDIASUBTYPE\_MPEG2\_VIDEO</span></span>

<span data-ttu-id="052a3-120">Pino de entrada da subimagem:</span><span class="sxs-lookup"><span data-stu-id="052a3-120">Subpicture input pin:</span></span><br/>

-   <span data-ttu-id="052a3-121">\_ \_ pacote de DVD criptografado \_ de MediaType, \_ SUBimagem de DVD MEDIASUBTYPE \_</span><span class="sxs-lookup"><span data-stu-id="052a3-121">MEDIATYPE\_DVD\_ENCRYPTED\_PACK, MEDIASUBTYPE\_DVD\_SUBPICTURE</span></span>

<span data-ttu-id="052a3-122">A partir do Windows 7, o PIN de entrada de vídeo também dá suporte aos seguintes tipos de entrada:</span><span class="sxs-lookup"><span data-stu-id="052a3-122">Starting in Windows 7, the video input pin also supports the following input types:</span></span><br/>

-   <span data-ttu-id="052a3-123">**MediaType \_ Vídeo**, **MEDIASUBTYPE \_ AVC1**</span><span class="sxs-lookup"><span data-stu-id="052a3-123">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_AVC1**</span></span>
-   <span data-ttu-id="052a3-124">**MediaType \_ Vídeo**, **MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="052a3-124">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_H264**</span></span>
-   <span data-ttu-id="052a3-125">**MediaType \_ Vídeo**, **MEDIASUBTYPE \_ H264**</span><span class="sxs-lookup"><span data-stu-id="052a3-125">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_h264**</span></span>
-   <span data-ttu-id="052a3-126">**MediaType \_ Vídeo**, **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="052a3-126">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_X264**</span></span>
-   <span data-ttu-id="052a3-127">**MediaType \_ Vídeo**, **MEDIASUBTYPE \_ x264**</span><span class="sxs-lookup"><span data-stu-id="052a3-127">**MEDIATYPE\_Video**, **MEDIASUBTYPE\_x264**</span></span>

<span data-ttu-id="052a3-128">Consulte [tipos de vídeo H. 264](h-264-video-types.md) para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="052a3-128">See [H.264 Video Types](h-264-video-types.md) for more information.</span></span> <span data-ttu-id="052a3-129">O tipo de mídia de entrada pode ser alterado dinamicamente entre os tipos MPEG2 e H. 264.</span><span class="sxs-lookup"><span data-stu-id="052a3-129">The input media type can change dynamically between MPEG2 and H.264 types.</span></span><br/>

<span data-ttu-id="052a3-130">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="052a3-130">Input Pin Interfaces</span></span>

[<span data-ttu-id="052a3-131">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="052a3-131">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> [<span data-ttu-id="052a3-132">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="052a3-132">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="052a3-133">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="052a3-133">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="052a3-134">**IMFSampleProtection**</span><span class="sxs-lookup"><span data-stu-id="052a3-134">**IMFSampleProtection**</span></span>](/windows/win32/api/mfidl/nn-mfidl-imfsampleprotection)<br/> [<span data-ttu-id="052a3-135">**IPin**</span><span class="sxs-lookup"><span data-stu-id="052a3-135">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="052a3-136">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="052a3-136">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="052a3-137">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="052a3-137">Output Pin Media Types</span></span>

<span data-ttu-id="052a3-138">Pino de saída do vídeo:</span><span class="sxs-lookup"><span data-stu-id="052a3-138">Video output pin:</span></span>

-   <span data-ttu-id="052a3-139">Vídeo de MEDIATYPE \_ , DXVA \_ ModeMPEG2 \_ A (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="052a3-139">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_A (DXVA 1.0)</span></span>
-   <span data-ttu-id="052a3-140">\_Vídeo de MediaType, DXVA \_ ModeMPEG2 \_ C (DXVA 1,0)</span><span class="sxs-lookup"><span data-stu-id="052a3-140">MEDIATYPE\_Video, DXVA\_ModeMPEG2\_C (DXVA 1.0)</span></span>
-   <span data-ttu-id="052a3-141">\_Vídeo de MediaType, MEDIASUBTYPE \_ I420 (decodificação de software ou DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="052a3-141">MEDIATYPE\_Video, MEDIASUBTYPE\_I420 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="052a3-142">\_Vídeo de MediaType, MEDIASUBTYPE \_ NV12 (decodificação de software ou DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="052a3-142">MEDIATYPE\_Video, MEDIASUBTYPE\_NV12 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="052a3-143">\_Vídeo de MediaType, MEDIASUBTYPE \_ YUY2 (decodificação de software ou DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="052a3-143">MEDIATYPE\_Video, MEDIASUBTYPE\_YUY2 (Software decode or DXVA2.0)</span></span>
-   <span data-ttu-id="052a3-144">\_Vídeo de MediaType, MEDIASUBTYPE \_ IMC3 (somente DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="052a3-144">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC3 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="052a3-145">\_Vídeo de MediaType, MEDIASUBTYPE \_ IMC4 (somente DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="052a3-145">MEDIATYPE\_Video, MEDIASUBTYPE\_IMC4 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="052a3-146">\_Vídeo de MediaType, MEDIASUBTYPE \_ S340 (somente DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="052a3-146">MEDIATYPE\_Video, MEDIASUBTYPE\_S340 (DXVA2.0 only)</span></span>
-   <span data-ttu-id="052a3-147">\_Vídeo de MediaType, MEDIASUBTYPE \_ YV12 (somente DXVA 2.0)</span><span class="sxs-lookup"><span data-stu-id="052a3-147">MEDIATYPE\_Video, MEDIASUBTYPE\_YV12 (DXVA2.0 only)</span></span>

<span data-ttu-id="052a3-148">Pino de saída de linha-21:</span><span class="sxs-lookup"><span data-stu-id="052a3-148">Line-21 output pin:</span></span><br/>

-   <span data-ttu-id="052a3-149">MEDIATYPE \_ AUXLine21Data, MEDIASUBTYPE \_ Line21 \_ GOPPacket</span><span class="sxs-lookup"><span data-stu-id="052a3-149">MEDIATYPE\_AUXLine21Data, MEDIASUBTYPE\_Line21\_GOPPacket</span></span>

<span data-ttu-id="052a3-150">Pino de saída da subimagem:</span><span class="sxs-lookup"><span data-stu-id="052a3-150">Subpicture output pin:</span></span><br/>

-   <span data-ttu-id="052a3-151">\_Vídeo de MediaType, MEDIASUBTYPE \_ AI44</span><span class="sxs-lookup"><span data-stu-id="052a3-151">MEDIATYPE\_Video, MEDIASUBTYPE\_AI44</span></span>
-   <span data-ttu-id="052a3-152">\_Vídeo de MediaType, MEDIASUBTYPE \_ ARGB32</span><span class="sxs-lookup"><span data-stu-id="052a3-152">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB32</span></span>
-   <span data-ttu-id="052a3-153">\_Vídeo de MediaType, MEDIASUBTYPE \_ ARGB4444</span><span class="sxs-lookup"><span data-stu-id="052a3-153">MEDIATYPE\_Video, MEDIASUBTYPE\_ARGB4444</span></span>
-   <span data-ttu-id="052a3-154">\_Vídeo de MediaType, MEDIASUBTYPE \_ AYUV</span><span class="sxs-lookup"><span data-stu-id="052a3-154">MEDIATYPE\_Video, MEDIASUBTYPE\_AYUV</span></span>

<span data-ttu-id="052a3-155">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="052a3-155">Output Pin Interfaces</span></span>

<span data-ttu-id="052a3-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (somente PIN de saída de vídeo)</span><span class="sxs-lookup"><span data-stu-id="052a3-156">[**IAMVideoAcceleratorNotify**](/previous-versions/windows/desktop/api/videoacc/nn-videoacc-iamvideoacceleratornotify) (video output pin only)</span></span><br/> [<span data-ttu-id="052a3-157">**IKsPropertySet**</span><span class="sxs-lookup"><span data-stu-id="052a3-157">**IKsPropertySet**</span></span>](ikspropertyset.md)<br/> [<span data-ttu-id="052a3-158">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="052a3-158">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="052a3-159">**IPin**</span><span class="sxs-lookup"><span data-stu-id="052a3-159">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="052a3-160">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="052a3-160">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/> [<span data-ttu-id="052a3-161">**IVPConfig**</span><span class="sxs-lookup"><span data-stu-id="052a3-161">**IVPConfig**</span></span>](/previous-versions/windows/desktop/api/Vpconfig/nn-vpconfig-ivpconfig)<br/>

<span data-ttu-id="052a3-162">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="052a3-162">Filter CLSID</span></span>

<span data-ttu-id="052a3-163">**CLSID \_ do CMPEG2VidDecoderDS** (definido em wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="052a3-163">**CLSID\_CMPEG2VidDecoderDS** (defined in wmcodecdsp.h)</span></span>

<span data-ttu-id="052a3-164">Executável</span><span class="sxs-lookup"><span data-stu-id="052a3-164">Executable</span></span>

<span data-ttu-id="052a3-165">msmpeg2vdec.dll</span><span class="sxs-lookup"><span data-stu-id="052a3-165">msmpeg2vdec.dll</span></span>

[<span data-ttu-id="052a3-166">Núcleo</span><span class="sxs-lookup"><span data-stu-id="052a3-166">Merit</span></span>](merit.md)

<span data-ttu-id="052a3-167">**Mérito \_ NORMAL** -1</span><span class="sxs-lookup"><span data-stu-id="052a3-167">**MERIT\_NORMAL** - 1</span></span>

[<span data-ttu-id="052a3-168">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="052a3-168">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="052a3-169">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="052a3-169">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="052a3-170">Comentários</span><span class="sxs-lookup"><span data-stu-id="052a3-170">Remarks</span></span>

<span data-ttu-id="052a3-171">Esse filtro tem dois Pins de entrada e três Pins de saída.</span><span class="sxs-lookup"><span data-stu-id="052a3-171">This filter has two input pins and three output pins.</span></span>

<span data-ttu-id="052a3-172">Pins de entrada:</span><span class="sxs-lookup"><span data-stu-id="052a3-172">Input pins:</span></span>

-   <span data-ttu-id="052a3-173">Entrada de vídeo</span><span class="sxs-lookup"><span data-stu-id="052a3-173">Video input</span></span>
-   <span data-ttu-id="052a3-174">Entrada de subimagem</span><span class="sxs-lookup"><span data-stu-id="052a3-174">Subpicture input</span></span>

<span data-ttu-id="052a3-175">Pins de saída:</span><span class="sxs-lookup"><span data-stu-id="052a3-175">Output pins:</span></span>

-   <span data-ttu-id="052a3-176">Saída de vídeo</span><span class="sxs-lookup"><span data-stu-id="052a3-176">Video output</span></span>
-   <span data-ttu-id="052a3-177">Saída de linha 21</span><span class="sxs-lookup"><span data-stu-id="052a3-177">Line-21 output</span></span>
-   <span data-ttu-id="052a3-178">Saída da subimagem</span><span class="sxs-lookup"><span data-stu-id="052a3-178">Subpicture output</span></span>

<span data-ttu-id="052a3-179">O filtro não criará o pino de saída da subimagem, a menos que o pino de entrada de vídeo esteja conectado a um tipo de mídia de **\_ \_ \_ pacote criptografado de DVD de MediaType** .</span><span class="sxs-lookup"><span data-stu-id="052a3-179">The filter does not create the subpicture output pin unless the video input pin is connected with a **MEDIATYPE\_DVD\_ENCRYPTED\_PACK** media type.</span></span>

### <a name="mpeg-12-support"></a><span data-ttu-id="052a3-180">Suporte a MPEG-1/2</span><span class="sxs-lookup"><span data-stu-id="052a3-180">MPEG-1/2 Support</span></span>

<span data-ttu-id="052a3-181">Para MPEG-1 e MPEG-2, o decodificador dá suporte aos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="052a3-181">For MPEG-1 and MPEG-2, the decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="052a3-182">Perfis/níveis</span><span class="sxs-lookup"><span data-stu-id="052a3-182">Profiles/Levels</span></span></td>
<td><span data-ttu-id="052a3-183">Qualquer combinação dos seguintes perfis e níveis:</span><span class="sxs-lookup"><span data-stu-id="052a3-183">Any combination of the following profiles and levels:</span></span><br/>
<ul>
<li><span data-ttu-id="052a3-184">Perfis: simples, principal</span><span class="sxs-lookup"><span data-stu-id="052a3-184">Profiles: Simple, Main</span></span></li>
<li><span data-ttu-id="052a3-185">Níveis: baixo, principal, alto, alto 1440</span><span class="sxs-lookup"><span data-stu-id="052a3-185">Levels: Low, Main, High, High 1440</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="052a3-186">Formatos de croma</span><span class="sxs-lookup"><span data-stu-id="052a3-186">Chroma Formats</span></span></td>
<td><span data-ttu-id="052a3-187">4:2:0 croma</span><span class="sxs-lookup"><span data-stu-id="052a3-187">4:2:0 chroma</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="052a3-188">Resolução máxima</span><span class="sxs-lookup"><span data-stu-id="052a3-188">Maximum Resolution</span></span></td>
<td><span data-ttu-id="052a3-189">1920 × 1088 pixels</span><span class="sxs-lookup"><span data-stu-id="052a3-189">1920 × 1088 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="052a3-190">DXVA</span><span class="sxs-lookup"><span data-stu-id="052a3-190">DXVA</span></span></td>
<td><span data-ttu-id="052a3-191">O decodificador dá suporte a DXVA (DirectX Video Acceleration) versão 1 e à versão 2.</span><span class="sxs-lookup"><span data-stu-id="052a3-191">The decoder supports DirectX Video Acceleration (DXVA) version 1 and version 2.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="052a3-192">O decodificador não dá suporte a fragmentado escalonáveis.</span><span class="sxs-lookup"><span data-stu-id="052a3-192">The decoder does not support scalable bitstreams.</span></span> <span data-ttu-id="052a3-193">A entrada deve ser um fluxo de vídeo elementar.</span><span class="sxs-lookup"><span data-stu-id="052a3-193">The input must be an elementary video stream.</span></span>

<span data-ttu-id="052a3-194">O decodificador não oferece suporte a formatos de 4:2:2 croma.</span><span class="sxs-lookup"><span data-stu-id="052a3-194">The decoder does not support 4:2:2 chroma formats.</span></span>

### <a name="h264-support"></a><span data-ttu-id="052a3-195">Suporte a H. 264</span><span class="sxs-lookup"><span data-stu-id="052a3-195">H.264 Support</span></span>

<span data-ttu-id="052a3-196">Para H. 264, o decodificador dá suporte aos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="052a3-196">For H.264, the decoder supports the following formats:</span></span>



| <span data-ttu-id="052a3-197">Requisito</span><span class="sxs-lookup"><span data-stu-id="052a3-197">Requirement</span></span> | <span data-ttu-id="052a3-198">Valor</span><span class="sxs-lookup"><span data-stu-id="052a3-198">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="052a3-199">Perfis/níveis</span><span class="sxs-lookup"><span data-stu-id="052a3-199">Profiles/Levels</span></span>    | <span data-ttu-id="052a3-200">Perfis de linha de base, principal e alto, até o nível 5,1.</span><span class="sxs-lookup"><span data-stu-id="052a3-200">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="052a3-201">(Consulte Especificação ITU-T H. 264 para obter detalhes.)</span><span class="sxs-lookup"><span data-stu-id="052a3-201">(See ITU-T H.264 specification for details.)</span></span>                                                                                                                                                                          |
| <span data-ttu-id="052a3-202">Formatos de croma</span><span class="sxs-lookup"><span data-stu-id="052a3-202">Chroma Formats</span></span>     | <span data-ttu-id="052a3-203">4:2:0 croma ou monocromático</span><span class="sxs-lookup"><span data-stu-id="052a3-203">4:2:0 chroma or monochrome</span></span>                                                                                                                                                                                                                                                |
| <span data-ttu-id="052a3-204">Resolução mínima</span><span class="sxs-lookup"><span data-stu-id="052a3-204">Minimum Resolution</span></span> | <span data-ttu-id="052a3-205">48 × 48 pixels</span><span class="sxs-lookup"><span data-stu-id="052a3-205">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                            |
| <span data-ttu-id="052a3-206">Resolução máxima</span><span class="sxs-lookup"><span data-stu-id="052a3-206">Maximum Resolution</span></span> | <span data-ttu-id="052a3-207">1920 × 1088 pixels</span><span class="sxs-lookup"><span data-stu-id="052a3-207">1920 × 1088 pixels</span></span>                                                                                                                                                                                                                                                        |
| <span data-ttu-id="052a3-208">DXVA</span><span class="sxs-lookup"><span data-stu-id="052a3-208">DXVA</span></span>               | <span data-ttu-id="052a3-209">O decodificador oferece suporte a DXVA versão 2, mas não a DXVA versão 1.</span><span class="sxs-lookup"><span data-stu-id="052a3-209">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="052a3-210">A decodificação de DXVA tem suporte apenas para fragmentado de linha de base, principal e de perfil alto compatíveis com o principal.</span><span class="sxs-lookup"><span data-stu-id="052a3-210">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="052a3-211">(Fragmentado de linha de base compatíveis principal são definidos como **perfil \_ idc**= 66 e **\_ \_ sinalizador conjunto1 restrito**= 1.)</span><span class="sxs-lookup"><span data-stu-id="052a3-211">(Main-compatible Baseline bitstreams are defined as **profile\_idc**=66 and **constrained\_set1\_flag**=1.)</span></span> |



 

<span data-ttu-id="052a3-212">O decodificador não oferece suporte à tecnologia de refinamento de filmes.</span><span class="sxs-lookup"><span data-stu-id="052a3-212">The decoder does not support Film Grain Technology.</span></span>

<span data-ttu-id="052a3-213">Para obter informações sobre os tipos de mídia H. 264, consulte [tipos de vídeo h. 264](h-264-video-types.md).</span><span class="sxs-lookup"><span data-stu-id="052a3-213">For information about the H.264 media types, see [H.264 Video Types](h-264-video-types.md).</span></span>

### <a name="codec-properties"></a><span data-ttu-id="052a3-214">Propriedades do codec</span><span class="sxs-lookup"><span data-stu-id="052a3-214">Codec Properties</span></span>

<span data-ttu-id="052a3-215">Os Pins de entrada dão suporte aos seguintes conjuntos de propriedades por meio de [**IKsPropertySet**](ikspropertyset.md):</span><span class="sxs-lookup"><span data-stu-id="052a3-215">The input pins support the following property sets through [**IKsPropertySet**](ikspropertyset.md):</span></span>

-   [<span data-ttu-id="052a3-216">**Conjunto de propriedades da proteção contra cópia de DVD**</span><span class="sxs-lookup"><span data-stu-id="052a3-216">**DVD Copy Protection Property Set**</span></span>](dvd-copy-protection-property-set.md)
-   <span data-ttu-id="052a3-217">[**Conjunto de propriedades de subimagem do DVD**](dvd-subpicture-property-set.md) (somente PIN da subimagem)</span><span class="sxs-lookup"><span data-stu-id="052a3-217">[**DVD Subpicture Property Set**](dvd-subpicture-property-set.md) (subpicture pin only)</span></span>

<span data-ttu-id="052a3-218">Os Pins de entrada dão suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="052a3-218">The input pins support the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="052a3-219">Propriedade</span><span class="sxs-lookup"><span data-stu-id="052a3-219">Property</span></span>                                                                  | <span data-ttu-id="052a3-220">Exige</span><span class="sxs-lookup"><span data-stu-id="052a3-220">Requires</span></span>      |
|---------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="052a3-221">**AVDecCommonInputFormat**</span><span class="sxs-lookup"><span data-stu-id="052a3-221">**AVDecCommonInputFormat**</span></span>](avdeccommoninputformat-property.md)         | <span data-ttu-id="052a3-222">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="052a3-222">Windows Vista</span></span> |
| [<span data-ttu-id="052a3-223">**AVDecVideoInputScanType**</span><span class="sxs-lookup"><span data-stu-id="052a3-223">**AVDecVideoInputScanType**</span></span>](avdecvideoinputscantype-property.md)       | <span data-ttu-id="052a3-224">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="052a3-224">Windows Vista</span></span> |
| [<span data-ttu-id="052a3-225">**AVDecVideoPixelAspectRatio**</span><span class="sxs-lookup"><span data-stu-id="052a3-225">**AVDecVideoPixelAspectRatio**</span></span>](avdecvideopixelaspectratio-property.md) | <span data-ttu-id="052a3-226">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="052a3-226">Windows Vista</span></span> |



 

<span data-ttu-id="052a3-227">O filtro oferece suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="052a3-227">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>



| <span data-ttu-id="052a3-228">Propriedade</span><span class="sxs-lookup"><span data-stu-id="052a3-228">Property</span></span>                                                                                | <span data-ttu-id="052a3-229">Exige</span><span class="sxs-lookup"><span data-stu-id="052a3-229">Requires</span></span>      |
|-----------------------------------------------------------------------------------------|---------------|
| [<span data-ttu-id="052a3-230">**AVDecMmcssClass**</span><span class="sxs-lookup"><span data-stu-id="052a3-230">**AVDecMmcssClass**</span></span>](avdecmmcss-property.md)                                          | <span data-ttu-id="052a3-231">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="052a3-231">Windows Vista</span></span> |
| [<span data-ttu-id="052a3-232">**AVDecVideoAcceleration \_ H264**</span><span class="sxs-lookup"><span data-stu-id="052a3-232">**AVDecVideoAcceleration\_H264**</span></span>](avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="052a3-233">Windows 7</span><span class="sxs-lookup"><span data-stu-id="052a3-233">Windows 7</span></span>     |
| [<span data-ttu-id="052a3-234">**AVDecVideoAcceleration \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="052a3-234">**AVDecVideoAcceleration\_MPEG2**</span></span>](avdecvideoacceleration-mpeg2-property.md)          | <span data-ttu-id="052a3-235">Windows 7</span><span class="sxs-lookup"><span data-stu-id="052a3-235">Windows 7</span></span>     |
| [<span data-ttu-id="052a3-236">**AVDecVideoDropPicWithMissingRef**</span><span class="sxs-lookup"><span data-stu-id="052a3-236">**AVDecVideoDropPicWithMissingRef**</span></span>](avdecvideodroppicwithmissingref-property.md)     | <span data-ttu-id="052a3-237">Windows 7</span><span class="sxs-lookup"><span data-stu-id="052a3-237">Windows 7</span></span>     |
| [<span data-ttu-id="052a3-238">**AVDecVideoFastDecodeMode**</span><span class="sxs-lookup"><span data-stu-id="052a3-238">**AVDecVideoFastDecodeMode**</span></span>](avdecvideofastdecodemode.md)                            | <span data-ttu-id="052a3-239">Windows 7</span><span class="sxs-lookup"><span data-stu-id="052a3-239">Windows 7</span></span>     |
| [<span data-ttu-id="052a3-240">**AVDecVideoImageSize**</span><span class="sxs-lookup"><span data-stu-id="052a3-240">**AVDecVideoImageSize**</span></span>](avdecvideoimagesize.md)                                      | <span data-ttu-id="052a3-241">Windows 7</span><span class="sxs-lookup"><span data-stu-id="052a3-241">Windows 7</span></span>     |
| [<span data-ttu-id="052a3-242">**AVDecVideoSoftwareDeinterlaceMode**</span><span class="sxs-lookup"><span data-stu-id="052a3-242">**AVDecVideoSoftwareDeinterlaceMode**</span></span>](avdecvideosoftwaredeinterlacemode-property.md) | <span data-ttu-id="052a3-243">Windows 7</span><span class="sxs-lookup"><span data-stu-id="052a3-243">Windows 7</span></span>     |
| [<span data-ttu-id="052a3-244">**AVDecVideoThumbnailGenerationMode**</span><span class="sxs-lookup"><span data-stu-id="052a3-244">**AVDecVideoThumbnailGenerationMode**</span></span>](avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="052a3-245">Windows 7</span><span class="sxs-lookup"><span data-stu-id="052a3-245">Windows 7</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="052a3-246">Requisitos</span><span class="sxs-lookup"><span data-stu-id="052a3-246">Requirements</span></span>



| <span data-ttu-id="052a3-247">Requisito</span><span class="sxs-lookup"><span data-stu-id="052a3-247">Requirement</span></span> | <span data-ttu-id="052a3-248">Valor</span><span class="sxs-lookup"><span data-stu-id="052a3-248">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="052a3-249">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="052a3-249">Minimum supported client</span></span><br/> | <span data-ttu-id="052a3-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="052a3-250">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="052a3-251">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="052a3-251">Minimum supported server</span></span><br/> | <span data-ttu-id="052a3-252">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="052a3-252">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="052a3-253">parâmetro</span><span class="sxs-lookup"><span data-stu-id="052a3-253">Header</span></span><br/>                   | <dl> <span data-ttu-id="052a3-254"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="052a3-254"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="052a3-255">Confira também</span><span class="sxs-lookup"><span data-stu-id="052a3-255">See also</span></span>

<dl> <dt>

[<span data-ttu-id="052a3-256">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="052a3-256">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="052a3-257">**Tipos de mídia de DVD**</span><span class="sxs-lookup"><span data-stu-id="052a3-257">**DVD Media Types**</span></span>](dvd-media-types.md)
</dt> <dt>

[<span data-ttu-id="052a3-258">Tipos de vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="052a3-258">H.264 Video Types</span></span>](h-264-video-types.md)
</dt> </dl>

 

 
