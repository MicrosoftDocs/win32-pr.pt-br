---
description: O codificador AAC do Microsoft Media Foundation é uma Transformação Media Foundation que codifica o perfil LC (Codificação de Áudio Avançado) de Baixa Complexidade (LC), conforme definido por ISO/IEC 13818-7 (MPEG-2 Audio Part 7) .
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Codificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9fb6867ad42645ffc2bbf2b853e215d3794053157a776e02eddf015b320e3215
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119943366"
---
# <a name="aac-encoder"></a>Codificador AAC

O codificador AAC do Microsoft Media Foundation é uma Transformação [Media Foundation](media-foundation-transforms.md) que codifica o perfil LC (Codificação de Áudio Avançado) de Baixa Complexidade (LC), conforme definido por ISO/IEC 13818-7 (MPEG-2 Audio Part 7) .

O codificador AAC não dá suporte à codificação para outros perfis AAC, como Main, SSR ou LTP.

## <a name="class-identifier"></a>Identificador de Classe

O CLSID (identificador de classe) do codificador AAC é **CLSID \_ AACMFTEncoder**, definido no arquivo de header wmcodecdsp.h.

## <a name="media-types"></a>Tipos de mídia

O codificador AAC dá suporte aos seguintes tipos de mídia. Você pode definir os tipos primeiro no tipo de entrada de ordem ou primeiro no tipo de saída.

### <a name="input-types"></a>Tipos de entrada

De definir os atributos a seguir no tipo de mídia de entrada.



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
<td>Subtipo.</td>
<td>Deve ser <strong>MFAudioFormat_PCM</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Bits por exemplo.</td>
<td>Deve ser 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Exemplos por segundo.</td>
<td>Os seguintes valores têm suporte:
<ul>
<li>44100 (44,1 KHz)</li>
<li>48000 (48 KHz)</li>
</ul></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Número de canais.</td>
<td>Deve ser 1 (mono) ou 2 (estéreo) ou 6 (5.1).
<blockquote>
[!Note]<br />
O suporte para seis canais de áudio foi introduzido com Windows 10 e não está disponível para versões anteriores do Windows.
</blockquote>
<br/></td>
</tr>
</tbody>
</table>



 

Depois que o tipo de entrada é definido, o codificador deriva os seguintes valores e os adiciona ao tipo de mídia:

-   [**BYTES MF \_ MT \_ AUDIO \_ AVG \_ POR \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**ALINHAMENTO DO \_ BLOCO DE ÁUDIO MT \_ \_ \_ MT**](mf-mt-audio-block-alignment-attribute.md)
-   [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a>Tipos de saída

De definir os atributos a seguir no tipo de mídia de saída.



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
<td>Deve ser <strong>MFAudioFormat_AAC</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Bits por exemplo.</td>
<td>Deve ser 16.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Exemplos por segundo.</td>
<td>Deve corresponder ao tipo de entrada.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Número de canais.</td>
<td>Deve corresponder ao tipo de entrada.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a></td>
<td>Taxa de bits do fluxo AAC codificado, em bytes por segundo.</td>
<td>Os seguintes valores têm suporte:
<ul>
<li>12000</li>
<li>16000</li>
<li>20000</li>
<li>24.000</li>
</ul>
O valor padrão para mono e estéreo é 12000 (96 Kbps).<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>O tipo de carga do AAC.</td>
<td>Opcional. Se definido, o valor deverá ser zero, indicando que o fluxo contém raw_data_block elementos.<br/> Opcional. Se o atributo não estiver definido, o valor padrão será zero, indicando que o fluxo contém raw_data_block somente elementos (AAC bruto). <br/> No Windows 7, se esse atributo estiver definido, o valor deverá ser zero.<br/> A partir Windows 8, o valor pode ser 0 (AAC bruto) ou 1 (ADTS AAC). <br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>O nível e o perfil de áudio do AAC.</td>
<td>Opcional. Os seguintes valores têm suporte:
<ul>
<li>0x29 (padrão)</li>
<li>0x2A</li>
<li>0x2B</li>
<li>0x2C</li>
<li>0x2E</li>
<li>0x2F</li>
<li>0x30</li>
<li>0x31</li>
<li>0x32</li>
<li>0x33</li>
</ul></td>
</tr>
</tbody>
</table>

A tabela a seguir lista os valores que podem ser usados para o atributo MF_MT_AAC_PROFILE_LEVEL_INDICATION dados.

| MF_MT_AAC_PROFILE_LEVEL_INDICATION valor | Perfil                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | Perfil do AAC L2                    | 
| 0x2A                                     | Perfil AAC L4                    | 
| 0x2B                                     | Perfil do AAC L5                    | 
| 0x2C                                     | Perfil AAC de alta eficiência v1 L2 | 
| 0x2E                                     | Perfil AAC de alta eficiência v1 L4 | 
| 0x2F                                     | Perfil AAC de alta eficiência do v1 | 
| 0x30                                     | L2 de perfil AAC de alta eficiência v2 | 
| 0x31                                     | Perfil AAC L3 de alta eficiência | 
| 0x32                                     | Perfil AAC de alta eficiência v2 | 
| 0x33                                     | Perfil AAC de alta eficiência v2 | 

 

Depois que o tipo de saída é definido, o codificador AAC atualiza o tipo adicionando o atributo de [**\_ dados de \_ usuário \_ MF MT**](mf-mt-user-data-attribute.md) . Esse atributo contém a parte da estrutura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece após a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) (ou seja, após o membro **WFX** ). Isso é seguido pelos dados de AudioSpecificConfig (), conforme definido por ISO/IEC 14496-3.

