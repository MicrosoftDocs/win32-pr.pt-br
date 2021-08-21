---
title: Atributo AlignShape VML
description: Atributo AlignShape VML
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e00e1fe8d07fb04c198ced2e2eb50d6ef0e6c020984d2d8cf12a3ca37cf09d79
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118125309"
---
# <a name="vml-alignshape-attribute"></a>Atributo AlignShape VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se uma imagem será alinhada com uma forma. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *elemento* alignshape=" *expressão* ">

**Sintaxe do script**

*elemento* .alignshape="*expression*"

*expressão* = *elemento*.alignshape

**Comentários**

Se **True**, a imagem usada para criar o preenchimento será alinhada com a forma. Se **False**, a imagem usada para criar o preenchimento será alinhada com a janela. O padrão é **True**.

*Atributo padrão VML*

**Exemplo**

A imagem de preenchimento lado a lado criada myimage.gif é alinhada com a janela, não com a forma; embora a forma seja girada, a imagem não é.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 