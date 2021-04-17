---
title: Atributo WM/MediaClassPrimaryID
description: O atributo WM/MediaClassPrimaryID é um GUID que especifica uma das classes de mídia primárias música, áudio não música, vídeo ou outro.
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- Atributo WM/MediaClassPrimaryID do Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5107a2c4e04e9424bf0a20a7d4cf7b8edef80492
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105797986"
---
# <a name="wmmediaclassprimaryid-attribute"></a>Atributo WM/MediaClassPrimaryID

O atributo **WM/MediaClassPrimaryID** é um GUID que especifica uma das classes de mídia primárias: música, áudio não musical, vídeo ou outro.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de rádio](radio-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca quanto no arquivo de mídia digital.

**MediaClassPrimaryID** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMMediaClassPrimaryID.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





