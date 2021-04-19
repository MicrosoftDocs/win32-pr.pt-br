---
description: Esta página descreve como desenhar gráficos em um OM XPS.
ms.assetid: 2384b522-208a-48db-ae0d-f82fa0214d09
title: Desenhar gráficos em um OM XPS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fabbf8cfb821c80dfff43e2e7844331c8920f726
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105768355"
---
# <a name="draw-graphics-in-an-xps-om"></a><span data-ttu-id="dc6de-103">Desenhar gráficos em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="dc6de-103">Draw Graphics in an XPS OM</span></span>

<span data-ttu-id="dc6de-104">Esta página descreve como desenhar gráficos em um OM XPS.</span><span class="sxs-lookup"><span data-stu-id="dc6de-104">This page describes how to draw graphics in an XPS OM.</span></span>

<span data-ttu-id="dc6de-105">Para desenhar gráficos baseados em vetor em uma página, crie uma instância de uma interface [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) , popule-a com o conteúdo desejado e adicione-a à lista de objetos visuais da página ou da tela.</span><span class="sxs-lookup"><span data-stu-id="dc6de-105">To draw vector-based graphics in a page, instantiate an [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface, populate it with the desired content, and add it to the page's or canvas' list of visual objects.</span></span> <span data-ttu-id="dc6de-106">Uma interface **IXpsOMPath** contém essas propriedades de uma forma baseada em vetor como estrutura de tópicos, cor de preenchimento, estilo de linha e cor de linha.</span><span class="sxs-lookup"><span data-stu-id="dc6de-106">An **IXpsOMPath** interface contains such properties of a vector-based shape as the outline, fill color, line style, and line color.</span></span> <span data-ttu-id="dc6de-107">A forma do caminho é especificada por uma interface [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) , que contém uma coleção de interfaces [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) e, opcionalmente, uma interface [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) .</span><span class="sxs-lookup"><span data-stu-id="dc6de-107">The path's shape is specified by an [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface, which contains a collection of [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interfaces and, optionally, an [**IXpsOMMatrixTransform**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsommatrixtransform) interface.</span></span> <span data-ttu-id="dc6de-108">Você pode usar qualquer interface que herda da interface [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) para preencher o perímetro do caminho e o interior da forma que é descrita pelo caminho.</span><span class="sxs-lookup"><span data-stu-id="dc6de-108">You can use any interface that inherits from the [**IXpsOMBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsombrush) interface to fill the perimeter of the path and the interior of the shape that is described by the path.</span></span>

<span data-ttu-id="dc6de-109">Antes de usar os exemplos de código a seguir em seu programa, leia o aviso de isenção de responsabilidade em [tarefas comuns de programação de documentos XPS](common-xps-document-tasks.md).</span><span class="sxs-lookup"><span data-stu-id="dc6de-109">Before using the following code examples in your program, read the disclaimer in [Common XPS Document Programming Tasks](common-xps-document-tasks.md).</span></span>

## <a name="code-example"></a><span data-ttu-id="dc6de-110">Exemplo de código</span><span class="sxs-lookup"><span data-stu-id="dc6de-110">Code Example</span></span>

<span data-ttu-id="dc6de-111">O exemplo de código a seguir cria um caminho simples que descreve um retângulo que é preenchido com uma única cor.</span><span class="sxs-lookup"><span data-stu-id="dc6de-111">The following code example creates a simple path that describes a rectangle that is filled with a single color.</span></span>

### <a name="create-the-stroke-and-the-fill-brushes"></a><span data-ttu-id="dc6de-112">Criar o traço e os pincéis de preenchimento</span><span class="sxs-lookup"><span data-stu-id="dc6de-112">Create the stroke and the fill brushes</span></span>

<span data-ttu-id="dc6de-113">A primeira seção do exemplo de código cria o [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) que será usado para preencher o objeto de caminho.</span><span class="sxs-lookup"><span data-stu-id="dc6de-113">The first section of the code example creates the [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) that will be used to fill the path object.</span></span>


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



### <a name="define-the-shape"></a><span data-ttu-id="dc6de-114">Definir a forma</span><span class="sxs-lookup"><span data-stu-id="dc6de-114">Define the shape</span></span>

<span data-ttu-id="dc6de-115">A segunda seção do exemplo de código cria a interface [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) .</span><span class="sxs-lookup"><span data-stu-id="dc6de-115">The second section of the code example creates the [**IXpsOMGeometry**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry) interface.</span></span> <span data-ttu-id="dc6de-116">Em seguida, ele cria a interface [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) que especifica a forma do número e adiciona a figura à interface **IXpsOMGeometry** .</span><span class="sxs-lookup"><span data-stu-id="dc6de-116">It then creates the [**IXpsOMGeometryFigure**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure) interface that specifies the figure's shape, and adds the figure to the **IXpsOMGeometry** interface.</span></span> <span data-ttu-id="dc6de-117">O exemplo cria um retângulo especificado por *Rect*.</span><span class="sxs-lookup"><span data-stu-id="dc6de-117">The example creates a rectangle that is specified by *rect*.</span></span> <span data-ttu-id="dc6de-118">Os segmentos devem ser definidos para apenas três dos quatro lados do retângulo.</span><span class="sxs-lookup"><span data-stu-id="dc6de-118">Segments must be defined for only three of the four sides of the rectangle.</span></span> <span data-ttu-id="dc6de-119">O perímetro da forma, o retângulo, nesse caso, começa a partir do ponto inicial e se estende conforme definido pelos segmentos da figura Geometry.</span><span class="sxs-lookup"><span data-stu-id="dc6de-119">The perimeter of the shape, the rectangle in this case, starts from the start point and extends as defined by the segments of the geometry figure.</span></span> <span data-ttu-id="dc6de-120">Definir a propriedade **IsClosed** como **true** indica que o retângulo está fechado adicionando um segmento adicional que conecta o final do último segmento ao ponto de partida.</span><span class="sxs-lookup"><span data-stu-id="dc6de-120">Setting the **IsClosed** property to **TRUE** indicates that the rectangle is closed by adding one additional segment that connects the end of the last segment to the start point.</span></span>


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



### <a name="create-the-path-and-add-it-to-the-visual-collection"></a><span data-ttu-id="dc6de-121">Criar o caminho e adicioná-lo à coleção Visual</span><span class="sxs-lookup"><span data-stu-id="dc6de-121">Create the path and add it to the visual collection</span></span>

<span data-ttu-id="dc6de-122">A seção final deste exemplo de código cria e configura o objeto Path e, em seguida, adiciona-o à lista de objetos visuais da página.</span><span class="sxs-lookup"><span data-stu-id="dc6de-122">The final section of this code example creates and configures the path object, then adds it to the page's list of visual objects.</span></span>


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



## <a name="best-practices"></a><span data-ttu-id="dc6de-123">Práticas Recomendadas</span><span class="sxs-lookup"><span data-stu-id="dc6de-123">Best Practices</span></span>

<span data-ttu-id="dc6de-124">Adicione uma descrição textual da forma especificada pela interface [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) .</span><span class="sxs-lookup"><span data-stu-id="dc6de-124">Add a textual description of the shape that is specified by the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface.</span></span> <span data-ttu-id="dc6de-125">Para o benefício de usuários com deficiência visual, use os métodos [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) e [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) para fornecer conteúdo textual para recursos de suporte de acessibilidade, como leitores de tela.</span><span class="sxs-lookup"><span data-stu-id="dc6de-125">For the benefit of visually impaired users, use the [**SetAccessibilityShortDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilityshortdescription) and [**SetAccessibilityLongDescription**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setaccessibilitylongdescription) methods to provide textual content for accessibility support features, such as screen readers.</span></span>

## <a name="additional-information"></a><span data-ttu-id="dc6de-126">Informações adicionais</span><span class="sxs-lookup"><span data-stu-id="dc6de-126">Additional Information</span></span>

<span data-ttu-id="dc6de-127">O exemplo de código nesta página usa uma interface [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) como pincel de preenchimento e pincel de traço para o caminho.</span><span class="sxs-lookup"><span data-stu-id="dc6de-127">The code example on this page uses an [**IXpsOMSolidColorBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush) interface as the fill brush and stroke brush for the path.</span></span> <span data-ttu-id="dc6de-128">Além da interface **IXpsOMSolidColorBrush** , você pode usar uma interface [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush)ou [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) .</span><span class="sxs-lookup"><span data-stu-id="dc6de-128">In addition to the **IXpsOMSolidColorBrush** interface, you can use an [**IXpsOMGradientBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgradientbrush), [**IXpsOMImageBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomimagebrush), or [**IXpsOMVisualBrush**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualbrush) interface.</span></span>

<span data-ttu-id="dc6de-129">O traço é a linha que pode ser desenhada em torno do perímetro da figura.</span><span class="sxs-lookup"><span data-stu-id="dc6de-129">The stroke is the line that can be drawn around the perimeter of the figure.</span></span> <span data-ttu-id="dc6de-130">A [especificação de papel XML](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) dá suporte a vários estilos de linha de traço diferentes.</span><span class="sxs-lookup"><span data-stu-id="dc6de-130">The [XML Paper Specification](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf) supports many different stroke line styles.</span></span> <span data-ttu-id="dc6de-131">Para especificar o estilo da linha do traço, defina as propriedades do traço com os seguintes métodos da interface [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) :</span><span class="sxs-lookup"><span data-stu-id="dc6de-131">To specify the stroke line style, set the stroke properties with the following methods of the [**IXpsOMPath**](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath) interface:</span></span>

-   <span data-ttu-id="dc6de-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) ou [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) para definir o pincel de traço</span><span class="sxs-lookup"><span data-stu-id="dc6de-132">[**SetStrokeBrushLocal**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlocal) or [**SetStrokeBrushLookup**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokebrushlookup) to set the stroke brush</span></span>
-   <span data-ttu-id="dc6de-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) para obter a coleção de traço tracejado que descreve os traços</span><span class="sxs-lookup"><span data-stu-id="dc6de-133">[**GetStrokeDashes**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-getstrokedashes) to get the stroke dash collection that describes the strokes</span></span>
-   <span data-ttu-id="dc6de-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) e [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) para descrever a aparência de um traço tracejado</span><span class="sxs-lookup"><span data-stu-id="dc6de-134">[**SetStrokeDashCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashcap) to and [**SetStrokeDashOffset**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokedashoffset) to describe the appearance of a dashed stroke</span></span>
-   <span data-ttu-id="dc6de-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) e [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) para definir o estilo de terminação de linha</span><span class="sxs-lookup"><span data-stu-id="dc6de-135">[**SetStrokeEndLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokeendlinecap) and [**SetStrokeStartLineCap**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokestartlinecap) to define the line termination style</span></span>
-   <span data-ttu-id="dc6de-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) e [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) para descrever como os segmentos são Unidos</span><span class="sxs-lookup"><span data-stu-id="dc6de-136">[**SetStrokeLineJoin**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokelinejoin) and [**SetStrokeMiterLimit**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokemiterlimit) to describe how the segments are joined</span></span>
-   <span data-ttu-id="dc6de-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) para definir a espessura do traço</span><span class="sxs-lookup"><span data-stu-id="dc6de-137">[**SetStrokeThickness**](/windows/desktop/api/xpsobjectmodel/nf-xpsobjectmodel-ixpsompath-setstrokethickness) to set the stroke thickness</span></span>

## <a name="related-topics"></a><span data-ttu-id="dc6de-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="dc6de-138">Related topics</span></span>

<dl> <dt>

<span data-ttu-id="dc6de-139">**Próximas etapas**</span><span class="sxs-lookup"><span data-stu-id="dc6de-139">**Next Steps**</span></span>
</dt> <dt>

[<span data-ttu-id="dc6de-140">Navegar no OM XPS</span><span class="sxs-lookup"><span data-stu-id="dc6de-140">Navigate the XPS OM</span></span>](navigate-the-xps-om.md)
</dt> <dt>

[<span data-ttu-id="dc6de-141">Gravar texto em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="dc6de-141">Write Text to an XPS OM</span></span>](write-text-to-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="dc6de-142">Coloque as imagens em um OM XPS</span><span class="sxs-lookup"><span data-stu-id="dc6de-142">Place Images in an XPS OM</span></span>](place-images-in-an-xps-om.md)
</dt> <dt>

[<span data-ttu-id="dc6de-143">Gravar um OM XPS em um documento XPS</span><span class="sxs-lookup"><span data-stu-id="dc6de-143">Write an XPS OM to an XPS Document</span></span>](write-an-xps-om-to-an-xps-document.md)
</dt> <dt>

[<span data-ttu-id="dc6de-144">Imprimir um OM XPS</span><span class="sxs-lookup"><span data-stu-id="dc6de-144">Print an XPS OM</span></span>](print-an-xps-om.md)
</dt> <dt>

<span data-ttu-id="dc6de-145">**Usado nesta página**</span><span class="sxs-lookup"><span data-stu-id="dc6de-145">**Used in This Page**</span></span>
</dt> <dt>

[<span data-ttu-id="dc6de-146">**IOpcPartUri**</span><span class="sxs-lookup"><span data-stu-id="dc6de-146">**IOpcPartUri**</span></span>](/previous-versions/windows/desktop/api/msopc/nn-msopc-iopcparturi)
</dt> <dt>

[<span data-ttu-id="dc6de-147">**IXpsOMGeometry**</span><span class="sxs-lookup"><span data-stu-id="dc6de-147">**IXpsOMGeometry**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometry)
</dt> <dt>

[<span data-ttu-id="dc6de-148">**IXpsOMGeometryFigure**</span><span class="sxs-lookup"><span data-stu-id="dc6de-148">**IXpsOMGeometryFigure**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigure)
</dt> <dt>

[<span data-ttu-id="dc6de-149">**IXpsOMGeometryFigureCollection**</span><span class="sxs-lookup"><span data-stu-id="dc6de-149">**IXpsOMGeometryFigureCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomgeometryfigurecollection)
</dt> <dt>

[<span data-ttu-id="dc6de-150">**IXpsOMObjectFactory**</span><span class="sxs-lookup"><span data-stu-id="dc6de-150">**IXpsOMObjectFactory**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomobjectfactory)
</dt> <dt>

[<span data-ttu-id="dc6de-151">**IXpsOMPage**</span><span class="sxs-lookup"><span data-stu-id="dc6de-151">**IXpsOMPage**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompage)
</dt> <dt>

[<span data-ttu-id="dc6de-152">**IXpsOMPath**</span><span class="sxs-lookup"><span data-stu-id="dc6de-152">**IXpsOMPath**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsompath)
</dt> <dt>

[<span data-ttu-id="dc6de-153">**IXpsOMSolidColorBrush**</span><span class="sxs-lookup"><span data-stu-id="dc6de-153">**IXpsOMSolidColorBrush**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomsolidcolorbrush)
</dt> <dt>

[<span data-ttu-id="dc6de-154">**IXpsOMVisualCollection**</span><span class="sxs-lookup"><span data-stu-id="dc6de-154">**IXpsOMVisualCollection**</span></span>](/windows/desktop/api/xpsobjectmodel/nn-xpsobjectmodel-ixpsomvisualcollection)
</dt> <dt>

<span data-ttu-id="dc6de-155">**Para obter mais informações**</span><span class="sxs-lookup"><span data-stu-id="dc6de-155">**For More Information**</span></span>
</dt> <dt>

[<span data-ttu-id="dc6de-156">Inicializar um OM XPS</span><span class="sxs-lookup"><span data-stu-id="dc6de-156">Initialize an XPS OM</span></span>](xps-object-model-initialization.md)
</dt> <dt>

[<span data-ttu-id="dc6de-157">Referência da API do documento XPS</span><span class="sxs-lookup"><span data-stu-id="dc6de-157">XPS Document API Reference</span></span>](xps-programming-reference.md)
</dt> <dt>

[<span data-ttu-id="dc6de-158">Especificação de Papel XML</span><span class="sxs-lookup"><span data-stu-id="dc6de-158">XML Paper Specification</span></span>](https://www.ecma-international.org/activities/XML%20Paper%20Specification/XPS%20Standard%20WD%201.6.pdf)
</dt> </dl>

 

 
