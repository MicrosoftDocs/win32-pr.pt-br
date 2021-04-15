---
description: O decodificador de vídeo Media Foundation H. 265 é uma transformação Media Foundation que dá suporte à decodificação de conteúdo H. 265/HEVC no formato anexo B e pode ser usado na reprodução de arquivos MP4 e M2TS.
ms.assetid: BBE754E4-2AAD-4CFD-B53F-2B66693502EE
title: Decodificador de vídeo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c0c20a83f82e106bd749deb8bf2350cc9e5a347a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502204"
---
# <a name="h265--hevc-video-decoder"></a><span data-ttu-id="957ab-103">Decodificador de vídeo H. 265/HEVC</span><span class="sxs-lookup"><span data-stu-id="957ab-103">H.265 / HEVC Video Decoder</span></span>

<span data-ttu-id="957ab-104">O decodificador de vídeo Media Foundation H. 265 é uma [transformação Media Foundation](media-foundation-transforms.md) que dá suporte à decodificação de conteúdo H. 265/HEVC no formato anexo B e pode ser usado na reprodução de arquivos MP4 e M2TS.</span><span class="sxs-lookup"><span data-stu-id="957ab-104">The Media Foundation H.265 video decoder is a [Media Foundation Transform](media-foundation-transforms.md) that supports decoding H.265/HEVC content in Annex B format and can be used in playback of mp4 and m2ts files.</span></span>

<span data-ttu-id="957ab-105">O decodificador de vídeo H. 265 expõe as interfaces a seguir.</span><span class="sxs-lookup"><span data-stu-id="957ab-105">The H.265 video decoder exposes the following interfaces.</span></span>

