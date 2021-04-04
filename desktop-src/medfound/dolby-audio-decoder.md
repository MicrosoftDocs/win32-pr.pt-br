---
description: O decodificador Dolby Audio é um MFT que decodifica Dolby Digital (AC-3) e Dolby Digital Plus.
ms.assetid: A968914A-E4C5-4472-8776-C73F5910089A
title: Decodificador de áudio Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2e4f1d8ca21cb3ab86f1fdbeddf03624aaaffb0b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103646590"
---
# <a name="dolby-audio-decoder"></a><span data-ttu-id="61073-103">Decodificador de áudio Dolby</span><span class="sxs-lookup"><span data-stu-id="61073-103">Dolby Audio Decoder</span></span>

<span data-ttu-id="61073-104">O decodificador Dolby Audio é uma [Media Foundation transformação](media-foundation-transforms.md) (MFT) que decodifica os seguintes tipos de fluxo:</span><span class="sxs-lookup"><span data-stu-id="61073-104">The Dolby audio decoder is a [Media Foundation transform](media-foundation-transforms.md) (MFT) that decodes the following stream types:</span></span>

-   <span data-ttu-id="61073-105">Dolby Digital, também chamado Dolby AC-3</span><span class="sxs-lookup"><span data-stu-id="61073-105">Dolby Digital, also called Dolby AC-3</span></span>
-   <span data-ttu-id="61073-106">Dolby Digital Plus, também chamado de AC reforçada 3 (E-AC-3)</span><span class="sxs-lookup"><span data-stu-id="61073-106">Dolby Digital Plus, also called Enhanced AC-3 (E-AC-3)</span></span>

> [!IMPORTANT]
> <span data-ttu-id="61073-107">Para versões do Windows anteriores ao Windows 8, a implementação da Microsoft da tecnologia Dolby Digital é restrita em termos do programa Dolby Digital Licensing para uso pelos aplicativos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="61073-107">For versions of Windows prior to Windows 8, the Microsoft implementation of the Dolby Digital technology is restricted under terms of the Dolby Digital licensing program to use by Microsoft applications.</span></span>

 

<span data-ttu-id="61073-108">Para obter mais informações sobre esses formatos, consulte a documentação do ATSC (Comitê de sistemas de televisão avançada) *padrão de compactação de áudio digital (AC-3, E-AC-3) revisão B*.</span><span class="sxs-lookup"><span data-stu-id="61073-108">For more information about these formats, refer to Advanced Television Systems Committee (ATSC) document *Digital Audio Compression Standard (AC-3, E-AC-3) Revision B*.</span></span>

<span data-ttu-id="61073-109">O decodificador também pode converter um fluxo Dolby Digital Plus para o formato Dolby Digital para saída AC-3 S/PIDF ou formatar um fluxo Dolby Digital Plus para saída digital HDMI.</span><span class="sxs-lookup"><span data-stu-id="61073-109">The decoder can also convert a Dolby Digital Plus stream to Dolby Digital format for AC-3 S/PIDF output, or format a Dolby Digital Plus stream for HDMI digital output.</span></span>

## <a name="class-identifier"></a><span data-ttu-id="61073-110">Identificador de classe</span><span class="sxs-lookup"><span data-stu-id="61073-110">Class Identifier</span></span>

<span data-ttu-id="61073-111">O CLSID (identificador de classe) do decodificador de áudio Dolby é **CLSID \_ CMSDDPlusDecMFT**, definido no arquivo de cabeçalho wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="61073-111">The class identifier (CLSID) of the Dolby audio decoder is **CLSID\_CMSDDPlusDecMFT**, defined in the header file wmcodecdsp.h.</span></span>

## <a name="input-types"></a><span data-ttu-id="61073-112">Tipos de entrada</span><span class="sxs-lookup"><span data-stu-id="61073-112">Input Types</span></span>

<span data-ttu-id="61073-113">O decodificador de áudio Dolby dá suporte aos seguintes subtipos de entrada.</span><span class="sxs-lookup"><span data-stu-id="61073-113">The Dolby audio decoder supports the following input subtypes.</span></span>



| <span data-ttu-id="61073-114">Subtype</span><span class="sxs-lookup"><span data-stu-id="61073-114">Subtype</span></span>                                 | <span data-ttu-id="61073-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="61073-115">Description</span></span>                                                                                                                                                 | <span data-ttu-id="61073-116">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61073-116">Header</span></span>       |
|-----------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| <span data-ttu-id="61073-117">**MEDIASUBTYPE \_ Dolby \_ AC3**</span><span class="sxs-lookup"><span data-stu-id="61073-117">**MEDIASUBTYPE\_DOLBY\_AC3**</span></span>            | <span data-ttu-id="61073-118">Áudio Dolby Digital.</span><span class="sxs-lookup"><span data-stu-id="61073-118">Dolby Digital audio.</span></span>                                                                                                                                        | <span data-ttu-id="61073-119">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="61073-119">mfapi.h</span></span>      |
| <span data-ttu-id="61073-120">**MEDIASUBTYPE \_ DVM**</span><span class="sxs-lookup"><span data-stu-id="61073-120">**MEDIASUBTYPE\_DVM**</span></span>                   | <span data-ttu-id="61073-121">Áudio Dolby Digital; consulte [**subtipos de áudio**](../directshow/audio-subtypes.md).</span><span class="sxs-lookup"><span data-stu-id="61073-121">Dolby Digital audio; see [**Audio Subtypes**](../directshow/audio-subtypes.md).</span></span> <span data-ttu-id="61073-122">Esse subtipo pode ser usado de forma intercambiável com **MEDIASUBTYPE \_ Dolby \_ AC3**.</span><span class="sxs-lookup"><span data-stu-id="61073-122">This subtype can be used interchangeably with **MEDIASUBTYPE\_DOLBY\_AC3**.</span></span><br/> | <span data-ttu-id="61073-123">wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="61073-123">wmcodecdsp.h</span></span> |
| <span data-ttu-id="61073-124">**MFAudioFormat \_ Dolby \_ digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="61073-124">**MFAudioFormat\_Dolby\_Digital\_Plus**</span></span> | <span data-ttu-id="61073-125">Áudio Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="61073-125">Dolby Digital Plus audio.</span></span>                                                                                                                                   | <span data-ttu-id="61073-126">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="61073-126">mfapi.h</span></span>      |



 

