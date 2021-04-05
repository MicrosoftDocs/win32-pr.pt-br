---
description: Este exemplo é baseado no exemplo de coleção de tinta. Ele mostra como usar o objeto divisória para analisar a entrada à tinta.
ms.assetid: 3350b643-11b3-4474-8dd0-bc3eb1b7121e
title: Exemplo de divisória de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a272d6a5530938e6fecfeefc9f46ffdd0835d045
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104460974"
---
# <a name="ink-divider-sample"></a><span data-ttu-id="08de4-104">Exemplo de divisória de tinta</span><span class="sxs-lookup"><span data-stu-id="08de4-104">Ink Divider Sample</span></span>

<span data-ttu-id="08de4-105">Este exemplo é baseado no [exemplo de coleção de tinta](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="08de4-105">This sample is based on the [Ink Collection Sample](ink-collection-sample.md).</span></span> <span data-ttu-id="08de4-106">Ele mostra como usar o objeto [divisória](/previous-versions/ms839398(v=msdn.10)) para analisar a entrada à tinta.</span><span class="sxs-lookup"><span data-stu-id="08de4-106">It shows how to use the [Divider](/previous-versions/ms839398(v=msdn.10)) object to analyze ink input.</span></span>

<span data-ttu-id="08de4-107">Para obter informações conceituais detalhadas sobre o [divisor](/previous-versions/ms839398(v=msdn.10)), consulte [o objeto divisória](the-divider-object.md).</span><span class="sxs-lookup"><span data-stu-id="08de4-107">For detailed conceptual information about [Divider](/previous-versions/ms839398(v=msdn.10)), see [The Divider Object](the-divider-object.md).</span></span>

<span data-ttu-id="08de4-108">Quando o formulário é atualizado, o exemplo desenha um retângulo delimitador em volta de cada unidade analisada, dividida em palavras, linhas, parágrafos e desenhos.</span><span class="sxs-lookup"><span data-stu-id="08de4-108">When the form is updated, the sample draws a bounding rectangle around each analyzed unit, broken into words, lines, paragraphs, and drawings.</span></span> <span data-ttu-id="08de4-109">Além de usar cores diferentes, esses retângulos são ampliados por diferentes quantidades para garantir que nenhum dos retângulos seja obscurecido por outros.</span><span class="sxs-lookup"><span data-stu-id="08de4-109">Besides using different colors, these rectangles are enlarged by different amounts to ensure that none of the rectangles is obscured by others.</span></span> <span data-ttu-id="08de4-110">A tabela a seguir especifica a cor e a ampliação para cada unidade analisada.</span><span class="sxs-lookup"><span data-stu-id="08de4-110">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="08de4-111">Unidade analisada</span><span class="sxs-lookup"><span data-stu-id="08de4-111">analyzed Unit</span></span>        | <span data-ttu-id="08de4-112">Cor</span><span class="sxs-lookup"><span data-stu-id="08de4-112">Color</span></span>              | <span data-ttu-id="08de4-113">Aumento de pixels</span><span class="sxs-lookup"><span data-stu-id="08de4-113">Pixel Enlargement</span></span> |
|----------------------|--------------------|-------------------|
| <span data-ttu-id="08de4-114">Word</span><span class="sxs-lookup"><span data-stu-id="08de4-114">Word</span></span><br/>      | <span data-ttu-id="08de4-115">Verde</span><span class="sxs-lookup"><span data-stu-id="08de4-115">Green</span></span><br/>   | <span data-ttu-id="08de4-116">1</span><span class="sxs-lookup"><span data-stu-id="08de4-116">1</span></span><br/>      |
| <span data-ttu-id="08de4-117">Linha</span><span class="sxs-lookup"><span data-stu-id="08de4-117">Line</span></span><br/>      | <span data-ttu-id="08de4-118">Magenta</span><span class="sxs-lookup"><span data-stu-id="08de4-118">Magenta</span></span><br/> | <span data-ttu-id="08de4-119">3</span><span class="sxs-lookup"><span data-stu-id="08de4-119">3</span></span><br/>      |
| <span data-ttu-id="08de4-120">Paragraph</span><span class="sxs-lookup"><span data-stu-id="08de4-120">Paragraph</span></span><br/> | <span data-ttu-id="08de4-121">Azul</span><span class="sxs-lookup"><span data-stu-id="08de4-121">Blue</span></span><br/>    | <span data-ttu-id="08de4-122">5</span><span class="sxs-lookup"><span data-stu-id="08de4-122">5</span></span><br/>      |
| <span data-ttu-id="08de4-123">Desenho</span><span class="sxs-lookup"><span data-stu-id="08de4-123">Drawing</span></span><br/>   | <span data-ttu-id="08de4-124">Vermelho</span><span class="sxs-lookup"><span data-stu-id="08de4-124">Red</span></span><br/>     | <span data-ttu-id="08de4-125">1</span><span class="sxs-lookup"><span data-stu-id="08de4-125">1</span></span><br/>      |



 

## <a name="setting-up-the-form"></a><span data-ttu-id="08de4-126">Configurando o formulário</span><span class="sxs-lookup"><span data-stu-id="08de4-126">Setting Up the Form</span></span>

<span data-ttu-id="08de4-127">Quando o formulário é carregado, um objeto [divisor](/previous-versions/ms839398(v=msdn.10)) é criado.</span><span class="sxs-lookup"><span data-stu-id="08de4-127">When the form loads, a [Divider](/previous-versions/ms839398(v=msdn.10)) object is created.</span></span> <span data-ttu-id="08de4-128">Um objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) é criado e associado a um painel no formulário.</span><span class="sxs-lookup"><span data-stu-id="08de4-128">An [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object is created and associated with a panel on the form.</span></span> <span data-ttu-id="08de4-129">Em seguida, os manipuladores de eventos são anexados ao objeto InkOverlay para controlar quando os traços são adicionados e excluídos.</span><span class="sxs-lookup"><span data-stu-id="08de4-129">Then event handlers are attached to the InkOverlay object to track when strokes are added and deleted.</span></span> <span data-ttu-id="08de4-130">Em seguida, se os reconhecedores estiverem disponíveis, um objeto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) para o reconhecedor padrão será atribuído ao divisor.</span><span class="sxs-lookup"><span data-stu-id="08de4-130">Then if recognizers are available, a [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) object for the default recognizer is assigned to the Divider.</span></span> <span data-ttu-id="08de4-131">Em seguida, a propriedade [LineHeight](/previous-versions/ms839409(v=msdn.10)) do objeto divisória é definida e a coleção [Strokes](/previous-versions/ms827799(v=msdn.10)) do objeto InkOverlay é atribuída ao divisor.</span><span class="sxs-lookup"><span data-stu-id="08de4-131">Then the Divider object's [LineHeight](/previous-versions/ms839409(v=msdn.10)) property is set and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection from the InkOverlay object is assigned to the Divider.</span></span> <span data-ttu-id="08de4-132">Por fim, o objeto InkOverlay está habilitado.</span><span class="sxs-lookup"><span data-stu-id="08de4-132">Finally, the InkOverlay object is enabled.</span></span>


