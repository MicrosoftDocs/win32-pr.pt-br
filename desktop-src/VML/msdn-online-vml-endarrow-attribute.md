---
title: Atributo EndArrow VML
description: Atributo EndArrow VML
ms.assetid: 056cd011-bb3b-4f9a-83d0-9702e0e82e4d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f289342c8bfb67e9a0c2ccc6e418f42bd954e9826a18f07260a2891bf4b4284
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120007826"
---
# <a name="vml-endarrow-attribute"></a>Atributo EndArrow VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma seta para o final de uma linha. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Curso](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *element* endarrow=" *expressão* ">

**Sintaxe do script**

*expressão* element .endarrow=""

*expressão* = *elemento*.endarrow

**Comentários**

Os valores são:

-   Nenhum (padrão)
-   Bloquear
-   Clássico
-   Diamond
-   Oval
-   Aberto

*Atributo padrão VML*

**Exemplo**

Uma linha é desenhada com uma seta clássica no final do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke endarrow="classic"/>
   </v:line>
```



 

 