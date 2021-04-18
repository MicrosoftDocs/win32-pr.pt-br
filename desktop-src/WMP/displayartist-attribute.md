---
title: Atributo DisplayArtist
description: O atributo DisplayArtist é o nome do artista que é exibido para um item.
ms.assetid: 8cf5a4e6-ce96-4fd4-b01a-6cd4264a5c09
keywords:
- Atributo DisplayArtist Windows Media Player
topic_type:
- apiref
api_name:
- DisplayArtist
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 44d479add519d8b7df346869e783c36560fc46dc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105760268"
---
# <a name="displayartist-attribute"></a>Atributo DisplayArtist

O atributo **DisplayArtist** é o nome do artista que é exibido para um item.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)

## <a name="remarks"></a>Comentários

Em geral, **DisplayArtist** terá o mesmo valor que o atributo **WM/AlbumArtist** quando esse atributo for definido. Caso contrário, o valor será o nome do artista associado à primeira faixa no álbum.

Para determinar se você pode alterar o valor desse atributo, use o método [Media. isReadOnlyItem](media-isreadonlyitem.md) .

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|------------------------------------|
| Versão<br/> | Windows Media Player 11<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> <dt>

[**Atributo WM/AlbumArtist**](wm-albumartist-attribute.md)
</dt> </dl>

 

 





