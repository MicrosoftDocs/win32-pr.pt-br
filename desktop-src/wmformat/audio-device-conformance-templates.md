---
title: Modelos de conformidade do dispositivo de áudio
description: Modelos de conformidade do dispositivo de áudio
ms.assetid: dad3dd2c-595e-45ce-bd84-2a20bc656cfb
keywords:
- SDK do Windows Media Format, modelos de conformidade do dispositivo
- ASF (Advanced Systems Format), modelos de conformidade do dispositivo
- ASF (formato de sistemas avançados), modelos de conformidade do dispositivo
- SDK do Windows Media Format, modelos de conformidade do dispositivo de áudio
- ASF (Advanced Systems Format), modelos de conformidade de dispositivo de áudio
- ASF (formato de sistemas avançados), modelos de conformidade de dispositivo de áudio
- Codec do Windows Media Audio 9, modelos de conformidade do dispositivo de áudio
- codecs, codec do Windows Media Audio 9
- modelos de conformidade do dispositivo, vídeo
- modelos de conformidade do dispositivo de áudio
- modelos, modelos de conformidade do dispositivo de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 39e1065395e64fdd2d8e60585900307a4dd3f39b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292163"
---
# <a name="audio-device-conformance-templates"></a><span data-ttu-id="675cb-114">Modelos de conformidade do dispositivo de áudio</span><span class="sxs-lookup"><span data-stu-id="675cb-114">Audio Device Conformance Templates</span></span>

<span data-ttu-id="675cb-115">A tabela a seguir lista os modelos de conformidade do dispositivo e os parâmetros associados para o codec do Windows Media Audio 9 ou posterior.</span><span class="sxs-lookup"><span data-stu-id="675cb-115">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 codec, or later.</span></span>



| <span data-ttu-id="675cb-116">Cadeia de caracteres do modelo</span><span class="sxs-lookup"><span data-stu-id="675cb-116">Template string</span></span> | <span data-ttu-id="675cb-117">Intervalo de taxa de bits</span><span class="sxs-lookup"><span data-stu-id="675cb-117">Bit rate range</span></span>     | <span data-ttu-id="675cb-118">Observações</span><span class="sxs-lookup"><span data-stu-id="675cb-118">Notes</span></span>                                                                                                                                                                                                                                |
|-----------------|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="675cb-119">L1</span><span class="sxs-lookup"><span data-stu-id="675cb-119">"L1"</span></span>            | <span data-ttu-id="675cb-120">64 Kbps 160 kbps</span><span class="sxs-lookup"><span data-stu-id="675cb-120">64 Kbps   160 Kbps</span></span> | <span data-ttu-id="675cb-121">Este modelo destina-se a dispositivos com somente áudio restrito.</span><span class="sxs-lookup"><span data-stu-id="675cb-121">This template is intended for constrained audio-only devices.</span></span>                                                                                                                                                                        |
| <span data-ttu-id="675cb-122">Cache</span><span class="sxs-lookup"><span data-stu-id="675cb-122">"L2"</span></span>            | <span data-ttu-id="675cb-123"><= 160 kbps</span><span class="sxs-lookup"><span data-stu-id="675cb-123"><= 160 Kbps</span></span>     | <span data-ttu-id="675cb-124">Este modelo corresponde à classe 4 no kit de portabilidade de áudio do Windows Media, que dá suporte a toda a implementação do decodificador de áudio do Windows Media.</span><span class="sxs-lookup"><span data-stu-id="675cb-124">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.</span></span>                                                                                   |
| <span data-ttu-id="675cb-125">MB</span><span class="sxs-lookup"><span data-stu-id="675cb-125">"L3"</span></span>            | <span data-ttu-id="675cb-126"><= 384 kbps</span><span class="sxs-lookup"><span data-stu-id="675cb-126"><= 384 Kbps</span></span>     | <span data-ttu-id="675cb-127">Este modelo corresponde à classe 4 no kit de portabilidade de áudio do Windows Media, que dá suporte a toda a implementação do decodificador de áudio do Windows Media. O intervalo de taxa de bits é a única diferença entre este modelo e o L2.</span><span class="sxs-lookup"><span data-stu-id="675cb-127">This template corresponds to Class 4 in the Windows Media Audio porting kit, which supports the entire Windows Media Audio decoder implementation.The bit rate range is the only difference between this template and L2.</span></span><br/> |
| <span data-ttu-id="675cb-128">Debug</span><span class="sxs-lookup"><span data-stu-id="675cb-128">"L"</span></span>             | <span data-ttu-id="675cb-129">Todas as taxas de bits</span><span class="sxs-lookup"><span data-stu-id="675cb-129">All bit rates</span></span>      | <span data-ttu-id="675cb-130">Este modelo é para uso apenas com computadores pessoais e é geralmente usado para demonstrar os recursos completos do codec.</span><span class="sxs-lookup"><span data-stu-id="675cb-130">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.</span></span>                                                                                                           |



 

