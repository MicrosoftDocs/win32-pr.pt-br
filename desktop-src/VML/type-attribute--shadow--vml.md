---
title: Atributo de tipo (sombra) (VML)
description: Atributo de tipo (sombra) (VML)
ms.assetid: 569957c6-508a-4323-804d-25f9a3e58c38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fea4fb54c04847a8ed5c4446cfb999f74161aa97
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366362"
---
# <a name="type-attribute-shadowvml"></a>Atributo de tipo (sombra) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Especifica o tipo de sombra. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Shadow](msdn-online-vml-shadow-element.md)

**Sintaxe de marca**

<v: tipo de *elemento* = " *expressão* " >

**Sintaxe do script**

*elemento* . Type = "*expressão*"

*expressão* = de *elemento*. Type

**Comentários**

Os valores são:



| Valor           | Descrição                                                                                                                                                                                          |
|-----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| único          | Sombra única. Padrão.                                                                                                                                                                              |
| double          | Uma sombra dupla. [Color2](color2-attribute--shadow--vml.md) é usado para a cor da segunda sombra e [Offset2](msdn-online-vml-offset2-attribute.md) é usado para o deslocamento da segunda sombra. |
| perspectiva     | Uma sombra em perspectiva.                                                                                                                                                                                |
| shapeRelative   | A sombra é criada em relação à forma.                                                                                                                                                         |
| drawingRelative | A sombra é criada em relação ao desenho.                                                                                                                                                       |
| embaralha          | A sombra tem uma aparência em relevo.                                                                                                                                                                     |



 

**Atributo padrão da VML**

**Exemplo**

Uma sombra dupla é criada com o segundo verde de sombra e deslocamento de 5 pontos para baixo e para a direita.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:shadow on="True" type="double" color2="green" offset2="5pt,5pt"/>
   </v:shape>
```



 

 