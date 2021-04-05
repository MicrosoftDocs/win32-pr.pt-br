---
description: O codificador AAC Microsoft Media Foundation é uma transformação de Media Foundation que codifica o perfil de alta complexidade (AAC) de codificação de áudio avançado, conforme definido por ISO/IEC 13818-7 (MPEG-2 Audio parte 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Codificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ec9730ffc17d7ac3d5e16d86ef5aa20a46b329cd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827208"
---
# <a name="aac-encoder"></a><span data-ttu-id="a35fc-103">Codificador AAC</span><span class="sxs-lookup"><span data-stu-id="a35fc-103">AAC Encoder</span></span>

<span data-ttu-id="a35fc-104">O codificador AAC Microsoft Media Foundation é uma [transformação de Media Foundation](media-foundation-transforms.md) que codifica o perfil de alta complexidade (AAC) de codificação de áudio avançado, conforme definido por ISO/IEC 13818-7 (MPEG-2 Audio parte 7).</span><span class="sxs-lookup"><span data-stu-id="a35fc-104">The Microsoft Media Foundation AAC encoder is a [Media Foundation Transform](media-foundation-transforms.md) that encodes Advanced Audio Coding (AAC) Low Complexity (LC) profile, as defined by ISO/IEC 13818-7 (MPEG-2 Audio Part 7) .</span></span>

<span data-ttu-id="a35fc-105">O codificador AAC não dá suporte à codificação para outros perfis AAC, como Main, SSR ou LTP.</span><span class="sxs-lookup"><span data-stu-id="a35fc-105">The AAC encoder does not support encoding to any other AAC profiles, such as Main, SSR, or LTP.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a35fc-106">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="a35fc-106">Class Identifier</span></span>

<span data-ttu-id="a35fc-107">O CLSID (identificador de classe) do codificador AAC é **CLSID \_ AACMFTEncoder**, definido no arquivo de cabeçalho wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="a35fc-107">The class identifier (CLSID) of the AAC encoder is **CLSID\_AACMFTEncoder**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="a35fc-108">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="a35fc-108">Media Types</span></span>

<span data-ttu-id="a35fc-109">O codificador AAC dá suporte aos seguintes tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="a35fc-109">The AAC encoder supports the following media types.</span></span> <span data-ttu-id="a35fc-110">Você pode definir os tipos em qualquer tipo de entrada de ordem primeiro ou no tipo de saída primeiro.</span><span class="sxs-lookup"><span data-stu-id="a35fc-110">You can set the types in either order input type first, or output type first.</span></span>

### <a name="input-types"></a><span data-ttu-id="a35fc-111">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="a35fc-111">Input Types</span></span>

<span data-ttu-id="a35fc-112">Defina os seguintes atributos no tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="a35fc-112">Set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a35fc-113">Atributo</span><span class="sxs-lookup"><span data-stu-id="a35fc-113">Attribute</span></span></th>
<th><span data-ttu-id="a35fc-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="a35fc-114">Description</span></span></th>
<th><span data-ttu-id="a35fc-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a35fc-115">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a35fc-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-116"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-117">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="a35fc-117">Major type.</span></span></td>
<td><span data-ttu-id="a35fc-118">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="a35fc-118">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a35fc-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-119"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-120">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="a35fc-120">Subtype.</span></span></td>
<td><span data-ttu-id="a35fc-121">Deve ser <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="a35fc-121">Must be <strong>MFAudioFormat_PCM</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a35fc-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-122"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-123">Bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="a35fc-123">Bits per sample.</span></span></td>
<td><span data-ttu-id="a35fc-124">Deve ser 16.</span><span class="sxs-lookup"><span data-stu-id="a35fc-124">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a35fc-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-125"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-126">Exemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="a35fc-126">Samples per second.</span></span></td>
<td><span data-ttu-id="a35fc-127">Os seguintes valores têm suporte:</span><span class="sxs-lookup"><span data-stu-id="a35fc-127">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="a35fc-128">44100 (44,1 KHz)</span><span class="sxs-lookup"><span data-stu-id="a35fc-128">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="a35fc-129">48000 (48 KHz)</span><span class="sxs-lookup"><span data-stu-id="a35fc-129">48000 (48 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a35fc-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-130"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-131">Número de canais.</span><span class="sxs-lookup"><span data-stu-id="a35fc-131">Number of channels.</span></span></td>
<td><span data-ttu-id="a35fc-132">Deve ser 1 (mono) ou 2 (estéreo) ou 6 (5,1).</span><span class="sxs-lookup"><span data-stu-id="a35fc-132">Must be 1 (mono) or 2 (stereo), or 6 (5.1).</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="a35fc-133">O suporte para 6 canais de áudio foi introduzido com o Windows 10 e não está disponível para versões anteriores do Windows.</span><span class="sxs-lookup"><span data-stu-id="a35fc-133">Support for 6 audio channels was introduced with Windows 10 and is not available for earlier versions of Windows.</span></span>
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a35fc-134">Depois que o tipo de entrada é definido, o codificador deriva os seguintes valores e os adiciona ao tipo de mídia:</span><span class="sxs-lookup"><span data-stu-id="a35fc-134">After the input type is set, the encoder derives the following values and adds them to the media type:</span></span>

-   [<span data-ttu-id="a35fc-135">**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="a35fc-135">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [<span data-ttu-id="a35fc-136">**\_alinhamento de \_ bloco de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a35fc-136">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)
-   [<span data-ttu-id="a35fc-137">**\_taxa de \_ \_ bits média de MF MT**</span><span class="sxs-lookup"><span data-stu-id="a35fc-137">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a><span data-ttu-id="a35fc-138">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="a35fc-138">Output Types</span></span>

<span data-ttu-id="a35fc-139">Defina os seguintes atributos no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="a35fc-139">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a35fc-140">Atributo</span><span class="sxs-lookup"><span data-stu-id="a35fc-140">Attribute</span></span></th>
<th><span data-ttu-id="a35fc-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="a35fc-141">Description</span></span></th>
<th><span data-ttu-id="a35fc-142">Comentários</span><span class="sxs-lookup"><span data-stu-id="a35fc-142">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a35fc-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-143"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-144">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="a35fc-144">Major type.</span></span></td>
<td><span data-ttu-id="a35fc-145">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="a35fc-145">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a35fc-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-146"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-147">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="a35fc-147">Audio subtype.</span></span></td>
<td><span data-ttu-id="a35fc-148">Deve ser <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="a35fc-148">Must be <strong>MFAudioFormat_AAC</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a35fc-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-149"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-150">Bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="a35fc-150">Bits per sample.</span></span></td>
<td><span data-ttu-id="a35fc-151">Deve ser 16.</span><span class="sxs-lookup"><span data-stu-id="a35fc-151">Must be 16.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a35fc-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-152"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-153">Exemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="a35fc-153">Samples per second.</span></span></td>
<td><span data-ttu-id="a35fc-154">Deve corresponder ao tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a35fc-154">Must match the input type.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a35fc-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-155"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-156">Número de canais.</span><span class="sxs-lookup"><span data-stu-id="a35fc-156">Number of channels.</span></span></td>
<td><span data-ttu-id="a35fc-157">Deve corresponder ao tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a35fc-157">Must match the input type.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a35fc-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="a35fc-158"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="a35fc-159">Taxa de bits do fluxo AAC codificado, em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="a35fc-159">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="a35fc-160">Os seguintes valores têm suporte:</span><span class="sxs-lookup"><span data-stu-id="a35fc-160">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="a35fc-161">12000</span><span class="sxs-lookup"><span data-stu-id="a35fc-161">12000</span></span></li>
<li><span data-ttu-id="a35fc-162">16000</span><span class="sxs-lookup"><span data-stu-id="a35fc-162">16000</span></span></li>
<li><span data-ttu-id="a35fc-163">20000</span><span class="sxs-lookup"><span data-stu-id="a35fc-163">20000</span></span></li>
<li><span data-ttu-id="a35fc-164">24.000</span><span class="sxs-lookup"><span data-stu-id="a35fc-164">24000</span></span></li>
</ul>
<span data-ttu-id="a35fc-165">O valor padrão para mono e estéreo é 12000 (96 kbps).</span><span class="sxs-lookup"><span data-stu-id="a35fc-165">The default value for both mono and stereo is 12000 (96 Kbps).</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a35fc-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="a35fc-166"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="a35fc-167">O tipo de carga AAC.</span><span class="sxs-lookup"><span data-stu-id="a35fc-167">The AAC payload type.</span></span></td>
<td><span data-ttu-id="a35fc-168">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a35fc-168">Optional.</span></span> <span data-ttu-id="a35fc-169">Se definido, o valor deve ser zero, indicando que o fluxo contém apenas elementos raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="a35fc-169">If set, the value must be zero, indicating that the stream contains raw_data_block elements only.</span></span><br/> <span data-ttu-id="a35fc-170">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a35fc-170">Optional.</span></span> <span data-ttu-id="a35fc-171">Se o atributo não for definido, o valor padrão será zero, indicando que o fluxo contém apenas elementos raw_data_block (AAC bruto).</span><span class="sxs-lookup"><span data-stu-id="a35fc-171">If the attribute is not set, the default value is zero, indicating that the stream contains raw_data_block elements only (raw AAC).</span></span> <br/> <span data-ttu-id="a35fc-172">No Windows 7, se esse atributo for definido, o valor deverá ser zero.</span><span class="sxs-lookup"><span data-stu-id="a35fc-172">In Windows 7, if this attribute is set, the value must be zero.</span></span><br/> <span data-ttu-id="a35fc-173">A partir do Windows 8, o valor pode ser 0 (AAC bruto) ou 1 (ADTS AAC).</span><span class="sxs-lookup"><span data-stu-id="a35fc-173">Starting in Windows 8, the value can be 0 (raw AAC) or 1 (ADTS AAC).</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a35fc-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="a35fc-174"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="a35fc-175">O perfil de áudio AAC e o nível.</span><span class="sxs-lookup"><span data-stu-id="a35fc-175">The AAC audio profile and level.</span></span></td>
<td><span data-ttu-id="a35fc-176">Opcional.</span><span class="sxs-lookup"><span data-stu-id="a35fc-176">Optional.</span></span> <span data-ttu-id="a35fc-177">Os seguintes valores têm suporte:</span><span class="sxs-lookup"><span data-stu-id="a35fc-177">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="a35fc-178">0x29 (padrão)</span><span class="sxs-lookup"><span data-stu-id="a35fc-178">0x29 (default)</span></span></li>
<li><span data-ttu-id="a35fc-179">0x2A</span><span class="sxs-lookup"><span data-stu-id="a35fc-179">0x2A</span></span></li>
<li><span data-ttu-id="a35fc-180">0x2B</span><span class="sxs-lookup"><span data-stu-id="a35fc-180">0x2B</span></span></li>
<li><span data-ttu-id="a35fc-181">0x2C</span><span class="sxs-lookup"><span data-stu-id="a35fc-181">0x2C</span></span></li>
<li><span data-ttu-id="a35fc-182">0x2E</span><span class="sxs-lookup"><span data-stu-id="a35fc-182">0x2E</span></span></li>
<li><span data-ttu-id="a35fc-183">0x2F</span><span class="sxs-lookup"><span data-stu-id="a35fc-183">0x2F</span></span></li>
<li><span data-ttu-id="a35fc-184">0x30</span><span class="sxs-lookup"><span data-stu-id="a35fc-184">0x30</span></span></li>
<li><span data-ttu-id="a35fc-185">0x31</span><span class="sxs-lookup"><span data-stu-id="a35fc-185">0x31</span></span></li>
<li><span data-ttu-id="a35fc-186">0x32</span><span class="sxs-lookup"><span data-stu-id="a35fc-186">0x32</span></span></li>
<li><span data-ttu-id="a35fc-187">0x33</span><span class="sxs-lookup"><span data-stu-id="a35fc-187">0x33</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a35fc-188">A tabela a seguir lista os valores que podem ser usados para o atributo MF_MT_AAC_PROFILE_LEVEL_INDICATION.</span><span class="sxs-lookup"><span data-stu-id="a35fc-188">The following table lists the values that can be used for the MF_MT_AAC_PROFILE_LEVEL_INDICATION attribute.</span></span>

| <span data-ttu-id="a35fc-189">Valor MF_MT_AAC_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="a35fc-189">MF_MT_AAC_PROFILE_LEVEL_INDICATION value</span></span> | <span data-ttu-id="a35fc-190">Perfil</span><span class="sxs-lookup"><span data-stu-id="a35fc-190">Profile</span></span>                           |
|------------------------------------------|-----------------------------------|
| <span data-ttu-id="a35fc-191">0x29</span><span class="sxs-lookup"><span data-stu-id="a35fc-191">0x29</span></span>                                     | <span data-ttu-id="a35fc-192">L2 do perfil AAC</span><span class="sxs-lookup"><span data-stu-id="a35fc-192">AAC Profile L2</span></span>                    | 
| <span data-ttu-id="a35fc-193">0x2A</span><span class="sxs-lookup"><span data-stu-id="a35fc-193">0x2A</span></span>                                     | <span data-ttu-id="a35fc-194">L4 perfil AAC</span><span class="sxs-lookup"><span data-stu-id="a35fc-194">AAC Profile L4</span></span>                    | 
| <span data-ttu-id="a35fc-195">0x2B</span><span class="sxs-lookup"><span data-stu-id="a35fc-195">0x2B</span></span>                                     | <span data-ttu-id="a35fc-196">Perfil AAC L5</span><span class="sxs-lookup"><span data-stu-id="a35fc-196">AAC Profile L5</span></span>                    | 
| <span data-ttu-id="a35fc-197">0x2C</span><span class="sxs-lookup"><span data-stu-id="a35fc-197">0x2C</span></span>                                     | <span data-ttu-id="a35fc-198">L2 do perfil AAC de alta eficiência</span><span class="sxs-lookup"><span data-stu-id="a35fc-198">High Efficiency v1 AAC Profile L2</span></span> | 
| <span data-ttu-id="a35fc-199">0x2E</span><span class="sxs-lookup"><span data-stu-id="a35fc-199">0x2E</span></span>                                     | <span data-ttu-id="a35fc-200">Perfil AAC de alta eficiência do v1</span><span class="sxs-lookup"><span data-stu-id="a35fc-200">High Efficiency v1 AAC Profile L4</span></span> | 
| <span data-ttu-id="a35fc-201">0x2F</span><span class="sxs-lookup"><span data-stu-id="a35fc-201">0x2F</span></span>                                     | <span data-ttu-id="a35fc-202">Perfil AAC de alta eficiência do v1</span><span class="sxs-lookup"><span data-stu-id="a35fc-202">High Efficiency v1 AAC Profile L5</span></span> | 
| <span data-ttu-id="a35fc-203">0x30</span><span class="sxs-lookup"><span data-stu-id="a35fc-203">0x30</span></span>                                     | <span data-ttu-id="a35fc-204">L2 de perfil AAC de alta eficiência v2</span><span class="sxs-lookup"><span data-stu-id="a35fc-204">High Efficiency v2 AAC Profile L2</span></span> | 
| <span data-ttu-id="a35fc-205">0x31</span><span class="sxs-lookup"><span data-stu-id="a35fc-205">0x31</span></span>                                     | <span data-ttu-id="a35fc-206">Perfil AAC L3 de alta eficiência</span><span class="sxs-lookup"><span data-stu-id="a35fc-206">High Efficiency v2 AAC Profile L3</span></span> | 
| <span data-ttu-id="a35fc-207">0x32</span><span class="sxs-lookup"><span data-stu-id="a35fc-207">0x32</span></span>                                     | <span data-ttu-id="a35fc-208">Perfil AAC de alta eficiência v2</span><span class="sxs-lookup"><span data-stu-id="a35fc-208">High Efficiency v2 AAC Profile L4</span></span> | 
| <span data-ttu-id="a35fc-209">0x33</span><span class="sxs-lookup"><span data-stu-id="a35fc-209">0x33</span></span>                                     | <span data-ttu-id="a35fc-210">Perfil AAC de alta eficiência v2</span><span class="sxs-lookup"><span data-stu-id="a35fc-210">High Efficiency v2 AAC Profile L5</span></span> | 

 

<span data-ttu-id="a35fc-211">Depois que o tipo de saída é definido, o codificador AAC atualiza o tipo adicionando o atributo de [**\_ dados de \_ usuário \_ MF MT**](mf-mt-user-data-attribute.md) .</span><span class="sxs-lookup"><span data-stu-id="a35fc-211">After the output type is set, the AAC encoder updates the type by adding the [**MF\_MT\_USER\_DATA**](mf-mt-user-data-attribute.md) attribute.</span></span> <span data-ttu-id="a35fc-212">Esse atributo contém a parte da estrutura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece após a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) (ou seja, após o membro **WFX** ).</span><span class="sxs-lookup"><span data-stu-id="a35fc-212">This attribute contains the portion of the [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure that appears after the [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) structure (that is, after the **wfx** member).</span></span> <span data-ttu-id="a35fc-213">Isso é seguido pelos dados de AudioSpecificConfig (), conforme definido por ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="a35fc-213">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span>

<span data-ttu-id="a35fc-214">Cada exemplo de saída contém um quadro AAC compactado sem cabeçalho.</span><span class="sxs-lookup"><span data-stu-id="a35fc-214">Each output sample contains one compressed AAC frame with no header.</span></span> <span data-ttu-id="a35fc-215">Esse formato é equivalente ao elemento de \_ bloco de dados brutos \_ () definido por MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="a35fc-215">This format is equivalent to the raw\_data\_block() element defined by MPEG-2.</span></span> <span data-ttu-id="a35fc-216">O atributo de [ \_ tipo de conteúdo MF MT \_ AAC \_ \_ ](mf-mt-aac-payload-type.md) , se presente no tipo de saída, deve ser definido como zero para indicar esse tipo de carga.</span><span class="sxs-lookup"><span data-stu-id="a35fc-216">The [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) attribute, if present in the output type, must be set to zero to indicate this payload type.</span></span>

<span data-ttu-id="a35fc-217">Cada exemplo de saída contém um quadro AAC compactado correspondente a 1024 exemplos de PCM.</span><span class="sxs-lookup"><span data-stu-id="a35fc-217">Each output sample contains one compressed AAC frame corresponding to 1024 PCM samples.</span></span> <span data-ttu-id="a35fc-218">Por exemplo, a taxa de amostragem de 48 kHz, a duração de um quadro compactado é de 21,33 MS.</span><span class="sxs-lookup"><span data-stu-id="a35fc-218">For example, at 48 Khz sampling rate, the duration of one compressed frame is 21.33 msec.</span></span>

<span data-ttu-id="a35fc-219">Se o [tipo de carga do MF \_ MT \_ AAC \_ \_ ](mf-mt-aac-payload-type.md) for zero (o valor padrão), cada exemplo de saída conterá um \_ elemento de bloco de dados brutos \_ (), conforme definido pelo ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="a35fc-219">If [MF\_MT\_AAC\_PAYLOAD\_TYPE](mf-mt-aac-payload-type.md) is zero (the default value), each output sample contains one raw\_data\_block() element as defined by ISO/IEC 13818-7.</span></span>

## <a name="example-media-types"></a><span data-ttu-id="a35fc-220">Exemplos de tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="a35fc-220">Example Media Types</span></span>

<span data-ttu-id="a35fc-221">Aqui está um exemplo dos tipos de mídia necessários para a codificação de áudio estéreo de 160 a 44,1-kHz, em relação ao AAC bruto</span><span class="sxs-lookup"><span data-stu-id="a35fc-221">Here is an example of the media types needed to encode from 44.1-kHz, 160-Kbps stereo audio to raw AAC</span></span>

<span data-ttu-id="a35fc-222">Tipo de mídia de entrada:</span><span class="sxs-lookup"><span data-stu-id="a35fc-222">Input media type:</span></span>



| <span data-ttu-id="a35fc-223">Atributo</span><span class="sxs-lookup"><span data-stu-id="a35fc-223">Attribute</span></span>                                                                                    | <span data-ttu-id="a35fc-224">Valor</span><span class="sxs-lookup"><span data-stu-id="a35fc-224">Value</span></span>                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [<span data-ttu-id="a35fc-225">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="a35fc-225">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="a35fc-226">**\_Áudio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a35fc-226">**MFMediaType\_Audio**</span></span> |
| [<span data-ttu-id="a35fc-227">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="a35fc-227">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="a35fc-228">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="a35fc-228">**MFAudioFormat\_PCM**</span></span> |
| [<span data-ttu-id="a35fc-229">**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**</span><span class="sxs-lookup"><span data-stu-id="a35fc-229">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="a35fc-230">16</span><span class="sxs-lookup"><span data-stu-id="a35fc-230">16</span></span>                     |
| [<span data-ttu-id="a35fc-231">**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="a35fc-231">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="a35fc-232">44100</span><span class="sxs-lookup"><span data-stu-id="a35fc-232">44100</span></span>                  |
| [<span data-ttu-id="a35fc-233">**\_canais de \_ número de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a35fc-233">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="a35fc-234">2</span><span class="sxs-lookup"><span data-stu-id="a35fc-234">2</span></span>                      |
| [<span data-ttu-id="a35fc-235">**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="a35fc-235">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="a35fc-236">176400 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-236">176400 (optional)</span></span>      |
| [<span data-ttu-id="a35fc-237">**\_alinhamento de \_ bloco de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a35fc-237">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="a35fc-238">4 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-238">4 (optional)</span></span>           |
| [<span data-ttu-id="a35fc-239">**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**</span><span class="sxs-lookup"><span data-stu-id="a35fc-239">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)         | <span data-ttu-id="a35fc-240">1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-240">1 (optional)</span></span>           |
| [<span data-ttu-id="a35fc-241">**\_taxa de \_ \_ bits média de MF MT**</span><span class="sxs-lookup"><span data-stu-id="a35fc-241">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                  | <span data-ttu-id="a35fc-242">1411200 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-242">1411200 (optional)</span></span>     |
| [<span data-ttu-id="a35fc-243">**\_amostras de \_ \_ tamanho fixo MF MT \_**</span><span class="sxs-lookup"><span data-stu-id="a35fc-243">**MF\_MT\_FIXED\_SIZE\_SAMPLES**</span></span>](mf-mt-fixed-size-samples-attribute.md)                   | <span data-ttu-id="a35fc-244">1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-244">1 (optional)</span></span>           |



 

<span data-ttu-id="a35fc-245">Tipo de mídia de saída:</span><span class="sxs-lookup"><span data-stu-id="a35fc-245">Output media type:</span></span>



| <span data-ttu-id="a35fc-246">Atributo</span><span class="sxs-lookup"><span data-stu-id="a35fc-246">Attribute</span></span>                                                                                      | <span data-ttu-id="a35fc-247">Valor</span><span class="sxs-lookup"><span data-stu-id="a35fc-247">Value</span></span>                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a35fc-248">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="a35fc-248">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="a35fc-249">**\_Áudio MFMediaType**</span><span class="sxs-lookup"><span data-stu-id="a35fc-249">**MFMediaType\_Audio**</span></span>                                                                          |
| [<span data-ttu-id="a35fc-250">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="a35fc-250">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="a35fc-251">**\_AAC MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="a35fc-251">**MFAudioFormat\_AAC**</span></span>                                                                          |
| [<span data-ttu-id="a35fc-252">**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**</span><span class="sxs-lookup"><span data-stu-id="a35fc-252">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)              | <span data-ttu-id="a35fc-253">16</span><span class="sxs-lookup"><span data-stu-id="a35fc-253">16</span></span>                                                                                              |
| [<span data-ttu-id="a35fc-254">**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="a35fc-254">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="a35fc-255">44100</span><span class="sxs-lookup"><span data-stu-id="a35fc-255">44100</span></span>                                                                                           |
| [<span data-ttu-id="a35fc-256">**\_canais de \_ número de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a35fc-256">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="a35fc-257">2</span><span class="sxs-lookup"><span data-stu-id="a35fc-257">2</span></span>                                                                                               |
| [<span data-ttu-id="a35fc-258">**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="a35fc-258">**MF\_MT\_AUDIO\_AVG\_BYTES\_PER\_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md)   | <span data-ttu-id="a35fc-259">20000</span><span class="sxs-lookup"><span data-stu-id="a35fc-259">20000</span></span>                                                                                           |
| [<span data-ttu-id="a35fc-260">\_tipo de conteúdo MF MT \_ AAC \_ \_</span><span class="sxs-lookup"><span data-stu-id="a35fc-260">MF\_MT\_AAC\_PAYLOAD\_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="a35fc-261">0 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-261">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="a35fc-262">\_indicação de \_ \_ nível de \_ perfil de áudio \_ \_ MF MT AAC</span><span class="sxs-lookup"><span data-stu-id="a35fc-262">MF\_MT\_AAC\_AUDIO\_PROFILE\_LEVEL\_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="a35fc-263">0x29 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-263">0x29 (optional)</span></span>                                                                                 |
| [<span data-ttu-id="a35fc-264">**\_alinhamento de \_ bloco de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a35fc-264">**MF\_MT\_AUDIO\_BLOCK\_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)               | <span data-ttu-id="a35fc-265">1 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-265">1 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="a35fc-266">**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**</span><span class="sxs-lookup"><span data-stu-id="a35fc-266">**MF\_MT\_ALL\_SAMPLES\_INDEPENDENT**</span></span>](mf-mt-all-samples-independent-attribute.md)           | <span data-ttu-id="a35fc-267">0 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-267">0 (optional)</span></span>                                                                                    |
| [<span data-ttu-id="a35fc-268">**\_taxa de \_ \_ bits média de MF MT**</span><span class="sxs-lookup"><span data-stu-id="a35fc-268">**MF\_MT\_AVG\_BITRATE**</span></span>](mf-mt-avg-bitrate-attribute.md)                                    | <span data-ttu-id="a35fc-269">160000 (opcional)</span><span class="sxs-lookup"><span data-stu-id="a35fc-269">160000 (optional)</span></span>                                                                               |
| [<span data-ttu-id="a35fc-270">**dados de usuário do MF \_ MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a35fc-270">**MF\_MT\_USER\_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="a35fc-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} adicional</span><span class="sxs-lookup"><span data-stu-id="a35fc-271">{0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (optional)</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="a35fc-272">Comentários</span><span class="sxs-lookup"><span data-stu-id="a35fc-272">Remarks</span></span>

<span data-ttu-id="a35fc-273">Na implementação atual, cada exemplo de entrada deve ter uma hora e uma duração válidas.</span><span class="sxs-lookup"><span data-stu-id="a35fc-273">In the current implementation, every input sample must have a valid time and duration.</span></span> <span data-ttu-id="a35fc-274">Para definir o tempo de exemplo, chame [**IMFSample:: Setsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span><span class="sxs-lookup"><span data-stu-id="a35fc-274">To set the sample time, call [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime).</span></span> <span data-ttu-id="a35fc-275">Para definir a duração da amostra, chame [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span><span class="sxs-lookup"><span data-stu-id="a35fc-275">To set the sample duration, call [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).</span></span>

<span data-ttu-id="a35fc-276">Se o tempo de amostra não for definido, o método do codificador [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) retornará **MF \_ E \_ nenhum \_ carimbo de \_ data/hora de amostra**.</span><span class="sxs-lookup"><span data-stu-id="a35fc-276">If the sample time is not set, the encoder's [**IMFTransform::ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) method returns **MF\_E\_NO\_SAMPLE\_TIMESTAMP**.</span></span> <span data-ttu-id="a35fc-277">Se a duração da amostra não for definida, o método **ProcessInput** retornará **MF \_ E \_ nenhuma \_ \_ duração de amostra**.</span><span class="sxs-lookup"><span data-stu-id="a35fc-277">If the sample duration is not set, the **ProcessInput** method returns **MF\_E\_NO\_SAMPLE\_DURATION**.</span></span>

<span data-ttu-id="a35fc-278">A duração da amostra pode ser calculada da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="a35fc-278">Sample duration can be calculated as follows:</span></span>


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



<span data-ttu-id="a35fc-279">em que *nAudioSamplesPerChannel* é o número de exemplos de áudio PCM por canal no buffer de entrada e *nSamplesPerSec* é a taxa de amostragem, em amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="a35fc-279">where *nAudioSamplesPerChannel* is the number of PCM audio samples per channel in the input buffer, and *nSamplesPerSec* is the sampling rate, in samples per second.</span></span>

> [!Note]  
> <span data-ttu-id="a35fc-280">Devido a um bug na implementação atual, se a duração da amostra for definida como zero, a chamada [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) terá sucesso, mas uma chamada subsequente para [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) lançará uma exceção de divisão por zero.</span><span class="sxs-lookup"><span data-stu-id="a35fc-280">Due to a bug in the current implementation, if the sample duration is set to zero, the [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) call succeeds, but a subsequent call to [**IMFTransform::ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) will throw a divide-by-zero exception.</span></span> <span data-ttu-id="a35fc-281">Para evitar esse erro, defina uma duração válida diferente de zero em cada amostra de entrada.</span><span class="sxs-lookup"><span data-stu-id="a35fc-281">To avoid this error, set a valid nonzero duration on each input sample.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="a35fc-282">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a35fc-282">Requirements</span></span>



| <span data-ttu-id="a35fc-283">Requisito</span><span class="sxs-lookup"><span data-stu-id="a35fc-283">Requirement</span></span> | <span data-ttu-id="a35fc-284">Valor</span><span class="sxs-lookup"><span data-stu-id="a35fc-284">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="a35fc-285">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a35fc-285">Minimum supported client</span></span><br/> | <span data-ttu-id="a35fc-286">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="a35fc-286">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="a35fc-287">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a35fc-287">Minimum supported server</span></span><br/> | <span data-ttu-id="a35fc-288">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="a35fc-288">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="a35fc-289">DLL</span><span class="sxs-lookup"><span data-stu-id="a35fc-289">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a35fc-290"><dt>Mfaacenc.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a35fc-290"><dt>Mfaacenc.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a35fc-291">Confira também</span><span class="sxs-lookup"><span data-stu-id="a35fc-291">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a35fc-292">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="a35fc-292">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="a35fc-293">**Decodificador AAC**</span><span class="sxs-lookup"><span data-stu-id="a35fc-293">**AAC Decoder**</span></span>](aac-decoder.md)
</dt> <dt>

[<span data-ttu-id="a35fc-294">Tipos de mídia AAC</span><span class="sxs-lookup"><span data-stu-id="a35fc-294">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="a35fc-295">Tipos de mídia de áudio</span><span class="sxs-lookup"><span data-stu-id="a35fc-295">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="a35fc-296">Suporte a MPEG-4 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a35fc-296">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="a35fc-297">Formatos de mídia compatíveis com o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="a35fc-297">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