<span data-ttu-id="61073-127">A tabela a seguir lista os atributos requires e optional para o tipo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="61073-127">The following table lists the requires and optional attributes for the input media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61073-128">Atributo</span><span class="sxs-lookup"><span data-stu-id="61073-128">Attribute</span></span></th>
<th><span data-ttu-id="61073-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="61073-129">Description</span></span></th>
<th><span data-ttu-id="61073-130">Comentários</span><span class="sxs-lookup"><span data-stu-id="61073-130">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61073-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="61073-131"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="61073-132">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="61073-132">Major type.</span></span></td>
<td><span data-ttu-id="61073-133">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="61073-133">Required.</span></span> <span data-ttu-id="61073-134">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="61073-134">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="61073-135"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="61073-136">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="61073-136">Audio subtype.</span></span></td>
<td><span data-ttu-id="61073-137">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="61073-137">Required.</span></span> <span data-ttu-id="61073-138">Consulte a tabela anterior para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="61073-138">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="61073-139"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="61073-140">Taxa de amostragem, em amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="61073-140">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="61073-141">Opcional.</span><span class="sxs-lookup"><span data-stu-id="61073-141">Optional.</span></span> <span data-ttu-id="61073-142">Os valores válidos são: 48000, 44100, 32000, 24000, 22050 e 16000.</span><span class="sxs-lookup"><span data-stu-id="61073-142">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="61073-143">Se esse atributo não for definido, o valor padrão será 48000.</span><span class="sxs-lookup"><span data-stu-id="61073-143">If this attribute is not set, the default value is 48000.</span></span> <br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="61073-144">Os fluxos Dolby AC-3 são limitados às três taxas mais altas nessa lista.</span><span class="sxs-lookup"><span data-stu-id="61073-144">Dolby AC-3 streams are limited to the three highest rates in this list.</span></span>
</blockquote>
<br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="61073-145"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="61073-146">Número de canais, incluindo o canal de baixa frequência (LFE), se presente.</span><span class="sxs-lookup"><span data-stu-id="61073-146">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="61073-147">Opcional.</span><span class="sxs-lookup"><span data-stu-id="61073-147">Optional.</span></span> <span data-ttu-id="61073-148">Os valores válidos estão no intervalo 1 (mono) a 8 (configuração de canal de 7,1).</span><span class="sxs-lookup"><span data-stu-id="61073-148">Valid values are in the range 1 (mono) to 8 (7.1 channel configuration).</span></span> <span data-ttu-id="61073-149">Se esse atributo não estiver definido, o valor padrão será 2 (estéreo).</span><span class="sxs-lookup"><span data-stu-id="61073-149">If this attribute is not set, the default value is 2 (stereo).</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="61073-150"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="61073-151">Especifica a atribuição de canais de áudio a posições do orador.</span><span class="sxs-lookup"><span data-stu-id="61073-151">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="61073-152">Opcional.</span><span class="sxs-lookup"><span data-stu-id="61073-152">Optional.</span></span> <span data-ttu-id="61073-153">Se especificado, o valor deve ser consistente com o número de canais de áudio.</span><span class="sxs-lookup"><span data-stu-id="61073-153">If specified, the value must be consistent with the number of audio channels.</span></span> <span data-ttu-id="61073-154">Se o atributo não estiver definido, o decodificador usará uma máscara de canal padrão, com base no número de canais.</span><span class="sxs-lookup"><span data-stu-id="61073-154">If the attribute is not set, the decoder uses a default channel mask, based on the number of channels.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="61073-155">A tabela a seguir lista as configurações de canal Dolby com suporte.</span><span class="sxs-lookup"><span data-stu-id="61073-155">The following table lists the supported Dolby channel configurations.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61073-156">Configuração de canal</span><span class="sxs-lookup"><span data-stu-id="61073-156">Channel configuration</span></span></th>
<th><span data-ttu-id="61073-157">Número de canais</span><span class="sxs-lookup"><span data-stu-id="61073-157">Number of channels</span></span></th>
<th><span data-ttu-id="61073-158">Máscaras de canal</span><span class="sxs-lookup"><span data-stu-id="61073-158">Channel masks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61073-159">1/0 (mono)</span><span class="sxs-lookup"><span data-stu-id="61073-159">1/0 (mono)</span></span></td>
<td><span data-ttu-id="61073-160">1</span><span class="sxs-lookup"><span data-stu-id="61073-160">1</span></span></td>
<td><span data-ttu-id="61073-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-161">0x4 (<strong>SPEAKER_FRONT_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-162">2/0 (estéreo) ou 1 + 1 (mono duplo)</span><span class="sxs-lookup"><span data-stu-id="61073-162">2/0 (stereo) or 1+1 (dual mono)</span></span></td>
<td><span data-ttu-id="61073-163">2</span><span class="sxs-lookup"><span data-stu-id="61073-163">2</span></span></td>
<td><span data-ttu-id="61073-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-164">0x3 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-165">3/0</span><span class="sxs-lookup"><span data-stu-id="61073-165">3/0</span></span></td>
<td><span data-ttu-id="61073-166">3</span><span class="sxs-lookup"><span data-stu-id="61073-166">3</span></span></td>
<td><span data-ttu-id="61073-167">0x7 (<strong></strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong> de SPEAKER_FRONT_LEFT | SPEAKER_FRONT_CENTER)</span><span class="sxs-lookup"><span data-stu-id="61073-167">0x7 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | SPEAKER_FRONT_CENTER)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-168">2/1</span><span class="sxs-lookup"><span data-stu-id="61073-168">2/1</span></span></td>
<td><span data-ttu-id="61073-169">3</span><span class="sxs-lookup"><span data-stu-id="61073-169">3</span></span></td>
<td><span data-ttu-id="61073-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-170">0x103 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-171">3/1</span><span class="sxs-lookup"><span data-stu-id="61073-171">3/1</span></span></td>
<td><span data-ttu-id="61073-172">4</span><span class="sxs-lookup"><span data-stu-id="61073-172">4</span></span></td>
<td><span data-ttu-id="61073-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_CENTER</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-173">0x107 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_CENTER</strong>)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-174">2/2</span><span class="sxs-lookup"><span data-stu-id="61073-174">2/2</span></span></td>
<td><span data-ttu-id="61073-175">4</span><span class="sxs-lookup"><span data-stu-id="61073-175">4</span></span></td>
<td><span data-ttu-id="61073-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-176">0x33 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="61073-177">ou</span><span class="sxs-lookup"><span data-stu-id="61073-177">or</span></span><br/> <span data-ttu-id="61073-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-178">0x603 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-179">3/2</span><span class="sxs-lookup"><span data-stu-id="61073-179">3/2</span></span></td>
<td><span data-ttu-id="61073-180">5</span><span class="sxs-lookup"><span data-stu-id="61073-180">5</span></span></td>
<td><span data-ttu-id="61073-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-181">0x37 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="61073-182">ou</span><span class="sxs-lookup"><span data-stu-id="61073-182">or</span></span><br/> <span data-ttu-id="61073-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-183">0x607 (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-184">3/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="61073-184">3/2 + LFE</span></span></td>
<td><span data-ttu-id="61073-185">6</span><span class="sxs-lookup"><span data-stu-id="61073-185">6</span></span></td>
<td><span data-ttu-id="61073-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-186">0x3F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong>)</span></span><br/> <span data-ttu-id="61073-187">ou</span><span class="sxs-lookup"><span data-stu-id="61073-187">or</span></span><br/> <span data-ttu-id="61073-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_SIDE_LEFT</strong>  |  <strong>SPEAKER_SIDE_RIGHT</strong>)</span><span class="sxs-lookup"><span data-stu-id="61073-188">0x60F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_SIDE_LEFT</strong> | <strong>SPEAKER_SIDE_RIGHT</strong>)</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-189">3/2/2 + LFE</span><span class="sxs-lookup"><span data-stu-id="61073-189">3/2/2 + LFE</span></span>
<blockquote>
[!Note]<br />
<span data-ttu-id="61073-190">Somente Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="61073-190">Dolby Digital Plus only.</span></span>
</blockquote>
<br/> <br/></td>
<td><span data-ttu-id="61073-191">8</span><span class="sxs-lookup"><span data-stu-id="61073-191">8</span></span></td>
<td><span data-ttu-id="61073-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong>  |  <strong>SPEAKER_FRONT_RIGHT</strong>  |  <strong>SPEAKER_FRONT_CENTER</strong>  |  <strong>SPEAKER_LOW_FREQUENCY</strong>  |  <strong>SPEAKER_BACK_LEFT</strong>  |  <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span><span class="sxs-lookup"><span data-stu-id="61073-192">0x63F (<strong>SPEAKER_FRONT_LEFT</strong> | <strong>SPEAKER_FRONT_RIGHT</strong> | <strong>SPEAKER_FRONT_CENTER</strong> | <strong>SPEAKER_LOW_FREQUENCY</strong> | <strong>SPEAKER_BACK_LEFT</strong> | <strong>SPEAKER_BACK_RIGHT</strong> | SPEAKER_SIDE_LEFT | SPEAKER_SIDE_RIGHT)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="61073-193">Além disso, as configurações de canal 1/0, 2/0, 3/0, 2/1, 3/1 e 2/2 também podem aparecer com um canal de LFE.</span><span class="sxs-lookup"><span data-stu-id="61073-193">In addition, channel configurations 1/0, 2/0, 3/0, 2/1, 3/1, and 2/2 may also appear with an LFE channel.</span></span>