-   <span data-ttu-id="957ab-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (com suporte no Windows 8)</span><span class="sxs-lookup"><span data-stu-id="957ab-106">[**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) (supported in Windows 8)</span></span>
-   [<span data-ttu-id="957ab-107">**IMFAttributes**</span><span class="sxs-lookup"><span data-stu-id="957ab-107">**IMFAttributes**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfattributes)
-   [<span data-ttu-id="957ab-108">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="957ab-108">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="957ab-109">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="957ab-109">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="957ab-110">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="957ab-110">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="957ab-111">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="957ab-111">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="957ab-112">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="957ab-112">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="957ab-113">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="957ab-113">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="957ab-114">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="957ab-114">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="957ab-115">Para criar uma instância do decodificador, chame a função [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) ou [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) .</span><span class="sxs-lookup"><span data-stu-id="957ab-115">To create an instance of the decoder call the [**MFTEnum**](/windows/desktop/api/mfapi/nf-mfapi-mftenum) or [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex) function.</span></span>

## <a name="input-types"></a><span data-ttu-id="957ab-116">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="957ab-116">Input Types</span></span>

<span data-ttu-id="957ab-117">O tipo de entrada deve conter pelo menos os dois atributos a seguir:</span><span class="sxs-lookup"><span data-stu-id="957ab-117">The input type must contain at least the following two attributes:</span></span>



| <span data-ttu-id="957ab-118">Atributo</span><span class="sxs-lookup"><span data-stu-id="957ab-118">Attribute</span></span>                                                 | <span data-ttu-id="957ab-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="957ab-119">Description</span></span>                                                                                   |
|-----------------------------------------------------------|-----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="957ab-120">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="957ab-120">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="957ab-121">**Vídeo do MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="957ab-121">**MFMediaType\_Video**</span></span>                                                                        |
| [<span data-ttu-id="957ab-122">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="957ab-122">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="957ab-123">[MFVideoFormat \_ HEVC](video-subtype-guids.md) ou MFVideoFormat \_ HEVC \_ es</span><span class="sxs-lookup"><span data-stu-id="957ab-123">[MFVideoFormat\_HEVC](video-subtype-guids.md) or MFVideoFormat\_HEVC\_ES</span></span> |



 

<span data-ttu-id="957ab-124">O primeiro subtipo de mídia, MFVideoFormat \_ HEVC, indica que os exemplos de mídia carregam H. 265 fragmentado com códigos de início e o fluxo tem SPS/PPS intercalados.</span><span class="sxs-lookup"><span data-stu-id="957ab-124">The first media subtype, MFVideoFormat\_HEVC, indicates that the media samples carry H.265 bitstream with start codes, and the stream has interleaved SPS/PPS.</span></span> <span data-ttu-id="957ab-125">Ele assume um quadro por amostra.</span><span class="sxs-lookup"><span data-stu-id="957ab-125">It assumes one frame per sample.</span></span>

<span data-ttu-id="957ab-126">O subtipo de mídia MFVideoFormat \_ HEVC \_ es é para indicar os exemplos de mídia que carregam o Element H. 265 fragmentado, em que cada exemplo pode conter uma imagem parcial, várias imagens, algumas imagens e uma imagem parcial.</span><span class="sxs-lookup"><span data-stu-id="957ab-126">The media subtype MFVideoFormat\_ HEVC\_ES is to indicate the media samples carry elementary H.265 bitstream, where each sample may contain a partial picture, multiple pictures, some pictures plus a partial picture.</span></span>

<span data-ttu-id="957ab-127">Os tipos de mídia de entrada não podem ser alterados dinamicamente entre dois tipos.</span><span class="sxs-lookup"><span data-stu-id="957ab-127">The input media types cannot change dynamically between two types.</span></span> <span data-ttu-id="957ab-128">O decodificador pode detectar alterações de formato de saída em andamento com base na sintaxe de fluxo elementar (taxa de proporção, dimensão, sinalizadores de entrelaçamento, informações de colorimetry) e disparar alterações de tipo de mídia de saída correspondente.</span><span class="sxs-lookup"><span data-stu-id="957ab-128">The decoder can detect in-flight output format changes based on the elementary stream syntax (aspect ratio, dimension, interlace flags, colorimetry information) and trigger corresponding output media type changes.</span></span>

<span data-ttu-id="957ab-129">Para o tipo de mídia de entrada, o decodificador espera que a origem defina o perfil correto.</span><span class="sxs-lookup"><span data-stu-id="957ab-129">For input media type, the decoder expects the source to set the correct Profile.</span></span> <span data-ttu-id="957ab-130">Por exemplo, se o conteúdo for descompactado, o tipo de mídia de entrada deverá especificar o perfil como Main10.</span><span class="sxs-lookup"><span data-stu-id="957ab-130">For example if the content is going to be 10bit, input media type should specify the profile as Main10.</span></span>

## <a name="output-types"></a><span data-ttu-id="957ab-131">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="957ab-131">Output Types</span></span>

<span data-ttu-id="957ab-132">O decodificador dá suporte aos seguintes subtipos de saída:</span><span class="sxs-lookup"><span data-stu-id="957ab-132">The decoder supports the following output subtypes:</span></span>

-   <span data-ttu-id="957ab-133">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="957ab-133">**MFVideoFormat\_NV12**</span></span>
-   <span data-ttu-id="957ab-134">**MFVideoFormat \_ P010**</span><span class="sxs-lookup"><span data-stu-id="957ab-134">**MFVideoFormat\_P010**</span></span>

<span data-ttu-id="957ab-135">Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="957ab-135">For more information about these subtypes, see [Video Subtype GUIDs](video-subtype-guids.md).</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="957ab-136">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="957ab-136">Transform Attributes</span></span>

<span data-ttu-id="957ab-137">O decodificador H. 265 implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="957ab-137">The H.265 decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="957ab-138">Os aplicativos podem usar esse método para obter ou definir os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="957ab-138">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="957ab-139">Atributo</span><span class="sxs-lookup"><span data-stu-id="957ab-139">Attribute</span></span>                                                                                       | <span data-ttu-id="957ab-140">Descrição</span><span class="sxs-lookup"><span data-stu-id="957ab-140">Description</span></span>                                                                                                                   |
|-------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="957ab-141">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="957ab-141">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                     | <span data-ttu-id="957ab-142">Habilita ou desabilita o modo de decodificação de baixa latência.</span><span class="sxs-lookup"><span data-stu-id="957ab-142">Enables or disables low-latency decoding mode.</span></span>                                                                                |
| [<span data-ttu-id="957ab-143">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="957ab-143">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)                           | <span data-ttu-id="957ab-144">Define o número de threads de trabalho usados pelo decodificador.</span><span class="sxs-lookup"><span data-stu-id="957ab-144">Sets the number of worker threads used by the decoder.</span></span>                                                                        |
| [<span data-ttu-id="957ab-145">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="957ab-145">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md) | <span data-ttu-id="957ab-146">Habilita ou desabilita o modo de geração de miniatura.</span><span class="sxs-lookup"><span data-stu-id="957ab-146">Enables or disables thumbnail generation mode.</span></span>                                                                                |
| [<span data-ttu-id="957ab-147">\_conjunto de \_ tamanhos de NALU MF \_</span><span class="sxs-lookup"><span data-stu-id="957ab-147">MF\_NALU\_LENGTH\_SET</span></span>](mf-nalu-length-set.md)                                                 | <span data-ttu-id="957ab-148">Indica que as informações de comprimento de NALU serão enviadas como um BLOB com cada exemplo de H. 265 compactada.</span><span class="sxs-lookup"><span data-stu-id="957ab-148">Indicates that NALU length information will be sent as a BLOB with each compressed H.265 sample.</span></span>                              |
| [<span data-ttu-id="957ab-149">\_informações de \_ comprimento de NALU MF \_</span><span class="sxs-lookup"><span data-stu-id="957ab-149">MF\_NALU\_LENGTH\_INFORMATION</span></span>](mf-nalu-length-information.md)                                 | <span data-ttu-id="957ab-150">Indica os comprimentos de NALUs no exemplo.</span><span class="sxs-lookup"><span data-stu-id="957ab-150">Indicates the lengths of NALUs in the sample.</span></span> <span data-ttu-id="957ab-151">Este é um BLOB MF que é definido em exemplos de entrada compactados para o decodificador H. 265.</span><span class="sxs-lookup"><span data-stu-id="957ab-151">This is a MF BLOB that is set on compressed input samples to the H.265 decoder.</span></span> |
| [<span data-ttu-id="957ab-152">\_contagem de \_ \_ amostra de saída mínima \_ \_ de e/o de MF</span><span class="sxs-lookup"><span data-stu-id="957ab-152">MF\_SA\_MINIMUM\_OUTPUT\_SAMPLE\_COUNT</span></span>](mf-sa-minimum-output-sample-count.md)                 | <span data-ttu-id="957ab-153">Especifica o número máximo de amostras de saída.</span><span class="sxs-lookup"><span data-stu-id="957ab-153">Specifies the maximum number of output samples.</span></span>                                                                               |



 

<span data-ttu-id="957ab-154">O decodificador H. 265 dá suporte à interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="957ab-154">The H.265 decoder supports the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span> <span data-ttu-id="957ab-155">Essa interface fornece uma API alternativate para definir as propriedades de codec a seguir.</span><span class="sxs-lookup"><span data-stu-id="957ab-155">This interface provides an alternativate API for setting the following codec properties.</span></span>

-   [<span data-ttu-id="957ab-156">CODECAPI \_ AVDecNumWorkerThreads</span><span class="sxs-lookup"><span data-stu-id="957ab-156">CODECAPI\_AVDecNumWorkerThreads</span></span>](codecapi-avdecnumworkerthreads.md)
-   [<span data-ttu-id="957ab-157">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="957ab-157">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="957ab-158">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="957ab-158">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

## <a name="format-constraints"></a><span data-ttu-id="957ab-159">Restrições de formato</span><span class="sxs-lookup"><span data-stu-id="957ab-159">Format Constraints</span></span>

<span data-ttu-id="957ab-160">O decodificador dá suporte aos seguintes formatos:</span><span class="sxs-lookup"><span data-stu-id="957ab-160">The decoder supports the following formats:</span></span>



| <span data-ttu-id="957ab-161">Requisito</span><span class="sxs-lookup"><span data-stu-id="957ab-161">Requirement</span></span> | <span data-ttu-id="957ab-162">Valor</span><span class="sxs-lookup"><span data-stu-id="957ab-162">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="957ab-163">Perfis/níveis</span><span class="sxs-lookup"><span data-stu-id="957ab-163">Profiles/Levels</span></span>    | <span data-ttu-id="957ab-164">Perfis principal, principal ainda e Main10</span><span class="sxs-lookup"><span data-stu-id="957ab-164">Main, Main Still Picture, and Main10 profiles</span></span>                                                                                                                                                                                                                        |
| <span data-ttu-id="957ab-165">Formatos de croma</span><span class="sxs-lookup"><span data-stu-id="957ab-165">Chroma Formats</span></span>     | <span data-ttu-id="957ab-166">4:2:0 croma</span><span class="sxs-lookup"><span data-stu-id="957ab-166">4:2:0 chroma</span></span>                                                                                                                                                                                                                                                         |
| <span data-ttu-id="957ab-167">Resolução mínima</span><span class="sxs-lookup"><span data-stu-id="957ab-167">Minimum Resolution</span></span> | <span data-ttu-id="957ab-168">48 × 48 pixels</span><span class="sxs-lookup"><span data-stu-id="957ab-168">48 × 48 pixels</span></span>                                                                                                                                                                                                                                                       |
| <span data-ttu-id="957ab-169">Resolução máxima</span><span class="sxs-lookup"><span data-stu-id="957ab-169">Maximum Resolution</span></span> | <span data-ttu-id="957ab-170">4096 × 2304 pixels</span><span class="sxs-lookup"><span data-stu-id="957ab-170">4096 × 2304 pixels</span></span><br/> <span data-ttu-id="957ab-171">A resolução máxima garantida para a aceleração de DXVA é 1920 × 1088 pixels; em resoluções mais altas, a decodificação é feita com o DXVA, se for compatível com o hardware subjacente, caso contrário, a decodificação será feita com o software.</span><span class="sxs-lookup"><span data-stu-id="957ab-171">The maximum guaranteed resolution for DXVA acceleration is 1920 × 1088 pixels; at higher resolutions, decoding is done with DXVA, if it is supported by the underlying hardware, otherwise, decoding is done with software.</span></span><br/> |
| <span data-ttu-id="957ab-172">DXVA</span><span class="sxs-lookup"><span data-stu-id="957ab-172">DXVA</span></span>               | <span data-ttu-id="957ab-173">O decodificador dá suporte a DX11 e DX12 DXVA, mas não a DXVA versão 2 ou a DXVA versão 1.</span><span class="sxs-lookup"><span data-stu-id="957ab-173">The decoder supports DX11 and DX12 DXVA, but not DXVA version 2 or DXVA version 1.</span></span>                                                                                                                                                                                                         |



 

<span data-ttu-id="957ab-174">Os dados de entrada devem estar em conformidade com o anexo B do ITU-T H. 265 \| ISO/IEC 23008-2.</span><span class="sxs-lookup"><span data-stu-id="957ab-174">Input data must conform to Annex B of ITU-T H.265 \| ISO/IEC 23008-2.</span></span> <span data-ttu-id="957ab-175">Os dados devem incluir os códigos de início.</span><span class="sxs-lookup"><span data-stu-id="957ab-175">The data must include the start codes.</span></span> <span data-ttu-id="957ab-176">O decodificador ignora os bytes até encontrar um conjunto de parâmetros de sequência (SPS) e um conjunto de parâmetros de imagem (PPS) válidos no fluxo de bytes.</span><span class="sxs-lookup"><span data-stu-id="957ab-176">The decoder skips bytes until it finds a valid sequence parameter set (SPS) and picture parameter set (PPS) in the byte stream.</span></span>

## <a name="requirements"></a><span data-ttu-id="957ab-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="957ab-177">Requirements</span></span>



| <span data-ttu-id="957ab-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="957ab-178">Requirement</span></span> | <span data-ttu-id="957ab-179">Valor</span><span class="sxs-lookup"><span data-stu-id="957ab-179">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="957ab-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="957ab-180">Minimum supported client</span></span><br/> | <span data-ttu-id="957ab-181">\[Somente aplicativos da área de trabalho do Windows 10\]</span><span class="sxs-lookup"><span data-stu-id="957ab-181">Windows 10 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="957ab-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="957ab-182">Minimum supported server</span></span><br/> | <span data-ttu-id="957ab-183">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="957ab-183">None supported</span></span><br/>                                                                |
| <span data-ttu-id="957ab-184">DLL</span><span class="sxs-lookup"><span data-stu-id="957ab-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="957ab-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span><span class="sxs-lookup"><span data-stu-id="957ab-185"><dt>hevcdecoder.dll</dt> <dt>hevcdecoder_store.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="957ab-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="957ab-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="957ab-187">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="957ab-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
