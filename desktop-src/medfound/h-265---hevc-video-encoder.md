---
description: O codificador de vídeo Media Foundation H. 265 é uma transformação Media Foundation que dá suporte à codificação de conteúdo no formato H. 265/HEVC.
ms.assetid: 790CFB39-6FC0-432D-A434-5262C30EABF4
title: Codificador de vídeo H. 265/HEVC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 015295792a72f3250c47389192586dbc00566858
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921174"
---
# <a name="h265--hevc-video-encoder"></a>Codificador de vídeo H. 265/HEVC

O codificador de vídeo Media Foundation H. 265 é uma [transformação Media Foundation](media-foundation-transforms.md) que dá suporte à codificação de conteúdo no formato H. 265/HEVC. O codificador dá suporte aos seguintes perfis:

-   Perfil Principal

O codificador de vídeo H. 265 expõe as seguintes interfaces:

-   [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)

## <a name="input-types"></a>Tipos de entrada

O tipo de mídia de entrada deve ter um dos seguintes subtipos:

-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Para obter mais informações sobre esses subtipos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

O tipo de saída deve ser definido antes do tipo de entrada. Até que o tipo de saída seja definido, o método [**IMFTransform:: SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype) do codificador retorna **MF \_ E \_ Transform \_ Type \_ não \_ definido**.

## <a name="output-types"></a>Tipos de saída

O codificador dá suporte a um subtipo de saída único:

-   **MFVideoFormat \_ H265**

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
<td>Subtipo de vídeo. Deve ser <strong>MFVideoFormat_HEVC</strong>.</td>
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
<td><a href="mf-mt-video-profile.md">MF_MT_VIDEO_PROFILE</a></td>
<td>Perfil de codificação H. 265.<br/> Os valores com suporte são: <br/>
<ul>
<li><strong>eAVEncH265VProfile_Main_420_8</strong></li>
</ul></td>
</tr>
<tr class="even">
<td><a href="mf-mt-mpeg2-level-attribute.md"><strong>MF_MT_MPEG2_LEVEL</strong></a></td>
<td>Especifica o nível do vídeo codificado. Para obter mais informações sobre restrições de perfil e de nível, consulte anexo A de ITU-T H. 265.<br/></td>
</tr>
<tr class="odd">
<td><a href="mf-mt-pixel-aspect-ratio-attribute.md"><strong>MF_MT_PIXEL_ASPECT_RATIO</strong></a></td>
<td>Opcional. Especifica a taxa de proporção de pixel. O valor padrão é 1:1.</td>
</tr>
</tbody>
</table>



 

Depois que o tipo de saída é definido, o codificador de vídeo atualiza o tipo adicionando o atributo de [**\_ cabeçalho de sequência MF MT \_ MPEG \_ \_**](mf-mt-mpeg-sequence-header-attribute.md) . Este atributo contém o cabeçalho de sequência.

## <a name="supported-imftransform-methods"></a>Métodos IMFTransform com suporte

Os métodos a seguir da interface [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) têm suporte para o codificador H. 265/HEVC:

-   [**Falha GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes)
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
-   [**ProcessEvent**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processevent)
-   [**ProcessMessage**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processmessage)
-   [**ProcessInput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processinput)
-   [**ProcessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput)
-   [**SetInputType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setinputtype)
-   [**Setoutputtypetype**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputtype)
-   [**SetOutputBounds**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-setoutputbounds)

Todos os outros métodos [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform) retornarão o erro E \_ NOTIMPL.

## <a name="supported-icodecapi-methods"></a>Métodos ICodecAPI com suporte

Os métodos a seguir da interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) têm suporte para o codificador H. 265/HEVC:

-   [**IsSupported**](/windows/win32/api/strmif/nf-strmif-icodecapi-issupported)
-   [**SetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-setvalue)
-   [**GetValue**](/windows/win32/api/strmif/nf-strmif-icodecapi-getvalue)
-   [**GetParameterRange**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparameterrange)
-   [**Parameters**](/windows/win32/api/strmif/nf-strmif-icodecapi-getparametervalues)

Todos os outros métodos [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) retornarão o erro E \_ NOTIMPL.

## <a name="codec-properties"></a>Propriedades do codec

O codificador H. 265 implementa a interface [**ICodecAPI**](/windows/win32/api/strmif/nn-strmif-icodecapi) para definir parâmetros de codificação. Ele dá suporte às propriedades a seguir.

