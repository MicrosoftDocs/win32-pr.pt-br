---
title: Atributo AlignShape de VML
description: Atributo AlignShape de VML
ms.assetid: 427e5969-4545-47b2-80f8-0e8783c52d65
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c32a4baba060dff4a7a45ccf5a374acf33620a4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104294448"
---
# <a name="vml-alignshape-attribute"></a>Atributo AlignShape de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se uma imagem será alinhada com uma forma. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* alignshape = " *expressão* " >

**Sintaxe do script**

*Element* . alignshape = "*expressão*"

*expressão* = de *elemento*. alignshape

**Comentários**

Se **for true**, a imagem usada para criar o preenchimento será alinhada com a forma. Se **for false**, a imagem usada para criar o preenchimento será alinhada com a janela. O padrão é **True**.

*Atributo padrão da VML*

**Exemplo**

A imagem de preenchimento à direita criada a partir de myimage.gif é alinhada com a janela, não a forma; Embora a forma seja girada, a imagem não é.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50;rotation:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill alignshape="False" type="tile" src="myimage.gif"/>
   </v:shape>
```



 

 