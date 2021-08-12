---
title: Atributo AltHRef (Preenchimento)(VML)
description: Atributo AltHRef (Preenchimento)(VML)
ms.assetid: 3f6376e3-24db-412c-b265-5916950c3824
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 181f98ace80403668f8f67c6f8412091271fdfcf2abcb5a1320d0685853d92bd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118602999"
---
# <a name="althref-attribute-fillvml"></a>Atributo AltHRef (Preenchimento)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma referência alternativa para uma imagem. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *elemento* o:althref=" *expressão* ">

**Sintaxe do script**

*elemento* .althref="*expression*"

*expressão* = *elemento*.althref

**Comentários**

Dá suporte à preservação de dados DE PICT por meio de arredondamento HTML. Na gravação HTML, a representação alternativa (os dados ORIGINAL DO PICT se o arquivo tiver sido originado do Apple Macintosh) será salva. Na leitura html, **AltHRef** é favorecido em relação **ao Src**.

*Microsoft Office Atributo Extensions*

**Exemplo**

O preenchimento da forma tem uma **AltHRef** que aponta para um arquivo chamado myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill o:althref="myimage.gif"/>
   </v:shape>
```



 

 