## <a name="output-types"></a><span data-ttu-id="61073-194">Tipos de saída</span><span class="sxs-lookup"><span data-stu-id="61073-194">Output Types</span></span>

<span data-ttu-id="61073-195">O decodificador de áudio Dolby dá suporte aos seguintes subtipos de saída.</span><span class="sxs-lookup"><span data-stu-id="61073-195">The Dolby audio decoder supports the following output subtypes.</span></span>



| <span data-ttu-id="61073-196">Subtype</span><span class="sxs-lookup"><span data-stu-id="61073-196">Subtype</span></span>                                                   | <span data-ttu-id="61073-197">Descrição</span><span class="sxs-lookup"><span data-stu-id="61073-197">Description</span></span>                                                                                                                               | <span data-ttu-id="61073-198">Cabeçalho</span><span class="sxs-lookup"><span data-stu-id="61073-198">Header</span></span>    |
|-----------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|-----------|
| <span data-ttu-id="61073-199">**MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**</span><span class="sxs-lookup"><span data-stu-id="61073-199">**MFAudioFormat\_Dolby\_AC3\_SPDIF**</span></span>                      | <span data-ttu-id="61073-200">Áudio Dolby AC-3 formatado para saída digital S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="61073-200">Dolby AC-3 audio formatted for S/PDIF digital output.</span></span>                                                                                     | <span data-ttu-id="61073-201">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="61073-201">mfapi.h</span></span>   |
| <span data-ttu-id="61073-202">**KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital \_ Plus**</span><span class="sxs-lookup"><span data-stu-id="61073-202">**KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**</span></span> | <span data-ttu-id="61073-203">Áudio Dolby Digital Plus formatado para saída digital HDMI.</span><span class="sxs-lookup"><span data-stu-id="61073-203">Dolby Digital Plus audio formatted for HDMI digital output.</span></span>                                                                               | <span data-ttu-id="61073-204">ksmedia. h</span><span class="sxs-lookup"><span data-stu-id="61073-204">ksmedia.h</span></span> |
| <span data-ttu-id="61073-205">**MFAudioFormat \_ float**</span><span class="sxs-lookup"><span data-stu-id="61073-205">**MFAudioFormat\_Float**</span></span>                                  | <span data-ttu-id="61073-206">Áudio PCM de ponto flutuante do IEEE 32-bit</span><span class="sxs-lookup"><span data-stu-id="61073-206">IEEE 32-bit floating-point PCM audio</span></span><br/> <span data-ttu-id="61073-207">**Windows 10**: estéreo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="61073-207">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="61073-208">**Versões anteriores**: estéreo, 5,1</span><span class="sxs-lookup"><span data-stu-id="61073-208">**Previous versions**: stereo, 5.1</span></span><br/> | <span data-ttu-id="61073-209">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="61073-209">mfapi.h</span></span>   |
| <span data-ttu-id="61073-210">**\_PCM MFAudioFormat**</span><span class="sxs-lookup"><span data-stu-id="61073-210">**MFAudioFormat\_PCM**</span></span>                                    | <span data-ttu-id="61073-211">áudio PCM de 16 bits</span><span class="sxs-lookup"><span data-stu-id="61073-211">16-bit PCM audio</span></span><br/> <span data-ttu-id="61073-212">**Windows 10**: estéreo, 5,1, 7,1</span><span class="sxs-lookup"><span data-stu-id="61073-212">**Windows 10**: stereo, 5.1, 7.1</span></span><br/> <span data-ttu-id="61073-213">**Versões anteriores**: estéreo, 5,1</span><span class="sxs-lookup"><span data-stu-id="61073-213">**Previous versions**: stereo, 5.1</span></span><br/>                     | <span data-ttu-id="61073-214">mfapi. h</span><span class="sxs-lookup"><span data-stu-id="61073-214">mfapi.h</span></span>   |



 

