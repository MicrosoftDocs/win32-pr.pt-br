---
title: Elemento VMLFrame VML
description: Elemento VMLFrame VML
ms.assetid: a1582223-d6e2-42d1-95bb-97f6f1d453d2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f53371afb0c2790ff6dd666f0121b30b586c51b
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104084597"
---
# <a name="vml-vmlframe-element"></a>Elemento VMLFrame VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um quadro para uma forma externa.

Os atributos a seguir modificam um quadro.



| Atributo                                     | Descrição                                                           |
|-----------------------------------------------|-----------------------------------------------------------------------|
| [Clipe](msdn-online-vml-clip-attribute.md)    | Determina se a imagem será recortada.                         |
| [ID](id-attribute--vmlframe--vml.md)         | Define um identificador exclusivo para o quadro.                            |
| [Ter](origin-attribute--vmlframe--vml.md) | Especifica a origem do quadro.                                    |
| [Tamanho](size-attribute--vmlframe.md)          | Especifica o tamanho do quadro.                                      |
| [Orig](src-attribute--vmlframe--vml.md)       | Especifica a origem dos dados que serão exibidos no quadro. |
| [Estilo](msdn-online-vml-style-attribute.md)  | Define os estilos normais de CSS que podem ser usados para posicionar o quadro. |



 

**Comentários**

Os dados de origem a serem exibidos no quadro podem estar contidos na mesma página da Web ou fazer parte de outra página. Por meio de scripts, a origem pode ser alterada dinamicamente e as características de exibição podem ser modificadas.

Os objetos dentro de **VMLFrame** são "zoom reduzido". Ou seja, eles são dimensionados como os metaarquivos, em que os pesos de linha, deslocamentos de sombra e área de texto são todos dimensionados proporcionalmente. Isso é diferente de um grupo, onde o tamanho e a posição do objeto são dimensionados proporcionalmente, mas linha, sombra etc. não são.

Veja a seguir o código mínimo necessário para carregar uma imagem em um quadro.


```HTML
   <v:vmlframe
     style="top:1;left:1;width:50;height:50">
     src="external.vml#rect01"/>
   </v:vmlframe>
```



Se o arquivo for externo, ele deverá ser um arquivo XML. O código a seguir é o código mínimo necessário para especificar um arquivo de origem externo que deve conter uma forma identificável. Este exemplo contém uma forma de imagem que exibe um bitmap.


```HTML
   <xml xmlns:v = "urn:schemas-microsoft-com:vml">
   <v:image id="rect01"
     style="height:100;width:100;top:50;left:50">
     src="kids.jpg">
   </v:rect>
   </xml>
```



> [!Note]  
> Nas versões de pré-lançamento do VML, esse elemento era chamado de **VMLCanvas** .

 

**Exemplos**

-   [Exemplo de VMLFrame simples](/previous-versions/bb263920(v=vs.85))
-   [Exemplo de VMLFrame dinâmico](/previous-versions/bb263902(v=vs.85))

 

 