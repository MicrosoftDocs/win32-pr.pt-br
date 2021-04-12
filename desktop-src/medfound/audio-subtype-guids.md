---
description: GUIDs de subtipo de áudio
ms.assetid: c38a1194-e2d8-42ca-8581-4054171f6f44
title: GUIDs de subtipo de áudio
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c04192f19f530c288b9aef7b5718b8329ea108bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457227"
---
# <a name="audio-subtype-guids"></a><span data-ttu-id="d04b0-103">GUIDs de subtipo de áudio</span><span class="sxs-lookup"><span data-stu-id="d04b0-103">Audio Subtype GUIDs</span></span>

<span data-ttu-id="d04b0-104">Os GUIDs de subtipo de áudio a seguir são definidos.</span><span class="sxs-lookup"><span data-stu-id="d04b0-104">The following audio subtype GUIDs are defined.</span></span> <span data-ttu-id="d04b0-105">Para especificar o subtipo, defina o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) no tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d04b0-105">To specify the subtype, set the [**MF\_MT\_SUBTYPE**](mf-mt-subtype-attribute.md) attribute on the media type.</span></span> <span data-ttu-id="d04b0-106">Exceto quando indicado, essas constantes são definidas no arquivo de cabeçalho mfapi. h.</span><span class="sxs-lookup"><span data-stu-id="d04b0-106">Except where noted, these constants are defined in the header file mfapi.h.</span></span>