```C++
// Create the ink overlay and associate it with the form
myInkOverlay = new Microsoft.Ink.InkOverlay(DrawArea.Handle);

// Set the erasing mode to stroke erase.
myInkOverlay.EraserMode = InkOverlayEraserMode.StrokeErase;

// Hook event handler for the Stroke event to myInkOverlay_Stroke.
// This is necessary since the application needs to pass the strokes 
// to the ink divider.
myInkOverlay.Stroke += new InkCollectorStrokeEventHandler(myInkOverlay_Stroke); 

// Hook the event handler for StrokeDeleting event to myInkOverlay_StrokeDeleting.
// This is necessary as the application needs to remove the strokes from 
// ink divider object as well.
myInkOverlay.StrokesDeleting += new InkOverlayStrokesDeletingEventHandler(myInkOverlay_StrokeDeleting);

// Hook the event handler for StrokeDeleted event to myInkOverlay_StrokeDeleted.
// This is necessary to update the layout analysis result when automatic layout analysis
// option is selected.
myInkOverlay.StrokesDeleted += new InkOverlayStrokesDeletedEventHandler(myInkOverlay_StrokeDeleted);

// Create the ink divider object
myInkDivider = new Divider();

// Add a default recognizer context to the divider object
// without adding the recognizer context, the divider would
// not use a recognizer to do its word segmentation and would
// have less accurate results.
// Adding the recognizer context slows down the call to 
// myInkDivider.Divide though.
// It is possible that there is no recognizer installed on the
// machine for this language. In that case the divider does
// not use a recognizer to improve its accuracy.
// Get the default recognizer if any
try
{
    Recognizers recognizers = new Recognizers();
     myInkDivider.RecognizerContext = recognizers.GetDefaultRecognizer().CreateRecognizerContext();
}
catch (InvalidOperationException)
{
     //We are in the case where no default recognizers can be found
}

    // The LineHeight property helps the InkDivider distinguish between 
    // drawing and handwriting. The value should be the expected height 
    // of the user's handwriting in ink space units (0.01mm).
    // Here we set the LineHeight to 840, which is about 1/3 of an inch.
    myInkDivider.LineHeight = 840;

// Assign ink overlay's strokes collection to the ink divider
// This strokes collection is updated in the event handler
myInkDivider.Strokes = myInkOverlay.Ink.Strokes;

// Enable ink collection
myInkOverlay.Enabled = true;
```



