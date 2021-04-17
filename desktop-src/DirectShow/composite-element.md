---
description: O elemento composto define uma composição, um objeto de contêiner para faixas e outras composições aninhadas.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento composto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7a1c81bf445769c049287bdfa7d23f4ab82bb0f8
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "105775624"
---
# <a name="composite-element"></a>Elemento composto

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `composite` elemento define uma composição, um objeto de contêiner para faixas e outras composições aninhadas.

## <a name="attributes"></a>Atributos

[**Lock**](lock-attribute.md), [**mudo**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informações de pai/filho



|          |                                                                                                                         |
|----------|-------------------------------------------------------------------------------------------------------------------------|
| Pai   | `composite`, [ **grupo**](group-element.md)                                                                             |
| Children | `composite`, [**efeito**](effect-element.md), [**controle**](track-element.md), [**transição**](transition-element.md) |



 

## <a name="remarks"></a>Comentários

Dentro de um `composite` elemento, a prioridade de camadas aninhadas é determinada implicitamente pela ordem em que aparecem dentro do elemento. A primeira camada tem a prioridade 0 e as camadas subsequentes têm valores de prioridade crescentes.

## <a name="examples"></a>Exemplos


```XML
<composite> </composite>
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



