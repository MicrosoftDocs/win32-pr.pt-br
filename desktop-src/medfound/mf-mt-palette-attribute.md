---
description: Contém as entradas da paleta para um tipo de mídia de vídeo. Use esse atributo para formatos de vídeo palettized, como RGB 8.
ms.assetid: 3efc124b-073e-4c48-9550-c100e29f2d6f
title: MF_MT_PALETTE atributo (Mfapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0a20623262be0129cabf5675fd4cd1a37ec2fb61b6b9a0dd5e135fa9e48e1abb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118741651"
---
# <a name="mf_mt_palette-attribute"></a>Atributo \_ MF MT \_ PALETTE

Contém as entradas da paleta para um tipo de mídia de vídeo. Use esse atributo para formatos de vídeo palettized, como RGB 8.

## <a name="data-type"></a>Tipo de dados

Matriz de bytes

## <a name="remarks"></a>Comentários

Os dados de atributo são uma matriz de [**uniões MFPaletteEntry.**](/windows/win32/api/mfobjects/ns-mfobjects-mfpaletteentry)

A constante GUID para esse atributo é exportada de mfuuid.lib.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Aplicativos \| UWP de aplicativos da área de trabalho do Vista\]<br/>                              |
| Servidor mínimo com suporte<br/> | Windows Aplicativos \[ UWP do Server 2008 Desktop \|\]<br/>                        |
| parâmetro<br/>                   | <dl> <dt>Mfapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Lista alfabética de Media Foundation atributos](alphabetical-list-of-media-foundation-attributes.md)
</dt> <dt>

[**IMFAttributes::GetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-getblob)
</dt> <dt>

[**IMFAttributes::SetBlob**](/windows/desktop/api/mfobjects/nf-mfobjects-imfattributes-setblob)
</dt> <dt>

[**IMFMediaType**](/windows/desktop/api/mfobjects/nn-mfobjects-imfmediatype)
</dt> <dt>

[Atributos de tipo de mídia](media-type-attributes.md)
</dt> </dl>

 

 




