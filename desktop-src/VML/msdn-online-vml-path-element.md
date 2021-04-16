---
title: Elemento de caminho VML
description: Elemento de caminho VML
ms.assetid: c5b9f9e3-edee-45fa-9387-8f15e09983ee
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1de9440761479d6b3dc6cb10c96b00ea48626247
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "105757729"
---
# <a name="vml-path-element"></a>Elemento de caminho VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define um caminho para uma forma.

Os atributos a seguir modificam uma sombra.



| Atributo                                                        | Descrição                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------|
| [Arrowok](msdn-online-vml-arrowok-attribute.md)                 | Determina se as pontas de seta serão exibidas.                                |
| [ConnectAngles](msdn-online-vml-connectangles-attribute.md)     | Especifica como uma curva se conectará a um ponto de conexão.                       |
| [ConnectLocs](msdn-online-vml-connectlocs-attribute.md)         | Define o local dos pontos de conexão em um caminho.                            |
| [Connecttype](msdn-online-vml-connecttype-attribute.md)         | Define o tipo de ponto de conexão usado para anexar formas a outras formas. |
| [ExtrusionOK](msdn-online-vml-extrusionok-attribute.md)         | Determina se uma extrusão será exibida.                              |
| [FillOK](msdn-online-vml-fillok-attribute.md)                   | Determina se um preenchimento será exibido.                                    |
| [GradientShapeOK](msdn-online-vml-gradientshapeok-attribute.md) | Determina se uma forma de gradiente será exibida.                          |
| [ID](id-attribute--path--vml.md)                                | Define um identificador exclusivo para um caminho.                                         |
| [Limo](msdn-online-vml-limo-attribute.md)                       | Define um ponto de ampliação no caminho.                                            |
| [ShadowOK](msdn-online-vml-shadowok-attribute.md)               | Determina se uma sombra será exibida.                                  |
| [StrokeOK](msdn-online-vml-strokeok-attribute.md)               | Determina se um traço será exibido.                                  |
| [TextBoxRect](msdn-online-vml-textboxrect-attribute.md)         | Define uma ou mais caixas de textdentro de uma forma.                                   |
| [TextPathOK](msdn-online-vml-textpathok-attribute.md)           | Determina se um TextPath será exibido.                                |
| [V](msdn-online-vml-v-attribute.md)                             | Define os comandos que compõem um caminho.                                       |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

O código a seguir mostra como definir uma forma com um caminho.


```HTML
   <v:shape strokecolor="red"
   coordorigin="0 0" coordsize="200 200"
   style="top:1;left:1;width:50;height:50">
   <v:path v="m 1,1 l 1,200, 200,200, 200,1 x e"/>
   </v:shape>
```



Observe que o atributo [V](msdn-online-vml-v-attribute.md) de **Path** substitui o atributo [Path](msdn-online-vml-path-attribute.md) de [Shape](shape-element--vml.md).

**Exemplos**

-   [Exemplo de elemento filho Path simples](/previous-versions/bb229545(v=vs.85))
-   [Exemplo de elemento filho de caminho dinâmico](https://samples.msdn.microsoft.com/workshop/samples/vml/shape/path/x_path.md)

 

 