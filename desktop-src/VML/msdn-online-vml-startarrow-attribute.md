---
title: Atributo StartArrow do VML
description: Atributo StartArrow do VML
ms.assetid: 484dfcdb-f68d-40f9-9a83-18abb054d1c8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 97b0d1ce8d352ef119e2745d0f7768332ad074d134877b03433aa788f1bb2e49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754478"
---
# <a name="vml-startarrow-attribute"></a>Atributo StartArrow do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a seta para o início de uma linha. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Curso](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *elemento* startarrow=" *expressão* ">

**Sintaxe do script**

*expressão element* .startarrow=""

*expressão* = *elemento*.startarrow

**Comentários**

Os valores são:

-   Nenhum (padrão)
-   Bloquear
-   Clássico
-   Diamond
-   Oval
-   Aberto

Atributo padrão VML

**Exemplo**

Uma linha é desenhada com uma seta clássica no início do traço.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" to="100pt,20pt" from="20pt,20pt">
   <v:stroke StartArrow="classic"/>
   </v:line>
```



 

 