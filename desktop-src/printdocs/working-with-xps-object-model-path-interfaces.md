---
description: Esta seção descreve como usar as interfaces relacionadas a caminho da API de documento XPS em um OM XPS.
ms.assetid: 4e76355a-ad53-4177-b8c7-3e768a1d4e3f
title: Trabalhando com interfaces de caminho de OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 136d742db0b176875715b3b715c4401bb8131323ceeb9f8d2a77311fb75a0672
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119460326"
---
# <a name="working-with-xps-om-path-interfaces"></a>Trabalhando com interfaces de caminho de OM XPS

Esta seção descreve como usar as interfaces relacionadas a caminho da API de documento XPS em um OM XPS.



| Nome da interface                                                            | Filhos conceituais                                                                                                                                                                                                                                                                                                                                                                                                                                         | Descrição                                                                                                                                                                                       |
|---------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)<br/>                               | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Descreve um elemento de caminho gráfico.<br/>                                                                                                                                                    |
| [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush)<br/>                             | [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/> [**IXpsOMTileBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomtilebrush)<br/> [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/> [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/> [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush)<br/> [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Um pincel é usado para preencher uma área ou uma linha.<br/>                                                                                                                                             |
| [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)<br/>         | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornece traços ou preenchimentos de cor sólidos. <br/>                                                                                                                                                |
| [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)<br/>                 | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornece um objeto visual, como um caminho, glifo ou tela, ou um Visual parcial a ser usado como um preenchimento ou traçado de divisão. <br/>                                                                  |
| [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)<br/>                   | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornece uma imagem (ou imagem parcial) a ser usada como um preenchimento ou traçado de divisão. <br/>                                                                                                           |
| [**IXpsOMLinearGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomlineargradientbrush)<br/> | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornece um gradiente linear a ser usado como um preenchimento ou um traço. <br/>                                                                                                                            |
| [**IXpsOMRadialGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomradialgradientbrush)<br/> | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Fornece um gradiente radial a ser usado como um preenchimento ou um traço. <br/>                                                                                                                            |
| [**IXpsOMGradientStop**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientstop)<br/>               | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Define um ponto de inflexão de valor de cor único dentro de um gradiente linear ou radial. <br/>                                                                                                     |
| [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)<br/>                       | [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>                                                                                                                                                                                                                                                                                                                                                                                             | Fornece uma definição de uma região de vetor a ser usada como uma definição de caminho ou região de recorte. Consiste em uma ou mais interfaces [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) . <br/> |
| [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)<br/>           | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Parte de uma definição de região que é referenciada por uma interface [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) e que consiste em um ou mais segmentos. <br/>                                    |
| [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)<br/>         | Nenhum<br/>                                                                                                                                                                                                                                                                                                                                                                                                                                             | Especifica a transformação da matriz afim a ser aplicada ao objeto durante a renderização. <br/>                                                                                              |



 

## <a name="contents"></a>Sumário

-   [Pincéis de OM XPS](xps-object-model-brushes.md)
-   [Gradientes de OM XPS](xps-object-model-gradients.md)
-   [Objetos de geometria de OM XPS](xps-object-model-geometry-objects.md)

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**Interface IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**Interface IXpsOMDashCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomdashcollection)
</dt> <dt>

[**Interface IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform)
</dt> </dl>

 

 




