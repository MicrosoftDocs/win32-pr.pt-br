---
description: 'O decodificador AAC Microsoft Media Foundation é uma transformação Media Foundation que decodifica os seguintes perfis de AAC (codificação de áudio avançada) e AAC (HE-AAC) de alta eficiência:'
ms.assetid: 036fb0ee-8165-41a3-b41a-2e9bf035a6a6
title: Decodificador AAC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 82dde090dee98cddce9658366bde593b5fc779d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105784677"
---
# <a name="aac-decoder"></a>Decodificador AAC

O decodificador AAC Microsoft Media Foundation é uma [transformação Media Foundation](media-foundation-transforms.md) que decodifica os seguintes perfis de AAC (codificação de áudio avançada) e AAC (HE-AAC) de alta eficiência:

-   Perfil MPEG-2 AAC de baixa complexidade (LC) (multicanal).
-   MPEG-4 HE-AAC V1 (multicanal) com núcleo AAC-LC.
-   MPEG-4 HE-AAC v2 (estéreo) com núcleo AAC-LC.

O decodificador AAC dá suporte a fluxos AAC brutos sem cabeçalhos e AAC em um fluxo de transporte de dados de áudio (ADTS).

A partir do Windows 8, o decodificador AAC também dá suporte à decodificação de fluxos de transporte de áudio MPEG-4 com uma camada de multiplexação (LATM) e uma camada de sincronização (LOAS). Ele também pode converter um fluxo LATM/LOAS em ADTS.

## <a name="media-types"></a>Tipos de mídia

O decodificador AAC dá suporte aos seguintes tipos de mídia.

### <a name="input-types"></a>Tipos de entrada

O decodificador AAC dá suporte aos seguintes subtipos de áudio:



| Subtype                     | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   | Cabeçalho       |
|-----------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------|
| **MFAudioFormat_AAC**      | AAC bruto ou ADTS.<br/> Para esse subtipo, o tipo de mídia fornece a taxa de amostra e o número de canais antes da aplicação de ferramentas de Spectral Band Replication (SBR) e de estéreo paramétrica (PS), se presente. O efeito da ferramenta SBR é dobrar a taxa de amostragem decodificada em relação à taxa de amostra AAC-LC principal. O efeito da ferramenta PS é decodificar o estéreo de um fluxo básico AAC-LC do canal mono.<br/> Esse subtipo é equivalente a **MEDIASUBTYPE_MPEG_HEAAC**, definido em wmcodecdsp. h. Consulte [GUIDs de subtipo de áudio](audio-subtype-guids.md). <br/> A [origem do arquivo MPEG-4](mpeg-4-file-source.md) e o ANALISAdor ADTS geram esse subtipo. <br/> | mfapi. h      |
| **MEDIASUBTYPE_RAW_AAC1** | AAC bruto. <br/> Esse subtipo é usado para AAC contido em um arquivo AVI com a marca de formato de áudio igual a WAVE_FORMAT_RAW_AAC1 (0x00FF). <br/> Para esse subtipo, o tipo de mídia fornece a taxa de amostra e o número de canais depois que as ferramentas SBR e PS são aplicadas, se presentes.<br/>                                                                                                                                                                                                                                                                                                                                                                                      | wmcodecdsp. h |



 

