---
description: Esta página descreve como desenhar gráficos em um OM XPS.
ms.assetid: 2384b522-208a-48db-ae0d-f82fa0214d09
title: Desenhar gráficos em um OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0ee2f9eacb19ba39263cff3898451479d8bed28e1d83ac6fe251fb9b4da62f49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119719306"
---
# <a name="draw-graphics-in-an-xps-om"></a>Desenhar gráficos em um OM XPS

Esta página descreve como desenhar gráficos em um OM XPS.

Para desenhar gráficos baseados em vetor em uma página, insinue uma interface [**IXpsOMPath,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) popule-a com o conteúdo desejado e adicione-a à lista de objetos visuais da página ou da tela. Uma interface **IXpsOMPath** contém essas propriedades de uma forma baseada em vetor como o contorno, a cor de preenchimento, o estilo de linha e a cor da linha. A forma do caminho é especificada por uma interface [**IXpsOMGeometry,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) que contém uma coleção de interfaces [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) e, opcionalmente, uma interface [**IXpsOMMatrixTransform.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) Você pode usar qualquer interface herdada da interface [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) para preencher o perímetro do caminho e o interior da forma descrita pelo caminho.

Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [Tarefas comuns de programação de documentos XPS.](common-xps-document-tasks.md)

## <a name="code-example"></a>Exemplo de código

O exemplo de código a seguir cria um caminho simples que descreve um retângulo que é preenchido com uma única cor.

### <a name="create-the-stroke-and-the-fill-brushes"></a>Criar o traço e os pincéis de preenchimento

A primeira seção do exemplo de código cria [**o IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) que será usado para preencher o objeto de caminho.


```C++
    HRESULT               hr = S_OK;

    XPS_COLOR             xpsColor;
    IXpsOMSolidColorBrush *xpsFillBrush = NULL;
    IXpsOMSolidColorBrush *xpsStrokeBrush = NULL;

    // Set the fill brush color to RED.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0xFF;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
        &xpsColor,
        NULL,          // color profile resource
        &xpsFillBrush);
    // The color profile resource parameter is NULL because
    //  this color type does not use a color profile resource.

    // Set the stroke brush color to BLACK.
    xpsColor.colorType = XPS_COLOR_TYPE_SRGB;
    xpsColor.value.sRGB.alpha = 0xFF;
    xpsColor.value.sRGB.red = 0x00;
    xpsColor.value.sRGB.green = 0x00;
    xpsColor.value.sRGB.blue = 0x00;

    // Use the object factory to create the brush.
    hr = xpsFactory->CreateSolidColorBrush( 
            &xpsColor,
            NULL, // This color type does not use a color profile resource.
            &xpsStrokeBrush);

    // The brushes are released below after they have been used.
```



### <a name="define-the-shape"></a>Definir a forma

A segunda seção do exemplo de código cria a interface [**IXpsOMGeometry.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) Em seguida, ele cria a interface [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) que especifica a forma da figura e adiciona a figura à interface **IXpsOMGeometry.** O exemplo cria um retângulo especificado por *rect*. Os segmentos devem ser definidos para apenas três dos quatro lados do retângulo. O perímetro da forma, o retângulo nesse caso, começa do ponto inicial e se estende conforme definido pelos segmentos da figura de geometria. Definir a **propriedade IsClosed** como **TRUE** indica que o retângulo é fechado adicionando um segmento adicional que conecta o final do último segmento ao ponto de partida.


```C++
    // rect is initialized outside of the sample and 
    //  contains the coordinates of the rectangular geometry to create.
    XPS_RECT                            rect = {0,0,100,100};       

    HRESULT                             hr = S_OK;
    IXpsOMGeometryFigure                *rectFigure;
    IXpsOMGeometry                      *imageRectGeometry;
    IXpsOMGeometryFigureCollection      *geomFigureCollection;

    // Define the start point and create an empty figure.
    XPS_POINT                           startPoint = {rect.x, rect.y};
    hr = xpsFactory->CreateGeometryFigure( &startPoint, &rectFigure );
    // Define the segments of the geometry figure.
    //  First, define the type of each segment.
    XPS_SEGMENT_TYPE segmentTypes[3] = {
        XPS_SEGMENT_TYPE_LINE,  // each segment is a straight line
        XPS_SEGMENT_TYPE_LINE, 
        XPS_SEGMENT_TYPE_LINE
    };

    // Define the x and y coordinates of each corner of the figure
    //  the start point has already been defined so only the 
    //  remaining three corners need to be defined.
    FLOAT segmentData[6] = {
        rect.x,                (rect.y + rect.height),
        (rect.x + rect.width), (rect.y + rect.height), 
        (rect.x + rect.width), rect.y 
    };

    // Describe if the segments are stroked (that is if the segment lines
    //  should be drawn as a line).
    BOOL segmentStrokes[3] = {
        TRUE, TRUE, TRUE // Yes, draw each of the segment lines.
    };

    // Add the segment data to the figure.
    hr = rectFigure->SetSegments(
                        3, 
                        6, 
                        segmentTypes, 
                        segmentData, 
                        segmentStrokes);

    // Set the closed and filled properties of the figure.
    hr = rectFigure->SetIsClosed( TRUE );
    hr = rectFigure->SetIsFilled( TRUE );
 
    // Create the geometry object.
    hr = xpsFactory->CreateGeometry( &imageRectGeometry );
    
    // Get a pointer to the figure collection interface of the geometry...
    hr = imageRectGeometry->GetFigures( &geomFigureCollection );

    // ...and then add the figure created above to this geometry.
    hr = geomFigureCollection->Append( rectFigure );
    // If not needed for anything else, release the rectangle figure.
    rectFigure->Release();

    // when done adding figures, release the figure collection. 
    geomFigureCollection->Release();

    //  When done with the geometry object, release the object.
    // imageRectGeometry->Release();
    //  In this case, imageRectGeometry is used in the next sample
    //  so the geometry object is not released, yet.
    
```



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a>Criar o caminho e adicioná-lo à coleção visual

