---
description: O codificador de áudio MPEG-2 Microsoft Media Foundation é uma transformação Media Foundation que codifica áudio mono ou estéreo em áudio MPEG-1 (ISO/IEC 11172-3) ou MPEG-2 Audio (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Codificador de áudio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827541"
---
# <a name="mpeg-2-audio-encoder"></a><span data-ttu-id="003e6-103">Codificador de áudio MPEG-2</span><span class="sxs-lookup"><span data-stu-id="003e6-103">MPEG-2 Audio Encoder</span></span>

<span data-ttu-id="003e6-104">O codificador de áudio MPEG-2 Microsoft Media Foundation é uma [transformação Media Foundation](media-foundation-transforms.md) que codifica áudio mono ou estéreo em áudio MPEG-1 (ISO/IEC 11172-3) ou MPEG-2 Audio (ISO/IEC 13818-3).</span><span class="sxs-lookup"><span data-stu-id="003e6-104">The Microsoft Media Foundation MPEG-2 audio encoder is a [Media Foundation transform](media-foundation-transforms.md) that encodes mono or stereo audio to MPEG-1 audio (ISO/IEC 11172-3) or MPEG-2 audio (ISO/IEC 13818-3).</span></span>

<span data-ttu-id="003e6-105">O codificador dá suporte a áudio de camada 1 e camada 2.</span><span class="sxs-lookup"><span data-stu-id="003e6-105">The encoder supports Layer 1 and Layer 2 audio.</span></span> <span data-ttu-id="003e6-106">Ele não dá suporte a áudio MPEG-Layer 3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="003e6-106">It does not support MPEG-Layer 3 (MP3) audio.</span></span> <span data-ttu-id="003e6-107">Para MPEG-2, o codificador dá suporte à parte de LSF (frequências de amostragem baixa) de áudio MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="003e6-107">For MPEG-2, the encoder supports the Low Sampling Frequencies (LSF) portion of MPEG-2 audio.</span></span> <span data-ttu-id="003e6-108">Ele não oferece suporte às extensões de multicanal.</span><span class="sxs-lookup"><span data-stu-id="003e6-108">It does not support the multichannel extensions.</span></span> <span data-ttu-id="003e6-109">O MFT gera um fluxo elementar MPEG.</span><span class="sxs-lookup"><span data-stu-id="003e6-109">The MFT outputs an MPEG elementary stream.</span></span> <span data-ttu-id="003e6-110">Ele não pode gerar fluxos elementares, fluxos de programa ou fluxos de transporte em pacotes.</span><span class="sxs-lookup"><span data-stu-id="003e6-110">It cannot generate packetized elementary streams, program streams, or transport streams.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="003e6-111">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="003e6-111">Class Identifier</span></span>

<span data-ttu-id="003e6-112">O CLSID (identificador de classe) do codificador de áudio MEPG-2 é **CLSID \_ CMPEG2AudioEncoderMFT**, definido no arquivo de cabeçalho wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="003e6-112">The class identifier (CLSID) of the MEPG-2 audio encoder is **CLSID\_CMPEG2AudioEncoderMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="output-types"></a><span data-ttu-id="003e6-113">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="003e6-113">Output Types</span></span>

<span data-ttu-id="003e6-114">O tipo de saída deve ser definido primeiro, antes do tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="003e6-114">The output type must be set first, before the input type.</span></span> <span data-ttu-id="003e6-115">A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="003e6-115">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="003e6-116">Atributo</span><span class="sxs-lookup"><span data-stu-id="003e6-116">Attribute</span></span></th>
<th><span data-ttu-id="003e6-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="003e6-117">Description</span></span></th>
<th><span data-ttu-id="003e6-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="003e6-118">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="003e6-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="003e6-119"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="003e6-120">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="003e6-120">Major type.</span></span></td>
<td><span data-ttu-id="003e6-121">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-121">Required.</span></span> <span data-ttu-id="003e6-122">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="003e6-122">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003e6-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="003e6-123"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="003e6-124">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="003e6-124">Audio subtype.</span></span></td>
<td><span data-ttu-id="003e6-125">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-125">Required.</span></span> <span data-ttu-id="003e6-126">Deve ser <strong>MFAudioFormat_MPEG</strong>.</span><span class="sxs-lookup"><span data-stu-id="003e6-126">Must be <strong>MFAudioFormat_MPEG</strong>.</span></span> <span data-ttu-id="003e6-127">Esse subtipo é usado para áudio MPEG-1 e MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="003e6-127">This subtype is used for both MPEG-1 and MPEG-2 audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="003e6-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="003e6-128"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="003e6-129">Exemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-129">Samples per second.</span></span></td>
<td><span data-ttu-id="003e6-130">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-130">Required.</span></span> <span data-ttu-id="003e6-131">Os valores a seguir têm suporte para MPEG-1 e MPEG-2:</span><span class="sxs-lookup"><span data-stu-id="003e6-131">The following values are supported for both MPEG-1 and MPEG-2:</span></span>
<ul>
<li><span data-ttu-id="003e6-132">32000</span><span class="sxs-lookup"><span data-stu-id="003e6-132">32000</span></span></li>
<li><span data-ttu-id="003e6-133">44100</span><span class="sxs-lookup"><span data-stu-id="003e6-133">44100</span></span></li>
<li><span data-ttu-id="003e6-134">48000</span><span class="sxs-lookup"><span data-stu-id="003e6-134">48000</span></span></li>
</ul>
<span data-ttu-id="003e6-135">Além disso, os seguintes valores têm suporte para LSF MPEG-2:</span><span class="sxs-lookup"><span data-stu-id="003e6-135">In addition, the following values are supported for MPEG-2 LSF:</span></span> <br/>
<ul>
<li><span data-ttu-id="003e6-136">16000</span><span class="sxs-lookup"><span data-stu-id="003e6-136">16000</span></span></li>
<li><span data-ttu-id="003e6-137">22050</span><span class="sxs-lookup"><span data-stu-id="003e6-137">22050</span></span></li>
<li><span data-ttu-id="003e6-138">24.000</span><span class="sxs-lookup"><span data-stu-id="003e6-138">24000</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003e6-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="003e6-139"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="003e6-140">Número de canais.</span><span class="sxs-lookup"><span data-stu-id="003e6-140">Number of channels.</span></span></td>
<td><span data-ttu-id="003e6-141">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-141">Required.</span></span> <span data-ttu-id="003e6-142">Deve ser 1 (mono) ou 2 (estéreo).</span><span class="sxs-lookup"><span data-stu-id="003e6-142">Must be either 1 (mono) or 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="003e6-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="003e6-143"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="003e6-144">Especifica a atribuição de canais de áudio a posições do orador.</span><span class="sxs-lookup"><span data-stu-id="003e6-144">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="003e6-145">Opcional.</span><span class="sxs-lookup"><span data-stu-id="003e6-145">Optional.</span></span> <span data-ttu-id="003e6-146">Se definido, o valor deve ser 0x3 para estéreo (canais frontal esquerdo e direito) ou 0x4 para mono (canal do front Center).</span><span class="sxs-lookup"><span data-stu-id="003e6-146">If set, the value must be 0x3 for stereo (front left and right channels) or 0x4 for mono (front center channel).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003e6-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="003e6-147"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="003e6-148">Taxa de bits do fluxo MPEG codificado, em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-148">Bit rate of the encoded MPEG stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="003e6-149">Opcional.</span><span class="sxs-lookup"><span data-stu-id="003e6-149">Optional.</span></span><br/> <span data-ttu-id="003e6-150">As especificações de ISO/IEC 11172-3 e ISO/IEC 13818-3 (LSF) definem várias taxas de bits, dependendo da taxa de amostragem, do número de canais e da camada de áudio (1 ou 2).</span><span class="sxs-lookup"><span data-stu-id="003e6-150">The ISO/IEC 11172-3 and ISO/IEC 13818-3 (LSF) specifications define several bit rates, depending on the sampling rate, the number of channels, and the audio layer (1 or 2).</span></span> <br/> <span data-ttu-id="003e6-151">O codificador assume como padrão o áudio de camada 2.</span><span class="sxs-lookup"><span data-stu-id="003e6-151">The encoder defaults to Layer 2 audio.</span></span> <span data-ttu-id="003e6-152">Se o atributo <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> não estiver definido, o codificador usará as seguintes taxas de bits padrão:</span><span class="sxs-lookup"><span data-stu-id="003e6-152">If the <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> attribute is not set, the encoder uses the following default bit rates:</span></span><br/>
<ul>
<li><span data-ttu-id="003e6-153">MPEG-1 estéreo: 224.000 bits por segundo (bps) = 28.000 bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-153">MPEG-1 stereo: 224,000 bits per second (bps) = 28,000 bytes per second.</span></span></li>
<li><span data-ttu-id="003e6-154">MPEG-1 mono: 192.000 bps = 24.000 bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-154">MPEG-1 mono: 192,000 bps = 24,000 bytes per second.</span></span></li>
<li><span data-ttu-id="003e6-155">MPEG-2 LSF, mono ou estéreo: 160.000 bps = 20.000 bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-155">MPEG-2 LSF, mono or stereo: 160,000 bps = 20,000 bytes per second.</span></span></li>
</ul>
<span data-ttu-id="003e6-156">Esse atributo pode ser definido como outros valores.</span><span class="sxs-lookup"><span data-stu-id="003e6-156">This attribute can be set to other values.</span></span> <span data-ttu-id="003e6-157">Se o valor não for válido de acordo com as especificações MPEG, o MFT rejeitará o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="003e6-157">If the value is not valid according to MPEG specifications, the MFT will reject the media type.</span></span><br/> <span data-ttu-id="003e6-158">Você também pode definir a taxa de bits usando a interface <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> .</span><span class="sxs-lookup"><span data-stu-id="003e6-158">You can also set the bit rate by using the <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> interface.</span></span> <span data-ttu-id="003e6-159">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="003e6-159">See Remarks for more information.</span></span><br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="003e6-160">Se os atributos opcionais não estiverem definidos, o codificador os adicionará ao tipo de mídia depois que o tipo for definido.</span><span class="sxs-lookup"><span data-stu-id="003e6-160">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="input-types"></a><span data-ttu-id="003e6-161">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="003e6-161">Input Types</span></span>

<span data-ttu-id="003e6-162">A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="003e6-162">The following table lists the required and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="003e6-163">Atributo</span><span class="sxs-lookup"><span data-stu-id="003e6-163">Attribute</span></span></th>
<th><span data-ttu-id="003e6-164">Descrição</span><span class="sxs-lookup"><span data-stu-id="003e6-164">Description</span></span></th>
<th><span data-ttu-id="003e6-165">Comentários</span><span class="sxs-lookup"><span data-stu-id="003e6-165">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="003e6-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="003e6-166"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="003e6-167">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="003e6-167">Major type.</span></span></td>
<td><span data-ttu-id="003e6-168">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-168">Required.</span></span> <span data-ttu-id="003e6-169">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="003e6-169">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003e6-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="003e6-170"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="003e6-171">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="003e6-171">Audio subtype.</span></span></td>
<td><span data-ttu-id="003e6-172">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-172">Required.</span></span> <span data-ttu-id="003e6-173">Deve ser <strong>MFAudioFormat_PCM</strong> ou <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="003e6-173">Must be <strong>MFAudioFormat_PCM</strong> or <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="003e6-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="003e6-174"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="003e6-175">Número de bits por amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="003e6-175">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="003e6-176">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-176">Required.</span></span> <span data-ttu-id="003e6-177">O valor deve ser 16 se o subtipo for <strong>MFAudioFormat_PCM</strong>ou 32 se o subtipo for <strong>MFAudioFormat_Float</strong>.</span><span class="sxs-lookup"><span data-stu-id="003e6-177">The value must be 16 if the subtype is <strong>MFAudioFormat_PCM</strong>, or 32 if the subtype is <strong>MFAudioFormat_Float</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003e6-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="003e6-178"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="003e6-179">Exemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-179">Samples per second.</span></span></td>
<td><span data-ttu-id="003e6-180">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-180">Required.</span></span> <span data-ttu-id="003e6-181">Deve corresponder ao tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="003e6-181">Must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="003e6-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="003e6-182"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="003e6-183">Número de canais.</span><span class="sxs-lookup"><span data-stu-id="003e6-183">Number of channels.</span></span></td>
<td><span data-ttu-id="003e6-184">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-184">Required.</span></span> <span data-ttu-id="003e6-185">Deve corresponder ao tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="003e6-185">Must match the output type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003e6-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="003e6-186"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="003e6-187">Alinhamento de bloco, em bytes.</span><span class="sxs-lookup"><span data-stu-id="003e6-187">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="003e6-188">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-188">Required.</span></span> <span data-ttu-id="003e6-189">Calcule o valor da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="003e6-189">Calculate the value as follows:</span></span>
<ul>
<li><span data-ttu-id="003e6-190"><strong>MFAudioFormat_PCM</strong>: número de canais × 2.</span><span class="sxs-lookup"><span data-stu-id="003e6-190"><strong>MFAudioFormat_PCM</strong>: Number of channels × 2.</span></span></li>
<li><span data-ttu-id="003e6-191"><strong>MFAudioFormat_Float</strong>: número de canais × 4.</span><span class="sxs-lookup"><span data-stu-id="003e6-191"><strong>MFAudioFormat_Float</strong>: Number of channels × 4.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="003e6-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="003e6-192"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="003e6-193">Taxa de bits do fluxo AC3 codificado, em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-193">Bit rate of the encoded AC3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="003e6-194">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="003e6-194">Required.</span></span> <span data-ttu-id="003e6-195">Deve ser igual ao alinhamento de bloco × amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-195">Must equal block alignment × samples per second.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="003e6-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="003e6-196"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="003e6-197">Especifica a atribuição de canais de áudio a posições do orador.</span><span class="sxs-lookup"><span data-stu-id="003e6-197">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="003e6-198">Opcional.</span><span class="sxs-lookup"><span data-stu-id="003e6-198">Optional.</span></span> <span data-ttu-id="003e6-199">Se definido, o valor deve corresponder ao tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="003e6-199">If set, the value must match the output type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="003e6-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="003e6-200"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="003e6-201">Número de bits válidos de dados de áudio em cada amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="003e6-201">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="003e6-202">Opcional.</span><span class="sxs-lookup"><span data-stu-id="003e6-202">Optional.</span></span> <span data-ttu-id="003e6-203">Se definido, o valor deve ser idêntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="003e6-203">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="003e6-204">O codificador não oferece suporte à conversão de taxa de amostragem ou conversão estéreo/mono.</span><span class="sxs-lookup"><span data-stu-id="003e6-204">The encoder does not support sample-rate conversion or stereo/mono conversion.</span></span> <span data-ttu-id="003e6-205">Se os atributos opcionais não estiverem definidos, o codificador os adicionará ao tipo de mídia depois que o tipo for definido.</span><span class="sxs-lookup"><span data-stu-id="003e6-205">If the optional attributes are not set, the encoder adds them to the media type after the type is set.</span></span>

## <a name="codec-properties"></a><span data-ttu-id="003e6-206">Propriedades do codec</span><span class="sxs-lookup"><span data-stu-id="003e6-206">Codec Properties</span></span>

<span data-ttu-id="003e6-207">O codificador dá suporte às seguintes propriedades por meio da interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="003e6-207">The encoder supports the following properties through the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface.</span></span>



| <span data-ttu-id="003e6-208">Propriedade</span><span class="sxs-lookup"><span data-stu-id="003e6-208">Property</span></span>                                                                                | <span data-ttu-id="003e6-209">Descrição</span><span class="sxs-lookup"><span data-stu-id="003e6-209">Description</span></span>                                                                                      | <span data-ttu-id="003e6-210">Valor padrão</span><span class="sxs-lookup"><span data-stu-id="003e6-210">Default value</span></span>                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="003e6-211">CODECAPI \_ AVEncCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="003e6-211">CODECAPI\_AVEncCommonMeanBitRate</span></span>](../directshow/avenccommonmeanbitrate-property.md)               | <span data-ttu-id="003e6-212">Especifica a taxa média de bits codificada, em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-212">Specifies the average encoded bit rate, in bits per second.</span></span>                                      | <span data-ttu-id="003e6-213">Conforme descrito para o atributo de [ \_ \_ \_ bytes médios \_ \_ por \_ segundo do áudio MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="003e6-213">As described for the [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute in the output media type.</span></span>                      |
| [<span data-ttu-id="003e6-214">CODECAPI \_ AVEncMPACodingMode</span><span class="sxs-lookup"><span data-stu-id="003e6-214">CODECAPI\_AVEncMPACodingMode</span></span>](../directshow/avencmpacodingmode-property.md)                       | <span data-ttu-id="003e6-215">Especifica o modo de codificação de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="003e6-215">Specifies the MPEG audio encoding mode.</span></span>                                                          | <span data-ttu-id="003e6-216">Estéreo para áudio de 2 canais ou canal único para áudio de 1 canal.</span><span class="sxs-lookup"><span data-stu-id="003e6-216">Stereo for 2-channel audio, or single channel for 1-channel audio.</span></span><br/> <span data-ttu-id="003e6-217">Para áudio de 2 canais, o codificador também dá suporte a canal duplo e estéreo conjunta.</span><span class="sxs-lookup"><span data-stu-id="003e6-217">For 2-channel audio, the encoder also supports dual channel and joint stereo.</span></span><br/> |
| [<span data-ttu-id="003e6-218">CODECAPI \_ AVEncMPACopyright</span><span class="sxs-lookup"><span data-stu-id="003e6-218">CODECAPI\_AVEncMPACopyright</span></span>](../directshow/avencmpacopyright-property.md)                         | <span data-ttu-id="003e6-219">Especifica se o bit de direitos autorais deve ser definido no fluxo de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="003e6-219">Specifies whether to set the copyright bit in the MPEG audio stream.</span></span>                             | <span data-ttu-id="003e6-220">Sem direitos autorais.</span><span class="sxs-lookup"><span data-stu-id="003e6-220">No copyright.</span></span>                                                                                                                                                          |
| [<span data-ttu-id="003e6-221">CODECAPI \_ AVEncMPAEmphasisType</span><span class="sxs-lookup"><span data-stu-id="003e6-221">CODECAPI\_AVEncMPAEmphasisType</span></span>](../directshow/avencmpaemphasistype-property.md)                   | <span data-ttu-id="003e6-222">Especifica o tipo de filtro de ênfase que deve ser usado quando o fluxo codificado é decodificado.</span><span class="sxs-lookup"><span data-stu-id="003e6-222">Specifies the type of de-emphasis filter that should be used when the encoded stream is decoded.</span></span> | <span data-ttu-id="003e6-223">Nenhuma ênfase especificada.</span><span class="sxs-lookup"><span data-stu-id="003e6-223">No emphasis specified.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="003e6-224">AVEncMPAEnableRedundancyProtection</span><span class="sxs-lookup"><span data-stu-id="003e6-224">AVEncMPAEnableRedundancyProtection</span></span>](../directshow/avencmpaenableredundancyprotection-property.md) | <span data-ttu-id="003e6-225">Especifica se uma CRC (verificação de redundância cíclica) deve ser adicionada ao cabeçalho do quadro.</span><span class="sxs-lookup"><span data-stu-id="003e6-225">Specifies whether to add a cyclic redundancy check (CRC) to the frame header.</span></span>                    | <span data-ttu-id="003e6-226">Uma soma de verificação de CRC é gravada no fluxo de bits.</span><span class="sxs-lookup"><span data-stu-id="003e6-226">A CRC checksum is written to the bit stream.</span></span>                                                                                                                           |
| [<span data-ttu-id="003e6-227">CODECAPI \_ AVEncMPALayer</span><span class="sxs-lookup"><span data-stu-id="003e6-227">CODECAPI\_AVEncMPALayer</span></span>](../directshow/avencmpalayer-property.md)                                 | <span data-ttu-id="003e6-228">Especifica a camada de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="003e6-228">Specifies the MPEG audio layer.</span></span>                                                                  | <span data-ttu-id="003e6-229">Áudio de camada 2.</span><span class="sxs-lookup"><span data-stu-id="003e6-229">Layer 2 audio.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="003e6-230">CODECAPI \_ AVEncMPAOriginalBitstream</span><span class="sxs-lookup"><span data-stu-id="003e6-230">CODECAPI\_AVEncMPAOriginalBitstream</span></span>](../directshow/avencmpaoriginalbitstream-property.md)         | <span data-ttu-id="003e6-231">Especifica se deve ser definido para o bit original no fluxo de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="003e6-231">Specifies whether to set for the original bit in the MPEG audio stream.</span></span>                          | <span data-ttu-id="003e6-232">O bit "original" está desativado.</span><span class="sxs-lookup"><span data-stu-id="003e6-232">"Original" bit is off.</span></span>                                                                                                                                                 |
| [<span data-ttu-id="003e6-233">CODECAPI \_ AVEncMPAPrivateUserBit</span><span class="sxs-lookup"><span data-stu-id="003e6-233">CODECAPI\_AVEncMPAPrivateUserBit</span></span>](../directshow/avencmpaprivateuserbit-property.md)               | <span data-ttu-id="003e6-234">Especifica se deve ser definido para o bit do usuário privado no fluxo de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="003e6-234">Specifies whether to set for the private user bit in the MPEG audio stream.</span></span>                      | <span data-ttu-id="003e6-235">O bit de usuário privado está desativado.</span><span class="sxs-lookup"><span data-stu-id="003e6-235">Private user bit is off.</span></span>                                                                                                                                               |



 

