---
description: O elemento composto define uma composição, um objeto de contêiner para faixas e outras composições aninhadas.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento composite
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dec9ce7c889829ee227ce31df25d5d17985e877ed107870170f6939aebf14fd3
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120084306"
---
# <a name="composite-element"></a>Elemento composite

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `composite` elemento define uma composição, um objeto de contêiner para faixas e outras composições aninhadas.

## <a name="attributes"></a>Atributos

[**lock**](lock-attribute.md), [**mute**](mute-attribute.md), [**userdata**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informações pai/filho



| Rótulo | Valor |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Pai   | `composite`, [ **grupo**](group-element.md)                                                                             |
| Children | `composite`, [**efeito**](effect-element.md), [**acompanhar**](track-element.md), [**transição**](transition-element.md) |



 

## <a name="remarks"></a>Comentários

Dentro de `composite` um elemento, a prioridade das camadas aninhadas é determinada implicitamente pela ordem em que elas aparecem dentro do elemento . A primeira camada tem prioridade 0 e as camadas subsequentes têm valores de prioridade crescentes.

## <a name="examples"></a>Exemplos


```XML
<composite> </composite>
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



