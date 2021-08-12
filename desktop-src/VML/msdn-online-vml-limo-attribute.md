---
title: Atributo de atributo Demá. VML
description: Atributo de atributo Demá. VML
ms.assetid: 61919d48-0cc8-4693-a8bb-a8a4498ef840
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa99325f396a3e4709fcd7ca1ee6ee82df1b653dff50df56df2df06ef2d513ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118598306"
---
# <a name="vml-limo-attribute"></a>Atributo de atributo Demá. VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define um ponto de alongamento no caminho. Leitura/gravação. **Vector2D**.

**Aplica-se a**

[Caminho](msdn-online-vml-path-element.md)

**Sintaxe de marca**

<v: *element* av=" *expressão* ">

**Sintaxe do script**

*expressão* element .mus=""

*expressão* = *elemento*.limo

**Comentários**

O valor padrão é "0 0". Alongamentos de shape são pontos na borda de uma forma que definem onde e como uma forma pode ser alongada por um usuário em um editor gráfico.

*Atributo padrão VML*

**Exemplo**

Um ponto de alongamento de barras é definido na metade da linha horizontal.


```HTML
   <v:line strokecolor="red"
   strokeweight="2pt" from="20pt,20pt" to="100pt,20pt">
   <v:path limo="60pt,20pt"/>
   </v:line>
```



 

 