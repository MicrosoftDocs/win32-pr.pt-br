---
title: Atributo CropBottom do VML
description: Atributo CropBottom do VML
ms.assetid: 9548d0fa-1708-4206-90d8-1d90cb42de87
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 667e5501f43d55dcc6a489406e4b10397c1a39773fad2fce7dc6f8601bf45024
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601949"
---
# <a name="vml-cropbottom-attribute"></a>Atributo CropBottom do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o percentual de remoção de imagem do lado inferior. Leitura/gravação. **VgNumber.**

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *elemento* cropbottom=" *expressão* ">

**Sintaxe do script**

*expressão* element .cropbottom=""

*expressão* = *elemento*.cropbottom

**Comentários**

A quantidade de corte pode variar de -1,0 a 1,0. O valor padrão é 0. Observe que um valor de 1 não exibirá nenhuma imagem. Valores negativos resultarão na imagem sendo pressionada para dentro da borda sendo cortada (o espaço vazio entre a imagem e a borda cortada será preenchido pela cor de preenchimento da forma). Valores positivos menores que 1 resultarão no alongamento da imagem restante para se ajustar à forma.

Atributo padrão VML

**Exemplo**

Nenhuma imagem será exibida porque a imagem está 100% cortada na parte inferior.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropbottom="1" src="kids.jpg"/>
   </v:shape>
```



 

 