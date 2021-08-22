---
title: Atributo Src (traço)(VML)
description: Atributo Src (traço)(VML)
ms.assetid: dac6b5b7-2038-4534-97e9-a1340102777e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 57bc71d7a36ee944a2352cde6bfa1ef33f0b5c480d78c7aada751ea67db9ca7f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596622"
---
# <a name="src-attribute-strokevml"></a>Atributo Src (traço)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define a imagem de origem a ser carregada para um preenchimento de traço. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Curso](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *elemento* src=" *expressão* ">

**Sintaxe do script**

*expressão* element .src=""

*expressão* = *elemento*.src

**Comentários**

URL para uma imagem a ser carregada para preenchimentos de imagem e padrão. Esse atributo deve estar sempre presente e apontar para dados de imagem válidos para que uma imagem apareça. Se esse atributo aparecer sozinho, ou seja, sem **HRef** ou **Title**, a imagem será vinculada.

*Atributo padrão VML*

**Exemplo**

O traço é criado com a imagem especificada pelo arquivo cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke src="cylinder.gif" filltype="tile" width="10pt"/>
   </v:shape>
```





 

 