<span data-ttu-id="675cb-131">A tabela a seguir lista os modelos de conformidade do dispositivo e os parâmetros associados para o codec de voz do Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="675cb-131">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Voice codec.</span></span>



| <span data-ttu-id="675cb-132">Cadeia de caracteres do modelo</span><span class="sxs-lookup"><span data-stu-id="675cb-132">Template string</span></span> | <span data-ttu-id="675cb-133">Intervalo de taxa de bits</span><span class="sxs-lookup"><span data-stu-id="675cb-133">Bit rate range</span></span> | <span data-ttu-id="675cb-134">Observações</span><span class="sxs-lookup"><span data-stu-id="675cb-134">Notes</span></span>                                                                                                                      |
|-----------------|----------------|----------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="675cb-135">S1</span><span class="sxs-lookup"><span data-stu-id="675cb-135">"S1"</span></span>            | <span data-ttu-id="675cb-136"><= 20 kbps</span><span class="sxs-lookup"><span data-stu-id="675cb-136"><= 20 Kbps</span></span>  | <span data-ttu-id="675cb-137">Este modelo destina-se apenas a dispositivos de baixa complexidade. Este modelo é somente fala.</span><span class="sxs-lookup"><span data-stu-id="675cb-137">This template is intended for very low-complexity devices only.This template is speech only.</span></span><br/>                    |
| <span data-ttu-id="675cb-138">S2</span><span class="sxs-lookup"><span data-stu-id="675cb-138">"S2"</span></span>            | <span data-ttu-id="675cb-139"><= 20 kbps</span><span class="sxs-lookup"><span data-stu-id="675cb-139"><= 20 Kbps</span></span>  | <span data-ttu-id="675cb-140">Esse é o modelo recomendado para a maioria dos aplicativos. Este modelo dá suporte a combinações de fala e música.</span><span class="sxs-lookup"><span data-stu-id="675cb-140">This is the recommended template for most applications.This template supports combinations of speech and music.</span></span><br/> |



 

<span data-ttu-id="675cb-141">A tabela a seguir lista os modelos de conformidade do dispositivo e os parâmetros associados para o codec do Windows Media Audio 9 Professional ou posterior.</span><span class="sxs-lookup"><span data-stu-id="675cb-141">The following table lists the device conformance templates and associated parameters for the Windows Media Audio 9 Professional codec, or later.</span></span>



