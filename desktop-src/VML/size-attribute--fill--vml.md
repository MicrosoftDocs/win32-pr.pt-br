---
title: Atributo Size (Preenchimento)(VML)
description: Atributo Size (Preenchimento)(VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b26568151961fb2186f8cf49ae25d9f2835665b8fd52a96a4d3a79e954c50ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754141"
---
# <a name="size-attribute-fillvml"></a>Atributo Size (Preenchimento)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define o tamanho da imagem para o preenchimento. Leitura/gravação. [VgVector2D.](msdn-online-vml-ivgvector2d-data-type.md)

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *element* size=" *expressão* ">

**Sintaxe do script**

*elemento* .size="*expression***"**

*expressão* = *elemento*.size

**Comentários**

O padrão é o tamanho da imagem original. Tamanhos maiores do que a forma exibirão uma versão ampliada, mas recortada da imagem.

*Atributo padrão VML*

**Exemplo**

Embora o tamanho original da imagem seja de 50 por 50 pontos, a imagem será exibida como uma imagem de 10 por 10 no centro do preenchimento.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 