<span data-ttu-id="003e6-236">Para obter um ponteiro para a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) , chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no MFT.</span><span class="sxs-lookup"><span data-stu-id="003e6-236">To get a pointer to the [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) interface, call [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) on the MFT.</span></span>

<span data-ttu-id="003e6-237">A MFT implementa os seguintes métodos [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :</span><span class="sxs-lookup"><span data-stu-id="003e6-237">The MFT implements the following [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods:</span></span>

-   [<span data-ttu-id="003e6-238">**GetParameterRange**</span><span class="sxs-lookup"><span data-stu-id="003e6-238">**GetParameterRange**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [<span data-ttu-id="003e6-239">**Parameters**</span><span class="sxs-lookup"><span data-stu-id="003e6-239">**GetParameterValues**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [<span data-ttu-id="003e6-240">**GetValue**</span><span class="sxs-lookup"><span data-stu-id="003e6-240">**GetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [<span data-ttu-id="003e6-241">**Ismodificável**</span><span class="sxs-lookup"><span data-stu-id="003e6-241">**IsModifiable**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [<span data-ttu-id="003e6-242">**IsSupported**</span><span class="sxs-lookup"><span data-stu-id="003e6-242">**IsSupported**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [<span data-ttu-id="003e6-243">**SetValue**</span><span class="sxs-lookup"><span data-stu-id="003e6-243">**SetValue**</span></span>](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

<span data-ttu-id="003e6-244">Todos os outros métodos [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retornam **E \_ NOTIMPL**.</span><span class="sxs-lookup"><span data-stu-id="003e6-244">All other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) methods return **E\_NOTIMPL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="003e6-245">Comentários</span><span class="sxs-lookup"><span data-stu-id="003e6-245">Remarks</span></span>

<span data-ttu-id="003e6-246">Cada quadro de áudio MPEG contém exemplos de áudio 384 (camada 1) ou 1152 (camada 2) por canal.</span><span class="sxs-lookup"><span data-stu-id="003e6-246">Each MPEG audio frame contains either 384 (Layer 1) or 1152 (Layer 2) audio samples per channel.</span></span> <span data-ttu-id="003e6-247">No entanto, cada buffer de entrada para o codificador pode conter qualquer número de amostras de PCM.</span><span class="sxs-lookup"><span data-stu-id="003e6-247">However, each input buffer to the encoder may contain any number of PCM samples.</span></span> <span data-ttu-id="003e6-248">O tamanho de cada buffer de entrada deve ser um múltiplo do alinhamento de bloco.</span><span class="sxs-lookup"><span data-stu-id="003e6-248">The size of each input buffer must be a multiple of the block alignment.</span></span> <span data-ttu-id="003e6-249">O codificador armazena em cache os exemplos de entrada até que ele tenha o suficiente para um quadro de áudio MPEG.</span><span class="sxs-lookup"><span data-stu-id="003e6-249">The encoder caches input samples until it has enough for an MPEG audio frame.</span></span>

<span data-ttu-id="003e6-250">Cada buffer de saída contém um quadro MPEG bruto.</span><span class="sxs-lookup"><span data-stu-id="003e6-250">Each output buffer contains one raw MPEG frame.</span></span> <span data-ttu-id="003e6-251">O tamanho de cada buffer de saída depende da taxa de bits e da taxa de amostragem.</span><span class="sxs-lookup"><span data-stu-id="003e6-251">The size of each output buffer depends on the bit rate and the sample rate.</span></span>

### <a name="configuring-the-encoder"></a><span data-ttu-id="003e6-252">Configurando o codificador</span><span class="sxs-lookup"><span data-stu-id="003e6-252">Configuring the Encoder</span></span>

<span data-ttu-id="003e6-253">Para alterar as configurações padrão no codificador, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="003e6-253">To change any of the default settings on the encoder, perform the following steps:</span></span>

1.  <span data-ttu-id="003e6-254">Crie uma instância do MFT do codificador.</span><span class="sxs-lookup"><span data-stu-id="003e6-254">Create an instance of the encoder MFT.</span></span>
2.  <span data-ttu-id="003e6-255">Chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter a lista dos tipos de saída preferenciais.</span><span class="sxs-lookup"><span data-stu-id="003e6-255">Call [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) to get the list of the preferred output types.</span></span> <span data-ttu-id="003e6-256">O codificador enumera todas as taxas de exemplo para mono e estéreo.</span><span class="sxs-lookup"><span data-stu-id="003e6-256">The encoder enumerates all sample rates for both mono and stereo.</span></span> <span data-ttu-id="003e6-257">Selecione um desses tipos de mídia, com base na taxa de amostra e no número de canais.</span><span class="sxs-lookup"><span data-stu-id="003e6-257">Select one of these media types, based on the sample rate and number of channels.</span></span> <span data-ttu-id="003e6-258">O atributo de [ \_ \_ \_ bytes médios \_ \_ por \_ segundo do áudio MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) indica a taxa de bits padrão, em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="003e6-258">The [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) attribute indicates the default bit rate, in bytes per second.</span></span>
3.  <span data-ttu-id="003e6-259">Opcional: você pode substituir a taxa de bits padrão definindo um novo valor para [áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="003e6-259">Optional: You can override the default bit rate by setting a new value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) on the output media type.</span></span> <span data-ttu-id="003e6-260">As taxas de bits válidas dependem da taxa de amostragem, do número de canais e da camada de áudio.</span><span class="sxs-lookup"><span data-stu-id="003e6-260">Valid bit rates depend on the sample rate, number of channels, and audio layer.</span></span>
    > [!Note]  
    > <span data-ttu-id="003e6-261">Neste ponto do processo de configuração, o codificador assume como padrão o áudio de camada 2 e só aceitará taxas de bits de camada 2.</span><span class="sxs-lookup"><span data-stu-id="003e6-261">At this point in the configuration process, the encoder defaults to Layer 2 audio and will only accept Layer 2 bit rates.</span></span> <span data-ttu-id="003e6-262">Você poderá alternar o codificador para a camada 1 em uma etapa posterior (consulte a etapa 7).</span><span class="sxs-lookup"><span data-stu-id="003e6-262">You will be able to switch the encoder to Layer 1 in a later step (see step 7).</span></span> <span data-ttu-id="003e6-263">Nesse caso, deixe a taxa de bits padrão por enquanto; Você pode alterá-lo novamente na etapa 8.</span><span class="sxs-lookup"><span data-stu-id="003e6-263">In that case, leave the default bit rate for now; you can change it again in step 8.</span></span>

     

4.  <span data-ttu-id="003e6-264">Chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="003e6-264">Call [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) to set the output media type.</span></span> <span data-ttu-id="003e6-265">Se você definir seu próprio valor para [o \_ áudio MF MT \_ \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) e o MFT rejeitar o tipo de mídia de saída, é provável que você tenha especificado uma taxa de bits inválida.</span><span class="sxs-lookup"><span data-stu-id="003e6-265">If you set your own value for [MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) and the MFT rejects the output media type, it is likely because you specified an invalid bit rate.</span></span>
5.  <span data-ttu-id="003e6-266">Chame [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para enumerar o tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="003e6-266">Call [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) to enumerate the input media type.</span></span> <span data-ttu-id="003e6-267">Como a taxa de amostra e o número de canais devem ser idênticos ao tipo de saída, somente duas opções são enumeradas: entrada PCM de ponto flutuante de 32 bits e entrada PCM de inteiro de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="003e6-267">Because the sample rate and number of channels must be identical to the output type, only two options are enumerated: 32-bit floating-point PCM input and 16-bit integer PCM input.</span></span> <span data-ttu-id="003e6-268">Selecione um deles.</span><span class="sxs-lookup"><span data-stu-id="003e6-268">Select one of these.</span></span>
6.  <span data-ttu-id="003e6-269">Chame [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="003e6-269">Call [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) to set the input media type.</span></span>
7.  <span data-ttu-id="003e6-270">Opcional: para codificar áudio de camada 1, defina a propriedade [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) como **eAVEncMPALayer \_ 1**.</span><span class="sxs-lookup"><span data-stu-id="003e6-270">Optional: To encode Layer 1 audio, set the [CODECAPI\_AVEncMPALayer](../directshow/avencmpalayer-property.md) property to **eAVEncMPALayer\_1**.</span></span>
8.  <span data-ttu-id="003e6-271">Opcional: para alterar a taxa de bits, defina a propriedade [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) .</span><span class="sxs-lookup"><span data-stu-id="003e6-271">Optional: To change the bit rate, set the [CODECAPI\_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) property.</span></span> <span data-ttu-id="003e6-272">A taxa de bits deve ser uma das taxas de bits válidas listadas nas especificações de LSF MPEG-1 ou MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="003e6-272">The bit rate must be one of the valid bit rates listed in the MPEG-1 or MPEG-2 LSF specifications.</span></span> <span data-ttu-id="003e6-273">Como alternativa, você pode chamar [**ICodecAPI:: getParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) para obter uma lista de taxas de bits válidas com base nas configurações atuais.</span><span class="sxs-lookup"><span data-stu-id="003e6-273">Alternatively, you can call [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) to get a list of valid bit rates, based on the current settings.</span></span>
9.  <span data-ttu-id="003e6-274">Opcional: com áudio de 2 canais, você pode definir a propriedade [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) para alterar o modo de codificação para canal duplo ou estéreo conjunta.</span><span class="sxs-lookup"><span data-stu-id="003e6-274">Optional: With 2-channel audio, you can set the [CODECAPI\_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) property to change the coding mode to dual channel or joint stereo.</span></span> <span data-ttu-id="003e6-275">Você pode chamar [**ICodecAPI:: GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) para obter as opções válidas.</span><span class="sxs-lookup"><span data-stu-id="003e6-275">You can call [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) to get the valid options.</span></span> <span data-ttu-id="003e6-276">(Para áudio de 1 canal, a única opção é mono.)</span><span class="sxs-lookup"><span data-stu-id="003e6-276">(For 1-channel audio, the only option is mono.)</span></span>
10. <span data-ttu-id="003e6-277">Opcional: defina qualquer uma das outras propriedades de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) listadas anteriormente.</span><span class="sxs-lookup"><span data-stu-id="003e6-277">Optional: Set any of the other [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties listed previously.</span></span>

<span data-ttu-id="003e6-278">É importante seguir a ordem dessas etapas.</span><span class="sxs-lookup"><span data-stu-id="003e6-278">It is important to follow the order of these steps.</span></span> <span data-ttu-id="003e6-279">Em particular, defina o tipo de mídia de saída antes de alterar as propriedades de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .</span><span class="sxs-lookup"><span data-stu-id="003e6-279">In particular, set the output media type before changing any [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) properties.</span></span> <span data-ttu-id="003e6-280">Além disso, você deve definir as propriedades **ICodecAPI** antes que a MFT receba a primeira amostra de entrada.</span><span class="sxs-lookup"><span data-stu-id="003e6-280">Also, you must set **ICodecAPI** properties before the MFT receives the first input sample.</span></span> <span data-ttu-id="003e6-281">Depois que o MFT recebe a entrada, as propriedades do codec são somente leitura e [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) retorna o valor **S \_ false**.</span><span class="sxs-lookup"><span data-stu-id="003e6-281">After the MFT receives input, the codec properties are read-only, and [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) returns the value **S\_FALSE**.</span></span>

### <a name="supported-bit-rates"></a><span data-ttu-id="003e6-282">Taxas de bits com suporte</span><span class="sxs-lookup"><span data-stu-id="003e6-282">Supported Bit Rates</span></span>

<span data-ttu-id="003e6-283">O codificador dá suporte às taxas de bits a seguir.</span><span class="sxs-lookup"><span data-stu-id="003e6-283">The encoder supports the following bit rates.</span></span>



<span data-ttu-id="003e6-284">MPEG-1</span><span class="sxs-lookup"><span data-stu-id="003e6-284">MPEG-1</span></span>

<span data-ttu-id="003e6-285">MPEG-2</span><span class="sxs-lookup"><span data-stu-id="003e6-285">MPEG-2</span></span>

<span data-ttu-id="003e6-286">Camada 1</span><span class="sxs-lookup"><span data-stu-id="003e6-286">Layer 1</span></span>

<span data-ttu-id="003e6-287">Camada 2</span><span class="sxs-lookup"><span data-stu-id="003e6-287">Layer 2</span></span>

<span data-ttu-id="003e6-288">Camada 1</span><span class="sxs-lookup"><span data-stu-id="003e6-288">Layer 1</span></span>

<span data-ttu-id="003e6-289">Camada 2</span><span class="sxs-lookup"><span data-stu-id="003e6-289">Layer 2</span></span>

<span data-ttu-id="003e6-290">32</span><span class="sxs-lookup"><span data-stu-id="003e6-290">32</span></span>

<span data-ttu-id="003e6-291">32\*</span><span class="sxs-lookup"><span data-stu-id="003e6-291">32\*</span></span>

<span data-ttu-id="003e6-292">32</span><span class="sxs-lookup"><span data-stu-id="003e6-292">32</span></span>

<span data-ttu-id="003e6-293">8</span><span class="sxs-lookup"><span data-stu-id="003e6-293">8</span></span>

<span data-ttu-id="003e6-294">64</span><span class="sxs-lookup"><span data-stu-id="003e6-294">64</span></span>

<span data-ttu-id="003e6-295">48\*</span><span class="sxs-lookup"><span data-stu-id="003e6-295">48\*</span></span>

<span data-ttu-id="003e6-296">38</span><span class="sxs-lookup"><span data-stu-id="003e6-296">38</span></span>

<span data-ttu-id="003e6-297">16</span><span class="sxs-lookup"><span data-stu-id="003e6-297">16</span></span>

<span data-ttu-id="003e6-298">96</span><span class="sxs-lookup"><span data-stu-id="003e6-298">96</span></span>

<span data-ttu-id="003e6-299">56\*</span><span class="sxs-lookup"><span data-stu-id="003e6-299">56\*</span></span>

<span data-ttu-id="003e6-300">56</span><span class="sxs-lookup"><span data-stu-id="003e6-300">56</span></span>

<span data-ttu-id="003e6-301">24</span><span class="sxs-lookup"><span data-stu-id="003e6-301">24</span></span>

<span data-ttu-id="003e6-302">128</span><span class="sxs-lookup"><span data-stu-id="003e6-302">128</span></span>

<span data-ttu-id="003e6-303">64</span><span class="sxs-lookup"><span data-stu-id="003e6-303">64</span></span>

<span data-ttu-id="003e6-304">64</span><span class="sxs-lookup"><span data-stu-id="003e6-304">64</span></span>

<span data-ttu-id="003e6-305">32</span><span class="sxs-lookup"><span data-stu-id="003e6-305">32</span></span>

<span data-ttu-id="003e6-306">160</span><span class="sxs-lookup"><span data-stu-id="003e6-306">160</span></span>

<span data-ttu-id="003e6-307">80\*</span><span class="sxs-lookup"><span data-stu-id="003e6-307">80\*</span></span>

<span data-ttu-id="003e6-308">80</span><span class="sxs-lookup"><span data-stu-id="003e6-308">80</span></span>

<span data-ttu-id="003e6-309">40</span><span class="sxs-lookup"><span data-stu-id="003e6-309">40</span></span>

<span data-ttu-id="003e6-310">192</span><span class="sxs-lookup"><span data-stu-id="003e6-310">192</span></span>

<span data-ttu-id="003e6-311">96</span><span class="sxs-lookup"><span data-stu-id="003e6-311">96</span></span>

<span data-ttu-id="003e6-312">96</span><span class="sxs-lookup"><span data-stu-id="003e6-312">96</span></span>

<span data-ttu-id="003e6-313">48</span><span class="sxs-lookup"><span data-stu-id="003e6-313">48</span></span>

<span data-ttu-id="003e6-314">224</span><span class="sxs-lookup"><span data-stu-id="003e6-314">224</span></span>

<span data-ttu-id="003e6-315">112</span><span class="sxs-lookup"><span data-stu-id="003e6-315">112</span></span>

<span data-ttu-id="003e6-316">112</span><span class="sxs-lookup"><span data-stu-id="003e6-316">112</span></span>

<span data-ttu-id="003e6-317">56</span><span class="sxs-lookup"><span data-stu-id="003e6-317">56</span></span>

<span data-ttu-id="003e6-318">256</span><span class="sxs-lookup"><span data-stu-id="003e6-318">256</span></span>

<span data-ttu-id="003e6-319">128</span><span class="sxs-lookup"><span data-stu-id="003e6-319">128</span></span>

<span data-ttu-id="003e6-320">128</span><span class="sxs-lookup"><span data-stu-id="003e6-320">128</span></span>

<span data-ttu-id="003e6-321">64</span><span class="sxs-lookup"><span data-stu-id="003e6-321">64</span></span>

<span data-ttu-id="003e6-322">288</span><span class="sxs-lookup"><span data-stu-id="003e6-322">288</span></span>

<span data-ttu-id="003e6-323">160</span><span class="sxs-lookup"><span data-stu-id="003e6-323">160</span></span>

<span data-ttu-id="003e6-324">144</span><span class="sxs-lookup"><span data-stu-id="003e6-324">144</span></span>

<span data-ttu-id="003e6-325">80</span><span class="sxs-lookup"><span data-stu-id="003e6-325">80</span></span>

<span data-ttu-id="003e6-326">320</span><span class="sxs-lookup"><span data-stu-id="003e6-326">320</span></span>

<span data-ttu-id="003e6-327">192</span><span class="sxs-lookup"><span data-stu-id="003e6-327">192</span></span>

<span data-ttu-id="003e6-328">160</span><span class="sxs-lookup"><span data-stu-id="003e6-328">160</span></span>

<span data-ttu-id="003e6-329">96</span><span class="sxs-lookup"><span data-stu-id="003e6-329">96</span></span>

<span data-ttu-id="003e6-330">352</span><span class="sxs-lookup"><span data-stu-id="003e6-330">352</span></span>

<span data-ttu-id="003e6-331">224\*\*</span><span class="sxs-lookup"><span data-stu-id="003e6-331">224\*\*</span></span>

<span data-ttu-id="003e6-332">176</span><span class="sxs-lookup"><span data-stu-id="003e6-332">176</span></span>

<span data-ttu-id="003e6-333">112</span><span class="sxs-lookup"><span data-stu-id="003e6-333">112</span></span>

<span data-ttu-id="003e6-334">384</span><span class="sxs-lookup"><span data-stu-id="003e6-334">384</span></span>

<span data-ttu-id="003e6-335">256\*\*</span><span class="sxs-lookup"><span data-stu-id="003e6-335">256\*\*</span></span>

<span data-ttu-id="003e6-336">192</span><span class="sxs-lookup"><span data-stu-id="003e6-336">192</span></span>

<span data-ttu-id="003e6-337">128</span><span class="sxs-lookup"><span data-stu-id="003e6-337">128</span></span>

<span data-ttu-id="003e6-338">416</span><span class="sxs-lookup"><span data-stu-id="003e6-338">416</span></span>

<span data-ttu-id="003e6-339">230\*\*</span><span class="sxs-lookup"><span data-stu-id="003e6-339">230\*\*</span></span>

<span data-ttu-id="003e6-340">224</span><span class="sxs-lookup"><span data-stu-id="003e6-340">224</span></span>

<span data-ttu-id="003e6-341">144</span><span class="sxs-lookup"><span data-stu-id="003e6-341">144</span></span>

<span data-ttu-id="003e6-342">448</span><span class="sxs-lookup"><span data-stu-id="003e6-342">448</span></span>

<span data-ttu-id="003e6-343">384\*\*</span><span class="sxs-lookup"><span data-stu-id="003e6-343">384\*\*</span></span>

<span data-ttu-id="003e6-344">256</span><span class="sxs-lookup"><span data-stu-id="003e6-344">256</span></span>

<span data-ttu-id="003e6-345">160</span><span class="sxs-lookup"><span data-stu-id="003e6-345">160</span></span>



 

<dl> <span data-ttu-id="003e6-346">\* Somente mono</span><span class="sxs-lookup"><span data-stu-id="003e6-346">\* Mono only</span></span>  
<span data-ttu-id="003e6-347">\*\* Somente estéreo</span><span class="sxs-lookup"><span data-stu-id="003e6-347">\*\* Stereo only</span></span>  
</dl>

### <a name="example-media-types"></a><span data-ttu-id="003e6-348">Exemplos de tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="003e6-348">Example Media Types</span></span>

<span data-ttu-id="003e6-349">Aqui está um exemplo dos tipos de mídia que são necessários para codificar o PCM de inteiro de 16 bits, áudio estéreo de 48 kHz na taxa de bits padrão.</span><span class="sxs-lookup"><span data-stu-id="003e6-349">Here is an example of the media types that are needed to encode 16-bit integer PCM, 48-kHz stereo audio at the default bit rate.</span></span>

<span data-ttu-id="003e6-350">Tipo de mídia de saída:</span><span class="sxs-lookup"><span data-stu-id="003e6-350">Output media type:</span></span>

| <span data-ttu-id="003e6-351">Atributo</span><span class="sxs-lookup"><span data-stu-id="003e6-351">Attribute</span></span>                                                                           | <span data-ttu-id="003e6-352">Valor</span><span class="sxs-lookup"><span data-stu-id="003e6-352">Value</span></span>                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [<span data-ttu-id="003e6-353">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="003e6-353">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="003e6-354">**\_Áudio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="003e6-354">**MFMediaType\_Audio**</span></span>  |
| [<span data-ttu-id="003e6-355">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="003e6-355">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="003e6-356">**MFAudioFormat \_ MPEG**</span><span class="sxs-lookup"><span data-stu-id="003e6-356">**MFAudioFormat\_MPEG**</span></span> |
| [<span data-ttu-id="003e6-357">\_amostras de áudio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="003e6-357">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="003e6-358">48000</span><span class="sxs-lookup"><span data-stu-id="003e6-358">48000</span></span>                   |
| [<span data-ttu-id="003e6-359">\_canais de \_ número de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="003e6-359">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="003e6-360">2</span><span class="sxs-lookup"><span data-stu-id="003e6-360">2</span></span>                       |



 

<span data-ttu-id="003e6-361">Tipo de mídia de entrada:</span><span class="sxs-lookup"><span data-stu-id="003e6-361">Input media type:</span></span>

| <span data-ttu-id="003e6-362">Atributo</span><span class="sxs-lookup"><span data-stu-id="003e6-362">Attribute</span></span>                                                                                | <span data-ttu-id="003e6-363">Valor</span><span class="sxs-lookup"><span data-stu-id="003e6-363">Value</span></span>                  |
|------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="003e6-364">\_ \_ tipo principal MF \_ MT</span><span class="sxs-lookup"><span data-stu-id="003e6-364">MF\_MT\_MAJOR\_TYPE</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="003e6-365">**\_Áudio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="003e6-365">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="003e6-366">subtipo MF \_ MT \_</span><span class="sxs-lookup"><span data-stu-id="003e6-366">MF\_MT\_SUBTYPE</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="003e6-367">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="003e6-367">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="003e6-368">\_bits de áudio MF MT \_ \_ \_ por \_ amostra</span><span class="sxs-lookup"><span data-stu-id="003e6-368">MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="003e6-369">16</span><span class="sxs-lookup"><span data-stu-id="003e6-369">16</span></span>                     |
| [<span data-ttu-id="003e6-370">\_amostras de áudio MF MT \_ \_ \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="003e6-370">MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="003e6-371">48000</span><span class="sxs-lookup"><span data-stu-id="003e6-371">48000</span></span>                  |
| [<span data-ttu-id="003e6-372">\_canais de \_ número de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="003e6-372">MF\_MT\_AUDIO\_NUM\_CHANNELS</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="003e6-373">2</span><span class="sxs-lookup"><span data-stu-id="003e6-373">2</span></span>                      |
| [<span data-ttu-id="003e6-374">\_alinhamento de \_ bloco de áudio MF MT \_ \_</span><span class="sxs-lookup"><span data-stu-id="003e6-374">MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="003e6-375">4</span><span class="sxs-lookup"><span data-stu-id="003e6-375">4</span></span>                      |
| [<span data-ttu-id="003e6-376">áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo</span><span class="sxs-lookup"><span data-stu-id="003e6-376">MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="003e6-377">192000</span><span class="sxs-lookup"><span data-stu-id="003e6-377">192000</span></span>                 |



 

## <a name="requirements"></a><span data-ttu-id="003e6-378">Requisitos</span><span class="sxs-lookup"><span data-stu-id="003e6-378">Requirements</span></span>



| <span data-ttu-id="003e6-379">Requisito</span><span class="sxs-lookup"><span data-stu-id="003e6-379">Requirement</span></span> | <span data-ttu-id="003e6-380">Valor</span><span class="sxs-lookup"><span data-stu-id="003e6-380">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="003e6-381">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="003e6-381">Minimum supported client</span></span><br/> | <span data-ttu-id="003e6-382">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="003e6-382">Windows 8 \[desktop apps only\]</span></span><br/>                                                |
| <span data-ttu-id="003e6-383">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="003e6-383">Minimum supported server</span></span><br/> | <span data-ttu-id="003e6-384">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="003e6-384">None supported</span></span><br/>                                                                 |
| <span data-ttu-id="003e6-385">DLL</span><span class="sxs-lookup"><span data-stu-id="003e6-385">DLL</span></span><br/>                      | <dl> <span data-ttu-id="003e6-386"><dt>Msmpeg2enc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="003e6-386"><dt>Msmpeg2enc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="003e6-387">Confira também</span><span class="sxs-lookup"><span data-stu-id="003e6-387">See also</span></span>

<dl> <dt>

[<span data-ttu-id="003e6-388">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="003e6-388">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
