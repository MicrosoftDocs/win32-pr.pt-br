---
title: Atributo CoordOrigin de VML
description: Atributo CoordOrigin de VML
ms.assetid: 0630e670-6ebe-424e-a5e0-545597454283
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fb08d35aac7e26cc15aa7699439ea9f7ab4dba94
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823793"
---
# <a name="vml-coordorigin-attribute"></a>Atributo CoordOrigin de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica a origem da unidade de coordenadas do retângulo que vincula uma forma. Leitura/gravação. [IVgVector2D](msdn-online-vml-ivgvector2d-data-type.md).

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* coordorigin = " *expressão* " >

**Sintaxe do script**

*Element* . coordorigin = "*expressão*"

*expressão* = de *elemento*. coordorigin

**Comentários**

Se não for especificado, as coordenadas de origem serão (0, 0) no canto superior esquerdo da caixa delimitadora de forma.

O valor x de **CoordSize** é adicionado ao valor x de **CoordOrigin** para determinar o intervalo dos valores horizontais. Por exemplo, se o valor x de **CoordOrigin** for-100 e o valor x de **CoordSize** for 200, as unidades horizontais irão variar de-100 a + 100. Se o valor x de **CoordOrigin** for 100 e o valor x de **CoordSize** for 200, as unidades horizontais irão variar de 100 a 300, tudo dentro da caixa delimitadora. O mesmo é verdadeiro para os valores y.

Observe que esse atributo é um vetor e que as unidades são do mesmo tipo de unidade que [CoordSize](msdn-online-vml-coordsize-attribute.md) .

No script, como esse é um vetor 2D, você pode acessar os valores x e y separadamente e também pode determinar o tipo de unidades esperado.

*Atributo padrão da VML*

**Exemplo**

O centro da caixa delimitadora será a origem (0, 0) do caminho para a forma. Como **CoordOrigin** é "-500-500" e **CoordSize** é "1000 1000", as unidades horizontais e verticais vão variar de-500 a + 500. O canto esquerdo e superior do caminho estará no centro da caixa delimitadora definida pelos pontos esquerdo e superior, conforme definido pelo **estilo**.


```HTML
   <v:shape id="rect01"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   </v:shape>
```



[Exemplo do atributo CoordOrigin](/previous-versions/bb229664(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 