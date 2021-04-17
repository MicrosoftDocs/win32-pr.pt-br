---
title: Atributo EndArrowLength de VML
description: Atributo EndArrowLength de VML
ms.assetid: aab898b6-4c59-4471-81fd-621f79610d63
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 43d9d8bfbd24a6a1b79208d50d4d2aef956a5bc5
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105770566"
---
# <a name="vml-endarrowlength-attribute"></a>Atributo EndArrowLength de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um comprimento de ponta de seta para o fim de uma linha. Leitura/gravação. **VgArrowheadLength**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* endarrowlength = " *expressão* " >

**Sintaxe do script**

*Element* . endarrowlength = "*expressão*"

*expressão* = de *elemento*. endarrowlength

**Comentários**

Os valores são:

-   Short
-   Médio (padrão)
-   long

*Atributo padrão da VML*

**Exemplo**

Uma linha é desenhada com uma seta clássica curta no final do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowlength="short"/>
   </v:line>
```



 

 