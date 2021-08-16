---
title: Atributo de in flip do VML
description: Atributo de in flip do VML
ms.assetid: 0d3d4c54-e769-4f6b-a9f5-6e48125a7215
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5293bdff5ab888b13fdc095038e74fdbcf725bbfb1948a04018fbf5a22c5677c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118346630"
---
# <a name="vml-flip-attribute"></a>Atributo de in flip do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Alterna a orientação de uma forma. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Forma](shape-element--vml.md)

**Sintaxe de marca**

<v: *element* style="flip: *expression* ">

**Sintaxe do script**

*expressão element* .style.flip=""

*expressão* = *elemento*.style.flip

**Comentários**

Os valores são:



| Valor | Descrição                                           |
|-------|-------------------------------------------------------|
| x     | Inversão ao longo do eixo y, revertendo *as coordenadas x.* |
| a     | Inversão ao longo *do eixo x,* revertendo as coordenadas y. |
| xy    | Inverter ao longo dos eixos y e *x.*                  |
| Yx    | Inverter ao longo dos *eixos x*- *e y*.                |



 

*Atributo padrão VML*

**Consulte também**

[VgFlipOrientation](msdn-online-vector-markup-language-object-model-reference.md)

**Exemplo**

A forma é invertida ao longo *do eixo y,* revertendo as *coordenadas x-.*


```HTML
   <v:rect id=myrect fillcolor="red"
   style="position:relative;top:1;left:1;width:20;height:20;flip:x">
   </v:rect>
```



[Exemplo de atributo flip](/previous-versions/bb229670(v=vs.85)). (Requer o Microsoft Internet Explorer 5 ou superior.)

 

 