<span data-ttu-id="61073-215">A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de saída.</span><span class="sxs-lookup"><span data-stu-id="61073-215">The following table lists the required and optional attributes for the output media type.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61073-216">Atributo</span><span class="sxs-lookup"><span data-stu-id="61073-216">Attribute</span></span></th>
<th><span data-ttu-id="61073-217">Descrição</span><span class="sxs-lookup"><span data-stu-id="61073-217">Description</span></span></th>
<th><span data-ttu-id="61073-218">Comentários</span><span class="sxs-lookup"><span data-stu-id="61073-218">Remarks</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="61073-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span><span class="sxs-lookup"><span data-stu-id="61073-219"><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></span></span></td>
<td><span data-ttu-id="61073-220">Tipo principal.</span><span class="sxs-lookup"><span data-stu-id="61073-220">Major type.</span></span></td>
<td><span data-ttu-id="61073-221">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="61073-221">Required.</span></span> <span data-ttu-id="61073-222">Deve ser <strong>MFMediaType_Audio</strong>.</span><span class="sxs-lookup"><span data-stu-id="61073-222">Must be <strong>MFMediaType_Audio</strong>.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span><span class="sxs-lookup"><span data-stu-id="61073-223"><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></span></span></td>
<td><span data-ttu-id="61073-224">Subtipo de áudio.</span><span class="sxs-lookup"><span data-stu-id="61073-224">Audio subtype.</span></span></td>
<td><span data-ttu-id="61073-225">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="61073-225">Required.</span></span> <span data-ttu-id="61073-226">Consulte a tabela anterior para obter detalhes.</span><span class="sxs-lookup"><span data-stu-id="61073-226">See the previous table for details.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="61073-227"><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="61073-228">Taxa de amostragem, em amostras por segundo.</span><span class="sxs-lookup"><span data-stu-id="61073-228">Sample rate, in samples per second.</span></span></td>
<td><span data-ttu-id="61073-229">Obrigatórios.</span><span class="sxs-lookup"><span data-stu-id="61073-229">Required.</span></span> <span data-ttu-id="61073-230">Os valores válidos são: 48000, 44100, 32000, 24000, 22050 e 16000.</span><span class="sxs-lookup"><span data-stu-id="61073-230">Valid values are: 48000, 44100, 32000, 24000, 22050, and 16000.</span></span> <span data-ttu-id="61073-231">A taxa de amostra de saída deve ser idêntica à taxa de amostra de entrada.</span><span class="sxs-lookup"><span data-stu-id="61073-231">The output sample rate must be identical to the input sample rate.</span></span> <span data-ttu-id="61073-232">O decodificador não pode alterar a taxa de amostragem do fluxo.</span><span class="sxs-lookup"><span data-stu-id="61073-232">The decoder cannot change the sampling rate of the stream.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span><span class="sxs-lookup"><span data-stu-id="61073-233"><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></span></span></td>
<td><span data-ttu-id="61073-234">Número de canais, incluindo o canal de baixa frequência (LFE), se presente.</span><span class="sxs-lookup"><span data-stu-id="61073-234">Number of channels, including the low frequency (LFE) channel, if present.</span></span></td>
<td><span data-ttu-id="61073-235">Necessário para a saída do PCM.</span><span class="sxs-lookup"><span data-stu-id="61073-235">Required for PCM output.</span></span> <br/> <span data-ttu-id="61073-236">Não é necessário para a saída digital.</span><span class="sxs-lookup"><span data-stu-id="61073-236">Not needed for digital output.</span></span> <br/> <span data-ttu-id="61073-237">Se o tipo de entrada for mono, estéreo ou dual-mono (tudo sem canal de LFE), o único valor válido será 2, para saída de estéreo.</span><span class="sxs-lookup"><span data-stu-id="61073-237">If the input type is mono, stereo, or dual-mono (all without LFE channel), the only valid value is 2, for stereo output.</span></span> <span data-ttu-id="61073-238">Caso contrário, o valor pode ser:</span><span class="sxs-lookup"><span data-stu-id="61073-238">Otherwise, the value can be:</span></span> <br/>
<ul>
<li><span data-ttu-id="61073-239">2 para downmix estéreo</span><span class="sxs-lookup"><span data-stu-id="61073-239">2 for stereo downmix</span></span></li>
<li><span data-ttu-id="61073-240">6 para configurações de canal de 5,1</span><span class="sxs-lookup"><span data-stu-id="61073-240">6 for 5.1 channel configurations</span></span></li>
<li><span data-ttu-id="61073-241">8 para configurações de canal de 7,1</span><span class="sxs-lookup"><span data-stu-id="61073-241">8 for 7.1 channel configurations</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span><span class="sxs-lookup"><span data-stu-id="61073-242"><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></span></span></td>
<td><span data-ttu-id="61073-243">Especifica a atribuição de canais de áudio a posições do orador.</span><span class="sxs-lookup"><span data-stu-id="61073-243">Specifies the assignment of audio channels to speaker positions.</span></span></td>
<td><span data-ttu-id="61073-244">Necessário para a saída do PCM se o número de canais for maior que 2.</span><span class="sxs-lookup"><span data-stu-id="61073-244">Required for PCM output if the number of channels is greater than 2.</span></span> <span data-ttu-id="61073-245">O valor deve ser:</span><span class="sxs-lookup"><span data-stu-id="61073-245">The value must be:</span></span><br/>
<ul>
<li><span data-ttu-id="61073-246">0x3 para saída de estéreo</span><span class="sxs-lookup"><span data-stu-id="61073-246">0x3 for stereo output</span></span></li>
<li><span data-ttu-id="61073-247">0x3F para saída de canal de 5,1</span><span class="sxs-lookup"><span data-stu-id="61073-247">0x3F for 5.1 channel output</span></span></li>
<li><span data-ttu-id="61073-248">0x63F para saída de canal de 7,1</span><span class="sxs-lookup"><span data-stu-id="61073-248">0x63F for 7.1 channel output</span></span></li>
</ul>
<span data-ttu-id="61073-249">Não é necessário para a saída digital.</span><span class="sxs-lookup"><span data-stu-id="61073-249">Not needed for digital output.</span></span> <br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="61073-250"><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="61073-251">Número de bits por amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="61073-251">Number of bits per audio sample.</span></span></td>
<td><span data-ttu-id="61073-252">Necessário para a saída do PCM.</span><span class="sxs-lookup"><span data-stu-id="61073-252">Required for PCM output.</span></span> <span data-ttu-id="61073-253">O valor deve ser 32 para <strong>MFAudioFormat_Float</strong>e 16 para <strong>MFAudioFormat_PCM</strong>.</span><span class="sxs-lookup"><span data-stu-id="61073-253">The value must be 32 for <strong>MFAudioFormat_Float</strong>, and 16 for <strong>MFAudioFormat_PCM</strong>.</span></span><br/> <span data-ttu-id="61073-254">Não é necessário para a saída digital.</span><span class="sxs-lookup"><span data-stu-id="61073-254">Not needed for digital output.</span></span><br/></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span><span class="sxs-lookup"><span data-stu-id="61073-255"><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></span></span></td>
<td><span data-ttu-id="61073-256">Número de bits válidos de dados de áudio em cada amostra de áudio.</span><span class="sxs-lookup"><span data-stu-id="61073-256">Number of valid bits of audio data in each audio sample.</span></span></td>
<td><span data-ttu-id="61073-257">Opcional para saída de PCM.</span><span class="sxs-lookup"><span data-stu-id="61073-257">Optional for PCM output.</span></span> <span data-ttu-id="61073-258">Se definido, o valor deve ser idêntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span><span class="sxs-lookup"><span data-stu-id="61073-258">If set, the value must be identical to <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</span></span><br/> <span data-ttu-id="61073-259">Não é necessário para os subtipos de saída digital.</span><span class="sxs-lookup"><span data-stu-id="61073-259">Not needed for the digital output subtypes.</span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="61073-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span><span class="sxs-lookup"><span data-stu-id="61073-260"><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></span></span></td>
<td><span data-ttu-id="61073-261">Alinhamento de bloco, em bytes.</span><span class="sxs-lookup"><span data-stu-id="61073-261">Block alignment, in bytes.</span></span></td>
<td><span data-ttu-id="61073-262">Opcional para saída de PCM.</span><span class="sxs-lookup"><span data-stu-id="61073-262">Optional for PCM output.</span></span> <span data-ttu-id="61073-263">Não é necessário para a saída digital.</span><span class="sxs-lookup"><span data-stu-id="61073-263">Not needed for digital output.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="61073-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span><span class="sxs-lookup"><span data-stu-id="61073-264"><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></span></span></td>
<td><span data-ttu-id="61073-265">Número médio de bytes por segundo.</span><span class="sxs-lookup"><span data-stu-id="61073-265">Average number of bytes per second.</span></span></td>
<td><span data-ttu-id="61073-266">Opcional para saída de PCM.</span><span class="sxs-lookup"><span data-stu-id="61073-266">Optional for PCM output.</span></span> <span data-ttu-id="61073-267">Não é necessário para a saída digital.</span><span class="sxs-lookup"><span data-stu-id="61073-267">Not needed for digital output.</span></span></td>
</tr>
</tbody>
</table>



 

