---
title: Atributo StartArrow de VML
description: Atributo StartArrow de VML
ms.assetid: 484dfcdb-f68d-40f9-9a83-18abb054d1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca2c17569750c1e655a5538ca5bf233e49f827e4
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917481"
---
# <a name="vml-startarrow-attribute"></a>Atributo StartArrow de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define a ponta de seta para o início de uma linha. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* startarrow = " *expressão* " >

**Sintaxe do script**

*Element* . startarrow = "*expressão*"

*expressão* = de *elemento*. startarrow

**Comentários**

Os valores são:

-   Nenhum (padrão)
-   Bloquear
-   Clássico
-   Diamond
-   Oval
-   Aberto

Atributo padrão da VML

**Exemplo**

Uma linha é desenhada com uma ponta de seta clássica no início do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke StartArrow="classic"/>
   </v:line>
```



 

 