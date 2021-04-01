---
description: O filtro de codificador MPEG-2 da Microsoft codificará áudio e vídeo MPEG-2 e multiplexa os fluxos para gerar um fluxo de programa MPEG-2 ou fluxo de transporte.
ms.assetid: 61e8918b-7f5a-4720-bb3b-df9ac7614894
title: Codificador MPEG-2 da Microsoft (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ef5fad3b316db9ac4e47efcb9de761227cdd3279
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "103645766"
---
# <a name="microsoft-mpeg-2-encoder"></a><span data-ttu-id="6a65a-103">Codificador MPEG-2 da Microsoft</span><span class="sxs-lookup"><span data-stu-id="6a65a-103">Microsoft MPEG-2 Encoder</span></span>

<span data-ttu-id="6a65a-104">O filtro de codificador MPEG-2 da Microsoft codificará áudio e vídeo MPEG-2 e multiplexa os fluxos para gerar um fluxo de programa MPEG-2 ou fluxo de transporte.</span><span class="sxs-lookup"><span data-stu-id="6a65a-104">The Microsoft MPEG-2 Encoder filter encodes MPEG-2 audio and video and multiplexes the streams to generate an MPEG-2 program stream or transport stream.</span></span>

> [!Note]  
> <span data-ttu-id="6a65a-105">Não há suporte para esse filtro em plataformas baseadas em IA-64.</span><span class="sxs-lookup"><span data-stu-id="6a65a-105">This filter is not supported on IA-64-based platforms.</span></span>

 



<span data-ttu-id="6a65a-106">Informações de filtro</span><span class="sxs-lookup"><span data-stu-id="6a65a-106">Filter Information</span></span>

<span data-ttu-id="6a65a-107">Filtrar interfaces</span><span class="sxs-lookup"><span data-stu-id="6a65a-107">Filter Interfaces</span></span>

[<span data-ttu-id="6a65a-108">**IBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="6a65a-108">**IBaseFilter**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ibasefilter)<br/> [<span data-ttu-id="6a65a-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="6a65a-109">**ICodecAPI**</span></span>](/windows/desktop/api/Strmif/nn-strmif-icodecapi)<br/> <span data-ttu-id="6a65a-110">**IEncoderAPI**</span><span class="sxs-lookup"><span data-stu-id="6a65a-110">**IEncoderAPI**</span></span><br/> [<span data-ttu-id="6a65a-111">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="6a65a-111">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="6a65a-112">**IVideoEncoder**</span><span class="sxs-lookup"><span data-stu-id="6a65a-112">**IVideoEncoder**</span></span>](/windows/win32/api/strmif/nn-strmif-ivideoencoder)<br/>

<span data-ttu-id="6a65a-113">Tipos de mídia de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="6a65a-113">Input Pin Media Types</span></span>

<span data-ttu-id="6a65a-114">Ver comentários</span><span class="sxs-lookup"><span data-stu-id="6a65a-114">See Remarks</span></span>

<span data-ttu-id="6a65a-115">Interfaces de pino de entrada</span><span class="sxs-lookup"><span data-stu-id="6a65a-115">Input Pin Interfaces</span></span>

[<span data-ttu-id="6a65a-116">**IMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="6a65a-116">**IMemInputPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imeminputpin)<br/> [<span data-ttu-id="6a65a-117">**IPin**</span><span class="sxs-lookup"><span data-stu-id="6a65a-117">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="6a65a-118">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="6a65a-118">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="6a65a-119">Tipos de mídia do pino de saída</span><span class="sxs-lookup"><span data-stu-id="6a65a-119">Output Pin Media Types</span></span>

<span data-ttu-id="6a65a-120">Ver comentários</span><span class="sxs-lookup"><span data-stu-id="6a65a-120">See Remarks</span></span>

<span data-ttu-id="6a65a-121">Interfaces de pino de saída</span><span class="sxs-lookup"><span data-stu-id="6a65a-121">Output Pin Interfaces</span></span>

[<span data-ttu-id="6a65a-122">**IMediaSeeking**</span><span class="sxs-lookup"><span data-stu-id="6a65a-122">**IMediaSeeking**</span></span>](/windows/desktop/api/Strmif/nn-strmif-imediaseeking)<br/> [<span data-ttu-id="6a65a-123">**IPin**</span><span class="sxs-lookup"><span data-stu-id="6a65a-123">**IPin**</span></span>](/windows/desktop/api/Strmif/nn-strmif-ipin)<br/> [<span data-ttu-id="6a65a-124">**IQualityControl**</span><span class="sxs-lookup"><span data-stu-id="6a65a-124">**IQualityControl**</span></span>](/windows/desktop/api/Strmif/nn-strmif-iqualitycontrol)<br/>

<span data-ttu-id="6a65a-125">CLSID do filtro</span><span class="sxs-lookup"><span data-stu-id="6a65a-125">Filter CLSID</span></span>

<span data-ttu-id="6a65a-126">**CLSID \_ do CMPEG2EncoderDS** (declarado em wmcodecdsp. h)</span><span class="sxs-lookup"><span data-stu-id="6a65a-126">**CLSID\_CMPEG2EncoderDS** (declared in wmcodecdsp.h)</span></span>

<span data-ttu-id="6a65a-127">Executável</span><span class="sxs-lookup"><span data-stu-id="6a65a-127">Executable</span></span>

<span data-ttu-id="6a65a-128">msmpeg2enc.dll</span><span class="sxs-lookup"><span data-stu-id="6a65a-128">msmpeg2enc.dll</span></span>

[<span data-ttu-id="6a65a-129">Núcleo</span><span class="sxs-lookup"><span data-stu-id="6a65a-129">Merit</span></span>](merit.md)

<span data-ttu-id="6a65a-130">**MÉRITO \_ \_ não \_ use**</span><span class="sxs-lookup"><span data-stu-id="6a65a-130">**MERIT\_DO\_NOT\_USE**</span></span>

[<span data-ttu-id="6a65a-131">Categoria do filtro</span><span class="sxs-lookup"><span data-stu-id="6a65a-131">Filter Category</span></span>](filter-categories.md)

<span data-ttu-id="6a65a-132">**\_LEGACYAMFILTERCATEGORY CLSID**</span><span class="sxs-lookup"><span data-stu-id="6a65a-132">**CLSID\_LegacyAmFilterCategory**</span></span>



 

## <a name="remarks"></a><span data-ttu-id="6a65a-133">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a65a-133">Remarks</span></span>

<span data-ttu-id="6a65a-134">Esse filtro combina a funcionalidade de codificação de dois outros filtros:</span><span class="sxs-lookup"><span data-stu-id="6a65a-134">This filter combines the encoding functionality of two other filters:</span></span>

-   [<span data-ttu-id="6a65a-135">**Codificador de áudio Microsoft MPEG-2**</span><span class="sxs-lookup"><span data-stu-id="6a65a-135">**Microsoft MPEG-2 Audio Encoder**</span></span>](microsoft-mpeg-2-audio-encoder.md)
-   [<span data-ttu-id="6a65a-136">**Codificador de vídeo MPEG-2 da Microsoft**</span><span class="sxs-lookup"><span data-stu-id="6a65a-136">**Microsoft MPEG-2 Video Encoder**</span></span>](microsoft-mpeg-2-video-encoder.md)

<span data-ttu-id="6a65a-137">Exceto como observado, esse filtro oferece suporte aos mesmos recursos de codificação que os dois codificadores.</span><span class="sxs-lookup"><span data-stu-id="6a65a-137">Except as noted, this filter supports the same encoding features as those two encoders.</span></span>

<span data-ttu-id="6a65a-138">Inicialmente, o filtro tem um pino de entrada, que pode aceitar entrada de áudio ou vídeo.</span><span class="sxs-lookup"><span data-stu-id="6a65a-138">Initially the filter has one input pin, which can accept audio or video input.</span></span> <span data-ttu-id="6a65a-139">Quando esse PIN é conectado, o filtro cria um segundo PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="6a65a-139">When that pin is connected, the filter creates a second input pin.</span></span> <span data-ttu-id="6a65a-140">Se o primeiro PIN de entrada receber áudio, o segundo PIN de entrada aceitará apenas o vídeo e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="6a65a-140">If the first input pin receives audio, the second input pin accepts only video, and vice versa.</span></span> <span data-ttu-id="6a65a-141">Cada PIN de entrada dá suporte aos mesmos tipos de mídia que o filtro de codificador correspondente.</span><span class="sxs-lookup"><span data-stu-id="6a65a-141">Each input pin supports the same media types as the corresponding encoder filter.</span></span>

<span data-ttu-id="6a65a-142">Se apenas um PIN de entrada estiver conectado, o filtro dará suporte aos mesmos tipos de saída que o codificador de áudio ou vídeo correspondente.</span><span class="sxs-lookup"><span data-stu-id="6a65a-142">If only one input pin is connected, the filter supports the same output types as the corresponding audio or video encoder.</span></span> <span data-ttu-id="6a65a-143">Se ambos os Pins estiverem conectados, o filtro dará suporte aos seguintes tipos de saída:</span><span class="sxs-lookup"><span data-stu-id="6a65a-143">If both pins are connected, the filter supports the following kinds of output:</span></span>

-   <span data-ttu-id="6a65a-144">Áudio-visual em um fluxo de programa MPEG-2</span><span class="sxs-lookup"><span data-stu-id="6a65a-144">Audio-visual in an MPEG-2 program stream</span></span>
-   <span data-ttu-id="6a65a-145">Áudio-visual em um fluxo de transporte MPEG-2</span><span class="sxs-lookup"><span data-stu-id="6a65a-145">Audio-visual in an MPEG-2 transport stream</span></span>

<span data-ttu-id="6a65a-146">Eles correspondem aos seguintes tipos de saída:</span><span class="sxs-lookup"><span data-stu-id="6a65a-146">These correspond to the following output types:</span></span>

-   <span data-ttu-id="6a65a-147">**MediaType \_ Fluxo**, **\_ \_ programa MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="6a65a-147">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_PROGRAM**</span></span>
-   <span data-ttu-id="6a65a-148">**MediaType \_ Fluxo**, **\_ \_ transporte MEDIASUBTYPE MPEG2**</span><span class="sxs-lookup"><span data-stu-id="6a65a-148">**MEDIATYPE\_Stream**, **MEDIASUBTYPE\_MPEG2\_TRANSPORT**</span></span>

<span data-ttu-id="6a65a-149">Esse filtro não pode multiplexar fluxos que foram codificados anteriormente.</span><span class="sxs-lookup"><span data-stu-id="6a65a-149">This filter cannot multiplex streams that were previously encoded.</span></span> <span data-ttu-id="6a65a-150">Os fluxos de entrada devem ser áudio/vídeo descompactado, que o filtro codifica antes da multiplexação.</span><span class="sxs-lookup"><span data-stu-id="6a65a-150">The input streams must be uncompressed audio/video, which the filter encodes before multiplexing.</span></span> <span data-ttu-id="6a65a-151">O fluxo multiplexado é limitado a um programa, contendo até um áudio e um fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6a65a-151">The multiplexed stream is limited to one program, containing up to one audio and one video stream.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="6a65a-152">Propriedades do codec</span><span class="sxs-lookup"><span data-stu-id="6a65a-152">Codec Properties</span></span>

<span data-ttu-id="6a65a-153">O filtro dá suporte às propriedades combinadas do [**codificador de áudio MPEG-2**](microsoft-mpeg-2-audio-encoder.md) e dos filtros de [**codificador de vídeo MPEG-2**](microsoft-mpeg-2-video-encoder.md) , com a seguinte diferença:</span><span class="sxs-lookup"><span data-stu-id="6a65a-153">The filter supports the combined properties of the [**MPEG-2 Audio Encoder**](microsoft-mpeg-2-audio-encoder.md) and [**MPEG-2 Video Encoder**](microsoft-mpeg-2-video-encoder.md) filters, with the following difference:</span></span>

-   <span data-ttu-id="6a65a-154">A propriedade [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) define a taxa média de bits para o fluxo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="6a65a-154">The [**AVEncCommonMeanBitRate**](avenccommonmeanbitrate-property.md) property sets the average bit rate for the video stream.</span></span>
-   <span data-ttu-id="6a65a-155">A propriedade [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) define a taxa média de bits para o fluxo de áudio.</span><span class="sxs-lookup"><span data-stu-id="6a65a-155">The [**AVEncAudioMeanBitRate**](avencaudiomeanbitrate.md) property sets the average bit rate for the audio stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="6a65a-156">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6a65a-156">Requirements</span></span>



| <span data-ttu-id="6a65a-157">Requisito</span><span class="sxs-lookup"><span data-stu-id="6a65a-157">Requirement</span></span> | <span data-ttu-id="6a65a-158">Valor</span><span class="sxs-lookup"><span data-stu-id="6a65a-158">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6a65a-159">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a65a-159">Minimum supported client</span></span><br/> | <span data-ttu-id="6a65a-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[ Desktop apps\]</span><span class="sxs-lookup"><span data-stu-id="6a65a-160">Windows Vista Home Premium, Windows Vista Ultimate, Windows 7 Home Premium, Windows 7 Professional, Windows 7 Enterprise, Windows 7 Ultimate \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="6a65a-161">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="6a65a-161">Minimum supported server</span></span><br/> | <span data-ttu-id="6a65a-162">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="6a65a-162">None supported</span></span><br/>                                                                                                                                                     |
| <span data-ttu-id="6a65a-163">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6a65a-163">Header</span></span><br/>                   | <dl> <span data-ttu-id="6a65a-164"><dt>Wmcodecdsp. h</dt></span><span class="sxs-lookup"><span data-stu-id="6a65a-164"><dt>Wmcodecdsp.h</dt></span></span> </dl>                                                                                       |



## <a name="see-also"></a><span data-ttu-id="6a65a-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="6a65a-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6a65a-166">Filtros do DirectShow</span><span class="sxs-lookup"><span data-stu-id="6a65a-166">DirectShow Filters</span></span>](directshow-filters.md)
</dt> </dl>

 

 
