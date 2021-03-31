---
description: O codificador de vídeo Media Foundation H. 265 é uma transformação Media Foundation que dá suporte à codificação de conteúdo no formato H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: Codificador de vídeo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921174"
---
# <a name="h265--hevc-video-encoder"></a><span data-ttu-id="82d11-103">Codificador de vídeo H. 265/HEVC</span><span class="sxs-lookup"><span data-stu-id="82d11-103">H.265 / HEVC Video Encoder</span></span>

<span data-ttu-id="82d11-104">O codificador de vídeo Media Foundation H. 265 é uma [transformação Media Foundation](media-foundation-transforms.md) que dá suporte à codificação de conteúdo no formato H. 265/HEVC.</span><span class="sxs-lookup"><span data-stu-id="82d11-104">The Media Foundation H.265 video encoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports encoding content into the H.265/HEVC format.</span></span> <span data-ttu-id="82d11-105">O codificador dá suporte aos seguintes perfis:</span><span class="sxs-lookup"><span data-stu-id="82d11-105">The encoder supports the following profiles:</span></span>

-   <span data-ttu-id="82d11-106">Perfil Principal</span><span class="sxs-lookup"><span data-stu-id="82d11-106">Main Profile</span></span>

<span data-ttu-id="82d11-107">O codificador de vídeo H. 265 expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="82d11-107">The H.265 video encoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="82d11-108">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="82d11-108">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="82d11-109">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="82d11-109">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a><span data-ttu-id="82d11-110">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="82d11-110">Input Types</span></span>

<span data-ttu-id="82d11-111">O tipo de mídia de entrada deve ter um dos seguintes subtipos:</span><span class="sxs-lookup"><span data-stu-id="82d11-111">The input media type must have one of the following subtypes:</span></span>

-   <span data-ttu-id="82d11-112">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="82d11-112">**MFVideoFormat\_IYUV**</span></span>
-   <span data-ttu-id="82d11-113">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="82d11-113">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="82d11-114">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="82d11-114">**MFVideoFormat\_YUY2**</span></span>
-   <span data-ttu-id="82d11-115">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="82d11-115">**MFVideoFormat\_YV12**</span></span>

<span data-ttu-id="82d11-116">Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="82d11-116">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

<span data-ttu-id="82d11-117">O tipo de saída deve ser definido antes do tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="82d11-117">The output type must be set before the input type.</span></span> <span data-ttu-id="82d11-118">Até que o tipo de saída seja definido, o método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) do codificador retorna **MF \_ E \_ Transform \_ Type \_ não \_ definido**.</span><span class="sxs-lookup"><span data-stu-id="82d11-118">Until the output type is set, the encoder's [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) method returns **MF\_E\_TRANSFORM\_TYPE\_NOT\_SET**.</span></span>

## <a name="output-types"></a><span data-ttu-id="82d11-119">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="82d11-119">Output Types</span></span>

<span data-ttu-id="82d11-120">O codificador dá suporte a um subtipo de saída único:</span><span class="sxs-lookup"><span data-stu-id="82d11-120">The encoder supports a single output subtype:</span></span>

-   <span data-ttu-id="82d11-121">**MFVideoFormat \_ H265**</span><span class="sxs-lookup"><span data-stu-id="82d11-121">**MFVideoFormat\_H265**</span></span>

