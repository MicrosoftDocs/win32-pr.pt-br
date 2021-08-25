---
title: Elemento de inclinação da VML
description: Elemento de inclinação da VML
ms.assetid: ab58bbd9-5fb2-434f-adea-9b3d2d170804
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71d659d16e6d10e9ec88875989a812de82403d2ac5b946580e7c7b7def956b45
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120099036"
---
# <a name="vml-skew-element"></a>Elemento de inclinação da VML

este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). para obter informações, recomendações e orientações sobre a versão atual do Windows Internet explorer, consulte [internet explorer developer Center](https://msdn.microsoft.com/ie/).

 

Define uma distorção para uma forma.

Os atributos a seguir modificam uma distorção.



| Atributo                                 | Descrição                                    |
|-------------------------------------------|------------------------------------------------|
| [Externa](ext-attribute--skew--vml.md)       | Define a maneira como uma distorção é exibida.           |
| [ID](id-attribute--skew--vml.md)         | Define um identificador exclusivo para uma distorção.        |
| [Matriz](matrix-attribute--skew--vml.md) | Define uma transformação de perspectiva para uma distorção.    |
| [Deslocamento](offset-attribute--skew--vml.md) | Define o deslocamento de uma distorção.                  |
| [Ativado](on-attribute--skew--vml.md)         | Determina se a distorção será exibida. |
| [Origem](origin-attribute--skew--vml.md) | Determina a origem de uma distorção.               |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

Além disso, a [matriz](matrix-attribute--skew--vml.md) e [os](on-attribute--skew--vml.md) atributos devem ser definidos como **true**.

Veja a seguir o código mínimo necessário para produzir uma distorção.


```HTML
   <v:rect
   fillcolor="green"
   style="position:relative;top:1;left:1;width:50;height:50">
   <o:skew on="t" matrix="1,-0.5,0,0.75,0,0"/>
   </v:rect>
```



o elemento **Skew** é uma extensão Microsoft Office para VML.

**Exemplos**

-   [Exemplo de distorção simples](/previous-versions/bb229482(v=vs.85))
-   [Exemplo de distorção dinâmica](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/skew/x_skew.md)

 

 