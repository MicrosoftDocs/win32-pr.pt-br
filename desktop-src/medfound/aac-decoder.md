---
description: 'O decodificador AAC Microsoft Media Foundation é uma transformação Media Foundation que decodifica os seguintes perfis de AAC (codificação de áudio avançada) e AAC (HE-AAC) de alta eficiência:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Decodificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784677"
---
# <a name="aac-decoder"></a><span data-ttu-id="432fe-103">Decodificador AAC</span><span class="sxs-lookup"><span data-stu-id="432fe-103">AAC Decoder</span></span>

<span data-ttu-id="432fe-104">O decodificador AAC Microsoft Media Foundation é uma [transformação Media Foundation](media-foundation-transforms.md) que decodifica os seguintes perfis de AAC (codificação de áudio avançada) e AAC (HE-AAC) de alta eficiência:</span><span class="sxs-lookup"><span data-stu-id="432fe-104">The Microsoft Media Foundation AAC decoder is a [Media Foundation Transform](media-foundation-transforms.md) that decodes the following Advanced Audio Coding (AAC) and High Efficiency AAC (HE-AAC) profiles:</span></span>

-   <span data-ttu-id="432fe-105">Perfil MPEG-2 AAC de baixa complexidade (LC) (multicanal).</span><span class="sxs-lookup"><span data-stu-id="432fe-105">MPEG-2 AAC Low Complexity (LC) profile (multichannel).</span></span>
-   <span data-ttu-id="432fe-106">MPEG-4 HE-AAC V1 (multicanal) com núcleo AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="432fe-106">MPEG-4 HE-AAC v1 (multichannel) with AAC-LC core.</span></span>
-   <span data-ttu-id="432fe-107">MPEG-4 HE-AAC v2 (estéreo) com núcleo AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="432fe-107">MPEG-4 HE-AAC v2 (stereo) with AAC-LC core.</span></span>

<span data-ttu-id="432fe-108">O decodificador AAC dá suporte a fluxos AAC brutos sem cabeçalhos e AAC em um fluxo de transporte de dados de áudio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="432fe-108">The AAC decoder supports both raw AAC streams with no headers and AAC in an audio data transport stream (ADTS).</span></span>

<span data-ttu-id="432fe-109">A partir do Windows 8, o decodificador AAC também dá suporte à decodificação de fluxos de transporte de áudio MPEG-4 com uma camada de multiplexação (LATM) e uma camada de sincronização (LOAS).</span><span class="sxs-lookup"><span data-stu-id="432fe-109">Starting in Windows 8, the AAC decoder also supports decoding MPEG-4 audio transport streams with a multiplex layer (LATM) and synchronization layer (LOAS).</span></span> <span data-ttu-id="432fe-110">Ele também pode converter um fluxo LATM/LOAS em ADTS.</span><span class="sxs-lookup"><span data-stu-id="432fe-110">It can also convert an LATM/LOAS stream to ADTS.</span></span>

## <a name="media-types"></a><span data-ttu-id="432fe-111">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="432fe-111">Media Types</span></span>

<span data-ttu-id="432fe-112">O decodificador AAC dá suporte aos seguintes tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="432fe-112">The AAC decoder supports the following media types.</span></span>

### <a name="input-types"></a><span data-ttu-id="432fe-113">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="432fe-113">Input Types</span></span>

<span data-ttu-id="432fe-114">O decodificador AAC dá suporte aos seguintes subtipos de áudio:</span><span class="sxs-lookup"><span data-stu-id="432fe-114">The AAC decoder supports the following audio subtypes:</span></span>



