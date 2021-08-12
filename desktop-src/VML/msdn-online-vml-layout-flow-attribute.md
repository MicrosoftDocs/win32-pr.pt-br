---
title: Atributo de Layout-Flow VML
description: Atributo de Layout-Flow VML
ms.assetid: 63b06dcb-5179-4046-9e02-4441d0d7bcd6
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bde6937a3f93ff2a462cfc5950c13b7f3910573c54d82449ef705bca4afbb068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118599350"
---
# <a name="vml-layout-flow-attribute"></a>Atributo de Layout-Flow VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Determina o fluxo do layout de texto em uma caixa de texto. Leitura/gravação. **Cadeia de caracteres**.

**Aplica-se a**

[TextBox](msdn-online-vml-textbox-element.md)

**Sintaxe de marca**

<v: *element* style="layout-flow: *expression* ">

**Comentários**

Os valores são:



| Valor                  | Descrição                                 |
|------------------------|---------------------------------------------|
| horizontal             | O texto é exibido horizontalmente. Padrão.    |
| Vertical               | O texto é exibido verticalmente.               |
| vertical-ideographic   | O texto ideográfico é exibido verticalmente.   |
| horizontal-ideographic | O texto ideográfico é exibido horizontalmente. |



 

*Atributo padrão VML*

**Exemplo**

O fluxo de texto na caixa de texto fluirá verticalmente.


```HTML
   <v:shape id="rect01"
   coordorigin="0 0" coordsize="200 200"
   strokecolor="red" fillcolor="red"
   style="top:1;left:1;width:50;height:50"
   path="m 1,1 l 1,200, 200,200, 200,1 x e">
   <textbox string="VML text" layout-flow="vertical"/>
   </v:shape>
```



 

 