---
title: Atributo from (line) (VML)
description: Atributo from (line) (VML)
ms.assetid: 37cc9b2e-c18d-48ea-bac5-a2d2ea10d3d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 950b3cae8e3b73efdc3a92bdc49a0b9e4366e224
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641776"
---
# <a name="from-attribute-linevml"></a>Atributo from (line) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o ponto de partida de uma linha. Leitura/gravação. **VgVector2D**.

**Aplica-se a**

[Linha](msdn-online-vml-line-element.md)

**Sintaxe de marca**

<v: *Element* de = " *expression* " >

**Sintaxe do script**

*elemento* . from = "*expressão*"

*expressão* = de *elemento*. from

**Comentários**

Define o ponto inicial da linha no espaço de coordenadas do elemento pai. Se o pai não for um elemento VML, a [unidade](msdn-online-vml-units.md) padrão será um pixel (mas no, cm, mm, pt, o PC também poderá ser especificado). O padrão é 0, 0.

*Atributo padrão da VML*

**Exemplo**

A linha começa em um local 10 aponta para baixo e 10 pontos à direita do canto superior esquerdo do espaço pai.


```HTML
   <v:line id="myline"
   from="10pt,10pt" to="100pt,100pt">
   </v:line>
```



 

 