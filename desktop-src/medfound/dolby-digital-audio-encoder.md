---
description: O decodificador de áudio Dolby é uma Media Foundation transformação (MFT) que codifica áudio mono ou estéreo em Dolby Digital, também chamada Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Codificador de áudio digital Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d6c5b59bc09cd8c0fd56f22703ef8afdfe3921
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105771267"
---
# <a name="dolby-digital-audio-encoder"></a><span data-ttu-id="3d920-103">Codificador de áudio digital Dolby</span><span class="sxs-lookup"><span data-stu-id="3d920-103">Dolby Digital Audio Encoder</span></span>

<span data-ttu-id="3d920-104">O decodificador de áudio Dolby é uma [Media Foundation transformação](media-foundation-transforms.md) (MFT) que codifica áudio mono ou estéreo em Dolby Digital, também chamada Dolby AC-3.</span><span class="sxs-lookup"><span data-stu-id="3d920-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that encodes mono or stereo audio to Dolby Digital, also called Dolby AC-3.</span></span> <span data-ttu-id="3d920-105">O codificador não oferece suporte à entrada de vários canais, como a configuração do canal 5,1.</span><span class="sxs-lookup"><span data-stu-id="3d920-105">The encoder does not support multi-channel input, such as the 5.1 channel configuration.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3d920-106">Para versões do Windows anteriores ao Windows 8, a implementação da Microsoft da tecnologia Dolby Digital é restrita em termos do programa Dolby Digital Licensing para uso pelos aplicativos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="3d920-106">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="3d920-107">Para obter mais informações sobre áudio Dolby Digital, consulte documento de compactação de áudio digital (ATSC) (Comitê de sistemas de televisão avançada) *padrão (AC-3, E-AC-3) revisão B*.</span><span class="sxs-lookup"><span data-stu-id="3d920-107">For more information about Dolby Digital audio, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="3d920-108">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="3d920-108">Class Identifier</span></span>

<span data-ttu-id="3d920-109">O CLSID (identificador de classe) do decodificador de áudio Dolby é **CLSID \_ CMSDolbyDigitalEncMFT**, definido no arquivo de cabeçalho wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="3d920-109">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDolbyDigitalEncMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="3d920-110">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="3d920-110">Output Types</span></span>

<span data-ttu-id="3d920-111">O tipo de saída deve ser definido primeiro, antes do tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="3d920-111">The output type must be set first, before the input type.</span></span> <span data-ttu-id="3d920-112">A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="3d920-112">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d920-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="3d920-113">Attribute</span></span></th>
<th><span data-ttu-id="3d920-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d920-114">Description</span></span></th>
<th><span data-ttu-id="3d920-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d920-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d920-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="3d920-116"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="3d920-117">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="3d920-117">Major type.</span></span></td>
<td><span data-ttu-id="3d920-118">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-118">Required.</span></span> <span data-ttu-id="3d920-119">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d920-119">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d920-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="3d920-120"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="3d920-121">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="3d920-121">Audio subtype.</span></span></td>
<td><span data-ttu-id="3d920-122">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-122">Required.</span></span> <span data-ttu-id="3d920-123">Deve ser <strong>MFAudioFormat_Dolby_AC3</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d920-123">Must be <strong>MFAudioFormat_Dolby_AC3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d920-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="3d920-124"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="3d920-125">Exemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="3d920-125">Samples per second.</span></span></td>
<td><span data-ttu-id="3d920-126">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-126">Required.</span></span> <span data-ttu-id="3d920-127">Os seguintes valores têm suporte:</span><span class="sxs-lookup"><span data-stu-id="3d920-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="3d920-128">32000</span><span class="sxs-lookup"><span data-stu-id="3d920-128">32000</span></span></li>
<li><span data-ttu-id="3d920-129">44100</span><span class="sxs-lookup"><span data-stu-id="3d920-129">44100</span></span></li>
<li><span data-ttu-id="3d920-130">48000</span><span class="sxs-lookup"><span data-stu-id="3d920-130">48000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d920-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="3d920-131"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="3d920-132">Número de canais.</span><span class="sxs-lookup"><span data-stu-id="3d920-132">Number of channels.</span></span></td>
<td><span data-ttu-id="3d920-133">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-133">Required.</span></span> <span data-ttu-id="3d920-134">Deve ser 1 (mono) ou 2 (estéreo).</span><span class="sxs-lookup"><span data-stu-id="3d920-134">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d920-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="3d920-135"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="3d920-136">Especifica a atribuição de canais de áudio a posições do orador.</span><span class="sxs-lookup"><span data-stu-id="3d920-136">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="3d920-137">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3d920-137">Optional.</span></span> <span data-ttu-id="3d920-138">Se definido, o valor deve ser 0x3 para estéreo (canais frontal esquerdo e direito) ou 0x4 para mono (canal do front Center).</span><span class="sxs-lookup"><span data-stu-id="3d920-138">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d920-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="3d920-139"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="3d920-140">Taxa de bits do fluxo AC-3 codificado, em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="3d920-140">Bit rate of the encoded AC-3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="3d920-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3d920-141">Optional.</span></span> <span data-ttu-id="3d920-142">Consulte comentários para obter os valores válidos.</span><span class="sxs-lookup"><span data-stu-id="3d920-142">See Remarks for valid values.</span></span> <span data-ttu-id="3d920-143">Se esse atributo não estiver definido, o codificador usará uma taxa de bits padrão, conforme descrito em comentários.</span><span class="sxs-lookup"><span data-stu-id="3d920-143">If this attribute is not set, the encoder uses a default bit rate, as described in Remarks.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3d920-144">Se os atributos opcionais não estiverem definidos, o codificador os adicionará ao tipo de mídia depois que o tipo for definido.</span><span class="sxs-lookup"><span data-stu-id="3d920-144">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="3d920-145">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="3d920-145">Input Types</span></span>

