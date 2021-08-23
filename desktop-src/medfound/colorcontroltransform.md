---
description: Ajusta as características de cor de um fluxo de vídeo.
ms.assetid: 738c1f0c-8417-4b12-a7f1-9bbf3c7e9dd3
title: DSP de transformação de controle de cores (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3c51321a8ffd725306f570619b9bcbe70fe7160e784358ce265157145b40347e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119606206"
---
# <a name="color-control-transform-dsp"></a>DSP de transformação de controle de cores

Ajusta as características de cor de um fluxo de vídeo.

## <a name="clsid"></a>CLSID

\_CCOLORCONTROLDMO CLSID

## <a name="interfaces"></a>Interfaces

-   **IMediaObject**
-   **IMFTransform**
-   **IPropertyStore**

## <a name="formats"></a>Formatos

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   AYUV
-   UYVY
-   YUY2
-   YV12

## <a name="properties"></a>Propriedades

-   [\_brilho da cor do MFPKEY \_](mfpkey-color-brightness.md)
-   [\_contraste de cor do MFPKEY \_](mfpkey-color-contrast.md)
-   [\_matiz de cor de MFPKEY \_](mfpkey-color-hue.md)
-   [\_saturação de cor MFPKEY \_](mfpkey-color-saturation.md)

## <a name="remarks"></a>Comentários

Esse DSP modifica o conteúdo do fluxo de vídeo. Para reprodução, você pode conseguir efeitos semelhantes com mais eficiência usando a interface **IMFVideoProcessor** , que controla o processamento de vídeo na placa gráfica.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Mfvdsp.dll</dt> </dl>   |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinais digitais](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 




