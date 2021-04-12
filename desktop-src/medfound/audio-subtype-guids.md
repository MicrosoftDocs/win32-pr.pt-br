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
# <a name="audio-subtype-guids"></a>GUIDs de subtipo de áudio

Os GUIDs de subtipo de áudio a seguir são definidos. Para especificar o subtipo, defina o atributo de [**\_ \_ subtipo MF MT**](mf-mt-subtype-attribute.md) no tipo de mídia. Exceto quando indicado, essas constantes são definidas no arquivo de cabeçalho mfapi. h.

Quando esses subtipos forem usados, defina o atributo de [ \_ \_ \_ tipo principal MF MT](mf-mt-major-type-attribute.md) como **MFMediaType \_ Audio**.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>GUID</th>
<th>Descrição</th>
<th>Marca de formato (FOURCC)</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MEDIASUBTYPE_RAW_AAC1</strong></td>
<td>AAC (codificação de áudio avançada).<br/> Esse subtipo é usado para AAC contido em um arquivo AVI com uma marca de formato de áudio igual a 0x00FF. <br/> Para obter mais informações, consulte o <a href="aac-decoder.md"><strong>decodificador AAC</strong></a>.<br/> Definido em wmcodecdsp. h<br/></td>
<td>WAVE_FORMAT_RAW_AAC1 (0x00FF)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>AAC (codificação de áudio avançada).<br/>
<blockquote>
[!Note]<br />
Equivalente a MEDIASUBTYPE_MPEG_HEAAC, definido em wmcodecdsp. h.
</blockquote>
<br/> O fluxo pode conter dados brutos AAC ou dados AAC em um fluxo de fluxo de transporte de dados de áudio (ADTS).<br/> Para obter mais informações, consulte:<br/>
<ul>
<li><a href="aac-decoder.md"><strong>Decodificador AAC</strong></a></li>
<li><a href="mpeg-4-file-source.md">Fonte de arquivo MPEG-4</a></li>
</ul></td>
<td>WAVE_FORMAT_MPEG_HEAAC (0x1610)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_ADTS</strong></td>
<td>Não usado.</td>
<td>WAVE_FORMAT_MPEG_ADTS_AAC (0x1600)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_ALAC</strong></td>
<td>Codec de áudio do Apple Lossless<br/> Com suporte no Windows 10 e posterior.<br/></td>
<td>WAVE_FORMAT_ALAC (0x6C61)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_NB</strong></td>
<td>Áudio de várias taxas Adaptative<br/> Com suporte no Windows 8.1 e posterior.<br/></td>
<td>WAVE_FORMAT_AMR_NB</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_AMR_WB</strong></td>
<td>Áudio Wideband de várias taxas Adaptative<br/> Com suporte no Windows 8.1 e posterior.<br/></td>
<td>WAVE_FORMAT_AMR_WB</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AMR_WP</strong></td>
<td>Com suporte no Windows 8.1 e posterior.<br/></td>
<td>WAVE_FORMAT_AMR_WP</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_AC3</strong></td>
<td>Dolby Digital (AC-3).<br/> Mesmo valor de GUID que <strong>MEDIASUBTYPE_DOLBY_AC3</strong>, que é definido em ksuuids. h<br/></td>
<td>Nenhum.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Dolby_AC3_SPDIF</strong></td>
<td>Áudio Dolby AC-3 por meio da Sony/Philips Digital Interface (S/PDIF).<br/> Esse valor de GUID é idêntico aos seguintes subtipos:<br/>
<ul>
<li><strong>KSDATAFORMAT_SUBTYPE_IEC61937_DOLBY_DIGITAL</strong>, definido em ksmedia. h.</li>
<li><strong>MEDIASUBTYPE_DOLBY_AC3_SPDIF</strong>, definido em UUIDs. h.</li>
</ul></td>
<td>WAVE_FORMAT_DOLBY_AC3_SPDIF (0x0092)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Dolby_DDPlus</strong></td>
<td>Dolby Digital Plus.<br/> Mesmo valor de GUID que <strong>MEDIASUBTYPE_DOLBY_DDPLUS</strong>, que é definido em wmcodecdsp. h.<br/></td>
<td>Nenhum</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_DRM</strong></td>
<td>Dados de áudio criptografados usados com o caminho de áudio seguro.</td>
<td>WAVE_FORMAT_DRM (0x0009)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_DTS</strong></td>
<td>Áudio de DTS (Digital Theater Systems).</td>
<td>WAVE_FORMAT_DTS (0x0008)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_FLAC</strong></td>
<td>Codec de áudio sem perdas gratuita<br/> Com suporte no Windows 10 e posterior.<br/></td>
<td>WAVE_FORMAT_FLAC (0xF1AC)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Áudio de ponto flutuante de IEEE não compactado.</td>
<td>WAVE_FORMAT_IEEE_FLOAT (0x0003)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Float_SpatialObjects</strong></td>
<td>Áudio de ponto flutuante de IEEE não compactado.</td>
<td>Nenhum</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MP3</strong></td>
<td>Camada de áudio MPEG-3 (MP3).</td>
<td>WAVE_FORMAT_MPEGLAYER3 (0x0055)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_MPEG</strong></td>
<td>Carga de áudio MPEG-1.</td>
<td>WAVE_FORMAT_MPEG (0x0050)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_MSP1</strong></td>
<td>Codec de voz do Windows Media Audio 9.</td>
<td>WAVE_FORMAT_WMAVOICE9 (0x000A)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_Opus</strong></td>
<td>Opus<br/> Com suporte no Windows 10 e posterior.<br/></td>
<td>WAVE_FORMAT_OPUS (0x704F)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>Áudio PCM não compactado.</td>
<td>WAVE_FORMAT_PCM (1)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_QCELP</strong></td>
<td>Áudio de QCELP (previsão de entusiasmo do código de Qualcomm).</td>
<td>Nenhum</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMASPDIF</strong></td>
<td>Codec do Windows Media Audio 9 Professional sobre S/PDIF.</td>
<td>WAVE_FORMAT_WMASPDIF (0x0164)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudio_Lossless</strong></td>
<td>Codec sem perdas do Windows Media Audio 9 ou codec do Windows Media Audio 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO_LOSSLESS (0x0163)</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_WMAudioV8</strong></td>
<td>Codec do Windows Media Audio 8, codec do Windows Media Audio 9 ou codec do Windows Media Audio 9,1.</td>
<td>WAVE_FORMAT_WMAUDIO2 (0x0161)</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_WMAudioV9</strong></td>
<td>Codec do Windows Media Audio 9 Professional ou Windows Media Audio 9,1 Professional.</td>
<td>WAVE_FORMAT_WMAUDIO3 (0x0162)</td>
</tr>
</tbody>
</table>



 

As marcas de formato listadas na terceira coluna dessa tabela são usadas na estrutura **WAVEFORMATEX** e são definidas no arquivo de cabeçalho Mmreg. h.

Dada uma marca de formato de áudio, você pode criar um GUID de subtipo de áudio da seguinte maneira:

1.  Comece com o valor **\_ base MFAudioFormat**, que é definido em mfaph. i.
2.  Substitua a primeira **DWORD** desse GUID pela marca de formato.

Você pode usar a [**macro \_ definir \_ GUID de MediaType**](/windows/desktop/api/mfapi/nf-mfapi-define_mediatype_guid) para definir uma nova constante de GUID que segue esse padrão.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Tipos de mídia de áudio](audio-media-types.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[GUIDs de tipo de mídia](media-type-guids.md)
</dt> <dt>

[Tipos de mídia](media-types.md)
</dt> </dl>

 

 




