---
description: Este tópico fornece um exemplo de como usar as interfaces relacionadas à geometria em um OM XPS.
ms.assetid: 2663c6fc-301e-4765-b37c-b5e29a714ce8
title: Objetos de geometria OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: db68127535b37e216d28423a034083e979f58c714cbbbee875bc3f1621974bfe
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112086"
---
# <a name="xps-om-geometry-objects"></a>Objetos de geometria OM XPS

Este tópico fornece um exemplo de como usar as interfaces relacionadas à geometria em um OM XPS.

## <a name="create-a-rectangular-geometry"></a>Criar uma geometria retangular

O exemplo de código a seguir cria um objeto geometry que descreve uma forma retangular fechada.


```C++
    HRESULT                         hr = S_OK;
    IXpsOMVisualCollection          *canvasVisuals = NULL;
    IXpsOMPath                      *pathSidebar = NULL;
    IXpsOMGeometry                  *xpsGeometry = NULL;
    IXpsOMGeometryFigure            *xpsFigure = NULL;
    IXpsOMGeometryFigureCollection  *xpsFigureCollection = NULL;
    IXpsOMSolidColorBrush           *sidebarBrush = NULL;

    XPS_POINT      startPoint;
    XPS_RECT       shape;

    // define the rectangle
    shape.x = 10.0f;
    shape.y = 10.0f;
    shape.height = 100.0f;
    shape.width = 200.0f;

    // set the start point
    startPoint.x = shape.x;
    startPoint.y = shape.y;

    // define the segment types to be straight lines
    XPS_SEGMENT_TYPE sidebarSegmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // define the points of the rectangular shape
    // other than the start point
    FLOAT sidebarSegmentData[6] = {
        shape.x,               shape.y + shape.height,
        shape.x + shape.width, shape.y + shape.height,
        shape.x + shape.width, shape.y
    };

    // set the lines to be solid (not stroked)
    BOOL sidebarSegmentStrokes[3] = {
        FALSE, FALSE, FALSE
    };

    // create the geometry figure interface
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &xpsFigure );

    // close the figure so that the last segment point is
    // connected to the start point
    hr = xpsFigure->SetIsClosed( TRUE );

    // set the shape to be filled by the fill brush
    hr = xpsFigure->SetIsFilled( TRUE );

    // set the segments using the information defined above
    hr = xpsFigure->SetSegments(
        3, 
        6, 
        sidebarSegmentTypes,
        sidebarSegmentData, 
        sidebarSegmentStrokes);

    // create a geometry using the figure just created
    hr = xpsFactory->CreateGeometry(&xpsGeometry);

    // get a pointer to the figure collection
    hr = xpsGeometry->GetFigures(&xpsFigureCollection);

    // and add the figure of the rectangle to the geometry
    hr = xpsFigureCollection->Append(xpsFigure);
```



Para obter mais informações sobre como adicionar segmentos a uma figura de geometria, consulte os exemplos de código nos tópicos de referência do método [**IXpsOMGeometryFigure::GetSegmentData**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata) e [**IXpsOMGeometryFigure::SetSegments Method**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setsegments) .

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[**IXpsOMGeometry Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[**IXpsOMGeometryFigure Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[**Método IXpsOMGeometryFigure::GetSegmentData**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-getsegmentdata)
</dt> <dt>

[**Método IXpsOMGeometryFigure::SetSegments**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsomgeometryfigure-setsegments)
</dt> <dt>

[**IXpsOMGeometryFigureCollection Interface**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> </dl>

 

 



