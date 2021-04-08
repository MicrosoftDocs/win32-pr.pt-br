---
title: Atributo FillType da VML
description: Atributo FillType da VML
ms.assetid: c6870100-8fb9-4589-9b83-cd46cc17eeb3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e880f7d13c7db647c586431f492a301ccf1aba0b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917655"
---
# <a name="vml-filltype-attribute"></a>Atributo FillType da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define o tipo de preenchimento usado para o plano de fundo de um traço. Leitura/gravação. **VgFillType**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* FILLIN = " *expression* " >

**Sintaxe do script**

*elemento* . FillType = "*expressão*"

*expressão* = de *elemento*. FillType

**Comentários**

Os valores são:



| DashStyle | Descrição                                    |
|-----------|------------------------------------------------|
| Sólido     | O padrão de preenchimento é sólido. Valor padrão.      |
| Tile      | A imagem de preenchimento é disposta lado a lado.                       |
| Padrão   | A imagem de preenchimento é ampliada para formar um padrão. |
| Quadro     | A imagem de preenchimento torna-se uma borda para a forma. |



 

*Atributo padrão da VML*

**Exemplo**

O traço da forma tem uma textura do lado do ladrilho criado a partir da imagem de cylinder.gif.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke width="5pt" filltype="tile" src="cylinder.gif"/>
   </v:shape>
```



 

 