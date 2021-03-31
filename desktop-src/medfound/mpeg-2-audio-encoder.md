---
description: O codificador de áudio MPEG-2 Microsoft Media Foundation é uma transformação Media Foundation que codifica áudio mono ou estéreo em áudio MPEG-1 (ISO/IEC 11172-3) ou MPEG-2 Audio (ISO/IEC 13818-3).
ms.assetid: EBEFED1F-D0B8-4C7E-B1FB-CDE3BDFD99AA
title: Codificador de áudio MPEG-2
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2454e542ba59f4955668bd1fcefbf5dbc0f11551
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103827541"
---
# <a name="mpeg-2-audio-encoder"></a>Codificador de áudio MPEG-2

O codificador de áudio MPEG-2 Microsoft Media Foundation é uma [transformação Media Foundation](media-foundation-transforms.md) que codifica áudio mono ou estéreo em áudio MPEG-1 (ISO/IEC 11172-3) ou MPEG-2 Audio (ISO/IEC 13818-3).

O codificador dá suporte a áudio de camada 1 e camada 2. Ele não dá suporte a áudio MPEG-Layer 3 (MP3). Para MPEG-2, o codificador dá suporte à parte de LSF (frequências de amostragem baixa) de áudio MPEG-2. Ele não oferece suporte às extensões de multicanal. O MFT gera um fluxo elementar MPEG. Ele não pode gerar fluxos elementares, fluxos de programa ou fluxos de transporte em pacotes.

## <a name="class-identifier"></a>Identificador de classe

O CLSID (identificador de classe) do codificador de áudio MEPG-2 é **CLSID \_ CMPEG2AudioEncoderMFT**, definido no arquivo de cabeçalho wmcodecdsp. h.

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
<td>Obrigatórios. Deve ser <strong>MFAudioFormat_MPEG</strong>. Esse subtipo é usado para áudio MPEG-1 e MPEG-2.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-audio-samples-per-second-attribute.md">MF_MT_AUDIO_SAMPLES_PER_SECOND</a></td>
<td>Exemplos por segundo.</td>
<td>Obrigatórios. Os valores a seguir têm suporte para MPEG-1 e MPEG-2:
<ul>
<li>32000</li>
<li>44100</li>
<li>48000</li>
</ul>
Além disso, os seguintes valores têm suporte para LSF MPEG-2: <br/>
<ul>
<li>16000</li>
<li>22050</li>
<li>24.000</li>
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
<td>Taxa de bits do fluxo MPEG codificado, em bytes por segundo.</td>
<td>Opcional.<br/> As especificações de ISO/IEC 11172-3 e ISO/IEC 13818-3 (LSF) definem várias taxas de bits, dependendo da taxa de amostragem, do número de canais e da camada de áudio (1 ou 2). <br/> O codificador assume como padrão o áudio de camada 2. Se o atributo <a href="mf-mt-audio-avg-bytes-per-second-attribute.md">MF_MT_AUDIO_AVG_BYTES_PER_SECOND</a> não estiver definido, o codificador usará as seguintes taxas de bits padrão:<br/>
<ul>
<li>MPEG-1 estéreo: 224.000 bits por segundo (bps) = 28.000 bytes por segundo.</li>
<li>MPEG-1 mono: 192.000 bps = 24.000 bytes por segundo.</li>
<li>MPEG-2 LSF, mono ou estéreo: 160.000 bps = 20.000 bytes por segundo.</li>
</ul>
Esse atributo pode ser definido como outros valores. Se o valor não for válido de acordo com as especificações MPEG, o MFT rejeitará o tipo de mídia.<br/> Você também pode definir a taxa de bits usando a interface <a href="/windows/desktop/api/strmif/nn-strmif-icodecapi"><strong>ICodecAPI</strong></a> . Consulte comentários para obter mais informações.<br/></td>
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



 

O codificador não oferece suporte à conversão de taxa de amostragem ou conversão estéreo/mono. Se os atributos opcionais não estiverem definidos, o codificador os adicionará ao tipo de mídia depois que o tipo for definido.

