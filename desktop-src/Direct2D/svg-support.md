---
title: Suporte a SVG
description: A partir da atualização de aniversário do Windows 10, o Direct2D dá suporte à renderização de fontes de cores que contêm contornos de glifos SVG, conforme descrito na especificação OpenType (consulte a tabela ' SVG ').
ms.assetid: 5cb4cb7c-9b96-e110-bff9-d75ad1980010
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 678c5d9ef42a53c854bb2f175fac63816345c519
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366060"
---
# <a name="svg-support"></a>Suporte a SVG

A partir da atualização de aniversário do Windows 10, o Direct2D dá suporte à renderização de [fontes de cores](../directwrite/color-fonts.md) que contêm contornos de glifos SVG, conforme descrito na [especificação OpenType](/typography/opentype/spec/) (consulte [a tabela SVG](/typography/opentype/spec/svg)). A partir da atualização do Windows 10 para criadores, o Direct2D também dá suporte à renderização de imagens SVG autônomas. No entanto, determinados recursos SVG não são permitidos em fontes de SVG OpenType e determinados recursos de SVG atualmente não são compatíveis com o Direct2D.  

Este tópico identifica o conjunto de recursos [SVG 1,1](https://www.w3.org/TR/SVG11/) com suporte do Direct2D na atualização de aniversário do Windows 10 e mais recente. Este documento se aplica ao SVG em fontes OpenType, bem como a imagens SVG autônomas.

## <a name="supported-svg-elements-and-attributes"></a>Elementos e atributos SVG com suporte

O Direct2D dá suporte à renderização dos seguintes elementos SVG e dos atributos associados para cada elemento. Outros elementos e atributos regulares são ignorados.



| Elemento                                                                                  | Atributos regulares com suporte                                                             |
|------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------|
| [Multiplica](https://www.w3.org/TR/SVG11/shapes.mdl#circleelement)                           | ID, estilo, transformação, CX, Cy, r                                                          |
| [clipPath](https://www.w3.org/TR/SVG11/masking.mdl#clippathelement)                      | ID, estilo, transformação, clipPathUnits                                                      |
| [defs](https://www.w3.org/TR/SVG11/struct.mdl#defselement)                               | ID, estilo, transformação                                                                     |
| [crescente](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup>  | id                                                                                       |
| [elipse](https://www.w3.org/TR/SVG11/shapes.mdl#ellipseelement)                         | ID, estilo, transformação, CX, Cy, RX, entar                                                     |
| [m](https://www.w3.org/TR/SVG11/struct.mdl#gelement)                                     | ID, estilo, transformação                                                                     |
| [imagem](https://www.w3.org/TR/SVG11/struct.mdl#imageelement)                             | ID, estilo, transformação, x, y, largura, altura, preserveAspectRatio, xlink: href               |
| [descritos](https://www.w3.org/TR/SVG11/shapes.mdl#lineelement)                               | ID, estilo, transformação, x1, y1, X2, Y2                                                     |
| [linearGradient](https://www.w3.org/TR/SVG11/pservers.mdl#lineargradientelement)         | ID, estilo, x1, y1, X2, Y2, gradientUnits, gradientTransform, spreadMethod, xlink: href    |
| [path](https://www.w3.org/TR/SVG11/paths.mdl#pathelement)                                | ID, estilo, transformação, d                                                                  |
| [Polygon](https://www.w3.org/TR/SVG11/shapes.mdl#polygonelement)                         | ID, estilo, transformação, pontos                                                             |
| [múltipla](https://www.w3.org/TR/SVG11/shapes.mdl#polylineelement)                       | ID, estilo, transformação, pontos                                                             |
| [radialGradient](https://www.w3.org/TR/SVG11/pservers.mdl#radialgradientelement)         | ID, estilo, CX, Cy, r, FX, AF, gradientUnits, gradientTransform, spreadMethod, xlink: href |
| [Rect](https://www.w3.org/TR/SVG11/shapes.mdl#rectelement)                               | ID, estilo, transformação, x, y, largura, altura, RX, entar                                        |
| [stop](https://www.w3.org/TR/SVG11/pservers.mdl#stopelement)                             | ID, estilo, deslocamento                                                                        |
| [escaláveis](https://www.w3.org/TR/SVG11/struct.mdl#svgelement)                                 | ID, estilo, x, y, largura, altura, viewBox, preserveAspectRatio                             |
| [título](https://www.w3.org/TR/SVG11/struct.mdl#descriptionandtitleelements)<sup>\*</sup> | id                                                                                       |
| [uso](https://www.w3.org/TR/SVG11/struct.mdl#useelement)                                 | ID, estilo, transformação, x, y, largura, altura, xlink: href                                    |



 

<sup>\*</sup> Somente com suporte na atualização do Windows 10 para criadores e mais recente

## <a name="supported-svg-presentation-attributes"></a>Atributos de apresentação SVG com suporte

O Direct2D também dá suporte aos seguintes atributos de apresentação. Elas podem ser especificadas em qualquer elemento SVG, mas afetam apenas a aparência de determinados elementos, conforme descrito na especificação SVG (consulte os [atributos de apresentação](https://www.w3.org/TR/SVG11/attindex.mdl#presentationattributes)).

-   caminho do clipe
-   regra de clipe
-   cor
-   display<sup>\*</sup>
-   fill
-   preenchimento – opacidade
-   preencher regra
-   opacidade
-   estouro
-   cor de parada
-   parar-opacidade
-   curso
-   Stroke-dashArray
-   Stroke-DashOffset
-   Stroke-LineCap
-   Stroke-LineJoin
-   Stroke-MiterLimit
-   traço-opacidade
-   largura do traço
-   Visualizar<sup>\*</sup>

<sup>\*</sup> Somente com suporte na atualização do Windows 10 para criadores e mais recente

## <a name="unsupported-svg-features"></a>Recursos SVG sem suporte

### <a name="unsupported-elements-and-attributes"></a>Elementos e atributos sem suporte

Qualquer elemento ou atributo não incluído nas listas acima é considerado sem suporte pelo Direct2D. Ao analisar o conteúdo SVG que contém um elemento ou atributo sem suporte, a entidade sem suporte é ignorada. O restante do conteúdo é renderizado da forma mais fiel possível.

### <a name="unsupported-length-units"></a>Unidades de comprimento sem suporte

A partir da atualização de aniversário do Windows 10, o Direct2D dá suporte apenas a valores de comprimento de espaço de usuário e valores de comprimento percentual. Não há suporte para comprimentos com sufixos de unidade, como "mm" ou "em".

A partir da atualização dos criadores de outono do Windows 10, o Direct2D também dá suporte a identificadores de unidade absolutas: px, pt, PC, cm, mm e in. Não há suporte para identificadores de unidade relativos (em, ex).

### <a name="unsupported-image-sources"></a>Fontes de imagens sem suporte

O elemento Image só terá suporte se seu atributo xlink: href estiver definido como uma imagem codificada em base64. Não há suporte para referências remotas.

 

 