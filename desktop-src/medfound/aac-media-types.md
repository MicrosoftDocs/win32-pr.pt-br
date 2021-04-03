---
description: Este tópico descreve como especificar o formato de um fluxo AAC (codificação de áudio avançado) no Media Foundation.
ms.assetid: 82218bc5-6660-4253-b50c-b6d9f30be3d5
title: Tipos de mídia AAC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab95423b26a0e2a327b599011e88a05ab2ab58c5
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/03/2021
ms.locfileid: "103930089"
---
# <a name="aac-media-types"></a><span data-ttu-id="b2490-103">Tipos de mídia AAC</span><span class="sxs-lookup"><span data-stu-id="b2490-103">AAC Media Types</span></span>

<span data-ttu-id="b2490-104">Este tópico descreve como especificar o formato de um fluxo AAC (codificação de áudio avançado) no Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="b2490-104">This topic describes how to specify the format of an Advanced Audio Coding (AAC) stream in Media Foundation.</span></span>

<span data-ttu-id="b2490-105">Dois subtipos são definidos para áudio AAC:</span><span class="sxs-lookup"><span data-stu-id="b2490-105">Two subtypes are defined for AAC audio:</span></span>



| <span data-ttu-id="b2490-106">Subtype</span><span class="sxs-lookup"><span data-stu-id="b2490-106">Subtype</span></span>                     | <span data-ttu-id="b2490-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2490-107">Description</span></span>          | <span data-ttu-id="b2490-108">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="b2490-108">Header</span></span>       |
|-----------------------------|----------------------|--------------|
| <span data-ttu-id="b2490-109">**\_AAC MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="b2490-109">**MFAudioFormat\_AAC**</span></span>      | <span data-ttu-id="b2490-110">AAC bruto ou ADTS.</span><span class="sxs-lookup"><span data-stu-id="b2490-110">Raw AAC or ADTS AAC.</span></span> | <span data-ttu-id="b2490-111">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="b2490-111">mfapi.h</span></span>      |
| <span data-ttu-id="b2490-112">**\_AAC1 bruto \_ MEDIASUBTYPE**</span><span class="sxs-lookup"><span data-stu-id="b2490-112">**MEDIASUBTYPE\_RAW\_AAC1**</span></span> | <span data-ttu-id="b2490-113">AAC bruto.</span><span class="sxs-lookup"><span data-stu-id="b2490-113">Raw AAC.</span></span>             | <span data-ttu-id="b2490-114">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="b2490-114">wmcodecdsp.h</span></span> |



 

<dl> <dt>

<span data-ttu-id="b2490-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>\_AAC MFAudioFormat</span><span class="sxs-lookup"><span data-stu-id="b2490-115"><span id="MFAudioFormat_AAC"></span><span id="mfaudioformat_aac"></span><span id="MFAUDIOFORMAT_AAC"></span>MFAudioFormat\_AAC</span></span>
</dt> <dd>

<span data-ttu-id="b2490-116">Para esse subtipo, o tipo de mídia fornece a taxa de amostra e o número de canais antes da aplicação de ferramentas de Spectral Band Replication (SBR) e de estéreo paramétrica (PS), se presente.</span><span class="sxs-lookup"><span data-stu-id="b2490-116">For this subtype, the media type gives the sample rate and number of channels prior to the application of spectral band replication (SBR) and parametric stereo (PS) tools, if present.</span></span> <span data-ttu-id="b2490-117">O efeito da ferramenta SBR é dobrar a taxa de amostragem decodificada em relação à taxa de amostra AAC-LC principal.</span><span class="sxs-lookup"><span data-stu-id="b2490-117">The effect of the SBR tool is to double the decoded sample rate relative to the core AAC-LC sample rate.</span></span> <span data-ttu-id="b2490-118">O efeito da ferramenta PS é decodificar o estéreo de um fluxo básico AAC-LC do canal mono.</span><span class="sxs-lookup"><span data-stu-id="b2490-118">The effect of the PS tool is to decode stereo from a mono-channel core AAC-LC stream.</span></span>

