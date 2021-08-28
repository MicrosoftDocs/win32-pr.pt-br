---
description: O Media Foundation codificador de vídeo H.265 é uma transformação Media Foundation que dá suporte à codificação de conteúdo no formato H.265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: Codificador de vídeo H.265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0b95eee96d3313df2604919883cf631b0aef999f
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/19/2021
ms.locfileid: "122467483"
---
# <a name="h265--hevc-video-encoder"></a>Codificador de vídeo H.265/HEVC

O Media Foundation codificador de vídeo H.265 é uma transformação Media Foundation que dá suporte à codificação de conteúdo no formato H.265/HEVC. [](media-foundation-transforms.md) O codificador dá suporte aos seguintes perfis:

-   Perfil Principal

O codificador de vídeo H.265 expõe as seguintes interfaces:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipos de entrada

O tipo de mídia de entrada deve ter um dos seguintes subtipos:

-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo.](video-subtype-guids.md)

O tipo de saída deve ser definido antes do tipo de entrada. Até que o tipo de saída seja definido, o método [**IMFTransform::SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) do codificador retornará **MF \_ E TRANSFORM TYPE NOT \_ \_ \_ \_ SET.**

## <a name="output-types"></a>Tipos de saída

O codificador dá suporte a um único subtipo de saída:

-   **MFVideoFormat \_ H265**

De definir os atributos a seguir no tipo de mídia de saída.




| Atributo | Descrição | 
|-----------|-------------|
| <a href="mf-mt-major-type-attribute.md"><strong>MF_MT_MAJOR_TYPE</strong></a> | Tipo principal. Deve ser <strong>MFMediaType_Video</strong>. | 
| <a href="mf-mt-subtype-attribute.md"><strong>MF_MT_SUBTYPE</strong></a> | Subtipo de vídeo. Deve ser <strong>MFVideoFormat_HEVC</strong>. | 
| <a href="mf-mt-avg-bitrate-attribute.md"><strong>MF_MT_AVG_BITRATE</strong></a> | Taxa de bits codificada média, em bits por segundo. Deve ser maior que zero. | 
| <a href="mf-mt-frame-rate-attribute.md"><strong>MF_MT_FRAME_RATE</strong></a> | Taxa de quadros. | 
| <a href="mf-mt-frame-size-attribute.md"><strong>MF_MT_FRAME_SIZE</strong></a> | Tamanho do quadro. | 
| <a href="mf-mt-interlace-mode-attribute.md"><strong>MF_MT_INTERLACE_MODE</strong></a> | Modo intercalar. | 
| <a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a> | Perfil de codificação H.265.<br /> Os valores com suporte são: <br /><ul><li><strong>eAVEncH265VProfile_Main_420_8</strong></li></ul> | 
| <a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a> | Especifica o nível do vídeo codificado. Para obter mais informações sobre restrições de perfil e nível, consulte Anexo A de ITU-T H.265.<br /> | 
| <a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a> | Opcional. Especifica a taxa de proporção de pixel. O valor padrão é 1:1. | 




 

Depois que o tipo de saída é definido, o codificador de vídeo atualiza o tipo adicionando o atributo [**\_ MT \_ MPEG \_ SEQUENCE \_ HEADER.**](mf-mt-mpeg-sequence-header-attribute.md) Esse atributo contém o header de sequência.

## <a name="supported-imftransform-methods"></a>Métodos IMFTransform com suporte

Os seguintes métodos da interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) têm suporte para o codificador H.265/HEVC:

