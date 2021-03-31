---
title: Atributo WrapCoords de VML
description: Atributo WrapCoords de VML
ms.assetid: 14a67ca9-3d36-4523-bdb1-5b7c36cd3d39
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61a4dc57b37cd84563c8ba3132244dff6daf6b23
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641265"
---
# <a name="vml-wrapcoords-attribute"></a>Atributo WrapCoords de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o polígono delimitador que circunda uma forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* o:wrapcoords = " *expressão* " >

**Comentários**

Descreve uma lista delimitada por vírgulas de x e ycoordinates; ou seja, "x1, y1, X2, Y2, X3, Y3,..." Isso é usado quando o texto é rigidamente disposto em torno de uma forma. O padrão é **NULL** (uma cadeia de caracteres vazia) até que o atributo **mso-Wrap-Mode** seja definido como **apertado** ou **até**.

*Atributo de extensões de Microsoft Office*

**Exemplo**

A forma tem uma caixa delimitadora de texto que é de 5 unidades maior do que o caminho.


```HTML
   <v:shape id="rect01" WrapCoords="0,0 0,200, 200,200, 200,0"
   fillcolor="red" strokecolor="red"
   coordorigin="-500 -500" coordsize="1000 1000"
   style="position:relative;top:0;left:0;width:100pt;height:100pt;mso-wrap-distance-top:10pt"
   path="m 5,5 l 5,195, 195,195, 195,5 x e">
   </v:shape>
```



 

 