## <a name="transform-attributes"></a><span data-ttu-id="61073-268">Atributos de transformação</span><span class="sxs-lookup"><span data-stu-id="61073-268">Transform Attributes</span></span>

<span data-ttu-id="61073-269">O decodificador de áudio Dolby implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) .</span><span class="sxs-lookup"><span data-stu-id="61073-269">The Dolby audio decoder implements the [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) method.</span></span> <span data-ttu-id="61073-270">O aplicativo pode usar esse método para obter ou definir os atributos a seguir.</span><span class="sxs-lookup"><span data-stu-id="61073-270">The application can use this method to get or set the following attributes.</span></span>



| <span data-ttu-id="61073-271">Atributo</span><span class="sxs-lookup"><span data-stu-id="61073-271">Attribute</span></span>                                                                                | <span data-ttu-id="61073-272">Descrição</span><span class="sxs-lookup"><span data-stu-id="61073-272">Description</span></span>                                                                                                                                                                                                                                                                              |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61073-273">CODECAPI \_ AVDecAudioDualMono</span><span class="sxs-lookup"><span data-stu-id="61073-273">CODECAPI\_AVDecAudioDualMono</span></span>](../directshow/avdecaudiodualmono-property.md)                        | <span data-ttu-id="61073-274">Especifica se um fluxo de áudio Dolby de 2 canais é codificado como estéreo ou dual-mono.</span><span class="sxs-lookup"><span data-stu-id="61073-274">Specifies whether a 2-channel Dolby audio stream is encoded as stereo or dual-mono.</span></span> <span data-ttu-id="61073-275">Antes de o primeiro quadro Dolby ser decodificado, o valor é **EAVDecAudioDualMono \_ não especificado**.</span><span class="sxs-lookup"><span data-stu-id="61073-275">Before the first Dolby frame is decoded, the value is **eAVDecAudioDualMono\_UnSpecified**.</span></span> <span data-ttu-id="61073-276">Após o início da decodificação, o valor reflete o quadro Dolby mais recente.</span><span class="sxs-lookup"><span data-stu-id="61073-276">After decoding begins, the value reflects the most recent Dolby frame.</span></span><br/> <span data-ttu-id="61073-277">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="61073-277">Read-only.</span></span> <br/> |
| [<span data-ttu-id="61073-278">CODECAPI \_ AVDecAudioDualMonoReproMode</span><span class="sxs-lookup"><span data-stu-id="61073-278">CODECAPI\_AVDecAudioDualMonoReproMode</span></span>](../directshow/avdecaudiodualmonorepromode-property.md)      | <span data-ttu-id="61073-279">Especifica como o decodificador Reproduz áudio dual-mono.</span><span class="sxs-lookup"><span data-stu-id="61073-279">Specifies how the decoder reproduces dual-mono audio.</span></span> <span data-ttu-id="61073-280">O valor padrão é **eAVDecAudioDualMonoReproMode \_ esquerdo \_ mono**.</span><span class="sxs-lookup"><span data-stu-id="61073-280">The default value is **eAVDecAudioDualMonoReproMode\_LEFT\_MONO**.</span></span> <span data-ttu-id="61073-281">O aplicativo pode definir essa propriedade a qualquer momento.</span><span class="sxs-lookup"><span data-stu-id="61073-281">The application can set this property at any time.</span></span><br/> <span data-ttu-id="61073-282">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="61073-282">Read/write.</span></span><br/>                                                                            |
| [<span data-ttu-id="61073-283">CODECAPI \_ AVDecCommonMeanBitRate</span><span class="sxs-lookup"><span data-stu-id="61073-283">CODECAPI\_AVDecCommonMeanBitRate</span></span>](../directshow/avdeccommonmeanbitrate.md)                         | <span data-ttu-id="61073-284">Para fluxos Dolby Digital (AC-3), especifica a taxa de bits do fluxo de entrada em bits por segundo.</span><span class="sxs-lookup"><span data-stu-id="61073-284">For Dolby Digital (AC-3) streams, specifies the bit rate of the input stream in bits per second.</span></span> <span data-ttu-id="61073-285">Para o Dolby Digital Plus (E-AC3), o valor é sempre zero.</span><span class="sxs-lookup"><span data-stu-id="61073-285">For Dolby Digital Plus (E-AC3), the value is always zero.</span></span><br/> <span data-ttu-id="61073-286">Somente leitura.</span><span class="sxs-lookup"><span data-stu-id="61073-286">Read only.</span></span><br/>                                                                                              |
| [<span data-ttu-id="61073-287">CODECAPI \_ AVDecDDDynamicRangeScaleHigh</span><span class="sxs-lookup"><span data-stu-id="61073-287">CODECAPI\_AVDecDDDynamicRangeScaleHigh</span></span>](../directshow/avdecdddynamicrangescalehigh-property.md)    | <span data-ttu-id="61073-288">O corte de alto nível quando o decodificador executa o controle de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="61073-288">The high-level cut when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="61073-289">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="61073-289">Read/write.</span></span><br/>                                                                                                                                                                                    |
| [<span data-ttu-id="61073-290">CODECAPI \_ AVDecDDDynamicRangeScaleLow</span><span class="sxs-lookup"><span data-stu-id="61073-290">CODECAPI\_AVDecDDDynamicRangeScaleLow</span></span>](../directshow/avdecdddynamicrangescalelow-property.md)      | <span data-ttu-id="61073-291">O aumento de nível baixo quando o decodificador executa o controle de intervalo dinâmico.</span><span class="sxs-lookup"><span data-stu-id="61073-291">The low-level boost when the decoder performs dynamic range control.</span></span><br/> <span data-ttu-id="61073-292">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="61073-292">Read/write.</span></span><br/>                                                                                                                                                                                   |
| [<span data-ttu-id="61073-293">CODECAPI \_ AVDecDDOperationalMode</span><span class="sxs-lookup"><span data-stu-id="61073-293">CODECAPI\_AVDecDDOperationalMode</span></span>](../directshow/avdecddoperationalmode-property.md)                | <span data-ttu-id="61073-294">O modo de controle de compactação.</span><span class="sxs-lookup"><span data-stu-id="61073-294">The compression control mode.</span></span><br/> <span data-ttu-id="61073-295">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="61073-295">Read/write.</span></span><br/>                                                                                                                                                                                                                          |
| [<span data-ttu-id="61073-296">CODECAPI \_ AVDecDDStereoDownMixMode</span><span class="sxs-lookup"><span data-stu-id="61073-296">CODECAPI\_AVDecDDStereoDownMixMode</span></span>](codecapi-avdecddstereodownmixmode.md)              | <span data-ttu-id="61073-297">O tipo de downmix estéreo.</span><span class="sxs-lookup"><span data-stu-id="61073-297">The type of stereo downmix.</span></span> <span data-ttu-id="61073-298">Essa propriedade se aplica quando a entrada é um fluxo multicanal e a saída é um fluxo estéreo.</span><span class="sxs-lookup"><span data-stu-id="61073-298">This property applies when the input is a multichannel stream and the output is a stereo stream.</span></span><br/> <span data-ttu-id="61073-299">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="61073-299">Read/write.</span></span><br/>                                                                                                                           |
| [<span data-ttu-id="61073-300">o MFT \_ dá suporte à \_ alteração de \_ formato dinâmico \_</span><span class="sxs-lookup"><span data-stu-id="61073-300">MFT\_SUPPORT\_DYNAMIC\_FORMAT\_CHANGE</span></span>](mft-support-dynamic-format-change-attribute.md) | <span data-ttu-id="61073-301">Esse atributo retorna **false**, indicando que o decodificador deve ser esvaziado antes que um novo tipo de entrada seja definido.</span><span class="sxs-lookup"><span data-stu-id="61073-301">This attribute returns **FALSE**, indicating that the decoder must be drained before a new input type is set.</span></span><br/> <span data-ttu-id="61073-302">Leitura/gravação.</span><span class="sxs-lookup"><span data-stu-id="61073-302">Read/write.</span></span><br/>                                                                                                                                          |



 

