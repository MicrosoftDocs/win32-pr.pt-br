---
title: Atributo do WM/gênero
description: O atributo WM/gênero é o gênero do conteúdo.
ms.assetid: 4b1b0512-d8fd-402a-a5f0-1002c64194f4
keywords:
- Windows Media Player de atributo do WM/gênero
topic_type:
- apiref
api_name:
- WM/Genre
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cd0ef67b0b41ff59f644b0d52376428ae7a2330d388aa62f9765cb4842eeb561
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120000976"
---
# <a name="wmgenre-attribute"></a>Atributo do WM/gênero

O atributo **WM/gênero** é o gênero do conteúdo.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)
-   [DVDs](dvd-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

Esse atributo pode ter vários valores. Para recuperar todos os valores de um atributo com valores múltiplos, você deve usar o método **Media. getItemInfoByType** , não o método **Media. getItemInfo** .

**Gênero** é um alias para este atributo.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMGenre.

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

 

 





