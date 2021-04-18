---
description: O decodificador de vídeo Media Foundation H. 264 é uma transformação Media Foundation que dá suporte à decodificação de perfis de linha de base, principal e alto, até o nível 5,1.
ms.assetid: 783a3618-981a-4573-9e9e-ebf5eeb75d06
title: Decodificador de vídeo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 75c4713b1a4e36d1ba085b2239c24ca0f6e4fae0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457208"
---
# <a name="h264-video-decoder"></a><span data-ttu-id="7e68f-103">Decodificador de vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="7e68f-103">H.264 Video Decoder</span></span>

<span data-ttu-id="7e68f-104">O decodificador de vídeo Media Foundation H. 264 é uma [transformação Media Foundation](media-foundation-transforms.md) que dá suporte à decodificação de perfis de linha de base, principal e alto, até o nível 5,1.</span><span class="sxs-lookup"><span data-stu-id="7e68f-104">The Media Foundation H.264 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding of Baseline, Main, and High profiles, up to level 5.1.</span></span>

<span data-ttu-id="7e68f-105">O decodificador de vídeo H. 264 expõe as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="7e68f-105">The H.264 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="7e68f-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (com suporte no Windows 8)</span><span class="sxs-lookup"><span data-stu-id="7e68f-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="7e68f-107">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="7e68f-107">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="7e68f-108">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="7e68f-108">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="7e68f-109">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="7e68f-109">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="7e68f-110">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="7e68f-110">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="7e68f-111">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="7e68f-111">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="7e68f-112">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="7e68f-112">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="7e68f-113">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="7e68f-113">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="7e68f-114">Para criar uma instância do decodificador, siga um destes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="7e68f-114">To create an instance of the decoder, do one of the following:</span></span>