A seção final deste exemplo de código cria e configura o objeto de caminho e, em seguida, adiciona-o à lista de objetos visuais da página.


```C++
    HRESULT                    hr = S_OK;
    // The page interface pointer is initialized outside of this sample.
    IXpsOMPath                *rectPath = NULL;
    IXpsOMVisualCollection    *pageVisuals = NULL;

    // Create the new path object.
    hr = xpsFactory->CreatePath( &rectPath );

    // Add the geometry to the path.
    //  imageRectGeometry is initialized outside of this example.
    hr = rectPath->SetGeometryLocal( imageRectGeometry );

    // Set the short description of the path to provide
    //  a textual description of the object for accessibility.
    hr = rectPath->SetAccessibilityShortDescription( L"Red Rectangle" );
    
    // Set the fill and stroke brushes to use the brushes 
    //  created in the first section.
    hr = rectPath->SetFillBrushLocal( xpsFillBrush );
    hr = rectPath->SetStrokeBrushLocal( xpsStrokeBrush);

    // Get the visual collection of this page and add this path to it.
    hr = xpsPage->GetVisuals( &pageVisuals );
    hr = pageVisuals->Append( rectPath );
    // If not needed for anything else, release the rectangle path.
    rectPath->Release();
    
    // When done with the visual collection, release it.
    pageVisuals->Release();

    // When finished with the brushes, release the interface pointers.
    if (NULL != xpsFillBrush) xpsFillBrush->Release();
    if (NULL != xpsStrokeBrush) xpsStrokeBrush->Release();

    // When done with the geometry interface, release it.
    imageRectGeometry->Release();

    // When done with the path interface, release it.
    rectPath->Release();

```



## <a name="best-practices"></a>Práticas Recomendadas

Adicione uma descrição textual da forma especificada pela interface [**IXpsOMPath.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) Para o benefício de usuários com deficiência visual, use os métodos [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) e [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) para fornecer conteúdo textual para recursos de suporte de acessibilidade, como leitores de tela.

## <a name="additional-information"></a>Informações adicionais

O exemplo de código nesta página usa uma interface [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) como o pincel de preenchimento e o pincel de traço para o caminho. Além da interface **IXpsOMSolidColorBrush,** você pode usar uma interface [**IXpsOMGradientBrush,**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush) [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)ou [**IXpsOMVisualBrush.**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush)

O traço é a linha que pode ser desenhada em torno do perímetro da figura. O [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) dá suporte a muitos estilos de linha de traço diferentes. Para especificar o estilo de linha de traço, de definir as propriedades de traço com os seguintes métodos da interface [**IXpsOMPath:**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)

-   [**SetRogkeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) ou [**SetRogkeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) para definir o pincel de traço
-   [**GetStrkeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) para obter a coleção de traços que descreve os traços
-   [**SetRogkeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) como e [**SetRogkeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) para descrever a aparência de um traço tracejado
-   [**SetRogkeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) e [**SetRogkeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) para definir o estilo de terminação de linha
-   [**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) e [**SetStrokeMiterLimit para**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) descrever como os segmentos são unidos
-   [**SetRogkeThickness para**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) definir a espessura do traço

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

**Próximas etapas**
</dt> <dt>

[Navegar pelo OM XPS](navigate-the-xps-om.md)
</dt> <dt>

[Gravar texto em um OM XPS](write-text-to-an-xps-om.md)
</dt> <dt>

[Colocar imagens em um OM XPS](place-images-in-an-xps-om.md)
</dt> <dt>

[Gravar um OM XPS em um documento XPS](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[Imprimir um OM XPS](print-an-xps-om.md)
</dt> <dt>

**Usado nesta página**
</dt> <dt>

[**IOpcPartUri**](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[**IXpsOMGeometryFigureCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[**IXpsOMObjectFactory**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[**IXpsOMPage**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[**IXpsOMVisualCollection**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

**Para obter mais informações**
</dt> <dt>

[Inicializar um OM XPS](xps-object-model-initialization.md)
</dt> <dt>

[Referência da API de Documento XPS](xps-programming-reference.md)
</dt> <dt>

[Especificação de Papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