<span data-ttu-id="82d11-122">Defina os seguintes atributos no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="82d11-122">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82d11-123">Atributo</span><span class="sxs-lookup"><span data-stu-id="82d11-123">Attribute</span></span></th>
<th><span data-ttu-id="82d11-124">Descrição</span><span class="sxs-lookup"><span data-stu-id="82d11-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82d11-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="82d11-125"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="82d11-126">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="82d11-126">Major type.</span></span> <span data-ttu-id="82d11-127">Deve ser <strong>MFMediaType_Video</strong>.</span><span class="sxs-lookup"><span data-stu-id="82d11-127">Must be <strong>MFMediaType_Video</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="82d11-128"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="82d11-129">Subtipo de vídeo.</span><span class="sxs-lookup"><span data-stu-id="82d11-129">Video subtype.</span></span> <span data-ttu-id="82d11-130">Deve ser <strong>MFVideoFormat_HEVC</strong>.</span><span class="sxs-lookup"><span data-stu-id="82d11-130">Must be <strong>MFVideoFormat_HEVC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="82d11-131"><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></span></span></td>
<td><span data-ttu-id="82d11-132">Taxa média de bits codificada, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="82d11-132">Average encoded bit rate, in bits per second.</span></span> <span data-ttu-id="82d11-133">Deve ser maior que zero.</span><span class="sxs-lookup"><span data-stu-id="82d11-133">Must be greater than zero.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span><span class="sxs-lookup"><span data-stu-id="82d11-134"><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></span></span></td>
<td><span data-ttu-id="82d11-135">Taxa de quadros.</span><span class="sxs-lookup"><span data-stu-id="82d11-135">Frame rate.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span><span class="sxs-lookup"><span data-stu-id="82d11-136"><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></span></span></td>
<td><span data-ttu-id="82d11-137">Tamanho do quadro.</span><span class="sxs-lookup"><span data-stu-id="82d11-137">Frame size.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span><span class="sxs-lookup"><span data-stu-id="82d11-138"><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></span></span></td>
<td><span data-ttu-id="82d11-139">Modo de entrelaçamento.</span><span class="sxs-lookup"><span data-stu-id="82d11-139">Interlace mode.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span><span class="sxs-lookup"><span data-stu-id="82d11-140"><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></span></span></td>
<td><span data-ttu-id="82d11-141">Perfil de codificação H. 265.</span><span class="sxs-lookup"><span data-stu-id="82d11-141">H.265 encoding profile.</span></span><br/> <span data-ttu-id="82d11-142">Os valores com suporte são:</span><span class="sxs-lookup"><span data-stu-id="82d11-142">The supported values are:</span></span> <br/>
<ul>
<li><span data-ttu-id="82d11-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span><span class="sxs-lookup"><span data-stu-id="82d11-143"><strong>eAVEncH265VProfile_Main_420_8</strong></span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span><span class="sxs-lookup"><span data-stu-id="82d11-144"><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></span></span></td>
<td><span data-ttu-id="82d11-145">Especifica o nível do vídeo codificado.</span><span class="sxs-lookup"><span data-stu-id="82d11-145">Specifies the level of the coded video.</span></span> <span data-ttu-id="82d11-146">Para obter mais informações sobre restrições de perfil e de nível, consulte anexo A de ITU-T H. 265.</span><span class="sxs-lookup"><span data-stu-id="82d11-146">For more information about profile and level constraints, refer to Annex A of ITU-T H.265.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span><span class="sxs-lookup"><span data-stu-id="82d11-147"><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></span></span></td>
<td><span data-ttu-id="82d11-148">Opcional.</span><span class="sxs-lookup"><span data-stu-id="82d11-148">Optional.</span></span> <span data-ttu-id="82d11-149">Especifica a taxa de proporção de pixel.</span><span class="sxs-lookup"><span data-stu-id="82d11-149">Specifies the pixel aspect ratio.</span></span> <span data-ttu-id="82d11-150">O valor padrão é 1:1.</span><span class="sxs-lookup"><span data-stu-id="82d11-150">The default value is 1:1.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="82d11-151">Depois que o tipo de saída é definido, o codificador de vídeo atualiza o tipo adicionando o atributo de [**\_ cabeçalho de sequência MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="82d11-151">After the output type is set, the video encoder updates the type by adding the [**MF\_MT\_MPEG\_SEQUENCE\_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) attribute.</span></span> <span data-ttu-id="82d11-152">Este atributo contém o cabeçalho de sequência.</span><span class="sxs-lookup"><span data-stu-id="82d11-152">This attribute contains the sequence header.</span></span>

## <a name="supported-imftransform-methods"></a><span data-ttu-id="82d11-153">Métodos IMFTransform com suporte</span><span class="sxs-lookup"><span data-stu-id="82d11-153">Supported IMFTransform methods</span></span>

<span data-ttu-id="82d11-154">Os métodos a seguir da interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) têm suporte para o codificador H. 265/HEVC:</span><span class="sxs-lookup"><span data-stu-id="82d11-154">The following methods of the [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="82d11-155">**Falha GetAttributes**</span><span class="sxs-lookup"><span data-stu-id="82d11-155">**GetAttributes**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [<span data-ttu-id="82d11-156">**GetInputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="82d11-156">**GetInputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [<span data-ttu-id="82d11-157">**GetInputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="82d11-157">**GetInputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [<span data-ttu-id="82d11-158">**GetInputStatus**</span><span class="sxs-lookup"><span data-stu-id="82d11-158">**GetInputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [<span data-ttu-id="82d11-159">**GetInputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="82d11-159">**GetInputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [<span data-ttu-id="82d11-160">**GetOutputAvailableType**</span><span class="sxs-lookup"><span data-stu-id="82d11-160">**GetOutputAvailableType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [<span data-ttu-id="82d11-161">**GetOutputCurrentType**</span><span class="sxs-lookup"><span data-stu-id="82d11-161">**GetOutputCurrentType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [<span data-ttu-id="82d11-162">**GetOutputStatus**</span><span class="sxs-lookup"><span data-stu-id="82d11-162">**GetOutputStatus**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [<span data-ttu-id="82d11-163">**GetOutputStreamInfo**</span><span class="sxs-lookup"><span data-stu-id="82d11-163">**GetOutputStreamInfo**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [<span data-ttu-id="82d11-164">**GetStreamCount**</span><span class="sxs-lookup"><span data-stu-id="82d11-164">**GetStreamCount**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [<span data-ttu-id="82d11-165">**GetStreamLimits**</span><span class="sxs-lookup"><span data-stu-id="82d11-165">**GetStreamLimits**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [<span data-ttu-id="82d11-166">**ProcessEvent**</span><span class="sxs-lookup"><span data-stu-id="82d11-166">**ProcessEvent**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [<span data-ttu-id="82d11-167">**ProcessMessage**</span><span class="sxs-lookup"><span data-stu-id="82d11-167">**ProcessMessage**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [<span data-ttu-id="82d11-168">**ProcessInput**</span><span class="sxs-lookup"><span data-stu-id="82d11-168">**ProcessInput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [<span data-ttu-id="82d11-169">**ProcessOutput**</span><span class="sxs-lookup"><span data-stu-id="82d11-169">**ProcessOutput**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [<span data-ttu-id="82d11-170">**SetInputType**</span><span class="sxs-lookup"><span data-stu-id="82d11-170">**SetInputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [<span data-ttu-id="82d11-171">**Setoutputtypetype**</span><span class="sxs-lookup"><span data-stu-id="82d11-171">**SetOutputType**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [<span data-ttu-id="82d11-172">**SetOutputBounds**</span><span class="sxs-lookup"><span data-stu-id="82d11-172">**SetOutputBounds**</span></span>](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

<span data-ttu-id="82d11-173">Todos os outros métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) retornarão o erro E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="82d11-173">All other [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) methods will return the error E\_NOTIMPL.</span></span>

## <a name="supported-icodecapi-methods"></a><span data-ttu-id="82d11-174">Métodos ICodecAPI com suporte</span><span class="sxs-lookup"><span data-stu-id="82d11-174">Supported ICodecAPI methods</span></span>

<span data-ttu-id="82d11-175">Os métodos a seguir da interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) têm suporte para o codificador H. 265/HEVC:</span><span class="sxs-lookup"><span data-stu-id="82d11-175">The following methods of the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface are supported for the H.265/HEVC encoder:</span></span>

-   [<span data-ttu-id="82d11-176">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="82d11-176">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="82d11-177">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="82d11-177">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [<span data-ttu-id="82d11-178">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="82d11-178">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="82d11-179">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="82d11-179">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="82d11-180">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="82d11-180">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

<span data-ttu-id="82d11-181">Todos os outros métodos [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retornarão o erro E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="82d11-181">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods will return the error E\_NOTIMPL.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="82d11-182">Propriedades do codec</span><span class="sxs-lookup"><span data-stu-id="82d11-182">Codec Properties</span></span>

<span data-ttu-id="82d11-183">O codificador H. 265 implementa a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para definir parâmetros de codificação.</span><span class="sxs-lookup"><span data-stu-id="82d11-183">The H.265 encoder implements the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface for setting encoding parameters.</span></span> <span data-ttu-id="82d11-184">Ele dá suporte às propriedades a seguir.</span><span class="sxs-lookup"><span data-stu-id="82d11-184">It supports the following properties.</span></span>

<span data-ttu-id="82d11-185">Para obter os requisitos de codec para a certificação do codificador HCK, consulte a seção **codificador de hardware certificado** abaixo.</span><span class="sxs-lookup"><span data-stu-id="82d11-185">For the codec requirements for HCK encoder certification, see the **Certified Hardware Encoder** section below.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="82d11-186">Propriedade</span><span class="sxs-lookup"><span data-stu-id="82d11-186">Property</span></span></th>
<th><span data-ttu-id="82d11-187">Descrição</span><span class="sxs-lookup"><span data-stu-id="82d11-187">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="82d11-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="82d11-188"><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></span></span></td>
<td><span data-ttu-id="82d11-189">Define o modo de controle de taxa.</span><span class="sxs-lookup"><span data-stu-id="82d11-189">Sets the rate control mode.</span></span> <span data-ttu-id="82d11-190">Os modos suportados são:</span><span class="sxs-lookup"><span data-stu-id="82d11-190">The supported modes are:</span></span><br/>
<ul>
<li><span data-ttu-id="82d11-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span><span class="sxs-lookup"><span data-stu-id="82d11-191"><strong>eAVEncCommonRateControlMode_CBR</strong></span></span></li>
<li><span data-ttu-id="82d11-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span><span class="sxs-lookup"><span data-stu-id="82d11-192"><strong>eAVEncCommonRateControlMode_Quality</strong></span></span></li>
</ul>
<span data-ttu-id="82d11-193">Se outros modos forem especificados, o controle de taxa de <strong>eAVEncCommonRateControlMode_CBR</strong> será usado.</span><span class="sxs-lookup"><span data-stu-id="82d11-193">If other modes are specified, the <strong>eAVEncCommonRateControlMode_CBR</strong> rate control will be used.</span></span><br/> <span data-ttu-id="82d11-194">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-194">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span><span class="sxs-lookup"><span data-stu-id="82d11-195"><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></span></span></td>
<td><span data-ttu-id="82d11-196">Define a taxa média de bits para o fluxo de bits codificado, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="82d11-196">Sets the average bit rate for the encoded bit stream, in bits per second.</span></span> <br/> <span data-ttu-id="82d11-197">O intervalo válido é [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="82d11-197">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="82d11-198">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-198">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span><span class="sxs-lookup"><span data-stu-id="82d11-199"><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></span></span></td>
<td><span data-ttu-id="82d11-200">Define o tamanho do buffer, em bytes, para a codificação de taxa de bits constante (CBR).</span><span class="sxs-lookup"><span data-stu-id="82d11-200">Sets the buffer size, in bytes, for constant bit rate (CBR) encoding.</span></span><br/> <span data-ttu-id="82d11-201">O intervalo válido é [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="82d11-201">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="82d11-202">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-202">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span><span class="sxs-lookup"><span data-stu-id="82d11-203"><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></span></span></td>
<td><span data-ttu-id="82d11-204">Define a taxa de bits máxima para modos de controle de taxa que permitem uma taxa de bits de pico.</span><span class="sxs-lookup"><span data-stu-id="82d11-204">Sets the maximum bitrate for rate control modes that allow a peak bitrate.</span></span> <br/> <span data-ttu-id="82d11-205">O intervalo válido é [1... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="82d11-205">The valid range is [1 ... 2³²–1].</span></span> <br/> <span data-ttu-id="82d11-206">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-206">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span><span class="sxs-lookup"><span data-stu-id="82d11-207"><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></span></span></td>
<td><span data-ttu-id="82d11-208">Define o número de imagens de um cabeçalho GOP para o seguinte, incluindo a âncora à esquerda, mas não o seguinte.</span><span class="sxs-lookup"><span data-stu-id="82d11-208">Sets the number of pictures from one GOP header to the next, including the leading anchor but not the following one.</span></span> <br/> <span data-ttu-id="82d11-209">O intervalo válido é [0... 2 ³ ² – 1].</span><span class="sxs-lookup"><span data-stu-id="82d11-209">The valid range is [0 ... 2³²–1].</span></span> <span data-ttu-id="82d11-210">Se for zero, o codificador selecionará o tamanho de GOP.</span><span class="sxs-lookup"><span data-stu-id="82d11-210">If zero, the encoder selects the GOP size.</span></span> <span data-ttu-id="82d11-211">O valor padrão é zero.</span><span class="sxs-lookup"><span data-stu-id="82d11-211">The default value is zero.</span></span> <br/> <span data-ttu-id="82d11-212">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-212">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span><span class="sxs-lookup"><span data-stu-id="82d11-213"><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></span></span></td>
<td><span data-ttu-id="82d11-214">Habilita ou desabilita o modo de baixa latência.</span><span class="sxs-lookup"><span data-stu-id="82d11-214">Enables or disables low-latency mode.</span></span> <br/> <span data-ttu-id="82d11-215">Esse é um valor VT_BOOL.</span><span class="sxs-lookup"><span data-stu-id="82d11-215">This is a VT_BOOL value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span><span class="sxs-lookup"><span data-stu-id="82d11-216"><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></span></span></td>
<td><span data-ttu-id="82d11-217">Define a compensação de qualidade/velocidade.</span><span class="sxs-lookup"><span data-stu-id="82d11-217">Sets the quality/speed tradeoff.</span></span> <span data-ttu-id="82d11-218">Esse valor afeta como o codificador executa várias operações de codificação, como compensação de movimento.</span><span class="sxs-lookup"><span data-stu-id="82d11-218">This value affects how the encoder performs various encoding operations, such as motion compensation.</span></span> <span data-ttu-id="82d11-219">Em níveis mais altos de complexidade, o codificador é executado mais lentamente, mas produz uma qualidade melhor na mesma taxa de bits.</span><span class="sxs-lookup"><span data-stu-id="82d11-219">At higher complexity levels, the encoder runs more slowly but produces better quality at the same bit rate.</span></span> <br/> <span data-ttu-id="82d11-220">O intervalo válido é de 0 a 100.</span><span class="sxs-lookup"><span data-stu-id="82d11-220">The valid range is 0 – 100.</span></span> <span data-ttu-id="82d11-221">Internamente, esse valor é mapeado para um conjunto menor de níveis de qualidade/velocidade com suporte pelo codificador.</span><span class="sxs-lookup"><span data-stu-id="82d11-221">Internally, this value is mapped to a smaller set of quality/speed levels supported by the encoder.</span></span><br/> <span data-ttu-id="82d11-222">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-222">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span><span class="sxs-lookup"><span data-stu-id="82d11-223"><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></span></span></td>
<td><span data-ttu-id="82d11-224">Força o codificador a codificar o próximo quadro como um quadro-chave.</span><span class="sxs-lookup"><span data-stu-id="82d11-224">Forces the encoder to code the next frame as a key frame.</span></span><br/> <span data-ttu-id="82d11-225">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-225">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span><span class="sxs-lookup"><span data-stu-id="82d11-226"><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></span></span></td>
<td><span data-ttu-id="82d11-227">Quando essa propriedade for definida, fará com que o codificador use a QP especificada para codificar o próximo quadro e todos os quadros subsequentes até que um novo QP seja especificado.</span><span class="sxs-lookup"><span data-stu-id="82d11-227">When this property is set it will cause the encoder to use the specified QP to encode the next frame and all subsequent frames until a new QP is specified.</span></span> <br/> <span data-ttu-id="82d11-228">Intervalo válido: 0 – 51, inclusivo</span><span class="sxs-lookup"><span data-stu-id="82d11-228">Valid range: 0–51, inclusive</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span><span class="sxs-lookup"><span data-stu-id="82d11-229"><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></span></span></td>
<td><span data-ttu-id="82d11-230">Essa propriedade definirá um limite no mínimo QP que o codificador pode usar durante a CBR ratecontrol.</span><span class="sxs-lookup"><span data-stu-id="82d11-230">This property will set a limit on the minimum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="82d11-231">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-231">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span><span class="sxs-lookup"><span data-stu-id="82d11-232"><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></span></span></td>
<td><span data-ttu-id="82d11-233">Essa propriedade definirá um limite no máximo QP que o codificador pode usar durante a CBR ratecontrol.</span><span class="sxs-lookup"><span data-stu-id="82d11-233">This property will set a limit on the maximum QP that the encoder can use during CBR ratecontrol.</span></span><br/> <span data-ttu-id="82d11-234">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-234">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="82d11-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span><span class="sxs-lookup"><span data-stu-id="82d11-235"><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></span></span></td>
<td><span data-ttu-id="82d11-236">Define se o conteúdo é um vídeo de tela inteira, em oposição ao conteúdo da tela que pode ter uma janela de vídeo menor ou sem nenhum vídeo.</span><span class="sxs-lookup"><span data-stu-id="82d11-236">Sets whether the content is full-screen video, as opposed to screen content that might have a smaller window of video or have no video at all.</span></span><br/> <span data-ttu-id="82d11-237">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-237">This is a VT_UI4 value.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="82d11-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span><span class="sxs-lookup"><span data-stu-id="82d11-238"><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></span></span></td>
<td><span data-ttu-id="82d11-239">Define o número de threads usados para executar a operação de compactação.</span><span class="sxs-lookup"><span data-stu-id="82d11-239">Sets the number of threads used to perform the compression operation.</span></span> <span data-ttu-id="82d11-240">O codificador dividirá o quadro em blocos, de modo que o número de threads seja igual ao número de blocos.</span><span class="sxs-lookup"><span data-stu-id="82d11-240">The encoder will divide the frame into tiles such that the number of threads equals the number of tiles.</span></span><br/>
<ul>
<li><span data-ttu-id="82d11-241">O número de processadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="82d11-241">The number of logical processors.</span></span> <span data-ttu-id="82d11-242">O número de threads deve ser menor ou igual ao número de processadores lógicos.</span><span class="sxs-lookup"><span data-stu-id="82d11-242">The number of threads must be less than or equal to the number of logical processors.</span></span></li>
<li><span data-ttu-id="82d11-243">O tamanho do quadro.</span><span class="sxs-lookup"><span data-stu-id="82d11-243">The size of the frame.</span></span> <span data-ttu-id="82d11-244">O tamanho de um bloco deve ser maior ou igual a 265x64 pixels.</span><span class="sxs-lookup"><span data-stu-id="82d11-244">The size of a tile must bigger than or equal to 265x64 pixels.</span></span></li>
<li><span data-ttu-id="82d11-245">Paridade.</span><span class="sxs-lookup"><span data-stu-id="82d11-245">Parity.</span></span> <span data-ttu-id="82d11-246">O número de threads deve ser um valor par.</span><span class="sxs-lookup"><span data-stu-id="82d11-246">The number of threads must be an even value.</span></span> <span data-ttu-id="82d11-247">Se o valor especificado for ímpar, o próximo valor inferior menor será usado.</span><span class="sxs-lookup"><span data-stu-id="82d11-247">If the specified value is odd then the next lower even value will be used.</span></span></li>
</ul>
<span data-ttu-id="82d11-248">Esse é um valor VT_UI4.</span><span class="sxs-lookup"><span data-stu-id="82d11-248">This is a VT_UI4 value.</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a><span data-ttu-id="82d11-249">Codificador de hardware certificado</span><span class="sxs-lookup"><span data-stu-id="82d11-249">Certified Hardware Encoder</span></span>

<span data-ttu-id="82d11-250">Se um codificador de hardware certificado estiver presente, ele geralmente será usado em vez do codificador do sistema da caixa de entrada para Media Foundation cenários relacionados.</span><span class="sxs-lookup"><span data-stu-id="82d11-250">If a certified hardware encoder is present, it will generally be used instead of the inbox system encoder for Media Foundation related scenarios.</span></span> <span data-ttu-id="82d11-251">Os codificadores certificados são necessários para dar suporte a um determinado conjunto de propriedades **ICodecAPI** e, opcionalmente, podem dar suporte a outro conjunto de propriedades.</span><span class="sxs-lookup"><span data-stu-id="82d11-251">Certified encoders are required to support a certain set of **ICodecAPI** properties and can optionally support another set of properties.</span></span> <span data-ttu-id="82d11-252">O processo de certificação deve garantir que as propriedades necessárias tenham suporte adequado e, se houver suporte para uma propriedade opcional, que também tenha suporte adequado.</span><span class="sxs-lookup"><span data-stu-id="82d11-252">The certification process should guarantee that the required properties are properly supported and, if an optional property is supported, that it is also properly supported.</span></span>

<span data-ttu-id="82d11-253">Veja a seguir o conjunto de propriedades obrigatórias e opcionais do **ICodecAPI** para que os codificadores passem a certificação do codificador HCK.</span><span class="sxs-lookup"><span data-stu-id="82d11-253">The following is the set of required and optional **ICodecAPI** properties for encoders to pass the HCK encoder certification.</span></span>

-   [<span data-ttu-id="82d11-254">CODECAPI \_ AVEncCommonRateControlMode</span><span class="sxs-lookup"><span data-stu-id="82d11-254">CODECAPI\_AVEncCommonRateControlMode</span></span>](../directshow/avenccommonratecontrolmode-property.md)
-   [<span data-ttu-id="82d11-255">CODECAPI \_ AVEncCommonQuality</span><span class="sxs-lookup"><span data-stu-id="82d11-255">CODECAPI\_AVEncCommonQuality</span></span>](../directshow/avenccommonquality-property.md)
-   [<span data-ttu-id="82d11-256">CODECAPI \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="82d11-256">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)
-   [<span data-ttu-id="82d11-257">CODECAPI \_ AVEncCommonBufferSize</span><span class="sxs-lookup"><span data-stu-id="82d11-257">CODECAPI\_AVEncCommonBufferSize</span></span>](../directshow/avenccommonbuffersize-property.md)
-   [<span data-ttu-id="82d11-258">CODECAPI \_ AVEncMPVGOPSize</span><span class="sxs-lookup"><span data-stu-id="82d11-258">CODECAPI\_AVEncMPVGOPSize</span></span>](../directshow/avencmpvgopsize-property.md)
-   [<span data-ttu-id="82d11-259">CODECAPI \_ AVEncVideoEncodeQP</span><span class="sxs-lookup"><span data-stu-id="82d11-259">CODECAPI\_AVEncVideoEncodeQP</span></span>](codecapi-avencvideoencodeqp.md)
-   [<span data-ttu-id="82d11-260">CODECAPI \_ AVEncVideoForceKeyFrame</span><span class="sxs-lookup"><span data-stu-id="82d11-260">CODECAPI\_AVEncVideoForceKeyFrame</span></span>](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a><span data-ttu-id="82d11-261">Requisitos</span><span class="sxs-lookup"><span data-stu-id="82d11-261">Requirements</span></span>



| <span data-ttu-id="82d11-262">Requisito</span><span class="sxs-lookup"><span data-stu-id="82d11-262">Requirement</span></span> | <span data-ttu-id="82d11-263">Valor</span><span class="sxs-lookup"><span data-stu-id="82d11-263">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="82d11-264">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82d11-264">Minimum supported client</span></span><br/> | <span data-ttu-id="82d11-265">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="82d11-265">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="82d11-266">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="82d11-266">Minimum supported server</span></span><br/> | <span data-ttu-id="82d11-267">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="82d11-267">None supported</span></span><br/>                                                                |
| <span data-ttu-id="82d11-268">DLL</span><span class="sxs-lookup"><span data-stu-id="82d11-268">DLL</span></span><br/>                      | <dl> <span data-ttu-id="82d11-269"><dt>Mfh265enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="82d11-269"><dt>Mfh265enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="82d11-270">Confira também</span><span class="sxs-lookup"><span data-stu-id="82d11-270">See also</span></span>

<dl> <dt>

[<span data-ttu-id="82d11-271">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="82d11-271">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
