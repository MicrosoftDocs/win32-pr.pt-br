---
description: O codificador de áudio Dolby é uma transformação Media Foundation (MFT) que codifica áudio mono ou estéreo para Dolby Digital, também chamado de Dolby AC-3.
ms.assetid: CBC31132-046C-4CD7-9DBA-20A9C666FB43
title: Codificador de Áudio Digital Dolby
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84d14a434481a94021617f04e4cb9e10329ad20a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483092"
---
# <a name="dolby-digital-audio-encoder"></a>Codificador de Áudio Digital Dolby

O codificador de áudio Dolby é uma [transformação Media Foundation](media-foundation-transforms.md) (MFT) que codifica áudio mono ou estéreo para Dolby Digital, também chamado de Dolby AC-3. O codificador não dá suporte à entrada de vários canais, como a configuração de canal 5.1.

> [!IMPORTANT]
> Para versões do Windows anteriores ao Windows 8, a implementação da Microsoft da tecnologia Dolby Digital é restrita nos termos do programa de licenciamento do Dolby Digital a ser usado pelos aplicativos da Microsoft.

 

Para obter mais informações sobre o áudio do Dolby Digital, consulte o documento ATSC (Advanced Tv Systems *Committee) (AC-3, E-AC-3) Revision B*.

## <a name="class-identifier"></a>Identificador de Classe

O CLSID (identificador de classe) do codificador de áudio Dolby é **\_ CLSID CMSDolbyDigitalEncMFT**, definido no arquivo de header wmcodecdsp.h.

## <a name="output-types"></a>Tipos de saída

O tipo de saída deve ser definido primeiro, antes do tipo de entrada. A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de saída.




| Atributo | Descrição | Comentários | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principal. | Obrigatórios. Deve ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Subtipo de áudio. | Obrigatórios. Deve ser <strong>MFAudioFormat_Dolby_AC3</strong>. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Exemplos por segundo. | Obrigatórios. Os seguintes valores têm suporte:<ul><li>32000</li><li>44100</li><li>48000</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Número de canais. | Obrigatórios. Deve ser 1 (mono) ou 2 (estéreo). | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Especifica a atribuição de canais de áudio para posições do locutor. | Opcional. Se definido, o valor deverá ser 0x3 estéreo (canais frontal esquerdo e direito) ou 0x4 para mono (canal central frontal). | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Taxa de bits do fluxo AC-3 codificado, em bytes por segundo. | Opcional. Consulte Comentários para ver os valores válidos. Se esse atributo não estiver definido, o codificador usará uma taxa de bits padrão, conforme descrito em Comentários. | 




 

Se os atributos opcionais não estão definidos, o codificador os adiciona ao tipo de mídia depois que o tipo é definido.

## <a name="input-types"></a>Tipos de entrada

A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de entrada.




| Atributo | Descrição | Comentários | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principal. | Obrigatórios. Deve ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Subtipo de áudio. | Obrigatórios. Deve ser <strong>MFAudioFormat_PCM</strong> ou <strong>MFAudioFormat_Float</strong>. | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md">MF_MT_AUDIO_BITS_PER_SAMPLE</a> | Número de bits por amostra de áudio. | Obrigatórios. O valor deverá ser 16 se o subtipo for <strong>MFAudioFormat_PCM</strong>ou 32 se o subtipo for <strong>MFAudioFormat_Float</strong>. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Exemplos por segundo. | Obrigatórios. Deve corresponder ao tipo de saída. | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Número de canais. | Obrigatórios. Deve corresponder ao tipo de saída. | 
| <a href="mf-mt-audio-block-alignment-attribute.md">MF_MT_AUDIO_BLOCK_ALIGNMENT</a> | Alinhamento de bloco, em bytes. | Obrigatórios. Calcule o valor da seguinte forma:<ul><li><strong>MFAudioFormat_PCM:</strong>número de canais × 2.</li><li><strong>MFAudioFormat_Float:</strong>número de canais × 4.</li></ul> | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Taxa de bits do fluxo AC3 codificado, em bytes por segundo. | Obrigatórios. Deve ser igual ao alinhamento de × amostras por segundo. | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Especifica a atribuição de canais de áudio para posições do locutor. | Opcional. Se definido, o valor deverá corresponder ao tipo de saída. | 
| <a href="mf-mt-audio-valid-bits-per-sample-attribute.md">MF_MT_AUDIO_VALID_BITS_PER_SAMPLE</a> | Número de bits válidos de dados de áudio em cada amostra de áudio. | Opcional. Se definido, o valor deverá ser idêntico <a href="mf-mt-audio-bits-per-sample-attribute.md">ao MF_MT_AUDIO_BITS_PER_SAMPLE</a>. | 




 

O codificador não dá suporte à conversão de taxa de amostra ou conversão estéreo/mono.

