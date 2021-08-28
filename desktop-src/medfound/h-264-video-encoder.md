---
description: 'O Microsoft Media Foundation codificador de vídeo H.264 é uma Media Foundation que dá suporte aos seguintes perfis H.264:'
ms.assetid: 4d4c768f-b76a-40ca-8736-2f592a4f4cc4
title: Codificador de vídeo H.264
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 875974c53be265fbcace8cf99e2bdd78d69cdda5
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467523"
---
# <a name="h264-video-encoder"></a>Codificador de vídeo H.264

O Microsoft Media Foundation codificador de vídeo H.264 é uma Media Foundation [que](media-foundation-transforms.md) dá suporte aos seguintes perfis H.264:

-   Perfil de Linha de Base
-   Perfil Principal
-   Perfil alto (requer Windows 8)

O codificador de vídeo H.264 expõe as seguintes interfaces:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipos de entrada

O tipo de mídia de entrada deve ter um dos seguintes subtipos:

-   **MFVideoFormat_I420**
-   **MFVideoFormat_IYUV**
-   **MFVideoFormat_NV12**
-   **MFVideoFormat_YUY2**
-   **MFVideoFormat_YV12**

Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo.](video-subtype-guids.md)

O tipo de saída deve ser definido antes do tipo de entrada. Até que o tipo de saída seja definido, o método [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) do **codificador retorna MF_E_TRANSFORM_TYPE_NOT_SET**.

## <a name="output-types"></a>Tipos de saída

O codificador dá suporte a um único subtipo de saída:

-   **MFVideoFormat_H264**

De definir os atributos a seguir no tipo de mídia de saída.




| Atributo | Descrição | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. Deve ser <strong>MFMediaType_Video</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de vídeo. Deve ser <strong>MFVideoFormat_H264</strong>. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Taxa de bits codificada média, em bits por segundo. Deve ser maior que zero. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Taxa de quadros. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Tamanho do quadro. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Modo intercalar. | 
| <a href="mf-mt-mpeg2-profile-attribute.md"><strong>MF_MT_MPEG2_PROFILE</strong></a> | Perfil de codificação H.264.<br /> Os valores com suporte são:<br /><ul><li><strong>eAVEncH264VProfile_Base</strong> (padrão)</li><li><strong>eAVEncH264VProfile_Main</strong></li><li><strong>eAVEncH264VProfile_High</strong> (requer Windows 8)</li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | Opcional. Especifica o nível de codificação H.264.<br /> O valor padrão é –1, indicando que o codificador selecionará o nível de codificação.<br /> É recomendável não definir o nível no tipo de mídia e permitir que o codificador selecione o nível. O codificador pode derivar o nível adequado para um determinado fluxo de vídeo, levando em conta as restrições de formato e as características do vídeo. Para obter mais informações sobre restrições de perfil e nível, consulte Anexo A do ITU-T H.264.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | Opcional. Especifica a taxa de proporção de pixel. O valor padrão é 1:1. | 




 

Depois que o tipo de saída é definido, o codificador de vídeo atualiza o tipo adicionando o [**MF_MT_MPEG_SEQUENCE_HEADER**](mf-mt-mpeg-sequence-header-attribute.md) atributo. Esse atributo contém o header de sequência.

## <a name="codec-properties"></a>Propriedades do Codec

O codificador H.264 implementa a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para definir parâmetros de codificação. Ele dá suporte às propriedades a seguir.

Para ver os requisitos de codec para certificação do codificador HCK, consulte a seção **Codificador de Hardware** Certificado abaixo.

As propriedades a seguir têm suporte no Windows 7.



