---
description: 'O codificador de vídeo Microsoft Media Foundation H. 264 é uma transformação Media Foundation que dá suporte aos seguintes perfis H. 264:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Codificador de vídeo H. 264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04d1c1c8af4487d02cbb8405ebf341458424074a3d8c3cae53bff4207f73490c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117879090"
---
# <a name="h264-video-encoder"></a>Codificador de vídeo H. 264

O codificador de vídeo Microsoft Media Foundation H. 264 é uma [transformação Media Foundation](media-foundation-transforms.md) que dá suporte aos seguintes perfis H. 264:

-   Perfil de linha de base
-   Perfil Principal
-   Perfil alto (requer Windows 8)

O codificador de vídeo H. 264 expõe as seguintes interfaces:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipos de entrada

O tipo de mídia de entrada deve ter um dos seguintes subtipos:

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

O tipo de saída deve ser definido antes do tipo de entrada. Até que o tipo de saída seja definido, o método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) do codificador retorna **MF_E_TRANSFORM_TYPE_NOT_SET**.

## <a name="output-types"></a>Tipos de saída

O codificador dá suporte a um subtipo de saída único:

-   **MFVideoFormat_H264**

Defina os seguintes atributos no tipo de mídia de saída.



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
<td><a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a></td>
<td>Tipo principal. Deve ser <strong>MFMediaType_Video</strong>.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a></td>
<td>Subtipo de vídeo. Deve ser <strong>MFVideoFormat_H264</strong>.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a></td>
<td>Taxa média de bits codificada, em bits por segundo. Deve ser maior que zero.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a></td>
<td>Taxa de quadros.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a></td>
<td>Tamanho do quadro.</td>
</tr>
<tr class="even">
<td><a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a></td>
<td>Modo de entrelaçamento.</td>
</tr>
<tr class="odd">
<td><a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a></td>
<td>Perfil de codificação H. 264.<br/> Os valores com suporte são:<br/>
<ul>
<li><strong>eAVEncH264VProfile_Base</strong> (padrão)</li>
<li><strong>eAVEncH264VProfile_Main</strong></li>
<li><strong>eAVEncH264VProfile_High</strong> (requer Windows 8)</li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>Opcional. Especifica o nível de codificação H. 264.<br/> O valor padrão é – 1, indicando que o codificador selecionará o nível de codificação.<br/> É recomendável não definir o nível no tipo de mídia e permitir que o codificador selecione o nível. O codificador pode derivar o nível apropriado para um determinado fluxo de vídeo, levando em conta as restrições de formato e as características do vídeo. Para obter mais informações sobre restrições de perfil e de nível, consulte anexo A de ITU-T H. 264.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Opcional. Especifica a taxa de proporção de pixel. O valor padrão é 1:1.</td>
</tr>
</tbody>
</table>



 

Depois que o tipo de saída é definido, o codificador de vídeo atualiza o tipo adicionando o atributo [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) . Este atributo contém o cabeçalho de sequência.

## <a name="codec-properties"></a>Propriedades do codec

O codificador H. 264 implementa a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para definir parâmetros de codificação. Ele dá suporte às propriedades a seguir.

Para obter os requisitos de codec para a certificação do codificador HCK, consulte a seção **codificador de hardware certificado** abaixo.

as propriedades a seguir têm suporte no Windows 7.



| Propriedade                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Define o modo de controle de taxa. Consulte Observações. O modo padrão é taxa de bits variável irrestrita (VBR).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Define o nível de qualidade. Essa propriedade se aplica quando o modo de controle de taxa é taxa de bits baseada em qualidade (**eAVEncCommonRateControlMode_Quality**). O intervalo válido é de 1 a 100. O valor padrão é 70. <br/> Para definir esse parâmetro, defina a propriedade antes de chamar [**IMFTransform:: SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). <br/> para definir esse parâmetro no Windows 7, defina a propriedade antes de chamar [**IMFTransform:: setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). O codificador ignora as alterações depois que o tipo de saída é definido. <br/> no Windows 8, essa propriedade pode ser definida a qualquer momento durante a codificação. As alterações são aplicadas começando no próximo quadro de entrada. <br/> Internamente, o codificador converte essa propriedade em um valor [AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md) . <br/> |



 