<span data-ttu-id="b2490-119">Esse subtipo é equivalente a **MEDIASUBTYPE \_ MPEG \_ HEAAC**, definido em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="b2490-119">This subtype is equivalent to **MEDIASUBTYPE\_MPEG\_HEAAC**, defined in wmcodecdsp.h.</span></span> <span data-ttu-id="b2490-120">Consulte [GUIDs de subtipo de áudio](audio-subtype-guids.md).</span><span class="sxs-lookup"><span data-stu-id="b2490-120">See [Audio Subtype GUIDs](audio-subtype-guids.md).</span></span>

</dd> <dt>

<span data-ttu-id="b2490-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>\_AAC1 bruto \_ MEDIASUBTYPE</span><span class="sxs-lookup"><span data-stu-id="b2490-121"><span id="MEDIASUBTYPE_RAW_AAC1"></span><span id="mediasubtype_raw_aac1"></span>MEDIASUBTYPE\_RAW\_AAC1</span></span>
</dt> <dd>

<span data-ttu-id="b2490-122">Esse subtipo é usado para AAC contido em um arquivo AVI com a marca de formato de áudio igual ao \_ formato Wave \_ \_ AAC1 RAW (0x00FF).</span><span class="sxs-lookup"><span data-stu-id="b2490-122">This subtype is used for AAC contained in an AVI file with the audio format tag equal to WAVE\_FORMAT\_RAW\_AAC1 (0x00FF).</span></span>

<span data-ttu-id="b2490-123">Para esse subtipo, o tipo de mídia fornece a taxa de amostra e o número de canais depois que as ferramentas SBR e PS são aplicadas, se presentes.</span><span class="sxs-lookup"><span data-stu-id="b2490-123">For this subtype, the media type gives the sample rate and number of channels after the SBR and PS tools are applied, if present.</span></span>

</dd> </dl>