Para configurar o decodificador AAC, defina os seguintes atributos no tipo de mídia de entrada.



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
<td>Consulte a descrição anterior para obter detalhes.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-aac-audio-profile-level-indication.md">MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION</a></td>
<td>Perfil de áudio e nível. <br/></td>
<td>Opcional. Aplica-se somente a <strong>MFAudioFormat_AAC</strong>. <br/> O valor desse atributo é o campo <strong>audioProfileLevelIndication</strong> , conforme definido por ISO/IEC 14496-3. <br/> Se for desconhecido, defina como zero ou 0xFE ( &quot; nenhum perfil de áudio especificado &quot; ).<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a></td>
<td>Tipo de carga.<br/></td>
<td>Aplica-se somente a <strong>MFAudioFormat_AAC</strong>. O decodificador dá suporte aos seguintes tipos de carga: <br/>
<ul>
<li>0: AAC bruto. O fluxo contém apenas elementos raw_data_block (), conforme definido por MPEG-2.</li>
<li>1: ADTS. O fluxo contém um adts_sequence (), conforme definido por MPEG-2. Somente um raw_data_block () por adts_frame () é permitido.</li>
<li>3: fluxo de transporte de áudio com uma camada de sincronização (LOAS) e uma camada de multiplexação (LATM). Dos três tipos de LOAS, há suporte apenas para <strong>AudioSyncStream</strong> . A camada multiplex é <strong>AudioMuxElement</strong>, restrita a um programa de áudio e uma camada.</li>
</ul>
<a href="mf-mt-aac-payload-type.md">MF_MT_AAC_PAYLOAD_TYPE</a> é opcional. Se esse atributo não for especificado, o valor padrão 0 será usado, o que especificará que o fluxo contém apenas elementos de raw_data_block.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-bits-per-sample-attribute.md"><strong>MF_MT_AUDIO_BITS_PER_SAMPLE</strong></a></td>
<td>Profundidade de bits desejada do áudio PCM decodificado.</td>

</tr>
<tr class="even">
<td><a href="mf-mt-audio-channel-mask-attribute.md"><strong>MF_MT_AUDIO_CHANNEL_MASK</strong></a></td>
<td>Especifica a atribuição de canais de áudio a posições do orador.</td>
<td>Opcional. Para obter mais informações, consulte <a href="#format-constraints">Format Constraints</a>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-num-channels-attribute.md"><strong>MF_MT_AUDIO_NUM_CHANNELS</strong></a></td>
<td>Número de canais, incluindo o canal de baixa frequência (LFE), se presente.<br/></td>
<td>A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.<br/></td>
</tr>
<tr class="even">
<td><a href="mf-mt-audio-samples-per-second-attribute.md"><strong>MF_MT_AUDIO_SAMPLES_PER_SECOND</strong></a></td>
<td>Taxa de amostragem, em amostras por segundo.<br/></td>
<td>A interpretação desse valor depende do subtipo de mídia, conforme descrito anteriormente.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-user-data-attribute.md"><strong>MF_MT_USER_DATA</strong></a></td>
<td>Informações de formato adicionais.</td>
<td>O valor desse atributo depende do subtipo.<br/>
<ul>
<li><strong>MFAudioFormat_AAC</strong>: contém a parte da estrutura <a href="/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo"><strong>HEAACWAVEINFO</strong></a> que aparece após a estrutura <strong>WAVEFORMATEX</strong> (ou seja, após o membro <strong>WFX</strong> ). Isso é seguido pelos dados de AudioSpecificConfig (), conforme definido por ISO/IEC 14496-3.</li>
<li><strong>MEDIASUBTYPE_RAW_AAC1</strong>: contém os dados de AudioSpecificConfig (). Esses dados devem aparecer; caso contrário, o decodificador rejeitará o tipo de mídia.</li>
</ul>
O comprimento dos dados de AudioSpecificConfig () é de 2 bytes para AAC-LC ou HE-AAC com sinalização implícita de SBR/PS. É mais de 2 bytes para HE-AAC com sinalização explícita de SBR/PS.<br/> O valor de <strong>audioObjectType</strong> conforme definido em AudioSpecificConfig () deve ser 2, indicando AAC-LC. O valor de <strong>extensionAudioObjectType</strong> deve ser 5 para SBR ou 29 para PS. <br/></td>
</tr>
</tbody>
</table>



 

### <a name="output-types"></a>Tipos de saída

O decodificador dá suporte aos seguintes tipos de saída:



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Subtype</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>MFAudioFormat_Float</strong></td>
<td>Áudio de ponto flutuante do IEEE.</td>
</tr>
<tr class="even">
<td><strong>MFAudioFormat_PCM</strong></td>
<td>áudio PCM de 16 bits.</td>
</tr>
<tr class="odd">
<td><strong>MFAudioFormat_AAC</strong></td>
<td>Requer o Windows 8. <br/> Esse tipo de saída pode ser usado para converter um fluxo AAC no formato LOAS/LATM no formato ADTS. <br/> Para converter um fluxo de LOAS/LATM em um fluxo de ADTS, defina o tipo de entrada como <strong>MFAudioFormat_AAC</strong> com o tipo de carga 3 (loas). Em seguida, defina o tipo de saída como <strong>MFAudioFormat_AAC</strong> com o tipo de carga 1 (ADTS). O decodificador reformatará o conainter sem decodificar o fragmentado. <br/>
<blockquote>
[!Note]<br />
O decodificador não registra <strong>MFAudioFormat_AAC</strong> como um tipo de saída. No entanto, se o aplicativo definir o tipo de entrada conforme descrito, o método <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype"><strong>IMFTransform:: GetOutputAvailableType</strong></a> retornará <strong>MFAudioFormat_AAC</strong> na lista de tipos de saída disponíveis.
</blockquote>
<br/> <br/></td>
</tr>
</tbody>
</table>



 