<span data-ttu-id="d04b0-107">Quando esses subtipos forem usados, defina o atributo de [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md) como **MFMediaType \_ Audio**.</span><span class="sxs-lookup"><span data-stu-id="d04b0-107">When these subtypes are used, set the [MF\_MT\_MAJOR\_TYPE](mf-mt-major-type-attribute.md) attribute to **MFMediaType\_Audio**.</span></span>



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d04b0-108">GUID</span><span class="sxs-lookup"><span data-stu-id="d04b0-108">GUID</span></span></th>
<th><span data-ttu-id="d04b0-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="d04b0-109">Description</span></span></th>
<th><span data-ttu-id="d04b0-110">Marca de formato (FOURCC)</span><span class="sxs-lookup"><span data-stu-id="d04b0-110">Format Tag (FOURCC)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d04b0-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-111"><strong>MEDIASUBTYPE_RAW_AAC1</strong></span></span></td>
<td><span data-ttu-id="d04b0-112">AAC (codificação de áudio avançada).</span><span class="sxs-lookup"><span data-stu-id="d04b0-112">Advanced Audio Coding (AAC).</span></span><br/> <span data-ttu-id="d04b0-113">Esse subtipo é usado para AAC contido em um arquivo AVI com uma marca de formato de áudio igual a 0x00FF.</span><span class="sxs-lookup"><span data-stu-id="d04b0-113">This subtype is used for AAC contained in an AVI file with an audio format tag equal to 0x00FF.</span></span> <br/> <span data-ttu-id="d04b0-114">Para obter mais informações, consulte o <a href="aac-decoder.md"><strong>decodificador AAC</strong></a>.</span><span class="sxs-lookup"><span data-stu-id="d04b0-114">For more information, see <a href="aac-decoder.md"><strong>AAC Decoder</strong></a>.</span></span><br/> <span data-ttu-id="d04b0-115">Definido em wmcodecdsp. h</span><span class="sxs-lookup"><span data-stu-id="d04b0-115">Defined in wmcodecdsp.h</span></span><br/></td>
<td><span data-ttu-id="d04b0-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span><span class="sxs-lookup"><span data-stu-id="d04b0-116">WAVE_FORMAT_RAW_AAC1 (0x00FF)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-117"><strong>MFAudioFormat_AAC</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-117"><strong>MFAudioFormat_AAC</strong></span></span></td>
<td><span data-ttu-id="d04b0-118">AAC (codificação de áudio avançada).</span><span class="sxs-lookup"><span data-stu-id="d04b0-118">Advanced Audio Coding (AAC).</span></span><br/>
<blockquote>
[!Note]<br />
<span data-ttu-id="d04b0-119">Equivalente a MEDIASUBTYPE_MPEG_HEAAC, definido em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="d04b0-119">Equivalent to MEDIASUBTYPE_MPEG_HEAAC, defined in wmcodecdsp.h.</span></span>
</blockquote>
<br/> <span data-ttu-id="d04b0-120">O fluxo pode conter dados brutos AAC ou dados AAC em um fluxo de fluxo de transporte de dados de áudio (ADTS).</span><span class="sxs-lookup"><span data-stu-id="d04b0-120">The stream can contain raw AAC data or AAC data in an Audio Data Transport Stream (ADTS) stream.</span></span><br/> <span data-ttu-id="d04b0-121">Para obter mais informações, consulte:</span><span class="sxs-lookup"><span data-stu-id="d04b0-121">For more information, see:</span></span><br/>
<ul>
<li><span data-ttu-id="d04b0-122"><a href="aac-decoder.md"><strong>Decodificador AAC</strong></a></span><span class="sxs-lookup"><span data-stu-id="d04b0-122"><a href="aac-decoder.md"><strong>AAC Decoder</strong></a></span></span></li>
<li><span data-ttu-id="d04b0-123"><a href="mpeg-4-file-source.md">Fonte de arquivo MPEG-4</a></span><span class="sxs-lookup"><span data-stu-id="d04b0-123"><a href="mpeg-4-file-source.md">MPEG-4 File Source</a></span></span></li>
</ul></td>
<td><span data-ttu-id="d04b0-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span><span class="sxs-lookup"><span data-stu-id="d04b0-124">WAVE_FORMAT_MPEG_HEAAC (0x1610)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-125"><strong>MFAudioFormat_ADTS</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-125"><strong>MFAudioFormat_ADTS</strong></span></span></td>
<td><span data-ttu-id="d04b0-126">Não usado.</span><span class="sxs-lookup"><span data-stu-id="d04b0-126">Not used.</span></span></td>
<td><span data-ttu-id="d04b0-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span><span class="sxs-lookup"><span data-stu-id="d04b0-127">WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-128"><strong>MFAudioFormat_ALAC</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-128"><strong>MFAudioFormat_ALAC</strong></span></span></td>
<td><span data-ttu-id="d04b0-129">Codec de áudio do Apple Lossless</span><span class="sxs-lookup"><span data-stu-id="d04b0-129">Apple Lossless Audio Codec</span></span><br/> <span data-ttu-id="d04b0-130">Com suporte no Windows 10 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d04b0-130">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="d04b0-131">WAVE_FORMAT_ALAC (0x6C61)</span><span class="sxs-lookup"><span data-stu-id="d04b0-131">WAVE_FORMAT_ALAC (0x6C61)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-132"><strong>MFAudioFormat_AMR_NB</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-132"><strong>MFAudioFormat_AMR_NB</strong></span></span></td>
<td><span data-ttu-id="d04b0-133">Áudio de várias taxas Adaptative</span><span class="sxs-lookup"><span data-stu-id="d04b0-133">Adaptative Multi-Rate audio</span></span><br/> <span data-ttu-id="d04b0-134">Com suporte no Windows 8.1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d04b0-134">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="d04b0-135">WAVE_FORMAT_AMR_NB</span><span class="sxs-lookup"><span data-stu-id="d04b0-135">WAVE_FORMAT_AMR_NB</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-136"><strong>MFAudioFormat_AMR_WB</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-136"><strong>MFAudioFormat_AMR_WB</strong></span></span></td>
<td><span data-ttu-id="d04b0-137">Áudio Wideband de várias taxas Adaptative</span><span class="sxs-lookup"><span data-stu-id="d04b0-137">Adaptative Multi-Rate Wideband audio</span></span><br/> <span data-ttu-id="d04b0-138">Com suporte no Windows 8.1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d04b0-138">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="d04b0-139">WAVE_FORMAT_AMR_WB</span><span class="sxs-lookup"><span data-stu-id="d04b0-139">WAVE_FORMAT_AMR_WB</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-140"><strong>MFAudioFormat_AMR_WP</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-140"><strong>MFAudioFormat_AMR_WP</strong></span></span></td>
<td><span data-ttu-id="d04b0-141">Com suporte no Windows 8.1 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d04b0-141">Supported in Windows 8.1 and later.</span></span><br/></td>
<td><span data-ttu-id="d04b0-142">WAVE_FORMAT_AMR_WP</span><span class="sxs-lookup"><span data-stu-id="d04b0-142">WAVE_FORMAT_AMR_WP</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-143"><strong>MFAudioFormat_Dolby_AC3</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-143"><strong>MFAudioFormat_Dolby_AC3</strong></span></span></td>
<td><span data-ttu-id="d04b0-144">Dolby Digital (AC-3).</span><span class="sxs-lookup"><span data-stu-id="d04b0-144">Dolby Digital (AC-3).</span></span><br/> <span data-ttu-id="d04b0-145">Mesmo valor de GUID que <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, que é definido em ksuuids. h</span><span class="sxs-lookup"><span data-stu-id="d04b0-145">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, which is defined in ksuuids.h</span></span><br/></td>
<td><span data-ttu-id="d04b0-146">Nenhum.</span><span class="sxs-lookup"><span data-stu-id="d04b0-146">None.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-147"><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></span></span></td>
<td><span data-ttu-id="d04b0-148">Áudio Dolby AC-3 por meio da Sony/Philips Digital Interface (S/PDIF).</span><span class="sxs-lookup"><span data-stu-id="d04b0-148">Dolby AC-3 audio over Sony/Philips Digital Interface (S/PDIF).</span></span><br/> <span data-ttu-id="d04b0-149">Esse valor de GUID é idêntico aos seguintes subtipos:</span><span class="sxs-lookup"><span data-stu-id="d04b0-149">This GUID value is identical to the following subtypes:</span></span><br/>
<ul>
<li><span data-ttu-id="d04b0-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, definido em ksmedia. h.</span><span class="sxs-lookup"><span data-stu-id="d04b0-150"><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, defined in ksmedia.h.</span></span></li>
<li><span data-ttu-id="d04b0-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, definido em UUIDs. h.</span><span class="sxs-lookup"><span data-stu-id="d04b0-151"><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, defined in uuids.h.</span></span></li>
</ul></td>
<td><span data-ttu-id="d04b0-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span><span class="sxs-lookup"><span data-stu-id="d04b0-152">WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-153"><strong>MFAudioFormat_Dolby_DDPlus</strong></span></span></td>
<td><span data-ttu-id="d04b0-154">Dolby Digital Plus.</span><span class="sxs-lookup"><span data-stu-id="d04b0-154">Dolby Digital Plus.</span></span><br/> <span data-ttu-id="d04b0-155">Mesmo valor de GUID que <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, que é definido em wmcodecdsp. h.</span><span class="sxs-lookup"><span data-stu-id="d04b0-155">Same GUID value as <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, which is defined in wmcodecdsp.h.</span></span><br/></td>
<td><span data-ttu-id="d04b0-156">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d04b0-156">None</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-157"><strong>MFAudioFormat_DRM</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-157"><strong>MFAudioFormat_DRM</strong></span></span></td>
<td><span data-ttu-id="d04b0-158">Dados de áudio criptografados usados com o caminho de áudio seguro.</span><span class="sxs-lookup"><span data-stu-id="d04b0-158">Encrypted audio data used with secure audio path.</span></span></td>
<td><span data-ttu-id="d04b0-159">WAVE_FORMAT_DRM (0x0009)</span><span class="sxs-lookup"><span data-stu-id="d04b0-159">WAVE_FORMAT_DRM (0x0009)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-160"><strong>MFAudioFormat_DTS</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-160"><strong>MFAudioFormat_DTS</strong></span></span></td>
<td><span data-ttu-id="d04b0-161">Áudio de DTS (Digital Theater Systems).</span><span class="sxs-lookup"><span data-stu-id="d04b0-161">Digital Theater Systems (DTS) audio.</span></span></td>
<td><span data-ttu-id="d04b0-162">WAVE_FORMAT_DTS (0x0008)</span><span class="sxs-lookup"><span data-stu-id="d04b0-162">WAVE_FORMAT_DTS (0x0008)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-163"><strong>MFAudioFormat_FLAC</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-163"><strong>MFAudioFormat_FLAC</strong></span></span></td>
<td><span data-ttu-id="d04b0-164">Codec de áudio sem perdas gratuita</span><span class="sxs-lookup"><span data-stu-id="d04b0-164">Free Lossless Audio Codec</span></span><br/> <span data-ttu-id="d04b0-165">Com suporte no Windows 10 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d04b0-165">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="d04b0-166">WAVE_FORMAT_FLAC (0xF1AC)</span><span class="sxs-lookup"><span data-stu-id="d04b0-166">WAVE_FORMAT_FLAC (0xF1AC)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-167"><strong>MFAudioFormat_Float</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-167"><strong>MFAudioFormat_Float</strong></span></span></td>
<td><span data-ttu-id="d04b0-168">Áudio de ponto flutuante de IEEE não compactado.</span><span class="sxs-lookup"><span data-stu-id="d04b0-168">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="d04b0-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span><span class="sxs-lookup"><span data-stu-id="d04b0-169">WAVE_FORMAT_IEEE_FLOAT (0x0003)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-170"><strong>MFAudioFormat_Float_SpatialObjects</strong></span></span></td>
<td><span data-ttu-id="d04b0-171">Áudio de ponto flutuante de IEEE não compactado.</span><span class="sxs-lookup"><span data-stu-id="d04b0-171">Uncompressed IEEE floating-point audio.</span></span></td>
<td><span data-ttu-id="d04b0-172">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d04b0-172">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-173"><strong>MFAudioFormat_MP3</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-173"><strong>MFAudioFormat_MP3</strong></span></span></td>
<td><span data-ttu-id="d04b0-174">Camada de áudio MPEG-3 (MP3).</span><span class="sxs-lookup"><span data-stu-id="d04b0-174">MPEG Audio Layer-3 (MP3).</span></span></td>
<td><span data-ttu-id="d04b0-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span><span class="sxs-lookup"><span data-stu-id="d04b0-175">WAVE_FORMAT_MPEGLAYER3 (0x0055)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-176"><strong>MFAudioFormat_MPEG</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-176"><strong>MFAudioFormat_MPEG</strong></span></span></td>
<td><span data-ttu-id="d04b0-177">Carga de áudio MPEG-1.</span><span class="sxs-lookup"><span data-stu-id="d04b0-177">MPEG-1 audio payload.</span></span></td>
<td><span data-ttu-id="d04b0-178">WAVE_FORMAT_MPEG (0x0050)</span><span class="sxs-lookup"><span data-stu-id="d04b0-178">WAVE_FORMAT_MPEG (0x0050)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-179"><strong>MFAudioFormat_MSP1</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-179"><strong>MFAudioFormat_MSP1</strong></span></span></td>
<td><span data-ttu-id="d04b0-180">Codec de voz do Windows Media Audio 9.</span><span class="sxs-lookup"><span data-stu-id="d04b0-180">Windows Media Audio 9 Voice codec.</span></span></td>
<td><span data-ttu-id="d04b0-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span><span class="sxs-lookup"><span data-stu-id="d04b0-181">WAVE_FORMAT_WMAVOICE9 (0x000A)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-182"><strong>MFAudioFormat_Opus</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-182"><strong>MFAudioFormat_Opus</strong></span></span></td>
<td><span data-ttu-id="d04b0-183">Opus</span><span class="sxs-lookup"><span data-stu-id="d04b0-183">Opus</span></span><br/> <span data-ttu-id="d04b0-184">Com suporte no Windows 10 e posterior.</span><span class="sxs-lookup"><span data-stu-id="d04b0-184">Supported in Windows 10 and later.</span></span><br/></td>
<td><span data-ttu-id="d04b0-185">WAVE_FORMAT_OPUS (0x704F)</span><span class="sxs-lookup"><span data-stu-id="d04b0-185">WAVE_FORMAT_OPUS (0x704F)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-186"><strong>MFAudioFormat_PCM</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-186"><strong>MFAudioFormat_PCM</strong></span></span></td>
<td><span data-ttu-id="d04b0-187">Áudio PCM não compactado.</span><span class="sxs-lookup"><span data-stu-id="d04b0-187">Uncompressed PCM audio.</span></span></td>
<td><span data-ttu-id="d04b0-188">WAVE_FORMAT_PCM (1)</span><span class="sxs-lookup"><span data-stu-id="d04b0-188">WAVE_FORMAT_PCM (1)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-189"><strong>MFAudioFormat_QCELP</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-189"><strong>MFAudioFormat_QCELP</strong></span></span></td>
<td><span data-ttu-id="d04b0-190">Áudio de QCELP (previsão de entusiasmo do código de Qualcomm).</span><span class="sxs-lookup"><span data-stu-id="d04b0-190">QCELP (Qualcomm Code Excited Linear Prediction) audio.</span></span></td>
<td><span data-ttu-id="d04b0-191">Nenhum</span><span class="sxs-lookup"><span data-stu-id="d04b0-191">None</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-192"><strong>MFAudioFormat_WMASPDIF</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-192"><strong>MFAudioFormat_WMASPDIF</strong></span></span></td>
<td><span data-ttu-id="d04b0-193">Codec do Windows Media Audio 9 Professional sobre S/PDIF.</span><span class="sxs-lookup"><span data-stu-id="d04b0-193">Windows Media Audio 9 Professional codec over S/PDIF.</span></span></td>
<td><span data-ttu-id="d04b0-194">WAVE_FORMAT_WMASPDIF (0x0164)</span><span class="sxs-lookup"><span data-stu-id="d04b0-194">WAVE_FORMAT_WMASPDIF (0x0164)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-195"><strong>MFAudioFormat_WMAudio_Lossless</strong></span></span></td>
<td><span data-ttu-id="d04b0-196">Codec sem perdas do Windows Media Audio 9 ou codec do Windows Media Audio 9,1.</span><span class="sxs-lookup"><span data-stu-id="d04b0-196">Windows Media Audio 9 Lossless codec or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="d04b0-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span><span class="sxs-lookup"><span data-stu-id="d04b0-197">WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="d04b0-198"><strong>MFAudioFormat_WMAudioV8</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-198"><strong>MFAudioFormat_WMAudioV8</strong></span></span></td>
<td><span data-ttu-id="d04b0-199">Codec do Windows Media Audio 8, codec do Windows Media Audio 9 ou codec do Windows Media Audio 9,1.</span><span class="sxs-lookup"><span data-stu-id="d04b0-199">Windows Media Audio 8 codec, Windows Media Audio 9 codec, or Windows Media Audio 9.1 codec.</span></span></td>
<td><span data-ttu-id="d04b0-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span><span class="sxs-lookup"><span data-stu-id="d04b0-200">WAVE_FORMAT_WMAUDIO2 (0x0161)</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="d04b0-201"><strong>MFAudioFormat_WMAudioV9</strong></span><span class="sxs-lookup"><span data-stu-id="d04b0-201"><strong>MFAudioFormat_WMAudioV9</strong></span></span></td>
<td><span data-ttu-id="d04b0-202">Codec do Windows Media Audio 9 Professional ou Windows Media Audio 9,1 Professional.</span><span class="sxs-lookup"><span data-stu-id="d04b0-202">Windows Media Audio 9 Professional codec or Windows Media Audio 9.1 Professional codec.</span></span></td>
<td><span data-ttu-id="d04b0-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span><span class="sxs-lookup"><span data-stu-id="d04b0-203">WAVE_FORMAT_WMAUDIO3 (0x0162)</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="d04b0-204">As marcas de formato listadas na terceira coluna dessa tabela são usadas na estrutura **WAVEFORMATEX** e são definidas no arquivo de cabeçalho Mmreg. h.</span><span class="sxs-lookup"><span data-stu-id="d04b0-204">The format tags listed in the third column of this table are used in the **WAVEFORMATEX** structure, and are defined in the header file mmreg.h.</span></span>

