---
description: O codificador AAC Microsoft Media Foundation é uma transformação de Media Foundation que codifica o perfil de alta complexidade (AAC) de codificação de áudio avançado, conforme definido por ISO/IEC 13818-7 (MPEG-2 Audio parte 7).
ms.assetid: d88a8c32-c71f-4ddb-af8c-e2fb54c2322c
title: Codificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 674ad291e1cf6b56f7ffef640fade683265b62a7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465633"
---
# <a name="aac-encoder"></a>Codificador AAC

O codificador AAC Microsoft Media Foundation é uma [transformação de Media Foundation](media-foundation-transforms.md) que codifica o perfil de alta complexidade (AAC) de codificação de áudio avançado, conforme definido por ISO/IEC 13818-7 (MPEG-2 Audio parte 7).

O codificador AAC não dá suporte à codificação para outros perfis AAC, como Main, SSR ou LTP.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do codificador AAC é **CLSID \_ AACMFTEncoder**, definido no arquivo de cabeçalho wmcodecdsp. h.

## <a name="media-types"></a>Tipos de mídia

O codificador AAC dá suporte aos seguintes tipos de mídia. Você pode definir os tipos em qualquer tipo de entrada de ordem primeiro ou no tipo de saída primeiro.

### <a name="input-types"></a>Tipos de entrada

Defina os seguintes atributos no tipo de mídia de entrada.




| Atributo | Descrição | Comentários | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. | Deve ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo. | Deve ser <strong>MFAudioFormat_PCM</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Bits por amostra. | Deve ser 16. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Exemplos por segundo. | Os seguintes valores têm suporte:<ul><li>44100 (44,1 KHz)</li><li>48000 (48 KHz)</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Número de canais. | Deve ser 1 (mono) ou 2 (estéreo) ou 6 (5,1).<blockquote>[!Note]<br />o suporte para 6 canais de áudio foi introduzido com o Windows 10 e não está disponível para versões anteriores do Windows.</blockquote><br /> | 




 

Depois que o tipo de entrada é definido, o codificador deriva os seguintes valores e os adiciona ao tipo de mídia:

-   [**áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo**](mf-mt-audio-avg-bytes-per-second-attribute.md)
-   [**\_alinhamento de \_ bloco de áudio MF MT \_ \_**](mf-mt-audio-block-alignment-attribute.md)
-   [**\_taxa de \_ \_ bits média de MF MT**](mf-mt-avg-bitrate-attribute.md)

### <a name="output-types"></a>Tipos de saída

Defina os seguintes atributos no tipo de mídia de saída.




| Atributo | Descrição | Comentários | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. | Deve ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de áudio. | Deve ser <strong>MFAudioFormat_AAC</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Bits por amostra. | Deve ser 16. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Exemplos por segundo. | Deve corresponder ao tipo de entrada. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Número de canais. | Deve corresponder ao tipo de entrada. | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md"><strong>MF_MT_AUDIO_AVG_BYTES_PER_SECOND</strong></a> | Taxa de bits do fluxo AAC codificado, em bytes por segundo. | Os seguintes valores têm suporte:<ul><li>12000</li><li>16000</li><li>20000</li><li>24.000</li></ul>O valor padrão para mono e estéreo é 12000 (96 kbps).<br /> | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | O tipo de carga AAC. | Opcional. Se definido, o valor deve ser zero, indicando que o fluxo contém apenas elementos raw_data_block.<br /> Opcional. Se o atributo não for definido, o valor padrão será zero, indicando que o fluxo contém apenas elementos raw_data_block (AAC bruto). <br /> no Windows 7, se esse atributo for definido, o valor deverá ser zero.<br /> a partir do Windows 8, o valor pode ser 0 (aac bruto) ou 1 (ADTS aac). <br /> | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | O perfil de áudio AAC e o nível. | Opcional. Os seguintes valores têm suporte:<ul><li>0x29 (padrão)</li><li>0x2A</li><li>0x2B</li><li>0x2C</li><li>0x2E</li><li>0x2F</li><li>0x30</li><li>0x31</li><li>0x32</li><li>0x33</li></ul> | 