Se o fluxo de entrada contiver mais de dois canais, o decodificador AAC fornecerá duas opções para o formato de saída:

-   A mesma configuração de canal que o tipo de entrada.
-   Dobra estéreo.

## <a name="format-constraints"></a>Restrições de formato

A taxa de amostragem de áudio decodificada deve ser uma das seguintes, após a aplicação de SBR (se houver):

-   8 kHz
-   11, 25 kHz
-   12 kHz
-   16 kHz
-   22, 5 kHz
-   24 kHz
-   32 kHz
-   44,1 kHz
-   48 kHz

As taxas de amostragem acima de 48 kHz não são suportadas.

O decodificador dá suporte a até 6 canais de áudio. Para cada configuração de palestrante, o decodificador espera que os elementos AAC sintáticas apareçam em uma determinada ordem. A tabela a seguir lista as configurações de alto-falante com suporte. A terceira coluna da tabela lista os elementos sintáticas esperados e sua ordem, usando a seguinte notação:

-   <SCE1>: O single_channel_element (SCE) associado ao orador do front Center.
-   <SCE2>: O SCE associado ao viva-voz do centro.
-   <CPE1>: O channel_pair_element (CPE) associado aos alto-falantes da frente.
-   <CPE2>: A CPE associada aos alto-falantes de volta (ou lado)
-   <LFE>: O lfe_channel_element (LFE).

Para obter mais informações sobre esses elementos sintáticos, consulte ISO/IEC 13818-7.



| Configuração       | Máscara de canal                                                                                                                                                              | Elementos de sintaxe AAC                          |
|---------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------|
| Mono                | **SPEAKER_FRONT_CENTER**                                                                                                                                                | <SCE1>                                    |
| Estéreo ou mono duplo | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT**                                                                                                                     | <CPE1>                                    |
| 2/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_CENTER**                                                                                        | <CPE1><SCE1>                        |
| 2/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                                              | <CPE1><CPE2>                        |
| 3/0                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER**                                                                                       | <SCE1><CPE1>                        |
| 3/1                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_CENTER**                                                          | <SCE1><CPE1><SCE2>            |
| 3/2                 | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT**                                | <SCE1><CPE1><CPE2>            |
| 3/2 + LFE           | **SPEAKER_FRONT_LEFT** \| **SPEAKER_FRONT_RIGHT** \| **SPEAKER_FRONT_CENTER** \| **SPEAKER_LOW_FREQUENCY** \| **SPEAKER_BACK_LEFT** \| **SPEAKER_BACK_RIGHT** | <SCE1><CPE1><CPE2><LFE> |



 

Para AAC bruto, cada amostra de entrada deve conter exatamente um quadro compactado AAC completo.

Para ADTS, cada amostra de entrada pode conter vários quadros de áudio, bem como os quadros parciais, os quadros podem abranger os limites de amostra. Cada cabeçalho ADTS deve ser seguido por um quadro AAC.

O decodificador AAC não oferece suporte a nenhum dos seguintes itens:

-   Perfil principal, perfil do SRS (Sample-Rate escalonável) ou perfil de previsão de longo prazo (LTP).
-   Formato de intercâmbio de dados de áudio (ADIF).
-   Fluxos de transporte LATM/LAOS.
-   Elementos de canal de acoplamento (CCEs). O decodificador irá ignorar os quadros de áudio com CCEs.
-   AAC-LC com um tamanho de quadro de 960-amostra. Somente há suporte para quadros de exemplo 1024.

## <a name="transform-attributes"></a>Atributos de transformação

