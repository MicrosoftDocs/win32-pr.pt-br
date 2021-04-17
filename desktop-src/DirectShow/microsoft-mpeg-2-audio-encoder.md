---
description: O filtro Microsoft MPEG-2 Audio Encoder codifica as camadas de áudio MPEG-1 I e II, incluindo suporte para as extensões MPEG-2 Low amostragem Frequency (LSF).
ms.assetid: a36e838b-8b11-4851-9dd2-efd9fe070770
title: Codificador de áudio Microsoft MPEG-2 (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d055acd379d9e966f43eac284e38a10c05a86c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105759494"
---
# <a name="microsoft-mpeg-2-audio-encoder"></a><span data-ttu-id="d30e3-103">Codificador de áudio Microsoft MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d30e3-103">Microsoft MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="d30e3-104">O filtro Microsoft MPEG-2 Audio Encoder codifica as camadas de áudio MPEG-1 I e II, incluindo suporte para as extensões MPEG-2 Low amostragem Frequency (LSF).</span><span class="sxs-lookup"><span data-stu-id="d30e3-104">The Microsoft MPEG-2 Audio Encoder filter encodes MPEG-1 audio layers I and II, including support for the MPEG-2 Low Sampling Frequency (LSF) extensions.</span></span>

<span data-ttu-id="d30e3-105">Para codificar e multiplexar fluxos de áudio/vídeo, use o filtro de [**codificador MPEG-2 da Microsoft**](microsoft-mpeg-2-encoder.md) , que encapsula as funções desse filtro e do filtro de [**codificador de vídeo MPEG-2 da Microsoft**](microsoft-mpeg-2-video-encoder.md) .</span><span class="sxs-lookup"><span data-stu-id="d30e3-105">To encode and multiplex audio/video streams, use the [**Microsoft MPEG-2 Encoder**](microsoft-mpeg-2-encoder.md) filter, which encapsulates the functions of both this filter and the [**Microsoft MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filter.</span></span>

> [!Note]  
> <span data-ttu-id="d30e3-106">Não há suporte para esse filtro em plataformas baseadas em IA-64.</span><span class="sxs-lookup"><span data-stu-id="d30e3-106">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="d30e3-107">Informações de filtro</span><span class="sxs-lookup"><span data-stu-id="d30e3-107">Filter Information</span></span>

<span data-ttu-id="d30e3-108">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="d30e3-108">Filter Interfaces</span></span>

[<span data-ttu-id="d30e3-109">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="d30e3-109">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="d30e3-110">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d30e3-110">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="d30e3-111">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="d30e3-111">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="d30e3-112">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="d30e3-112">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="d30e3-113">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="d30e3-113">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="d30e3-114">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="d30e3-114">Input Pin Media Types</span></span>

<span data-ttu-id="d30e3-115">**MediaType \_ Áudio**, **MEDIASUBTYPE \_ PCM**</span><span class="sxs-lookup"><span data-stu-id="d30e3-115">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_PCM**</span></span>

<span data-ttu-id="d30e3-116">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="d30e3-116">Input Pin Interfaces</span></span>

[<span data-ttu-id="d30e3-117">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="d30e3-117">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="d30e3-118">**IPin**</span><span class="sxs-lookup"><span data-stu-id="d30e3-118">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="d30e3-119">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="d30e3-119">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="d30e3-120">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="d30e3-120">Output Pin Media Types</span></span>

<span data-ttu-id="d30e3-121">**MediaType \_ Áudio**, **\_ \_ áudio MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="d30e3-121">**MEDIATYPE\_Audio**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="d30e3-122">**MediaType \_ Fluxo**, **\_ \_ áudio MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="d30e3-122">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_AUDIO**</span></span><br/> <span data-ttu-id="d30e3-123">**MediaType \_ Fluxo**, **\_ \_ programa MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="d30e3-123">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span><br/> <span data-ttu-id="d30e3-124">**MediaType \_ Fluxo**, **\_ \_ transporte MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="d30e3-124">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span><br/>

<span data-ttu-id="d30e3-125">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="d30e3-125">Output Pin Interfaces</span></span>

[<span data-ttu-id="d30e3-126">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="d30e3-126">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="d30e3-127">**IPin**</span><span class="sxs-lookup"><span data-stu-id="d30e3-127">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="d30e3-128">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="d30e3-128">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="d30e3-129">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="d30e3-129">Filter CLSID</span></span>

<span data-ttu-id="d30e3-130">**CLSID \_ do CMPEG2EncoderAudioDS** (declarado em wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="d30e3-130">**CLSID\_CMPEG2EncoderAudioDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="d30e3-131">Executável</span><span class="sxs-lookup"><span data-stu-id="d30e3-131">Executable</span></span>

<span data-ttu-id="d30e3-132">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="d30e3-132">msmpeg2enc.dll</span></span>

[<span data-ttu-id="d30e3-133">Núcleo</span><span class="sxs-lookup"><span data-stu-id="d30e3-133">Merit</span></span>](merit.md)

<span data-ttu-id="d30e3-134">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="d30e3-134">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="d30e3-135">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="d30e3-135">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="d30e3-136">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="d30e3-136">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="d30e3-137">Comentários</span><span class="sxs-lookup"><span data-stu-id="d30e3-137">Remarks</span></span>

<span data-ttu-id="d30e3-138">O codificador de áudio MPEG-2 pode produzir os seguintes tipos de saída:</span><span class="sxs-lookup"><span data-stu-id="d30e3-138">The MPEG-2 Audio Encoder can produce the following kinds of output:</span></span>

-   <span data-ttu-id="d30e3-139">Fluxo elementar áudio</span><span class="sxs-lookup"><span data-stu-id="d30e3-139">Audio elementary stream</span></span>
-   <span data-ttu-id="d30e3-140">Áudio em um fluxo de programa MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d30e3-140">Audio in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="d30e3-141">Áudio em um fluxo de transporte MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d30e3-141">Audio in an MPEG-2 transport stream</span></span>

<span data-ttu-id="d30e3-142">Ele dá suporte a camadas MPEG-1 I e II e extensões LSF (baixa amostragem Frequency) de MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d30e3-142">It supports MPEG-1 layers I and II and MPEG-2 low sampling frequency (LSF) extensions</span></span>

<span data-ttu-id="d30e3-143">Os exemplos de entrada devem ter 16 bits por amostra, com uma taxa de amostragem de áudio de 48, 44,1, 32, 22, 5 ou 16 KHz.</span><span class="sxs-lookup"><span data-stu-id="d30e3-143">Input samples must 16 bits per sample, with an audio sampling rate of 48, 44.1, 32, 22.05, or 16 KHz.</span></span> <span data-ttu-id="d30e3-144">O codificador não pode reamostrar o fluxo de áudio; o áudio codificado tem a mesma taxa de amostragem que a entrada.</span><span class="sxs-lookup"><span data-stu-id="d30e3-144">The encoder cannot resample the audio stream; the encoded audio has the same sample rate as the input.</span></span>

<span data-ttu-id="d30e3-145">Os exemplos de entrada devem ser mono ou estéreo.</span><span class="sxs-lookup"><span data-stu-id="d30e3-145">Input samples must be mono or stereo.</span></span> <span data-ttu-id="d30e3-146">O áudio codificado tem o número de canais como entrada.</span><span class="sxs-lookup"><span data-stu-id="d30e3-146">The encoded audio has the number of channels as the input.</span></span>

### <a name="limitations"></a><span data-ttu-id="d30e3-147">Limitações</span><span class="sxs-lookup"><span data-stu-id="d30e3-147">Limitations</span></span>

<span data-ttu-id="d30e3-148">O codificador não oferece suporte ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="d30e3-148">The encoder does not support the following:</span></span>

-   <span data-ttu-id="d30e3-149">Áudio MPEG Layer III fragmentado.</span><span class="sxs-lookup"><span data-stu-id="d30e3-149">MPEG layer III audio bitstreams.</span></span>
-   <span data-ttu-id="d30e3-150">Extensão de vários canais MPEG-2 fragmentado.</span><span class="sxs-lookup"><span data-stu-id="d30e3-150">MPEG-2 multi-channel extension bitstreams.</span></span>
-   <span data-ttu-id="d30e3-151">MPEG-4 AAC fragmentado.</span><span class="sxs-lookup"><span data-stu-id="d30e3-151">MPEG-4 AAC bitstreams.</span></span>
-   <span data-ttu-id="d30e3-152">Fragmentado (NBC) compatível com MPEG-2 sem versões anteriores.</span><span class="sxs-lookup"><span data-stu-id="d30e3-152">MPEG-2 non-backward compatible (NBC) bitstreams.</span></span>
-   <span data-ttu-id="d30e3-153">Geração de pacotes de pacote de fluxo elementar (PES).</span><span class="sxs-lookup"><span data-stu-id="d30e3-153">Generation of packetized elementary stream (PES) packets.</span></span>
-   <span data-ttu-id="d30e3-154">Codificação digital Dolby.</span><span class="sxs-lookup"><span data-stu-id="d30e3-154">Dolby Digital encoding.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="d30e3-155">Propriedades do codec</span><span class="sxs-lookup"><span data-stu-id="d30e3-155">Codec Properties</span></span>

<span data-ttu-id="d30e3-156">O filtro oferece suporte às seguintes propriedades por meio de [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span><span class="sxs-lookup"><span data-stu-id="d30e3-156">The filter supports the following properties through [**ICodecAPI**](/windows/desktop/api/Strmif/nn-strmif-icodecapi):</span></span>

-   [<span data-ttu-id="d30e3-157">**AVAudioChannelCount**</span><span class="sxs-lookup"><span data-stu-id="d30e3-157">**AVAudioChannelCount**</span></span>](avaudiochannelcount-property.md)
-   [<span data-ttu-id="d30e3-158">**AVAudioSampleRate**</span><span class="sxs-lookup"><span data-stu-id="d30e3-158">**AVAudioSampleRate**</span></span>](avaudiosamplerate-property.md)
-   [<span data-ttu-id="d30e3-159">**AVEncAudioIntervalToEncode**</span><span class="sxs-lookup"><span data-stu-id="d30e3-159">**AVEncAudioIntervalToEncode**</span></span>](avencaudiointervaltoencode-property.md)
-   [<span data-ttu-id="d30e3-160">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="d30e3-160">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
-   [<span data-ttu-id="d30e3-161">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="d30e3-161">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="d30e3-162">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="d30e3-162">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)
-   [<span data-ttu-id="d30e3-163">**AVEncMPACopyright**</span><span class="sxs-lookup"><span data-stu-id="d30e3-163">**AVEncMPACopyright**</span></span>](avencmpacopyright-property.md)
-   [<span data-ttu-id="d30e3-164">**AVEncMPAEmphasisType**</span><span class="sxs-lookup"><span data-stu-id="d30e3-164">**AVEncMPAEmphasisType**</span></span>](avencmpaemphasistype-property.md)
-   [<span data-ttu-id="d30e3-165">**AVEncMPAEnableRedundancyProtection**</span><span class="sxs-lookup"><span data-stu-id="d30e3-165">**AVEncMPAEnableRedundancyProtection**</span></span>](avencmpaenableredundancyprotection-property.md)
-   [<span data-ttu-id="d30e3-166">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="d30e3-166">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
-   [<span data-ttu-id="d30e3-167">**AVEncMPAOriginalBitstream**</span><span class="sxs-lookup"><span data-stu-id="d30e3-167">**AVEncMPAOriginalBitstream**</span></span>](avencmpaoriginalbitstream-property.md)
-   [<span data-ttu-id="d30e3-168">**AVEncMPAPrivateUserBit**</span><span class="sxs-lookup"><span data-stu-id="d30e3-168">**AVEncMPAPrivateUserBit**</span></span>](avencmpaprivateuserbit-property.md)

> [!Note]  
> <span data-ttu-id="d30e3-169">Uma versão anterior da documentação listava incorretamente algumas propriedades adicionais que não têm suporte.</span><span class="sxs-lookup"><span data-stu-id="d30e3-169">An earlier version of the documentation incorrectly listed some additional properties that are not supported.</span></span>

 

<span data-ttu-id="d30e3-170">Para compatibilidade com versões anteriores, o filtro oferece suporte à seguinte propriedade por meio da interface **IEncoderAPI** :</span><span class="sxs-lookup"><span data-stu-id="d30e3-170">For backward compatibility, the filter supports the following property through the **IEncoderAPI** interface:</span></span>



| <span data-ttu-id="d30e3-171">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d30e3-171">Property</span></span>                 | <span data-ttu-id="d30e3-172">Descrição</span><span class="sxs-lookup"><span data-stu-id="d30e3-172">Description</span></span>                                                                      |
|--------------------------|----------------------------------------------------------------------------------|
| <span data-ttu-id="d30e3-173">**\_taxa de bits ENCAPIPARAM**</span><span class="sxs-lookup"><span data-stu-id="d30e3-173">**ENCAPIPARAM\_BITRATE**</span></span> | <span data-ttu-id="d30e3-174">Equivalente a [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span><span class="sxs-lookup"><span data-stu-id="d30e3-174">Equivalent to [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md).</span></span> |



 

<span data-ttu-id="d30e3-175">É recomendável definir as propriedades na seguinte ordem:</span><span class="sxs-lookup"><span data-stu-id="d30e3-175">It is recommended to set properties in the following order:</span></span>

1.  [<span data-ttu-id="d30e3-176">**AVEncCommonFormatConstraint**</span><span class="sxs-lookup"><span data-stu-id="d30e3-176">**AVEncCommonFormatConstraint**</span></span>](avenccommonformatconstraint-property.md)
2.  [<span data-ttu-id="d30e3-177">**AVEncMPALayer**</span><span class="sxs-lookup"><span data-stu-id="d30e3-177">**AVEncMPALayer**</span></span>](avencmpalayer-property.md)
3.  [<span data-ttu-id="d30e3-178">**AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="d30e3-178">**AVEncCommonMeanBitRate**</span></span>](avenccommonmeanbitrate-property.md)
4.  [<span data-ttu-id="d30e3-179">**AVEncMPACodingMode**</span><span class="sxs-lookup"><span data-stu-id="d30e3-179">**AVEncMPACodingMode**</span></span>](avencmpacodingmode-property.md)

<span data-ttu-id="d30e3-180">Defina as propriedades restantes em qualquer ordem.</span><span class="sxs-lookup"><span data-stu-id="d30e3-180">Set the remaining properties in any order.</span></span>

## <a name="requirements"></a><span data-ttu-id="d30e3-181">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d30e3-181">Requirements</span></span>



| <span data-ttu-id="d30e3-182">Requisito</span><span class="sxs-lookup"><span data-stu-id="d30e3-182">Requirement</span></span> | <span data-ttu-id="d30e3-183">Valor</span><span class="sxs-lookup"><span data-stu-id="d30e3-183">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d30e3-184">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d30e3-184">Minimum supported client</span></span><br/> | <span data-ttu-id="d30e3-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="d30e3-185">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="d30e3-186">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d30e3-186">Minimum supported server</span></span><br/> | <span data-ttu-id="d30e3-187">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="d30e3-187">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="d30e3-188">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d30e3-188">Header</span></span><br/>                   | <dl> <span data-ttu-id="d30e3-189"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="d30e3-189"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="d30e3-190">Confira também</span><span class="sxs-lookup"><span data-stu-id="d30e3-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d30e3-191">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="d30e3-191">DirectShow Filters</span></span>](directshow-filters.md)
</dt> <dt>

[<span data-ttu-id="d30e3-192">**Tipos de mídia de Desmultiplexador MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="d30e3-192">**MPEG-2 Demultiplexer Media Types**</span></span>](mpeg-2-demultiplexer-media-types.md)
</dt> </dl>

 

 
