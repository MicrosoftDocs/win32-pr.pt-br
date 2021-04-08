---
description: O Microsoft Media Foundation.
ms.assetid: 4C397139-6553-4707-B737-7C31C5D423BA
title: Codificador de áudio MP3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7ea2b22d2fe8cd51f9a2990970493e0415f34d3c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104010667"
---
# <a name="mp3-audio-encoder"></a><span data-ttu-id="a003a-103">Codificador de áudio MP3</span><span class="sxs-lookup"><span data-stu-id="a003a-103">MP3 Audio Encoder</span></span>

<span data-ttu-id="a003a-104">O codificador de áudio MP3 Microsoft Media Foundation é uma [Media Foundation transformação](media-foundation-transforms.md) (MFT) que codifica áudio MPEG-1 Layer 3 (mp3).</span><span class="sxs-lookup"><span data-stu-id="a003a-104">The Microsoft Media Foundation MP3 audio encoder is a [Media Foundation Transform](media-foundation-transforms.md) (MFT) that encodes MPEG-1 layer 3 (MP3) audio.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="a003a-105">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="a003a-105">Class Identifier</span></span>

<span data-ttu-id="a003a-106">O CLSID (identificador de classe) do codificador MP3 é **CLSID \_ MP3ACMCodecWrapper**, definido no arquivo de cabeçalho wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="a003a-106">The class identifier (CLSID) of the MP3 encoder is **CLSID\_MP3ACMCodecWrapper**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="media-types"></a><span data-ttu-id="a003a-107">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="a003a-107">Media Types</span></span>

<span data-ttu-id="a003a-108">O codificador MP3 dá suporte aos seguintes tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="a003a-108">The MP3 encoder supports the following media types.</span></span> <span data-ttu-id="a003a-109">O tipo de saída deve ser definido antes do tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="a003a-109">The output type must be set before the input type.</span></span>

### <a name="output-types"></a><span data-ttu-id="a003a-110">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="a003a-110">Output Types</span></span>

