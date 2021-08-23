---
description: Redimensiona um fluxo de vídeo.
ms.assetid: 4acd6366-1abf-43f3-b6c9-4ea17a335cec
title: DSP de redimensionador de vídeo (Wmcodecdsp. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58d26dcc53baf38336656d870acc5583066e0816a0bf963217db1da54513ee18
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119721315"
---
# <a name="video-resizer-dsp"></a>DSP de redimensionador de vídeo

Redimensiona um fluxo de vídeo.

## <a name="clsid"></a>CLSID

\_CRESIZERDMO CLSID

## <a name="interfaces"></a>Interfaces

-   [**IMediaObject**](/previous-versions/windows/desktop/api/mediaobj/nn-mediaobj-imediaobject)
-   [**IMFRealTimeClient**](/windows/desktop/api/mfidl/nn-mfidl-imfrealtimeclient)
-   [**IMFTransform**](/windows/desktop/api/mftransform/nn-mftransform-imftransform)
-   [**IPropertyStore**](/windows/win32/api/propsys/nn-propsys-ipropertystore)
-   [**IWMResizerProps**](/windows/desktop/api/wmcodecdsp/nn-wmcodecdsp-iwmresizerprops)

## <a name="formats"></a>Formatos

O DSP do redimensionador de vídeo dá suporte aos seguintes subtipos de mídia de entrada/saída quando ele está agindo como um objeto de mídia DirectX (DMO).

-   MEDIASUBTYPE \_ IYUV
-   MEDIASUBTYPE \_ YUY2
-   MEDIASUBTYPE \_ UYVY
-   MEDIASUBTYPE \_ I420
-   MEDIASUBTYPE \_ RGB32
-   MEDIASUBTYPE \_ RGB24
-   MEDIASUBTYPE \_ RGB565
-   MEDIASUBTYPE \_ RGB8
-   MEDIASUBTYPE \_ RGB555
-   MEDIASUBTYPE \_ AYUV
-   MEDIASUBTYPE \_ V216
-   MEDIASUBTYPE \_ YV12

O DSP do redimensionador de vídeo dá suporte aos seguintes subtipos de mídia de entrada/saída quando está atuando como uma Media Foundation transformação (MFT).

-   MFVideoFormat \_ IYUV
-   MFVideoFormat \_ YUY2
-   MFVideoFormat \_ UYVY
-   MFVideoFormat \_ I420
-   MFVideoFormat \_ RGB32
-   MFVideoFormat \_ RGB24
-   MFVideoFormat \_ RGB565
-   MFVideoFormat \_ RGB8
-   MFVideoFormat \_ RGB555
-   MFVideoFormat \_ AYUV
-   MFVideoFormat \_ V216
-   MFVideoFormat \_ YV12

## <a name="properties"></a>Propriedades

-   [MFPKEY \_ redimensionar \_ src \_ Left](mfpkey-resize-src-left.md)
-   [MFPKEY \_ redimensionar \_ src \_ superior](mfpkey-resize-src-top.md)
-   [\_largura de src de redimensionamento MFPKEY \_ \_](mfpkey-resize-src-width.md)
-   [MFPKEY \_ dimensionar \_ altura de src \_](mfpkey-resize-src-height.md)
-   [MFPKEY \_ redimensionar o \_ DST \_ esquerdo](mfpkey-resize-dst-left.md)
-   [MFPKEY \_ redimensionar o \_ DST \_ superior](mfpkey-resize-dst-top.md)
-   [\_largura de hora de redimensionamento MFPKEY \_ \_](mfpkey-resize-dst-width.md)
-   [MFPKEY \_ redimensionar a \_ altura do horário de verão \_](mfpkey-resize-dst-height.md)
-   [\_qualidade de redimensionamento MFPKEY \_](mfpkey-resize-quality.md)
-   [MFPKEY \_ redimensionar \_ entrelaçamento](mfpkey-resize-interlace.md)
-   [MFPKEY \_ redimensionar \_ GEOMAPX](mfpkey-resize-geomapx.md)
-   [MFPKEY \_ redimensionar \_ GEOMAPY](mfpkey-resize-geomapy.md)
-   [MFPKEY \_ redimensionar \_ GEOMAPWIDTH](mfpkey-resize-geomapwidth.md)
-   [MFPKEY \_ redimensionar \_ GEOMAPHEIGHT](mfpkey-resize-geomapheight.md)
-   [MFPKEY \_ redimensionar \_ MINAPX](mfpkey-resize-minapx.md)
-   [MFPKEY \_ redimensionar \_ MINAPY](mfpkey-resize-minapy.md)
-   [MFPKEY \_ redimensionar \_ MINAPWIDTH](mfpkey-resize-minapwidth.md)
-   [MFPKEY \_ redimensionar \_ MINAPHEIGHT](mfpkey-resize-minapheight.md)
-   [MFPKEY \_ redimensionar \_ PANSCANAPX](mfpkey-resize-panscanapx.md)
-   [MFPKEY \_ redimensionar \_ PANSCANAPY](mfpkey-resize-panscanapy.md)
-   [MFPKEY \_ redimensionar \_ PANSCANAPWIDTH](mfpkey-resize-panscanapwidth.md)
-   [MFPKEY \_ redimensionar \_ PANSCANAPHEIGHT](mfpkey-resize-panscanapheight.md)
-   [MFPKEY \_ PIXELASPECTRATIO](mfpkey-pixelaspectratio.md)

## <a name="remarks"></a>Comentários

o DSP do redimensionador de vídeo é implementado como um objeto COM que pode atuar como um DMO ou um MFT. o objeto tem um único identificador de classe (CLSID), independentemente de agir como um DMO ou um MFT. para obter informações sobre quando um DSP atua como um DMO ou uma MFT, consulte [processadores de sinais digitais](windowsmediadigitalsignalprocessors.md).

os identificadores globalmente exclusivos (guids) para subtipos de mídia RGB diferem dependendo se um DSP está agindo como um DMO ou um MFT. os guids para subtipos de mídia não RGB são os mesmos, independentemente de um DSP estar agindo como um DMO ou um MFT. Para obter informações sobre os GUIDs que representam subtipos de mídia, consulte [GUIDs de subtipo de vídeo](video-subtype-guids.md).

Esse DSP pode executar o corte e o dimensionamento na imagem de vídeo. O formato do tipo de saída deve corresponder ao formato do tipo de entrada. O DSP não executa conversões de espaço em cores.

Antes de definir o tipo de saída, você pode definir qualquer uma das seguintes regiões usando as propriedades listadas nesta tabela.



| Região                   | Propriedades                                                                                                                                                       |
|--------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Retângulo de origem         | MFPKEY \_ redimensionar \_ src \_ Left<br/> MFPKEY \_ redimensionar \_ src \_ superior<br/> \_largura de src de redimensionamento MFPKEY \_ \_<br/> MFPKEY \_ dimensionar \_ altura de src \_<br/>            |
| Retângulo de destino    | MFPKEY \_ redimensionar o \_ DST \_ esquerdo<br/> MFPKEY \_ redimensionar o \_ DST \_ superior<br/> \_largura de hora de redimensionamento MFPKEY \_ \_<br/> MFPKEY \_ redimensionar a \_ altura do horário de verão \_<br/>            |
| Abertura geométrica       | MFPKEY \_ redimensionar \_ GEOMAPX<br/> MFPKEY \_ redimensionar \_ GEOMAPY<br/> MFPKEY \_ redimensionar \_ GEOMAPWIDTH<br/> MFPKEY \_ redimensionar \_ GEOMAPHEIGHT<br/>             |
| Abertura de exibição mínima | MFPKEY \_ redimensionar \_ MINAPX<br/> MFPKEY \_ redimensionar \_ MINAPY<br/> MFPKEY \_ redimensionar \_ MINAPWIDTH<br/> MFPKEY \_ redimensionar \_ MINAPHEIGHT<br/>                 |
| Região de panorâmica/verificação          | MFPKEY \_ redimensionar \_ PANSCANAPX<br/> MFPKEY \_ redimensionar \_ PANSCANAPY<br/> MFPKEY \_ redimensionar \_ PANSCANAPWIDTH<br/> MFPKEY \_ redimensionar \_ PANSCANAPHEIGHT<br/> |



 

Em cada caso, você deve definir todas as propriedades associadas para que a configuração entre em vigor.

O DSP copia a parte da imagem de origem definida pelo retângulo de origem e a amplia ou compacta para o retângulo de destino no buffer de saída. Os retângulos de origem e de destino não precisam ter o mesmo tamanho. O tamanho do quadro no tipo de mídia de saída deve ser grande o suficiente para conter o retângulo de destino.

A abertura geométrica, a abertura de exibição mínima e a região de panorâmica/verificação não afetam o modo como o DSP redimensiona o vídeo. No entanto, eles podem afetar como o componente downstream interpreta o quadro de vídeo. Em particular, o processador de vídeo avançado (EVR) usa esses valores quando calcula a taxa de proporção da imagem e a área de exibição.

Se você estiver usando Media Foundation tipos de mídia, poderá definir a abertura geométrica, a abertura de exibição mínima e as regiões de panorâmica/verificação diretamente no tipo de mídia de saída. caso contrário, se você estiver usando DMO tipos de mídia, defina-os usando as propriedades.

Para obter mais informações, consulte estes tópicos:

-   [**\_ \_ abertura geométrica do MF MT \_**](mf-mt-geometric-aperture-attribute.md)
-   [**\_abertura de \_ \_ exibição mínima \_ de MF MT**](mf-mt-minimum-display-aperture-attribute.md)
-   [**\_abertura de \_ digitalização de Pan MT \_ MF \_**](mf-mt-pan-scan-aperture-attribute.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                          |
| Servidor mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do servidor 2008\]<br/>                                    |
| Cabeçalho<br/>                   | <dl> <dt>Wmcodecdsp. h</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vidreszr.dll</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Processadores de sinais digitais](windowsmediadigitalsignalprocessors.md)
</dt> </dl>

 

 