As propriedades a seguir exigem Windows 8.



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Propriedade</th>
<th>Descrição</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a></td>
<td>Define o modo de codificação adaptável. O codificador H. 264 dá suporte aos seguintes modos no Windows 8:
<ul>
<li><strong>eAVEncAdaptiveMode_None</strong>. Sem codificação adaptável. (Padrão.)</li>
<li><strong>eAVEncAdaptiveMode_FrameRate</strong>. Altere adaptativamente a taxa de quadros.</li>
</ul>
<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>Define o tamanho do buffer, em bytes, para a codificação de taxa de bits constante (CBR).<br/> O intervalo válido é [1... 2 ³ ² – 1]. <br/> Requer Windows 8. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>Para a codificação de taxa de bits restrita, especifica a taxa na qual o &quot; Bucket de vazamentos &quot; é esgotado, em bits por segundo. Essa propriedade se aplica quando o modo de controle de taxa é <strong>eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>. <br/> O intervalo válido é [1... 2 ³ ² – 1]. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>Define a taxa média de bits para o fluxo de bits codificado, em bits por segundo. Essa propriedade será ignorada se o modo de controle de taxa for <strong>eAVEncCommonRateControlMode_Quality</strong>. <br/> O intervalo válido é [1... 2 ³ ² – 1]. <br/> Na CBR e nos modos de VBR não restritos, a taxa média de bits determina o tamanho final do arquivo. No modo CBR, a taxa média de bits também é a taxa na qual bits compactados são drenados do &quot; Bucket de vazamento. &quot; (para obter mais informações, consulte <a href="the-leaky-bucket-buffer-model.md">o modelo de buffer de buckets de vazamentos</a>.) <br/> no Windows 7, a taxa média de bits é especificada pelo atributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> no tipo de mídia. <br/> no Windows 8, você pode definir a taxa média de bits usando o atributo <a href="mf-mt-avg-bitrate-attribute.md">MF_MT_AVG_BITRATE</a> ou a propriedade <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> . Se ambos estiverem definidos, CODECAPI_AVEncCommonMeanBitRate substituições. no Windows 8, você pode definir a taxa de bits média durante a codificação. Se a taxa de bits for alterada, o codificador usará a codificação adaptável.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>Define a compensação de qualidade/velocidade. Intervalo válido:
<ul>
<li>0 – 33: baixa complexidade</li>
<li>34 – 66: complexidade média (padrão)</li>
<li>67 – 100: alta complexidade</li>
</ul>
<br/> Esse valor afeta como o codificador executa várias operações de codificação, como compensação de movimento. Em níveis mais altos de complexidade, o codificador é executado mais lentamente, mas produz uma qualidade melhor na mesma taxa de bits.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a></td>
<td>Habilita ou desabilita CABAC (codificação aritmética binária de contexto) para codificação de entropia H. 264. O valor padrão é <strong>VARIANT_FALSE</strong>. <br/> CABAC não é usado para o perfil de linha de base.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a></td>
<td>Define o valor de <strong>seq_parameter_set_id</strong> na unidade de nal do SPS do H. 264 fragmentado. <br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a></td>
<td>Define o número máximo de quadros B consecutivos no fragmentado de saída. Os valores válidos são:
<ul>
<li>0: não use quadros B (padrão).</li>
<li>1: usar um quadro B.</li>
<li>2: usar dois quadros B.</li>
</ul>
Para definir esse parâmetro, defina a propriedade antes de chamar <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform:: SetOutputType</strong></a>. <br/> Para o perfil de linha de base, o número de quadros B é sempre zero. O codificador substituirá valores diferentes de zero.<br/> Para outros perfis H. 264, se essa propriedade for diferente de zero, o padrão de codificação será IBBPBBP, em que o número máximo de quadros B consecutivos será igual a <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a>. <br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>Define o número de imagens de um cabeçalho GOP para o seguinte, incluindo a âncora à esquerda, mas não o seguinte. <br/> O intervalo válido é [0... 2 ³ ² – 1]. Se for zero, o codificador selecionará o tamanho de GOP. O valor padrão é zero. <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>Define o número de threads de trabalho usados por um codificador.<br/> O intervalo válido é de 0 a 16. Se for zero, o codificador selecionará o número de threads. <br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a></td>
<td>Indica o tipo de conteúdo de vídeo.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>Intervalo válido: 16 a 51. O valor padrão é 24. <br/> Essa propriedade se aplica quando o modo de controle de taxa é <strong>eAVEncCommonRateControlMode_Quality</strong>. <br/> Essa propriedade define a mesma configuração de codificação que <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>. No entanto, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> permite que o aplicativo especifique o valor de QP diretamente. Se ambas as propriedades forem definidas, AVEncVideoEncodeQP substituições. <br/> O valor padrão de 24 corresponde ao valor padrão de 70 para a configuração <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>Força o codificador a codificar o próximo quadro como um quadro-chave.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>Intervalo válido: 0 – 51. O valor padrão é 0. <br/> Essa propriedade se aplica a todos os modos de controle de taxa. O codificador não deve produzir um valor de QP menor do que o especificado pela propriedade <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> .<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>Habilita ou desabilita o modo de baixa latência. Consulte &quot; multithreading &quot; na seção comentários.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="remarks"></a>Comentários

O codificador dá suporte aos modos de controle de taxa a seguir.



