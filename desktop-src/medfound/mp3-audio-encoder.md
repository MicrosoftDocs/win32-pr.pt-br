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
# <a name="mp3-audio-encoder"></a>Codificador de áudio MP3

O codificador de áudio MP3 Microsoft Media Foundation é uma [Media Foundation transformação](media-foundation-transforms.md) (MFT) que codifica áudio MPEG-1 Layer 3 (mp3).

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do codificador MP3 é **CLSID \_ MP3ACMCodecWrapper**, definido no arquivo de cabeçalho wmcodecdsp. h.

## <a name="media-types"></a>Tipos de mídia

O codificador MP3 dá suporte aos seguintes tipos de mídia. O tipo de saída deve ser definido antes do tipo de entrada.

### <a name="output-types"></a>Tipos de saída

Defina os seguintes atributos no tipo de mídia de saída.



<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
<th>Comentários</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principal.</td>
<td>Deve ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Subtipo de áudio.</td>
<td>Deve ser <strong>MFAudioFormat_MP3</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Taxa de bits do fluxo MP3 codificado, em bytes por segundo.</td>
<td>O codificador dá suporte a todas as taxas de bits definidas pelo padrão (32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256 ou 320 kbps).<br/> As taxas de bits padrão são 128 kbps para mono e 320 kbps para estéreo.<br/> Use esse atributo para especificar a taxa de bits codificada.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Número de canais.</td>
<td>Os seguintes valores têm suporte:
<ul>
<li>1 (mono)</li>
<li>2 (estéreo)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Exemplos por segundo.</td>
<td>Os seguintes valores têm suporte:
<ul>
<li>48000 (48 KHz)</li>
<li>44100 (44,1 KHz)</li>
<li>32000 (32 KHz)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-user-data-attribute.md">MF_MT_USER_DATA</a></td>
<td>Dados de codec adicionais.</td>
<td>Esse atributo contém os 12 bytes da estrutura <a href="/windows/desktop/api/mmreg/ns-mmreg-mpeglayer3waveformat"><strong>MPEGLAYER3WAVEFORMAT</strong></a> que seguem o membro <strong>WFX</strong> dessa estrutura.</td>
</tr>
</tbody>
</table>



 

Como alternativa, você pode preencher uma estrutura [**MPEGLAYER3WAVEFORMAT**](/windows/win32/api/mmreg/ns-mmreg-mpeglayer3waveformat) e chamar [**MFInitMediaTypeFromWaveFormatEx**](/windows/desktop/api/mfapi/nf-mfapi-mfinitmediatypefromwaveformatex) para converter a estrutura em um tipo de mídia Media Foundation.

### <a name="input-types"></a>Tipos de entrada

Defina os seguintes atributos no tipo de mídia de entrada.



| Atributo                                                                               | Descrição         | Comentários                         |
|-----------------------------------------------------------------------------------------|---------------------|---------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                               | Tipo principal.         | Deve ser **\_ áudio MFMediaType**. |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                      | Subtipo.            | Deve ser **MFAudioFormat \_ PCM**. |
| [**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md)       | Bits por amostra.    | Deve ser 16.                     |
| [**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md) | Exemplos por segundo. | Deve corresponder ao tipo de saída.     |
| [**\_canais de \_ número de áudio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)              | Número de canais. | Deve corresponder ao tipo de saída.     |



 

O codificador dá suporte apenas à entrada PCM de inteiro de 16 bits. Ele não dá suporte à entrada de ponto flutuante de 32 bits.

### <a name="media-formats"></a>Formatos de mídia

O padrão MPEG-1 e MPEG-2 define 252 formatos de áudio de camada 3. O codificador MP3 dá suporte ao padrão com algumas exceções, bem como alguns formatos adicionais, conforme descrito abaixo. A camada 3 é definida como:



| Requisito | Valor |
|----------------------------------|---------------------------------------------------------------|
| Canais                         | mono ou estéreo                                                |
| Taxas de amostragem MPEG-1 em kHz       | 44,1, 48, 32                                                  |
| Taxas de bits codificadas MPEG-1 em Kbps | 32, 40, 48, 56, 64, 80, 96, 112, 128, 160, 192, 224, 256, 320 |
| Taxas de exemplo MPEG-2 em kHz       | 8, 11, 25, 12, 16, 22, 5, 24                                  |
| Taxas de bits codificadas MPEG-2 em Kbps | 8, 16, 24, 32, 40, 48, 56, 64, 80, 96, 112, 144, 160          |



 

O codificador MP3 também dá suporte aos seguintes formatos.



| Taxa de amostragem | Taxa de bits     | Número do canal |
|-------------|--------------|----------------|
| 8000        | 18000, 20000 | 2              |
| 11025       | 18000, 20000 | 1 ou 2         |
| 12000       | 18000, 20000 | 1 ou 2         |
| 16000       | 18000, 20000 | 1              |
| 32000       | 144000       | 1 ou 2         |
| 44100       | 144000       | 1 ou 2         |
| 48000       | 144000       | 1 ou 2         |



 

O codificador MP3 não oferece suporte aos seguintes formatos definidos pelo padrão.



| Taxa de amostragem | Taxas de bits                                    | Número do canal |
|-------------|----------------------------------------------|----------------|
| 12000       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 ou 2         |
| 11025       | 80000, 96000, 112000, 128000, 144000, 160000 | 1 ou 2         |
| 8000        | 80000, 96000, 112000, 128000, 144000, 160000 | 1 ou 2         |
| 8000        | 8000, 11025, 12000, 16000, 22050, 24000      | 2              |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>           |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2012\]<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 
