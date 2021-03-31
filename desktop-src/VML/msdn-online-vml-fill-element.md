---
title: Elemento Fill VML
description: Elemento Fill VML
ms.assetid: ea790017-5aaa-4e75-8fc7-77fc94fd1d1e
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bdc7205baa9db0eaa7d84d4022057f81804ea790
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917656"
---
# <a name="vml-fill-element"></a>Elemento Fill VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um preenchimento para uma forma.

Os atributos a seguir modificam um preenchimento.



| Atributo                                                          | Descrição                                            |
|--------------------------------------------------------------------|--------------------------------------------------------|
| [AlignShape](msdn-online-vml-alignshape-attribute.md)             | Determina se uma imagem será alinhada com uma forma.   |
| [AltHRef](althref-attribute--fill--vml.md)                        | Especifica uma referência alternativa para uma imagem.         |
| [Firmeza](angle-attribute--fill--vml.md)                            | Define o ângulo de um preenchimento gradual.                  |
| [Aspecto](msdn-online-vml-aspect-attribute.md)                     | Especifica como o aspecto da imagem de preenchimento será preservado. |
| [Cor](color-attribute--fill--vml.md)                            | Define a cor de um preenchimento.                           |
| [Color2](color2-attribute--fill--vml.md)                          | Define a segunda cor para um preenchimento.                   |
| [Cores](msdn-online-vml-colors-attribute.md)                     | Define várias cores para um preenchimento gradual.           |
| [DetectMouseClick](detectmouseclick-attribute--fill--vml.md)      | Determina se um clique do mouse é detectado.          |
| [Foco](msdn-online-vml-focus-attribute.md)                       | Define o centro de um preenchimento gradiente linear.          |
| [FocusPosition](msdn-online-vml-focusposition-attribute.md)       | Define o centro de um preenchimento gradiente radial.          |
| [FocusSize](msdn-online-vml-focussize-attribute.md)               | Define o tamanho do foco para um preenchimento radial.              |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Define uma URL para o arquivo de imagem original.              |
| [ID](id-attribute--fill--vml.md)                                  | Define um identificador exclusivo para o preenchimento.              |
| [Método](msdn-online-vml-method-attribute.md)                     | Define o método usado para gerar um preenchimento gradual.   |
| [Ativado](on-attribute--fill--vml.md)                                  | Determina se o colocará de preenchimento deve ser exibido.          |
| [Opacidade](opacity-attribute--fill--vml.md)                        | Define a transparência de um preenchimento.                    |
| [Opacity2](msdn-online-vml-opacity2-attribute.md)                 | Define a transparência da segunda cor de preenchimento.     |
| [Ter](origin-attribute--fill--vml.md)                          | Define o centro de uma imagem.                        |
| [Posição](position-attribute--fill--vml.md)                      | Define a posição de uma imagem.                      |
| [Tamanho](size-attribute--fill--vml.md)                              | Define o tamanho de uma imagem.                          |
| [Orig](src-attribute--fill--vml.md)                                | Define a imagem a ser carregada para um preenchimento.                  |
| [Título](title-attribute--fill--vml.md)                            | Define o título de um preenchimento.                           |
| [Tipo](type-attribute--fill--vml.md)                              | Define o tipo de preenchimento.                              |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

O código a seguir mostra um preenchimento de gradiente simples para uma forma.


```HTML
   <v:shape
   style="position:relative;top:1;left:1;width:400;height:400"
   path = "m 1,1 l 1,200, 200,200, 200,1 x e">
   <v:fill type=gradient color="blue" color2="yellow"/>
   </v:shape>
```



**Exemplos**

-   [Preenchimento de gradiente simples](/previous-versions/bb229620(v=vs.85))
-   [Exemplo de preenchimento dinâmico](/previous-versions/bb229621(v=vs.85))

 

 