<span data-ttu-id="b2490-124">Os seguintes atributos de tipo de mídia se aplicam ao áudio AAC.</span><span class="sxs-lookup"><span data-stu-id="b2490-124">The following media type attributes apply to AAC audio.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b2490-125">Atributo</span><span class="sxs-lookup"><span data-stu-id="b2490-125">Attribute</span></span></th>
<th><span data-ttu-id="b2490-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="b2490-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b2490-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b2490-127"><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></span></span></td>
<td><span data-ttu-id="b2490-128">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="b2490-128">Major type.</span></span> <span data-ttu-id="b2490-129">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2490-129">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2490-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b2490-130"><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></span></span></td>
<td><span data-ttu-id="b2490-131">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="b2490-131">Audio subtype.</span></span> <span data-ttu-id="b2490-132">Consulte a descrição anterior para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="b2490-132">Refer to the previous description for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2490-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span><span class="sxs-lookup"><span data-stu-id="b2490-133"><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></span></span></td>
<td><span data-ttu-id="b2490-134">Perfil de áudio e nível.</span><span class="sxs-lookup"><span data-stu-id="b2490-134">Audio profile and level.</span></span> <br/> <span data-ttu-id="b2490-135">O valor desse atributo é o campo <strong>audioProfileLevelIndication</strong> , conforme definido por ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="b2490-135">The value of this attribute is the <strong>audioProfileLevelIndication</strong> field, as defined by ISO/IEC 14496-3.</span></span><br/> <span data-ttu-id="b2490-136">Se for desconhecido, defina como zero ou 0xFE ( &quot; nenhum perfil de áudio especificado &quot; ).</span><span class="sxs-lookup"><span data-stu-id="b2490-136">If unknown, set to zero or 0xFE (&quot;no audio profile specified&quot;).</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2490-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="b2490-137"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="b2490-138">Taxa de bits do fluxo AAC codificado, em bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="b2490-138">Bit rate of the encoded AAC stream, in bytes per second.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2490-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="b2490-139"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></span></span></td>
<td><span data-ttu-id="b2490-140">Tipo de carga.</span><span class="sxs-lookup"><span data-stu-id="b2490-140">Payload type.</span></span><br/> <span data-ttu-id="b2490-141">Aplica-se somente a <strong>MFAudioFormat_AAC</strong>.</span><span class="sxs-lookup"><span data-stu-id="b2490-141">Applies only to <strong>MFAudioFormat_AAC</strong>.</span></span><br/> <span data-ttu-id="b2490-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> é opcional.</span><span class="sxs-lookup"><span data-stu-id="b2490-142"><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> is optional.</span></span> <span data-ttu-id="b2490-143">Se esse atributo não for especificado, o valor padrão 0 será usado, o que especificará que o fluxo contém apenas elementos de raw_data_block.</span><span class="sxs-lookup"><span data-stu-id="b2490-143">If this attribute is not specified, the default value 0 is used, which specifies the stream contains raw_data_block elements only.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2490-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span><span class="sxs-lookup"><span data-stu-id="b2490-144"><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></span></span></td>
<td><span data-ttu-id="b2490-145">Profundidade de bits do áudio PCM decodificado.</span><span class="sxs-lookup"><span data-stu-id="b2490-145">Bit depth of the decoded PCM audio.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2490-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span><span class="sxs-lookup"><span data-stu-id="b2490-146"><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></span></span></td>
<td><span data-ttu-id="b2490-147">Atribuição de canais de áudio a posições do orador.</span><span class="sxs-lookup"><span data-stu-id="b2490-147">Assignment of audio channels to speaker positions.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2490-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span><span class="sxs-lookup"><span data-stu-id="b2490-148"><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></span></span></td>
<td><span data-ttu-id="b2490-149">Número de canais, incluindo o canal de baixa frequência (LFE), se presente.</span><span class="sxs-lookup"><span data-stu-id="b2490-149">Number of channels, including the low frequency (LFE) channel, if present.</span></span><br/> <span data-ttu-id="b2490-150">A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b2490-150">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b2490-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span><span class="sxs-lookup"><span data-stu-id="b2490-151"><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></span></span></td>
<td><span data-ttu-id="b2490-152">Taxa de amostragem, em amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="b2490-152">Sample rate, in samples per second.</span></span><br/> <span data-ttu-id="b2490-153">A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.</span><span class="sxs-lookup"><span data-stu-id="b2490-153">The interpretation of this value depends on the media subtype, as described previously.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b2490-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span><span class="sxs-lookup"><span data-stu-id="b2490-154"><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></span></span></td>
<td><span data-ttu-id="b2490-155">O valor desse atributo depende do subtipo:</span><span class="sxs-lookup"><span data-stu-id="b2490-155">The value of this attribute depends on the subtype:</span></span><br/>
<ul>
<li><span data-ttu-id="b2490-156"><strong>MFAudioFormat_AAC</strong>: contém a parte da estrutura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece após a estrutura <strong>WAVEFORMATEX</strong> (ou seja, após o membro <strong>WFX</strong> ).</span><span class="sxs-lookup"><span data-stu-id="b2490-156"><strong>MFAudioFormat_AAC</strong>: Contains the portion of the <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> structure that appears after the <strong>WAVEFORMATEX</strong> structure (that is, after the <strong>wfx</strong> member).</span></span> <span data-ttu-id="b2490-157">Isso é seguido pelos dados de AudioSpecificConfig (), conforme definido por ISO/IEC 14496-3.</span><span class="sxs-lookup"><span data-stu-id="b2490-157">This is followed by the AudioSpecificConfig() data, as defined by ISO/IEC 14496-3.</span></span></li>
<li><span data-ttu-id="b2490-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contém os dados de AudioSpecificConfig ().</span><span class="sxs-lookup"><span data-stu-id="b2490-158"><strong>MEDIASUBTYPE_RAW_AAC1</strong>: Contains the AudioSpecificConfig() data.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>



 

## <a name="related-topics"></a><span data-ttu-id="b2490-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b2490-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b2490-160">Tipos de mídia de áudio</span><span class="sxs-lookup"><span data-stu-id="b2490-160">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="b2490-161">Atributos de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="b2490-161">Media Type Attributes</span></span>](media-type-attributes.md)
</dt> <dt>

[<span data-ttu-id="b2490-162">Suporte a MPEG-4 no Media Foundation</span><span class="sxs-lookup"><span data-stu-id="b2490-162">MPEG-4 Support in Media Foundation</span></span>](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[<span data-ttu-id="b2490-163">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="b2490-163">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> </dl>

 

