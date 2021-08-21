---
title: Atributo AlbumIDAlbumArtist
description: O atributo AlbumIDAlbumArtist é um identificador exclusivo para o álbum.
ms.assetid: beaa8d01-1722-4545-8705-6b3d130113b1
keywords:
- Windows Media Player de atributo AlbumIDAlbumArtist
topic_type:
- apiref
api_name:
- AlbumIDAlbumArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4905f0448c7e08abe308a57b1ad08020d47563847db1aa32744c0de3279cdcdb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119055384"
---
# <a name="albumidalbumartist-attribute"></a>Atributo AlbumIDAlbumArtist

O atributo **AlbumIDAlbumArtist** é um identificador exclusivo para o álbum.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado somente na biblioteca do.

O identificador exclusivo é uma combinação do título do álbum e do nome do artista do álbum. Nesse atributo, o nome do artista do álbum é exibido primeiro. Quando você usa o método [mediacollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) para obter um objeto **StringCollection** usando esse atributo, os valores são classificados pelo nome do artista do álbum.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributo albumid**](albumid-attribute.md)
</dt> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