-   [**Getattributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
-   [**GetInputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputavailabletype)
-   [**GetInputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputcurrenttype)
-   [**GetInputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstatus)
-   [**GetInputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getinputstreaminfo)
-   [**GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype)
-   [**GetOutputCurrentType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputcurrenttype)
-   [**GetOutputStatus**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstatus)
-   [**GetOutputStreamInfo**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputstreaminfo)
-   [**GetStreamCount**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamcount)
-   [**GetStreamLimits**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getstreamlimits)
-   [**Processevent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [**Processmessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [**Processoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [**Setinputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [**Setoutputtype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [**SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

Todos os [**outros métodos IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) retornarão o erro E \_ NOTIMPL.

## <a name="supported-icodecapi-methods"></a>Métodos ICodecAPI com suporte

Os seguintes métodos da interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) têm suporte para o codificador H.265/HEVC:

-   [**Issupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**Getvalue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**GetParameterValues**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Todos os [**outros métodos ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retornarão o erro E \_ NOTIMPL.

## <a name="codec-properties"></a>Propriedades do Codec

O codificador H.265 implementa a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para definir parâmetros de codificação. Ele dá suporte às propriedades a seguir.

Para ver os requisitos de codec para certificação do codificador HCK, consulte a seção **Codificador de Hardware** Certificado abaixo.




| Propriedade | Descrição | 
|----------|-------------|
| <a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a> | Define o modo de controle de taxa. Os modos suportados são:<br /><ul><li><strong>eAVEncCommonRateControlMode_CBR</strong></li><li><strong>eAVEncCommonRateControlMode_Quality</strong></li></ul>Se outros modos são especificados, o <strong>eAVEncCommonRateControlMode_CBR</strong> controle de taxa será usado.<br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a> | Define a taxa média de bits para o fluxo de bits codificado, em bits por segundo. <br /> O intervalo válido é [1 ... 2– 1]. <br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a> | Define o tamanho do buffer, em bytes, para codificação CBR (taxa de bits constante).<br /> O intervalo válido é [1 ... 2– 1]. <br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a> | Define a taxa de bits máxima para modos de controle de taxa que permitem uma taxa de bits de pico. <br /> O intervalo válido é [1 ... 2– 1]. <br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a> | Define o número de imagens de um header GOP para o próximo, incluindo a âncora à frente, mas não a seguinte. <br /> O intervalo válido é [0 ... 2– 1]. Se zero, o codificador selecionará o tamanho do GOP. O valor padrão é zero. <br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a> | Habilita ou desabilita o modo de baixa latência. <br /> Esse é um VT_BOOL valor.<br /> | 
| <a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a> | Define a troca de qualidade/velocidade. Esse valor afeta como o codificador executa várias operações de codificação, como a compensação de movimento. Em níveis de complexidade mais altos, o codificador é executado mais lentamente, mas produz melhor qualidade na mesma taxa de bits. <br /> O intervalo válido é de 0 a 100. Internamente, esse valor é mapeado para um conjunto menor de níveis de qualidade/velocidade com suporte pelo codificador.<br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a> | Força o codificador a codificar o próximo quadro como um quadro-chave.<br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a> | Quando essa propriedade for definida, o codificador usará o QP especificado para codificar o próximo quadro e todos os quadros subsequentes até que um novo QP seja especificado. <br /> Intervalo válido: 0 a 51, inclusive <br /> | 
| <a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a> | Essa propriedade definirá um limite no QP mínimo que o codificador pode usar durante o controle de taxa cbr.<br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a> | Essa propriedade definirá um limite no QP máximo que o codificador pode usar durante o controle de taxa CBR.<br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a> | Define se o conteúdo é um vídeo de tela inteira, em vez de conteúdo de tela que pode ter uma janela menor de vídeo ou não ter nenhum vídeo.<br /> Esse é um VT_UI4 valor.<br /> | 
| <a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a> | Define o número de threads usados para executar a operação de compactação. O codificador dividirá o quadro em blocos de forma que o número de threads seja igual ao número de blocos.<br /><ul><li>O número de processadores lógicos. O número de threads deve ser menor ou igual ao número de processadores lógicos.</li><li>O tamanho do quadro. O tamanho de um painel deve ser maior ou igual a 265 x 64 pixels.</li><li>Paridade. O número de threads deve ser um valor de even. Se o valor especificado for ímpar, o próximo valor menor de even será usado.</li></ul>Esse é um VT_UI4 valor.<br /> | 




 

## <a name="certified-hardware-encoder"></a>Codificador de hardware certificado

Se um codificador de hardware certificado estiver presente, ele geralmente será usado em vez do codificador do sistema de caixa de entrada para Media Foundation cenários relacionados. Codificadores certificados são necessários para dar suporte a um determinado conjunto de **propriedades ICodecAPI** e, opcionalmente, podem dar suporte a outro conjunto de propriedades. O processo de certificação deve garantir que as propriedades necessárias sejam corretamente suportadas e, se uma propriedade opcional tiver suporte, também terá suporte adequado.

A seguir está o conjunto de propriedades **ICodecAPI** necessárias e opcionais para codificadores passarem na certificação do codificador HCK.

-   [CODECAPI \_ AVEncCommonRateControlMode](../directshow/avenccommonratecontrolmode-property.md)
-   [CODECAPI \_ AVEncCommonQuality](../directshow/avenccommonquality-property.md)
-   [CODECAPI \_ AVEncCommonMeanBitRate](../directshow/avenccommonmeanbitrate-property.md)
-   [CODECAPI \_ AVEncCommonBufferSize](../directshow/avenccommonbuffersize-property.md)
-   [CODECAPI \_ AVEncMPVGOPSize](../directshow/avencmpvgopsize-property.md)
-   [CODECAPI \_ AVEncVideoEncodeQP](codecapi-avencvideoencodeqp.md)
-   [CODECAPI \_ AVEncVideoForceKeyFrame](codecapi-avencvideoforcekeyframe.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Windows 10 somente aplicativos da área de trabalho\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos codec](codecobjects.md)
</dt> </dl>

 

 
