---
title: Atributo albumid
description: O atributo albumid é um identificador exclusivo para o álbum.
ms.assetid: 0412d91a-11a7-434c-8717-a71d85655679
keywords:
- Atributo albumid do Windows Media Player
topic_type:
- apiref
api_name:
- AlbumID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 339253c82554579fa549371e2ebe4cb2f1926cc5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783639"
---
# <a name="albumid-attribute"></a>Atributo albumid

O atributo **albumid** é um identificador exclusivo para o álbum.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)

## <a name="remarks"></a>Comentários

Esse atributo é armazenado somente na biblioteca do.

O identificador exclusivo é uma combinação do título do álbum e do nome do artista do álbum. Nesse atributo, o título do álbum é exibido primeiro. Quando você usa o método [mediacollection. getAttributeStringCollection](mediacollection-getattributestringcollection.md) para obter um objeto **StringCollection** usando esse atributo, os valores são classificados por título de álbum.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player 9 Series ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Atributo AlbumIDAlbumArtist**](albumidalbumartist-attribute.md)
</dt> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





