---
title: Atributo UserRating
description: O atributo UserRating é a classificação especificada pelo usuário na biblioteca.
ms.assetid: 33df5316-1506-4ecb-b729-c2d66b878825
keywords:
- Atributo UserRating Windows Media Player
topic_type:
- apiref
api_name:
- UserRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 41725119f97e0609931a3c9b7789e86d16a20507523e76a3f5642a0955998d6a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120001646"
---
# <a name="userrating-attribute"></a>Atributo UserRating

O **atributo UserRating** é a classificação especificada pelo usuário na biblioteca.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Outros itens](other-item-attributes.md)
-   [Itens de foto](photo-item-attributes.md)
-   [Playlists](playlist-attributes-ref.md)
-   [Itens de vídeo](video-item-attributes.md)

## <a name="remarks"></a>Comentários

As classificações de usuário são representadas por valores inteiros, conforme descrito na tabela a seguir. Ao especificar um valor, use um dos valores da coluna Valor de escrita. Ao recuperar valores, você pode usar os intervalos na coluna Valores de leitura para determinar o número de estrelas.



| Classificação  | Valor de escrita | Lendo valores |
|---------|---------------|----------------|
| Unrated | 0             | 0              |
| 1 estrela  | 1             | 1 a 12        |
| 2 estrelas | 25            | 13 a 37       |
| 3 estrelas | 50            | 38 a 62       |
| 4 estrelas | 75            | 63 a 86       |
| 5 estrelas | 99            | 87 a 99       |



 

Esse atributo é armazenado somente na biblioteca.

Para determinar se você pode alterar o valor desse atributo, use o [método Media.isReadOnlyItem.](media-isreadonlyitem.md)

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|--------------------|--------------------------------------------------------------------------------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior (o item de foto tem suporte apenas no Windows Media Player 10 ou posterior)<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





