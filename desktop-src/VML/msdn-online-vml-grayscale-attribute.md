---
title: Atributo de escala de cinza da VML
description: Atributo de escala de cinza da VML
ms.assetid: 0715b78c-f529-422e-9064-7b99324e60de
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c1c4b5da616ec5f96eeb226ecb2ba18202874f67
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366226"
---
# <a name="vml-grayscale-attribute"></a>Atributo de escala de cinza da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina se uma imagem será exibida no modo de escala de cinza. Leitura/gravação. **VgTriState**.

**Aplica-se a**

[ImageData](msdn-online-vml-imagedata-element.md)

**Sintaxe de marca**

<v: *Element* tons de cinza = " *expressão* " >

**Sintaxe do script**

*elemento* . escala de cinza = "*expressão*"

*expressão* = de *elemento*. escala de cinza

**Comentários**

Se **for true**, a imagem será exibida em escala de cinza em vez de cor. O padrão é **False**.

O valor é baseado de acordo com a recomendação de CCIR 709, que favorece mais o peso verde e produz resultados mais agradáveis para a cor natural.

*Atributo padrão da VML*

**Exemplo**

A imagem será exibida em escala de cinza em vez de cor.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:300;height:200"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:imagedata grayscale="True" src="kids.jpg"/>
   </v:shape>
```



 

 