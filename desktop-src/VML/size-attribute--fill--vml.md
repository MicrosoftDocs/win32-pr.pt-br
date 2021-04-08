---
title: Atributo de tamanho (Fill) (VML)
description: Atributo de tamanho (Fill) (VML)
ms.assetid: a84d2d81-0f6f-4011-867d-516225a314aa
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1eea5638d619853857499cc317517dfc5ffc762
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917367"
---
# <a name="size-attribute-fillvml"></a>Atributo de tamanho (Fill) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o tamanho da imagem para o preenchimento. Leitura/gravação. [VgVector2D](msdn-online-vml-ivgvector2d-data-type.md) .

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: *Element* tamanho = " *expression* " >

**Sintaxe do script**

*elemento* . Size = "*expressão * * *"**

*expressão* = de *elemento*. Size

**Comentários**

O padrão é o tamanho da imagem original. Os tamanhos maiores que o shapewill exibem uma versão ampliada, mas recortada da imagem.

*Atributo padrão da VML*

**Exemplo**

Embora o tamanho original da imagem seja de 50 a 50 pontos, a imagem será exibida como uma imagem de 10 por 10 no centro do preenchimento.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill src="myimage.gif" type="frame" size="10pt,10pt"/>
   </v:shape>
```



 

 