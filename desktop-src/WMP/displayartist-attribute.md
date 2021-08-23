---
title: Atributo DisplayArtist
description: O atributo DisplayArtist é o nome do artista exibido para um item.
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
ms.openlocfilehash: c6c20e3d693aa7d5be5be0236d9eefebe7efcb70bc236db3f84389e5a3ceeccf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997316"
---
# <a name="displayartist-attribute"></a>Atributo DisplayArtist

O **atributo DisplayArtist** é o nome do artista exibido para um item.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)

## <a name="remarks"></a>Comentários

Em geral, **DisplayArtist** terá o mesmo valor que o **atributo WM/AlbumArtist** quando esse atributo for definido. Caso contrário, o valor será o nome do artista associado à primeira faixa do álbum.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

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

 

 





