---
description: 'O codificador de vídeo Microsoft Media Foundation H. 264 é uma transformação Media Foundation que dá suporte aos seguintes perfis H. 264:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Codificador de vídeo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5631239e9db0ddf078848bc3c4a04282e7e79990
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771329"
---
# <a name="h264-video-encoder"></a><span data-ttu-id="cf210-103">Codificador de vídeo H. 264</span><span class="sxs-lookup"><span data-stu-id="cf210-103">H.264 Video Encoder</span></span>

<span data-ttu-id="cf210-104">O codificador de vídeo Microsoft Media Foundation H. 264 é uma [transformação Media Foundation](media-foundation-transforms.md) que dá suporte aos seguintes perfis H. 264:</span><span class="sxs-lookup"><span data-stu-id="cf210-104">The Microsoft Media Foundation H.264 video encoder is a [Media Foundation transform](media-foundation-transforms.md) that supports the following H.264 profiles:</span></span>

-   <span data-ttu-id="cf210-105">Perfil de linha de base</span><span class="sxs-lookup"><span data-stu-id="cf210-105">Baseline Profile</span></span>
-   <span data-ttu-id="cf210-106">Perfil Principal</span><span class="sxs-lookup"><span data-stu-id="cf210-106">Main Profile</span></span>
-   <span data-ttu-id="cf210-107">Perfil alto (requer o Windows 8)</span><span class="sxs-lookup"><span data-stu-id="cf210-107">High profile (requires Windows 8)</span></span>

<span data-ttu-id="cf210-108">O codificador de vídeo H. 264 expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="cf210-108">The H.264 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="cf210-109">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="cf210-109">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="cf210-110">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="cf210-110">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="cf210-111">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="cf210-111">Input Types</span></span>

<span data-ttu-id="cf210-112">O tipo de mídia de entrada deve ter um dos seguintes subtipos:</span><span class="sxs-lookup"><span data-stu-id="cf210-112">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="cf210-113">**MFVideoFormat_I420**</span><span class="sxs-lookup"><span data-stu-id="cf210-113">**MFVideoFormat_I420**</span></span>
-   <span data-ttu-id="cf210-114">**MFVideoFormat_IYUV**</span><span class="sxs-lookup"><span data-stu-id="cf210-114">**MFVideoFormat_IYUV**</span></span>
-   <span data-ttu-id="cf210-115">**MFVideoFormat_NV12**</span><span class="sxs-lookup"><span data-stu-id="cf210-115">**MFVideoFormat_NV12**</span></span>
-   <span data-ttu-id="cf210-116">**MFVideoFormat_YUY2**</span><span class="sxs-lookup"><span data-stu-id="cf210-116">**MFVideoFormat_YUY2**</span></span>
-   <span data-ttu-id="cf210-117">**MFVideoFormat_YV12**</span><span class="sxs-lookup"><span data-stu-id="cf210-117">**MFVideoFormat_YV12**</span></span>

<span data-ttu-id="cf210-118">Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="cf210-118">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="cf210-119">O tipo de saída deve ser definido antes do tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf210-119">The output type must be set before the input type.</span></span> <span data-ttu-id="cf210-120">Até que o tipo de saída seja definido, o método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) do codificador retorna **MF_E_TRANSFORM_TYPE_NOT_SET**.</span><span class="sxs-lookup"><span data-stu-id="cf210-120">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF_E_TRANSFORM_TYPE_NOT_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="cf210-121">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="cf210-121">Output Types</span></span>

<span data-ttu-id="cf210-122">O codificador dá suporte a um subtipo de saída único:</span><span class="sxs-lookup"><span data-stu-id="cf210-122">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="cf210-123">**MFVideoFormat_H264**</span><span class="sxs-lookup"><span data-stu-id="cf210-123">**MFVideoFormat_H264**</span></span>

