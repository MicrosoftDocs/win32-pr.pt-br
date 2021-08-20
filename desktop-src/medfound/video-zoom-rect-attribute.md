---
description: Especifica o retângulo de origem para o mixer de vídeo do EVR (Renderização de Vídeo Aprimorado). O retângulo de origem é a parte do quadro de vídeo que o mixer blitsa para a superfície de destino.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: VIDEO_ZOOM_RECT atributo (Evr.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c2e6ce19c808545d400f53b9c0091cdbcc20c8efbc13372ae5386e419d244143
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118737141"
---
# <a name="video_zoom_rect-attribute"></a>Atributo VIDEO \_ ZOOM \_ RECT

Especifica o retângulo de origem para o mixer de vídeo do EVR [(Renderização](enhanced-video-renderer.md) de Vídeo Aprimorado). O retângulo de origem é a parte do quadro de vídeo que o mixer blitsa para a superfície de destino.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

O valor desse atributo é uma [**estrutura MFVideoNormalizedRect.**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect)

O retângulo de origem é definido em relação a um sistema de coordenadas normalizado, no qual todo o quadro de vídeo ocupa um retângulo com coordenadas {0, 0, 1, 1}. O retângulo de origem deve caber no quadro de vídeo; as coordenadas do retângulo de origem têm um intervalo de (0...1).

O apresentador EVR padrão define esse atributo no mixer. Para definir o atributo, faça o seguinte:

1.  Chame [**IMFTransform::GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no mixer para obter o armazenamento de atributos do mixer.
2.  Chame [**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) para definir o atributo **VIDEO ZOOM \_ \_ RECT** no mixer. O valor é uma [**estrutura MFVideoNormalizedRect.**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect)

Em um apresentador de EVR personalizado, você pode usar esse atributo para implementar o método [**IMFVideoDisplayControl::SetVideoPosition.**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) Para obter mais informações, consulte [Retângulos de origem e destino.](how-to-write-an-evr-presenter.md)

A constante GUID para esse atributo é exportada de strmiids.lib.

## <a name="examples"></a>Exemplos

O exemplo a seguir define o retângulo de origem no mixer.


```C++
HRESULT SetMixerSourceRect(IMFTransform *pMixer, const MFVideoNormalizedRect& nrcSource)
{
    if (pMixer == NULL)
    {
        return E_POINTER;
    }

    IMFAttributes *pAttributes = NULL;

    HRESULT hr = pMixer->GetAttributes(&pAttributes);
    if (SUCCEEDED(hr))
    {
        hr = pAttributes->SetBlob(VIDEO_ZOOM_RECT, (const UINT8*)&nrcSource, sizeof(nrcSource));
        pAttributes->Release();
    }
    return hr;
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|----------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2008 \[\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>Evr.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos de renderização de vídeo aprimorados](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Como escrever um apresentador de EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




