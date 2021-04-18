---
title: Atributo de fim da seta de VML
description: Atributo de fim da seta de VML
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 542d6dbb3b30467c4bcad909f2b49d617f8bd886
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105770125"
---
# <a name="vml-endarrow-attribute"></a>Atributo de fim da seta de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma ponta de seta para o final de uma linha. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *elemento* endarrow = " *expressão* " >

**Sintaxe do script**

*elemento* . endarrow = "*expressão*"

*expressão* = de *elemento*. endarrow

**Comentários**

Os valores são:

-   Nenhum (padrão)
-   Bloquear
-   Clássico
-   Diamond
-   Oval
-   Aberto

*Atributo padrão da VML*

**Exemplo**

Uma linha é desenhada com uma ponta de seta clássica no final do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 