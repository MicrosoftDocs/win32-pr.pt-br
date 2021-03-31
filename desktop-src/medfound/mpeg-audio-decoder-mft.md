---
description: O decodificador de áudio MPEG da Microsoft é uma Media Foundation de transformação síncrona que permite decodificar formatos de fluxo elementares de áudio MPEG usando o pipeline de Media Foundation (MF).
ms.assetid: 29A0491D-CA0D-4909-96F0-5640D5EE77F9
title: Decodificador de áudio MPEG
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a98106ce4610c7c89a5e6212c225fd8eca3e4526
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921216"
---
# <a name="mpeg-audio-decoder"></a><span data-ttu-id="20a6f-103">Decodificador de áudio MPEG</span><span class="sxs-lookup"><span data-stu-id="20a6f-103">MPEG Audio Decoder</span></span>

<span data-ttu-id="20a6f-104">O decodificador de áudio MPEG da Microsoft é uma [Media Foundation de transformação](media-foundation-transforms.md) síncrona que permite decodificar formatos de fluxo elementares de áudio MPEG usando o pipeline de Media Foundation (MF).</span><span class="sxs-lookup"><span data-stu-id="20a6f-104">The Microsoft MPEG Audio Decoder is a synchronous [Media Foundation Transform](media-foundation-transforms.md) (MFT) that enables decoding MPEG audio elementary stream formats using the Media Foundation (MF) pipeline.</span></span>

<span data-ttu-id="20a6f-105">O decodificador dá suporte aos seguintes formatos de fluxo de do MPEG elementar.</span><span class="sxs-lookup"><span data-stu-id="20a6f-105">The decoder supports the following MPEG elementary stream formats.</span></span>