| Propriedade                                                                              | Descrição                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                     |
|---------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**CODECAPI_AVEncCommonRateControlMode**](../directshow/avenccommonratecontrolmode-property.md) | Define o modo de controle de taxa. Consulte Observações. O modo padrão é a VBR (taxa de bits variável irrimplente).                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                             |
| [**CODECAPI_AVEncCommonQuality**](../directshow/avenccommonquality-property.md)                 | Define o nível de qualidade. Essa propriedade se aplica quando o modo de controle de taxa é VBR baseado em qualidade (**eAVEncCommonRateControlMode_Quality**). O intervalo válido é de 1 a 100. O valor padrão é 70. <br/> Para definir esse parâmetro, de definido a propriedade antes de chamar [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). <br/> Para definir esse parâmetro no Windows 7, de definido a propriedade antes de chamar [**IMFTransform::SetOutputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype). O codificador ignora as alterações depois que o tipo de saída é definido. <br/> No Windows 8, essa propriedade pode ser definida a qualquer momento durante a codificação. As alterações são aplicadas a partir do próximo quadro de entrada. <br/> Internamente, o codificador converte essa propriedade em [um valor AVEncVideoEncodeQP.](codecapi-avencvideoencodeqp.md) <br/> |



 

As propriedades a seguir exigem Windows 8.




| Propriedade | Descrição | 
|----------|-------------|
| <a href="codecapi-avencadaptivemode.md">CODECAPI_AVEncAdaptiveMode</a> | Define o modo de codificação adaptável. O codificador H.264 dá suporte aos seguintes modos Windows 8:<ul><li><strong>eAVEncAdaptiveMode_None</strong>. Nenhuma codificação adaptável. (Padrão.)</li><li><strong>eAVEncAdaptiveMode_FrameRate</strong>. Altere adaptávelmente a taxa de quadros.</li></ul><br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Define o tamanho do buffer, em bytes, para codificação CBR (taxa de bits constante).<br /> O intervalo válido é [1 ... 2– 1]. <br /> Requer Windows 8. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Para codificação VBR restrita, especifica a taxa na qual o "bucket vazado" é esvaziado, em bits por segundo. Essa propriedade se aplica quando o modo de controle de taxa <strong>é eAVEncCommonRateControlMode_PeakConstrainedVBR</strong>. <br /> O intervalo válido é [1 ... 2– 1]. <br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Define a taxa média de bits para o fluxo de bits codificado, em bits por segundo. Essa propriedade será ignorada se o modo de controle de taxa for <strong>eAVEncCommonRateControlMode_Quality</strong>. <br /> O intervalo válido é [1 ... 2– 1]. <br /> Nos modos CBR e VBR não restritos, a taxa média de bits determina o tamanho final do arquivo. No modo CBR, a taxa média de bits também é a taxa na qual os bits compactados são esvaziados do "bucket vazado". (Para obter mais informações, consulte <a href="the-leaky-bucket-buffer-model.md">O modelo de buffer de bucket vazado</a>.) <br /> No Windows 7, a taxa média de bits é especificada pelo <a href="mf-mt-avg-bitrate-attribute.md">atributo MF_MT_AVG_BITRATE</a> no tipo de mídia. <br /> No Windows 8, você pode definir a taxa média de bits usando o <a href="mf-mt-avg-bitrate-attribute.md">atributo MF_MT_AVG_BITRATE</a> ou a <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">propriedade CODECAPI_AVEncCommonMeanBitRate.</a> Se ambos estão definidos, CODECAPI_AVEncCommonMeanBitRate substituições. No Windows 8, você pode definir a taxa média de bits durante a codificação. Se a taxa de bits mudar, o codificador usará a codificação adaptável.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Define a troca de qualidade/velocidade. Intervalo válido:<ul><li>0 a 33: baixa complexidade</li><li>34 a 66: Complexidade média (padrão)</li><li>67 a 100: alta complexidade</li></ul><br /> Esse valor afeta como o codificador executa várias operações de codificação, como a compensação de movimento. Em níveis de complexidade mais altos, o codificador é executado mais lentamente, mas produz melhor qualidade na mesma taxa de bits.<br /> | 
| <a href="codecapi-avench264cabacenable.md">CODECAPI_AVEncH264CABACEnable</a> | Habilita ou desabilita CABAC (codificação aritmética binária context-adaptável) para codificação de entropia H.264. O valor padrão é <strong>VARIANT_FALSE</strong>. <br /> CABAC não é usado para perfil de linha de base.<br /> | 
| <a href="codecapi-avench264spsid.md">CODECAPI_AVEncH264SPSID</a> | Define o valor de <strong>seq_parameter_set_id</strong> na unidade SPS NAL do fluxo de bits H.264. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">CODECAPI_AVEncMPVDefaultBPictureCount</a> | Define o número máximo de quadros B consecutivos no bitstream de saída. Os valores válidos são:<ul><li>0: Não use quadros B (padrão).</li><li>1: use um quadro B.</li><li>2: use dois quadros B.</li></ul>Para definir esse parâmetro, de definido a propriedade antes de chamar <a href="/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype"><strong>IMFTransform::SetOutputType</strong></a>. <br /> Para Perfil de linha de base, o número de quadros B é sempre zero. O codificador substituirá valores diferentes de zero.<br /> Para outros perfis H.264, se essa propriedade for diferente de zero, o padrão de codificação será IBBBP, em que o número máximo de quadros B consecutivos será igual <a href="/windows/desktop/DirectShow/avencmpvdefaultbpicturecount-property">a CODECAPI_AVEncMPVDefaultBPictureCount</a>. <br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Define o número de imagens de um header GOP para o próximo, incluindo a âncora à frente, mas não a seguinte. <br /> O intervalo válido é [0 ... 2– 1]. Se zero, o codificador selecionará o tamanho do GOP. O valor padrão é zero. <br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Define o número de threads de trabalho usados por um codificador.<br /> O intervalo válido é de 0 a 16. Se zero, o codificador selecionará o número de threads. <br /> | 
| <a href="codecapi-avencvideocontenttype.md">CODECAPI_AVEncVideoContentType</a> | Indica o tipo de conteúdo de vídeo.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Intervalo válido: 16 a 51. O valor padrão é 24. <br /> Essa propriedade se aplica quando o modo de controle de taxa <strong>é eAVEncCommonRateControlMode_Quality</strong>. <br /> Essa propriedade define a mesma configuração de codificação que <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>AVEncCommonQuality</strong></a>. No entanto, <a href="codecapi-avencvideoencodeqp.md">AVEncVideoEncodeQP</a> permite que o aplicativo especifique o valor de QP diretamente. Se ambas as propriedades estão definidas, AVEncVideoEncodeQP substitui. <br /> O valor padrão de 24 corresponde ao valor padrão de 70 para a <a href="/windows/desktop/DirectShow/avenccommonquality-property"><strong>configuração AVEncCommonQuality.</strong></a><br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Força o codificador a codificar o próximo quadro como um quadro-chave.<br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Intervalo válido: 0 a 51. O valor padrão é 0. <br /> Essa propriedade se aplica a todos os modos de controle de taxa. O codificador não deve produzir um valor QP menor do que o especificado pela <a href="codecapi-avencvideominqp.md">propriedade CODECAPI_AVEncVideoMinQP.</a><br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Habilita ou desabilita o modo de baixa latência. Consulte "Multithreading" na seção Comentários.<br /> | 




 

