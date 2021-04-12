---
title: Elemento Extrusion VML
description: Elemento Extrusion VML
ms.assetid: d26b2451-383a-4ded-a46d-5ecca05ddb7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6a6160a035853153c615576c3875ef9d90791245
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366229"
---
# <a name="vml-extrusion-element"></a>Elemento Extrusion VML

Este tópico descreve a VML, um recurso que foi preterido a partir do Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem de VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [conteúdo arquivado](/previous-versions/windows/internet-explorer/ie-developer/). Para obter informações, recomendações e orientações sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center](https://msdn.microsoft.com/ie/).

 

Define uma extrusão para uma forma.

Os atributos a seguir modificam uma extrusão.



| Atributo                                                              | Descrição                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [AutoRotationCenter](msdn-online-vml-autorotationcenter-attribute.md) | Determina se o centro de rotação será o centro geométrico da extrusão.                |
| [Profundidade de fundo](msdn-online-vml-backdepth-attribute.md)                   | Define a quantidade de extrusão regressiva.                                                               |
| [Brightness](msdn-online-vml-brightness-attribute.md)                 | Especifica a quantidade de brilho de uma cena.                                                          |
| [Cor](color-attribute--extrusion--vml.md)                           | Define a cor das faces da extrusão.                                                               |
| [ColorMode](msdn-online-vml-colormode-attribute.md)                   | Determina o modo de cor da extrusão.                                                                 |
| [Difusão](msdn-online-vml-diffusity-attribute.md)                   | Define a quantidade de difusão de luz refletida de uma forma extrudada.                              |
| [Edge](msdn-online-vml-edge-attribute.md)                             | Define o bisel aparente das bordas de extrusão.                                                      |
| [Externa](ext-attribute--extrusion--vml.md)                               | Define o comportamento de extrusão padrão para editores gráficos.                                           |
| [Faceta](msdn-online-vml-facet-attribute.md)                           | Define o número de facetas usadas para descrever superfícies curvas de uma extrusão.                          |
| [ForeDepth](msdn-online-vml-foredepth-attribute.md)                   | Define a quantidade de extrusão posterior.                                                                |
| [LightFace](msdn-online-vml-lightface-attribute.md)                   | Determina se a face frontal da extrusão responderá às alterações na iluminação.             |
| [LightHarsh](msdn-online-vml-lightharsh-attribute.md)                 | Determina se a fonte de luz primária será dura.                                              |
| [LightHarsh2](msdn-online-vml-lightharsh2-attribute.md)               | Determina se a fonte de luz secundária será dura.                                            |
| [LightLevel](msdn-online-vml-lightlevel-attribute.md)                 | Define a intensidade da fonte de luz primária para a cena.                                        |
| [LightLevel2](msdn-online-vml-lightlevel2-attribute.md)               | Define a intensidade da fonte de luz secundária para a cena.                                      |
| [LightPosition](msdn-online-vml-lightposition-attribute.md)           | Especifica a posição da luz primária em uma cena.                                                 |
| [LightPosition2](msdn-online-vml-lightposition2-attribute.md)         | Especifica a posição da luz secundária em uma cena.                                               |
| [LockRotationCenter](msdn-online-vml-lockrotationcenter-attribute.md) | Determina se a rotação do objeto extrudada é especificada pelo atributo **RotationAngle** . |
| [Metal](msdn-online-vml-metal-attribute.md)                           | Determina se a superfície da forma extrudada será semelhante a um metal.                               |
| [Ativado](on-attribute--extrusion--vml.md)                                 | Determina se uma extrusão será exibida.                                                      |
| [Direção](msdn-online-vml-orientation-attribute.md)               | Especifica o vetor em volta do qual uma forma será girada.                                              |
| [OrientationAngle](msdn-online-vml-orientationangle-attribute.md)     | Define o ângulo que uma extrusão gira em torno da orientação.                                     |
| [Aérea](msdn-online-vml-plane-attribute.md)                           | Especifica o plano que está em ângulos retos para a extrusão.                                           |
| [Render](msdn-online-vml-render-attribute.md)                         | Define o modo de renderização da extrusão.                                                            |
| [RotationAngle](msdn-online-vml-rotationangle-attribute.md)           | Especifica a rotação do objeto sobre os eixos x e y.                                           |
| [RotationCenter](msdn-online-vml-rotationcenter-attribute.md)         | Especifica o centro de rotação para uma forma.                                                           |
| [Luminosidade](msdn-online-vml-shininess-attribute.md)                   | Define a concentração de luz refletida de uma superfície de extrusão.                                   |
| [SkewAmt](msdn-online-vml-skewamt-attribute.md)                       | Define a quantidade de distorção de uma extrusão.                                                             |
| [SkewAngle](msdn-online-vml-skewangle-attribute.md)                   | Define o ângulo de distorção de uma extrusão.                                                              |
| [Refletir](msdn-online-vml-specularity-attribute.md)               | Define a especulação de uma forma extrudada.                                                           |
| [Tipo](type-attribute--extrusion--vml.md)                             | Define a maneira como a forma é extrudada.                                                             |
| [Ponto](msdn-online-vml-viewpoint-attribute.md)                   | Define o ponto de vista do observador.                                                                  |
| [ViewpointOrigin](msdn-online-vml-viewpointorigin-attribute.md)       | Define a origem do ponto de vista dentro da caixa delimitadora da forma.                               |



 

**Comentários**

Esse elemento deve ser definido dentro de um elemento [Shape](shape-element--vml.md) .

Além disso, o atributo [on](on-attribute--extrusion--vml.md) deve ser definido como **true**.

Veja a seguir o código mínimo necessário para produzir uma extrusão.


```HTML
   <v:rect style="width:50px;height:50px">
   <v:extrusion on="True"/>
   </v:rect>
```



**Exemplos**

-   [Extrusão de forma simples](/previous-versions/bb229656(v=vs.85))
-   [Extrusão de forma dinâmica](/previous-versions/bb229657(v=vs.85))

 

 