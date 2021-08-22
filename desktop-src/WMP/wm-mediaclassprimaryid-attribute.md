---
title: Atributo WM/MediaClassPrimaryID
description: O atributo WM/MediaClassPrimaryID é um GUID que especifica uma das classes de mídia primárias música, áudio sem música, vídeo ou outro.
ms.assetid: eb78f4a9-7c18-4cad-bb34-fd1ff15bad4f
keywords:
- Atributo WM/MediaClassPrimaryID Windows Media Player
topic_type:
- apiref
api_name:
- WM/MediaClassPrimaryID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7aebc52488ebcabfca843a8fdfdfbb51307cd96be4fe923386c718bab8752c61
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119506456"
---
# <a name="wmmediaclassprimaryid-attribute"></a>Atributo WM/MediaClassPrimaryID

O **atributo WM/MediaClassPrimaryID** é um GUID que especifica uma das classes de mídia primária: música, áudio não música, vídeo ou outros.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Atributos de arquivo de Windows mídia comumente usados](commonly-used-windows-media-file-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de rádio](radio-item-attributes.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado na biblioteca e no arquivo de mídia digital.

**MediaClassPrimaryID** é um alias para esse atributo.

A Windows constante do SDK de Formato de Mídia para esse atributo é g \_ wszWMMediaClassPrimaryID.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





