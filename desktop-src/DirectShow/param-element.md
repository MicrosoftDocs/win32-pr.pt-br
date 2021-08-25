---
description: O elemento param especifica o valor de uma propriedade em uma transição, efeito ou outro subobjeto.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 35c58543c5daae7ad0a77f6380bc3f3db48cf8443461eaf919c4c727163436cb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120050816"
---
# <a name="param-element"></a>Elemento param

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `param` elemento especifica o valor de uma propriedade em uma transição, efeito ou outro subobjeto.

## <a name="attributes"></a>Atributos

[**name**](name-attribute.md), [ **value**](value-attribute.md)

## <a name="parentchild-information"></a>Informações pai/filho



| Rótulo | Valor |
|----------|----------------------------------------------------------------------------------------------------------|
| Pai   | [**clip**](clip-element.md), [**effect**](effect-element.md), [**transition**](transition-element.md) |
| Children | [**em**](at-element.md), [ **linear**](linear-element.md)                                               |



 

## <a name="remarks"></a>Comentários

O **atributo** value especifica o valor da propriedade no início da transição ou efeito. Use o **elemento em** ou **linear** para especificar valores de alteração. Se o **elemento param** não contiver **nenhum elemento** **linear** ou , o valor permanecerá constante durante a duração do efeito ou da transição.

> [!Note]  
> Um **elemento param** dentro de um **elemento clip** não pode conter **elementos** **lineares ou** .

 

Muitas transições suportam uma propriedade **Progress** padrão que varia de 0 a 1,0, indicando qual percentual da transição é refletido na saída. Em **Andamento** = 0,0, a transição está no início de sua sequência (inteiramente a primeira imagem de vídeo). Em **Andamento** = 0,5, a transição está pela metade concluída. (Por exemplo, em um apagando, em **Progresso** = 0,5, o limite de transição está no centro da imagem) Em **Andamento** = 1,0, a transição é concluída (inteiramente a segunda imagem). Por padrão, as transições vão **de Progresso** = 0,0 no início da transição para **Progresso** = 1,0 no final.

Outras propriedades geralmente são específicas para uma transição ou efeito específico. Por exemplo, a transição de apagaamento dá suporte a **uma propriedade GradientSize** que controla a largura da área de transição.

Para executar uma transição para trás, de definido a propriedade **Progress** como 1.0 no início da transição e use o elemento **linear** para alterar o valor para 0,0, conforme mostrado no exemplo a seguir:


```
<transition clsid="{af279b30-86eb-11d1-81bf-0000f87557db}" start="0" stop="6">
    <param name="progress" value="1.0">
        <linear time="6" value="0.0" />
    </param>
</transition>
```



## <a name="examples"></a>Exemplos


```XML
<param name="progress" value="1.0" />
```



## <a name="see-also"></a>Confira também

<dl> <dt>

[Elementos XTL](xtl-elements.md)
</dt> </dl>

 

 



