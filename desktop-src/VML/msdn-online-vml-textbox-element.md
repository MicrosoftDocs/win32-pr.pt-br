---
title: Elemento TextBox da VML
description: Elemento TextBox da VML
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 34a46ce8b6636b79099b7f7423fd8f746602a00f
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641166"
---
# <a name="vml-textbox-element"></a>Elemento TextBox da VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma caixa de texto para uma forma.

Os atributos a seguir modificam uma caixa de texto.



| Atributo                                                                    | Descrição                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Direção](msdn-online-vml-direction-attribute.md)                         | Define a direção do texto.                         |
| [ID](id-attribute--textbox--vml.md)                                         | Define um identificador exclusivo para a caixa de texto.               |
| [Levo](msdn-online-vml-inset-attribute.md)                                 | Especifica valores de margem interna para texto de TextBox.            |
| [Acinserir](msdn-online-vml-insetmode-attribute.md)                         | Define como um aplicativo permitirá valores de inserção personalizados. |
| [Layout-fluxo](msdn-online-vml-layout-flow-attribute.md)                     | Determina o fluxo do texto na caixa de texto.            |
| [MSO-Direction-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Define direções alternativas para texto em caixas de textos.        |
| [MSO-ajustar-forma-a-texto](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Determina se uma forma será alongada para ajustar o texto.       |
| [Die-ajuste de texto para forma](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Determina se o texto será alongado para se ajustar a uma forma.       |
| [MSO-layout-Flow-Alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Define o fluxo de layout alternativo para texto em uma caixa de texto.   |
| [MSO-Next-TextBox](msdn-online-vml-mso-next-textbox-attribute.md)           | Especifica a próxima caixa de texto em uma série.                    |
| [MSO-girar](msdn-online-vml-mso-rotate-attribute.md)                       | Determina se o texto gira com uma forma girada.      |
| [MSO – escala de texto](msdn-online-vml-mso-text-scale-attribute.md)               | Define o fator de dimensionamento para ajustar o texto às formas.     |
| [SingleClick](msdn-online-vml-singleclick-attribute.md)                     | Determina se o texto é selecionável com um único clique. |
| [Ancoragem de texto V](msdn-online-vml-v-text-anchor-attribute.md)                 | Define a ancoragem vertical do texto em uma caixa de texto.       |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

Veja a seguir o código mínimo necessário para produzir uma caixa de texto.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Observe que o texto exibido na caixa de texto é colocado entre as marcas de caixa de texto. O texto dentro das marcas pode ser modificado por marcas HTML comuns.

**Exemplo**

-   [Exemplo da caixa de texto simples](/previous-versions/bb264075(v=vs.85))

 

 