<span data-ttu-id="a003a-111">Defina os seguintes atributos no tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="a003a-111">Set the following attributes on the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a003a-112">Atributo</span><span class="sxs-lookup"><span data-stu-id="a003a-112">Attribute</span></span></th>
<th><span data-ttu-id="a003a-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="a003a-113">Description</span></span></th>
<th><span data-ttu-id="a003a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a003a-114">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a003a-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a003a-115"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="a003a-116">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="a003a-116">Major type.</span></span></td>
<td><span data-ttu-id="a003a-117">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="a003a-117">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a003a-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="a003a-118"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="a003a-119">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="a003a-119">Audio subtype.</span></span></td>
<td><span data-ttu-id="a003a-120">Deve ser <strong>MFAudioFormat_MP3</strong>.</span><span class="sxs-lookup"><span data-stu-id="a003a-120">Must be <strong>MFAudioFormat_MP3</strong>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a003a-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="a003a-121"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="a003a-122">Taxa de bits do fluxo MP3 codificado, em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="a003a-122">Bit rate of the encoded MP3 stream, in bytes per second.</span></span></td>
<td><span data-ttu-id="a003a-123">O codificador dá suporte a todas as taxas de bits definidas pelo padrão (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 ou 320 kbps).</span><span class="sxs-lookup"><span data-stu-id="a003a-123">The encoder supports all bit rates defined by the standard (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, or 320 Kbps).</span></span><br/> <span data-ttu-id="a003a-124">As taxas de bits padrão são 128 kbps para mono e 320 kbps para estéreo.</span><span class="sxs-lookup"><span data-stu-id="a003a-124">The default bit rates are 128 Kbps for mono and 320 Kbps for stereo.</span></span><br/> <span data-ttu-id="a003a-125">Use esse atributo para especificar a taxa de bits codificada.</span><span class="sxs-lookup"><span data-stu-id="a003a-125">Use this attribute to specify the encoded bit rate.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a003a-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="a003a-126"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="a003a-127">Número de canais.</span><span class="sxs-lookup"><span data-stu-id="a003a-127">Number of channels.</span></span></td>
<td><span data-ttu-id="a003a-128">Os seguintes valores têm suporte:</span><span class="sxs-lookup"><span data-stu-id="a003a-128">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="a003a-129">1 (mono)</span><span class="sxs-lookup"><span data-stu-id="a003a-129">1 (mono)</span></span></li>
<li><span data-ttu-id="a003a-130">2 (estéreo)</span><span class="sxs-lookup"><span data-stu-id="a003a-130">2 (stereo)</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a003a-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="a003a-131"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="a003a-132">Exemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="a003a-132">Samples per second.</span></span></td>
<td><span data-ttu-id="a003a-133">Os seguintes valores têm suporte:</span><span class="sxs-lookup"><span data-stu-id="a003a-133">The following values are supported:</span></span>
<ul>
<li><span data-ttu-id="a003a-134">48000 (48 KHz)</span><span class="sxs-lookup"><span data-stu-id="a003a-134">48000 (48 KHz)</span></span></li>
<li><span data-ttu-id="a003a-135">44100 (44,1 KHz)</span><span class="sxs-lookup"><span data-stu-id="a003a-135">44100 (44.1 KHz)</span></span></li>
<li><span data-ttu-id="a003a-136">32000 (32 KHz)</span><span class="sxs-lookup"><span data-stu-id="a003a-136">32000 (32 KHz)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a003a-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span><span class="sxs-lookup"><span data-stu-id="a003a-137"><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></span></span></td>
<td><span data-ttu-id="a003a-138">Dados de codec adicionais.</span><span class="sxs-lookup"><span data-stu-id="a003a-138">Additional codec data.</span></span></td>
<td><span data-ttu-id="a003a-139">Esse atributo contém os 12 bytes da estrutura <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> que seguem o membro <strong>WFX</strong> dessa estrutura.</span><span class="sxs-lookup"><span data-stu-id="a003a-139">This attribute contains the 12 bytes of the <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> structure that follow the <strong>wfx</strong> member of that structure.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="a003a-140">Como alternativa, você pode preencher uma estrutura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) e chamar [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) para converter a estrutura em um tipo de mídia Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="a003a-140">Alternatively, you can fill in an [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) structure and call [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) to convert the structure to a Media Foundation media type.</span></span>

### <a name="input-types"></a><span data-ttu-id="a003a-141">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="a003a-141">Input Types</span></span>

<span data-ttu-id="a003a-142">Defina os seguintes atributos no tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="a003a-142">Set the following attributes on the input media type.</span></span>



