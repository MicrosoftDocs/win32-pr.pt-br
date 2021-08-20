---
description: Largura e altura de um quadro de vídeo, em pixels.
ms.assetid: 9f10a972-406f-47ef-b71c-86ed771c9a9a
title: MF_MT_FRAME_SIZE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d0801e9fb074521c7ca22a0feb21d84687ad0d00aad8156e16733786523f6e5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118060177"
---
# <a name="mf_mt_frame_size-attribute"></a>Atributo \_ MF MT \_ FRAME \_ SIZE

Largura e altura de um quadro de vídeo, em pixels.

## <a name="data-type"></a>Tipo de dados

**UINT64**

## <a name="remarks"></a>Comentários

Os 32 bits superiores contêm a largura e os 32 bits inferiores contêm a altura.

Para definir esse atributo, use a [**função MFSetAttributeSize.**](/windows/desktop/api/mfapi/nf-mfapi-mfsetattributesize) Para obter esse atributo, use a [**função MFGetAttributeSize.**](/windows/desktop/api/mfapi/nf-mfapi-mfgetattributesize)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="examples"></a>Exemplos


```
// Helper function to set the frame size on a video media type.
inline HRESULT SetFrameSize(IMFMediaType *pType, UINT32 width, UINT32 height)
{
    return MFSetAttributeSize(pType, MF_MT_FRAME_SIZE, width, height);
}

// Helper function to get the frame size from a video media type.
inline HRESULT GetFrameSize(IMFMediaType *pType, UINT32 *pWidth, UINT32 *pHeight)
{
    return MFGetAttributeSize(pType, MF_MT_FRAME_SIZE, pWidth, pHeight);
}
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                        |
| Cabeçalho<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