## <a name="codec-properties"></a>Propriedades do codec

O codificador dá suporte às seguintes propriedades por meio da interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) .



| Propriedade                                                                                | Descrição                                                                                      | Valor padrão                                                                                                                                                          |
|-----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)               | Especifica a taxa média de bits codificada, em bits por segundo.                                      | Conforme descrito para o atributo de [ \_ \_ \_ bytes médios \_ \_ por \_ segundo do áudio MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) no tipo de mídia de saída.                      |
| [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md)                       | Especifica o modo de codificação de áudio MPEG.                                                          | Estéreo para áudio de 2 canais ou canal único para áudio de 1 canal.<br/> Para áudio de 2 canais, o codificador também dá suporte a canal duplo e estéreo conjunta.<br/> |
| [CODECAPI \_ AVEncMPACopyright](../directshow/avencmpacopyright-property.md)                         | Especifica se o bit de direitos autorais deve ser definido no fluxo de áudio MPEG.                             | Sem direitos autorais.                                                                                                                                                          |
| [CODECAPI \_ AVEncMPAEmphasisType](../directshow/avencmpaemphasistype-property.md)                   | Especifica o tipo de filtro de ênfase que deve ser usado quando o fluxo codificado é decodificado. | Nenhuma ênfase especificada.                                                                                                                                                 |
| [AVEncMPAEnableRedundancyProtection](../directshow/avencmpaenableredundancyprotection-property.md) | Especifica se uma CRC (verificação de redundância cíclica) deve ser adicionada ao cabeçalho do quadro.                    | Uma soma de verificação de CRC é gravada no fluxo de bits.                                                                                                                           |
| [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md)                                 | Especifica a camada de áudio MPEG.                                                                  | Áudio de camada 2.                                                                                                                                                         |
| [CODECAPI \_ AVEncMPAOriginalBitstream](../directshow/avencmpaoriginalbitstream-property.md)         | Especifica se deve ser definido para o bit original no fluxo de áudio MPEG.                          | O bit "original" está desativado.                                                                                                                                                 |
| [CODECAPI \_ AVEncMPAPrivateUserBit](../directshow/avencmpaprivateuserbit-property.md)               | Especifica se deve ser definido para o bit do usuário privado no fluxo de áudio MPEG.                      | O bit de usuário privado está desativado.                                                                                                                                               |



 

Para obter um ponteiro para a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) , chame [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q)) no MFT.

A MFT implementa os seguintes métodos [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) :

-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**Parameters**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**Ismodificável**](/windows/win32/api/strmif/nf-strmif-icodecapi-ismodifiable)
-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)

Todos os outros métodos [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retornam **E \_ NOTIMPL**.

## <a name="remarks"></a>Comentários

Cada quadro de áudio MPEG contém exemplos de áudio 384 (camada 1) ou 1152 (camada 2) por canal. No entanto, cada buffer de entrada para o codificador pode conter qualquer número de amostras de PCM. O tamanho de cada buffer de entrada deve ser um múltiplo do alinhamento de bloco. O codificador armazena em cache os exemplos de entrada até que ele tenha o suficiente para um quadro de áudio MPEG.

Cada buffer de saída contém um quadro MPEG bruto. O tamanho de cada buffer de saída depende da taxa de bits e da taxa de amostragem.

### <a name="configuring-the-encoder"></a>Configurando o codificador

Para alterar as configurações padrão no codificador, execute as seguintes etapas:

1.  Crie uma instância do MFT do codificador.
2.  Chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype) para obter a lista dos tipos de saída preferenciais. O codificador enumera todas as taxas de exemplo para mono e estéreo. Selecione um desses tipos de mídia, com base na taxa de amostra e no número de canais. O atributo de [ \_ \_ \_ bytes médios \_ \_ por \_ segundo do áudio MF MT](mf-mt-audio-avg-bytes-per-second-attribute.md) indica a taxa de bits padrão, em bytes por segundo.
3.  Opcional: você pode substituir a taxa de bits padrão definindo um novo valor para [áudio do MF \_ MT \_ média de \_ \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) no tipo de mídia de saída. As taxas de bits válidas dependem da taxa de amostragem, do número de canais e da camada de áudio.
    > [!Note]  
    > Neste ponto do processo de configuração, o codificador assume como padrão o áudio de camada 2 e só aceitará taxas de bits de camada 2. Você poderá alternar o codificador para a camada 1 em uma etapa posterior (consulte a etapa 7). Nesse caso, deixe a taxa de bits padrão por enquanto; Você pode alterá-lo novamente na etapa 8.

     