## <a name="remarks"></a><span data-ttu-id="61073-303">Comentários</span><span class="sxs-lookup"><span data-stu-id="61073-303">Remarks</span></span>

<span data-ttu-id="61073-304">O decodificador aceita apenas fluxos Dolby brutos, conforme definido por um/52B.</span><span class="sxs-lookup"><span data-stu-id="61073-304">The decoder accepts only raw Dolby streams, as defined by A/52B.</span></span> <span data-ttu-id="61073-305">Não há suporte para cargas como os fluxos de elementar pacotes (PES).</span><span class="sxs-lookup"><span data-stu-id="61073-305">Payloads such as Packetized Elementary Streams (PES) are not supported.</span></span> <span data-ttu-id="61073-306">Para o Dolby Digital Plus, o decodificador decodifica até 5,1 canais.</span><span class="sxs-lookup"><span data-stu-id="61073-306">For Dolby Digital Plus, the decoder decodes up to 5.1 channels.</span></span> <span data-ttu-id="61073-307">No Windows 10, 7,1 fluxos de canal são decodificados sem downmix.</span><span class="sxs-lookup"><span data-stu-id="61073-307">On Windows 10, 7.1 channel streams are decoded without downmix.</span></span> <span data-ttu-id="61073-308">Nas versões anteriores do sistema operacional, se o fluxo for de 7,1 canais, somente o downmix do canal 5,1 será decodificado.</span><span class="sxs-lookup"><span data-stu-id="61073-308">On previous OS versions, if the stream is 7.1 channels, only the 5.1 channel downmix will be decoded.</span></span> <span data-ttu-id="61073-309">Se o fluxo for Dolby Digital Plus com mais de um substream independente, somente substream independente 0 será decodificado.</span><span class="sxs-lookup"><span data-stu-id="61073-309">If the stream is Dolby Digital Plus with more than one independent substream, only independent substream 0 is decoded.</span></span> <span data-ttu-id="61073-310">O decodificador ignora outros subfluxos independentes.</span><span class="sxs-lookup"><span data-stu-id="61073-310">The decoder skips other independent substreams.</span></span> <span data-ttu-id="61073-311">Além disso, o decodificador ignora todos os subfluxos dependentes.</span><span class="sxs-lookup"><span data-stu-id="61073-311">In addition, the decoder skips all dependent substreams.</span></span> <span data-ttu-id="61073-312">O decodificador dá suporte à descriptografia e decodificação de fluxos protegidos pela tecnologia de Rights Management digital (DRM).</span><span class="sxs-lookup"><span data-stu-id="61073-312">The decoder supports decryption and decoding of streams that are protected by Digital Rights Management (DRM) technology.</span></span>

