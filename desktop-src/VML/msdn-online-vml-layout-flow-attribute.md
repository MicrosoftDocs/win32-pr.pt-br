---
title: Atributo Layout-Flow de VML
description: Atributo Layout-Flow de VML
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e437e31043afcf7fba4967076a861c9bca86477
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917466"
---
# <a name="vml-layout-flow-attribute"></a>Atributo Layout-Flow de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Determina o fluxo do layout de texto em uma caixa de texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxe de marca**

<v: *Element* estilo = "layout-Flow: *expressão* " >

**Comentários**

Os valores são:



| Valor                  | Descrição                                 |
|------------------------|---------------------------------------------|
| horizontal             | O texto é exibido horizontalmente. Padrão.    |
| vertical               | O texto é exibido verticalmente.               |
| vertical-Ideograma   | O texto ideográficar é exibido verticalmente.   |
| Ideograma horizontal | O texto ideográficar é exibido horizontalmente. |



 

*Atributo padrão da VML*

**Exemplo**

O fluxo de texto na TextBox fluirá verticalmente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 