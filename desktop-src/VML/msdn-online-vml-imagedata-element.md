---
title: Elemento Imagedata VML
description: Elemento Imagedata VML
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0d3a307dd36daf0ff08d2fab7cd9086a3bc07447872cf36cb41972e4aa5a4d4c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118600287"
---
# <a name="vml-imagedata-element"></a>Elemento Imagedata VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define uma imagem para uma forma.

Os atributos a seguir modificam uma imagem.



| Atributo                                                          | Descrição                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [AltHRef](althref-attribute--imagedata--vml.md)                   | Especifica uma referência alternativa para uma imagem.                        |
| [Bilevel](msdn-online-vml-bilevel-attribute.md)                   | Determina se uma imagem será exibida em preto e branco.          |
| [BlackLevel](msdn-online-vml-blacklevel-attribute.md)             | Determina a intensidade de preto em uma imagem.                        |
| [Chromakey](msdn-online-vml-chromakey-attribute.md)               | Define a cor no paleta que será tratada como transparente. |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | Define o percentual de remoção de imagem do lado inferior.       |
| [CropLeft](msdn-online-vml-cropleft-attribute.md)                 | Define o percentual de remoção de imagem do lado esquerdo.         |
| [CropRight](msdn-online-vml-cropright-attribute.md)               | Define o percentual de remoção de imagem do lado direito.        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | Define o percentual de remoção de imagem do lado superior.          |
| [DetectMouseClick](detectmouseclick-attribute--imagedata--vml.md) | Determina se um clique do mouse será detectado.                    |
| [EmbossColor](msdn-online-vml-embosscolor-attribute.md)           | Define a cor para efeitos de cor embossed.                         |
| [Ganhar](msdn-online-vml-gain-attribute.md)                         | Define a intensidade de todas as cores em uma imagem.                      |
| [Gama](msdn-online-vml-gamma-attribute.md)                       | Define a quantidade de contraste para uma imagem.                          |
| [Cinza](msdn-online-vml-grayscale-attribute.md)               | Determina se uma imagem será exibida no modo de escala de cinza.          |
| [Href](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Define uma URL para uma imagem.                                           |
| [ID](id-attribute--image--vml.md)                                 | Define um identificador exclusivo para uma imagem.                             |
| [Filme](msdn-online-vml-movie-attribute.md)                       | Define um ponteiro para uma imagem de filme.                                   |
| [OLEID](msdn-online-vml-oleid-attribute.md)                       | Armazena a ID OLE de uma imagem.                                        |
| [Src](src-attribute--imagedata--vml.md)                           | Define uma origem para a imagem.                                       |
| [Título](title-attribute--imagedata--vml.md)                       | Define o título de uma imagem.                                        |



 

**Comentários**

Esse elemento deve ser definido dentro de um [elemento Shape.](shape-element--vml.md)

Além disso, o [**atributo Src**](src-attribute--imagedata--vml.md) deve apontar para uma imagem.

A seguir está o código mínimo necessário para produzir uma imagem.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> Em versões de pré-lançamento do VML, esse elemento era chamado **de Imagem** .

 

**Exemplos**

-   [Exemplo de ImageData simples](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Exemplo de Dynamic ImageData](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 