<span data-ttu-id="3d920-146">A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="3d920-146">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3d920-147">Atributo</span><span class="sxs-lookup"><span data-stu-id="3d920-147">Attribute</span></span></th>
<th><span data-ttu-id="3d920-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="3d920-148">Description</span></span></th>
<th><span data-ttu-id="3d920-149">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d920-149">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3d920-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="3d920-150"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="3d920-151">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="3d920-151">Major type.</span></span></td>
<td><span data-ttu-id="3d920-152">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-152">Required.</span></span> <span data-ttu-id="3d920-153">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d920-153">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d920-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="3d920-154"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="3d920-155">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="3d920-155">Audio subtype.</span></span></td>
<td><span data-ttu-id="3d920-156">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-156">Required.</span></span> <span data-ttu-id="3d920-157">Deve ser <strong>MFAudioFormat_PCM</strong> ou <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d920-157">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d920-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="3d920-158"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="3d920-159">Número de bits por amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="3d920-159">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="3d920-160">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-160">Required.</span></span> <span data-ttu-id="3d920-161">O valor deve ser 16 se o subtipo for <strong>MFAudioFormat_PCM</strong>ou 32 se o subtipo for <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="3d920-161">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d920-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="3d920-162"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="3d920-163">Exemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="3d920-163">Samples per second.</span></span></td>
<td><span data-ttu-id="3d920-164">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-164">Required.</span></span> <span data-ttu-id="3d920-165">Deve corresponder ao tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="3d920-165">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d920-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="3d920-166"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="3d920-167">Número de canais.</span><span class="sxs-lookup"><span data-stu-id="3d920-167">Number of channels.</span></span></td>
<td><span data-ttu-id="3d920-168">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-168">Required.</span></span> <span data-ttu-id="3d920-169">Deve corresponder ao tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="3d920-169">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d920-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="3d920-170"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="3d920-171">Alinhamento de bloco, em bytes.</span><span class="sxs-lookup"><span data-stu-id="3d920-171">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="3d920-172">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-172">Required.</span></span> <span data-ttu-id="3d920-173">Calcule o valor da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="3d920-173">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="3d920-174"><strong>MFAudioFormat_PCM</strong>: número de canais × 2.</span><span class="sxs-lookup"><span data-stu-id="3d920-174"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="3d920-175"><strong>MFAudioFormat_Float</strong>: número de canais × 4.</span><span class="sxs-lookup"><span data-stu-id="3d920-175"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d920-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="3d920-176"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="3d920-177">Taxa de bits do fluxo AC3 codificado, em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="3d920-177">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="3d920-178">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="3d920-178">Required.</span></span> <span data-ttu-id="3d920-179">Deve ser igual ao alinhamento de bloco × amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="3d920-179">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3d920-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="3d920-180"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="3d920-181">Especifica a atribuição de canais de áudio a posições do orador.</span><span class="sxs-lookup"><span data-stu-id="3d920-181">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="3d920-182">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3d920-182">Optional.</span></span> <span data-ttu-id="3d920-183">Se definido, o valor deve corresponder ao tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="3d920-183">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3d920-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="3d920-184"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="3d920-185">Número de bits válidos de dados de áudio em cada amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="3d920-185">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="3d920-186">Opcional.</span><span class="sxs-lookup"><span data-stu-id="3d920-186">Optional.</span></span> <span data-ttu-id="3d920-187">Se definido, o valor deve ser idêntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="3d920-187">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3d920-188">O codificador não oferece suporte à conversão de taxa de amostragem ou conversão estéreo/mono.</span><span class="sxs-lookup"><span data-stu-id="3d920-188">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span>