-   <span data-ttu-id="7e68f-115">Chame a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="7e68f-115">Call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>
-   <span data-ttu-id="7e68f-116">Chame [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span><span class="sxs-lookup"><span data-stu-id="7e68f-116">Call [**CoCreateInstance**](/windows/win32/api/combaseapi/nf-combaseapi-cocreateinstance).</span></span> <span data-ttu-id="7e68f-117">O CLSID para o decodificador é **CLSID \_ CMSH264DecoderMFT**, declarado em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="7e68f-117">The CLSID for the decoder is **CLSID\_CMSH264DecoderMFT**, declared in wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="7e68f-118">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="7e68f-118">Input Types</span></span>

<span data-ttu-id="7e68f-119">O tipo de entrada deve conter pelo menos os dois atributos a seguir:</span><span class="sxs-lookup"><span data-stu-id="7e68f-119">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="7e68f-120">Atributo</span><span class="sxs-lookup"><span data-stu-id="7e68f-120">Attribute</span></span>                                                 | <span data-ttu-id="7e68f-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e68f-121">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e68f-122">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="7e68f-122">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="7e68f-123">**Vídeo do MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="7e68f-123">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="7e68f-124">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="7e68f-124">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="7e68f-125">[MFVideoFormat \_ H264](video-subtype-guids.md) ou MFVideoFormat de \_ H264 \_ es</span><span class="sxs-lookup"><span data-stu-id="7e68f-125">[MFVideoFormat\_H264](video-subtype-guids.md) or MFVideoFormat\_H264\_ES</span></span> |



 

<span data-ttu-id="7e68f-126">Se o tipo de entrada contiver apenas esses dois atributos, o decodificador oferecerá um tipo de saída padrão, que funciona como um espaço reservado.</span><span class="sxs-lookup"><span data-stu-id="7e68f-126">If the input type contains only these two attributes, the decoder will offer a default output type, which acts as a placeholder.</span></span> <span data-ttu-id="7e68f-127">Quando o decodificador recebe amostras de entrada suficientes para produzir um quadro de saída, ele sinaliza uma alteração de formato retornando a **\_ alteração de fluxo MF E \_ Transform \_ \_** de [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span><span class="sxs-lookup"><span data-stu-id="7e68f-127">When the decoder receives enough input samples to produce an output frame, it signals a format change by returning **MF\_E\_TRANSFORM\_STREAM\_CHANGE** from [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput).</span></span> <span data-ttu-id="7e68f-128">Consulte a documentação do **ProcessOutput** para obter detalhes sobre como lidar com alterações de formato.</span><span class="sxs-lookup"><span data-stu-id="7e68f-128">See the **ProcessOutput** documentation for details about handling format changes.</span></span>

<span data-ttu-id="7e68f-129">Para evitar uma alteração de formato inicial, forneça o máximo possível de informações no tipo de entrada, incluindo:</span><span class="sxs-lookup"><span data-stu-id="7e68f-129">To avoid an initial format change, provide as much information in the input type as possible, including:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7e68f-130">Atributo</span><span class="sxs-lookup"><span data-stu-id="7e68f-130">Attribute</span></span></th>
<th><span data-ttu-id="7e68f-131">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e68f-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e68f-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e68f-132"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="7e68f-133">Taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="7e68f-133">Frame rate.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e68f-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e68f-134"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="7e68f-135">Dimensões do quadro.</span><span class="sxs-lookup"><span data-stu-id="7e68f-135">Frame dimensions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e68f-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e68f-136"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="7e68f-137">Modo de entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="7e68f-137">Interlace mode.</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e68f-138">No vídeo H. 264, a estrutura entrelaçada pode ser alterada dinamicamente, portanto, o valor recomendado desse atributo é <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span><span class="sxs-lookup"><span data-stu-id="7e68f-138">In H.264 video, the interlace structure can change dynamically, so the recommended value of this attribute is <strong>MFVideoInterlace_MixedInterlaceOrProgressive</strong>.</span></span> <span data-ttu-id="7e68f-139">As informações de entrelaçamento na transmissão elementar do vídeo têm precedência sobre o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="7e68f-139">Interlace information in the video elementary stream takes precedence over the media type.</span></span> <span data-ttu-id="7e68f-140">Para obter mais informações, consulte <a href="video-interlacing.md">vídeo entrelaçado</a>.</span><span class="sxs-lookup"><span data-stu-id="7e68f-140">For more information, see <a href="video-interlacing.md">Video Interlacing</a>.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e68f-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="7e68f-141"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="7e68f-142">Taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="7e68f-142">Pixel aspect ratio.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7e68f-143">O tipo de entrada deve ser definido antes do tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="7e68f-143">The input type must be set before the output type.</span></span> <span data-ttu-id="7e68f-144">Até que o tipo de entrada seja definido, o método [**IMFTransform:: Setoutputtypetype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) do codificador retorna **MF \_ E \_ Transform \_ Type \_ não \_ definido**.</span><span class="sxs-lookup"><span data-stu-id="7e68f-144">Until the input type is set, the encoder's [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="7e68f-145">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="7e68f-145">Output Types</span></span>

<span data-ttu-id="7e68f-146">O decodificador dá suporte aos seguintes subtipos de saída:</span><span class="sxs-lookup"><span data-stu-id="7e68f-146">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="7e68f-147">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="7e68f-147">**MFVideoFormat\_I420**</span></span>
-   <span data-ttu-id="7e68f-148">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="7e68f-148">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="7e68f-149">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="7e68f-149">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="7e68f-150">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="7e68f-150">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="7e68f-151">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="7e68f-151">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="7e68f-152">Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="7e68f-152">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="7e68f-153">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="7e68f-153">Transform Attributes</span></span>

<span data-ttu-id="7e68f-154">O decodificador H. 264 implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="7e68f-154">The H.264 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="7e68f-155">Os aplicativos podem usar esse método para obter ou definir os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="7e68f-155">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="7e68f-156">Atributo</span><span class="sxs-lookup"><span data-stu-id="7e68f-156">Attribute</span></span>                                                                                       | <span data-ttu-id="7e68f-157">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e68f-157">Description</span></span>                                                                                |
|-------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e68f-158">CODECAPI \_ AVDecVideoAcceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="7e68f-158">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)            | <span data-ttu-id="7e68f-159">Habilita ou desabilita a aceleração de hardware.</span><span class="sxs-lookup"><span data-stu-id="7e68f-159">Enables or disables hardware acceleration.</span></span>                                                 |
| [<span data-ttu-id="7e68f-160">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="7e68f-160">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="7e68f-161">Habilita ou desabilita o modo de geração de miniatura.</span><span class="sxs-lookup"><span data-stu-id="7e68f-161">Enables or disables thumbnail generation mode.</span></span>                                             |
| [<span data-ttu-id="7e68f-162">\_Reconhecimento de \_ D3D \_ SA do MF</span><span class="sxs-lookup"><span data-stu-id="7e68f-162">MF\_SA\_D3D\_AWARE</span></span>](mf-sa-d3d-aware-attribute.md)                                             | <span data-ttu-id="7e68f-163">Indica que o decodificador dá suporte a DXVA (aceleração de vídeo do DirectX).</span><span class="sxs-lookup"><span data-stu-id="7e68f-163">Indicates that the decoder supports DirectX Video Acceleration (DXVA).</span></span> <span data-ttu-id="7e68f-164">Tratar como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="7e68f-164">Treat as read-only.</span></span> |



 

<span data-ttu-id="7e68f-165">No Windows 8, o decodificador H. 264 também oferece suporte aos seguintes atributos.</span><span class="sxs-lookup"><span data-stu-id="7e68f-165">In Windows 8, the H.264 decoder also supports the following attributes.</span></span>



| <span data-ttu-id="7e68f-166">Atributo</span><span class="sxs-lookup"><span data-stu-id="7e68f-166">Attribute</span></span>                                                                                                     | <span data-ttu-id="7e68f-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="7e68f-167">Description</span></span>                                                                                                 |
|---------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="7e68f-168">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="7e68f-168">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="7e68f-169">Habilita ou desabilita o modo de decodificação de baixa latência.</span><span class="sxs-lookup"><span data-stu-id="7e68f-169">Enables or disables low-latency decoding mode.</span></span>                                                              |
| [<span data-ttu-id="7e68f-170">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="7e68f-170">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                                         | <span data-ttu-id="7e68f-171">Define o número de threads de trabalho usados pelo decodificador.</span><span class="sxs-lookup"><span data-stu-id="7e68f-171">Sets the number of worker threads used by the decoder.</span></span>                                                      |
| [<span data-ttu-id="7e68f-172">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="7e68f-172">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)                                     | <span data-ttu-id="7e68f-173">Define a largura máxima da imagem que o decodificador aceitará como um tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="7e68f-173">Sets the maximum picture width that the decoder will accept as an input type.</span></span>                               |
| [<span data-ttu-id="7e68f-174">CODECAPI \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="7e68f-174">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)                                   | <span data-ttu-id="7e68f-175">Define a altura máxima da imagem que o decodificador aceitará como um tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="7e68f-175">Sets the maximum picture height that the decoder will accept as an input type.</span></span>                              |
| [<span data-ttu-id="7e68f-176">\_contagem de \_ \_ amostra de saída mínima \_ \_ de e/o de MF</span><span class="sxs-lookup"><span data-stu-id="7e68f-176">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                               | <span data-ttu-id="7e68f-177">Especifica o número máximo de amostras de saída.</span><span class="sxs-lookup"><span data-stu-id="7e68f-177">Specifies the maximum number of output samples.</span></span>                                                             |
| [<span data-ttu-id="7e68f-178">o \_ decodificador MFT \_ expõe os \_ \_ tipos \_ de saída na \_ \_ ordem nativa</span><span class="sxs-lookup"><span data-stu-id="7e68f-178">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="7e68f-179">Especifica se um decodificador expõe os tipos de saída IYUV/I420 (adequados para transcodificação) antes de outros formatos.</span><span class="sxs-lookup"><span data-stu-id="7e68f-179">Specifies whether a decoder exposes IYUV/I420 output types (suitable for transcoding) before other formats.</span></span> |



 

<span data-ttu-id="7e68f-180">No Windows 8, o decodificador H. 264 dá suporte à interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="7e68f-180">In Windows 8, the H.264 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="7e68f-181">Essa interface fornece uma API alternativate para definir as propriedades de codec a seguir.</span><span class="sxs-lookup"><span data-stu-id="7e68f-181">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="7e68f-182">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="7e68f-182">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="7e68f-183">CODECAPI \_ AVDecVideoAcceleration \_ H264</span><span class="sxs-lookup"><span data-stu-id="7e68f-183">CODECAPI\_AVDecVideoAcceleration\_H264</span></span>](../directshow/avdecvideoacceleration-h264-property.md)
-   [<span data-ttu-id="7e68f-184">CODECAPI \_ AVDecVideoMaxCodedHeight</span><span class="sxs-lookup"><span data-stu-id="7e68f-184">CODECAPI\_AVDecVideoMaxCodedHeight</span></span>](codecapi-avdecvideomaxcodedheight.md)
-   [<span data-ttu-id="7e68f-185">CODECAPI \_ AVDecVideoMaxCodedWidth</span><span class="sxs-lookup"><span data-stu-id="7e68f-185">CODECAPI\_AVDecVideoMaxCodedWidth</span></span>](codecapi-avdecvideomaxcodedwidth.md)
-   [<span data-ttu-id="7e68f-186">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="7e68f-186">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)

## <a name="format-constraints"></a><span data-ttu-id="7e68f-187">Restrições de formato</span><span class="sxs-lookup"><span data-stu-id="7e68f-187">Format Constraints</span></span>

<span data-ttu-id="7e68f-188">O decodificador dá suporte aos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="7e68f-188">The decoder supports the following formats:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="7e68f-189">Perfis/níveis</span><span class="sxs-lookup"><span data-stu-id="7e68f-189">Profiles/Levels</span></span></td>
<td><span data-ttu-id="7e68f-190">Perfis de linha de base, principal e alto, até o nível 5,1.</span><span class="sxs-lookup"><span data-stu-id="7e68f-190">Baseline, Main, and High profiles, up to level 5.1.</span></span> <span data-ttu-id="7e68f-191">(Consulte Especificação ITU-T H. 264 para obter detalhes.)</span><span class="sxs-lookup"><span data-stu-id="7e68f-191">(See ITU-T H.264 specification for details.)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e68f-192">Formatos de croma</span><span class="sxs-lookup"><span data-stu-id="7e68f-192">Chroma Formats</span></span></td>
<td><span data-ttu-id="7e68f-193">4:2:0 croma ou monocromático</span><span class="sxs-lookup"><span data-stu-id="7e68f-193">4:2:0 chroma or monochrome</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e68f-194">Resolução mínima</span><span class="sxs-lookup"><span data-stu-id="7e68f-194">Minimum Resolution</span></span></td>
<td><span data-ttu-id="7e68f-195">48 × 48 pixels</span><span class="sxs-lookup"><span data-stu-id="7e68f-195">48 × 48 pixels</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="7e68f-196">Resolução máxima</span><span class="sxs-lookup"><span data-stu-id="7e68f-196">Maximum Resolution</span></span></td>
<td><span data-ttu-id="7e68f-197">4096 × 2304 pixels</span><span class="sxs-lookup"><span data-stu-id="7e68f-197">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="7e68f-198">A resolução máxima garantida para a aceleração de DXVA é 1920 × 1088 pixels; em resoluções mais altas, a decodificação é feita com o DXVA, se for compatível com o hardware subjacente, caso contrário, a decodificação será feita com o software.</span><span class="sxs-lookup"><span data-stu-id="7e68f-198">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="7e68f-199">No Windows 7, a resolução máxima com suporte é de 1920 × 1088 pixels para decodificação de software e DXVA.</span><span class="sxs-lookup"><span data-stu-id="7e68f-199">In Windows 7, the maximum supported resolution is 1920 × 1088 pixels for both software and DXVA decoding.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="7e68f-200">DXVA</span><span class="sxs-lookup"><span data-stu-id="7e68f-200">DXVA</span></span></td>
<td><span data-ttu-id="7e68f-201">O decodificador oferece suporte a DXVA versão 2, mas não a DXVA versão 1.</span><span class="sxs-lookup"><span data-stu-id="7e68f-201">The decoder supports DXVA version 2, but not DXVA version 1.</span></span> <span data-ttu-id="7e68f-202">A decodificação de DXVA tem suporte apenas para fragmentado de linha de base, principal e de perfil alto compatíveis com o principal.</span><span class="sxs-lookup"><span data-stu-id="7e68f-202">DXVA decoding is supported only for Main-compatible Baseline, Main, and High profile bitstreams.</span></span> <span data-ttu-id="7e68f-203">(Fragmentado de linha de base compatíveis principal são definidos como <strong>profile_idc</strong>= 66 e <strong>constrained_set1_flag</strong>= 1.)</span><span class="sxs-lookup"><span data-stu-id="7e68f-203">(Main-compatible Baseline bitstreams are defined as <strong>profile_idc</strong>=66 and <strong>constrained_set1_flag</strong>=1.)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="7e68f-204">Os dados de entrada devem estar em conformidade com o anexo B do ISO/IEC 14496-10.</span><span class="sxs-lookup"><span data-stu-id="7e68f-204">Input data must conform to Annex B of ISO/IEC 14496-10.</span></span> <span data-ttu-id="7e68f-205">Os dados devem incluir os códigos de início.</span><span class="sxs-lookup"><span data-stu-id="7e68f-205">The data must include the start codes.</span></span> <span data-ttu-id="7e68f-206">O decodificador ignora os bytes até encontrar um conjunto de parâmetros de sequência (SPS) e um conjunto de parâmetros de imagem (PPS) válidos no fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="7e68f-206">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

<span data-ttu-id="7e68f-207">O decodificador não oferece suporte à tecnologia de refinamento de filmes.</span><span class="sxs-lookup"><span data-stu-id="7e68f-207">The decoder does not support Film Grain Technology.</span></span>

> [!Note]  
> <span data-ttu-id="7e68f-208">Uma versão anterior da documentação incorretamente afirmou que o decodificador tem suporte no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="7e68f-208">A previous version of the documentation incorrectly stated that the decoder is supported on Windows Server 2008 R2.</span></span>

 

<span data-ttu-id="7e68f-209">Se o suplemento de atualização de plataforma para Windows Vista estiver instalado, o decodificador de vídeo H. 264 estará disponível no Windows Vista, mas poderá ser acessado somente no Windows Vista usando o [leitor de origem](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="7e68f-209">If Platform Update Supplement for Windows Vista is installed, the H.264 video decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7e68f-210">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7e68f-210">Requirements</span></span>



| <span data-ttu-id="7e68f-211">Requisito</span><span class="sxs-lookup"><span data-stu-id="7e68f-211">Requirement</span></span> | <span data-ttu-id="7e68f-212">Valor</span><span class="sxs-lookup"><span data-stu-id="7e68f-212">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="7e68f-213">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e68f-213">Minimum supported client</span></span><br/> | <span data-ttu-id="7e68f-214">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="7e68f-214">Windows 7 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="7e68f-215">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="7e68f-215">Minimum supported server</span></span><br/> | <span data-ttu-id="7e68f-216">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="7e68f-216">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="7e68f-217">DLL</span><span class="sxs-lookup"><span data-stu-id="7e68f-217">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7e68f-218"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7e68f-218"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7e68f-219">Confira também</span><span class="sxs-lookup"><span data-stu-id="7e68f-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7e68f-220">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="7e68f-220">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="7e68f-221">Suporte a MPEG-4 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e68f-221">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="7e68f-222">Formatos de mídia compatíveis com o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="7e68f-222">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="7e68f-223">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="7e68f-223">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
