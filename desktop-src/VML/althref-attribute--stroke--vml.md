---
title: Atributo AltHRef (traço)(VML)
description: Atributo AltHRef (traço)(VML)
ms.assetid: ee7c1710-1f8e-42c4-895f-d0f3d15ca6db
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0cbdbe82330d154675b135f7e9f35869c8f47e25715680d97df05e5511a01e9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867436"
---
# <a name="althref-attribute-strokevml"></a>Atributo AltHRef (traço)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica uma referência alternativa para uma imagem. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Curso](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *elemento* o:althref=" *expressão* ">

**Sintaxe do script**

*elemento* .althref="*expression*"

*expressão* = *elemento*.althref

**Comentários**

Dá suporte à preservação de dados DE PICT por meio de arredondamento HTML. Na gravação HTML, a representação alternativa (ou seja, os dados ORIGINAL DO PICT se o arquivo originado do Macintosh) for salvo. Na leitura html, **AltHRef** é favorecido em relação **ao Src**.

*Microsoft Office Atributo Extensions*

**Exemplo**

O traço da forma tem uma **AltHRef** que aponta para um arquivo chamado myimage.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200,200, 200, 200,1 x e">
   <v:stroke o:althref="myimage.gif"/>
   </v:shape>
```



 

 