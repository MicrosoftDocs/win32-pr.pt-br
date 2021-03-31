---
description: Define a abertura geométrica para um tipo de mídia de vídeo.
ms.assetid: a2489ba1-f322-4b63-a479-0d9879c30a8c
title: Atributo MF_MT_GEOMETRIC_APERTURE (Mfapi. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e194408dd8b6bf4a4dac717c7d41aaecbb06f306
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921267"
---
# <a name="mf_mt_geometric_aperture-attribute"></a>\_Atributo de \_ abertura geométrica do MF MT \_

Define a abertura geométrica para um tipo de mídia de vídeo.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

O valor desse atributo é uma estrutura [**MFVideoArea**](/windows/desktop/api/mfobjects/ns-mfobjects-mfvideoarea) .

A taxa de proporção da imagem é calculada em relação à abertura geométrica, usando a fórmula a seguir: taxa de proporção da imagem = (largura da abertura geométrica/altura da abertura geométrica) × taxa de proporção do pixel.

Se esse atributo não for definido, a abertura geométrica será considerada como o quadro de vídeo inteiro. Você deve definir esse atributo somente quando o tipo de mídia descrever um padrão de vídeo com uma área ativa definida.

Por exemplo, na televisão NTSC, o quadro de vídeo é 720 × 480 com uma área ativa de 704 × 480 e uma taxa de proporção de 10:11 pixels. A imagem resultante tem uma taxa de proporção de (704/480) × (10/11) = 4:3.

> [!Note]  
> O apresentador padrão para o [processador de vídeo avançado](enhanced-video-renderer.md) (EVR) mostra a abertura geométrica do vídeo, se especificado.

 

A constante de GUID para esse atributo é exportada de mfuuid. lib.

## <a name="examples"></a>Exemplos


```
HRESULT SetGeometricAperture(
    IMFMediaType *pMediaType, 
    const MFVideoArea& area
    )
{
    return pMediaType->SetBlob(
        MF_MT_GEOMETRIC_APERTURE, 
        (UINT8*)&area, 
        sizeof(MFVideoArea)
        );
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Aplicativos de \[ aplicativos \| UWP do Windows Vista desktop\]<br/>                              |
| Servidor mínimo com suporte<br/> | Aplicativos do Windows Server 2008 \[ Desktop aplicativos \| UWP\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de Media Foundation](media-foundation-attributes.md)
</dt> <dt>

[Taxa de proporção da imagem](picture-aspect-ratio.md)
</dt> <dt>

[Tipos de mídia de vídeo](video-media-types.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[**\_abertura de \_ \_ exibição mínima \_ de MF MT**](mf-mt-minimum-display-aperture-attribute.md)
</dt> <dt>

[**\_abertura de \_ digitalização de Pan MT \_ MF \_**](mf-mt-pan-scan-aperture-attribute.md)
</dt> </dl>

 

 