<span data-ttu-id="cf210-124">Defina os seguintes atributos no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="cf210-124">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf210-125">Atributo</span><span class="sxs-lookup"><span data-stu-id="cf210-125">Attribute</span></span></th>
<th><span data-ttu-id="cf210-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf210-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf210-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf210-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="cf210-128">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="cf210-128">Major type.</span></span> <span data-ttu-id="cf210-129">Deve ser <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf210-129">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf210-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="cf210-131">Subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cf210-131">Video subtype.</span></span> <span data-ttu-id="cf210-132">Deve ser <strong>MFVideoFormat_H264</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf210-132">Must be <strong>MFVideoFormat_H264</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf210-133"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="cf210-134">Taxa média de bits codificada, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="cf210-134">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="cf210-135">Deve ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="cf210-135">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf210-136"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="cf210-137">Taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="cf210-137">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf210-138"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="cf210-139">Tamanho do quadro.</span><span class="sxs-lookup"><span data-stu-id="cf210-139">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf210-140"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="cf210-141">Modo de entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="cf210-141">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf210-142"><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></span></span></td>
<td><span data-ttu-id="cf210-143">Perfil de codificação H. 264.</span><span class="sxs-lookup"><span data-stu-id="cf210-143">H.264 encoding profile.</span></span><br/> <span data-ttu-id="cf210-144">Os valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="cf210-144">The supported values are:</span></span><br/>
<ul>
<li><span data-ttu-id="cf210-145"><strong>eAVEncH264VProfile_Base</strong> (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf210-145"><strong>eAVEncH264VProfile_Base</strong> (default)</span></span></li>
<li><span data-ttu-id="cf210-146"><strong>eAVEncH264VProfile_Main</strong></span><span class="sxs-lookup"><span data-stu-id="cf210-146"><strong>eAVEncH264VProfile_Main</strong></span></span></li>
<li><span data-ttu-id="cf210-147"><strong>eAVEncH264VProfile_High</strong> (requer o Windows 8)</span><span class="sxs-lookup"><span data-stu-id="cf210-147"><strong>eAVEncH264VProfile_High</strong> (requires Windows 8)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf210-148"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="cf210-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cf210-149">Optional.</span></span> <span data-ttu-id="cf210-150">Especifica o nível de codificação H. 264.</span><span class="sxs-lookup"><span data-stu-id="cf210-150">Specifies the H.264 encoding level.</span></span><br/> <span data-ttu-id="cf210-151">O valor padrão é – 1, indicando que o codificador selecionará o nível de codificação.</span><span class="sxs-lookup"><span data-stu-id="cf210-151">The default value is –1, indicating that the encoder will select the encoding level.</span></span><br/> <span data-ttu-id="cf210-152">É recomendável não definir o nível no tipo de mídia e permitir que o codificador selecione o nível.</span><span class="sxs-lookup"><span data-stu-id="cf210-152">It is recommended not to set the level in the media type, and allow the encoder to select the level.</span></span> <span data-ttu-id="cf210-153">O codificador pode derivar o nível apropriado para um determinado fluxo de vídeo, levando em conta as restrições de formato e as características do vídeo.</span><span class="sxs-lookup"><span data-stu-id="cf210-153">The encoder can derive the proper level for a given video stream, taking into account the format constraints and the characteristics of the video.</span></span> <span data-ttu-id="cf210-154">Para obter mais informações sobre restrições de perfil e de nível, consulte anexo A de ITU-T H. 264.</span><span class="sxs-lookup"><span data-stu-id="cf210-154">For more information about profile and level constraints, refer to Annex A of ITU-T H.264.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="cf210-155"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="cf210-156">Opcional.</span><span class="sxs-lookup"><span data-stu-id="cf210-156">Optional.</span></span> <span data-ttu-id="cf210-157">Especifica a taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="cf210-157">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="cf210-158">O valor padrão é 1:1.</span><span class="sxs-lookup"><span data-stu-id="cf210-158">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="cf210-159">Depois que o tipo de saída é definido, o codificador de vídeo atualiza o tipo adicionando o atributo [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="cf210-159">After the output type is set, the video encoder updates the type by adding the [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="cf210-160">Este atributo contém o cabeçalho de sequência.</span><span class="sxs-lookup"><span data-stu-id="cf210-160">This attribute contains the sequence header.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="cf210-161">Propriedades do codec</span><span class="sxs-lookup"><span data-stu-id="cf210-161">Codec Properties</span></span>

<span data-ttu-id="cf210-162">O codificador H. 264 implementa a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para definir parâmetros de codificação.</span><span class="sxs-lookup"><span data-stu-id="cf210-162">The H.264 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="cf210-163">Ele dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf210-163">It supports the following properties.</span></span>

<span data-ttu-id="cf210-164">Para obter os requisitos de codec para a certificação do codificador HCK, consulte a seção **codificador de hardware certificado** abaixo.</span><span class="sxs-lookup"><span data-stu-id="cf210-164">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>

<span data-ttu-id="cf210-165">As propriedades a seguir têm suporte no Windows 7.</span><span class="sxs-lookup"><span data-stu-id="cf210-165">The following properties are supported in Windows 7.</span></span>



| <span data-ttu-id="cf210-166">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cf210-166">Property</span></span>                                                                              | <span data-ttu-id="cf210-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf210-167">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf210-168">**CODECAPI_AVEncCommonRateControlMode**</span><span class="sxs-lookup"><span data-stu-id="cf210-168">**CODECAPI_AVEncCommonRateControlMode**</span></span>](../directshow/avenccommonratecontrolmode-property.md) | <span data-ttu-id="cf210-169">Define o modo de controle de taxa.</span><span class="sxs-lookup"><span data-stu-id="cf210-169">Sets the rate control mode.</span></span> <span data-ttu-id="cf210-170">Consulte Observações.</span><span class="sxs-lookup"><span data-stu-id="cf210-170">See Remarks.</span></span> <span data-ttu-id="cf210-171">O modo padrão é taxa de bits variável irrestrita (VBR).</span><span class="sxs-lookup"><span data-stu-id="cf210-171">The default mode is unconstrained variable bit rate (VBR).</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [<span data-ttu-id="cf210-172">**CODECAPI_AVEncCommonQuality**</span><span class="sxs-lookup"><span data-stu-id="cf210-172">**CODECAPI_AVEncCommonQuality**</span></span>](../directshow/avenccommonquality-property.md)                 | <span data-ttu-id="cf210-173">Define o nível de qualidade.</span><span class="sxs-lookup"><span data-stu-id="cf210-173">Sets the quality level.</span></span> <span data-ttu-id="cf210-174">Essa propriedade se aplica quando o modo de controle de taxa é taxa de bits baseada em qualidade (**eAVEncCommonRateControlMode_Quality**).</span><span class="sxs-lookup"><span data-stu-id="cf210-174">This property applies when the rate control mode is quality-based VBR (**eAVEncCommonRateControlMode_Quality**).</span></span> <span data-ttu-id="cf210-175">O intervalo válido é de 1 a 100.</span><span class="sxs-lookup"><span data-stu-id="cf210-175">The valid range is 1–100.</span></span> <span data-ttu-id="cf210-176">O valor padrão é 70.</span><span class="sxs-lookup"><span data-stu-id="cf210-176">The default value is 70.</span></span> <br/> <span data-ttu-id="cf210-177">Para definir esse parâmetro, defina a propriedade antes de chamar [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="cf210-177">To set this parameter, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <br/> <span data-ttu-id="cf210-178">Para definir esse parâmetro no Windows 7, defina a propriedade antes de chamar [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span><span class="sxs-lookup"><span data-stu-id="cf210-178">To set this parameter in Windows 7, set the property before calling [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype).</span></span> <span data-ttu-id="cf210-179">O codificador ignora as alterações depois que o tipo de saída é definido.</span><span class="sxs-lookup"><span data-stu-id="cf210-179">The encoder ignores changes after the output type is set.</span></span> <br/> <span data-ttu-id="cf210-180">No Windows 8, essa propriedade pode ser definida a qualquer momento durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="cf210-180">In Windows 8, this property can be set at any time during encoding.</span></span> <span data-ttu-id="cf210-181">As alterações são aplicadas começando no próximo quadro de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf210-181">Changes are applied starting at the next input frame.</span></span> <br/> <span data-ttu-id="cf210-182">Internamente, o codificador converte essa propriedade em um valor [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) .</span><span class="sxs-lookup"><span data-stu-id="cf210-182">Internally, the encoder converts this property to an [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) value.</span></span> <br/> |



 

<span data-ttu-id="cf210-183">As propriedades a seguir exigem o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cf210-183">The following properties require Windows 8.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf210-184">Propriedade</span><span class="sxs-lookup"><span data-stu-id="cf210-184">Property</span></span></th>
<th><span data-ttu-id="cf210-185">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf210-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf210-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span><span class="sxs-lookup"><span data-stu-id="cf210-186"><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></span></span></td>
<td><span data-ttu-id="cf210-187">Define o modo de codificação adaptável.</span><span class="sxs-lookup"><span data-stu-id="cf210-187">Sets the adaptive encoding mode.</span></span> <span data-ttu-id="cf210-188">O codificador H. 264 dá suporte aos seguintes modos no Windows 8:</span><span class="sxs-lookup"><span data-stu-id="cf210-188">The H.264 encoder supports the following modes in Windows 8:</span></span>
<ul>
<li><span data-ttu-id="cf210-189"><strong>eAVEncAdaptiveMode_None</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf210-189"><strong>eAVEncAdaptiveMode_None</strong>.</span></span> <span data-ttu-id="cf210-190">Sem codificação adaptável.</span><span class="sxs-lookup"><span data-stu-id="cf210-190">No adaptive encoding.</span></span> <span data-ttu-id="cf210-191">(Padrão.)</span><span class="sxs-lookup"><span data-stu-id="cf210-191">(Default.)</span></span></li>
<li><span data-ttu-id="cf210-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf210-192"><strong>eAVEncAdaptiveMode_FrameRate</strong>.</span></span> <span data-ttu-id="cf210-193">Altere adaptativamente a taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="cf210-193">Adaptively change the frame rate.</span></span></li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="cf210-194"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="cf210-195">Define o tamanho do buffer, em bytes, para a codificação de taxa de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="cf210-195">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="cf210-196">O intervalo válido é [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="cf210-196">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="cf210-197">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cf210-197">Requires Windows 8.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="cf210-198"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="cf210-199">Para a codificação de taxa de bits restrita, especifica a taxa na qual o &quot; Bucket de vazamentos &quot; é esgotado, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="cf210-199">For constrained VBR encoding, specifies the rate at which the &quot;leaky bucket&quot; is drained, in bits per second.</span></span> <span data-ttu-id="cf210-200">Essa propriedade se aplica quando o modo de controle de taxa é <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf210-200">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>.</span></span> <br/> <span data-ttu-id="cf210-201">O intervalo válido é [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="cf210-201">The valid range is [1 ... 2³²–1].</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="cf210-202"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="cf210-203">Define a taxa média de bits para o fluxo de bits codificado, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="cf210-203">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <span data-ttu-id="cf210-204">Essa propriedade será ignorada se o modo de controle de taxa for <strong>eAVEncCommonRateControlMode_Quality</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf210-204">This property is ignored if the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="cf210-205">O intervalo válido é [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="cf210-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="cf210-206">Na CBR e nos modos de VBR não restritos, a taxa média de bits determina o tamanho final do arquivo.</span><span class="sxs-lookup"><span data-stu-id="cf210-206">In CBR and unconstrained VBR modes, the average bit rate determines the final size of the file.</span></span> <span data-ttu-id="cf210-207">No modo CBR, a taxa média de bits também é a taxa na qual bits compactados são drenados do &quot; Bucket de vazamento. &quot; (para obter mais informações, consulte <a href="the-leaky-bucket-buffer-model.md">o modelo de buffer de buckets de vazamentos</a>.)</span><span class="sxs-lookup"><span data-stu-id="cf210-207">In CBR mode, the average bit rate is also the rate at which compressed bits are drained from the &quot;leaky bucket.&quot; (For more information, see <a href="the-leaky-bucket-buffer-model.md">The Leaky Bucket Buffer Model</a>.)</span></span> <br/> <span data-ttu-id="cf210-208">No Windows 7, a taxa média de bits é especificada pelo atributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="cf210-208">In Windows 7, the average bit rate is specified by the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute on the media type.</span></span> <br/> <span data-ttu-id="cf210-209">No Windows 8, você pode definir a taxa média de bits usando o atributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> ou a propriedade <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> .</span><span class="sxs-lookup"><span data-stu-id="cf210-209">In Windows 8, you can set the average bit rate using either the <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> attribute or the <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> property.</span></span> <span data-ttu-id="cf210-210">Se ambos estiverem definidos, CODECAPI_AVEncCommonMeanBitRate substituições.</span><span class="sxs-lookup"><span data-stu-id="cf210-210">If both are set, CODECAPI_AVEncCommonMeanBitRate overrides.</span></span> <span data-ttu-id="cf210-211">No Windows 8, você pode definir a taxa de bits média durante a codificação.</span><span class="sxs-lookup"><span data-stu-id="cf210-211">In Windows 8, you can set the average bit rate during encoding.</span></span> <span data-ttu-id="cf210-212">Se a taxa de bits for alterada, o codificador usará a codificação adaptável.</span><span class="sxs-lookup"><span data-stu-id="cf210-212">If the bit rate changes, the encoder uses adaptive encoding.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="cf210-213"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="cf210-214">Define a compensação de qualidade/velocidade.</span><span class="sxs-lookup"><span data-stu-id="cf210-214">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="cf210-215">Intervalo válido:</span><span class="sxs-lookup"><span data-stu-id="cf210-215">Valid range:</span></span>
<ul>
<li><span data-ttu-id="cf210-216">0 – 33: baixa complexidade</span><span class="sxs-lookup"><span data-stu-id="cf210-216">0–33: Low complexity</span></span></li>
<li><span data-ttu-id="cf210-217">34 – 66: complexidade média (padrão)</span><span class="sxs-lookup"><span data-stu-id="cf210-217">34–66: Medium complexity (default)</span></span></li>
<li><span data-ttu-id="cf210-218">67 – 100: alta complexidade</span><span class="sxs-lookup"><span data-stu-id="cf210-218">67–100: High complexity</span></span></li>
</ul>
<br/> <span data-ttu-id="cf210-219">Esse valor afeta como o codificador executa várias operações de codificação, como compensação de movimento.</span><span class="sxs-lookup"><span data-stu-id="cf210-219">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="cf210-220">Em níveis mais altos de complexidade, o codificador é executado mais lentamente, mas produz uma qualidade melhor na mesma taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="cf210-220">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span><span class="sxs-lookup"><span data-stu-id="cf210-221"><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></span></span></td>
<td><span data-ttu-id="cf210-222">Habilita ou desabilita CABAC (codificação aritmética binária de contexto) para codificação de entropia H. 264.</span><span class="sxs-lookup"><span data-stu-id="cf210-222">Enables or disables CABAC (context-adaptive binary arithmetic coding) for H.264 entropy coding.</span></span> <span data-ttu-id="cf210-223">O valor padrão é <strong>VARIANT_FALSE</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf210-223">The default value is <strong>VARIANT_FALSE</strong>.</span></span> <br/> <span data-ttu-id="cf210-224">CABAC não é usado para o perfil de linha de base.</span><span class="sxs-lookup"><span data-stu-id="cf210-224">CABAC is not used for Baseline profile.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span><span class="sxs-lookup"><span data-stu-id="cf210-225"><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></span></span></td>
<td><span data-ttu-id="cf210-226">Define o valor de <strong>seq_parameter_set_id</strong> na unidade de nal do SPS do H. 264 fragmentado.</span><span class="sxs-lookup"><span data-stu-id="cf210-226">Sets the value of <strong>seq_parameter_set_id</strong> in the SPS NAL unit of the H.264 bitstream.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span><span class="sxs-lookup"><span data-stu-id="cf210-227"><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></span></span></td>
<td><span data-ttu-id="cf210-228">Define o número máximo de quadros B consecutivos no fragmentado de saída.</span><span class="sxs-lookup"><span data-stu-id="cf210-228">Sets the maximum number of consecutive B frames in the output bitstream.</span></span> <span data-ttu-id="cf210-229">Os valores válidos são:</span><span class="sxs-lookup"><span data-stu-id="cf210-229">Valid values are:</span></span>
<ul>
<li><span data-ttu-id="cf210-230">0: não use quadros B (padrão).</span><span class="sxs-lookup"><span data-stu-id="cf210-230">0: Do not use B frames (default).</span></span></li>
<li><span data-ttu-id="cf210-231">1: usar um quadro B.</span><span class="sxs-lookup"><span data-stu-id="cf210-231">1: Use one B frame.</span></span></li>
<li><span data-ttu-id="cf210-232">2: usar dois quadros B.</span><span class="sxs-lookup"><span data-stu-id="cf210-232">2: Use two B frames.</span></span></li>
</ul>
<span data-ttu-id="cf210-233">Para definir esse parâmetro, defina a propriedade antes de chamar <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform:: SetOutputType</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf210-233">To set this parameter, set the property before calling <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform::SetOutputType</strong></a>.</span></span> <br/> <span data-ttu-id="cf210-234">Para o perfil de linha de base, o número de quadros B é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="cf210-234">For Baseline profile, the number of B frames is always zero.</span></span> <span data-ttu-id="cf210-235">O codificador substituirá valores diferentes de zero.</span><span class="sxs-lookup"><span data-stu-id="cf210-235">The encoder will override nonzero values.</span></span><br/> <span data-ttu-id="cf210-236">Para outros perfis H. 264, se essa propriedade for diferente de zero, o padrão de codificação será IBBPBBP, em que o número máximo de quadros B consecutivos será igual a <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span><span class="sxs-lookup"><span data-stu-id="cf210-236">For other H.264 profiles, if this property is nonzero, the encoding pattern is IBBPBBP, where the maximum number of consecutive B frames is equal to <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="cf210-237"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="cf210-238">Define o número de imagens de um cabeçalho GOP para o seguinte, incluindo a âncora à esquerda, mas não o seguinte.</span><span class="sxs-lookup"><span data-stu-id="cf210-238">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="cf210-239">O intervalo válido é [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="cf210-239">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="cf210-240">Se for zero, o codificador selecionará o tamanho de GOP.</span><span class="sxs-lookup"><span data-stu-id="cf210-240">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="cf210-241">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="cf210-241">The default value is zero.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="cf210-242"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="cf210-243">Define o número de threads de trabalho usados por um codificador.</span><span class="sxs-lookup"><span data-stu-id="cf210-243">Sets the number of worker threads used by a encoder.</span></span><br/> <span data-ttu-id="cf210-244">O intervalo válido é de 0 a 16.</span><span class="sxs-lookup"><span data-stu-id="cf210-244">The valid range is 0–16.</span></span> <span data-ttu-id="cf210-245">Se for zero, o codificador selecionará o número de threads.</span><span class="sxs-lookup"><span data-stu-id="cf210-245">If zero, the encoder selects the number of threads.</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span><span class="sxs-lookup"><span data-stu-id="cf210-246"><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></span></span></td>
<td><span data-ttu-id="cf210-247">Indica o tipo de conteúdo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="cf210-247">Indicates the type of video content.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="cf210-248"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="cf210-249">Intervalo válido: 16 a 51.</span><span class="sxs-lookup"><span data-stu-id="cf210-249">Valid range: 16–51.</span></span> <span data-ttu-id="cf210-250">O valor padrão é 24.</span><span class="sxs-lookup"><span data-stu-id="cf210-250">The default value is 24.</span></span> <br/> <span data-ttu-id="cf210-251">Essa propriedade se aplica quando o modo de controle de taxa é <strong>eAVEncCommonRateControlMode_Quality</strong>.</span><span class="sxs-lookup"><span data-stu-id="cf210-251">This property applies when the rate control mode is <strong>eAVEncCommonRateControlMode_Quality</strong>.</span></span> <br/> <span data-ttu-id="cf210-252">Essa propriedade define a mesma configuração de codificação que <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="cf210-252">This property configures the same encoding setting as <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>.</span></span> <span data-ttu-id="cf210-253">No entanto, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> permite que o aplicativo especifique o valor de QP diretamente.</span><span class="sxs-lookup"><span data-stu-id="cf210-253">However, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> enables the application to specify the value of QP directly.</span></span> <span data-ttu-id="cf210-254">Se ambas as propriedades forem definidas, AVEncVideoEncodeQP substituições.</span><span class="sxs-lookup"><span data-stu-id="cf210-254">If both properties are set, AVEncVideoEncodeQP overrides.</span></span> <br/> <span data-ttu-id="cf210-255">O valor padrão de 24 corresponde ao valor padrão de 70 para a configuração <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="cf210-255">The default value of 24 corresponds to the default value of 70 for the <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> setting.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="cf210-256"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="cf210-257">Força o codificador a codificar o próximo quadro como um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="cf210-257">Forces the encoder to code the next frame as a key frame.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf210-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="cf210-258"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="cf210-259">Intervalo válido: 0 – 51.</span><span class="sxs-lookup"><span data-stu-id="cf210-259">Valid range: 0–51.</span></span> <span data-ttu-id="cf210-260">O valor padrão é 0.</span><span class="sxs-lookup"><span data-stu-id="cf210-260">The default value is 0.</span></span> <br/> <span data-ttu-id="cf210-261">Essa propriedade se aplica a todos os modos de controle de taxa.</span><span class="sxs-lookup"><span data-stu-id="cf210-261">This property applies to all rate control modes.</span></span> <span data-ttu-id="cf210-262">O codificador não deve produzir um valor de QP menor do que o especificado pela propriedade <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .</span><span class="sxs-lookup"><span data-stu-id="cf210-262">The encoder should not produce a QP value lower than what is specified by the <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> property.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="cf210-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="cf210-263"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="cf210-264">Habilita ou desabilita o modo de baixa latência.</span><span class="sxs-lookup"><span data-stu-id="cf210-264">Enables or disables low-latency mode.</span></span> <span data-ttu-id="cf210-265">Consulte &quot; multithreading &quot; na seção comentários.</span><span class="sxs-lookup"><span data-stu-id="cf210-265">See &quot;Multithreading&quot; in the Remarks section.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a><span data-ttu-id="cf210-266">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf210-266">Remarks</span></span>

<span data-ttu-id="cf210-267">O codificador dá suporte aos modos de controle de taxa a seguir.</span><span class="sxs-lookup"><span data-stu-id="cf210-267">The encoder supports the following rate control modes.</span></span>



| <span data-ttu-id="cf210-268">Mode</span><span class="sxs-lookup"><span data-stu-id="cf210-268">Mode</span></span>                                  | <span data-ttu-id="cf210-269">Constante</span><span class="sxs-lookup"><span data-stu-id="cf210-269">Constant</span></span>                                            | <span data-ttu-id="cf210-270">Descrição</span><span class="sxs-lookup"><span data-stu-id="cf210-270">Description</span></span>                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf210-271">Taxa de bits constante (CBR)</span><span class="sxs-lookup"><span data-stu-id="cf210-271">Constant bit rate (CBR)</span></span>               | <span data-ttu-id="cf210-272">**eAVEncCommonRateControlMode_CBR**</span><span class="sxs-lookup"><span data-stu-id="cf210-272">**eAVEncCommonRateControlMode_CBR**</span></span>                | <span data-ttu-id="cf210-273">O codificador tenta atingir uma taxa de bits constante, usando um modelo de "Bucket de vazamentos".</span><span class="sxs-lookup"><span data-stu-id="cf210-273">The encoder tries to achieve a constant bit rate, using a "leaky bucket" model.</span></span> <span data-ttu-id="cf210-274">A taxa de bits de destino é fornecida pela propriedade [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="cf210-274">The target bit rate is given by the [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="cf210-275">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cf210-275">Requires Windows 8.</span></span> <br/> |
| <span data-ttu-id="cf210-276">Taxa de bits de variável restrita (VBR)</span><span class="sxs-lookup"><span data-stu-id="cf210-276">Constrained variable bit rate (VBR)</span></span>   | <span data-ttu-id="cf210-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="cf210-277">**eAVEncCommonRateControlMode_PeakConstrainedVBR**</span></span> | <span data-ttu-id="cf210-278">O codificador usa um modelo de "Bucket de vazamentos" com uma taxa de bits de pico.</span><span class="sxs-lookup"><span data-stu-id="cf210-278">The encoder uses a "leaky bucket" model with a peak bit rate.</span></span> <span data-ttu-id="cf210-279">A taxa de descarga para o Bucket de vazamento é fornecida pela propriedade [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="cf210-279">The drain rate for the leaky bucket is given by the [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) property.</span></span> <br/> <span data-ttu-id="cf210-280">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cf210-280">Requires Windows 8.</span></span> <br/>     |
| <span data-ttu-id="cf210-281">Taxa de bits variável baseada em qualidade (VBR)</span><span class="sxs-lookup"><span data-stu-id="cf210-281">Quality-based variable bit rate (VBR)</span></span> | <span data-ttu-id="cf210-282">**eAVEncCommonRateControlMode_Quality**</span><span class="sxs-lookup"><span data-stu-id="cf210-282">**eAVEncCommonRateControlMode_Quality**</span></span>            | <span data-ttu-id="cf210-283">O codificador tenta atingir um nível de qualidade constante, fornecido pela propriedade [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) .</span><span class="sxs-lookup"><span data-stu-id="cf210-283">The encoder tries to achieve a constant quality level, given by the [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) property.</span></span>                                                                                                           |
| <span data-ttu-id="cf210-284">VBR não restringida</span><span class="sxs-lookup"><span data-stu-id="cf210-284">Unconstrained VBR</span></span>                     | <span data-ttu-id="cf210-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span><span class="sxs-lookup"><span data-stu-id="cf210-285">**eAVEncCommonRateControlMode_UnconstrainedVBR**</span></span>   | <span data-ttu-id="cf210-286">O codificador tenta atingir a taxa de bits de destino fornecida pelo atributo [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="cf210-286">The encoder tries to achieve the target bitrate given by the [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) attribute in the output media type.</span></span> <span data-ttu-id="cf210-287">Esse é o modo padrão.</span><span class="sxs-lookup"><span data-stu-id="cf210-287">This is the default mode.</span></span>                                                              |



 

<span data-ttu-id="cf210-288">Os modos de CBR e VBR restrita exigem o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="cf210-288">CBR and constrained VBR modes require Windows 8.</span></span>

<span data-ttu-id="cf210-289">No Windows 8, o codificador define os seguintes atributos nos exemplos de saída:</span><span class="sxs-lookup"><span data-stu-id="cf210-289">In Windows 8, the encoder sets the following attributes on the output samples:</span></span>

-   [<span data-ttu-id="cf210-290">MFSampleExtension_DecodeTimestamp</span><span class="sxs-lookup"><span data-stu-id="cf210-290">MFSampleExtension_DecodeTimestamp</span></span>](mfsampleextension-decodetimestamp.md)
-   [<span data-ttu-id="cf210-291">MFSampleExtension_VideoEncodePictureType</span><span class="sxs-lookup"><span data-stu-id="cf210-291">MFSampleExtension_VideoEncodePictureType</span></span>](mfsampleextension-videoencodepicturetype.md)
-   [<span data-ttu-id="cf210-292">MFSampleExtension_VideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="cf210-292">MFSampleExtension_VideoEncodeQP</span></span>](mfsampleextension-videoencodeqp.md)

> [!Note]  
> <span data-ttu-id="cf210-293">Uma versão anterior da documentação declarava incorretamente que o codificador tem suporte no Windows Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="cf210-293">A previous version of the documentation incorrectly stated that the encoder is supported on Windows Server 2008 R2.</span></span>

 

### <a name="multithreading"></a><span data-ttu-id="cf210-294">Multithreading</span><span class="sxs-lookup"><span data-stu-id="cf210-294">Multithreading</span></span>

<span data-ttu-id="cf210-295">No Windows 8, o codificador dá suporte a dois modos de codificação:</span><span class="sxs-lookup"><span data-stu-id="cf210-295">In Windows 8, the encoder supports two encoding modes:</span></span>

-   <span data-ttu-id="cf210-296">**Codificação de fatia.**</span><span class="sxs-lookup"><span data-stu-id="cf210-296">**Slice encoding.**</span></span> <span data-ttu-id="cf210-297">Nesse modo, as fatias são codificadas em paralelo.</span><span class="sxs-lookup"><span data-stu-id="cf210-297">In this mode, slices are encoded in parallel.</span></span> <span data-ttu-id="cf210-298">Cada fatia é codificada em um thread diferente.</span><span class="sxs-lookup"><span data-stu-id="cf210-298">Each slice is encoded on a different thread.</span></span> <span data-ttu-id="cf210-299">Esse modo tem baixa latência, pois uma única imagem é codificada em paralelo.</span><span class="sxs-lookup"><span data-stu-id="cf210-299">This mode has low latency, because a single picture is encoded in parallel.</span></span> <span data-ttu-id="cf210-300">No entanto, essa abordagem não é dimensionada conforme o número de núcleos aumenta, pois o número de fatias é limitado pelo número de linhas macrobloco na imagem de entrada.</span><span class="sxs-lookup"><span data-stu-id="cf210-300">However, this approach does not scale as the number of cores increases, because the number of slices is bounded by the number of macroblock rows in the input picture.</span></span>
-   <span data-ttu-id="cf210-301">**Codificação de vários quadros.**</span><span class="sxs-lookup"><span data-stu-id="cf210-301">**Multi-frame encoding.**</span></span> <span data-ttu-id="cf210-302">Nesse modo, o codificador aceita vários quadros de entrada e os codifica em paralelo.</span><span class="sxs-lookup"><span data-stu-id="cf210-302">In this mode, the encoder accepts multiple frames of input and encodes them in parallel.</span></span> <span data-ttu-id="cf210-303">Esse modo escala melhor em um ambiente de vários núcleos, mas apresenta mais latência.</span><span class="sxs-lookup"><span data-stu-id="cf210-303">This mode scales better in a multicore environment, but introduces more latency.</span></span>

<span data-ttu-id="cf210-304">O codificador usa como padrão a codificação de fatia para minimizar a latência.</span><span class="sxs-lookup"><span data-stu-id="cf210-304">The encoder defaults to slice encoding, to minimize latency.</span></span> <span data-ttu-id="cf210-305">Para habilitar a codificação de vários quadros, defina a propriedade [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) como **VARIANT_FALSE**.</span><span class="sxs-lookup"><span data-stu-id="cf210-305">To enable multi-frame encoding, set the [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) property to **VARIANT_FALSE**.</span></span>

<span data-ttu-id="cf210-306">Para definir o número de threads de trabalho usados pelo codificador, defina a propriedade [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .</span><span class="sxs-lookup"><span data-stu-id="cf210-306">To set the number of worker threads used by the encoder, set the [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) property.</span></span>

<span data-ttu-id="cf210-307">No Windows 7, o codificador sempre usa a codificação de fatia.</span><span class="sxs-lookup"><span data-stu-id="cf210-307">In Windows 7, the encoder always uses slice encoding.</span></span>

### <a name="certified-hardware-encoder"></a><span data-ttu-id="cf210-308">Codificador de hardware certificado</span><span class="sxs-lookup"><span data-stu-id="cf210-308">Certified Hardware Encoder</span></span>

<span data-ttu-id="cf210-309">Se um codificador de hardware certificado estiver presente, ele geralmente será usado em vez do codificador do sistema da caixa de entrada para Media Foundation cenários relacionados.</span><span class="sxs-lookup"><span data-stu-id="cf210-309">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="cf210-310">Os codificadores certificados são necessários para dar suporte a um determinado conjunto de propriedades **ICodecAPI** e, opcionalmente, podem dar suporte a outro conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="cf210-310">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="cf210-311">O processo de certificação deve garantir que as propriedades necessárias tenham suporte adequado e, se houver suporte para uma propriedade opcional, que também tenha suporte adequado.</span><span class="sxs-lookup"><span data-stu-id="cf210-311">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="cf210-312">Veja a seguir o conjunto de propriedades obrigatórias e opcionais do **ICodecAPI** para que os codificadores passem a certificação do codificador HCK.</span><span class="sxs-lookup"><span data-stu-id="cf210-312">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

<span data-ttu-id="cf210-313">As seguintes propriedades do Windows 8 e Windows 8.1 **ICodecAPI** são necessárias:</span><span class="sxs-lookup"><span data-stu-id="cf210-313">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are required:</span></span>

-   [<span data-ttu-id="cf210-314">CODECAPI_AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="cf210-314">CODECAPI_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="cf210-315">CODECAPI_AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="cf210-315">CODECAPI_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="cf210-316">CODECAPI_AVEncCommonQualityVsSpeed</span><span class="sxs-lookup"><span data-stu-id="cf210-316">CODECAPI_AVEncCommonQualityVsSpeed</span></span>](../directshow/avenccommonqualityvsspeed-property.md)
-   [<span data-ttu-id="cf210-317">CODECAPI_AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="cf210-317">CODECAPI_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="cf210-318">CODECAPI_AVEncCommonMaxBitRate</span><span class="sxs-lookup"><span data-stu-id="cf210-318">CODECAPI_AVEncCommonMaxBitRate</span></span>](../directshow/avenccommonmaxbitrate-property.md)
-   [<span data-ttu-id="cf210-319">CODECAPI_AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="cf210-319">CODECAPI_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="cf210-320">CODECAPI_AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="cf210-320">CODECAPI_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="cf210-321">CODECAPI_AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="cf210-321">CODECAPI_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="cf210-322">CODECAPI_AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="cf210-322">CODECAPI_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

<span data-ttu-id="cf210-323">As seguintes Windows 8.1 propriedades **ICodecAPI** são opcionais, mas são testadas em HCK, se houver suporte.</span><span class="sxs-lookup"><span data-stu-id="cf210-323">The following Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   [<span data-ttu-id="cf210-324">CODECAPI_AVEncVideoMinQP</span><span class="sxs-lookup"><span data-stu-id="cf210-324">CODECAPI_AVEncVideoMinQP</span></span>](codecapi-avencvideominqp.md)
-   [<span data-ttu-id="cf210-325">CODECAPI_AVEncVideoLTRBufferControl</span><span class="sxs-lookup"><span data-stu-id="cf210-325">CODECAPI_AVEncVideoLTRBufferControl</span></span>](codecapi-avencvideoltrbuffercontrol.md)
-   [<span data-ttu-id="cf210-326">CODECAPI_AVEncVideoMarkLTRFrame</span><span class="sxs-lookup"><span data-stu-id="cf210-326">CODECAPI_AVEncVideoMarkLTRFrame</span></span>](codecapi-avencvideomarkltrframe.md)
-   [<span data-ttu-id="cf210-327">CODECAPI_AVEncVideoUseLTRFrame</span><span class="sxs-lookup"><span data-stu-id="cf210-327">CODECAPI_AVEncVideoUseLTRFrame</span></span>](codecapi-avencvideouseltrframe.md)
-   [<span data-ttu-id="cf210-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span><span class="sxs-lookup"><span data-stu-id="cf210-328">CODECAPI_AVEncVideoEncodeFrameTypeQP</span></span>](codecapi-avencvideoencodeframetypeqp.md)
-   [<span data-ttu-id="cf210-329">CODECAPI_AVEncSliceControlMode</span><span class="sxs-lookup"><span data-stu-id="cf210-329">CODECAPI_AVEncSliceControlMode</span></span>](codecapi-avencslicecontrolmode.md)
-   [<span data-ttu-id="cf210-330">CODECAPI_AVEncSliceControlSize</span><span class="sxs-lookup"><span data-stu-id="cf210-330">CODECAPI_AVEncSliceControlSize</span></span>](codecapi-avencslicecontrolsize.md)
-   [<span data-ttu-id="cf210-331">CODECAPI_AVEncVideoMaxNumRefFrame</span><span class="sxs-lookup"><span data-stu-id="cf210-331">CODECAPI_AVEncVideoMaxNumRefFrame</span></span>](codecapi-avencvideomaxnumrefframe.md)
-   [<span data-ttu-id="cf210-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span><span class="sxs-lookup"><span data-stu-id="cf210-332">CODECAPI_AVEncVideoMeanAbsoluteDifference</span></span>](codecapi-avencvideomeanabsolutedifference.md)
-   [<span data-ttu-id="cf210-333">CODECAPI_AVEncVideoMaxQP</span><span class="sxs-lookup"><span data-stu-id="cf210-333">CODECAPI_AVEncVideoMaxQP</span></span>](codecapi-avencvideomaxqp.md)
-   [<span data-ttu-id="cf210-334">CODECAPI_AVEncVideoROIEnabled</span><span class="sxs-lookup"><span data-stu-id="cf210-334">CODECAPI_AVEncVideoROIEnabled</span></span>](codecapi-avencvideoroienabled.md)
-   <span data-ttu-id="cf210-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dinâmico)</span><span class="sxs-lookup"><span data-stu-id="cf210-335">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Dynamic)</span></span>
-   [<span data-ttu-id="cf210-336">CODECAPI_AVEncH264CABACEnable</span><span class="sxs-lookup"><span data-stu-id="cf210-336">CODECAPI_AVEncH264CABACEnable</span></span>](codecapi-avench264cabacenable.md)

<span data-ttu-id="cf210-337">As seguintes propriedades do Windows 8 e Windows 8.1 **ICodecAPI** são opcionais, mas são testadas em HCK, se houver suporte.</span><span class="sxs-lookup"><span data-stu-id="cf210-337">The following Windows 8 and Windows 8.1 **ICodecAPI** properties are optional, but are tested in HCK if supported.</span></span>

-   <span data-ttu-id="cf210-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (estático)</span><span class="sxs-lookup"><span data-stu-id="cf210-338">[CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Static)</span></span>
-   [<span data-ttu-id="cf210-339">CODECAPI_AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="cf210-339">CODECAPI_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

<span data-ttu-id="cf210-340">As propriedades **ICodecAPI** a seguir são opcionais.</span><span class="sxs-lookup"><span data-stu-id="cf210-340">The following **ICodecAPI** properties are optional.</span></span> <span data-ttu-id="cf210-341">Eles não são testados em HCK.</span><span class="sxs-lookup"><span data-stu-id="cf210-341">They are not tested in HCK.</span></span>

-   [<span data-ttu-id="cf210-342">CODECAPI_AVEncMPVDefaultBPictureCount</span><span class="sxs-lookup"><span data-stu-id="cf210-342">CODECAPI_AVEncMPVDefaultBPictureCount</span></span>](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a><span data-ttu-id="cf210-343">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cf210-343">Requirements</span></span>



| <span data-ttu-id="cf210-344">Requisito</span><span class="sxs-lookup"><span data-stu-id="cf210-344">Requirement</span></span> | <span data-ttu-id="cf210-345">Valor</span><span class="sxs-lookup"><span data-stu-id="cf210-345">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="cf210-346">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf210-346">Minimum supported client</span></span><br/> | <span data-ttu-id="cf210-347">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="cf210-347">Windows 7 \[desktop apps only\]</span></span><br/>                                               |
| <span data-ttu-id="cf210-348">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="cf210-348">Minimum supported server</span></span><br/> | <span data-ttu-id="cf210-349">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="cf210-349">None supported</span></span><br/>                                                                |
| <span data-ttu-id="cf210-350">DLL</span><span class="sxs-lookup"><span data-stu-id="cf210-350">DLL</span></span><br/>                      | <dl> <span data-ttu-id="cf210-351"><dt>Mfh264enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="cf210-351"><dt>Mfh264enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cf210-352">Confira também</span><span class="sxs-lookup"><span data-stu-id="cf210-352">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cf210-353">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="cf210-353">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="cf210-354">Suporte a MPEG-4 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cf210-354">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="cf210-355">Formatos de mídia compatíveis com o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="cf210-355">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="cf210-356">Tipos de mídia de vídeo</span><span class="sxs-lookup"><span data-stu-id="cf210-356">Video Media Types</span></span>](video-media-types.md)
</dt> </dl>

 

 
