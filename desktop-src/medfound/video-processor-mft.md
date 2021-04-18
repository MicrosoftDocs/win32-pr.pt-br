---
description: O MFT do processador de vídeo é uma Microsoft Media Foundation de transformação (MFT) que executa conversão de colorspace, redimensionamento de vídeo, desentrelaçamento, conversão de taxa de quadros, rotação, corte, desempacotamento de exibição à esquerda e à direita e espelhamento.
ms.assetid: 1476995A-9692-4B08-8EF7-7DB6321BEC24
title: MFT do processador de vídeo (Camerauicontrol. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 53783b42073414e4dc440546698bf295b404dcc0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105791604"
---
# <a name="video-processor-mft"></a>MFT do processador de vídeo

O MFT do processador de vídeo é uma Microsoft Media Foundation de transformação (MFT) que executa conversão de colorspace, redimensionamento de vídeo, desentrelaçamento, conversão de taxa de quadros, rotação, corte, desempacotamento de exibição à esquerda e à direita e espelhamento.

## <a name="clsid"></a>CLSID

\_VIDEOPROCESSORMFT CLSID

## <a name="interfaces"></a>Interfaces

-   [**IMFRealTimeClientEx**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclientex)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IMFVideoProcessorControl**](/windows/desktop/api/mfidl/nn-mfidl-imfvideoprocessorcontrol)

## <a name="input-formats"></a>Formatos de entrada

-   **MFVideoFormat \_ ARGB32**
-   **MFVideoFormat \_ AYUV**
-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV11**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ RGB24**
-   **MFVideoFormat \_ RGB32**
-   **MFVideoFormat \_ RGB555**
-   **MFVideoFormat \_ RGB565**
-   **MFVideoFormat \_ RGB8**
-   **MFVideoFormat \_ UYVY**
-   **MFVideoFormat \_ v410**
-   **MFVideoFormat \_ Y216**
-   **MFVideoFormat \_ Y41P**
-   **MFVideoFormat \_ Y41T**
-   **MFVideoFormat \_ Y42T**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**
-   **MFVideoFormat \_ YVYU**

## <a name="output-formats"></a>Formatos de saída

-   **MFVideoFormat \_ ARGB32**
-   **MFVideoFormat \_ AYUV**
-   **MFVideoFormat \_ I420**
-   **MFVideoFormat \_ IYUV**
-   **MFVideoFormat \_ NV12**
-   **MFVideoFormat \_ RGB24**
-   **MFVideoFormat \_ RGB32**
-   **MFVideoFormat \_ RGB555**
-   **MFVideoFormat \_ RGB565**
-   **MFVideoFormat \_ UYVY**
-   **MFVideoFormat \_ Y216**
-   **MFVideoFormat \_ YUY2**
-   **MFVideoFormat \_ YV12**

Nem todas as combinações de formatos de entrada e saída têm suporte. Para testar se há suporte para uma conversão, defina o tipo de entrada e, em seguida, chame [**IMFTransform:: GetOutputAvailableType**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getoutputavailabletype).

Para obter mais informações sobre esses formatos, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

## <a name="remarks"></a>Comentários

Uma instância do processador de vídeo pode ser criada de uma das seguintes maneiras:

-   Chamando [**MFTEnumEx**](/windows/desktop/api/mfapi/nf-mfapi-mftenumex). O processador de vídeo é registrado sob a categoria **MFT do \_ \_ \_ processador de vídeo** categoria.
-   Chamando a função COM **CoCreateInstance** passando-a para o CLSID **CLSID \_ VideoProcessorMFT**.

Os comentários a seguir pertencem ao trabalho com retângulos de origem e retângulos de destino na **MFT do processador de vídeo**. Os retângulos de origem e de destino são definidos com [**IMFVideoProcessorControl:: SetDestinationRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setdestinationrectangle) e [**SetSourceRectangle**](/windows/desktop/api/mfidl/nf-mfidl-imfvideoprocessorcontrol-setsourcerectangle) e algumas vezes com [**IMFMediaEngineEx:: UpdateVideoStream**](/windows/desktop/api/mfmediaengine/nf-mfmediaengine-imfmediaengineex-updatevideostream).

-   O retângulo de origem deve ser alinhado e arredondado para corresponder aos requisitos do formato de cor do quadro inserido no processador de vídeo. Isso é importante porque formatos como 420 e 422 têm requisitos sobre as dimensões e os deslocamentos que podem ser criados e acessados. Por exemplo, um retângulo de origem de {1, 0, 319, 240} (esquerda, superior, direita, inferior) será arredondado para {2, 0, 320, 240} quando o formato de entrada for 420.
-   O destino e o retângulo de origem sempre serão clamped para caber dentro de seus respectivos quadros — o retângulo de origem para o quadro de origem e o retângulo de destino para o quadro de destino. Isso significa que valores negativos não são significativos — eles serão sempre clamped para 0.
-   O retângulo de origem está no sistema de coordenadas do quadro de destino, menos qualquer retângulo de destino. Isso significa que as transformações como a rotação são "desfeitas" no retângulo de origem. Portanto, você não precisa saber se o vídeo foi girado ou 3D desempacotado. Por exemplo, você pode desenhar um retângulo sobre a marca de vídeo, pegar as coordenadas relativas (em relação à marca de vídeo), Normalize-las (intervalo de 0 a 1) e passá-las como o retângulo de origem e elas devem funcionar conforme o esperado, mesmo se o vídeo estiver sendo girado.

O processador de vídeo dá suporte ao processamento de vídeo acelerado por GPU, usando o Microsoft Direct3D 11. Para obter mais informações, consulte [MF \_ SA \_ D3D11 \_ Aware](mf-sa-d3d11-aware.md).

### <a name="stereoscopic-video"></a>Vídeo do estereoscópico

O processador de vídeo dá suporte à operação exibir desempacotamento em quadros de vídeo 3D:

Se o quadro de entrada contiver dois modos de exibição compactados no mesmo quadro, o processador de vídeo poderá dividir as exibições em buffers separados ou extrair a exibição de base e descartar a segunda exibição. Para habilitar o desempacotamento de View, defina o atributo de [ \_ \_ \_ saída MF Enable 3DVIDEO](mf-enable-3dvideo-output.md) para **MF3DVideoOutputType \_ estéreo** ou **MF3DVideoOutputType \_ BaseView**.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Camerauicontrol. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinais digitais](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




