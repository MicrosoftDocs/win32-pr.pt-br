---
description: O elemento Transition define um objeto de transição. Uma transição é uma transformação de duas entradas que resulta em uma transição de um fluxo (como uma composição ou faixa) para outra.
ms.assetid: d344a29f-5b6d-44a3-b1d7-759442e229f5
title: Elemento Transition
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5b7663785c641252609366c8bfd6044582829e82
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105764707"
---
# <a name="transition-element"></a>Elemento Transition

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `transition` elemento define um objeto de transição. Uma transição é uma transformação de duas entradas que resulta em uma transição de um fluxo (como uma composição ou faixa) para outra.

## <a name="attributes"></a>Atributos

[**CLSID**](clsid-attribute.md), [**cutpoint**](cutpoint-attribute.md), [**cutsonly**](cutsonly-attribute.md), [**Lock**](lock-attribute.md), [**mudo**](mute-attribute.md), [**Iniciar**](start-attribute.md), [**parar**](stop-attribute.md), [**swapinputs**](swapinputs-attribute.md), [**UserData**](userdata-attribute.md), [**userid**](userid-attribute.md), [**username**](username-attribute.md)

## <a name="parentchild-information"></a>Informações de pai/filho



|          |                                                                        |
|----------|------------------------------------------------------------------------|
| Pai   | [**composto**](composite-element.md), [ **faixa**](track-element.md) |
| Children | [**param**](param-element.md)                                         |



 

## <a name="remarks"></a>Comentários

O atributo **CLSID** especifica o subobjeto que cria a transição.

## <a name="examples"></a>Exemplos


```XML
<transition
    clsid="{2a54c913-07aa-11d2-8d6d-00c04f8ef8e0}"
    start="7"
    stop="10"
/>
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



