---
title: Atributo Src (ImageData)(VML)
description: Atributo Src (ImageData)(VML)
ms.assetid: ef6b57d9-dca7-4f6e-8fd1-e846e4d09fb7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 688bc1e82afbaf0747a03465c93feb1d760cc60eb441792654ef11ec59cee749
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596678"
---
# <a name="src-attribute-imagedatavml"></a>Atributo Src (ImageData)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma origem para a imagem. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *elemento* src=" *expressão* ">

**Sintaxe do script**

*expressão* element .src=""

*expressão* = *elemento*.src

**Comentários**

Esse atributo sempre deve ser usado com o [elemento ImageData](msdn-online-vml-imagedata-element.md) e apontar para dados de imagem válidos para que uma imagem seja exibida. Se esse atributo aparecer sem [HRef](https://www.bing.com/search?q=HRef) ou [Title](title-attribute--imagedata--vml.md), a imagem será vinculada.

*Atributo padrão VML*

**Exemplo**

A origem da imagem é um arquivo chamado "kids.jpg".


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata src="kids.jpg"/>
   </v:shape>
```



 

 