A tabela a seguir lista os valores que podem ser usados para o atributo MF_MT_AAC_PROFILE_LEVEL_INDICATION.

| Valor MF_MT_AAC_PROFILE_LEVEL_INDICATION | Perfil                           |
|------------------------------------------|-----------------------------------|
| 0x29                                     | L2 do perfil AAC                    | 
| 0x2A                                     | L4 perfil AAC                    | 
| 0x2B                                     | Perfil AAC L5                    | 
| 0x2C                                     | L2 do perfil AAC de alta eficiência | 
| 0x2E                                     | Perfil AAC de alta eficiência do v1 | 
| 0x2F                                     | Perfil AAC de alta eficiência v1 L5 | 
| 0x30                                     | Perfil AAC de Alta Eficiência v2 L2 | 
| 0x31                                     | Perfil AAC de alta eficiência v2 L3 | 
| 0x32                                     | Perfil AAC de alta eficiência v2 L4 | 
| 0x33                                     | Perfil AAC de alta eficiência v2 L5 | 

 

Depois que o tipo de saída é definido, o codificador AAC atualiza o tipo adicionando o atributo [**\_ MT \_ USER \_ DATA.**](mf-mt-user-data-attribute.md) Esse atributo contém a parte da estrutura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) que aparece após a estrutura [**WAVEFORMATEX**](/previous-versions/dd757713(v=vs.85)) (ou seja, após o **membro wfx).** Isso é seguido pelos dados AudioSpecificConfig(), conforme definido por ISO/IEC 14496-3.

Cada exemplo de saída contém um quadro AAC compactado sem nenhum header. Esse formato é equivalente ao elemento \_ raw data \_ block() definido pelo MPEG-2. O [atributo \_ MF MT \_ AAC \_ PAYLOAD \_ TYPE,](mf-mt-aac-payload-type.md) se presente no tipo de saída, deve ser definido como zero para indicar esse tipo de carga.

Cada exemplo de saída contém um quadro AAC compactado correspondente a 1024 amostras de PCM. Por exemplo, a 48 taxa de amostragem De kz, a duração de um quadro compactado é de 21,33 ms.

Se [ \_ MF MT \_ AAC \_ PAYLOAD \_ TYPE](mf-mt-aac-payload-type.md) for zero (o valor padrão), cada amostra de saída conterá um elemento raw data block() conforme definido por \_ \_ ISO/IEC 13818-7.

## <a name="example-media-types"></a>Tipos de mídia de exemplo

Aqui está um exemplo dos tipos de mídia necessários para codificar de áudio estéreo de 44,1 kHz, 160 Kbps para AAC bruto

Tipo de mídia de entrada:



| Atributo                                                                                    | Valor                  |
|----------------------------------------------------------------------------------------------|------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                                    | **Áudio MFMediaType \_** |
| [**SUBTIPO \_ MF MT \_**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [**BITS DE \_ ÁUDIO MT \_ MT \_ POR \_ \_ EXEMPLO**](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [**AMOSTRAS \_ DE ÁUDIO MT \_ \_ MT POR \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)      | 44100                  |
| [**CANAIS NUM DE ÁUDIO \_ MF MT \_ \_ \_**](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [**BYTES MF \_ MT \_ AUDIO \_ AVG \_ POR \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 176400 (opcional)      |
| [**ALINHAMENTO DO \_ BLOCO DE ÁUDIO MT \_ \_ \_ MT**](mf-mt-audio-block-alignment-attribute.md)             | 4 (opcional)           |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md)         | 1 (opcional)           |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                  | 1411200 (opcional)     |
| [**EXEMPLOS \_ DE TAMANHO FIXO do MT MF \_ \_ \_**](mf-mt-fixed-size-samples-attribute.md)                   | 1 (opcional)           |



 

Tipo de mídia de saída:



| Atributo                                                                                      | Valor                                                                                           |
|------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------|
| [**MF \_ MT \_ MAJOR \_ TYPE**](mf-mt-major-type-attribute.md)                                      | **Áudio MFMediaType \_**                                                                          |
| [**SUBTIPO \_ MF MT \_**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat \_ AAC**                                                                          |
| [**BITS DE \_ ÁUDIO MT \_ MT \_ POR \_ \_ EXEMPLO**](mf-mt-audio-bits-per-sample-attribute.md)              | 16                                                                                              |
| [**AMOSTRAS \_ DE ÁUDIO MT \_ \_ MT POR \_ \_ SEGUNDO**](mf-mt-audio-samples-per-second-attribute.md)        | 44100                                                                                           |
| [**CANAIS NUM DE ÁUDIO \_ MF MT \_ \_ \_**](mf-mt-audio-num-channels-attribute.md)                     | 2                                                                                               |
| [**BYTES MF \_ MT \_ AUDIO \_ AVG \_ POR \_ \_ SEGUNDO**](mf-mt-audio-avg-bytes-per-second-attribute.md)   | 20000                                                                                           |
| [TIPO \_ DE CARGA \_ AAC MT MT \_ \_](mf-mt-aac-payload-type.md)                                       | 0 (opcional)                                                                                    |
| [MF \_ MT \_ AAC \_ AUDIO \_ PROFILE \_ LEVEL \_ INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x29 (opcional)                                                                                 |
| [**ALINHAMENTO DO \_ BLOCO DE ÁUDIO MT \_ \_ \_ MT**](mf-mt-audio-block-alignment-attribute.md)               | 1 (opcional)                                                                                    |
| [**MF \_ MT \_ ALL \_ SAMPLES \_ INDEPENDENT**](mf-mt-all-samples-independent-attribute.md)           | 0 (opcional)                                                                                    |
| [**MF \_ MT \_ AVG \_ BITRATE**](mf-mt-avg-bitrate-attribute.md)                                    | 160000 (opcional)                                                                               |
| [**MF \_ MT \_ USER \_ DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x29, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x12, 0x10} (opcional) |



 

## <a name="remarks"></a>Comentários

Na implementação atual, cada exemplo de entrada deve ter um tempo e uma duração válidos. Para definir o tempo de exemplo, chame [**IMFSample::SetSampleTime**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampletime). Para definir a duração do exemplo, chame [**IMFSample::SetSampleDuration**](/windows/desktop/api/mfobjects/nf-mfobjects-imfsample-setsampleduration).

Se o tempo de exemplo não for definido, o método [**IMFTransform::P rocessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) do codificador retornará **MF \_ E NO \_ SAMPLE \_ \_ TIMESTAMP**. Se a duração da amostra não for definida, o **método ProcessInput** retornará **MF \_ E NO \_ SAMPLE \_ \_ DURATION**.

A duração da amostra pode ser calculada da seguinte forma:


```C++
LONGLONG hnsSampleDuration = 
    ( nAudioSamplesPerChannel * (LONGLONG)10000000 )/nSamplesPerSec;
```



em *que nAudioSamplesPerChannel* é o número de amostras de áudio PCM por canal no buffer de entrada e *nSamplesPerSec* é a taxa de amostragem, em amostras por segundo.

> [!Note]  
> Devido a um bug na implementação atual, se a duração da amostra for definida como zero, a chamada [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput) terá êxito, mas uma chamada subsequente para [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) lançará uma exceção de divisão por zero. Para evitar esse erro, de definir uma duração não zero válida em cada exemplo de entrada.

 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho do Server 2008 R2 \[\]<br/>                                 |
| DLL<br/>                      | <dl> <dt>Mfaacenc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> <dt>

[**Decodificador AAC**](aac-decoder.md)
</dt> <dt>

[Tipos de mídia do AAC](aac-media-types.md)
</dt> <dt>

[Tipos de mídia de áudio](audio-media-types.md)
</dt> <dt>

[Suporte ao MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>

 

