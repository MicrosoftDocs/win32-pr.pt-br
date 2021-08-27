---
title: Atributo FitShape de VML
description: Atributo FitShape de VML
ms.assetid: a6e5a198-1478-4256-a4f2-b9ae6db6d7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0adbb6fd92f296156cf2f95cf2b714cfacd2f193f8e1e1b912e6637b9e8d5cd6
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099246"
---
# <a name="vml-fitshape-attribute"></a>Atributo FitShape de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define se o texto se ajusta à caixa delimitadora de uma forma. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *Element* FitShape = " *expressão* " >

**Sintaxe do script**

*Element* . FitShape = "*expressão*"

*expressão* = de *elemento*. FitShape

**Comentários**

Se **for true**, alongará o texto para as bordas da caixa que define a forma inteira. O padrão é **False**.

*Atributo padrão da VML*

**Exemplo**

O texto será alongado para se ajustar à forma.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text" fitshape="True"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 