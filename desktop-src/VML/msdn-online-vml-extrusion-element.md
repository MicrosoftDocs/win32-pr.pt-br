---
title: Elemento Extrusion VML
description: Elemento Extrusion VML
ms.assetid: d26b2451-383a-4ded-a46d-5ecca05ddb7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9ee19db9d933f0b6b749c3165281614d1be87b0e0828f43849f8a36a5b37067
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118601336"
---
# <a name="vml-extrusion-element"></a>Elemento Extrusion VML

Este tópico descreve o VML, um recurso que foi preterido a partir Windows Internet Explorer 9. As páginas da Web e os aplicativos que dependem do VML devem ser migrados para o SVG ou outros padrões amplamente suportados.

> [!Note]  
> A partir de dezembro de 2011, este tópico foi arquivado. Como resultado, ele não é mais mantido ativamente. Para obter mais informações, consulte [Conteúdo arquivado.](/previous-versions/windows/internet-explorer/ie-developer/) Para obter informações, recomendações e diretrizes sobre a versão atual do Windows Internet Explorer, consulte [Internet Explorer Developer Center.](https://msdn.microsoft.com/ie/)

 

Define umaion para uma forma.

Os atributos a seguir modificam uma interceptação.



| Atributo                                                              | Descrição                                                                                             |
|------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------|
| [AutoRotationCenter](msdn-online-vml-autorotationcenter-attribute.md) | Determina se o centro de rotação será o centro geométrico daion.                |
| [BackDepth](msdn-online-vml-backdepth-attribute.md)                   | Define a quantidade deion para trás.                                                               |
| [Brightness](msdn-online-vml-brightness-attribute.md)                 | Especifica a quantidade de brilho de uma cena.                                                          |
| [Cor](color-attribute--extrusion--vml.md)                           | Define a cor das faces de paleta.                                                               |
| [Colormode](msdn-online-vml-colormode-attribute.md)                   | Determina o modo de cor de paleta.                                                                 |
| [Difusidade](msdn-online-vml-diffusity-attribute.md)                   | Define a quantidade de difusão de luz refletida de uma forma extrudida.                              |
| [Edge](msdn-online-vml-edge-attribute.md)                             | Define o bevel aparente das bordas deion.                                                      |
| [Ext](ext-attribute--extrusion--vml.md)                               | Define o comportamento de predefinição para editores gráficos.                                           |
| [Faceta](msdn-online-vml-facet-attribute.md)                           | Define o número de facetas usadas para descrever superfícies curvadas de umaion.                          |
| [ForeDepth](msdn-online-vml-foredepth-attribute.md)                   | Define a quantidade deion de avanço.                                                                |
| [LightFace](msdn-online-vml-lightface-attribute.md)                   | Determina se a face frontal daion responderá às alterações na iluminação.             |
| [LightHarsh](msdn-online-vml-lightharsh-attribute.md)                 | Determina se a fonte de luz primária será dura.                                              |
| [LightHarsh2](msdn-online-vml-lightharsh2-attribute.md)               | Determina se a fonte de luz secundária será dura.                                            |
| [LightLevel](msdn-online-vml-lightlevel-attribute.md)                 | Define a intensidade da fonte de luz primária para a cena.                                        |
| [LightLevel2](msdn-online-vml-lightlevel2-attribute.md)               | Define a intensidade da fonte de luz secundária para a cena.                                      |
| [LightPosition](msdn-online-vml-lightposition-attribute.md)           | Especifica a posição da luz primária em uma cena.                                                 |
| [LightPosition2](msdn-online-vml-lightposition2-attribute.md)         | Especifica a posição da luz secundária em uma cena.                                               |
| [LockRotationCenter](msdn-online-vml-lockrotationcenter-attribute.md) | Determina se a rotação do objeto extruded é especificada pelo atributo **RotationAngle.** |
| [Metal](msdn-online-vml-metal-attribute.md)                           | Determina se a superfície da forma extrudada será semelhante ao metal.                               |
| [Ativado](on-attribute--extrusion--vml.md)                                 | Determina se umaion será exibida.                                                      |
| [Orientation](msdn-online-vml-orientation-attribute.md)               | Especifica o vetor em torno do qual uma forma será girada.                                              |
| [OrientationAngle](msdn-online-vml-orientationangle-attribute.md)     | Define o ângulo que umaion gira em torno da orientação.                                     |
| [Avião](msdn-online-vml-plane-attribute.md)                           | Especifica o plano que está em ângulos à direita para aion.                                           |
| [Render](msdn-online-vml-render-attribute.md)                         | Define o modo de renderização daion.                                                            |
| [RotationAngle](msdn-online-vml-rotationangle-attribute.md)           | Especifica a rotação do objeto sobre os eixos x e y.                                           |
| [RotationCenter](msdn-online-vml-rotationcenter-attribute.md)         | Especifica o centro de rotação de uma forma.                                                           |
| [Luminosidade](msdn-online-vml-shininess-attribute.md)                   | Define a concentração da luz refletida de uma superfície deion.                                   |
| [SkewAmt](msdn-online-vml-skewamt-attribute.md)                       | Define a quantidade de distorção de umaion.                                                             |
| [SkewAngle](msdn-online-vml-skewangle-attribute.md)                   | Define o ângulo de distorção de umaion.                                                              |
| [Especularidade](msdn-online-vml-specularity-attribute.md)               | Define a especificação de uma forma extrudada.                                                           |
| [Tipo](type-attribute--extrusion--vml.md)                             | Define a maneira como a forma é extrudida.                                                             |
| [Vista](msdn-online-vml-viewpoint-attribute.md)                   | Define o ponto de vista do observador.                                                                  |
| [ViewpointOrigin](msdn-online-vml-viewpointorigin-attribute.md)       | Define a origem do ponto de vista dentro da caixa delimitada da forma.                               |



 

**Comentários**

Esse elemento deve ser definido dentro de um [elemento Shape.](shape-element--vml.md)

Além disso, o [atributo On](on-attribute--extrusion--vml.md) deve ser definido como **True.**

A seguir está o código mínimo necessário para produzir umaion.


```HTML
   <v:rect style="width:50px;height:50px">
   <v:extrusion on="True"/>
   </v:rect>
```



**Exemplos**

-   [Shape Shape Simples](/previous-versions/bb229656(v=vs.85))
-   [Dynamic Shape Extrusion](/previous-versions/bb229657(v=vs.85))

 

 