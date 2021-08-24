---
title: Atributo de Text-Decoration VML
description: Atributo de Text-Decoration VML
ms.assetid: a64985bd-d025-4e9c-bb4b-bf0450d5143a
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 474d76b9e37cb363a8b2a28b84c30be77f857159767cc4db221fd7a684b4951e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119796026"
---
# <a name="vml-text-decoration-attribute"></a>Atributo de Text-Decoration VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o estilo da decoração de texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Textpath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *element* style="text-decoration: *expression* ">

**Sintaxe do script**

*elemento* .style.textdecoration="*expression*"

*expressão* = *elemento*.style.textdecoration

**Comentários**

Os valores são:

-   none (padrão)
-   underline
-   sobreposta
-   passagem de linha
-   blink

*Atributo padrão VML*

**Exemplo**

O texto será sublinhado.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="text-decoration:underline;font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 