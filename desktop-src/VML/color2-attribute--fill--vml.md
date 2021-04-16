---
title: Atributo Color2 (Fill) (VML)
description: Atributo Color2 (Fill) (VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5689bba52277b4056f57a171f3ffc1e197aa4c8b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105782289"
---
# <a name="color2-attribute-fillvml"></a>Atributo Color2 (Fill) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma segunda cor para preenchimentos. Leitura/gravação. [VgColor](msdn-online-vml-ivgcolor.md) .

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* color2 = " *expressão* " >

**Sintaxe do script**

*Element* . color2 = "*expressão*"

*expressão* = de *elemento*. color2

**Comentários**

Uma segunda cor é usada quando um tipo de preenchimento é um padrão ou um gradiente. O valor padrão é **branco**.

*Atributo padrão da VML*

**Exemplo**

O tipo de preenchimento da forma é um padrão em que o preenchimento em primeiro plano é definido pela imagem de origem, mas o plano de fundo transparente é definido pela segunda cor.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 