Cada exemplo de saída contém um quadro AAC compactado sem cabeçalho. Esse formato é equivalente ao elemento de \_ bloco de dados brutos \_ () definido por MPEG-2. O atributo de [ \_ tipo de conteúdo MF MT \_ AAC \_ \_ ](mf-mt-aac-payload-type.md) , se presente no tipo de saída, deve ser definido como zero para indicar esse tipo de carga.

Cada exemplo de saída contém um quadro AAC compactado correspondente a 1024 exemplos de PCM. Por exemplo, a taxa de amostragem de 48 kHz, a duração de um quadro compactado é de 21,33 MS.

Se o [tipo de carga do MF \_ MT \_ AAC \_ \_ ](mf-mt-aac-payload-type.md) for zero (o valor padrão), cada exemplo de saída conterá um \_ elemento de bloco de dados brutos \_ (), conforme definido pelo ISO/IEC 13818-7.

## <a name="example-media-types"></a>Exemplos de tipos de mídia

Aqui está um exemplo dos tipos de mídia necessários para a codificação de áudio estéreo de 160 a 44,1-kHz, em relação ao AAC bruto

Tipo de mídia de entrada:



| Atributo                                                                                    | Valor                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                                    | **\_Áudio MFMediaType** |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                           | **\_PCM MFAudioFormat** |
| [**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**\_canais de \_ número de áudio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (opcional)      |
| [**\_alinhamento de \_ bloco de áudio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)             | 4 (opcional)           |
| [**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**](mf-mt-all-samples-independent-attribute.md)         | 1 (opcional)           |
| [**\_taxa de \_ \_ bits média de MF MT**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (opcional)     |
| [**\_amostras de \_ \_ tamanho fixo MF MT \_**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (opcional)           |



 

Tipo de mídia de saída:



| Atributo                                                                                      | Valor                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**\_ \_ tipo principal MF \_ MT**](mf-mt-major-type-attribute.md)                                      | **\_Áudio MFMediaType**                                                                          |
| [**subtipo MF \_ MT \_**](mf-mt-subtype-attribute.md)                                             | **\_AAC MFAudioFormat**                                                                          |
| [**\_bits de áudio MF MT \_ \_ \_ por \_ amostra**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**\_amostras de áudio MF MT \_ \_ \_ por \_ segundo**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**\_canais de \_ número de áudio MF MT \_ \_**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [\_tipo de conteúdo MF MT \_ AAC \_ \_](mf-mt-aac-payload-type.md)                                       | 0 (opcional)                                                                                    |
| [\_indicação de \_ \_ nível de \_ perfil de áudio \_ \_ MF MT AAC](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (opcional)                                                                                 |
| [**\_alinhamento de \_ bloco de áudio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)               | 1 (opcional)                                                                                    |
| [**\_ \_ todos os exemplos do MF MT são \_ \_ independentes**](mf-mt-all-samples-independent-attribute.md)           | 0 (opcional)                                                                                    |
| [**\_taxa de \_ \_ bits média de MF MT**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (opcional)                                                                               |
| [**dados de usuário do MF \_ MT \_ \_**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} adicional |



 

## <a name="remarks"></a>Comentários

Na implementação atual, cada exemplo de entrada deve ter uma hora e uma duração válidas. Para definir o tempo de exemplo, chame [**IMFSample:: Setsampletime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Para definir a duração da amostra, chame [**IMFSample:: SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Se o tempo de amostra não for definido, o método do codificador [**IMFTransform::P rocessinput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) retornará **MF \_ E \_ nenhum \_ carimbo de \_ data/hora de amostra**. Se a duração da amostra não for definida, o método **ProcessInput** retornará **MF \_ E \_ nenhuma \_ \_ duração de amostra**.

A duração da amostra pode ser calculada da seguinte maneira:


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



em que *nAudioSamplesPerChannel* é o número de exemplos de áudio PCM por canal no buffer de entrada e *nSamplesPerSec* é a taxa de amostragem, em amostras por segundo.

> [!Note]  
> Devido a um bug na implementação atual, se a duração da amostra for definida como zero, a chamada [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) terá sucesso, mas uma chamada subsequente para [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) lançará uma exceção de divisão por zero. Para evitar esse erro, defina uma duração válida diferente de zero em cada amostra de entrada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[**Decodificador AAC**](aac-decoder.md)
</dt> <dt>

[Tipos de mídia AAC](aac-media-types.md)
</dt> <dt>

[Tipos de mídia de áudio](audio-media-types.md)
</dt> <dt>

[Suporte a MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

