---
title: Atributo do WM/gênero
description: O atributo WM/gênero é o gênero do conteúdo.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Atributo do WM/gênero Windows Media Player
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: aae4a0c6ae27e85fa1ed147a3173c4cc31b20f1b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105765299"
---
# <a name="wmgenre-attribute"></a>Atributo do WM/gênero

O atributo **WM/gênero** é o gênero do conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [Atributos de arquivo de mídia do Windows comumente usados](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

Esse atributo pode ter vários valores. Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar o método **Media. getItemInfoByType** , não o método **Media. getItemInfo** .

**Gênero** é um alias para este atributo.

A constante do Windows Media Format SDK para esse atributo é g \_ wszWMGenre.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> <dt>

[**Media. getItemInfoByType**](media-getiteminfobytype.md)
</dt> </dl>

 

 