## <a name="remarks"></a>Comentários

O codificador dá suporte aos seguintes modos de controle de taxa.



| Modo                                  | Constante                                            | Descrição                                                                                                                                                                                                                                         |
|---------------------------------------|-----------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Taxa de bits constante (CBR)               | **eAVEncCommonRateControlMode_CBR**                | O codificador tenta atingir uma taxa de bits constante, usando um modelo de "bucket vazado". A taxa de bits de destino é determinada pela [propriedade CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md) destino. <br/> Requer Windows 8. <br/> |
| Taxa de bits de variável restrita (VBR)   | **eAVEncCommonRateControlMode_PeakConstrainedVBR** | O codificador usa um modelo de "bucket vazado" com uma taxa de bits de pico. A taxa de dreno para o bucket vazado é determinada pela [propriedade CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md) dados. <br/> Requer Windows 8. <br/>     |
| Taxa de bits variável baseada em qualidade (VBR) | **eAVEncCommonRateControlMode_Quality**            | O codificador tenta atingir um nível de qualidade constante, dado pela [**propriedade AVEncCommonQuality.**](../directshow/avenccommonquality-property.md)                                                                                                           |
| VBR irredido                     | **eAVEncCommonRateControlMode_UnconstrainedVBR**   | O codificador tenta atingir a taxa de bits de destino determinada [**pelo atributo MF_MT_AVG_BITRATE**](mf-mt-avg-bitrate-attribute.md) no tipo de mídia de saída. Esse é o modo padrão.                                                              |



 