## <a name="remarks"></a><span data-ttu-id="3d920-189">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d920-189">Remarks</span></span>

<span data-ttu-id="3d920-190">Cada quadro de áudio Dolby AC-3 contém 1536 amostras de áudio por canal.</span><span class="sxs-lookup"><span data-stu-id="3d920-190">Each Dolby AC-3 audio frame contains 1536 audio samples per channel.</span></span> <span data-ttu-id="3d920-191">No entanto, cada buffer de entrada para o codificador pode conter qualquer número de amostras de PCM.</span><span class="sxs-lookup"><span data-stu-id="3d920-191">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="3d920-192">O tamanho de cada buffer de entrada deve ser um múltiplo do alinhamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="3d920-192">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="3d920-193">O codificador armazena em cache os exemplos de entrada até que ele tenha o suficiente para 1536 amostras de áudio por canal; em que ponto o codificador gera um quadro AC-3.</span><span class="sxs-lookup"><span data-stu-id="3d920-193">The encoder caches input samples until it has enough for 1536 audio samples per channel; at which point the encoder outputs one AC-3 frame.</span></span>

<span data-ttu-id="3d920-194">Cada buffer de saída contém um quadro bruto AC-3.</span><span class="sxs-lookup"><span data-stu-id="3d920-194">Each output buffer contains one raw AC-3 frame.</span></span> <span data-ttu-id="3d920-195">A duração é equivalente à duração de 1536 amostras de PCM na taxa de amostragem atual (32 ms) a taxa de amostragem de 48 kHz, 34,83 MS às 44,1 kHz e 48 mseg em 32 kHz).</span><span class="sxs-lookup"><span data-stu-id="3d920-195">The duration is equivalent to the duration of 1536 PCM samples at the current sampling rate (32 msec) at 48 kHz sample rate, 34.83 msec at 44.1 kHz, and 48 msec at 32 kHz).</span></span> <span data-ttu-id="3d920-196">O tamanho de cada buffer de saída depende da taxa de bits e da taxa de amostragem.</span><span class="sxs-lookup"><span data-stu-id="3d920-196">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

<span data-ttu-id="3d920-197">Para especificar a taxa de bits de codificação, defina o atributo [ \_ \_ vídeo \_ médio de \_ bytes \_ por \_ segundo do MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) no tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="3d920-197">To specify the encoding bit rate, set the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output type.</span></span> <span data-ttu-id="3d920-198">A tabela a seguir mostra a relação entre taxa de bits de codificação e \_ média de bytes de áudio MF MT \_ \_ \_ \_ por \_ segundo.</span><span class="sxs-lookup"><span data-stu-id="3d920-198">The following table shows the relation between encoding bit rate and MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND.</span></span>



