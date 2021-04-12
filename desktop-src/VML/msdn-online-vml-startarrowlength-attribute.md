---
title: Atributo StartArrowLength de VML
description: Atributo StartArrowLength de VML
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 90a57e10c9cf7b9a8683f4b1856355232afc16be
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366283"
---
# <a name="vml-startarrowlength-attribute"></a>Atributo StartArrowLength de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o comprimento da ponta de seta para o início de uma linha. Leitura/gravação. **VgArrowheadLength**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* startarrowlength = " *expressão* " >

**Sintaxe do script**

*Element* . startarrowlength = "*expressão*"

*expressão* = de *elemento*. startarrowlength

**Comentários**

Os valores são:

-   Short
-   Médio (padrão)
-   long

Atributo padrão da VML

**Exemplo**

Uma linha é desenhada com uma pequena ponta de seta clássica no início do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowlength="short"/>
   </v:line>
```



 

 