---
title: Atributo Color (Shadow) (VML)
description: Atributo Color (Shadow) (VML)
ms.assetid: 677615b7-b4a4-411f-b04e-3ed0399f4c05
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73df77e65a3ae0f74c6e79b9c179c31da27698f9
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105764016"
---
# <a name="color-attribute-shadowvml"></a>Atributo Color (Shadow) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a cor da sombra. Leitura/gravação. **VgColor**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *Element* Color = " *expressão* " >

**Sintaxe do script**

*Element* . Color = "*expressão*"

*expressão* = de *elemento*. Color

**Comentários**

Use o atributo Color para definir ou obter a cor de uma sombra.

*Atributo padrão da VML*

**Exemplo**

A sombra está verde.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" color="green"/>
   </v:shape>
```



 

 