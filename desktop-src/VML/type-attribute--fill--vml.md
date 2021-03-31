---
title: Atributo de tipo (Fill) (VML)
description: Atributo de tipo (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb40999b9596a41a8469e586dcc8a7f934577e36
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641476"
---
# <a name="type-attribute-fillvml"></a>Atributo de tipo (Fill) (VML)

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina o tipo de preenchimento. Leitura/gravação. **VgFillType**.

**Aplica-se a**

[Preencher](msdn-online-vml-fill-element.md)

**Sintaxe de marca**

<v: tipo de *elemento* = " *expressão* " >

**Sintaxe do script**

*elemento* . Type = "*expressão*"

*expressão* = de *elemento*. Type

**Comentários**

Os valores são:



| Type           | Description                                                             |
|----------------|-------------------------------------------------------------------------|
| consolidou          | O padrão de preenchimento é sólido. Padrão.                                     |
| gradiente       | As cores de preenchimento se misturam em um gradiente linear de baixo para cima. |
| gradientradial | As cores de preenchimento mesclam juntas em um gradiente radial.                    |
| bloco           | A imagem de preenchimento é disposta lado a lado.                                                |
| pattern        | A imagem é usada para criar um padrão usando as cores de preenchimento.            |
| frame          | A imagem é ampliada para preencher a forma.                               |



 

**Atributo padrão da VML**

**Exemplo**

Um preenchimento de primeiro plano vermelho e plano de fundo azul é criado usando o padrão da imagem myimage.gif.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill color="red" color2="blue" type="pattern" src="myimage.gif"/>
   </v:shape>
```



 

 