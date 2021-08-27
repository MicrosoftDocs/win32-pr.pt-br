---
description: 'O Microsoft Media Foundation decodificador AAC é uma transformação Media Foundation que decodifica os seguintes perfis AAC (Codificação de Áudio Avançada) e HE-AAC (Alta Eficiência:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Decodificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1b9990965092c04b6ddc9e7b6c7b4d26cf577937
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122483102"
---
# <a name="aac-decoder"></a>Decodificador AAC

O Microsoft Media Foundation decodificador AAC é uma transformação [Media Foundation](media-foundation-transforms.md) que decodifica os seguintes perfis de AAC (Codificação de Áudio Avançada) e HE-AAC (Alta Eficiência:

-   Perfil de LC (baixa complexidade) do MPEG-2 AAC (multicanal).
-   MPEG-4 HE-AAC v1 (multicanal) com núcleo AAC-LC.
-   MPEG-4 HE-AAC v2 (estéreo) com núcleo AAC-LC.

O decodificador AAC dá suporte a fluxos AAC brutos sem nenhum headers e AAC em um fluxo de transporte de dados de áudio (ADTS).

A partir do Windows 8, o decodificador AAC também dá suporte à decodificação de fluxos de transporte de áudio MPEG-4 com latm (camada multiplex) e LOAS (camada de sincronização). Ele também pode converter um fluxo LATM/LOAS em ADTS.

## <a name="class-identifier"></a>Identificador de Classe

O CLSID (identificador de classe) do codificador AAC é **\_ CLSID CMSAACDecMFT**, definido no arquivo de header wmcodecdsp.h.

## <a name="media-types"></a>Tipos de mídia

O decodificador AAC dá suporte aos seguintes tipos de mídia.

### <a name="input-types"></a>Tipos de entrada

O decodificador AAC dá suporte aos seguintes subtipos de áudio:



| Subtype                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Cabeçalho       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | AAC bruto ou ADTS AAC.<br/> Para esse subtipo, o tipo de mídia fornece a taxa de exemplo e o número de canais antes da aplicação de ferramentas SBR (replicação de banda espectral) e PS (estéreo paramétrico), se presente. O efeito da ferramenta SBR é duplicar a taxa de amostra decodificada em relação à taxa de amostra principal do AAC-LC. O efeito da ferramenta PS é decodificar estéreo de um fluxo AAC-LC de núcleo mono canal.<br/> Esse subtipo é equivalente **a MEDIASUBTYPE_MPEG_HEAAC**, definido em wmcodecdsp.h. Consulte [GUIDs de subtipo de áudio.](audio-subtype-guids.md) <br/> A [Origem do Arquivo MPEG-4](mpeg-4-file-source.md) e o Analisador do ADTS saídam esse subtipo. <br/> | mfapi.h      |
| **MEDIASUBTYPE_RAW_AAC1** | AAC bruto. <br/> Esse subtipo é usado para AAC contido em um arquivo AVI com a marca de formato de áudio igual a WAVE_FORMAT_RAW_AAC1 (0x00FF). <br/> Para esse subtipo, o tipo de mídia fornece a taxa de exemplo e o número de canais depois que as ferramentas SBR e PS são aplicadas, se presente.<br/>                                                                                                                                                                                                                                                                                                                                                                                      | wmcodecdsp.h |



 

Para configurar o decodificador AAC, de definidos os seguintes atributos no tipo de mídia de entrada.




| Atributo | Descrição | Comentários | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. | Deve ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de áudio. | Consulte a descrição anterior para obter detalhes. | 
| <a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a> | Nível e perfil de áudio. <br /> | Opcional. Aplica-se somente a <strong>MFAudioFormat_AAC</strong>. <br /> O valor desse atributo é o <strong>campo audioProfileLevelIndication,</strong> conforme definido por ISO/IEC 14496-3. <br /> Se for desconhecido, de definido como zero ou 0xFE ("nenhum perfil de áudio especificado").<br /> | 
| <a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> | Tipo de carga.<br /> | Aplica-se somente a <strong>MFAudioFormat_AAC</strong>. O decodificador dá suporte aos seguintes tipos de carga: <br /><ul><li>0: AAC bruto. O fluxo contém raw_data_block(), conforme definido pelo MPEG-2.</li><li>1: ADTS. O fluxo contém um adts_sequence(), conforme definido pelo MPEG-2. Apenas um raw_data_block() por adts_frame() é permitido.</li><li>3: fluxo de transporte de áudio com uma LOAS (camada de sincronização) e uma latm (camada multiplex). Dos três tipos de LOAS, há suporte <strong>apenas para AudioSyncStream.</strong> A camada multiplex é <strong>AudioMuxElement,</strong>restrita a um programa de áudio e uma camada.</li></ul><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> é opcional. Se esse atributo não for especificado, o valor padrão 0 será usado, o que especifica que o fluxo contém raw_data_block elementos.<br /> | 
| <a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a> | Profundidade de bits desejada do áudio PCM decodificado. | 
| <a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a> | Especifica a atribuição de canais de áudio para posições do locutor. | Opcional. Para obter mais informações, consulte <a href="#format-constraints">Format Constraints</a>. | 
| <a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a> | Número de canais, incluindo o canal LFE (baixa frequência), se presente.<br /> | A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.<br /> | 
| <a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a> | Taxa de exemplo, em amostras por segundo.<br /> | A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.<br /> | 
| <a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a> | Informações de formato adicionais. | O valor desse atributo depende do subtipo .<br /><ul><li><strong>MFAudioFormat_AAC</strong>: contém a parte da estrutura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece após a estrutura <strong>WAVEFORMATEX</strong> (ou seja, após o <strong>membro wfx).</strong> Isso é seguido pelos dados AudioSpecificConfig(), conforme definido por ISO/IEC 14496-3.</li><li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contém os dados AudioSpecificConfig(). Esses dados devem aparecer; caso contrário, o decodificador rejeitará o tipo de mídia.</li></ul>O comprimento dos dados AudioSpecificConfig() é de 2 bytes para AAC-LC ou HE-AAC com sinalização implícita de SBR/PS. São mais de 2 bytes para HE-AAC com sinalização explícita de SBR/PS.<br /> O valor de <strong>audioObjectType</strong> conforme definido em AudioSpecificConfig() deve ser 2, indicando AAC-LC. O valor de <strong>extensionAudioObjectType</strong> deve ser 5 para SBR ou 29 para PS. <br /> | 




 

### <a name="output-types"></a>Tipos de saída

O decodificador dá suporte aos seguintes tipos de saída:




| Subtype | Descrição | 
|---------|-------------|
| <strong>MFAudioFormat_Float</strong> | Áudio de ponto flutuante IEEE. | 
| <strong>MFAudioFormat_PCM</strong> | Áudio PCM de 16 bits. | 
| <strong>MFAudioFormat_AAC</strong> | Requer Windows 8. <br /> Esse tipo de saída pode ser usado para converter um fluxo AAC no formato LOAS/LATM no formato ADTS. <br /> Para converter um fluxo LOAS/LATM em um fluxo do ADTS, de definido o tipo de entrada como <strong>MFAudioFormat_AAC</strong> com o tipo de carga 3 (LOAS). Em seguida, de definido o <strong>tipo de saída como MFAudioFormat_AAC</strong> com o tipo de carga 1 (ADTS). O decodificador reformata o conainter sem decodificar o bitstream. <br /><blockquote>[!Note]<br />O decodificador não registra <strong>MFAudioFormat_AAC</strong> como um tipo de saída. No entanto, se o aplicativo define o tipo de entrada conforme descrito, o método <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform::GetOutputAvailableType</strong></a> <strong>retorna MFAudioFormat_AAC</strong> na lista de tipos de saída disponíveis.</blockquote><br /><br /> | 




 

Se o fluxo de entrada contiver mais de dois canais, o decodificador AAC fornece duas opções para o formato de saída:

-   A mesma configuração de canal que o tipo de entrada.
-   Dobramento estéreo.

## <a name="format-constraints"></a>Restrições de formato

A taxa de amostragem de áudio decodificada deve ser uma das seguintes, depois que o SBR for aplicado (se presente):

-   8 kHz
-   11,025 kHz
-   12 kHz
-   16 kHz
-   22,05 kHz
-   24 kHz
-   32 kHz
-   44,1 kHz
-   48 kHz

Não há suporte para taxas de amostragem acima de 48 kHz.

O decodificador dá suporte a até 6 canais de áudio. Para cada configuração do locutor, o decodificador espera que os elementos sintáticos do AAC apareçam em uma determinada ordem. A tabela a seguir lista as configurações do locutor com suporte. A terceira coluna da tabela lista os elementos sintáticos esperados e sua ordem, usando a seguinte notação:

-   <SCE1>: o single_channel_element (SCE) associado ao alto-falante do front center.
-   <SCE2>: O SCE associado ao alto-falante do back center.
-   <CPE1>: o channel_pair_element (CPE) associado aos alto-falantes da frente.
-   <CPE2>: O CPE associado aos alto-falantes de fundo (ou lado)
-   <LFE>: o lfe_channel_element (LFE).

Para obter mais informações sobre esses elementos sintáticos, consulte ISO/IEC 13818-7.



| Configuração       | Máscara de Canal                                                                                                                                                              | Elementos sintáticos do AAC                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | <SCE1>                                    |
| Estéreo ou mono duplo | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**                                                                                                                     | <CPE1>                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**                                                                                        | <CPE1><SCE1>                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                                              | <CPE1><CPE2>                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**                                                                                       | <SCE1><CPE1>                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**                                                          | <SCE1><CPE1><SCE2>            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                | <SCE1><CPE1><CPE2>            |
| 3/2 + LFE           | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT** | <SCE1><CPE1><CPE2><LFE> |



 

Para o AAC bruto, cada amostra de entrada deve conter exatamente um quadro compactado AAC completo.

Para o ADTS, cada exemplo de entrada pode conter vários quadros de áudio, bem como quadros parciais, ou seja, quadros podem abranger limites de exemplo. Cada header do ADTS deve ser seguido por um quadro AAC.

O decodificador AAC não dá suporte a nenhum dos seguintes:

-   Perfil principal, Sample-Rate perfil SRS (Escalonável) ou ltP (Previsão de Longo Prazo).
-   ADIF (formato de intercâmbio de dados de áudio).
-   Fluxos de transporte LATM/LAOS.
-   Elementos de canal de acoplamento (CCEs). O decodificador ignorará quadros de áudio com CCEs.
-   AAC-LC com um tamanho de quadro de 960 amostras. Há suporte apenas para quadros de 1024 amostras.

## <a name="transform-attributes"></a>Transformar atributos

O decodificador AAC implementa o [**método IMFTransform::GetAttributes.**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) Os aplicativos podem usar esse método para obter ou definir os atributos a seguir.




| Atributo | Descrição | 
|-----------|-------------|
| <a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a> | Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo. Trate como somente leitura. | 
| <a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a> | Especifica como o decodificador reproduz áudio mono duplo. O valor padrão é <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: Saída Ch1 para os alto-falantes esquerdo e direito. <br /> Os aplicativos podem definir essa propriedade para alterar o comportamento padrão.<br /> | 
| <a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a> | O decodificador AAC não lida com alterações de formato dinâmico e deve ser liberado ou esvaziado antes que um novo tipo de mídia de entrada seja definido. Trate esse atributo como somente leitura. <br /><blockquote>[!Note]<br />O decodificador AAC relata incorretamente um valor <strong>true</strong> para esse atributo.</blockquote><br /><br /> No Windows 7, o decodificador relata incorretamente um valor <strong>true</strong> para esse atributo. No Windows 8, o decodificador <strong>relata FALSE,</strong>que é o valor correto<br /> | 




 

## <a name="example-media-types"></a>Tipos de mídia de exemplo

Aqui está um exemplo do tipo de mídia de entrada necessário para um fluxo AAC-LC de 6 canais de 48 kHz, usando uma carga bruta do AAC:



| Atributo                                                                                      | Valor                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x2a, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2a (opcional)                                                                      |



 

Os primeiros 12 bytes [**de MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspondem aos seguintes membros da estrutura [**HEAACWAVEINFO:**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo)

-   **wPayloadType** = 0 (AAC bruto)
-   **wAudioProfileLevelIndication** = 0x2a (Perfil do AAC, Nível 4)
-   **wStructType** = 0

Os dois últimos bytes [**de MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contêm o valor de AudioSpecificConfig(), conforme definido por MPEG-4.

-   AudioSpecificConfig.audioObjectType = 2 (AAC LC) (5 bits)
-   AudioSpecificConfig.samplingFrequencyIndex = 3 (4 bits)
-   AudioSpecificConfig. channelConfiguration = 6 (4 bits)
-   GASpecificConfig. frameLengthFlag = 0 (1 bit)
-   GASpecificConfig. dependsOnCoreCoder = 0 (1 bit)
-   GASpecificConfig. extensionFlag = 0 (1 bit)

Dado esse tipo de entrada, use o seguinte tipo de mídia de saída para obter o áudio PCM de ponto flutuante de 6 canais, 32 bits do decodificador:



| Atributo                                                                                    | Valor                    |
|----------------------------------------------------------------------------------------------|--------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                    | **MFMediaType_Audio**   |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                           | **MFAudioFormat_Float** |
| [**MF_MT_AUDIO_BITS_PER_SAMPLE**](mf-mt-audio-bits-per-sample-attribute.md)            | 32                       |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)      | 48000                    |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                   | 6                        |
| [**MF_MT_AUDIO_AVG_BYTES_PER_SECOND**](mf-mt-audio-avg-bytes-per-second-attribute.md) | 1152000 (opcional)       |
| [**MF_MT_AUDIO_BLOCK_ALIGNMENT**](mf-mt-audio-block-alignment-attribute.md)             | 24 (opcional)            |
| [**MF_MT_AUDIO_CHANNEL_MASK**](mf-mt-audio-channel-mask-attribute.md)                   | 0x3F (opcional)          |



 

se o suplemento de atualização de plataforma para o Windows Vista estiver instalado, o decodificador de áudio AAC estará disponível no Windows vista, mas poderá ser acessado no Windows vista somente usando o [leitor de origem](source-reader.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                                                                                                                                  |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do Server 2008 R2\]<br/>                                                                                                                                     |
| DLL<br/>                      | <dl> <dt>Msmpeg2adec.dll no Windows 7;</dt> <dt>MSAudDecMFT.dll em Windows 8</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Tipos de mídia AAC](aac-media-types.md)
</dt> <dt>

[Tipos de mídia de áudio](audio-media-types.md)
</dt> <dt>

[**Decodificador de áudio do Microsoft MPEG-1/DD/AAC**](/windows/desktop/DirectShow/microsoft-mpeg-1-dd-audio-decoder)
</dt> <dt>

[Suporte a MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> </dl>
