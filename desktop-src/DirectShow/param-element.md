---
description: O elemento param especifica o valor de uma propriedade em uma transição, efeito ou outro subobjeto.
ms.assetid: a727c47c-b925-436c-b1e8-d5f407120dc9
title: Elemento param (DirectShow)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8a10f902e85066f6cea14023e8cff9250126add0
ms.sourcegitcommit: 63753fcfb0afbbe5ec283fb8316e62c2dc950f66
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/22/2021
ms.locfileid: "107909034"
---
# <a name="param-element"></a>Elemento param

> [!Note]  
> \[Preterido. Essa API pode ser removida de versões futuras do Windows.\]

 

O `param` elemento Especifica o valor de uma propriedade em uma transição, efeito ou outro subobjeto.

## <a name="attributes"></a>Atributos

[**nome**](name-attribute.md), [ **valor**](value-attribute.md)

## <a name="parentchild-information"></a>Informações de pai/filho



| Label | Valor |
|----------|----------------------------------------------------------------------------------------------------------|
| Pai   | [**clip**](clip-element.md), [**efeito**](effect-element.md), [**transição**](transition-element.md) |
| Children | [**em**](at-element.md), [ **linear**](linear-element.md)                                               |



 

## <a name="remarks"></a>Comentários

O atributo **Value** especifica o valor da propriedade no início da transição ou efeito. Use o elemento **at** ou **linear** para especificar valores de alteração. Se o elemento **param** não contiver elementos **at** ou **lineares** , o valor permanecerá constante ao longo da duração do efeito ou da transição.

> [!Note]  
> Um elemento **param** dentro de um elemento **clip** não pode conter elementos **at** ou **lineares** .

 

Muitas transições dão suporte a uma propriedade de **progresso** padrão que varia de 0 a 1,0, indicando qual porcentagem da transição é refletida na saída. Em **andamento** = 0,0, a transição está no início de sua sequência (totalmente a primeira imagem de vídeo). Em **andamento** = 0,5, a transição é a metade concluída. (Por exemplo, em um apagamento, em **andamento** = 0,5, o limite de transição está no centro da imagem) Em **andamento** = 1,0, a transição é concluída (totalmente a segunda imagem). Por padrão, as transições vão de **Progress** = 0,0 no início da transição para **Progress** = 1,0 no final.

Outras propriedades geralmente são específicas para uma transição ou efeito específico. Por exemplo, a transição de apagamento dá suporte a uma propriedade **GradientSize** que controla a largura da área de transição.

Para executar uma transição para trás, defina a propriedade **Progress** como 1,0 no início da transição e use o elemento **linear** para alterar o valor para 0,0, conforme mostrado no exemplo a seguir:


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

 

 



