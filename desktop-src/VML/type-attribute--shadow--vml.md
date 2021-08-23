---
title: Atributo type (Shadow)(VML)
description: Atributo type (Shadow)(VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d90a264cbaf77890e39f10d56103c8acdc84727de21d7f2de9946911b6df41dd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119513156"
---
# <a name="type-attribute-shadowvml"></a>Atributo type (Shadow)(VML)

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Especifica o tipo de sombra. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: *element* type=" *expressão* ">

**Sintaxe do script**

*element* .type="*expression*"

*expressão* = *elemento*.type

**Comentários**

Os valores são:



| Valor           | Descrição                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| único          | Sombra única. Padrão.                                                                                                                                                                              |
| double          | Uma sombra dupla. [Color2](color2-attribute--shadow--vml.md) é usado para a cor da segunda sombra e [Offset2](msdn-online-vml-offset2-attribute.md) é usado para o deslocamento da segunda sombra. |
| perspectiva     | Uma sombra de perspectiva.                                                                                                                                                                                |
| shapeRelative   | A sombra é criada em relação à forma.                                                                                                                                                         |
| drawingRelative | A sombra é criada em relação ao desenho.                                                                                                                                                       |
| Emboss          | A sombra tem uma aparência embossada.                                                                                                                                                                     |



 

**Atributo padrão VML**

**Exemplo**

Uma sombra dupla é criada com a segunda sombra verde e deslocamento 5 pontos para baixo e para a direita.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 