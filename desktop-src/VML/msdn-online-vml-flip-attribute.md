---
title: Atributo de flip da VML
description: Atributo de flip da VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d7d17c224ee8ec04a5dcf301ad501de51323efe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641811"
---
# <a name="vml-flip-attribute"></a>Atributo de flip da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Alterna a orientação de uma forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *Element* estilo = "flip: *expression* " >

**Sintaxe do script**

*elemento* . Style. flip = "*expressão*"

*expressão* = de *elemento*. Style. flip

**Comentários**

Os valores são:



| Valor | Descrição                                           |
|-------|-------------------------------------------------------|
| x     | Inverter ao longo do eixo y, revertendo as coordenadas *x*. |
| a     | Inverter ao longo do eixo *x*, revertendo as coordenadas y. |
| xy    | Inverta o eixo y e *x*.                  |
| yx    | Inverta o eixo *x* e *y*.                |



 

*Atributo padrão da VML*

**Consulte também**

[VgFlipOrientation](msdn-online-vector-markup-language-object-model-reference.md)

**Exemplo**

A forma é invertida ao longo do eixo *y* , revertendo as coordenadas *x* .


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Exemplo de atributo flip](/previous-versions/bb229670(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 