---
title: Elemento TextBox do VML
description: Elemento TextBox do VML
ms.assetid: 3573256e-f241-4de7-8541-252c92109af7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 84b6ef160e975f00dd859e0f6db6f2821054a34815b3aef1ea19f520ad3d01a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118597505"
---
# <a name="vml-textbox-element"></a>Elemento TextBox do VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma caixa de texto para uma forma.

Os atributos a seguir modificam uma caixa de texto.



| Atributo                                                                    | Descrição                                                |
|------------------------------------------------------------------------------|------------------------------------------------------------|
| [Direção](msdn-online-vml-direction-attribute.md)                         | Define a direção do texto.                         |
| [ID](id-attribute--textbox--vml.md)                                         | Define um identificador exclusivo para a caixa de texto.               |
| [Inserir](msdn-online-vml-inset-attribute.md)                                 | Especifica valores de margem interna para texto da caixa de texto.            |
| [InsetMode](msdn-online-vml-insetmode-attribute.md)                         | Define como um aplicativo permitirá valores de inset personalizados. |
| [Layout-Flow](msdn-online-vml-layout-flow-attribute.md)                     | Determina o fluxo do texto na caixa de texto.            |
| [MSO-Direction-Alt](msdn-online-vml-mso-direction-alt-attribute.md)         | Define instruções alternativas para texto em caixas de texto.        |
| [MSO-Fit-Shape-to-Text](msdn-online-vml-mso-fit-shape-to-text-attribute.md) | Determina se uma forma será alongada para se ajustar ao texto.       |
| [MSO-Fit-Text-To-Shape](msdn-online-vml-mso-fit-text-to-shape-attribute.md) | Determina se o texto será estendido para se ajustar a uma forma.       |
| [MSO-Layout-Flow-Alt](msdn-online-vml-mso-layout-flow-alt-attribute.md)     | Define o fluxo de layout alternativo para texto em uma caixa de texto.   |
| [Caixa de texto MSO-Next](msdn-online-vml-mso-next-textbox-attribute.md)           | Especifica a próxima caixa de texto em uma série.                    |
| [Rotação de MSO](msdn-online-vml-mso-rotate-attribute.md)                       | Determina se o texto gira com uma forma girada.      |
| [MSO-Text-Scale](msdn-online-vml-mso-text-scale-attribute.md)               | Define o fator de dimensionamento para ajustar o texto às formas.     |
| [Singleclick](msdn-online-vml-singleclick-attribute.md)                     | Determina se o texto é selecionável com um único clique. |
| [Âncora de texto V](msdn-online-vml-v-text-anchor-attribute.md)                 | Define a ancoragem vertical do texto em uma caixa de texto.       |



 

**Comentários**

Esse elemento deve ser definido dentro de um [elemento Shape.](shape-element--vml.md)

A seguir está o código mínimo necessário para produzir uma caixa de texto.


```HTML
   <v:oval strokecolor="red" fillcolor="yellow
   style="position:relative;top:50;left:50;width:75;height:50">
   <v:textbox>VML</v:textbox>
   </v:oval>
```



Observe que o texto exibido na caixa de texto é incluído pelas marcas TextBox. O texto dentro das marcas pode ser modificado por marcas HTML comuns.

**Exemplo**

-   [Exemplo de Caixa de Texto Simples](/previous-versions/bb264075(v=vs.85))

 

 