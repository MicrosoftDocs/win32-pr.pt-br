---
description: O codificador de áudio Microsoft Media Foundation MPEG-2 é uma transformação de Media Foundation que codifica áudio mono ou estéreo para áudio MPEG-1 (ISO/IEC 11172-3) ou áudio MPEG-2 (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Codificador de áudio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c75956f55dfa22034b27465082ced0888fbe03b
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122475532"
---
# <a name="mpeg-2-audio-encoder"></a>Codificador de áudio MPEG-2

O codificador de áudio Microsoft Media Foundation MPEG-2 é uma transformação de [Media Foundation](media-foundation-transforms.md) que codifica áudio mono ou estéreo para áudio MPEG-1 (ISO/IEC 11172-3) ou áudio MPEG-2 (ISO/IEC 13818-3).

O codificador dá suporte ao áudio de Camada 1 e Camada 2. Ele não dá suporte MPEG-Layer áudio 3 (MP3). Para MPEG-2, o codificador dá suporte à parte de LSF (Frequências de Amostragem Baixas) do áudio MPEG-2. Ele não dá suporte a extensões multicanal. O MFT cria um fluxo elementar MPEG. Ele não pode gerar fluxos elementares em pacotes, fluxos de programas ou fluxos de transporte.

## <a name="class-identifier"></a>Identificador de Classe

O CLSID (identificador de classe) do codificador de áudio MEPG-2 é **CLSID \_ CMPEG2AudioEncoderMFT**, definido no arquivo de header wmcodecdsp.h.

## <a name="output-types"></a>Tipos de saída

O tipo de saída deve ser definido primeiro, antes do tipo de entrada. A tabela a seguir lista os atributos obrigatórios e opcionais para o tipo de mídia de saída.




| Atributo | Descrição | Comentários | 
|-----------|-------------|---------|
| <a href="mf-mt-major-type-attribute.md">MF_MT_MAJOR_TYPE</a> | Tipo principal. | Obrigatórios. Deve ser <strong>MFMediaType_Audio</strong>. | 
| <a href="mf-mt-subtype-attribute.md">MF_MT_SUBTYPE</a> | Subtipo de áudio. | Obrigatórios. Deve ser <strong>MFAudioFormat_MPEG</strong>. Esse subtipo é usado para áudio MPEG-1 e MPEG-2. | 
| <a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a> | Exemplos por segundo. | Obrigatórios. Os seguintes valores têm suporte para MPEG-1 e MPEG-2:<ul><li>32000</li><li>44100</li><li>48000</li></ul>Além disso, os seguintes valores têm suporte para MPEG-2 LSF: <br /><ul><li>16000</li><li>22050</li><li>24.000</li></ul> | 
| <a href="mf-mt-audio-num-channels-attribute.md">MF_MT_AUDIO_NUM_CHANNELS</a> | Número de canais. | Obrigatórios. Deve ser 1 (mono) ou 2 (estéreo). | 
| <a href="mf-mt-audio-channel-mask-attribute.md">MF_MT_AUDIO_CHANNEL_MASK</a> | Especifica a atribuição de canais de áudio para posições do locutor. | Opcional. Se definido, o valor deverá ser 0x3 estéreo (canais frontal esquerdo e direito) ou 0x4 para mono (canal central frontal). | 
| <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> | Taxa de bits do fluxo MPEG codificado, em bytes por segundo. | Opcional.<br /> As especificações ISO/IEC 11172-3 e ISO/IEC 13818-3 (LSF) definem várias taxas de bits, dependendo da taxa de amostragem, do número de canais e da camada de áudio (1 ou 2). <br /> O codificador assume como padrão o áudio da Camada 2. Se o <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> atributo não estiver definido, o codificador usará as seguintes taxas de bits padrão:<br /><ul><li>MPEG-1 estéreo: 224.000 bits por segundo (bps) = 28.000 bytes por segundo.</li><li>MPEG-1 mono: 192.000 bps = 24.000 bytes por segundo.</li><li>MPEG-2 LSF, mono ou estéreo: 160.000 bps = 20.000 bytes por segundo.</li></ul>Esse atributo pode ser definido como outros valores. Se o valor não for válido de acordo com as especificações do MPEG, o MFT rejeitará o tipo de mídia.<br /> Você também pode definir a taxa de bits usando a interface <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI.</strong></a> Consulte Comentários para obter mais informações.<br /> | 




 

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




 

O codificador não dá suporte à conversão de taxa de amostra ou conversão estéreo/mono. Se os atributos opcionais não estão definidos, o codificador os adiciona ao tipo de mídia depois que o tipo é definido.

## <a name="codec-properties"></a>Propriedades do Codec

O codificador dá suporte às propriedades a seguir por meio da interface [**ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi)



| Propriedade                                                                                | Descrição                                                                                      | Valor padrão                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)               | Especifica a taxa de bits codificada média, em bits por segundo.                                      | Conforme descrito para o [atributo \_ MF \_ AUDIO \_ AVG BYTES PER \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) no tipo de mídia de saída.                      |
| [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md)                       | Especifica o modo de codificação de áudio MPEG.                                                          | Estéreo para áudio de 2 canais ou canal único para áudio de 1 canal.<br/> Para áudio de dois canais, o codificador também dá suporte a canal duplo e estéreo conjunto.<br/> |
| [CODECAPI \_ AVEncMPACopyright](../directshow/avencmpacopyright-property.md)                         | Especifica se o bit de direitos autorais deve ser definido no fluxo de áudio MPEG.                             | Sem direitos autorais.                                                                                                                                                          |
| [CODECAPI \_ AVEncMPAEmphasisType](../directshow/avencmpaemphasistype-property.md)                   | Especifica o tipo de filtro de des ênfase que deve ser usado quando o fluxo codificado é decodificado. | Nenhuma ênfase especificada.                                                                                                                                                 |
| [AVEncMPAEnableRedundancyProtection](../directshow/avencmpaenableredundancyprotection-property.md) | Especifica se uma CRC (verificação de redundância cíclica) deve ser acrescentada ao header do quadro.                    | Uma verificação CRC é escrita no fluxo de bits.                                                                                                                           |
| [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md)                                 | Especifica a camada de áudio MPEG.                                                                  | Áudio de camada 2.                                                                                                                                                         |
| [CODECAPI \_ AVEncMPAOriginalBitstream](../directshow/avencmpaoriginalbitstream-property.md)         | Especifica se deve ser definido para o bit original no fluxo de áudio MPEG.                          | O bit "Original" está desligado.                                                                                                                                                 |
| [CODECAPI \_ AVEncMPAPrivateUserBit](../directshow/avencmpaprivateuserbit-property.md)               | Especifica se o bit do usuário privado deve ser definido no fluxo de áudio MPEG.                      | O bit do usuário privado está desligado.                                                                                                                                               |



 