-   <span data-ttu-id="20a6f-106">Camadas de áudio MPEG-1 I e II (ISO/IEC 11172-3).</span><span class="sxs-lookup"><span data-stu-id="20a6f-106">MPEG-1 audio layers I and II (ISO/IEC 11172-3).</span></span> <span data-ttu-id="20a6f-107">2.</span><span class="sxs-lookup"><span data-stu-id="20a6f-107">2.</span></span> <span data-ttu-id="20a6f-108">MPEG-2 retroativa-Compatible, camadas I e II (ISO</span><span class="sxs-lookup"><span data-stu-id="20a6f-108">MPEG-2 backward-compatible, layers I and II (ISO</span></span>

-   <span data-ttu-id="20a6f-109">MPEG-2 retroativa-Compatible, camadas I e II (ISO/IEC 13818-3), mono e estéreo somente</span><span class="sxs-lookup"><span data-stu-id="20a6f-109">MPEG-2 backward-compatible, layers I and II (ISO/IEC 13818-3), mono and stereo only</span></span>

## <a name="class-identifier"></a><span data-ttu-id="20a6f-110">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="20a6f-110">Class Identifier</span></span>

<span data-ttu-id="20a6f-111">O CLSID (identificador de classe) do decodificador de áudio MPEG é **CLSID \_ MSMPEGAudDecMFT**, definido no arquivo de cabeçalho wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="20a6f-111">The class identifier (CLSID) of the MPEG Audio decoder is **CLSID\_MSMPEGAudDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-media-types"></a><span data-ttu-id="20a6f-112">Tipos de mídia de entrada</span><span class="sxs-lookup"><span data-stu-id="20a6f-112">Input Media Types</span></span>

<span data-ttu-id="20a6f-113">O decodificador de áudio MPEG dá suporte aos seguintes atributos de tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="20a6f-113">The MPEG Audio decoder supports the following input media type attributes.</span></span>



| <span data-ttu-id="20a6f-114">Atributo</span><span class="sxs-lookup"><span data-stu-id="20a6f-114">Attribute</span></span>                                                                               | <span data-ttu-id="20a6f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="20a6f-115">Value</span></span>                                                                                                                                                                                                                                                                 |
|-----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20a6f-116">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="20a6f-116">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="20a6f-117">**\_Áudio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="20a6f-117">**MFMediaType\_Audio**</span></span>                                                                                                                                                                                                                                                |
| [<span data-ttu-id="20a6f-118">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="20a6f-118">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="20a6f-119">**MFAudioFormat \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="20a6f-119">**MFAudioFormat\_MPEG**</span></span>                                                                                                                                                                                                                                               |
| [<span data-ttu-id="20a6f-120">**\_canais de \_ número de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20a6f-120">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="20a6f-121">Adicional Geralmente 1 para mono ou 2 para estéreo, mas pode ter até 6 canais.</span><span class="sxs-lookup"><span data-stu-id="20a6f-121">(Optional) Usually 1 for mono or 2 for stereo, but can be up to 6 channels.</span></span><br/>                                                                                                                                                                                |
| [<span data-ttu-id="20a6f-122">**\_máscara de \_ canal de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="20a6f-122">**MF\_MT\_AUDIO\_CHANNEL\_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="20a6f-123">Adicional Normalmente 0x4 para mono ou 0x3 para estéreo, mas também pode ser qualquer uma das máscaras de canal associadas a até 6 canais (3/2/1, 3/2, 3/1, 2/2, 2/1).</span><span class="sxs-lookup"><span data-stu-id="20a6f-123">(Optional) Usually 0x4 for mono or 0x3 for stereo, but can also be any one of the channel masks associated with up to 6 channels (3/2/1, 3/2, 3/1, 2/2, 2/1).</span></span> <span data-ttu-id="20a6f-124">Se presente, a máscara de canal deve ser consistente com o número de entrada especificado de canais.</span><span class="sxs-lookup"><span data-stu-id="20a6f-124">If present, the channel mask must be consistent with the specified input number of channels.</span></span><br/> |
| [<span data-ttu-id="20a6f-125">**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="20a6f-125">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="20a6f-126">Adicional Um dos seguintes: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="20a6f-126">(Optional) One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span> <span data-ttu-id="20a6f-127">Se especificado, a taxa de amostragem de entrada deve ser uma das taxas de amostragem de MPEG válidas.</span><span class="sxs-lookup"><span data-stu-id="20a6f-127">If specified, the input sampling rate must be one of the valid MPEG sampling rates.</span></span><br/>                                                                                             |



 

## <a name="output-media-types"></a><span data-ttu-id="20a6f-128">Tipos de mídia de saída</span><span class="sxs-lookup"><span data-stu-id="20a6f-128">Output Media Types</span></span>

<span data-ttu-id="20a6f-129">O decodificador de áudio MPEG dará suporte a até quatro subtipos de mídia de saída, na seguinte ordem.</span><span class="sxs-lookup"><span data-stu-id="20a6f-129">The MPEG Audio decoder will support up to four output media subtypes, in the following order.</span></span>

<dl> 1. <span data-ttu-id="20a6f-130">Estéreo, ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="20a6f-130">Stereo, floating point.</span></span>  
2. <span data-ttu-id="20a6f-131">Estéreo de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="20a6f-131">Stereo, 16-bit PCM.</span></span>  
3. <span data-ttu-id="20a6f-132">Mono, ponto flutuante (somente se a entrada for mono ou dual-mono).</span><span class="sxs-lookup"><span data-stu-id="20a6f-132">Mono, floating point (only if the input is mono or dual-mono).</span></span>  
4. <span data-ttu-id="20a6f-133">Mono, PCM de 16 bits (somente se a entrada for mono ou dual-mono).</span><span class="sxs-lookup"><span data-stu-id="20a6f-133">Mono, 16-bit PCM (only if the input is mono or dual-mono).</span></span>  
</dl>

<span data-ttu-id="20a6f-134">O decodificador sempre dá suporte à saída de estéreo e é enumerado como o primeiro tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="20a6f-134">The decoder always supports stereo output and it is enumerated as the first output media type.</span></span>

<span data-ttu-id="20a6f-135">O decodificador dá suporte aos seguintes atributos de tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="20a6f-135">The decoder supports the following output media type attributes.</span></span>



| <span data-ttu-id="20a6f-136">Atributo</span><span class="sxs-lookup"><span data-stu-id="20a6f-136">Attribute</span></span>                                                                           | <span data-ttu-id="20a6f-137">Valor</span><span class="sxs-lookup"><span data-stu-id="20a6f-137">Value</span></span>                                                                      |
|-------------------------------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="20a6f-138">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="20a6f-138">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="20a6f-139">**\_Áudio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="20a6f-139">**MFMediaType\_Audio**</span></span>                                                     |
| [<span data-ttu-id="20a6f-140">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="20a6f-140">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="20a6f-141">**MFAudioFormat \_ PCM** ou **MFAudioFormat \_ float**</span><span class="sxs-lookup"><span data-stu-id="20a6f-141">Either **MFAudioFormat\_PCM** or **MFAudioFormat\_Float**</span></span>                  |
| [<span data-ttu-id="20a6f-142">\_bits de áudio MF MT \_ \_ \_ por \_ amostra</span><span class="sxs-lookup"><span data-stu-id="20a6f-142">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="20a6f-143">16 ou 32</span><span class="sxs-lookup"><span data-stu-id="20a6f-143">16 or 32</span></span>                                                                   |
| [<span data-ttu-id="20a6f-144">\_canais de \_ número de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="20a6f-144">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="20a6f-145">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="20a6f-145">1 or 2</span></span>                                                                     |
| [<span data-ttu-id="20a6f-146">\_máscara de \_ canal de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="20a6f-146">MF\_MT\_AUDIO\_CHANNEL\_MASK</span></span>](mf-mt-audio-channel-mask-attribute.md)              | <span data-ttu-id="20a6f-147">0x4 para mono ou 0x3 para estéreo</span><span class="sxs-lookup"><span data-stu-id="20a6f-147">0x4 for mono or 0x3 for stereo</span></span>                                             |
| [<span data-ttu-id="20a6f-148">\_amostras de áudio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="20a6f-148">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="20a6f-149">Um dos seguintes: 16000, 22050, 24000, 32000, 44100, 48000.</span><span class="sxs-lookup"><span data-stu-id="20a6f-149">One of the following: 16000, 22050, 24000, 32000, 44100, 48000.</span></span><br/> |



 

## <a name="transform-attributes"></a><span data-ttu-id="20a6f-150">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="20a6f-150">Transform Attributes</span></span>

<span data-ttu-id="20a6f-151">O decodificador de áudio MPEG implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="20a6f-151">The MPEG Audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="20a6f-152">Os aplicativos podem usar esse método para obter ou definir os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="20a6f-152">Applications can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="20a6f-153">Atributo</span><span class="sxs-lookup"><span data-stu-id="20a6f-153">Attribute</span></span>                                                                               | <span data-ttu-id="20a6f-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="20a6f-154">Description</span></span>                                                                                                                                                                                                                                                                                                  |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="20a6f-155">**CODECAPI \_ AVDecAudioDualMono**</span><span class="sxs-lookup"><span data-stu-id="20a6f-155">**CODECAPI\_AVDecAudioDualMono**</span></span>](../directshow/avdecaudiodualmono-property.md)                   | <span data-ttu-id="20a6f-156">Especifica se o áudio de 2 canais que está sendo decodificado é dual mono ou não.</span><span class="sxs-lookup"><span data-stu-id="20a6f-156">Specifies whether 2-channel audio being decoded is dual mono or not.</span></span> <span data-ttu-id="20a6f-157">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="20a6f-157">Read-only.</span></span> <span data-ttu-id="20a6f-158">Definido pelo MFT.</span><span class="sxs-lookup"><span data-stu-id="20a6f-158">Set by the MFT.</span></span> <span data-ttu-id="20a6f-159">Para obter mais informações, consulte [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="20a6f-159">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span>                                                                                                                               |
| [<span data-ttu-id="20a6f-160">**CODECAPI \_ AVDecAudioDualMonoReproMode**</span><span class="sxs-lookup"><span data-stu-id="20a6f-160">**CODECAPI\_AVDecAudioDualMonoReproMode**</span></span>](../directshow/avdecaudiodualmonorepromode-property.md) | <span data-ttu-id="20a6f-161">Especifica como o decodificador Reproduz áudio mono duplo.</span><span class="sxs-lookup"><span data-stu-id="20a6f-161">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="20a6f-162">O valor padrão é **eAVDecAudioDualMonoReproMode \_ esquerdo \_ mono**.</span><span class="sxs-lookup"><span data-stu-id="20a6f-162">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span><br/> <span data-ttu-id="20a6f-163">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="20a6f-163">Read/Write.</span></span> <span data-ttu-id="20a6f-164">Os aplicativos podem definir essa propriedade para alterar o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="20a6f-164">Applications can set this property to change the default behavior.</span></span> <span data-ttu-id="20a6f-165">Para obter mais informações, consulte [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span><span class="sxs-lookup"><span data-stu-id="20a6f-165">For more information see [**eAVDecAudioDualMono**](/windows/win32/api/codecapi/ne-codecapi-eavdecaudiodualmono).</span></span><br/> |
| [<span data-ttu-id="20a6f-166">**CODECAPI \_ AVEncCommonMeanBitRate**</span><span class="sxs-lookup"><span data-stu-id="20a6f-166">**CODECAPI\_AVEncCommonMeanBitRate**</span></span>](../directshow/avenccommonmeanbitrate-property.md)           | <span data-ttu-id="20a6f-167">Especifica a taxa de bits do fluxo compactado.</span><span class="sxs-lookup"><span data-stu-id="20a6f-167">Specifies the compressed stream bit rate.</span></span> <span data-ttu-id="20a6f-168">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="20a6f-168">Read-only.</span></span> <span data-ttu-id="20a6f-169">Definido pelo MFT.</span><span class="sxs-lookup"><span data-stu-id="20a6f-169">Set by the MFT.</span></span>                                                                                                                                                                                                                                         |



 

## <a name="see-also"></a><span data-ttu-id="20a6f-170">Confira também</span><span class="sxs-lookup"><span data-stu-id="20a6f-170">See also</span></span>

<dl> <dt>

[<span data-ttu-id="20a6f-171">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="20a6f-171">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