Os modos CBR e VBR restritos exigem Windows 8.

No Windows 8, o codificador define os seguintes atributos nos exemplos de saída:

-   [MFSampleExtension_DecodeTimestamp](mfsampleextension-decodetimestamp.md)
-   [MFSampleExtension_VideoEncodePictureType](mfsampleextension-videoencodepicturetype.md)
-   [MFSampleExtension_VideoEncodeQP](mfsampleextension-videoencodeqp.md)

> [!Note]  
> Uma versão anterior da documentação incorretamente declarou que o codificador tem suporte no Windows Server 2008 R2.

 

### <a name="multithreading"></a>Multithreading

No Windows 8, o codificador dá suporte a dois modos de codificação:

-   **Codificação de fatia.** Nesse modo, as fatias são codificadas em paralelo. Cada fatia é codificada em um thread diferente. Esse modo tem baixa latência, porque uma única imagem é codificada em paralelo. No entanto, essa abordagem não é dimensionada conforme o número de núcleos aumenta, pois o número de fatias é limitado pelo número de linhas macrobloco na imagem de entrada.
-   **Codificação de vários quadros.** Nesse modo, o codificador aceita vários quadros de entrada e os codifica em paralelo. Esse modo escala melhor em um ambiente de vários núcleos, mas apresenta mais latência.

O codificador usa como padrão a codificação de fatia para minimizar a latência. Para habilitar a codificação de vários quadros, defina a propriedade [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md) como **VARIANT_FALSE**.

Para definir o número de threads de trabalho usados pelo codificador, defina a propriedade [CODECAPI_AVEncNumWorkerThreads](codecapi-avencnumworkerthreads.md) .

no Windows 7, o codificador sempre usa a codificação de fatia.

### <a name="certified-hardware-encoder"></a>Codificador de hardware certificado

Se um codificador de hardware certificado estiver presente, ele geralmente será usado em vez do codificador do sistema da caixa de entrada para Media Foundation cenários relacionados. Os codificadores certificados são necessários para dar suporte a um determinado conjunto de propriedades **ICodecAPI** e, opcionalmente, podem dar suporte a outro conjunto de propriedades. O processo de certificação deve garantir que as propriedades necessárias tenham suporte adequado e, se houver suporte para uma propriedade opcional, que também tenha suporte adequado.

Veja a seguir o conjunto de propriedades obrigatórias e opcionais do **ICodecAPI** para que os codificadores passem a certificação do codificador HCK.

as propriedades Windows 8 e Windows 8.1 **ICodecAPI** a seguir são necessárias:

-   [CODECAPI_AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI_AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI_AVEncCommonQualityVsSpeed](../directshow/avenccommonqualityvsspeed-property.md)
-   [CODECAPI_AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI_AVEncCommonMaxBitRate](../directshow/avenccommonmaxbitrate-property.md)
-   [CODECAPI_AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI_AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI_AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI_AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

as seguintes Windows 8.1 propriedades **ICodecAPI** são opcionais, mas são testadas em HCK, se houver suporte.

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

as propriedades Windows 8 e Windows 8.1 **ICodecAPI** a seguir são opcionais, mas são testadas em HCK, se houver suporte.

-   [CODECAPI_AVEncVideoTemporalLayerCount](codecapi-avencvideotemporallayercount.md) (estático)
-   [CODECAPI_AVLowLatencyMode](codecapi-avlowlatencymode.md)

As propriedades **ICodecAPI** a seguir são opcionais. Eles não são testados em HCK.

-   [CODECAPI_AVEncMPVDefaultBPictureCount](../directshow/avencmpvdefaultbpicturecount-property.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[somente aplicativos de área de trabalho Windows 7\]<br/>                                               |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh264enc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> <dt>

[Suporte a MPEG-4 no Media Foundation](mpeg-4-support-in-media-foundation.md)
</dt> <dt>

[Formatos de mídia compatíveis com o Media Foundation](supported-media-formats-in-media-foundation.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> </dl>

 

 