Para obter um ponteiro para a interface [**ICodecAPI,**](/windows/win32/api/strmif/nn-strmif-icodecapi) chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no MFT.

O MFT implementa os seguintes [**métodos ICodecAPI:**](/windows/win32/api/strmif/nn-strmif-icodecapi)

-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**Getvalue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**Ismodifiable**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**Issupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Todos os [**outros métodos ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retornam **E \_ NOTIMPL.**

## <a name="remarks"></a>Comentários

Cada quadro de áudio MPEG contém amostras de áudio 384 (Camada 1) ou 1152 (Camada 2) por canal. No entanto, cada buffer de entrada para o codificador pode conter qualquer número de exemplos de PCM. O tamanho de cada buffer de entrada deve ser um múltiplo do alinhamento do bloco. O codificador armazena em cache exemplos de entrada até que ele tenha o suficiente para um quadro de áudio MPEG.

Cada buffer de saída contém um quadro MPEG bruto. O tamanho de cada buffer de saída depende da taxa de bits e da taxa de exemplo.

### <a name="configuring-the-encoder"></a>Configurando o codificador

Para alterar qualquer uma das configurações padrão no codificador, execute as seguintes etapas:

1.  Crie uma instância do MFT do codificador.
2.  Chame [**IMFTransform::GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter a lista dos tipos de saída preferenciais. O codificador enumera todas as taxas de exemplo para mono e estéreo. Selecione um desses tipos de mídia, com base na taxa de exemplo e no número de canais. O [atributo \_ MF MT \_ AUDIO \_ AVG BYTES PER \_ \_ \_ SECOND](mf-mt-audio-avg-bytes-per-second-attribute.md) indica a taxa de bits padrão, em bytes por segundo.
3.  Opcional: você pode substituir a taxa de bits padrão definindo um novo valor para [ \_ BYTES \_ MT AUDIO \_ AVG POR \_ \_ \_ SEGUNDO](mf-mt-audio-avg-bytes-per-second-attribute.md) no tipo de mídia de saída. As taxas de bits válidas dependem da taxa de exemplo, do número de canais e da camada de áudio.
    > [!Note]  
    > Neste ponto do processo de configuração, o codificador assume como padrão o áudio da Camada 2 e aceitará apenas taxas de bits de Camada 2. Você poderá alternar o codificador para a Camada 1 em uma etapa posterior (consulte a etapa 7). Nesse caso, deixe a taxa de bits padrão por enquanto; você pode alterá-lo novamente na etapa 8.

     

4.  Chame [**IMFTransform::SetOutputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) definir o tipo de mídia de saída. Se você definir seu próprio valor para [ \_ BYTES MT AUDIO \_ \_ AVG \_ \_ POR \_ ](mf-mt-audio-avg-bytes-per-second-attribute.md) SEGUNDO e o MFT rejeitar o tipo de mídia de saída, provavelmente será porque você especificou uma taxa de bits inválida.
5.  Chame [**IMFTransform::GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para enumerar o tipo de mídia de entrada. Como a taxa de exemplo e o número de canais devem ser idênticos ao tipo de saída, apenas duas opções são enumeradas: entrada PCM de ponto flutuante de 32 bits e entrada PCM de inteiro de 16 bits. Selecione um deles.
6.  Chame [**IMFTransform::SetInputType para**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) definir o tipo de mídia de entrada.
7.  Opcional: para codificar o áudio da Camada 1, de definido a propriedade [ \_ CODECAPI AVEncMPALayer](../directshow/avencmpalayer-property.md) como **eAVEncMPALayer \_ 1**.
8.  Opcional: para alterar a taxa de bits, de acordo com a [propriedade \_ CODECAPI AVEncCommonMeanBitRate.](../directshow/avenccommonmeanbitrate-property.md) A taxa de bits deve ser uma das taxas de bits válidas listadas nas especificações mpeg-1 ou MPEG-2 LSF. Como alternativa, você pode chamar [**ICodecAPI::GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) para obter uma lista de taxas de bits válidas, com base nas configurações atuais.
9.  Opcional: com o áudio de dois canais, você pode definir a propriedade [ \_ CODECAPI AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) para alterar o modo de codificação para canal duplo ou estéreo conjunto. Você pode chamar [**ICodecAPI::GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) para obter as opções válidas. (Para áudio de 1 canal, a única opção é mono.)
10. Opcional: de definir qualquer uma das outras [**propriedades ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) listadas anteriormente.

É importante seguir a ordem dessas etapas. Em particular, de acordo com o tipo de mídia de saída antes de alterar as [**propriedades de ICodecAPI.**](/windows/win32/api/strmif/nn-strmif-icodecapi) Além disso, você deve definir **propriedades ICodecAPI** antes que o MFT receba o primeiro exemplo de entrada. Depois que o MFT recebe a entrada, as propriedades do codec são somente leitura e [**ICodecAPI::SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) retorna o valor **S \_ FALSE.**

### <a name="supported-bit-rates"></a>Taxas de bits com suporte

O codificador dá suporte às taxas de bits a seguir.



MPEG-1

MPEG-2

Camada 1

Camada 2

Camada 1

Camada 2

32

32\*

32

8

64

48\*

38

16

96

56\*

56

24

128

64

64

32

160

80\*

80

40

192

96

96

48

224

112

112

56

256

128

128

64

288

160

144

80

320

192

160

96

352

224\*\*

176

112

384

256\*\*

192

128

416

230\*\*

224

144

448

384\*\*

256

160



 

<dl> \* Somente Mono  
\*\* Somente estéreo  
</dl>

### <a name="example-media-types"></a>Tipos de mídia de exemplo

Aqui está um exemplo dos tipos de mídia necessários para codificar o PCM inteiro de 16 bits, áudio estéreo de 48 kHz na taxa de bits padrão.

Tipo de mídia de saída:

| Atributo                                                                           | Valor                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [MF \_ MT \_ MAJOR \_ TYPE](mf-mt-major-type-attribute.md)                               | **Áudio MFMediaType \_**  |
| [SUBTIPO \_ MF MT \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG** |
| [AMOSTRAS \_ DE ÁUDIO MT \_ \_ MT POR \_ \_ SEGUNDO](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [CANAIS NUM DE ÁUDIO \_ MF MT \_ \_ \_](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

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
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 8 somente aplicativos da área de trabalho\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> </dl>

 

 
