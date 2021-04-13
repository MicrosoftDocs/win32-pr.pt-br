---
title: Atributo de origem (preenchimento) (VML)
description: Atributo de origem (preenchimento) (VML)
ms.assetid: 7ebb70eb-e8f2-4749-88fd-935562da0b74
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb1d26f5e544ffa19b347ceec1549885c1ff6b90
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366666"
---
# <a name="origin-attribute-fillvml"></a>Atributo de origem (preenchimento) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o centro de uma imagem de preenchimento. Leitura/gravação. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *elemento* Origin = " *expressão* " >

**Sintaxe do script**

*elemento* . Origin = "*expressão*"

*expressão* = de *elemento*. Origin

**Comentários**

Especifica um ponto relativo ao canto superior esquerdo da imagem; esse ponto é tratado como a origem da imagem. O padrão é o centro da imagem. O vetor é uma fração da largura e da altura da imagem.

*Atributo padrão da VML*

**Exemplo**

A imagem do preenchimento é deslocada para a esquerda para um ponto de 50% da largura da forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" origin="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 