O decodificador AAC implementa o método [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) . Os aplicativos podem usar esse método para obter ou definir os atributos a seguir.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Atributo</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmono-property"><strong>CODECAPI_AVDecAudioDualMono</strong></a></td>
<td>Especifica se o áudio de 2 canais é codificado como estéreo ou mono duplo. Tratar como somente leitura.</td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avdecaudiodualmonorepromode-property"><strong>CODECAPI_AVDecAudioDualMonoReproMode</strong></a></td>
<td>Especifica como o decodificador Reproduz áudio mono duplo. O valor padrão é <strong>eAVDecAudioDualMonoReproMode_LEFT_MONO</strong>: saída CH1 para os alto-falantes esquerdo e direito. <br/> Os aplicativos podem definir essa propriedade para alterar o comportamento padrão.<br/></td>
</tr>
<tr class="odd">
<td><a href="mft-support-dynamic-format-change-attribute.md"><strong>MFT_SUPPORT_DYNAMIC_FORMAT_CHANGE</strong></a></td>
<td>O decodificador AAC não manipula alterações de formato dinâmico e deve ser liberado ou esgotado antes que um novo tipo de mídia de entrada seja definido. Trate este atributo como somente leitura. <br/>
<blockquote>
[!Note]<br />
O decodificador AAC relata incorretamente um valor de <strong>true</strong> para este atributo.
</blockquote>
<br/> <br/> No Windows 7, o decodificador relata incorretamente um valor de <strong>true</strong> para esse atributo. No Windows 8, o decodificador relata <strong>false</strong>, que é o valor correto<br/></td>
</tr>
</tbody>
</table>



 

## <a name="example-media-types"></a>Exemplos de tipos de mídia

Aqui está um exemplo do tipo de mídia de entrada necessário para um fluxo AAC-LC de 6 canais, 48-kHz, usando uma carga AAC bruta:



| Atributo                                                                                      | Valor                                                                                |
|------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [**MF_MT_MAJOR_TYPE**](mf-mt-major-type-attribute.md)                                      | **MFMediaType_Audio**                                                               |
| [**MF_MT_SUBTYPE**](mf-mt-subtype-attribute.md)                                             | **MFAudioFormat_AAC**                                                               |
| [**MF_MT_AUDIO_SAMPLES_PER_SECOND**](mf-mt-audio-samples-per-second-attribute.md)        | 48000                                                                                |
| [**MF_MT_AUDIO_NUM_CHANNELS**](mf-mt-audio-num-channels-attribute.md)                     | 6                                                                                    |
| [MF_MT_AAC_PAYLOAD_TYPE](mf-mt-aac-payload-type.md)                                       | 0                                                                                    |
| [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md)                                        | {0x00, 0x00, 0x2A, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x11, 0xb0} |
| [MF_MT_AAC_AUDIO_PROFILE_LEVEL_INDICATION](mf-mt-aac-audio-profile-level-indication.md) | 0x2A (opcional)                                                                      |



 

Os primeiros 12 bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) correspondem aos seguintes membros da estrutura [**HEAACWAVEINFO**](/windows/desktop/api/mmreg/ns-mmreg-heaacwaveinfo) :

-   **wPayloadType** = 0 (AAC bruto)
-   **wAudioProfileLevelIndication** = 0X2a (perfil AAC, nível 4)
-   **wStructType** = 0

Os dois últimos bytes de [**MF_MT_USER_DATA**](mf-mt-user-data-attribute.md) contêm o valor de AudioSpecificConfig (), conforme definido pelo MPEG-4.

-   AudioSpecificConfig. audioObjectType = 2 (AAC LC) (5 bits)
-   AudioSpecificConfig. samplingFrequencyIndex = 3 (4 bits)
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



 

Se o suplemento de atualização de plataforma para Windows Vista estiver instalado, o decodificador de áudio AAC estará disponível no Windows Vista, mas poderá ser acessado somente no Windows Vista usando o [leitor de origem](source-reader.md).

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 7\]<br/>                                                                                                                                                  |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008 R2\]<br/>                                                                                                                                     |
| DLL<br/>                      | <dl> <dt>Msmpeg2adec.dll no Windows 7; </dt> <dt>MSAudDecMFT.dll no Windows 8</dt> </dl> |



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