| <span data-ttu-id="a003a-143">Atributo</span><span class="sxs-lookup"><span data-stu-id="a003a-143">Attribute</span></span>                                                                               | <span data-ttu-id="a003a-144">Descrição</span><span class="sxs-lookup"><span data-stu-id="a003a-144">Description</span></span>         | <span data-ttu-id="a003a-145">Comentários</span><span class="sxs-lookup"><span data-stu-id="a003a-145">Remarks</span></span>                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [<span data-ttu-id="a003a-146">**\_ \_ tipo principal MF \_ MT**</span><span class="sxs-lookup"><span data-stu-id="a003a-146">**MF\_MT\_MAJOR\_TYPE**</span></span>](mf-mt-major-type-attribute.md)                               | <span data-ttu-id="a003a-147">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="a003a-147">Major type.</span></span>         | <span data-ttu-id="a003a-148">Deve ser **\_ áudio MFMediaType**.</span><span class="sxs-lookup"><span data-stu-id="a003a-148">Must be **MFMediaType\_Audio**.</span></span> |
| [<span data-ttu-id="a003a-149">**subtipo MF \_ MT \_**</span><span class="sxs-lookup"><span data-stu-id="a003a-149">**MF\_MT\_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                      | <span data-ttu-id="a003a-150">Subtipo.</span><span class="sxs-lookup"><span data-stu-id="a003a-150">Subtype.</span></span>            | <span data-ttu-id="a003a-151">Deve ser **MFAudioFormat \_ PCM**.</span><span class="sxs-lookup"><span data-stu-id="a003a-151">Must be **MFAudioFormat\_PCM**.</span></span> |
| [<span data-ttu-id="a003a-152">**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**</span><span class="sxs-lookup"><span data-stu-id="a003a-152">**MF\_MT\_AUDIO\_BITS\_PER\_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)       | <span data-ttu-id="a003a-153">Bits por amostra.</span><span class="sxs-lookup"><span data-stu-id="a003a-153">Bits per sample.</span></span>    | <span data-ttu-id="a003a-154">Deve ser 16.</span><span class="sxs-lookup"><span data-stu-id="a003a-154">Must be 16.</span></span>                     |
| [<span data-ttu-id="a003a-155">**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**</span><span class="sxs-lookup"><span data-stu-id="a003a-155">**MF\_MT\_AUDIO\_SAMPLES\_PER\_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md) | <span data-ttu-id="a003a-156">Exemplos por segundo.</span><span class="sxs-lookup"><span data-stu-id="a003a-156">Samples per second.</span></span> | <span data-ttu-id="a003a-157">Deve corresponder ao tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="a003a-157">Must match the output type.</span></span>     |
| [<span data-ttu-id="a003a-158">**\_canais de \_ número de áudio MF MT \_ \_**</span><span class="sxs-lookup"><span data-stu-id="a003a-158">**MF\_MT\_AUDIO\_NUM\_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)              | <span data-ttu-id="a003a-159">Número de canais.</span><span class="sxs-lookup"><span data-stu-id="a003a-159">Number of channels.</span></span> | <span data-ttu-id="a003a-160">Deve corresponder ao tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="a003a-160">Must match the output type.</span></span>     |



 

<span data-ttu-id="a003a-161">O codificador dá suporte apenas à entrada PCM de inteiro de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="a003a-161">The encoder supports only 16-bit integer PCM input.</span></span> <span data-ttu-id="a003a-162">Ele não dá suporte à entrada de ponto flutuante de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a003a-162">It does not support 32-bit floating point input.</span></span>

### <a name="media-formats"></a><span data-ttu-id="a003a-163">Formatos de mídia</span><span class="sxs-lookup"><span data-stu-id="a003a-163">Media Formats</span></span>

<span data-ttu-id="a003a-164">O padrão MPEG-1 e MPEG-2 define 252 formatos de áudio de camada 3.</span><span class="sxs-lookup"><span data-stu-id="a003a-164">The MPEG-1 and MPEG-2 standard defines 252 layer 3 audio formats.</span></span> <span data-ttu-id="a003a-165">O codificador MP3 dá suporte ao padrão com algumas exceções, bem como alguns formatos adicionais, conforme descrito abaixo.</span><span class="sxs-lookup"><span data-stu-id="a003a-165">The MP3 encoder supports the standard with some exceptions, as well as some additional formats, as described below.</span></span> <span data-ttu-id="a003a-166">A camada 3 é definida como:</span><span class="sxs-lookup"><span data-stu-id="a003a-166">Layer 3 is defined as:</span></span>



| <span data-ttu-id="a003a-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="a003a-167">Requirement</span></span> | <span data-ttu-id="a003a-168">Valor</span><span class="sxs-lookup"><span data-stu-id="a003a-168">Value</span></span> |
|----------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="a003a-169">Canais</span><span class="sxs-lookup"><span data-stu-id="a003a-169">Channels</span></span>                         | <span data-ttu-id="a003a-170">mono ou estéreo</span><span class="sxs-lookup"><span data-stu-id="a003a-170">mono or stereo</span></span>                                                |
| <span data-ttu-id="a003a-171">Taxas de amostragem MPEG-1 em kHz</span><span class="sxs-lookup"><span data-stu-id="a003a-171">MPEG-1 sample rates in kHz</span></span>       | <span data-ttu-id="a003a-172">44,1, 48, 32</span><span class="sxs-lookup"><span data-stu-id="a003a-172">44.1, 48, 32</span></span>                                                  |
| <span data-ttu-id="a003a-173">Taxas de bits codificadas MPEG-1 em Kbps</span><span class="sxs-lookup"><span data-stu-id="a003a-173">MPEG-1 encoded bit rates in kbps</span></span> | <span data-ttu-id="a003a-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span><span class="sxs-lookup"><span data-stu-id="a003a-174">32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320</span></span> |
| <span data-ttu-id="a003a-175">Taxas de exemplo MPEG-2 em kHz</span><span class="sxs-lookup"><span data-stu-id="a003a-175">MPEG-2 sample rates in kHz</span></span>       | <span data-ttu-id="a003a-176">8, 11, 25, 12, 16, 22, 5, 24</span><span class="sxs-lookup"><span data-stu-id="a003a-176">8, 11.025, 12, 16, 22.05, 24</span></span>                                  |
| <span data-ttu-id="a003a-177">Taxas de bits codificadas MPEG-2 em Kbps</span><span class="sxs-lookup"><span data-stu-id="a003a-177">MPEG-2 encoded bit rates in kbps</span></span> | <span data-ttu-id="a003a-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span><span class="sxs-lookup"><span data-stu-id="a003a-178">8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160</span></span>          |



 

<span data-ttu-id="a003a-179">O codificador MP3 também dá suporte aos seguintes formatos.</span><span class="sxs-lookup"><span data-stu-id="a003a-179">The MP3 encoder also supports the following formats.</span></span>



| <span data-ttu-id="a003a-180">Taxa de amostragem</span><span class="sxs-lookup"><span data-stu-id="a003a-180">Sample Rate</span></span> | <span data-ttu-id="a003a-181">Taxa de bits</span><span class="sxs-lookup"><span data-stu-id="a003a-181">Bit Rate</span></span>     | <span data-ttu-id="a003a-182">Número do canal</span><span class="sxs-lookup"><span data-stu-id="a003a-182">Channel Number</span></span> |
|-------------|--------------|----------------|
| <span data-ttu-id="a003a-183">8000</span><span class="sxs-lookup"><span data-stu-id="a003a-183">8000</span></span>        | <span data-ttu-id="a003a-184">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="a003a-184">18000, 20000</span></span> | <span data-ttu-id="a003a-185">2</span><span class="sxs-lookup"><span data-stu-id="a003a-185">2</span></span>              |
| <span data-ttu-id="a003a-186">11025</span><span class="sxs-lookup"><span data-stu-id="a003a-186">11025</span></span>       | <span data-ttu-id="a003a-187">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="a003a-187">18000, 20000</span></span> | <span data-ttu-id="a003a-188">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="a003a-188">1 or 2</span></span>         |
| <span data-ttu-id="a003a-189">12000</span><span class="sxs-lookup"><span data-stu-id="a003a-189">12000</span></span>       | <span data-ttu-id="a003a-190">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="a003a-190">18000, 20000</span></span> | <span data-ttu-id="a003a-191">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="a003a-191">1 or 2</span></span>         |
| <span data-ttu-id="a003a-192">16000</span><span class="sxs-lookup"><span data-stu-id="a003a-192">16000</span></span>       | <span data-ttu-id="a003a-193">18000, 20000</span><span class="sxs-lookup"><span data-stu-id="a003a-193">18000, 20000</span></span> | <span data-ttu-id="a003a-194">1</span><span class="sxs-lookup"><span data-stu-id="a003a-194">1</span></span>              |
| <span data-ttu-id="a003a-195">32000</span><span class="sxs-lookup"><span data-stu-id="a003a-195">32000</span></span>       | <span data-ttu-id="a003a-196">144000</span><span class="sxs-lookup"><span data-stu-id="a003a-196">144000</span></span>       | <span data-ttu-id="a003a-197">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="a003a-197">1 or 2</span></span>         |
| <span data-ttu-id="a003a-198">44100</span><span class="sxs-lookup"><span data-stu-id="a003a-198">44100</span></span>       | <span data-ttu-id="a003a-199">144000</span><span class="sxs-lookup"><span data-stu-id="a003a-199">144000</span></span>       | <span data-ttu-id="a003a-200">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="a003a-200">1 or 2</span></span>         |
| <span data-ttu-id="a003a-201">48000</span><span class="sxs-lookup"><span data-stu-id="a003a-201">48000</span></span>       | <span data-ttu-id="a003a-202">144000</span><span class="sxs-lookup"><span data-stu-id="a003a-202">144000</span></span>       | <span data-ttu-id="a003a-203">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="a003a-203">1 or 2</span></span>         |



 

<span data-ttu-id="a003a-204">O codificador MP3 não oferece suporte aos seguintes formatos definidos pelo padrão.</span><span class="sxs-lookup"><span data-stu-id="a003a-204">The MP3 encoder does not support the following formats defined by the standard.</span></span>



| <span data-ttu-id="a003a-205">Taxa de amostragem</span><span class="sxs-lookup"><span data-stu-id="a003a-205">Sample Rate</span></span> | <span data-ttu-id="a003a-206">Taxas de bits</span><span class="sxs-lookup"><span data-stu-id="a003a-206">Bit Rates</span></span>                                    | <span data-ttu-id="a003a-207">Número do canal</span><span class="sxs-lookup"><span data-stu-id="a003a-207">Channel Number</span></span> |
|-------------|----------------------------------------------|----------------|
| <span data-ttu-id="a003a-208">12000</span><span class="sxs-lookup"><span data-stu-id="a003a-208">12000</span></span>       | <span data-ttu-id="a003a-209">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="a003a-209">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="a003a-210">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="a003a-210">1 or 2</span></span>         |
| <span data-ttu-id="a003a-211">11025</span><span class="sxs-lookup"><span data-stu-id="a003a-211">11025</span></span>       | <span data-ttu-id="a003a-212">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="a003a-212">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="a003a-213">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="a003a-213">1 or 2</span></span>         |
| <span data-ttu-id="a003a-214">8000</span><span class="sxs-lookup"><span data-stu-id="a003a-214">8000</span></span>        | <span data-ttu-id="a003a-215">80000, 96000, 112000, 128000, 144000, 160000</span><span class="sxs-lookup"><span data-stu-id="a003a-215">80000, 96000, 112000, 128000, 144000, 160000</span></span> | <span data-ttu-id="a003a-216">1 ou 2</span><span class="sxs-lookup"><span data-stu-id="a003a-216">1 or 2</span></span>         |
| <span data-ttu-id="a003a-217">8000</span><span class="sxs-lookup"><span data-stu-id="a003a-217">8000</span></span>        | <span data-ttu-id="a003a-218">8000, 11025, 12000, 16000, 22050, 24000</span><span class="sxs-lookup"><span data-stu-id="a003a-218">8000, 11025, 12000, 16000, 22050, 24000</span></span>      | <span data-ttu-id="a003a-219">2</span><span class="sxs-lookup"><span data-stu-id="a003a-219">2</span></span>              |



 

## <a name="requirements"></a><span data-ttu-id="a003a-220">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a003a-220">Requirements</span></span>



| <span data-ttu-id="a003a-221">Requisito</span><span class="sxs-lookup"><span data-stu-id="a003a-221">Requirement</span></span> | <span data-ttu-id="a003a-222">Valor</span><span class="sxs-lookup"><span data-stu-id="a003a-222">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="a003a-223">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a003a-223">Minimum supported client</span></span><br/> | <span data-ttu-id="a003a-224">\[Somente aplicativos de área de trabalho do Windows 8\]</span><span class="sxs-lookup"><span data-stu-id="a003a-224">Windows 8 \[desktop apps only\]</span></span><br/>           |
| <span data-ttu-id="a003a-225">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="a003a-225">Minimum supported server</span></span><br/> | <span data-ttu-id="a003a-226">\[Somente aplicativos da área de trabalho do Windows Server 2012\]</span><span class="sxs-lookup"><span data-stu-id="a003a-226">Windows Server 2012 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="a003a-227">Confira também</span><span class="sxs-lookup"><span data-stu-id="a003a-227">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a003a-228">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="a003a-228">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
