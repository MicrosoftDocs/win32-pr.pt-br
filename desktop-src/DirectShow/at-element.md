---
description: O elemento at define o valor de um elemento param em um momento específico, em relação ao início da transição ou efeito que contém o parâmetro.
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: no elemento
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b5822f82a349f31f0d4c8de3f522f7f4f3346a08
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909824"
---
# <a name="at-element"></a>no elemento

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `at` elemento define o valor de um elemento [**param**](param-element.md) em um momento específico, em relação ao início da transição ou efeito que contém o parâmetro. O `at` elemento faz com que o parâmetro salte abruptamente para o novo valor no momento determinado. Para uma progressão suave para um novo valor, use o elemento [**linear**](linear-element.md) .

## <a name="attributes"></a>Atributos

[**tempo**](time-attribute.md), [ **valor**](value-attribute.md)

## <a name="parentchild-information"></a>Informações de pai/filho



| Label | Valor |
|----------|--------------------------------|
| Pai   | [**param**](param-element.md) |
| Children | Nenhum                           |



 

## <a name="examples"></a>Exemplos


```XML
<at time="1" value="0.5" />
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



