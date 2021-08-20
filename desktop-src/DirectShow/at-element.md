---
description: O elemento at define o valor de um elemento param em um momento específico, em relação ao início da transição ou efeito que contém o parâmetro .
ms.assetid: 523aa25c-790b-4532-9c69-76544235bdfe
title: Elemento at
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4d67a5e3c3ca2bd47381084ad0e0090d7aa208db87f35e5efe3a7d805a73d097
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117824386"
---
# <a name="at-element"></a>Elemento at

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O elemento define o valor de um elemento param em um determinado momento, em relação ao início da transição ou `at` efeito que contém o parâmetro . [](param-element.md) O `at` elemento faz com que o parâmetro pule repentinamente para o novo valor no momento determinado. Para uma progressão suave para um novo valor, use o [**elemento linear.**](linear-element.md)

## <a name="attributes"></a>Atributos

[**time**](time-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informações pai/filho



| Rótulo | Valor |
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

 

 



