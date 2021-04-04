---
title: Atributo BWPure de VML
description: Atributo BWPure de VML
ms.assetid: a68e8197-bfd6-4b8e-8d4c-598590addff8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83e39c658265a5ab8c617fc8856db362a80d1ea8
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823843"
---
# <a name="vml-bwpure-attribute"></a>Atributo BWPure de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o modo preto e branco para dispositivos de saída puros preto e branco. Leitura/gravação. [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md).

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:bwpure = " *expressão* " >

**Comentários**

Quando [BWMode](msdn-online-vml-bwmode-attribute.md) é definido como **auto**, esse atributo é usado para determinar como renderizar a forma em preto e branco puro.

Para obter mais informações sobre os valores desse atributo, consulte o tópico [VgBlackWhiteMode](msdn-online-vml-vgblackwhitemode.md) . O padrão é **auto**.

*Atributo de extensões de Microsoft Office*

**Exemplo**

A forma é processada como uma imagem de alto contraste para saída puro de preto e branco.


```HTML
   <v:rect id=myrect fillcolor="red" o:bwpure="highcontrast" o:bwmode="auto"
   style="position:relative;top:1;left:1;width:20;height:20">
   </v:rect>
```



 

 