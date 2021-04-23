---
description: O elemento composto define uma composição, um objeto de contêiner para faixas e outras composições aninhadas.
ms.assetid: 7551da3a-1da6-426a-ba9d-f715df53718f
title: Elemento composto
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5eff3e0c16040f837e4c8a792ebac3124d723d1
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107908834"
---
# <a name="composite-element"></a>Elemento composto

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `composite` elemento define uma composição, um objeto de contêiner para faixas e outras composições aninhadas.

## <a name="attributes"></a>Atributos

[**Lock**](lock-attribute.md), [**mudo**](mute-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informações de pai/filho



| Label | Valor |
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

 

 