| <span data-ttu-id="3d920-199">Taxa de bits (Kbps)</span><span class="sxs-lookup"><span data-stu-id="3d920-199">Bit rate (kbps)</span></span> | [<span data-ttu-id="3d920-200">áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="3d920-200">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="3d920-201">Comentários</span><span class="sxs-lookup"><span data-stu-id="3d920-201">Remarks</span></span>                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="3d920-202">64</span><span class="sxs-lookup"><span data-stu-id="3d920-202">64</span></span>              | <span data-ttu-id="3d920-203">8000</span><span class="sxs-lookup"><span data-stu-id="3d920-203">8000</span></span>                                                                                     | <span data-ttu-id="3d920-204">Somente mono.</span><span class="sxs-lookup"><span data-stu-id="3d920-204">Mono only.</span></span>                                              |
| <span data-ttu-id="3d920-205">80</span><span class="sxs-lookup"><span data-stu-id="3d920-205">80</span></span>              | <span data-ttu-id="3d920-206">10000</span><span class="sxs-lookup"><span data-stu-id="3d920-206">10000</span></span>                                                                                    | <span data-ttu-id="3d920-207">Somente mono.</span><span class="sxs-lookup"><span data-stu-id="3d920-207">Mono only.</span></span>                                              |
| <span data-ttu-id="3d920-208">96</span><span class="sxs-lookup"><span data-stu-id="3d920-208">96</span></span>              | <span data-ttu-id="3d920-209">12000</span><span class="sxs-lookup"><span data-stu-id="3d920-209">12000</span></span>                                                                                    | <span data-ttu-id="3d920-210">Somente mono.</span><span class="sxs-lookup"><span data-stu-id="3d920-210">Mono only.</span></span>                                              |
| <span data-ttu-id="3d920-211">112</span><span class="sxs-lookup"><span data-stu-id="3d920-211">112</span></span>             | <span data-ttu-id="3d920-212">14000</span><span class="sxs-lookup"><span data-stu-id="3d920-212">14000</span></span>                                                                                    | <span data-ttu-id="3d920-213">Somente mono.</span><span class="sxs-lookup"><span data-stu-id="3d920-213">Mono only.</span></span>                                              |
| <span data-ttu-id="3d920-214">128</span><span class="sxs-lookup"><span data-stu-id="3d920-214">128</span></span>             | <span data-ttu-id="3d920-215">16000</span><span class="sxs-lookup"><span data-stu-id="3d920-215">16000</span></span>                                                                                    | <span data-ttu-id="3d920-216">Mono ou estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d920-216">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="3d920-217">160</span><span class="sxs-lookup"><span data-stu-id="3d920-217">160</span></span>             | <span data-ttu-id="3d920-218">20000</span><span class="sxs-lookup"><span data-stu-id="3d920-218">20000</span></span>                                                                                    | <span data-ttu-id="3d920-219">Mono ou estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d920-219">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="3d920-220">192</span><span class="sxs-lookup"><span data-stu-id="3d920-220">192</span></span>             | <span data-ttu-id="3d920-221">24.000</span><span class="sxs-lookup"><span data-stu-id="3d920-221">24000</span></span>                                                                                    | <span data-ttu-id="3d920-222">Mono ou estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d920-222">Mono or stereo.</span></span> <span data-ttu-id="3d920-223">Essa é a configuração padrão para mono.</span><span class="sxs-lookup"><span data-stu-id="3d920-223">This is the default setting for mono.</span></span>   |
| <span data-ttu-id="3d920-224">224</span><span class="sxs-lookup"><span data-stu-id="3d920-224">224</span></span>             | <span data-ttu-id="3d920-225">28000</span><span class="sxs-lookup"><span data-stu-id="3d920-225">28000</span></span>                                                                                    | <span data-ttu-id="3d920-226">Mono ou estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d920-226">Mono or stereo.</span></span>                                         |
| <span data-ttu-id="3d920-227">256</span><span class="sxs-lookup"><span data-stu-id="3d920-227">256</span></span>             | <span data-ttu-id="3d920-228">32000</span><span class="sxs-lookup"><span data-stu-id="3d920-228">32000</span></span>                                                                                    | <span data-ttu-id="3d920-229">Mono ou estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d920-229">Mono or stereo.</span></span> <span data-ttu-id="3d920-230">Essa é a configuração padrão para estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d920-230">This is the default setting for stereo.</span></span> |
| <span data-ttu-id="3d920-231">320</span><span class="sxs-lookup"><span data-stu-id="3d920-231">320</span></span>             | <span data-ttu-id="3d920-232">40000</span><span class="sxs-lookup"><span data-stu-id="3d920-232">40000</span></span>                                                                                    | <span data-ttu-id="3d920-233">Somente estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d920-233">Stereo only.</span></span>                                            |
| <span data-ttu-id="3d920-234">384</span><span class="sxs-lookup"><span data-stu-id="3d920-234">384</span></span>             | <span data-ttu-id="3d920-235">48000</span><span class="sxs-lookup"><span data-stu-id="3d920-235">48000</span></span>                                                                                    | <span data-ttu-id="3d920-236">Somente estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d920-236">Stereo only.</span></span>                                            |
| <span data-ttu-id="3d920-237">448</span><span class="sxs-lookup"><span data-stu-id="3d920-237">448</span></span>             | <span data-ttu-id="3d920-238">56000</span><span class="sxs-lookup"><span data-stu-id="3d920-238">56000</span></span>                                                                                    | <span data-ttu-id="3d920-239">Somente estéreo.</span><span class="sxs-lookup"><span data-stu-id="3d920-239">Stereo only.</span></span>                                            |



 

<span data-ttu-id="3d920-240">A taxa de bits de codificação padrão é definida em 256 kbps para estéreo e 192 kbps para mono.</span><span class="sxs-lookup"><span data-stu-id="3d920-240">The default encoding bit rate is set at 256 kbps for stereo and 192 kbps for mono.</span></span> <span data-ttu-id="3d920-241">As configurações padrão são refletidas nos tipos de mídia retornados pelo método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) do codificador.</span><span class="sxs-lookup"><span data-stu-id="3d920-241">The default settings are reflected in the media types returned by the encoder's [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) method.</span></span>

