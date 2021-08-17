---
title: Atributo CropLeft do VML
description: Atributo CropLeft do VML
ms.assetid: 923482f2-e3eb-4508-81d4-f19db8fcf4eb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26112aa969e95c6bfb1ec715024aca9eb17b2dbfc2d7d214fb3679cf7ab77447
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754846"
---
# <a name="vml-cropleft-attribute"></a>Atributo CropLeft do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o percentual de remoção de imagem do lado esquerdo. Leitura/gravação. **VgNumber.**

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *elemento* cropleft=" *expressão* ">

**Sintaxe do script**

*expressão* element .cropleft=""

*expressão* = *elemento*.cropleft

**Comentários**

A quantidade de corte pode variar de -1,0 a 1,0. O valor padrão é 0. Observe que um valor de 1 não exibirá nenhuma imagem. Valores negativos resultarão na imagem sendo pressionada para dentro da borda sendo cortada (o espaço vazio entre a imagem e a borda cortada será preenchido pela cor de preenchimento da forma). Valores positivos menores que 1 resultarão no alongamento da imagem restante para se ajustar à forma.

*Atributo padrão VML*

**Exemplo**

20% da imagem será removida no lado esquerdo e a imagem restante será alongada para se ajustar à forma.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata cropleft=".2" src="kids.jpg"/>
   </v:shape>
```



 

 