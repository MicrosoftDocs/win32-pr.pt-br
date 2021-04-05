---
description: Converte um fluxo de vídeo entre formatos de cor.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: Conversor de cores DSP (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 73a8418d6eeeffcf83a38452b19f18a6baa60bcc
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104457221"
---
# <a name="color-converter-dsp"></a>DSP de conversor de cores

Converte um fluxo de vídeo entre formatos de cor.

## <a name="clsid"></a>CLSID

\_CCOLORCONVERTDMO CLSID

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [IWMColorConvProps](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmcolorconvprops)

## <a name="input-formats"></a>Formatos de entrada

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   Y41P
-   Y41T
-   Y42T
-   YUY2
-   YV12
-   YVU9
-   YVYU

## <a name="output-formats"></a>Formatos de saída

-   RGB 24
-   RGB 32
-   RGB 555
-   RGB 565
-   RGB 8
-   AYUV
-   I420
-   IYUV
-   NV11
-   NV12
-   UYVY
-   V216
-   V410
-   YUY2
-   YV12
-   YVYU

## <a name="properties"></a>Propriedades

-   [MFPKEY \_ COLORCONV \_ SRCLEFT](mfpkey-colorconv-srcleft.md)
-   [MFPKEY \_ COLORCONV \_ SRCTOP](mfpkey-colorconv-srctop.md)
-   [MFPKEY \_ COLORCONV \_ DSTLEFT](mfpkey-colorconv-dstleft.md)
-   [MFPKEY \_ COLORCONV \_ DSTTOP](mfpkey-colorconv-dsttop.md)
-   [\_largura de COLORCONV MFPKEY \_](mfpkey-colorconv-width.md)
-   [\_altura de COLORCONV MFPKEY \_](mfpkey-colorconv-height.md)
-   [\_modo de COLORCONV MFPKEY \_](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Comentários

O DSP do conversor de cores é implementado como um objeto COM que pode atuar como um objeto DirectXMedia (DMO) ou uma Media Foundation transformação (MFT). O objeto tem um único identificador de classe (CLSID), independentemente de agir como um DMO ou uma MFT. Para obter informações sobre quando um DSP atua como um DMO ou uma MFT, consulte [processadores de sinais digitais](windowsmediadigitalsignalprocessors.md).

Os identificadores globalmente exclusivos (GUIDs) para subtipos de mídia RGB diferem dependendo se um DSP está agindo como um DMO ou uma MFT. Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um DSP estar agindo como um DMO ou um MFT. Para obter informações sobre os GUIDs que representam subtipos de mídia, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

Por padrão, esse DSP copia a imagem de origem inteira para o buffer de saída. Opcionalmente, você pode especificar retângulos de origem e de destino. O DSP copia a parte da imagem de origem definida pelo retângulo de origem e a grava no retângulo de destino no buffer de saída. O DSP não executa nenhum dimensionamento; os retângulos de origem e de destino devem ter o mesmo tamanho. Os retângulos de origem e de destino não podem exceder os limites do quadro de vídeo.

Todas as propriedades, exceto [**o \_ \_ modo MFPKEY COLORCONV**](mfpkey-colorconv-mode.md) , devem ser definidas em um grupo. Se você definir qualquer uma dessas propriedades, deverá definir todas as outras. Caso contrário, os retângulos de origem e de destino podem ser inválidos. nesse caso, os métodos [**IMFTransform::P rocessoutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) e [**IMediaObject::P Rocessoutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) retornarão **E \_ INVALIDARG**.

O conversor de cores não oferece suporte a todas as combinações de formato de entrada e saída. Normalmente, você deve definir o formato de mídia que você conhece, entrada ou saída e, em seguida, enumerar os formatos disponíveis no fluxo oposto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                                    |
| parâmetro<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinais digitais](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
