---
description: Converte um fluxo de vídeo entre formatos de cor.
ms.assetid: 1c15dc2b-0e69-4d16-af02-8056a1eb2c5c
title: DSP do Conversor de Cores (Wmcodecdsp.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3e97db9f3131ed7cea9076255005149544363ba8d6b548736a211973cda3999d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117880658"
---
# <a name="color-converter-dsp"></a>DSP do Conversor de Cores

Converte um fluxo de vídeo entre formatos de cor.

## <a name="clsid"></a>CLSID

CLSID \_ CColorConvertDMO

## <a name="interfaces"></a>Interfaces

-   [**Imediaobject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**Ipropertystore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
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
-   Y LTD9
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
-   [MFPKEY \_ COLORCONV \_ WIDTH](mfpkey-colorconv-width.md)
-   [MFPKEY \_ COLORCONV \_ HEIGHT](mfpkey-colorconv-height.md)
-   [MODO MFPKEY \_ \_ COLORCONV](mfpkey-colorconv-mode.md)

## <a name="remarks"></a>Comentários

O DSP do Conversor de Cores é implementado como um objeto COM que pode atuar como um objeto directXMedia (DMO) ou uma transformação Media Foundation (MFT). O objeto tem um CLSID (identificador de classe única), independentemente de atuar como um DMO ou um MFT. Para obter informações sobre quando um DSP atua como um DMO ou um MFT, consulte [Processadores de sinal digital](windowsmediadigitalsignalprocessors.md).

Os GUIDs (identificadores globalmente exclusivos) para subtipos de mídia RGB diferem dependendo se um DSP está atuando como um DMO ou um MFT. Os GUIDs para subtipos de mídia não RGB são os mesmos, independentemente de um DSP estar atuando como um DMO ou um MFT. Para obter informações sobre os GUIDs que representam subtipos de mídia, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

Por padrão, esse DSP copia toda a imagem de origem para o buffer de saída. Opcionalmente, você pode especificar retângulos de origem e de destino. O DSP copia a parte da imagem de origem definida pelo retângulo de origem e a grava no retângulo de destino no buffer de saída. O DSP não executa nenhum dimensionamento; os retângulos de origem e de destino devem ter o mesmo tamanho. Os retângulos de origem e destino não podem exceder os limites do quadro de vídeo.

Todas as propriedades, exceto [**MFPKEY \_ COLORCONV \_ MODE,**](mfpkey-colorconv-mode.md) devem ser definidas em um grupo. Se você definir qualquer uma dessas propriedades, deverá definir todas as outras. Caso contrário, os retângulos de origem e de destino poderão ser inválidos; nesse caso, os métodos [**IMFTransform::P rocessOutput**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-processoutput) e [**IMediaObject::P rocessOutput**](/previous-versions/windows/desktop/api/mediaobj/nf-mediaobj-imediaobject-processoutput) retornarão **E \_ INVALIDARG.**

O conversor de cores não dá suporte a todas as combinações de formato de entrada e formato de saída. Normalmente, você deve definir o formato de mídia que você conhece, entrada ou saída e, em seguida, enumerar os formatos disponíveis no fluxo oposto.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp.h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Colorcnv.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinal digital](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
