---
title: Elemento Stroke VML
description: Elemento Stroke VML
ms.assetid: 300ecde5-f19d-4ff7-89a4-af9b8e82ae9d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62048227fca074276b825ceedb793eaa9a5d84dc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104454133"
---
# <a name="vml-stroke-element"></a>Elemento Stroke VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um traço para uma forma.

Os atributos a seguir modificam um traço.



| Atributo                                                          | Descrição                                                   |
|--------------------------------------------------------------------|---------------------------------------------------------------|
| [AltHRef](althref-attribute--stroke--vml.md)                      | Especifica uma referência alternativa para um traço.                |
| [Cor](color-attribute--stroke--vml.md)                          | Define a cor de um traço.                                |
| [Color2](color2-attribute--stroke--vml.md)                        | Define uma segunda cor para um traço.                          |
| [DashStyle](msdn-online-vml-dashstyle-attribute.md)               | Especifica o padrão de ponto e tracejado para um traço.              |
| [Seta de fim](msdn-online-vml-endarrow-attribute.md)                 | Define um estilo de ponta de seta para o final de um traço.           |
| [EndArrowLength](msdn-online-vml-endarrowlength-attribute.md)     | Define um comprimento de ponta de seta para o final de um traço.          |
| [EndArrowWidth](msdn-online-vml-endarrowwidth-attribute.md)       | Define uma largura de seta para o final de um traço.           |
| [EndCap](msdn-online-vml-endcap-attribute.md)                     | Define o estilo de extremidade para o final de um traço.                |
| [FillType](msdn-online-vml-filltype-attribute.md)                 | Define o tipo de preenchimento usado para o plano de fundo de um traço. |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229431(v=vs.85))    | Define a URL para a imagem original para o traço.         |
| [ID](id-attribute--stroke--vml.md)                                | Define um identificador exclusivo para o traço.                   |
| [ImageAlignShape](msdn-online-vml-imagealignshape-attribute.md)   | Determina o alinhamento de uma imagem de traço.                   |
| [ImageAspect](msdn-online-vml-imageaspect-attribute.md)           | Define como a taxa de proporção da imagem de traço será preservada.  |
| [ImageSize](msdn-online-vml-imagesize-attribute.md)               | Define o tamanho da imagem para o traço.                 |
| [Joinstyle](msdn-online-vml-joinstyle-attribute.md)               | Define o estilo de junção de uma polilinha.                         |
| [Estilo de Linha](msdn-online-vml-linestyle-attribute.md)               | Define o estilo de linha de um traço.                           |
| [MiterLimit](msdn-online-vml-miterlimit-attribute.md)             | Define a suavidade de uma junção de mitre.                      |
| [Ativado](on-attribute--stroke--vml.md)                                | Determina se o traço será exibido.              |
| [Opacidade](opacity-attribute--stroke--vml.md)                      | Define a quantidade de transparência de um traço.               |
| [Orig](src-attribute--stroke--vml.md)                              | Define a imagem de origem a ser carregada para um preenchimento de traço.           |
| [StartArrow](msdn-online-vml-startarrow-attribute.md)             | Define a ponta de seta para o início de um traço.              |
| [StartArrowLength](msdn-online-vml-startarrowlength-attribute.md) | Define o comprimento da ponta de seta para o início de um traço.       |
| [StartArrowWidth](msdn-online-vml-startarrowwidth-attribute.md)   | Define a largura da ponta de seta para o início de um traço.        |
| [Título](title-attribute--stroke--vml.md)                          | Define o título de um traço.                                |
| [Weight](msdn-online-vml-weight-attribute.md)                     | Define a espessura de um traço.                            |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

O código a seguir mostra como o elemento **Stroke** pode ser usado para modificar uma linha.


```HTML
   <v:line
   to="300pt,50pt" from="50pt,50pt">
   <v:stroke weight="50pt" color="red" linestyle="ThickThin"/>
   </v:line>
```



**Exemplos**

-   [Exemplo de traço simples](/previous-versions/bb229466(v=vs.85))
-   [Exemplo de imagem de traço](/previous-versions/bb229468(v=vs.85))

 

 