---
title: Atributo UserEffectiveRating
description: O atributo UserEffectiveRating é a classificação calculada por Windows Media Player com base na frequência com que o item foi tocado.
ms.assetid: 6a420e20-f61d-4e15-84f8-a738caabd1d7
keywords:
- Atributo UserEffectiveRating Windows Media Player
topic_type:
- apiref
api_name:
- UserEffectiveRating
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 25e3244d793288fe1535c7e7cb4d44c05a3b71404531cf2ae344eb77528dd4a5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119134439"
---
# <a name="usereffectiverating-attribute"></a>Atributo UserEffectiveRating

O **atributo UserEffectiveRating** é a classificação calculada por Windows Media Player com base na frequência com que o item foi tocado.

## <a name="applies-to"></a>Aplica-se A

-   [Itens de áudio](audio-item-attributes.md)
-   [Outros itens](other-item-attributes.md)
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
|--------------------|---------------------------------------------------|
| Versão<br/> | Windows Media Player série 9 ou posterior<br/> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de atributo**](attribute-reference.md)
</dt> </dl>

 

 