| <span data-ttu-id="675cb-142">Cadeia de caracteres do modelo</span><span class="sxs-lookup"><span data-stu-id="675cb-142">Template string</span></span> | <span data-ttu-id="675cb-143">Propriedades</span><span class="sxs-lookup"><span data-stu-id="675cb-143">Properties</span></span>                                                                                   | <span data-ttu-id="675cb-144">Observações</span><span class="sxs-lookup"><span data-stu-id="675cb-144">Notes</span></span>                                                                                                                                                                                                                                           |
|-----------------|----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="675cb-145">M1</span><span class="sxs-lookup"><span data-stu-id="675cb-145">"M1"</span></span>            | <span data-ttu-id="675cb-146">Taxa de bits <= 384 taxa de KbpsSampling <= 48 kHz</span><span class="sxs-lookup"><span data-stu-id="675cb-146">Bit rate <= 384 KbpsSampling rate <= 48 kHz</span></span><br/> <span data-ttu-id="675cb-147">Canais <= 5,1</span><span class="sxs-lookup"><span data-stu-id="675cb-147">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="675cb-148">Esse modelo é recomendado para filmes padrão com Surround Sound.</span><span class="sxs-lookup"><span data-stu-id="675cb-148">This template is recommended for standard movies with surround sound.</span></span>                                                                                                                                                                           |
| <span data-ttu-id="675cb-149">M2</span><span class="sxs-lookup"><span data-stu-id="675cb-149">"M2"</span></span>            | <span data-ttu-id="675cb-150">Taxa de bits <= 768 taxa de KbpsSampling <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="675cb-150">Bit rate <= 768 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="675cb-151">Canais <= 5,1</span><span class="sxs-lookup"><span data-stu-id="675cb-151">Channels <= 5.1</span></span><br/>   | <span data-ttu-id="675cb-152">Esse modelo é recomendado para filmes de alta definição com som surround.</span><span class="sxs-lookup"><span data-stu-id="675cb-152">This template is recommended for high-definition movies with surround sound.</span></span>                                                                                                                                                                    |
| <span data-ttu-id="675cb-153">M3</span><span class="sxs-lookup"><span data-stu-id="675cb-153">"M3"</span></span>            | <span data-ttu-id="675cb-154">Taxa de bits <= 1.500 taxa de KbpsSampling <= 96 kHz</span><span class="sxs-lookup"><span data-stu-id="675cb-154">Bit rate <= 1,500 KbpsSampling rate <= 96 kHz</span></span><br/> <span data-ttu-id="675cb-155">Canais <= 7,1</span><span class="sxs-lookup"><span data-stu-id="675cb-155">Channels <= 7.1</span></span><br/> | <span data-ttu-id="675cb-156">Este modelo é recomendado para filmes de alta definição com som surround de 8 canais, como conteúdo codificado para apresentação em teatros.</span><span class="sxs-lookup"><span data-stu-id="675cb-156">This template is recommended for high-definition movies with 8-channel surround sound, such as content encoded for presentation in theaters.</span></span>                                                                                                    |
| <span data-ttu-id="675cb-157">“M”</span><span class="sxs-lookup"><span data-stu-id="675cb-157">"M"</span></span>             | <span data-ttu-id="675cb-158">Todas as taxas de amostragem de ratesAll de bits</span><span class="sxs-lookup"><span data-stu-id="675cb-158">All bit ratesAll sampling rates</span></span><br/> <span data-ttu-id="675cb-159">Todos os canais</span><span class="sxs-lookup"><span data-stu-id="675cb-159">All channels</span></span><br/>                           | <span data-ttu-id="675cb-160">Este modelo é para uso apenas com computadores pessoais e é geralmente usado para demonstrar os recursos completos do codec. Essa também é a designação de modelo para todos os áudios codificados com o codec Windows Media Audio 9 Lossless.</span><span class="sxs-lookup"><span data-stu-id="675cb-160">This template is for use with personal computers only, and is usually used to showcase the full capabilities of the codec.This is also the template designation for all audio encoded with the Windows Media Audio 9 Lossless codec.</span></span><br/> |



 

## <a name="related-topics"></a><span data-ttu-id="675cb-161">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="675cb-161">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="675cb-162">**Parâmetros do modelo de conformidade do dispositivo**</span><span class="sxs-lookup"><span data-stu-id="675cb-162">**Device Conformance Template Parameters**</span></span>](device-conformance-template-parameters.md)
</dt> <dt>

[<span data-ttu-id="675cb-163">**Combinações de modelo de conformidade do dispositivo recomendado**</span><span class="sxs-lookup"><span data-stu-id="675cb-163">**Recommended Device Conformance Template Combinations**</span></span>](recommended-device-conformance-template-combinations.md)
</dt> <dt>

[<span data-ttu-id="675cb-164">**Modelos de conformidade de dispositivo de vídeo**</span><span class="sxs-lookup"><span data-stu-id="675cb-164">**Video Device Conformance Templates**</span></span>](video-device-conformance-templates.md)
</dt> </dl>

 

 