<span data-ttu-id="08de4-133">A coleção [Strokes](/previous-versions/ms839422(v=msdn.10)) do objeto [divisória](/previous-versions/ms839398(v=msdn.10)) deve ser mantida em sincronia com a coleção [Strokes](/previous-versions/ms827799(v=msdn.10)) do objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) (acessada por meio da propriedade [Ink](/previous-versions/ms833110(v=msdn.10)) do objeto InkOverlay).</span><span class="sxs-lookup"><span data-stu-id="08de4-133">The [Divider](/previous-versions/ms839398(v=msdn.10)) object's [Strokes](/previous-versions/ms839422(v=msdn.10)) collection must be kept in sync with the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Strokes](/previous-versions/ms827799(v=msdn.10)) collection (accessed through the InkOverlay object's [Ink](/previous-versions/ms833110(v=msdn.10)) property).</span></span> <span data-ttu-id="08de4-134">Para garantir que isso aconteça, o manipulador de eventos [Stroke](/previous-versions/ms835344(v=msdn.10)) do objeto InkOverlay é escrito da seguinte maneira.</span><span class="sxs-lookup"><span data-stu-id="08de4-134">To ensure that this happens, the [Stroke](/previous-versions/ms835344(v=msdn.10)) event handler for the InkOverlay object is written as follows.</span></span> <span data-ttu-id="08de4-135">Observe que o manipulador de eventos primeiro testa para ver se o [EditingMode](/previous-versions/ms833105(v=msdn.10)) está definido como **Ink** para filtrar os traços de borracha.</span><span class="sxs-lookup"><span data-stu-id="08de4-135">Note that the event handler first tests to see if the [EditingMode](/previous-versions/ms833105(v=msdn.10)) is set to **Ink** to filter out eraser strokes.</span></span> <span data-ttu-id="08de4-136">Se o usuário tiver solicitado a análise automática de layout, o aplicativo chamará o método DivideInk do formulário e atualizará a área de desenho.</span><span class="sxs-lookup"><span data-stu-id="08de4-136">If the user has requested automatic layout analysis, then the application calls the form's DivideInk method and refreshes the drawing area.</span></span>


