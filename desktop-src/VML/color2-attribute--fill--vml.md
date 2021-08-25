---
title: Atributo Color2 (Preenchimento)(VML)
description: Atributo Color2 (Preenchimento)(VML)
ms.assetid: 971c8783-8c7b-43c7-8b94-01159336eef6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8e651245ddf9fb2a3669c3529038b5d0d8cbb3922b8a112c201858d2efd786a9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007886"
---
# <a name="color2-attribute-fillvml"></a>Atributo Color2 (Preenchimento)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma segunda cor para preenchimentos. Leitura/gravação. [VgColor](msdn-online-vml-ivgcolor.md) .

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *elemento* color2=" *expressão* ">

**Sintaxe do script**

*elemento* .color2="*expression*"

*expressão* = *elemento*.color2

**Comentários**

Uma segunda cor é usada quando um tipo de preenchimento é um padrão ou um gradiente. O valor padrão é **Branco.**

*Atributo padrão VML*

**Exemplo**

O tipo de preenchimento da forma é um padrão em que o preenchimento de primeiro plano é definido pela imagem de origem, mas a tela de fundo transparente é definida pela segunda cor.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type="pattern" color2="green" src="myimage.gif"/>
   </v:shape>
```



 

 