<span data-ttu-id="61073-313">Se o tipo de mídia de entrada tiver uma configuração de canal diferente de mono, estéreo ou dual-mono (tudo sem canal de LFE), o decodificador fornecerá duas opções para as configurações de canal de saída:</span><span class="sxs-lookup"><span data-stu-id="61073-313">If the input media type has a channel configuration other than mono, stereo, or dual-mono (all without LFE channel), the decoder provides two options for the output channel configurations:</span></span>

-   <span data-ttu-id="61073-314">saída de 8 canais (configuração de canal de 7,1)</span><span class="sxs-lookup"><span data-stu-id="61073-314">8-channel output (7.1 channel configuration)</span></span>
-   <span data-ttu-id="61073-315">saída de 6 canais (configuração de canal de 5,1)</span><span class="sxs-lookup"><span data-stu-id="61073-315">6-channel output (5.1 channel configuration)</span></span>
-   <span data-ttu-id="61073-316">Downmix estéreo</span><span class="sxs-lookup"><span data-stu-id="61073-316">Stereo downmix</span></span>

<span data-ttu-id="61073-317">Se downmix estéreo for selecionado, o tipo de downmix poderá ser definido no MFT usando a propriedade [CODECAPI \_ AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) .</span><span class="sxs-lookup"><span data-stu-id="61073-317">If stereo downmix is selected, the type of downmix can be set on the MFT by using the [CODECAPI\_AVDecDDStereoDownMixMode](codecapi-avdecddstereodownmixmode.md) property.</span></span>

