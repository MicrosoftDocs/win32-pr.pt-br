---
title: Atributo BWNormal de VML
description: Atributo BWNormal de VML
ms.assetid: 4d361fc8-e1a9-4af4-91d1-72cff898650c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2811a9cd734e0f2ca6ca2f707b6313d7434ac756a1f9cd8982d7179c75748bf
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117754951"
---
# <a name="vml-bwnormal-attribute"></a>Atributo BWNormal de VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define o modo preto e branco para dispositivos normais de saída em preto e branco. Leitura/gravação. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:bwnormal = " *expressão* " >

**Comentários**

Quando [BWMode](msdn-online-vml-bwmode-attribute.md) é definido como **auto**, esse atributo é usado para determinar como renderizar a forma em preto e branco normal.

Para obter mais informações sobre os valores desse atributo, consulte o tópico [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . O valor padrão é **auto**.

*Microsoft Office Atributo de extensões*

**Exemplo**

A forma é processada como uma imagem em escala de cinza para saída normal de preto e branco.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwnormal="grayscale" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 