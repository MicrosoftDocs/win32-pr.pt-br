---
description: O elemento linear define o valor de um elemento param em um momento específico, em relação ao início da transição ou efeito que contém o elemento param.
ms.assetid: f6af4bf1-fc2d-439c-b1e3-8e095ecad503
title: Elemento linear (Camerauicontrol.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 34bff0ef1ef4c9c95752f986aabeddd24b40cc695a8a0f292b1072dfdc1d3d28
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118397140"
---
# <a name="linear-element"></a>Elemento linear

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O elemento linear define o valor de um elemento [**param**](param-element.md) em um momento específico, em relação ao início da transição ou efeito que contém o **elemento param.** O `linear` elemento faz com que o parâmetro faça uma transição suave de seu valor anterior para o novo valor. Para um salto instantâneo para um novo valor, use o [**elemento at.**](at-element.md)

## <a name="attributes"></a>Atributos

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informações pai/filho



| Rótulo | Valor |
|----------|--------------------------------|
| Pai   | [**param**](param-element.md) |
| Children | Nenhum                           |



 

## <a name="examples"></a>Exemplos


```XML
<linear time="6" value="0.0" />
```



## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------|----------------------------------------------------------------------------------------------|
| parâmetro<br/> | <dl> <dt>Camerauicontrol.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 




