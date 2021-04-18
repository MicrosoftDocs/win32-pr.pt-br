---
description: O decodificador de vídeo MPEG-2 é uma Media Foundation transformação que decodifica o vídeo MPEG-1 e MPEG-2.
ms.assetid: 3E7FAE14-932D-44A3-997B-567C0D2EAE7B
title: Decodificador de vídeo MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ca4384154faff777280fd0a03cf4fd289603e7a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104502272"
---
# <a name="mpeg-2-video-decoder"></a><span data-ttu-id="d27b2-103">Decodificador de vídeo MPEG-2</span><span class="sxs-lookup"><span data-stu-id="d27b2-103">MPEG-2 Video Decoder</span></span>

<span data-ttu-id="d27b2-104">O decodificador de vídeo MPEG-2 é uma [Media Foundation transformação](media-foundation-transforms.md) que decodifica o vídeo MPEG-1 e MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="d27b2-104">The MPEG-2 Video Decoder is a [Media Foundation transform](media-foundation-transforms.md) that decodes MPEG-1 and MPEG-2 video.</span></span> <span data-ttu-id="d27b2-105">O decodificador dá suporte ao vídeo de perfil principal e simples MPEG-2 (H. 262, ISO/IEC 13818-2) e vídeo MPEG-1 (ISO/IEC 11172-2).</span><span class="sxs-lookup"><span data-stu-id="d27b2-105">The decoder supports MPEG-2 Simple and Main profile video (H.262, ISO/IEC 13818-2) and MPEG-1 video (ISO/IEC 11172-2).</span></span>

## <a name="input-types"></a><span data-ttu-id="d27b2-106">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="d27b2-106">Input Types</span></span>

<span data-ttu-id="d27b2-107">O decodificador dá suporte aos seguintes tipos de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="d27b2-107">The decoder supports the following input media types.</span></span>

