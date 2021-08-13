---
title: Atributo EndArrowLength do VML
description: Atributo EndArrowLength do VML
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3fb11c07300127acd2446c7c2c643e0a891957d63f7650044514427f3e8535d0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601346"
---
# <a name="vml-endarrowlength-attribute"></a>Atributo EndArrowLength do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define um comprimento de seta para o final de uma linha. Leitura/gravação. **VgArrowheadLength.**

**Aplica-se a**

[Curso](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *elemento* endarrowlength=" *expressão* ">

**Sintaxe do script**

*element* .endarrowlength="*expression*"

*expressão* = *elemento*.endarrowlength

**Comentários**

Os valores são:

-   Short
-   Médio (padrão)
-   long

*Atributo padrão VML*

**Exemplo**

Uma linha é desenhada com uma seta clássica curta no final do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 