---
description: Especifica o retângulo de origem para o mixer de vídeo do processador de vídeo avançado (EVR). O retângulo de origem é a parte do quadro de vídeo que o mixer blits para a superfície de destino.
ms.assetid: 4364ff87-816e-4b64-b5e9-c53dd6c9bb33
title: Atributo VIDEO_ZOOM_RECT (EVR. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dda4efca5beab844baf3b3f53074d6b3012e8621
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105759017"
---
# <a name="video_zoom_rect-attribute"></a>\_Atributo Rect de zoom de vídeo \_

Especifica o retângulo de origem para o mixer de vídeo do [processador de vídeo avançado](enhanced-video-renderer.md) (EVR). O retângulo de origem é a parte do quadro de vídeo que o mixer blits para a superfície de destino.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

O valor desse atributo é uma estrutura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .

O retângulo de origem é definido em relação a um sistema de coordenadas normalizado, no qual todo o quadro de vídeo ocupa um retângulo com coordenadas {0, 0, 1, 1}. O retângulo de origem deve caber no quadro de vídeo; as coordenadas do retângulo de origem têm um intervalo de (0... 1).

O apresentador EVR padrão define esse atributo no mixer. Para definir o atributo, faça o seguinte:

1.  Chame [**IMFTransform:: GetAttributes**](/windows/desktop/api/mftransform/nf-mftransform-imftransform-getattributes) no mixer para obter o repositório de atributos do mixer.
2.  Chame [**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob) para definir o atributo de **\_ \_ retângulo de zoom de vídeo** no mixer. O valor é uma estrutura [**MFVideoNormalizedRect**](/windows/desktop/api/evr/ns-evr-mfvideonormalizedrect) .

Em um apresentador personalizado do EVR, você pode usar esse atributo para implementar o método [**IMFVideoDisplayControl:: SetVideoPosition**](/windows/desktop/api/evr/nf-evr-imfvideodisplaycontrol-setvideoposition) . Para obter mais informações, consulte [retângulos de origem e de destino](how-to-write-an-evr-presenter.md).

A constante de GUID para esse atributo é exportada de strmiids. lib.

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
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                   |
| Servidor mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Server 2008\]<br/>                             |
| parâmetro<br/>                   | <dl> <dt>EVR. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de atributos de Media Foundation](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[Atributos avançados de processador de vídeo](enhanced-video-renderer-attributes.md)
</dt> <dt>

[Como escrever um apresentador EVR](how-to-write-an-evr-presenter.md)
</dt> <dt>

[**IMFAttributes:: getBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes:: setBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> </dl>

 

 