```C++
private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e )
{
    // Filter out the eraser stroke.
    if(InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
    {
        // Add the new stroke to the ink divider's strokes collection
        myInkDivider.Strokes.Add(e.Stroke);
        
        if(miAutomaticLayoutAnalysis.Checked)
        {
            // Call DivideInk
            DivideInk();

            // Repaint the screen to reflect the change
            DrawArea.Refresh();
        }
    }
}
```



## <a name="dividing-the-ink"></a><span data-ttu-id="08de4-137">Dividindo a tinta</span><span class="sxs-lookup"><span data-stu-id="08de4-137">Dividing the Ink</span></span>

<span data-ttu-id="08de4-138">Quando o usuário clica em dividir no menu arquivo, o método de [divisão](/previous-versions/ms839461(v=msdn.10)) é chamado no objeto [divisória](/previous-versions/ms839398(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="08de4-138">When the user clicks Divide on the File menu, the [Divide](/previous-versions/ms839461(v=msdn.10)) method is called on the [Divider](/previous-versions/ms839398(v=msdn.10)) object.</span></span> <span data-ttu-id="08de4-139">O reconhecedor padrão é usado, se disponível.</span><span class="sxs-lookup"><span data-stu-id="08de4-139">The default recognizer is used, if available.</span></span>


```C++
DivisionResult divResult = myInkDivider.Divide();
```



<span data-ttu-id="08de4-140">O objeto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) resultante, referenciado pela variável `divResult` , é passado para uma função de utilitário, `getUnitBBBoxes()` .</span><span class="sxs-lookup"><span data-stu-id="08de4-140">The resulting [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object, referenced by the variable `divResult`, is passed to a utility function, `getUnitBBBoxes()`.</span></span> <span data-ttu-id="08de4-141">A função utilitário retorna uma matriz de retângulos para qualquer tipo de divisão solicitado: segmentos, linhas, parágrafos ou desenhos.</span><span class="sxs-lookup"><span data-stu-id="08de4-141">The utility function returns an array of rectangles for whatever division type is requested: segments, lines, paragraphs, or drawings.</span></span>


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



<span data-ttu-id="08de4-142">Por fim, o painel formulário é forçado a redesenhar para que os retângulos delimitadores sejam exibidos.</span><span class="sxs-lookup"><span data-stu-id="08de4-142">Finally, the form panel is forced to redraw so that the bounding rectangles appear.</span></span>


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a><span data-ttu-id="08de4-143">Resultados da análise de tinta</span><span class="sxs-lookup"><span data-stu-id="08de4-143">Ink Analysis Results</span></span>

<span data-ttu-id="08de4-144">Na função do utilitário, o objeto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) é consultado em busca de seus resultados usando o método [ResultByType](/previous-versions/ms839388(v=msdn.10)) , com base no tipo de divisão solicitado pelo chamador.</span><span class="sxs-lookup"><span data-stu-id="08de4-144">In the utility function, the [DivisionResult](/previous-versions/ms839371(v=msdn.10)) object is queried for its results by using the [ResultByType](/previous-versions/ms839388(v=msdn.10)) method, based on the division type requested by the caller.</span></span> <span data-ttu-id="08de4-145">O método ResultByType retorna uma coleção [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="08de4-145">The ResultByType method returns a [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) collection.</span></span> <span data-ttu-id="08de4-146">Cada [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) na coleção representa um desenho, um único segmento de reconhecimento de manuscrito, uma linha de manuscrito ou um bloco de manuscrito, dependendo do que foi especificado quando a função do utilitário foi chamada.</span><span class="sxs-lookup"><span data-stu-id="08de4-146">Each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) in the collection represents a drawing, a single recognition segment of handwriting, a line of handwriting, or a block of handwriting, depending upon what was specified when the utility function was called.</span></span>


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



<span data-ttu-id="08de4-147">Se houver pelo menos um [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), uma matriz de retângulos será criada contendo um retângulo delimitador por unidade.</span><span class="sxs-lookup"><span data-stu-id="08de4-147">If there is at least one [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), an array of rectangles is created containing one bounding rectangle per unit.</span></span> <span data-ttu-id="08de4-148">(Os retângulos são inalterados por valores diferentes para cada tipo de unidade, mantidos na variável de inflação, para evitar sobreposição.)</span><span class="sxs-lookup"><span data-stu-id="08de4-148">(The rectangles are inflated by differing amounts for each type of unit, held in the inflate variable, to prevent overlapping.)</span></span>


```C++
// If there is at least one unit, we construct the rectangles
if((null != units) && (0 < units.Count))
{
    // We need to convert rectangles from ink units to
    // pixel units. For that, we need Graphics object
    // to pass to InkRenderer.InkSpaceToPixel method
    using (Graphics g = DrawArea.CreateGraphics())
    {

    // InkSpace to Pixel Space conversion setup done here. 
    // Not shown for brevity.

        // Iterate through the collection of division units to obtain the bounding boxes
        foreach(DivisionUnit unit in units)
        {
            // Get the bounding box of the strokes of the division unit
            divRects[i] = unit.Strokes.GetBoundingBox();

            // Div unit rect Ink space to Pixel space conversion done here. 
            // Not shown for brevity.

            // Inflate the rectangle by inflate pixels in both directions
            divRects[i].Inflate(inflate, inflate);

            // Increment the index
            ++i;
        }

    } // Relinquish the Graphics object
}
```



## <a name="redrawing-the-form"></a><span data-ttu-id="08de4-149">Redesenhando o formulário</span><span class="sxs-lookup"><span data-stu-id="08de4-149">Redrawing the Form</span></span>

<span data-ttu-id="08de4-150">Quando o redesenho é forçado acima, o código a seguir é executado para pintar as caixas delimitadoras para cada [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) no formulário em volta da tinta.</span><span class="sxs-lookup"><span data-stu-id="08de4-150">When the redraw is forced above, the following code executes to paint the bounding boxes for each [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) on the form around the ink.</span></span>


```C++
private void DrawArea_Paint(object sender, System.Windows.Forms.PaintEventArgs e)
        {
            // Create the Pen used to draw bounding boxes.
            // First set of bounding boxes drawn here are 
            // the bounding boxes of paragraphs.
            // These boxes are drawn with Blue pen.
            Pen penBox = new Pen(Color.Blue, 2);

            // First, draw the bounding boxes for Paragraphs
            if(null != myParagraphBoundingBoxes)
            {
                // Draw bounding boxes for Paragraphs
                e.Graphics.DrawRectangles(penBox, myParagraphBoundingBoxes);
            }

            // Next, draw the bounding boxes for Lines
            if(null != myLineBoundingBoxes)
            {
                // Color is Magenta pen
                penBox.Color = Color.Magenta;
                // Draw the bounding boxes for Lines
                e.Graphics.DrawRectangles(penBox, myLineBoundingBoxes);
            }
            
            // Then, draw the bounding boxes for Words
            if(null != myWordBoundingBoxes)
            {
                // Color is Green
                penBox.Color = Color.Green;
                // Draw bounding boxes for Words
                e.Graphics.DrawRectangles(penBox, myWordBoundingBoxes);
            }
            
            // Finally, draw the boxes for Drawings
            if(null != myDrawingBoundingBoxes)
            {
                // Color is Red pen
                penBox.Color = Color.Red;
                // Draw bounding boxes for Drawings
                e.Graphics.DrawRectangles(penBox, myDrawingBoundingBoxes);
            }
        }
```



## <a name="closing-the-form"></a><span data-ttu-id="08de4-151">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="08de4-151">Closing the Form</span></span>

<span data-ttu-id="08de4-152">O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta os objetos [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [divisor](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) e a coleção [Strokes](/previous-versions/ms827799(v=msdn.10)) usada no exemplo.</span><span class="sxs-lookup"><span data-stu-id="08de4-152">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [Divider](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) objects and the [Strokes](/previous-versions/ms827799(v=msdn.10)) collection used in the sample.</span></span>

 

