---
title: Atributo de Font-Family VML
description: Atributo de Font-Family VML
ms.assetid: 10586ae0-1480-4ffe-a690-ce8464e9bf41
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1254be6f7264e0d8f77d5881a11b9c2ec5085a931a0cad713813c059c60e5e62
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754728"
---
# <a name="vml-font-family-attribute"></a>Atributo de Font-Family VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a família da fonte textpath. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Textpath](msdn-online-vml-textpath-element.md)

**Sintaxe de marca**

<v: *element* style="font-family: *expression* ">

**Sintaxe do script**

*elemento* .style.fontfamily="*expression*"

*expressão* = *elemento*.style.fontfamily

**Comentários**

Define o nome da fonte. Nomes específicos, como Arial, podem ser usados ou tipos genéricos, como serif, sans-serif, cursive, ou monospace. Os valores são os mesmos que os atributos de estilo HTML padrão.

*Atributo padrão VML*

**Exemplo**

A família de fontes do texto é Arial.


```HTML
   <v:line from="50 100" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



 

 