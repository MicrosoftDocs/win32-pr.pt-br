---
title: Atributo EndArrowWidth de VML
description: Atributo EndArrowWidth de VML
ms.assetid: a68854d2-33f8-44fb-a0be-830d2be3040f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108d65fc1a06ace3d318d54a6416e0d98c0a4652
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641813"
---
# <a name="vml-endarrowwidth-attribute"></a>Atributo EndArrowWidth de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma largura de seta para o fim de uma linha. Leitura/gravação. **VgArrowheadWidth**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* endarrowwidth = " *expressão* " >

**Sintaxe do script**

*Element* . endarrowwidth = "*expressão*"

*expressão* = de *elemento*. endarrowwidth

**Comentários**

Os valores são:

-   Encontrar
-   Médio (padrão)
-   Ampla

*Atributo padrão da VML*

**Exemplo**

Uma linha é desenhada com uma ponta de seta clássica no final do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic" endarrowwidth="wide"/>
   </v:line>
```



 

 