| <span data-ttu-id="432fe-115">Subtype</span><span class="sxs-lookup"><span data-stu-id="432fe-115">Subtype</span></span>                     | <span data-ttu-id="432fe-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="432fe-116">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | <span data-ttu-id="432fe-117">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="432fe-117">Header</span></span>       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="432fe-118">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="432fe-118">**MFAudioFormat_AAC**</span></span>      | <span data-ttu-id="432fe-119">AAC bruto ou ADTS.</span><span class="sxs-lookup"><span data-stu-id="432fe-119">Raw AAC or ADTS AAC.</span></span><br/> <span data-ttu-id="432fe-120">Para esse subtipo, o tipo de mídia fornece a taxa de amostra e o número de canais antes da aplicação de ferramentas de Spectral Band Replication (SBR) e de estéreo paramétrica (PS), se presente.</span><span class="sxs-lookup"><span data-stu-id="432fe-120">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="432fe-121">O efeito da ferramenta SBR é dobrar a taxa de amostragem decodificada em relação à taxa de amostra AAC-LC principal.</span><span class="sxs-lookup"><span data-stu-id="432fe-121">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="432fe-122">O efeito da ferramenta PS é decodificar o estéreo de um fluxo básico AAC-LC do canal mono.</span><span class="sxs-lookup"><span data-stu-id="432fe-122">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span><br/> <span data-ttu-id="432fe-123">Esse subtipo é equivalente a **MEDIASUBTYPE_MPEG_HEAAC**, definido em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="432fe-123">This subtype is equivalent to **MEDIASUBTYPE_MPEG_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="432fe-124">Consulte [GUIDs de subtipo de áudio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="432fe-124">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span> <br/> <span data-ttu-id="432fe-125">A [origem do arquivo MPEG-4](mpeg-4-file-source.md) e o ANALISAdor ADTS geram esse subtipo.</span><span class="sxs-lookup"><span data-stu-id="432fe-125">The [MPEG-4 File Source](mpeg-4-file-source.md) and the ADTS Parser output this subtype.</span></span> <br/> | <span data-ttu-id="432fe-126">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="432fe-126">mfapi.h</span></span>      |
| <span data-ttu-id="432fe-127">**MEDIASUBTYPE_RAW_AAC1**</span><span class="sxs-lookup"><span data-stu-id="432fe-127">**MEDIASUBTYPE_RAW_AAC1**</span></span> | <span data-ttu-id="432fe-128">AAC bruto.</span><span class="sxs-lookup"><span data-stu-id="432fe-128">Raw AAC.</span></span> <br/> <span data-ttu-id="432fe-129">Esse subtipo é usado para AAC contido em um arquivo AVI com a marca de formato de áudio igual a WAVE_FORMAT_RAW_AAC1 (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="432fe-129">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE_FORMAT_RAW_AAC1 (0x00FF).</span></span> <br/> <span data-ttu-id="432fe-130">Para esse subtipo, o tipo de mídia fornece a taxa de amostra e o número de canais depois que as ferramentas SBR e PS são aplicadas, se presentes.</span><span class="sxs-lookup"><span data-stu-id="432fe-130">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span><br/>                                                                                                                                                                                                                                                                                                                                                                                      | <span data-ttu-id="432fe-131">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="432fe-131">wmcodecdsp.h</span></span> |



 

<span data-ttu-id="432fe-132">Para configurar o decodificador AAC, defina os seguintes atributos no tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="432fe-132">To configure the AAC decoder, set the following attributes on the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="432fe-133">Atributo</span><span class="sxs-lookup"><span data-stu-id="432fe-133">Attribute</span></span></th>
<th><span data-ttu-id="432fe-134">Descrição</span><span class="sxs-lookup"><span data-stu-id="432fe-134">Description</span></span></th>
<th><span data-ttu-id="432fe-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="432fe-135">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="432fe-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-136"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="432fe-137">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="432fe-137">Major type.</span></span></td>
<td><span data-ttu-id="432fe-138">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="432fe-138">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="432fe-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-139"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="432fe-140">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="432fe-140">Audio subtype.</span></span></td>
<td><span data-ttu-id="432fe-141">Consulte a descrição anterior para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="432fe-141">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="432fe-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="432fe-142"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="432fe-143">Perfil de áudio e nível.</span><span class="sxs-lookup"><span data-stu-id="432fe-143">Audio profile and level.</span></span> <br/></td>
<td><span data-ttu-id="432fe-144">Opcional.</span><span class="sxs-lookup"><span data-stu-id="432fe-144">Optional.</span></span> <span data-ttu-id="432fe-145">Aplica-se somente a <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="432fe-145">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <br/> <span data-ttu-id="432fe-146">O valor desse atributo é o campo <strong>audioProfileLevelIndication</strong> , conforme definido por ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="432fe-146">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span> <br/> <span data-ttu-id="432fe-147">Se for desconhecido, defina como zero ou 0xFE ( &quot; nenhum perfil de áudio especificado &quot; ).</span><span class="sxs-lookup"><span data-stu-id="432fe-147">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="432fe-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="432fe-148"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="432fe-149">Tipo de carga.</span><span class="sxs-lookup"><span data-stu-id="432fe-149">Payload type.</span></span><br/></td>
<td><span data-ttu-id="432fe-150">Aplica-se somente a <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="432fe-150">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span> <span data-ttu-id="432fe-151">O decodificador dá suporte aos seguintes tipos de carga:</span><span class="sxs-lookup"><span data-stu-id="432fe-151">The decoder supports the following payload types:</span></span> <br/>
<ul>
<li><span data-ttu-id="432fe-152">0: AAC bruto.</span><span class="sxs-lookup"><span data-stu-id="432fe-152">0: Raw AAC.</span></span> <span data-ttu-id="432fe-153">O fluxo contém apenas elementos raw_data_block (), conforme definido por MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="432fe-153">The stream contains raw_data_block() elements only, as defined by MPEG-2.</span></span></li>
<li><span data-ttu-id="432fe-154">1: ADTS.</span><span class="sxs-lookup"><span data-stu-id="432fe-154">1: ADTS.</span></span> <span data-ttu-id="432fe-155">O fluxo contém um adts_sequence (), conforme definido por MPEG-2.</span><span class="sxs-lookup"><span data-stu-id="432fe-155">The stream contains an adts_sequence(), as defined by MPEG-2.</span></span> <span data-ttu-id="432fe-156">Somente um raw_data_block () por adts_frame () é permitido.</span><span class="sxs-lookup"><span data-stu-id="432fe-156">Only one raw_data_block() per adts_frame() is allowed.</span></span></li>
<li><span data-ttu-id="432fe-157">3: fluxo de transporte de áudio com uma camada de sincronização (LOAS) e uma camada de multiplexação (LATM).</span><span class="sxs-lookup"><span data-stu-id="432fe-157">3: Audio transport stream with a synchronization layer (LOAS) and a multiplex layer (LATM).</span></span> <span data-ttu-id="432fe-158">Dos três tipos de LOAS, há suporte apenas para <strong>AudioSyncStream</strong> .</span><span class="sxs-lookup"><span data-stu-id="432fe-158">Of the three types of LOAS, only <strong>AudioSyncStream</strong> is supported.</span></span> <span data-ttu-id="432fe-159">A camada multiplex é <strong>AudioMuxElement</strong>, restrita a um programa de áudio e uma camada.</span><span class="sxs-lookup"><span data-stu-id="432fe-159">The multiplex layer is <strong>AudioMuxElement</strong>, restricted to one audio program and one layer.</span></span></li>
</ul><span data-ttu-id="432fe-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> é opcional.</span><span class="sxs-lookup"><span data-stu-id="432fe-160">
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="432fe-161">Se esse atributo não for especificado, o valor padrão 0 será usado, o que especificará que o fluxo contém apenas elementos de raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="432fe-161">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="432fe-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-162"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="432fe-163">Profundidade de bits desejada do áudio PCM decodificado.</span><span class="sxs-lookup"><span data-stu-id="432fe-163">Desired bit depth of the decoded PCM audio.</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="432fe-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-164"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="432fe-165">Especifica a atribuição de canais de áudio a posições do orador.</span><span class="sxs-lookup"><span data-stu-id="432fe-165">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="432fe-166">Opcional.</span><span class="sxs-lookup"><span data-stu-id="432fe-166">Optional.</span></span> <span data-ttu-id="432fe-167">Para obter mais informações, consulte <a href="#format-constraints">Format Constraints</a>.</span><span class="sxs-lookup"><span data-stu-id="432fe-167">For more information, see <a href="#format-constraints">Format Constraints</a>.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="432fe-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-168"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="432fe-169">Número de canais, incluindo o canal de baixa frequência (LFE), se presente.</span><span class="sxs-lookup"><span data-stu-id="432fe-169">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/></td>
<td><span data-ttu-id="432fe-170">A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="432fe-170">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="432fe-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-171"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="432fe-172">Taxa de amostragem, em amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="432fe-172">Sample rate, in samples per second.</span></span><br/></td>
<td><span data-ttu-id="432fe-173">A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="432fe-173">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="432fe-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-174"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="432fe-175">Informações de formato adicionais.</span><span class="sxs-lookup"><span data-stu-id="432fe-175">Additional format information.</span></span></td>
<td><span data-ttu-id="432fe-176">O valor desse atributo depende do subtipo.</span><span class="sxs-lookup"><span data-stu-id="432fe-176">The value of this attribute depends on the subtype.</span></span><br/>
<ul>
<li><span data-ttu-id="432fe-177"><strong>MFAudioFormat_AAC</strong>: contém a parte da estrutura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece após a estrutura <strong>WAVEFORMATEX</strong> (ou seja, após o membro <strong>WFX</strong> ).</span><span class="sxs-lookup"><span data-stu-id="432fe-177"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="432fe-178">Isso é seguido pelos dados de AudioSpecificConfig (), conforme definido por ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="432fe-178">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="432fe-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contém os dados de AudioSpecificConfig ().</span><span class="sxs-lookup"><span data-stu-id="432fe-179"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span> <span data-ttu-id="432fe-180">Esses dados devem aparecer; caso contrário, o decodificador rejeitará o tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="432fe-180">This data must appear; otherwise, the decoder will reject the media type.</span></span></li>
</ul>
<span data-ttu-id="432fe-181">O comprimento dos dados de AudioSpecificConfig () é de 2 bytes para AAC-LC ou HE-AAC com sinalização implícita de SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="432fe-181">The length of the AudioSpecificConfig() data is 2 bytes for AAC-LC or HE-AAC with implicit signaling of SBR/PS.</span></span> <span data-ttu-id="432fe-182">É mais de 2 bytes para HE-AAC com sinalização explícita de SBR/PS.</span><span class="sxs-lookup"><span data-stu-id="432fe-182">It is more than 2 bytes for HE-AAC with explicit signaling of SBR/PS.</span></span><br/> <span data-ttu-id="432fe-183">O valor de <strong>audioObjectType</strong> conforme definido em AudioSpecificConfig () deve ser 2, indicando AAC-LC.</span><span class="sxs-lookup"><span data-stu-id="432fe-183">The value of <strong>audioObjectType</strong> as defined in AudioSpecificConfig() must be 2, indicating AAC-LC.</span></span> <span data-ttu-id="432fe-184">O valor de <strong>extensionAudioObjectType</strong> deve ser 5 para SBR ou 29 para PS.</span><span class="sxs-lookup"><span data-stu-id="432fe-184">The value of <strong>extensionAudioObjectType</strong> must be 5 for SBR or 29 for PS.</span></span> <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a><span data-ttu-id="432fe-185">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="432fe-185">Output Types</span></span>

<span data-ttu-id="432fe-186">O decodificador dá suporte aos seguintes tipos de saída:</span><span class="sxs-lookup"><span data-stu-id="432fe-186">The decoder supports the following output types:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="432fe-187">Subtype</span><span class="sxs-lookup"><span data-stu-id="432fe-187">Subtype</span></span></th>
<th><span data-ttu-id="432fe-188">Descrição</span><span class="sxs-lookup"><span data-stu-id="432fe-188">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="432fe-189"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="432fe-189"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="432fe-190">Áudio de ponto flutuante do IEEE.</span><span class="sxs-lookup"><span data-stu-id="432fe-190">IEEE floating-point audio.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="432fe-191"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="432fe-191"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="432fe-192">áudio PCM de 16 bits.</span><span class="sxs-lookup"><span data-stu-id="432fe-192">16-bit PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="432fe-193"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="432fe-193"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="432fe-194">Requer o Windows 8.</span><span class="sxs-lookup"><span data-stu-id="432fe-194">Requires Windows 8.</span></span> <br/> <span data-ttu-id="432fe-195">Esse tipo de saída pode ser usado para converter um fluxo AAC no formato LOAS/LATM no formato ADTS.</span><span class="sxs-lookup"><span data-stu-id="432fe-195">This output type can be used to convert an AAC stream in the LOAS/LATM format to ADTS format.</span></span> <br/> <span data-ttu-id="432fe-196">Para converter um fluxo de LOAS/LATM em um fluxo de ADTS, defina o tipo de entrada como <strong>MFAudioFormat_AAC</strong> com o tipo de carga 3 (loas).</span><span class="sxs-lookup"><span data-stu-id="432fe-196">To convert an LOAS/LATM stream to an ADTS stream, set the input type to <strong>MFAudioFormat_AAC</strong> with payload type 3 (LOAS).</span></span> <span data-ttu-id="432fe-197">Em seguida, defina o tipo de saída como <strong>MFAudioFormat_AAC</strong> com o tipo de carga 1 (ADTS).</span><span class="sxs-lookup"><span data-stu-id="432fe-197">Then set the output type to <strong>MFAudioFormat_AAC</strong> with payload type 1 (ADTS).</span></span> <span data-ttu-id="432fe-198">O decodificador reformatará o conainter sem decodificar o fragmentado.</span><span class="sxs-lookup"><span data-stu-id="432fe-198">The decoder will reformat the conainter without decoding the bitstream.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="432fe-199">O decodificador não registra <strong>MFAudioFormat_AAC</strong> como um tipo de saída.</span><span class="sxs-lookup"><span data-stu-id="432fe-199">The decoder does not register <strong>MFAudioFormat_AAC</strong> as an output type.</span></span> <span data-ttu-id="432fe-200">No entanto, se o aplicativo definir o tipo de entrada conforme descrito, o método <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform:: GetOutputAvailableType</strong></a> retornará <strong>MFAudioFormat_AAC</strong> na lista de tipos de saída disponíveis.</span><span class="sxs-lookup"><span data-stu-id="432fe-200">However, if the application sets the input type as described, the <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> method returns <strong>MFAudioFormat_AAC</strong> in the list of available output types.</span></span>
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="432fe-201">Se o fluxo de entrada contiver mais de dois canais, o decodificador AAC fornecerá duas opções para o formato de saída:</span><span class="sxs-lookup"><span data-stu-id="432fe-201">If the input stream contains more than two channels, the AAC decoder provides two options for the output format:</span></span>

-   <span data-ttu-id="432fe-202">A mesma configuração de canal que o tipo de entrada.</span><span class="sxs-lookup"><span data-stu-id="432fe-202">The same channel configuration as the input type.</span></span>
-   <span data-ttu-id="432fe-203">Dobra estéreo.</span><span class="sxs-lookup"><span data-stu-id="432fe-203">Stereo fold-down.</span></span>

## <a name="format-constraints"></a><span data-ttu-id="432fe-204">Restrições de formato</span><span class="sxs-lookup"><span data-stu-id="432fe-204">Format Constraints</span></span>

<span data-ttu-id="432fe-205">A taxa de amostragem de áudio decodificada deve ser uma das seguintes, após a aplicação de SBR (se houver):</span><span class="sxs-lookup"><span data-stu-id="432fe-205">The decoded audio sampling rate must be one of the following, after SBR is applied (if present):</span></span>

-   <span data-ttu-id="432fe-206">8 kHz</span><span class="sxs-lookup"><span data-stu-id="432fe-206">8 kHz</span></span>
-   <span data-ttu-id="432fe-207">11, 25 kHz</span><span class="sxs-lookup"><span data-stu-id="432fe-207">11.025 kHz</span></span>
-   <span data-ttu-id="432fe-208">12 kHz</span><span class="sxs-lookup"><span data-stu-id="432fe-208">12 kHz</span></span>
-   <span data-ttu-id="432fe-209">16 kHz</span><span class="sxs-lookup"><span data-stu-id="432fe-209">16 kHz</span></span>
-   <span data-ttu-id="432fe-210">22, 5 kHz</span><span class="sxs-lookup"><span data-stu-id="432fe-210">22.05 kHz</span></span>
-   <span data-ttu-id="432fe-211">24 kHz</span><span class="sxs-lookup"><span data-stu-id="432fe-211">24 kHz</span></span>
-   <span data-ttu-id="432fe-212">32 kHz</span><span class="sxs-lookup"><span data-stu-id="432fe-212">32 kHz</span></span>
-   <span data-ttu-id="432fe-213">44,1 kHz</span><span class="sxs-lookup"><span data-stu-id="432fe-213">44.1 kHz</span></span>
-   <span data-ttu-id="432fe-214">48 kHz</span><span class="sxs-lookup"><span data-stu-id="432fe-214">48 kHz</span></span>

<span data-ttu-id="432fe-215">As taxas de amostragem acima de 48 kHz não são suportadas.</span><span class="sxs-lookup"><span data-stu-id="432fe-215">Sampling rates above 48 kHz are not supported.</span></span>

<span data-ttu-id="432fe-216">O decodificador dá suporte a até 6 canais de áudio.</span><span class="sxs-lookup"><span data-stu-id="432fe-216">The decoder supports up to 6 audio channels.</span></span> <span data-ttu-id="432fe-217">Para cada configuração de palestrante, o decodificador espera que os elementos AAC sintáticas apareçam em uma determinada ordem.</span><span class="sxs-lookup"><span data-stu-id="432fe-217">For each speaker configuration, the decoder expects the AAC syntactic elements to appear in a certain order.</span></span> <span data-ttu-id="432fe-218">A tabela a seguir lista as configurações de alto-falante com suporte.</span><span class="sxs-lookup"><span data-stu-id="432fe-218">The following table lists the supported speaker configurations.</span></span> <span data-ttu-id="432fe-219">A terceira coluna da tabela lista os elementos sintáticas esperados e sua ordem, usando a seguinte notação:</span><span class="sxs-lookup"><span data-stu-id="432fe-219">The third column of the table lists the expected syntactic elements and their order, using the following notation:</span></span>

-   <span data-ttu-id="432fe-220"><SCE1>: O single_channel_element (SCE) associado ao orador do front Center.</span><span class="sxs-lookup"><span data-stu-id="432fe-220"><SCE1>: The single_channel_element (SCE) associated with the front center speaker.</span></span>
-   <span data-ttu-id="432fe-221"><SCE2>: O SCE associado ao viva-voz do centro.</span><span class="sxs-lookup"><span data-stu-id="432fe-221"><SCE2>: The SCE associated with the back center speaker.</span></span>
-   <span data-ttu-id="432fe-222"><CPE1>: O channel_pair_element (CPE) associado aos alto-falantes da frente.</span><span class="sxs-lookup"><span data-stu-id="432fe-222"><CPE1>: The channel_pair_element (CPE) associated with the front speakers.</span></span>
-   <span data-ttu-id="432fe-223"><CPE2>: A CPE associada aos alto-falantes de volta (ou lado)</span><span class="sxs-lookup"><span data-stu-id="432fe-223"><CPE2>: The CPE associated with the back (or side) speakers</span></span>
-   <span data-ttu-id="432fe-224"><LFE>: O lfe_channel_element (LFE).</span><span class="sxs-lookup"><span data-stu-id="432fe-224"><LFE>: The lfe_channel_element (LFE).</span></span>

<span data-ttu-id="432fe-225">Para obter mais informações sobre esses elementos sintáticos, consulte ISO/IEC 13818-7.</span><span class="sxs-lookup"><span data-stu-id="432fe-225">For more information about these syntactic elements, refer to ISO/IEC 13818-7.</span></span>



| <span data-ttu-id="432fe-226">Configuração</span><span class="sxs-lookup"><span data-stu-id="432fe-226">Configuration</span></span>       | <span data-ttu-id="432fe-227">Máscara de canal</span><span class="sxs-lookup"><span data-stu-id="432fe-227">Channel Mask</span></span>                                                                                                                                                              | <span data-ttu-id="432fe-228">Elementos de sintaxe AAC</span><span class="sxs-lookup"><span data-stu-id="432fe-228">AAC Syntactic Elements</span></span>                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| <span data-ttu-id="432fe-229">Mono</span><span class="sxs-lookup"><span data-stu-id="432fe-229">Mono</span></span>                | <span data-ttu-id="432fe-230">**SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="432fe-230">**SPEAKER_FRONT_CENTER**</span></span>                                                                                                                                                | <SCE1>                                    |
| <span data-ttu-id="432fe-231">Estéreo ou mono duplo</span><span class="sxs-lookup"><span data-stu-id="432fe-231">Stereo or dual mono</span></span> | <span data-ttu-id="432fe-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="432fe-232">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**</span></span>                                                                                                                     | <CPE1>                                    |
| <span data-ttu-id="432fe-233">2/1</span><span class="sxs-lookup"><span data-stu-id="432fe-233">2/1</span></span>                 | <span data-ttu-id="432fe-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="432fe-234">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**</span></span>                                                                                        | <CPE1><SCE1>                        |
| <span data-ttu-id="432fe-235">2/2</span><span class="sxs-lookup"><span data-stu-id="432fe-235">2/2</span></span>                 | <span data-ttu-id="432fe-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="432fe-236">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                                              | <CPE1><CPE2>                        |
| <span data-ttu-id="432fe-237">3/0</span><span class="sxs-lookup"><span data-stu-id="432fe-237">3/0</span></span>                 | <span data-ttu-id="432fe-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span><span class="sxs-lookup"><span data-stu-id="432fe-238">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**</span></span>                                                                                       | <SCE1><CPE1>                        |
| <span data-ttu-id="432fe-239">3/1</span><span class="sxs-lookup"><span data-stu-id="432fe-239">3/1</span></span>                 | <span data-ttu-id="432fe-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span><span class="sxs-lookup"><span data-stu-id="432fe-240">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**</span></span>                                                          | <SCE1><CPE1><SCE2>            |
| <span data-ttu-id="432fe-241">3/2</span><span class="sxs-lookup"><span data-stu-id="432fe-241">3/2</span></span>                 | <span data-ttu-id="432fe-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="432fe-242">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span>                                | <SCE1><CPE1><CPE2>            |
| <span data-ttu-id="432fe-243">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="432fe-243">3/2 + LFE</span></span>           | <span data-ttu-id="432fe-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span><span class="sxs-lookup"><span data-stu-id="432fe-244">**SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**</span></span> | <SCE1><CPE1><CPE2><LFE> |



 

<span data-ttu-id="432fe-245">Para AAC bruto, cada amostra de entrada deve conter exatamente um quadro compactado AAC completo.</span><span class="sxs-lookup"><span data-stu-id="432fe-245">For raw AAC, each input sample must contain exactly one full AAC compressed frame.</span></span>

<span data-ttu-id="432fe-246">Para ADTS, cada amostra de entrada pode conter vários quadros de áudio, bem como os quadros parciais, os quadros podem abranger os limites de amostra.</span><span class="sxs-lookup"><span data-stu-id="432fe-246">For ADTS, each input sample can contain multiple audio frames, as well as partial frames   that is, frames can span sample boundaries.</span></span> <span data-ttu-id="432fe-247">Cada cabeçalho ADTS deve ser seguido por um quadro AAC.</span><span class="sxs-lookup"><span data-stu-id="432fe-247">Each ADTS header must be followed by one AAC frame.</span></span>

<span data-ttu-id="432fe-248">O decodificador AAC não oferece suporte a nenhum dos seguintes itens:</span><span class="sxs-lookup"><span data-stu-id="432fe-248">The AAC decoder does not support any of the following:</span></span>

-   <span data-ttu-id="432fe-249">Perfil principal, perfil do SRS (Sample-Rate escalonável) ou perfil de previsão de longo prazo (LTP).</span><span class="sxs-lookup"><span data-stu-id="432fe-249">Main profile, Sample-Rate Scalable (SRS) profile, or Long Term Prediction (LTP) profile.</span></span>
-   <span data-ttu-id="432fe-250">Formato de intercâmbio de dados de áudio (ADIF).</span><span class="sxs-lookup"><span data-stu-id="432fe-250">Audio data interchange format (ADIF).</span></span>
-   <span data-ttu-id="432fe-251">Fluxos de transporte LATM/LAOS.</span><span class="sxs-lookup"><span data-stu-id="432fe-251">LATM/LAOS transport streams.</span></span>
-   <span data-ttu-id="432fe-252">Elementos de canal de acoplamento (CCEs).</span><span class="sxs-lookup"><span data-stu-id="432fe-252">Coupling channel elements (CCEs).</span></span> <span data-ttu-id="432fe-253">O decodificador irá ignorar os quadros de áudio com CCEs.</span><span class="sxs-lookup"><span data-stu-id="432fe-253">The decoder will skip audio frames with CCEs.</span></span>
-   <span data-ttu-id="432fe-254">AAC-LC com um tamanho de quadro de 960-amostra.</span><span class="sxs-lookup"><span data-stu-id="432fe-254">AAC-LC with a 960-sample frame size.</span></span> <span data-ttu-id="432fe-255">Somente há suporte para quadros de exemplo 1024.</span><span class="sxs-lookup"><span data-stu-id="432fe-255">Only 1024-sample frames are supported.</span></span>

## <a name="transform-attributes"></a><span data-ttu-id="432fe-256">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="432fe-256">Transform Attributes</span></span>

<span data-ttu-id="432fe-257">O decodificador AAC implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="432fe-257">The AAC decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="432fe-258">Os aplicativos podem usar esse método para obter ou definir os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="432fe-258">Applications can use this method to get or set the following attributes.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="432fe-259">Atributo</span><span class="sxs-lookup"><span data-stu-id="432fe-259">Attribute</span></span></th>
<th><span data-ttu-id="432fe-260">Descrição</span><span class="sxs-lookup"><span data-stu-id="432fe-260">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="432fe-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-261"><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></span></span></td>
<td><span data-ttu-id="432fe-262">Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo.</span><span class="sxs-lookup"><span data-stu-id="432fe-262">Specifies whether 2-channel audio is encoded as stereo or dual mono.</span></span> <span data-ttu-id="432fe-263">Tratar como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="432fe-263">Treat as read-only.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="432fe-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-264"><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></span></span></td>
<td><span data-ttu-id="432fe-265">Especifica como o decodificador Reproduz áudio mono duplo.</span><span class="sxs-lookup"><span data-stu-id="432fe-265">Specifies how the decoder reproduces dual mono audio.</span></span> <span data-ttu-id="432fe-266">O valor padrão é <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: saída CH1 para os alto-falantes esquerdo e direito.</span><span class="sxs-lookup"><span data-stu-id="432fe-266">The default value is <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Output Ch1 to the left and right speakers.</span></span> <br/> <span data-ttu-id="432fe-267">Os aplicativos podem definir essa propriedade para alterar o comportamento padrão.</span><span class="sxs-lookup"><span data-stu-id="432fe-267">Applications can set this property to change the default behavior.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="432fe-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span><span class="sxs-lookup"><span data-stu-id="432fe-268"><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></span></span></td>
<td><span data-ttu-id="432fe-269">O decodificador AAC não manipula alterações de formato dinâmico e deve ser liberado ou esgotado antes que um novo tipo de mídia de entrada seja definido.</span><span class="sxs-lookup"><span data-stu-id="432fe-269">The AAC decoder does not handle dynamic format changes, and must be flushed or drained before a new input media type is set.</span></span> <span data-ttu-id="432fe-270">Trate este atributo como somente leitura.</span><span class="sxs-lookup"><span data-stu-id="432fe-270">Treat this attribute as read-only.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="432fe-271">O decodificador AAC relata incorretamente um valor de <strong>true</strong> para este atributo.</span><span class="sxs-lookup"><span data-stu-id="432fe-271">The AAC decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span>
</blockquote>
<br/> <br/> <span data-ttu-id="432fe-272">No Windows 7, o decodificador relata incorretamente um valor de <strong>true</strong> para esse atributo.</span><span class="sxs-lookup"><span data-stu-id="432fe-272">In Windows 7, the decoder incorrectly reports a value of <strong>TRUE</strong> for this attribute.</span></span> <span data-ttu-id="432fe-273">No Windows 8, o decodificador relata <strong>false</strong>, que é o valor correto</span><span class="sxs-lookup"><span data-stu-id="432fe-273">In Windows 8, the decoder reports <strong>FALSE</strong>, which is the correct value</span></span><br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a><span data-ttu-id="432fe-274">Exemplos de tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="432fe-274">Example Media Types</span></span>

<span data-ttu-id="432fe-275">Aqui está um exemplo do tipo de mídia de entrada necessário para um fluxo AAC-LC de 6 canais, 48-kHz, usando uma carga AAC bruta:</span><span class="sxs-lookup"><span data-stu-id="432fe-275">Here is an example of the input media type needed for a 6-channel, 48-kHz AAC-LC stream, using a raw AAC payload:</span></span>



| <span data-ttu-id="432fe-276">Atributo</span><span class="sxs-lookup"><span data-stu-id="432fe-276">Attribute</span></span>                                                                                      | <span data-ttu-id="432fe-277">Valor</span><span class="sxs-lookup"><span data-stu-id="432fe-277">Value</span></span>                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="432fe-278">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="432fe-278">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                      | <span data-ttu-id="432fe-279">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="432fe-279">**MFMediaType_Audio**</span></span>                                                               |
| [<span data-ttu-id="432fe-280">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="432fe-280">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                             | <span data-ttu-id="432fe-281">**MFAudioFormat_AAC**</span><span class="sxs-lookup"><span data-stu-id="432fe-281">**MFAudioFormat_AAC**</span></span>                                                               |
| [<span data-ttu-id="432fe-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="432fe-282">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)        | <span data-ttu-id="432fe-283">48000</span><span class="sxs-lookup"><span data-stu-id="432fe-283">48000</span></span>                                                                                |
| [<span data-ttu-id="432fe-284">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="432fe-284">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                     | <span data-ttu-id="432fe-285">6</span><span class="sxs-lookup"><span data-stu-id="432fe-285">6</span></span>                                                                                    |
| [<span data-ttu-id="432fe-286">MF_MT_AAC_PAYLOAD_TYPE</span><span class="sxs-lookup"><span data-stu-id="432fe-286">MF_MT_AAC_PAYLOAD_TYPE</span></span>](mf-mt-aac-payload-type.md)                                       | <span data-ttu-id="432fe-287">0</span><span class="sxs-lookup"><span data-stu-id="432fe-287">0</span></span>                                                                                    |
| [<span data-ttu-id="432fe-288">**MF_MT_USER_DATA**</span><span class="sxs-lookup"><span data-stu-id="432fe-288">**MF_MT_USER_DATA**</span></span>](mf-mt-user-data-attribute.md)                                        | <span data-ttu-id="432fe-289">{0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span><span class="sxs-lookup"><span data-stu-id="432fe-289">{0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0}</span></span> |
| [<span data-ttu-id="432fe-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span><span class="sxs-lookup"><span data-stu-id="432fe-290">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</span></span>](mf-mt-aac-audio-profile-level-indication.md) | <span data-ttu-id="432fe-291">0x2A (opcional)</span><span class="sxs-lookup"><span data-stu-id="432fe-291">0x2a (optional)</span></span>                                                                      |



 

<span data-ttu-id="432fe-292">Os primeiros 12 bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspondem aos seguintes membros da estrutura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) :</span><span class="sxs-lookup"><span data-stu-id="432fe-292">The first 12 bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspond to the following [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) structure members:</span></span>

-   <span data-ttu-id="432fe-293">**wPayloadType** = 0 (AAC bruto)</span><span class="sxs-lookup"><span data-stu-id="432fe-293">**wPayloadType** = 0 (raw AAC)</span></span>
-   <span data-ttu-id="432fe-294">**wAudioProfileLevelIndication** = 0X2a (perfil AAC, nível 4)</span><span class="sxs-lookup"><span data-stu-id="432fe-294">**wAudioProfileLevelIndication** = 0x2a (AAC Profile, Level 4)</span></span>
-   <span data-ttu-id="432fe-295">**wStructType** = 0</span><span class="sxs-lookup"><span data-stu-id="432fe-295">**wStructType** = 0</span></span>

<span data-ttu-id="432fe-296">Os dois últimos bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contêm o valor de AudioSpecificConfig (), conforme definido pelo MPEG-4.</span><span class="sxs-lookup"><span data-stu-id="432fe-296">The last two bytes of [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contain the value of AudioSpecificConfig(), as defined by MPEG-4.</span></span>

-   <span data-ttu-id="432fe-297">AudioSpecificConfig. audioObjectType = 2 (AAC LC) (5 bits)</span><span class="sxs-lookup"><span data-stu-id="432fe-297">AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)</span></span>
-   <span data-ttu-id="432fe-298">AudioSpecificConfig. samplingFrequencyIndex = 3 (4 bits)</span><span class="sxs-lookup"><span data-stu-id="432fe-298">AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)</span></span>
-   <span data-ttu-id="432fe-299">AudioSpecificConfig. channelConfiguration = 6 (4 bits)</span><span class="sxs-lookup"><span data-stu-id="432fe-299">AudioSpecificConfig.channelConfiguration = 6 (4 bits)</span></span>
-   <span data-ttu-id="432fe-300">GASpecificConfig. frameLengthFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="432fe-300">GASpecificConfig.frameLengthFlag = 0 (1 bit)</span></span>
-   <span data-ttu-id="432fe-301">GASpecificConfig. dependsOnCoreCoder = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="432fe-301">GASpecificConfig.dependsOnCoreCoder = 0 (1 bit)</span></span>
-   <span data-ttu-id="432fe-302">GASpecificConfig. extensionFlag = 0 (1 bit)</span><span class="sxs-lookup"><span data-stu-id="432fe-302">GASpecificConfig.extensionFlag = 0 (1 bit)</span></span>

<span data-ttu-id="432fe-303">Dado esse tipo de entrada, use o seguinte tipo de mídia de saída para obter o áudio PCM de ponto flutuante de 6 canais, 32 bits do decodificador:</span><span class="sxs-lookup"><span data-stu-id="432fe-303">Given this input type, use the following output media type to get 6-channel, 32-bit floating point PCM audio from the decoder:</span></span>



| <span data-ttu-id="432fe-304">Atributo</span><span class="sxs-lookup"><span data-stu-id="432fe-304">Attribute</span></span>                                                                                    | <span data-ttu-id="432fe-305">Valor</span><span class="sxs-lookup"><span data-stu-id="432fe-305">Value</span></span>                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [<span data-ttu-id="432fe-306">**MF_MT_MAJOR_TYPE**</span><span class="sxs-lookup"><span data-stu-id="432fe-306">**MF_MT_MAJOR_TYPE**</span></span>](mf-mt-major-type-attribute.md)                                    | <span data-ttu-id="432fe-307">**MFMediaType_Audio**</span><span class="sxs-lookup"><span data-stu-id="432fe-307">**MFMediaType_Audio**</span></span>   |
| [<span data-ttu-id="432fe-308">**MF_MT_SUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="432fe-308">**MF_MT_SUBTYPE**</span></span>](mf-mt-subtype-attribute.md)                                           | <span data-ttu-id="432fe-309">**MFAudioFormat_Float**</span><span class="sxs-lookup"><span data-stu-id="432fe-309">**MFAudioFormat_Float**</span></span> |
| [<span data-ttu-id="432fe-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span><span class="sxs-lookup"><span data-stu-id="432fe-310">**MF_MT_AUDIO_BITS_PER_SAMPLE**</span></span>](mf-mt-audio-bits-per-sample-attribute.md)            | <span data-ttu-id="432fe-311">32</span><span class="sxs-lookup"><span data-stu-id="432fe-311">32</span></span>                       |
| [<span data-ttu-id="432fe-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="432fe-312">**MF_MT_AUDIO_SAMPLES_PER_SECOND**</span></span>](mf-mt-audio-samples-per-second-attribute.md)      | <span data-ttu-id="432fe-313">48000</span><span class="sxs-lookup"><span data-stu-id="432fe-313">48000</span></span>                    |
| [<span data-ttu-id="432fe-314">**MF_MT_AUDIO_NUM_CHANNELS**</span><span class="sxs-lookup"><span data-stu-id="432fe-314">**MF_MT_AUDIO_NUM_CHANNELS**</span></span>](mf-mt-audio-num-channels-attribute.md)                   | <span data-ttu-id="432fe-315">6</span><span class="sxs-lookup"><span data-stu-id="432fe-315">6</span></span>                        |
| [<span data-ttu-id="432fe-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span><span class="sxs-lookup"><span data-stu-id="432fe-316">**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**</span></span>](mf-mt-audio-avg-bytes-per-second-attribute.md) | <span data-ttu-id="432fe-317">1152000 (opcional)</span><span class="sxs-lookup"><span data-stu-id="432fe-317">1152000 (optional)</span></span>       |
| [<span data-ttu-id="432fe-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span><span class="sxs-lookup"><span data-stu-id="432fe-318">**MF_MT_AUDIO_BLOCK_ALIGNMENT**</span></span>](mf-mt-audio-block-alignment-attribute.md)             | <span data-ttu-id="432fe-319">24 (opcional)</span><span class="sxs-lookup"><span data-stu-id="432fe-319">24 (optional)</span></span>            |
| [<span data-ttu-id="432fe-320">**MF_MT_AUDIO_CHANNEL_MASK**</span><span class="sxs-lookup"><span data-stu-id="432fe-320">**MF_MT_AUDIO_CHANNEL_MASK**</span></span>](mf-mt-audio-channel-mask-attribute.md)                   | <span data-ttu-id="432fe-321">0x3F (opcional)</span><span class="sxs-lookup"><span data-stu-id="432fe-321">0x3f (optional)</span></span>          |



 

<span data-ttu-id="432fe-322">Se o suplemento de atualização de plataforma para Windows Vista estiver instalado, o decodificador de áudio AAC estará disponível no Windows Vista, mas poderá ser acessado somente no Windows Vista usando o [leitor de origem](source-reader.md).</span><span class="sxs-lookup"><span data-stu-id="432fe-322">If Platform Update Supplement for Windows Vista is installed, the AAC audio decoder is available on Windows Vista, but is accessible on Windows Vista only by using the [Source Reader](source-reader.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="432fe-323">Requisitos</span><span class="sxs-lookup"><span data-stu-id="432fe-323">Requirements</span></span>



| <span data-ttu-id="432fe-324">Requisito</span><span class="sxs-lookup"><span data-stu-id="432fe-324">Requirement</span></span> | <span data-ttu-id="432fe-325">Valor</span><span class="sxs-lookup"><span data-stu-id="432fe-325">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="432fe-326">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="432fe-326">Minimum supported client</span></span><br/> | <span data-ttu-id="432fe-327">\[Somente aplicativos de área de trabalho do Windows 7\]</span><span class="sxs-lookup"><span data-stu-id="432fe-327">Windows 7 \[desktop apps only\]</span></span><br/>                                                                                                                                                  |
| <span data-ttu-id="432fe-328">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="432fe-328">Minimum supported server</span></span><br/> | <span data-ttu-id="432fe-329">\[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]</span><span class="sxs-lookup"><span data-stu-id="432fe-329">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                                                                                                     |
| <span data-ttu-id="432fe-330">DLL</span><span class="sxs-lookup"><span data-stu-id="432fe-330">DLL</span></span><br/>                      | <dl> <span data-ttu-id="432fe-331"><dt>Msmpeg2adec.dll no Windows 7; </dt> <dt>MSAudDecMFT.dll no Windows 8</dt></span><span class="sxs-lookup"><span data-stu-id="432fe-331"><dt>Msmpeg2adec.dll on Windows 7; </dt> <dt>MSAudDecMFT.dll on Windows 8</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="432fe-332">Confira também</span><span class="sxs-lookup"><span data-stu-id="432fe-332">See also</span></span>

<dl> <dt>

[<span data-ttu-id="432fe-333">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="432fe-333">Codec Objects</span></span>](codecobjects.md)
</dt> <dt>

[<span data-ttu-id="432fe-334">Tipos de mídia AAC</span><span class="sxs-lookup"><span data-stu-id="432fe-334">AAC Media Types</span></span>](aac-media-types.md)
</dt> <dt>

[<span data-ttu-id="432fe-335">Tipos de mídia de áudio</span><span class="sxs-lookup"><span data-stu-id="432fe-335">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="432fe-336">**Decodificador de áudio do Microsoft MPEG-1/DD/AAC**</span><span class="sxs-lookup"><span data-stu-id="432fe-336">**Microsoft MPEG-1/DD/AAC Audio Decoder**</span></span>](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[<span data-ttu-id="432fe-337">Suporte a MPEG-4 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="432fe-337">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="432fe-338">Formatos de mídia compatíveis com o Media Foundation</span><span class="sxs-lookup"><span data-stu-id="432fe-338">Supported Media Formats in Media Foundation</span></span>](supported-media-formats-in-media-foundation.md)
</dt> </dl>