## <a name="remarks"></a>Comentários

Cada quadro de áudio do Dolby AC-3 contém 1536 amostras de áudio por canal. No entanto, cada buffer de entrada para o codificador pode conter qualquer número de exemplos de PCM. O tamanho de cada buffer de entrada deve ser um múltiplo do alinhamento do bloco. O codificador armazena em cache amostras de entrada até ter o suficiente para 1536 amostras de áudio por canal; em que ponto o codificador embute um quadro AC-3.

Cada buffer de saída contém um quadro AC-3 bruto. A duração é equivalente à duração de 1536 amostras de PCM na taxa de amostragem atual (32 msec) a 48 kHz de taxa de amostragem, 34,83 msec a 44,1 kHz e 48 msec a 32 kHz). O tamanho de cada buffer de saída depende da taxa de bits e da taxa de exemplo.

Para especificar a taxa de bits de codificação, de definir o atributo [ \_ MF \_ MT AUDIO \_ AVG \_ BYTES PER \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) no tipo de saída. A tabela a seguir mostra a relação entre a taxa de bits de codificação e BYTES \_ \_ \_ MT AUDIO AVG POR SEGUNDO do \_ \_ \_ MF.



| Taxa de bits (kbps) | [BYTES MF \_ MT \_ AUDIO \_ AVG \_ POR \_ \_ SEGUNDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | Comentários                                                 |
|-----------------|------------------------------------------------------------------------------------------|---------------------------------------------------------|
| 64              | 8000                                                                                     | Somente Mono.                                              |
| 80              | 10000                                                                                    | Somente Mono.                                              |
| 96              | 12000                                                                                    | Somente Mono.                                              |
| 112             | 14000                                                                                    | Somente Mono.                                              |
| 128             | 16000                                                                                    | Mono ou estéreo.                                         |
| 160             | 20000                                                                                    | Mono ou estéreo.                                         |
| 192             | 24.000                                                                                    | Mono ou estéreo. Essa é a configuração padrão para mono.   |
| 224             | 28000                                                                                    | Mono ou estéreo.                                         |
| 256             | 32000                                                                                    | Mono ou estéreo. Essa é a configuração padrão para estéreo. |
| 320             | 40000                                                                                    | Somente estéreo.                                            |
| 384             | 48000                                                                                    | Somente estéreo.                                            |
| 448             | 56000                                                                                    | Somente estéreo.                                            |



 

A taxa de bits de codificação padrão é definida em 256 kbps para estéreo e 192 kbps para mono. As configurações padrão são refletidas nos tipos de mídia retornados pelo método [**IMFTransform::GetOutputAvailableType do**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) codificador.

### <a name="example-media-types"></a>Tipos de mídia de exemplo

Aqui está um exemplo dos tipos de mídia necessários para codificar o PCM inteiro de 16 bits, áudio estéreo de 48 kHz na taxa de bits padrão de 256 kbps.

Tipo de mídia de saída:

| Atributo                                                                           | Valor                         |
|-------------------------------------------------------------------------------------|-------------------------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md)                               | **Áudio MFMediaType \_**        |
| [SUBTIPO \_ MF MT \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ Dolby \_ AC3** |
| [AMOSTRAS \_ DE ÁUDIO MT \_ \_ MT POR \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md) | 48000                         |
| [CANAIS NUM DE ÁUDIO \_ MF MT \_ \_ \_](mf-mt-audio-num-channels-attribute.md)              | 2                             |



 

Tipo de mídia de entrada:

| Atributo                                                                                | Valor                  |
|------------------------------------------------------------------------------------------|------------------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md)                                    | **Áudio MFMediaType \_** |
| [SUBTIPO \_ MF MT \_](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat \_ PCM** |
| [BITS DE \_ ÁUDIO MT \_ MT \_ POR \_ \_ EXEMPLO](mf-mt-audio-bits-per-sample-attribute.md)            | 16                     |
| [AMOSTRAS \_ DE ÁUDIO MT \_ \_ MT POR \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md)      | 48000                  |
| [CANAIS NUM DE ÁUDIO \_ MF MT \_ \_ \_](mf-mt-audio-num-channels-attribute.md)                   | 2                      |
| [ALINHAMENTO DO \_ BLOCO DE ÁUDIO MT \_ \_ \_ MT](mf-mt-audio-block-alignment-attribute.md)             | 4                      |
| [BYTES MF \_ MT \_ AUDIO \_ AVG \_ POR \_ \_ SEGUNDO](mf-mt-audio-avg-bytes-per-second-attribute.md) | 192000                 |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 aplicativos UWP de aplicativos da área \| de trabalho\]<br/>                                       |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                               |
| DLL<br/>                      | <dl> <dt>Msac3enc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> </dl>

 

 




