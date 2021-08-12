---
title: Atributo CoordOrigin do VML
description: Atributo CoordOrigin do VML
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf568f2c305108a651d56a891a96890154f9493cbadd80a9c5610414c88f4f03
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601936"
---
# <a name="vml-coordorigin-attribute"></a>Atributo CoordOrigin do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica a origem da unidade de coordenadas do retângulo que delimita uma forma. Leitura/gravação. [IVgVector2D.](msdn-online-vml-ivgvector2d-data-type.md)

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *elemento* coordorigin=" *expressão* ">

**Sintaxe do script**

*element* .coordorigin="*expression*"

*expressão* = *elemento*.coordorigin

**Comentários**

Se não for especificado, as coordenadas de origem serão (0,0) no canto superior esquerdo da caixa delimitada por forma.

O valor x de **CoordSize** é adicionado ao valor x de **CoordOrigin** para determinar o intervalo dos valores horizontais. Por exemplo, se o valor x de **CoordOrigin** for -100 e o valor x de **CoordSize** for 200, as unidades horizontais variarão de -100 a +100. Se o valor x de **CoordOrigin** for 100 e o valor x de **CoordSize** for 200, as unidades horizontais variarão de 100 a 300, tudo dentro da caixa delimitada. O mesmo é verdadeiro para os valores y.

Observe que esse atributo é um vetor e que as unidades são do mesmo tipo de unidade que [CoordSize](msdn-online-vml-coordsize-attribute.md) .

No script, como esse é um vetor 2D, você pode acessar os valores x e y separadamente e também pode determinar o tipo de unidades esperado.

*Atributo padrão VML*

**Exemplo**

O centro da caixa delimitador será a origem (0,0) do caminho para a forma. Como **CoordOrigin** é "-500 -500" e **CoordSize** é "1000 1000", as unidades horizontais e verticais variam de -500 a +500. O canto superior e esquerdo do caminho estará no centro da caixa delimitador definida pelos pontos esquerdo e superior, conforme definido por **Style**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo de atributo CoordOrigin](/previous-versions/bb229664(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 