---
title: Atributo ImageAlignShape do VML
description: Atributo ImageAlignShape do VML
ms.assetid: 45d72560-ab64-4e85-b495-88f1557a62f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86090936556ba8a4f022024f292293b396d953d46962423a222b172adc2a15f6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600464"
---
# <a name="vml-imagealignshape-attribute"></a>Atributo ImageAlignShape do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina o alinhamento da imagem de traço. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Curso](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v:

elemento *imagealignshape="* expressão *">*

**Sintaxe do script**

element *.imagealignshape="* expression *"*

elemento *=* expression *.imagealignshape*

**Comentários**

Se **True**, alinhe a imagem com a forma; caso disso, alinhe a imagem com a janela. O padrão é **True**.

*Atributo padrão VML*

**Exemplo**

A imagem está alinhada com a janela.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red" strokeweight="20pt"
   style="top:20;left:20;width:300;height:300"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke imagealignshape="false" width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 