---
title: Atributo JoinStyle do VML
description: Atributo JoinStyle do VML
ms.assetid: d947d115-2064-446a-8c12-e8063fe10953
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1cbad649d2a8889846d1d0c1e1df3d62e94cb8e8ff03f0dfa5c47f7bd414dcdc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599360"
---
# <a name="vml-joinstyle-attribute"></a>Atributo JoinStyle do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o estilo de junção de uma polilinha. Leitura/gravação. Cadeia de caracteres.

**Aplica-se a**

[Curso](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *element* joinstyle=" *expressão* ">

**Sintaxe do script**

*expressão element* .joinstyle=""

*expressão* = *elemento*.joinstyle

**Comentários**

Os valores são:

-   round (padrão)
-   Bisel
-   Esquadria

*Atributo padrão VML*

**Exemplo**

As junções na polilinha são envelhadas.


```HTML
   <v:polyline
   strokecolor="red" strokeweight="2pt"
   points="18pt,54pt,90pt,-9pt,180pt,63pt,261pt,27pt">
   <v:stroke joinstyle="bevel"/>
   </v:polyline>
```



 

 