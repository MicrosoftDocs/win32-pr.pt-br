---
title: Atributo Color2 (Stroke) (VML)
description: Atributo Color2 (Stroke) (VML)
ms.assetid: 60b8035e-9477-4f8b-817b-dd6c41bdfa79
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 108c767f7337f486f8b7df5a4506b3b3d487dabf146656890def0c5e1ad32a88
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867426"
---
# <a name="color2-attribute-strokevml"></a>Atributo Color2 (Stroke) (VML)

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define uma segunda cor para traços. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[Pincel](msdn-online-vml-stroke-element.md)

**Sintaxe de marca**

<v: *Element* color2 = " *expressão* " >

Sintaxe do script

*Element* . color2 = "*expressão*"

*expressão* = de *elemento*. color2

**Comentários**

Uma segunda cor é usada quando o tipo de preenchimento de um traço é um padrão.

*Atributo padrão da VML*

**Exemplo**

O traço da forma é um preenchimento de padrão em que o preenchimento é definido pela imagem de origem, mas o plano de fundo transparente é definido pela segunda cor.


```HTML
   <v:shape id="rect01"
   strokecolor="red" fillcolor="red"
   style="top:20;left:20;width:30;height:30"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:stroke filltype="pattern" width="5pt" src="cylinder.gif" color2="green"/>
   </v:shape>
```



 

 