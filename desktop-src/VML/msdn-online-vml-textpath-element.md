---
title: Elemento TextPath VML
description: Elemento TextPath VML
ms.assetid: dcc3b723-4c5c-4069-93c7-c41737292109
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08707ae79bf297e6094228b26ae118c57a03c736
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105757728"
---
# <a name="vml-textpath-element"></a>Elemento TextPath VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um caminho de texto para uma forma.

Os atributos a seguir modificam um caminho de texto.



| Atributo                                                                    | Descrição                                                                    |
|------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [FitPath](msdn-online-vml-fitpath-attribute.md)                             | Define se o texto se ajusta ao caminho de uma forma.                             |
| [FitShape](msdn-online-vml-fitshape-attribute.md)                           | Define se o texto se ajusta aos limites da forma.                            |
| [Família de fontes](msdn-online-vml-font-family-attribute.md)                     | Especifica a família de fontes de texto.                                             |
| [Tamanho da fonte](msdn-online-vml-font-size-attribute.md)                         | Especifica o tamanho da fonte do texto.                                               |
| [Estilo de fonte](msdn-online-vml-font-style-attribute.md)                       | Especifica o estilo de fonte do texto.                                              |
| [Fonte-variante](msdn-online-vml-font-variant-attribute.md)                   | Especifica a variante de fonte de texto.                                            |
| [Espessura da fonte](msdn-online-vml-font-weight-attribute.md)                     | Especifica o peso da fonte de texto.                                             |
| [Fonte](msdn-online-vml-font-attribute.md)                                   | Especifica o valor da fonte composta de texto.                                     |
| [Die-text-shadow](msdn-online-vml-mso-text-shadow-attribute.md)             | Define se uma sombra é aplicada ao texto.                               |
| [Ativado](on-attribute--textpath--vml.md)                                        | Define se o texto é exibido.                                         |
| [Cadeia de caracteres](msdn-online-vml-string-attribute.md)                               | Define a cadeia de texto.                                                       |
| [Decoração de texto](msdn-online-vml-text-decoration-attribute.md)             | Define a decoração de texto do texto.                                       |
| [Trim](msdn-online-vml-trim-attribute.md)                                   | Define se o espaço extra é removido acima e abaixo do texto.               |
| [V-girar-letras](msdn-online-vml-v-rotate-letters-attribute.md)           | Determina se as letras do texto são giradas.                        |
| [Altura da mesma letra](msdn-online-vml-v-same-letter-heights-attribute.md) | Determina se todas as letras terão a mesma altura.                      |
| [Alinhamento de texto V](msdn-online-vml-v-text-align-attribute.md)                   | Define o alinhamento do texto.                                             |
| [Kerning de texto em V](msdn-online-vml-v-text-kern-attribute.md)                     | Determina se o kerning está ativado.                                       |
| [V-texto-reverso](msdn-online-vml-v-text-reverse-attribute.md)               | Determina se a ordem de layout das linhas é invertida.                       |
| [Modo de espaçamento de texto V](msdn-online-vml-v-text-spacing-mode-attribute.md)     | Define o modo para espaçamento.                                            |
| [Espaçamento de texto V](msdn-online-vml-v-text-spacing-attribute.md)               | Define a quantidade de espaçamento do texto.                                        |
| [XScale](msdn-online-vml-xscale-attribute.md)                               | Determina se um TextPath direto será usado em vez do caminho da forma. |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

Além dos atributos de preenchimento, Cadeia de caracteres e estilo normais, o atributo [TextPathOK](msdn-online-vml-textpathok-attribute.md) do [caminho](msdn-online-vml-path-element.md) deve ser definido como **true** e o atributo [on](on-attribute--textpath--vml.md) de TextPath deve ser definido como **true** para exibir o texto em um caminho de texto.

Veja a seguir o código mínimo necessário para exibir o texto em um caminho.


```HTML
   <v:line from="50 200" to="400 100">
   <v:fill on="True" color="red"/>
   <v:path textpathok="True"/>
   <v:textpath on="True" string="VML Text"
   style="font:normal normal normal 36pt Arial"/>
   </v:line>
```



**Exemplos**

-   [Exemplo de TextPath simples](/previous-versions/bb264038(v=vs.85))
-   [Exemplo de tipo de loadpath dinâmico](/previous-versions/bb264042(v=vs.85))
-   [Exemplo de curva de TextPath dinâmico](/previous-versions/bb264041(v=vs.85))

 

 