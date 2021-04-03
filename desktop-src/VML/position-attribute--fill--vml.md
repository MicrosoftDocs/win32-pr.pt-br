---
title: Atributo de posição (Fill) (VML)
description: Atributo de posição (Fill) (VML)
ms.assetid: 0d532d4c-0c96-4f41-b54f-55b6aade0c03
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01fff487f134d50b5a72623abf21c0b5710f9bc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084858"
---
# <a name="position-attribute-fillvml"></a>Atributo de posição (Fill) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a posição da imagem de preenchimento. Leitura/gravação. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *elemento* position = " *expressão* " >

**Sintaxe do script**

*elemento* . Position = "*expressão*"

*expressão* = de *elemento*. Position

**Comentários**

Especifica um ponto na forma para posicionar a origem da imagem. O padrão é o centro do retângulo do contêiner. O vetor é uma fração da largura e da altura da imagem.

*Atributo padrão da VML*

**Exemplo**

A imagem do preenchimento é deslocada para a direita para um ponto de 50% da largura da forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" position="0.5,0" src="myimage.gif"/>
   </v:shape>
```



 

 