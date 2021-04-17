---
title: Elemento ImageData de VML
description: Elemento ImageData de VML
ms.assetid: 91004646-b031-4973-a32d-7afdd10dab48
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1b416a53f97efc8a1f1875eda0e842c4cfbe96bf
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105789731"
---
# <a name="vml-imagedata-element"></a>Elemento ImageData de VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma imagem para uma forma.

Os atributos a seguir modificam uma imagem.



| Atributo                                                          | Descrição                                                           |
|--------------------------------------------------------------------|-----------------------------------------------------------------------|
| [AltHRef](althref-attribute--imagedata--vml.md)                   | Especifica uma referência alternativa para uma imagem.                        |
| [Binível](msdn-online-vml-bilevel-attribute.md)                   | Determina se uma imagem será exibida em preto e branco.          |
| [BlackLevel](msdn-online-vml-blacklevel-attribute.md)             | Determina a intensidade de preto em uma imagem.                        |
| [Chromakey](msdn-online-vml-chromakey-attribute.md)               | Define a cor no palatte que será tratada como transparente. |
| [CropBottom](msdn-online-vml-cropbottom-attribute.md)             | Define a porcentagem de remoção de imagem do lado inferior.       |
| [CropLeft](msdn-online-vml-cropleft-attribute.md)                 | Define a porcentagem de remoção de imagem do lado esquerdo.         |
| [CropRight](msdn-online-vml-cropright-attribute.md)               | Define a porcentagem de remoção de imagem do lado direito.        |
| [CropTop](msdn-online-vml-croptop-attribute.md)                   | Define a porcentagem de remoção de imagem do lado superior.          |
| [DetectMouseClick](detectmouseclick-attribute--imagedata--vml.md) | Determina se um clique do mouse será detectado.                    |
| [EmbossColor](msdn-online-vml-embosscolor-attribute.md)           | Define a cor para efeitos de cor em relevo.                         |
| [Conheça](msdn-online-vml-gain-attribute.md)                         | Define a intensidade de todas as cores em uma imagem.                      |
| [Gama](msdn-online-vml-gamma-attribute.md)                       | Define a quantidade de contraste para uma imagem.                          |
| [Escala](msdn-online-vml-grayscale-attribute.md)               | Determina se uma imagem será exibida no modo de escala de cinza.          |
| [HRef](/previous-versions/windows/internet-explorer/ie-developer/platform-apis/bb229574(v=vs.85)) | Define uma URL para uma imagem.                                           |
| [ID](id-attribute--image--vml.md)                                 | Define um identificador exclusivo para uma imagem.                             |
| [Filme](msdn-online-vml-movie-attribute.md)                       | Define um ponteiro para uma imagem de filme.                                   |
| [OLEID](msdn-online-vml-oleid-attribute.md)                       | Armazena a ID de OLE de uma imagem.                                        |
| [Orig](src-attribute--imagedata--vml.md)                           | Define uma origem para a imagem.                                       |
| [Título](title-attribute--imagedata--vml.md)                       | Define o título de uma imagem.                                        |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

Além disso, o atributo [**src**](src-attribute--imagedata--vml.md) deve apontar para uma imagem.

Veja a seguir o código mínimo necessário para produzir uma imagem.


```HTML
   <v:rect
   style="position:relative;top:1;left:1;width:50;height:50">
   <v:imagedata src="../art/kids.jpg"/>
   </v:rect>
```



> [!Note]  
> Nas versões de pré-lançamento do VML, esse elemento era chamado de **imagem** .

 

**Exemplos**

-   [Exemplo de ImageData simples](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/t_image.md)
-   [Exemplo de ImageData dinâmico](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/image/x_image.md)

 

 