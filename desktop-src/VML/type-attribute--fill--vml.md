---
title: Atributo de tipo (Fill) (VML)
description: Atributo de tipo (Fill) (VML)
ms.assetid: 5dcc53cd-a156-48cd-ae32-951660d91556
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 883318c82758178ee9693a1199cb76c5798e351ec809aecb54fe7d0a266d85d4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118596137"
---
# <a name="type-attribute-fillvml"></a>Atributo de tipo (Fill) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

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



| Tipo           | Descrição                                                             |
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



 

 