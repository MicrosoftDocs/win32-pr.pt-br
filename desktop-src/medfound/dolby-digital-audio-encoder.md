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
# <a name="dolby-digital-audio-encoder"></a>Codificador de áudio digital Dolby

O decodificador de áudio Dolby é uma [Media Foundation transformação](media-foundation-transforms.md) (MFT) que codifica áudio mono ou estéreo em Dolby Digital, também chamada Dolby AC-3. O codificador não oferece suporte à entrada de vários canais, como a configuração do canal 5,1.

> [!IMPORTANT]
> Para versões do Windows anteriores ao Windows 8, a implementação da Microsoft da tecnologia Dolby Digital é restrita em termos do programa Dolby Digital Licensing para uso pelos aplicativos da Microsoft.

 

Para obter mais informações sobre áudio Dolby Digital, consulte documento de compactação de áudio digital (ATSC) (Comitê de sistemas de televisão avançada) *padrão (AC-3, E-AC-3) revisão B*.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do decodificador de áudio Dolby é **CLSID \_ CMSDolbyDigitalEncMFT**, definido no arquivo de cabeçalho wmcodecdsp. h.

## <a name="output-types"></a>Tipos de saída

O tipo de saída deve ser definido primeiro, antes do tipo de entrada. A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de saída.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principal.</td>
<td>Obrigatórios. Deve ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Subtipo de áudio.</td>
<td>Obrigatórios. Deve ser <strong>MFAudioFormat_Dolby_AC3</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Exemplos por segundo.</td>
<td>Obrigatórios. Os seguintes valores têm suporte:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canais.</td>
<td>Obrigatórios. Deve ser 1 (mono) ou 2 (estéreo).</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica a atribuição de canais de áudio a posições do orador.</td>
<td>Opcional. Se definido, o valor deve ser 0x3 para estéreo (canais frontal esquerdo e direito) ou 0x4 para mono (canal do front Center).</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Taxa de bits do fluxo AC-3 codificado, em bytes por segundo.</td>
<td>Opcional. Consulte comentários para obter os valores válidos. Se esse atributo não estiver definido, o codificador usará uma taxa de bits padrão, conforme descrito em comentários.</td>
</tr>
</tbody>
</table>



 

Se os atributos opcionais não estiverem definidos, o codificador os adicionará ao tipo de mídia depois que o tipo for definido.

## <a name="input-types"></a>Tipos de entrada

A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de entrada.



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
<td><a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a></td>
<td>Tipo principal.</td>
<td>Obrigatórios. Deve ser <strong>MFMediaType_Audio</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a></td>
<td>Subtipo de áudio.</td>
<td>Obrigatórios. Deve ser <strong>MFAudioFormat_PCM</strong> ou <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a></td>
<td>Número de bits por amostra de áudio.</td>
<td>Obrigatórios. O valor deve ser 16 se o subtipo for <strong>MFAudioFormat_PCM</strong>ou 32 se o subtipo for <strong>MFAudioFormat_Float</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Exemplos por segundo.</td>
<td>Obrigatórios. Deve corresponder ao tipo de saída.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a></td>
<td>Número de canais.</td>
<td>Obrigatórios. Deve corresponder ao tipo de saída.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a></td>
<td>Alinhamento de bloco, em bytes.</td>
<td>Obrigatórios. Calcule o valor da seguinte maneira:
<ul>
<li><strong>MFAudioFormat_PCM</strong>: número de canais × 2.</li>
<li><strong>MFAudioFormat_Float</strong>: número de canais × 4.</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a></td>
<td>Taxa de bits do fluxo AC3 codificado, em bytes por segundo.</td>
<td>Obrigatórios. Deve ser igual ao alinhamento de bloco × amostras por segundo.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a></td>
<td>Especifica a atribuição de canais de áudio a posições do orador.</td>
<td>Opcional. Se definido, o valor deve corresponder ao tipo de saída.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a></td>
<td>Número de bits válidos de dados de áudio em cada amostra de áudio.</td>
<td>Opcional. Se definido, o valor deve ser idêntico a <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a>.</td>
</tr>
</tbody>
</table>



 

O codificador não oferece suporte à conversão de taxa de amostragem ou conversão estéreo/mono.

## <a name="remarks"></a>Comentários

Cada quadro de áudio Dolby AC-3 contém 1536 amostras de áudio por canal. No entanto, cada buffer de entrada para o codificador pode conter qualquer número de amostras de PCM. O tamanho de cada buffer de entrada deve ser um múltiplo do alinhamento de bloco. O codificador armazena em cache os exemplos de entrada até que ele tenha o suficiente para 1536 amostras de áudio por canal; em que ponto o codificador gera um quadro AC-3.

Cada buffer de saída contém um quadro bruto AC-3. A duração é equivalente à duração de 1536 amostras de PCM na taxa de amostragem atual (32 ms) a taxa de amostragem de 48 kHz, 34,83 MS às 44,1 kHz e 48 mseg em 32 kHz). O tamanho de cada buffer de saída depende da taxa de bits e da taxa de amostragem.

Para especificar a taxa de bits de codificação, defina o atributo [ \_ \_ vídeo \_ médio de \_ bytes \_ por \_ segundo do MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) no tipo de saída. A tabela a seguir mostra a relação entre taxa de bits de codificação e \_ média de bytes de áudio MF MT \_ \_ \_ \_ por \_ segundo.



| Taxa de bits (Kbps) | [áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) | Comentários                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8000                                                                                     | Somente mono.                                              |
| 80              | 10000                                                                                    | Somente mono.                                              |
| 96              | 12000                                                                                    | Somente mono.                                              |
| 112             | 14000                                                                                    | Somente mono.                                              |
| 128             | 16000                                                                                    | Mono ou estéreo.                                         |
| 160             | 20000                                                                                    | Mono ou estéreo.                                         |
| 192             | 24.000                                                                                    | Mono ou estéreo. Essa é a configuração padrão para mono.   |
| 224             | 28000                                                                                    | Mono ou estéreo.                                         |
| 256             | 32000                                                                                    | Mono ou estéreo. Essa é a configuração padrão para estéreo. |
| 320             | 40000                                                                                    | Somente estéreo.                                            |
| 384             | 48000                                                                                    | Somente estéreo.                                            |
| 448             | 56000                                                                                    | Somente estéreo.                                            |



 

A taxa de bits de codificação padrão é definida em 256 kbps para estéreo e 192 kbps para mono. As configurações padrão são refletidas nos tipos de mídia retornados pelo método [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) do codificador.

### <a name="example-media-types"></a>Exemplos de tipos de mídia

Aqui está um exemplo dos tipos de mídia que são necessários para codificar o PCM de inteiros de 16 bits, áudio estéreo de 48 kHz na taxa de bits padrão de 256 kbps.

Tipo de mídia de saída:

| Atributo                                                                           | Valor                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md)                               | **\_Áudio MFMediaType**        |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ Dolby \_ AC3** |
| [\_amostras de áudio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [\_canais de \_ número de áudio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Tipo de mídia de entrada:

| Atributo                                                                                | Valor                  |
|------------------------------------------------------------------------------------------|------------------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md)                                    | **\_Áudio MFMediaType** |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                           | **\_PCM MFAudioFormat** |
| [\_bits de áudio MF MT \_ \_ \_ por \_ amostra](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [\_amostras de áudio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [\_canais de \_ número de áudio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [\_alinhamento de \_ bloco de áudio MF MT \_ \_](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos da área de trabalho do Windows 8 \| UWP\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 




