---
title: Objeto StringCollection
description: O objeto StringCollection fornece uma maneira de manipular uma coleção de cadeias de caracteres.
ms.assetid: bd4f82e7-1a6a-47c5-b019-7aff520e621a
keywords:
- Objeto StringCollection Windows Media Player
topic_type:
- apiref
api_name:
- StringCollection Object
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0d1872bec7e00e87ada845f7518608ea4149f137
ms.sourcegitcommit: 4f5016b1fbfd703dbf769c508db464c2518c0fa5
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/06/2019
ms.locfileid: "104293429"
---
# <a name="stringcollection-object"></a>Objeto StringCollection

O objeto **StringCollection** fornece uma maneira de manipular uma coleção de cadeias de caracteres.

O objeto **StringCollection** dá suporte à propriedade a seguir.



| Propriedade                            | Descrição                                             |
|-------------------------------------|---------------------------------------------------------|
| [contagem](stringcollection-count.md) | Recupera o número de itens na coleção de cadeias de caracteres. |



 

O objeto **StringCollection** dá suporte aos métodos a seguir.



| Método                                                                  | Descrição                                                                                                                     |
|-------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------|
| [getAttributeCountByType](stringcollection-getattributecountbytype.md) | Recupera o número de atributos associados ao índice do item **StringCollection** especificado, nome do atributo e idioma. |
| [getItemInfo](stringcollection-getiteminfo.md)                         | Recupera a cadeia de caracteres correspondente ao índice e nome do item **StringCollection** especificado.                                   |
| [getItemInfoByType](stringcollection-getiteminfobytype.md)             | Recupera a cadeia de caracteres correspondente ao índice, nome, idioma e índice de atributos especificados do item **StringCollection** .       |
| [isidêntico](stringcollection-isidentical.md)                         | Recupera um valor que indica se o objeto fornecido é o mesmo que o atual.                                        |
| [item](stringcollection-item.md)                                       | Recupera a cadeia de caracteres no índice especificado.                                                                                    |



 

O objeto **StringCollection** é acessado por meio do método a seguir.



| Objeto                                        | Método                                                                           |
|-----------------------------------------------|----------------------------------------------------------------------------------|
| [Mediacollection](mediacollection-object.md) | [getAttributeStringCollection](mediacollection-getattributestringcollection.md) |



 

Para fins de ilustração, *Player*. *mediacollection*. **getAttributeStringCollection**(*Attribute*, *MediaType*) é usado nas seções de sintaxe de referência.

## <a name="see-also"></a>Confira também

<dl> <dt>

[**Referência de modelo de objeto para scripts**](object-model-reference-for-scripting.md)
</dt> </dl>

 

 