<span data-ttu-id="d04b0-205">Dada uma marca de formato de áudio, você pode criar um GUID de subtipo de áudio da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="d04b0-205">Given an audio format tag, you can create an audio subtype GUID as follows:</span></span>

1.  <span data-ttu-id="d04b0-206">Comece com o valor **\_ base MFAudioFormat**, que é definido em mfaph. i.</span><span class="sxs-lookup"><span data-stu-id="d04b0-206">Start with the value **MFAudioFormat\_Base**, which is defined in mfaph.i.</span></span>
2.  <span data-ttu-id="d04b0-207">Substitua a primeira **DWORD** desse GUID pela marca de formato.</span><span class="sxs-lookup"><span data-stu-id="d04b0-207">Replace the first **DWORD** of this GUID with the format tag.</span></span>

<span data-ttu-id="d04b0-208">Você pode usar a [**macro \_ definir \_ GUID de MediaType**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) para definir uma nova constante de GUID que segue esse padrão.</span><span class="sxs-lookup"><span data-stu-id="d04b0-208">You can use the [**DEFINE\_MEDIATYPE\_GUID**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) macro to define a new GUID constant that follows this pattern.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d04b0-209">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="d04b0-209">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d04b0-210">Tipos de mídia de áudio</span><span class="sxs-lookup"><span data-stu-id="d04b0-210">Audio Media Types</span></span>](audio-media-types.md)
</dt> <dt>

[<span data-ttu-id="d04b0-211">**IMFMediaType**</span><span class="sxs-lookup"><span data-stu-id="d04b0-211">**IMFMediaType**</span></span>](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[<span data-ttu-id="d04b0-212">GUIDs de tipo de mídia</span><span class="sxs-lookup"><span data-stu-id="d04b0-212">Media Type GUIDs</span></span>](media-type-guids.md)
</dt> <dt>

[<span data-ttu-id="d04b0-213">Tipos de mídia</span><span class="sxs-lookup"><span data-stu-id="d04b0-213">Media Types</span></span>](media-types.md)
</dt> </dl>

 

 