Para obter os requisitos de codec para a certificação do codificador HCK, consulte a seção **codificador de hardware certificado** abaixo.



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
<td><a href="/windows/desktop/DirectShow/avenccommonratecontrolmode-property"><strong>CODECAPI_AVEncCommonRateControlMode</strong></a></td>
<td>Define o modo de controle de taxa. Os modos suportados são:<br/>
<ul>
<li><strong>eAVEncCommonRateControlMode_CBR</strong></li>
<li><strong>eAVEncCommonRateControlMode_Quality</strong></li>
</ul>
Se outros modos forem especificados, o controle de taxa de <strong>eAVEncCommonRateControlMode_CBR</strong> será usado.<br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmeanbitrate-property">CODECAPI_AVEncCommonMeanBitRate</a></td>
<td>Define a taxa média de bits para o fluxo de bits codificado, em bits por segundo. <br/> O intervalo válido é [1... 2 ³ ² – 1]. <br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonbuffersize-property">CODECAPI_AVEncCommonBufferSize</a></td>
<td>Define o tamanho do buffer, em bytes, para a codificação de taxa de bits constante (CBR).<br/> O intervalo válido é [1... 2 ³ ² – 1]. <br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="/windows/desktop/DirectShow/avenccommonmaxbitrate-property">CODECAPI_AVEncCommonMaxBitRate</a></td>
<td>Define a taxa de bits máxima para modos de controle de taxa que permitem uma taxa de bits de pico. <br/> O intervalo válido é [1... 2 ³ ² – 1]. <br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avencmpvgopsize-property">CODECAPI_AVEncMPVGOPSize</a></td>
<td>Define o número de imagens de um cabeçalho GOP para o seguinte, incluindo a âncora à esquerda, mas não o seguinte. <br/> O intervalo válido é [0... 2 ³ ² – 1]. Se for zero, o codificador selecionará o tamanho de GOP. O valor padrão é zero. <br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avlowlatencymode.md">CODECAPI_AVLowLatencyMode</a></td>
<td>Habilita ou desabilita o modo de baixa latência. <br/> Esse é um valor VT_BOOL.<br/></td>
</tr>
<tr class="odd">
<td><a href="/windows/desktop/DirectShow/avenccommonqualityvsspeed-property">CODECAPI_AVEncCommonQualityVsSpeed</a></td>
<td>Define a compensação de qualidade/velocidade. Esse valor afeta como o codificador executa várias operações de codificação, como compensação de movimento. Em níveis mais altos de complexidade, o codificador é executado mais lentamente, mas produz uma qualidade melhor na mesma taxa de bits. <br/> O intervalo válido é de 0 a 100. Internamente, esse valor é mapeado para um conjunto menor de níveis de qualidade/velocidade com suporte pelo codificador.<br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideoforcekeyframe.md">CODECAPI_AVEncVideoForceKeyFrame</a></td>
<td>Força o codificador a codificar o próximo quadro como um quadro-chave.<br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideoencodeqp.md">CODECAPI_AVEncVideoEncodeQP</a></td>
<td>Quando essa propriedade for definida, fará com que o codificador use a QP especificada para codificar o próximo quadro e todos os quadros subsequentes até que um novo QP seja especificado. <br/> Intervalo válido: 0 – 51, inclusivo <br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-avencvideominqp.md">CODECAPI_AVEncVideoMinQP</a></td>
<td>Essa propriedade definirá um limite no mínimo QP que o codificador pode usar durante a CBR ratecontrol.<br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencvideomaxqp.md">CODECAPI_AVEncVideoMaxQP</a></td>
<td>Essa propriedade definirá um limite no máximo QP que o codificador pode usar durante a CBR ratecontrol.<br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="even">
<td><a href="codecapi-videoencoderdisplaycontenttype.md">CODECAPI_VideoEncoderDisplayContentType</a></td>
<td>Define se o conteúdo é um vídeo de tela inteira, em oposição ao conteúdo da tela que pode ter uma janela de vídeo menor ou sem nenhum vídeo.<br/> Esse é um valor VT_UI4.<br/></td>
</tr>
<tr class="odd">
<td><a href="codecapi-avencnumworkerthreads.md">CODECAPI_AVEncNumWorkerThreads</a></td>
<td>Define o número de threads usados para executar a operação de compactação. O codificador dividirá o quadro em blocos, de modo que o número de threads seja igual ao número de blocos.<br/>
<ul>
<li>O número de processadores lógicos. O número de threads deve ser menor ou igual ao número de processadores lógicos.</li>
<li>O tamanho do quadro. O tamanho de um bloco deve ser maior ou igual a 265x64 pixels.</li>
<li>Paridade. O número de threads deve ser um valor par. Se o valor especificado for ímpar, o próximo valor inferior menor será usado.</li>
</ul>
Esse é um valor VT_UI4.<br/></td>
</tr>
</tbody>
</table>



 

## <a name="certified-hardware-encoder"></a>Codificador de hardware certificado

Se um codificador de hardware certificado estiver presente, ele geralmente será usado em vez do codificador do sistema da caixa de entrada para Media Foundation cenários relacionados. Os codificadores certificados são necessários para dar suporte a um determinado conjunto de propriedades **ICodecAPI** e, opcionalmente, podem dar suporte a outro conjunto de propriedades. O processo de certificação deve garantir que as propriedades necessárias tenham suporte adequado e, se houver suporte para uma propriedade opcional, que também tenha suporte adequado.

Veja a seguir o conjunto de propriedades obrigatórias e opcionais do **ICodecAPI** para que os codificadores passem a certificação do codificador HCK.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows 10\]<br/>                                              |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                                |
| DLL<br/>                      | <dl> <dt>Mfh265enc.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Objetos de codec](codecobjects.md)
</dt> </dl>

 

 
