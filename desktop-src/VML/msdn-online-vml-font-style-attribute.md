---
title: Atributo Font-Style de VML
description: Atributo Font-Style de VML
ms.assetid: 3dfea8d0-d03b-46c0-b972-a529bc12b62c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4571f9805b3a12f1c3c7b340780d0f3d9f6ce8644c2ec501e8c93aa58d378de6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119057854"
---
# <a name="vml-font-style-attribute"></a>Atributo Font-Style de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define a quantidade de inclinação de uma fonte. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextPath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *elemento* Style = "fonte-estilo: *expressão* " >

**Sintaxe do script**

*elemento* . Style. FontStyle = "*expressão*"

*expressão* = de *elemento*. Style. FontStyle

**Comentários**

Os valores são:

-   normal (padrão)
-   oblíquo
-   itálico

A maioria dos navegadores renderiza Oblique como itálico. Os valores são os mesmos que os atributos de estilo HTML padrão.

*Atributo padrão da VML*

**Exemplo**

A fonte é itálico (inclinada).


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:italic normal normal 36pt Arial"/>
   </v:line>
```



 

 