### <a name="example-media-types"></a><span data-ttu-id="3d920-242">Exemplos de tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="3d920-242">Example Media Types</span></span>

<span data-ttu-id="3d920-243">Aqui está um exemplo dos tipos de mídia que são necessários para codificar o PCM de inteiros de 16 bits, áudio estéreo de 48 kHz na taxa de bits padrão de 256 kbps.</span><span class="sxs-lookup"><span data-stu-id="3d920-243">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate of 256 kbps.</span></span>

<span data-ttu-id="3d920-244">Tipo de mídia de saída:</span><span class="sxs-lookup"><span data-stu-id="3d920-244">Output media type:</span></span>

| <span data-ttu-id="3d920-245">Atributo</span><span class="sxs-lookup"><span data-stu-id="3d920-245">Attribute</span></span>                                                                           | <span data-ttu-id="3d920-246">Valor</span><span class="sxs-lookup"><span data-stu-id="3d920-246">Value</span></span>                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [<span data-ttu-id="3d920-247">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="3d920-247">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="3d920-248">**\_Áudio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3d920-248">**MFMediaType\_Audio**</span></span>        |
| [<span data-ttu-id="3d920-249">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="3d920-249">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="3d920-250">**MFAudioFormat \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="3d920-250">**MFAudioFormat\_Dolby\_AC3**</span></span> |
| [<span data-ttu-id="3d920-251">\_amostras de áudio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="3d920-251">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="3d920-252">48000</span><span class="sxs-lookup"><span data-stu-id="3d920-252">48000</span></span>                         |
| [<span data-ttu-id="3d920-253">\_canais de \_ número de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="3d920-253">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="3d920-254">2</span><span class="sxs-lookup"><span data-stu-id="3d920-254">2</span></span>                             |



 

<span data-ttu-id="3d920-255">Tipo de mídia de entrada:</span><span class="sxs-lookup"><span data-stu-id="3d920-255">Input media type:</span></span>

| <span data-ttu-id="3d920-256">Atributo</span><span class="sxs-lookup"><span data-stu-id="3d920-256">Attribute</span></span>                                                                                | <span data-ttu-id="3d920-257">Valor</span><span class="sxs-lookup"><span data-stu-id="3d920-257">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="3d920-258">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="3d920-258">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="3d920-259">**\_Áudio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="3d920-259">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="3d920-260">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="3d920-260">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="3d920-261">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="3d920-261">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="3d920-262">\_bits de áudio MF MT \_ \_ \_ por \_ amostra</span><span class="sxs-lookup"><span data-stu-id="3d920-262">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="3d920-263">16</span><span class="sxs-lookup"><span data-stu-id="3d920-263">16</span></span>                     |
| [<span data-ttu-id="3d920-264">\_amostras de áudio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="3d920-264">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="3d920-265">48000</span><span class="sxs-lookup"><span data-stu-id="3d920-265">48000</span></span>                  |
| [<span data-ttu-id="3d920-266">\_canais de \_ número de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="3d920-266">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="3d920-267">2</span><span class="sxs-lookup"><span data-stu-id="3d920-267">2</span></span>                      |
| [<span data-ttu-id="3d920-268">\_alinhamento de \_ bloco de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="3d920-268">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="3d920-269">4</span><span class="sxs-lookup"><span data-stu-id="3d920-269">4</span></span>                      |
| [<span data-ttu-id="3d920-270">áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="3d920-270">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="3d920-271">192000</span><span class="sxs-lookup"><span data-stu-id="3d920-271">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="3d920-272">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3d920-272">Requirements</span></span>



| <span data-ttu-id="3d920-273">Requisito</span><span class="sxs-lookup"><span data-stu-id="3d920-273">Requirement</span></span> | <span data-ttu-id="3d920-274">Valor</span><span class="sxs-lookup"><span data-stu-id="3d920-274">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d920-275">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d920-275">Minimum supported client</span></span><br/> | <span data-ttu-id="3d920-276">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="3d920-276">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                       |
| <span data-ttu-id="3d920-277">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="3d920-277">Minimum supported server</span></span><br/> | <span data-ttu-id="3d920-278">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="3d920-278">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3d920-279">DLL</span><span class="sxs-lookup"><span data-stu-id="3d920-279">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d920-280"><dt>Msac3enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d920-280"><dt>Msac3enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d920-281">Confira também</span><span class="sxs-lookup"><span data-stu-id="3d920-281">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d920-282">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="3d920-282">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 




