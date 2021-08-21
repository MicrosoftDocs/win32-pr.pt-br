---
title: Atributo VML V-Rotate-Letters
description: Atributo VML V-Rotate-Letters
ms.assetid: f9bd5c04-7479-4dc0-83d7-4a0bd5e2d41d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 779f7878b01765416560dacaed5e3b81a1e00a25d4bf7c53e0071c8bb487d16a
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118123776"
---
# <a name="vml-v-rotate-letters-attribute"></a>Atributo VML V-Rotate-Letters

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina se as letras do texto são giradas. Leitura/gravação. **VgTriState.**

**Aplica-se a**

[Textpath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *element* style="v-rotate-letters: *expression* ">

**Sintaxe do script**

*expressão* element .style.v-rotate-letters=""

*expressão* = *elemento*.style.v-rotate-letters

**Comentários**

Se **True**, as letras do texto serão giradas em 90 graus. O valor padrão é **Falso**.

*Atributo padrão VML*

**Exemplo**

As letras são giradas em 90 graus.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="v-rotate-letters:True;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 