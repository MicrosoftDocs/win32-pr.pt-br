---
title: Atributo StartArrowLength de VML
description: Atributo StartArrowLength de VML
ms.assetid: 7c108132-4f74-41cc-bfac-123f0259e6cb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25446737118c546727d769d54d98e4503faaadd063102fa98a417ebea13c976d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395826"
---
# <a name="vml-startarrowlength-attribute"></a>Atributo StartArrowLength de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

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



 

 