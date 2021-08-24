---
title: Atributo StartArrowWidth de VML
description: Atributo StartArrowWidth de VML
ms.assetid: 47b55330-7165-4368-ad01-5b7b38a6e5b2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d427db8e504fca57fc77b24b7b5fa1360ed7716276cd67b43c55ee8d0552d8f5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513236"
---
# <a name="vml-startarrowwidth-attribute"></a>Atributo StartArrowWidth de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define a largura da ponta de seta para o início de uma linha. Leitura/gravação. **VgArrowheadWidth**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* startarrowwidth = " *expressão* " >

**Sintaxe do script**

*Element* . startarrowwidth = "*expressão*"

*expressão* = de *elemento*. startarrowwidth

**Comentários**

Os valores são:

-   Encontrar
-   Médio (padrão)
-   Ampla

Atributo padrão da VML

**Exemplo**

Uma linha é desenhada com uma ponta de seta clássica no início do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke startarrow="classic" startarrowwidth="wide"/>
   </v:line>
```



 

 