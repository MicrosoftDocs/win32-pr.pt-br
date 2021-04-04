---
title: Atributo de pontos de VML
description: Atributo de pontos de VML
ms.assetid: 343d843e-9a09-4c89-af54-fb079129429b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98a0ea1136a040218a482b49323dc3784908899
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007643"
---
# <a name="vml-points-attribute"></a>Atributo de pontos de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um conjunto de pontos que compõem uma polilinha. Leitura/gravação. [IVgPoints](msdn-online-vml-ivgpoints-data-type.md) .

**Aplica-se a**

[Múltipla](msdn-online-vml-polyline-element.md)

**Sintaxe de marca**

<v: *Element* Points = " *expression* " >

**Sintaxe do script**

*Element* . Points = "*Expression * * *"**

*expressão* = de *elemento*. Points

**Comentários**

Define um conjunto de segmentos de linha reta que são compostos por uma série de pontos. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado). O valor padrão é "0, 0 10, 10". Observe que as vírgulas não são necessárias, mas elas tornam a legibilidade mais fácil.

*Atributo padrão da VML*

**Exemplo**

A polilinha começa no ponto 10, 10 e termina em 100.100, com os valores de pontos.


```HTML
   <v:polyline id="mypolyline"
   points="10pt,10pt 100pt,100pt">
   </v:polyline>
```



 

 