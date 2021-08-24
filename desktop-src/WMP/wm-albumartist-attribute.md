---
title: Atributo WM/AlbumArtist
description: O atributo WM/AlbumArtist é o nome do artista principal para o álbum.
ms.assetid: 9da02a85-d0cf-41e3-ad5b-08b908315993
keywords:
- Windows Media Player do atributo WM/AlbumArtist
topic_type:
- apiref
api_name:
- WM/AlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 550805894ed3744400afe0e118834b437908f173447139b2c3ebad15391288a4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761436"
---
# <a name="wmalbumartist-attribute"></a>Atributo WM/AlbumArtist

O atributo **WM/AlbumArtist** é o nome do artista principal para o álbum.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Playlists de CD](cd-playlist-attributes.md)
-   [Faixas de CD](cd-track-attributes.md)
-   [atributos de arquivo de mídia Windows usados com frequência](commonly-used-windows-media-file-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado tanto na biblioteca (ou no cache) quanto no arquivo de mídia digital.

**AlbumArtist** é um alias para este atributo.

a constante do SDK do formato de mídia Windows para esse atributo é g \_ wszWMAlbumArtist.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