4.  Chame [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype) para definir o tipo de mídia de saída. Se você definir seu próprio valor para [o \_ áudio MF MT \_ \_ AVG \_ bytes \_ por \_ segundo](mf-mt-audio-avg-bytes-per-second-attribute.md) e o MFT rejeitar o tipo de mídia de saída, é provável que você tenha especificado uma taxa de bits inválida.
5.  Chame [**IMFTransform:: GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype) para enumerar o tipo de mídia de entrada. Como a taxa de amostra e o número de canais devem ser idênticos ao tipo de saída, somente duas opções são enumeradas: entrada PCM de ponto flutuante de 32 bits e entrada PCM de inteiro de 16 bits. Selecione um deles.
6.  Chame [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) para definir o tipo de mídia de entrada.
7.  Opcional: para codificar áudio de camada 1, defina a propriedade [CODECAPI \_ AVEncMPALayer](../directshow/avencmpalayer-property.md) como **eAVEncMPALayer \_ 1**.
8.  Opcional: para alterar a taxa de bits, defina a propriedade [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) . A taxa de bits deve ser uma das taxas de bits válidas listadas nas especificações de LSF MPEG-1 ou MPEG-2. Como alternativa, você pode chamar [**ICodecAPI:: getParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues) para obter uma lista de taxas de bits válidas com base nas configurações atuais.
9.  Opcional: com áudio de 2 canais, você pode definir a propriedade [CODECAPI \_ AVEncMPACodingMode](../directshow/avencmpacodingmode-property.md) para alterar o modo de codificação para canal duplo ou estéreo conjunta. Você pode chamar [**ICodecAPI:: GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange) para obter as opções válidas. (Para áudio de 1 canal, a única opção é mono.)
10. Opcional: defina qualquer uma das outras propriedades de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) listadas anteriormente.

É importante seguir a ordem dessas etapas. Em particular, defina o tipo de mídia de saída antes de alterar as propriedades de [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) . Além disso, você deve definir as propriedades **ICodecAPI** antes que a MFT receba a primeira amostra de entrada. Depois que o MFT recebe a entrada, as propriedades do codec são somente leitura e [**ICodecAPI:: SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue) retorna o valor **S \_ false**.

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



 

<dl> \* Somente mono  
\*\* Somente estéreo  
</dl>

### <a name="example-media-types"></a>Exemplos de tipos de mídia

Aqui está um exemplo dos tipos de mídia que são necessários para codificar o PCM de inteiro de 16 bits, áudio estéreo de 48 kHz na taxa de bits padrão.

Tipo de mídia de saída:

| Atributo                                                                           | Valor                   |
|-------------------------------------------------------------------------------------|-------------------------|
| [\_ \_ tipo principal MF \_ MT](mf-mt-major-type-attribute.md)                               | **\_Áudio MFMediaType**  |
| [subtipo MF \_ MT \_](mf-mt-subtype-attribute.md)                                      | **MFAudioFormat \_ MPEG** |
| [\_amostras de áudio MF MT \_ \_ \_ por \_ segundo](mf-mt-audio-samples-per-second-attribute.md) | 48000                   |
| [\_canais de \_ número de áudio MF MT \_ \_](mf-mt-audio-num-channels-attribute.md)              | 2                       |



 

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
|-------------------------------------|-------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos de área de trabalho do Windows 8\]<br/>                                                |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                 |
| DLL<br/>                      | <dl> <dt>Msmpeg2enc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 