<span data-ttu-id="61073-318">Se o tipo de saída for **MFAudioFormat \_ Dolby \_ AC3 \_ SPDIF**, cada buffer de saída conterá 6.144 bytes.</span><span class="sxs-lookup"><span data-stu-id="61073-318">If the output type is **MFAudioFormat\_Dolby\_AC3\_SPDIF**, each output buffer contains 6,144 bytes.</span></span> <span data-ttu-id="61073-319">O buffer começa com um cabeçalho S/PDIF de 8 bytes, seguido por um quadro AC-3 compactado, seguido por zero Padding para 6.144 bytes.</span><span class="sxs-lookup"><span data-stu-id="61073-319">The buffer starts with an 8-byte S/PDIF header, followed by a compressed AC-3 frame, followed by zero padding to 6,144 bytes.</span></span>

<span data-ttu-id="61073-320">Se o tipo de saída for **KSDATAFORMAT \_ subtipo \_ IEC61937 \_ Dolby \_ digital \_ Plus**, cada buffer de saída conterá 24.576 bytes.</span><span class="sxs-lookup"><span data-stu-id="61073-320">If the output type is **KSDATAFORMAT\_SUBTYPE\_IEC61937\_DOLBY\_DIGITAL\_PLUS**, each output buffer contains 24,576 bytes.</span></span> <span data-ttu-id="61073-321">O buffer começa com um cabeçalho S/PDIF de 8 bytes, seguido de 1 a 6 quadros Dolby Digital Plus compactados correspondentes a 1.536 exemplos de PCM, seguidos de zero preenchimento para 24.576 bytes.</span><span class="sxs-lookup"><span data-stu-id="61073-321">The buffer starts with an 8-byte S/PDIF header, followed by 1–6 compressed Dolby Digital Plus frames corresponding to 1,536 PCM samples, followed by zero padding to 24,576 bytes.</span></span> <span data-ttu-id="61073-322">Para saída de HDMI, somente substream independente 0 é empacotado.</span><span class="sxs-lookup"><span data-stu-id="61073-322">For HDMI output, only independent substream 0 is packed.</span></span>

<span data-ttu-id="61073-323">O MFT do decodificador é registrado com o sinalizador de enumeração de MFT de sinalizador **\_ \_ \_ FIELDOFUSE**, que indica que o MFT deve ser desbloqueado pelo aplicativo antes do uso.</span><span class="sxs-lookup"><span data-stu-id="61073-323">The decoder MFT is registered with the flag **MFT\_ENUM\_FLAG\_FIELDOFUSE**, which indicates that the MFT that must be unlocked by the application before use.</span></span> <span data-ttu-id="61073-324">Para obter mais informações, consulte [campo de restrições de uso](field-of-use-restrictions.md).</span><span class="sxs-lookup"><span data-stu-id="61073-324">For more information, see [Field of Use Restrictions](field-of-use-restrictions.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="61073-325">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61073-325">Requirements</span></span>



| <span data-ttu-id="61073-326">Requisito</span><span class="sxs-lookup"><span data-stu-id="61073-326">Requirement</span></span> | <span data-ttu-id="61073-327">Valor</span><span class="sxs-lookup"><span data-stu-id="61073-327">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------|
| <span data-ttu-id="61073-328">Cliente mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61073-328">Minimum supported client</span></span><br/> | <span data-ttu-id="61073-329">Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]</span><span class="sxs-lookup"><span data-stu-id="61073-329">Windows 8 \[desktop apps \| UWP apps\]</span></span><br/>                                          |
| <span data-ttu-id="61073-330">Servidor mínimo com suporte</span><span class="sxs-lookup"><span data-stu-id="61073-330">Minimum supported server</span></span><br/> | <span data-ttu-id="61073-331">Nenhum compatível</span><span class="sxs-lookup"><span data-stu-id="61073-331">None supported</span></span><br/>                                                                  |
| <span data-ttu-id="61073-332">DLL</span><span class="sxs-lookup"><span data-stu-id="61073-332">DLL</span></span><br/>                      | <dl> <span data-ttu-id="61073-333"><dt>Msauddecmft.dll</dt></span><span class="sxs-lookup"><span data-stu-id="61073-333"><dt>Msauddecmft.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61073-334">Confira também</span><span class="sxs-lookup"><span data-stu-id="61073-334">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61073-335">Objetos de codec</span><span class="sxs-lookup"><span data-stu-id="61073-335">Codec Objects</span></span>](codecobjects.md)
</dt> </dl>

 

 