| Mode                                  | Constante                                            | Descrição                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Taxa de bits constante (CBR)               | **eAVEncCommonRateControlMode_CBR**                | O codificador tenta atingir uma taxa de bits constante, usando um modelo de "Bucket de vazamentos". A taxa de bits de destino é fornecida pela propriedade [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) . <br/> Requer Windows 8. <br/> |
| Taxa de bits de variável restrita (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | O codificador usa um modelo de "Bucket de vazamentos" com uma taxa de bits de pico. A taxa de descarga para o Bucket de vazamento é fornecida pela propriedade [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) . <br/> Requer Windows 8. <br/>     |
| Taxa de bits variável baseada em qualidade (VBR) | **eAVEncCommonRateControlMode_Quality**            | O codificador tenta atingir um nível de qualidade constante, fornecido pela propriedade [**AVEncCommonQuality**](../directshow/avenccommonquality-property.md) .                                                                                                           |
| VBR não restringida                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | O codificador tenta atingir a taxa de bits de destino fornecida pelo atributo [**MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia de saída. Esse é o modo padrão.                                                              |



 

Os modos de CBR e VBR restrita exigem Windows 8.

no Windows 8, o codificador define os seguintes atributos nos exemplos de saída:

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> uma versão anterior da documentação declarava incorretamente que o codificador tem suporte no Windows Server 2008 R2.

 

### <a name="multithreading"></a>Multithreading

no Windows 8, o codificador dá suporte a dois modos de codificação:

-   **Codificação de fatia.** Nesse modo, as fatias são codificadas em paralelo. Cada fatia é codificada em um thread diferente. Esse modo tem baixa latência, pois uma única imagem é codificada em paralelo. No entanto, essa abordagem não é dimensionada conforme o número de núcleos aumenta, pois o número de fatias é limitado pelo número de linhas macrobloco na imagem de entrada.
-   **Codificação de vários quadros.** Nesse modo, o codificador aceita vários quadros de entrada e os codifica em paralelo. Esse modo escala melhor em um ambiente de vários núcleos, mas introduz mais latência.

O codificador assume como padrão a codificação de fatia, para minimizar a latência. Para habilitar a codificação de vários quadros, de definir [a propriedade CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) como **VARIANT_FALSE**.

Para definir o número de threads de trabalho usados pelo codificador, de definir a [propriedade CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) trabalho.

No Windows 7, o codificador sempre usa codificação de fatia.

### <a name="certified-hardware-encoder"></a>Codificador de hardware certificado

Se um codificador de hardware certificado estiver presente, ele geralmente será usado em vez do codificador do sistema de caixa de entrada para Media Foundation cenários relacionados. Codificadores certificados são necessários para dar suporte a um determinado conjunto de **propriedades ICodecAPI** e, opcionalmente, podem dar suporte a outro conjunto de propriedades. O processo de certificação deve garantir que as propriedades necessárias sejam corretamente suportadas e, se uma propriedade opcional tiver suporte, também terá suporte adequado.

A seguir está o conjunto de propriedades **ICodecAPI** necessárias e opcionais para codificadores passarem na certificação do codificador HCK.

As seguintes Windows 8 e Windows 8.1 **ICodecAPI** são necessárias:

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

As propriedades Windows 8.1 **ICodecAPI** a seguir são opcionais, mas são testadas em HCK se há suporte.

-   [CODECAPI_AVEncVideoMinQP](codecapi-avencvideominqp.md)
-   [CODECAPI_AVEncVideoLTRBufferControl](codecapi-avencvideoltrbuffercontrol.md)
-   [CODECAPI_AVEncVideoMarkLTRFrame](codecapi-avencvideomarkltrframe.md)
-   [CODECAPI_AVEncVideoUseLTRFrame](codecapi-avencvideouseltrframe.md)
-   [CODECAPI_AVEncVideoEncodeFrameTypeQP](codecapi-avencvideoencodeframetypeqp.md)
-   [CODECAPI_AVEncSliceControlMode](codecapi-avencslicecontrolmode.md)
-   [CODECAPI_AVEncSliceControlSize](codecapi-avencslicecontrolsize.md)
-   [CODECAPI_AVEncVideoMaxNumRefFrame](codecapi-avencvideomaxnumrefframe.md)
-   [CODECAPI_AVEncVideoMeanAbsoluteDifference](codecapi-avencvideomeanabsolutedifference.md)
-   [CODECAPI_AVEncVideoMaxQP](codecapi-avencvideomaxqp.md)
-   [CODECAPI_AVEncVideoROIEnabled](codecapi-avencvideoroienabled.md)
-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (dinâmico)
-   [CODECAPI_AVEncH264CABACEnable](codecapi-avench264cabacenable.md)

As propriedades Windows 8 e Windows 8.1 **ICodecAPI** são opcionais, mas são testadas em HCK se há suporte.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (Estático)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

As propriedades **ICodecAPI a seguir** são opcionais. Eles não são testados no HCK.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows 7 \[ aplicativos da área de trabalho\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> <dt>

[Suporte ao MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> </dl>

 

 