| <span data-ttu-id="d27b2-108">Atributo</span><span class="sxs-lookup"><span data-stu-id="d27b2-108">Attribute</span></span>                                                 | <span data-ttu-id="d27b2-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d27b2-109">Description</span></span>                                                             |
|-----------------------------------------------------------|-------------------------------------------------------------------------|
| [<span data-ttu-id="d27b2-110">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="d27b2-110">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="d27b2-111">**Vídeo do MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d27b2-111">**MFMediaType\_Video**</span></span>                                                  |
| [<span data-ttu-id="d27b2-112">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="d27b2-112">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="d27b2-113">**MFVideoFormat \_ MPEG1**</span><span class="sxs-lookup"><span data-stu-id="d27b2-113">**MFVideoFormat\_MPEG1**</span></span><br/> <span data-ttu-id="d27b2-114">**MFVideoFormat \_ MPEG2**</span><span class="sxs-lookup"><span data-stu-id="d27b2-114">**MFVideoFormat\_MPEG2**</span></span><br/> |



 

## <a name="output-types"></a><span data-ttu-id="d27b2-115">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="d27b2-115">Output Types</span></span>

<span data-ttu-id="d27b2-116">O decodificador dá suporte aos seguintes tipos de saída.</span><span class="sxs-lookup"><span data-stu-id="d27b2-116">The decoder supports the following output types.</span></span>

| <span data-ttu-id="d27b2-117">Atributo</span><span class="sxs-lookup"><span data-stu-id="d27b2-117">Attribute</span></span>                                                 | <span data-ttu-id="d27b2-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="d27b2-118">Description</span></span>                                                                                                                                                                    |
|-----------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d27b2-119">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="d27b2-119">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md) | <span data-ttu-id="d27b2-120">**Vídeo do MFMediaType \_**</span><span class="sxs-lookup"><span data-stu-id="d27b2-120">**MFMediaType\_Video**</span></span>                                                                                                                                                         |
| [<span data-ttu-id="d27b2-121">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="d27b2-121">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)        | <span data-ttu-id="d27b2-122">**MFVideoFormat \_ I420**</span><span class="sxs-lookup"><span data-stu-id="d27b2-122">**MFVideoFormat\_I420**</span></span><br/> <span data-ttu-id="d27b2-123">**MFVideoFormat \_ IYUV**</span><span class="sxs-lookup"><span data-stu-id="d27b2-123">**MFVideoFormat\_IYUV**</span></span><br/> <span data-ttu-id="d27b2-124">**MFVideoFormat \_ NV12**</span><span class="sxs-lookup"><span data-stu-id="d27b2-124">**MFVideoFormat\_NV12**</span></span><br/> <span data-ttu-id="d27b2-125">**MFVideoFormat \_ YUY2**</span><span class="sxs-lookup"><span data-stu-id="d27b2-125">**MFVideoFormat\_YUY2**</span></span><br/> <span data-ttu-id="d27b2-126">**MFVideoFormat \_ YV12**</span><span class="sxs-lookup"><span data-stu-id="d27b2-126">**MFVideoFormat\_YV12**</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="d27b2-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="d27b2-127">Remarks</span></span>

<span data-ttu-id="d27b2-128">O decodificador de vídeo MPEG-2 expõe as seguintes interfaces:</span><span class="sxs-lookup"><span data-stu-id="d27b2-128">The MPEG-2 video decoder exposes the following interfaces:</span></span>

-   [<span data-ttu-id="d27b2-129">**ICodecAPI**</span><span class="sxs-lookup"><span data-stu-id="d27b2-129">**ICodecAPI**</span></span>](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [<span data-ttu-id="d27b2-130">**IMFGetService**</span><span class="sxs-lookup"><span data-stu-id="d27b2-130">**IMFGetService**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfgetservice)
-   [<span data-ttu-id="d27b2-131">**IMFQualityAdvise**</span><span class="sxs-lookup"><span data-stu-id="d27b2-131">**IMFQualityAdvise**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise)
-   [<span data-ttu-id="d27b2-132">**IMFQualityAdvise2**</span><span class="sxs-lookup"><span data-stu-id="d27b2-132">**IMFQualityAdvise2**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfqualityadvise2)
-   [<span data-ttu-id="d27b2-133">**IMFRateControl**</span><span class="sxs-lookup"><span data-stu-id="d27b2-133">**IMFRateControl**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratecontrol)
-   [<span data-ttu-id="d27b2-134">**IMFRateSupport**</span><span class="sxs-lookup"><span data-stu-id="d27b2-134">**IMFRateSupport**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfratesupport)
-   [<span data-ttu-id="d27b2-135">**IMFRealTimeClient**</span><span class="sxs-lookup"><span data-stu-id="d27b2-135">**IMFRealTimeClient**</span></span>](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [<span data-ttu-id="d27b2-136">**IMFTransform**</span><span class="sxs-lookup"><span data-stu-id="d27b2-136">**IMFTransform**</span></span>](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

<span data-ttu-id="d27b2-137">A entrada para o decodificador deve ser um fluxo elementar.</span><span class="sxs-lookup"><span data-stu-id="d27b2-137">The input to the decoder must be an elementary stream.</span></span> <span data-ttu-id="d27b2-138">A resolução máxima com suporte é de 1920 × 1088 pixels.</span><span class="sxs-lookup"><span data-stu-id="d27b2-138">The maximum supported resolution is 1920 × 1088 pixels.</span></span>

<span data-ttu-id="d27b2-139">O decodificador dá suporte a DXVA (DirectX Video Acceleration) usando o Microsoft Direct3D 9 ou o Microsoft Direct3D 11.</span><span class="sxs-lookup"><span data-stu-id="d27b2-139">The decoder supports DirectX Video Acceleration (DXVA) using either Microsoft Direct3D 9 or Microsoft Direct3D 11.</span></span>

### <a name="special-decoding-modes"></a><span data-ttu-id="d27b2-140">Modos de decodificação especiais</span><span class="sxs-lookup"><span data-stu-id="d27b2-140">Special Decoding Modes</span></span>

-   <span data-ttu-id="d27b2-141">**Modo de baixa latência.**</span><span class="sxs-lookup"><span data-stu-id="d27b2-141">**Low latency mode.**</span></span> <span data-ttu-id="d27b2-142">Esse modo é apropriado para cenários como comunicações em tempo real.</span><span class="sxs-lookup"><span data-stu-id="d27b2-142">This mode is appropriate for scenarios such as real-time communications.</span></span> <span data-ttu-id="d27b2-143">Ele reduz a latência de inicialização, portanto, o decodificador produz o primeiro exemplo de saída mais cedo.</span><span class="sxs-lookup"><span data-stu-id="d27b2-143">It reduces start-up latency, so the decoder produces the first output sample sooner.</span></span> <span data-ttu-id="d27b2-144">No entanto, o decodificador armazena em buffer menos amostras nesse modo, o que pode levar a falhas, pois o decodificador não decodifica o máximo de quadros com antecedência.</span><span class="sxs-lookup"><span data-stu-id="d27b2-144">However, the decoder buffers fewer samples in this mode, which can potentially lead to glitches, because the decoder does not decode as many frames in advance.</span></span> <span data-ttu-id="d27b2-145">Para habilitar o modo de baixa latência, defina o atributo [CODECAPI \_ AVLowLatencyMode](codecapi-avlowlatencymode.md) .</span><span class="sxs-lookup"><span data-stu-id="d27b2-145">To enable low latency mode, set the [CODECAPI\_AVLowLatencyMode](codecapi-avlowlatencymode.md) attribute.</span></span>
-   <span data-ttu-id="d27b2-146">**Atingir.**</span><span class="sxs-lookup"><span data-stu-id="d27b2-146">**Seeking.**</span></span> <span data-ttu-id="d27b2-147">Para busca precisa, chame o método [**IMFTransform:: SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) .</span><span class="sxs-lookup"><span data-stu-id="d27b2-147">For precise seeking, call the [**IMFTransform::SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds) method.</span></span> <span data-ttu-id="d27b2-148">Quando esse método é chamado, o decodificador gera apenas quadros que se enquadram no intervalo de carimbos de data/hora especificado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="d27b2-148">When this method is called, the decoder outputs only frames that fall within the range of time stamps specified by the caller.</span></span>
-   <span data-ttu-id="d27b2-149">**Modo de geração de miniatura**.</span><span class="sxs-lookup"><span data-stu-id="d27b2-149">**Thumbnail generation mode**.</span></span> <span data-ttu-id="d27b2-150">Esse modo destina-se à geração rápida de imagens em miniatura.</span><span class="sxs-lookup"><span data-stu-id="d27b2-150">This mode is intended for quick generation of thumbnail images.</span></span> <span data-ttu-id="d27b2-151">Nesse modo, o decodificador inicialmente decodifica apenas quadros I.</span><span class="sxs-lookup"><span data-stu-id="d27b2-151">In this mode, the decoder initially decodes only I frames.</span></span> <span data-ttu-id="d27b2-152">Se nenhum quadro I for encontrado em um determinado número de quadros, o decodificador iniciará a decodificação de quadros P e produzirá quadros não-I em um intervalo fixo (um por *N* imagens) até que um quadro I seja atingido.</span><span class="sxs-lookup"><span data-stu-id="d27b2-152">If no I frame is found within a certain number of frames, the decoder starts decoding P frames and outputs non–I frames at a fixed interval (one per *N* pictures) until an I frame is reached.</span></span> <span data-ttu-id="d27b2-153">Para habilitar o modo de geração de miniatura, defina a propriedade [CODECAPI \_ AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) .</span><span class="sxs-lookup"><span data-stu-id="d27b2-153">To enable thumbnail generation mode, set the [CODECAPI\_AVDecVideoThumbnailGenerationMode](../directshow/avdecvideothumbnailgenerationmode-property.md) property.</span></span>
-   <span data-ttu-id="d27b2-154">**Rodada de toque.**</span><span class="sxs-lookup"><span data-stu-id="d27b2-154">**Trick play.**</span></span> <span data-ttu-id="d27b2-155">O decodificador pode decodificar taxas com mais rapidez do que o tempo real.</span><span class="sxs-lookup"><span data-stu-id="d27b2-155">The decoder can decode at rates faster than real time.</span></span> <span data-ttu-id="d27b2-156">Em taxas de reprodução mais altas, o decodificador mudará para decodificar apenas quadros I.</span><span class="sxs-lookup"><span data-stu-id="d27b2-156">At higher playback rates, the decoder will switch to decoding only I frames.</span></span> <span data-ttu-id="d27b2-157">Para reprodução reversa, apenas os quadros I são decodificados.</span><span class="sxs-lookup"><span data-stu-id="d27b2-157">For reverse playback, only I frames are decoded.</span></span>

### <a name="codec-properties"></a><span data-ttu-id="d27b2-158">Propriedades do codec</span><span class="sxs-lookup"><span data-stu-id="d27b2-158">Codec Properties</span></span>

<span data-ttu-id="d27b2-159">O decodificador dá suporte às seguintes propriedades por meio do método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="d27b2-159">The decoder supports the following properties through the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span>



| <span data-ttu-id="d27b2-160">Propriedade</span><span class="sxs-lookup"><span data-stu-id="d27b2-160">Property</span></span>                                                                                                      | <span data-ttu-id="d27b2-161">Descrição</span><span class="sxs-lookup"><span data-stu-id="d27b2-161">Description</span></span>                                                                                                |
|---------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="d27b2-162">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="d27b2-162">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)               | <span data-ttu-id="d27b2-163">Habilita ou desabilita o modo de geração de miniatura.</span><span class="sxs-lookup"><span data-stu-id="d27b2-163">Enables or disables thumbnail generation mode.</span></span>                                                             |
| [<span data-ttu-id="d27b2-164">CODECAPI \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="d27b2-164">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)                        | <span data-ttu-id="d27b2-165">Habilita ou desabilita a decodificação acelerada de hardware.</span><span class="sxs-lookup"><span data-stu-id="d27b2-165">Enables or disables hardware accelerated decoding.</span></span>                                                         |
| [<span data-ttu-id="d27b2-166">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="d27b2-166">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)                                                   | <span data-ttu-id="d27b2-167">Habilita ou desabilita o modo de baixa latência.</span><span class="sxs-lookup"><span data-stu-id="d27b2-167">Enables or disables low-latency mode.</span></span>                                                                      |
| [<span data-ttu-id="d27b2-168">o \_ decodificador MFT \_ expõe os \_ \_ tipos \_ de saída na \_ \_ ordem nativa</span><span class="sxs-lookup"><span data-stu-id="d27b2-168">MFT\_DECODER\_EXPOSE\_OUTPUT\_TYPES\_IN\_NATIVE\_ORDER</span></span>](mft-decoder-expose-output-types-in-native-order.md) | <span data-ttu-id="d27b2-169">Especifica se o decodificador expõe os tipos de saída que são adequados para transcodificação antes de outros formatos.</span><span class="sxs-lookup"><span data-stu-id="d27b2-169">Specifies whether the decoder exposes output types that are suitable for transcoding before other formats.</span></span> |



 

<span data-ttu-id="d27b2-170">Dessas propriedades, o seguinte também pode ser definido por meio da interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="d27b2-170">Of these properties, the following can also be set through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface:</span></span>

-   [<span data-ttu-id="d27b2-171">CODECAPI \_ AVDecVideoThumbnailGenerationMode</span><span class="sxs-lookup"><span data-stu-id="d27b2-171">CODECAPI\_AVDecVideoThumbnailGenerationMode</span></span>](../directshow/avdecvideothumbnailgenerationmode-property.md)
-   [<span data-ttu-id="d27b2-172">CODECAPI \_ AVDecVideoAcceleration \_ MPEG2</span><span class="sxs-lookup"><span data-stu-id="d27b2-172">CODECAPI\_AVDecVideoAcceleration\_MPEG2</span></span>](../directshow/avdecvideoacceleration-mpeg2-property.md)
-   [<span data-ttu-id="d27b2-173">CODECAPI \_ AVLowLatencyMode</span><span class="sxs-lookup"><span data-stu-id="d27b2-173">CODECAPI\_AVLowLatencyMode</span></span>](codecapi-avlowlatencymode.md)

### <a name="limitations"></a><span data-ttu-id="d27b2-174">Limitações</span><span class="sxs-lookup"><span data-stu-id="d27b2-174">Limitations</span></span>

-   <span data-ttu-id="d27b2-175">Não há suporte para o decodificador em plataformas baseadas em IA-64.</span><span class="sxs-lookup"><span data-stu-id="d27b2-175">The decoder is not supported on IA-64–based platforms.</span></span>
-   <span data-ttu-id="d27b2-176">O decodificador não dá suporte à descriptografia de CSS nem à reprodução de DVDs criptografados.</span><span class="sxs-lookup"><span data-stu-id="d27b2-176">The decoder does not support CSS decryption or playback of encrypted DVDs.</span></span>

## <a name="requirements"></a><span data-ttu-id="d27b2-177">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d27b2-177">Requirements</span></span>



| <span data-ttu-id="d27b2-178">Requisito</span><span class="sxs-lookup"><span data-stu-id="d27b2-178">Requirement</span></span> | <span data-ttu-id="d27b2-179">Valor</span><span class="sxs-lookup"><span data-stu-id="d27b2-179">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="d27b2-180">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d27b2-180">Minimum supported client</span></span><br/> | <span data-ttu-id="d27b2-181">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="d27b2-181">Windows 8 \[desktop apps only\]</span></span><br/>                                                 |
| <span data-ttu-id="d27b2-182">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="d27b2-182">Minimum supported server</span></span><br/> | <span data-ttu-id="d27b2-183">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="d27b2-183">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                       |
| <span data-ttu-id="d27b2-184">DLL</span><span class="sxs-lookup"><span data-stu-id="d27b2-184">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d27b2-185"><dt>Msmpeg2vdec.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d27b2-185"><dt>Msmpeg2vdec.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d27b2-186">Confira também</span><span class="sxs-lookup"><span data-stu-id="d27b2-186">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d27b2-187">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="d27b2-187">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
