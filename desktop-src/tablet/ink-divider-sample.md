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
# <a name="ink-divider-sample"></a>Exemplo de divisória de tinta

Este exemplo é baseado no [exemplo de coleção de tinta](ink-collection-sample.md). Ele mostra como usar o objeto [divisória](/previous-versions/ms839398(v=msdn.10)) para analisar a entrada à tinta.

Para obter informações conceituais detalhadas sobre o [divisor](/previous-versions/ms839398(v=msdn.10)), consulte [o objeto divisória](the-divider-object.md).

Quando o formulário é atualizado, o exemplo desenha um retângulo delimitador em volta de cada unidade analisada, dividida em palavras, linhas, parágrafos e desenhos. Além de usar cores diferentes, esses retângulos são ampliados por diferentes quantidades para garantir que nenhum dos retângulos seja obscurecido por outros. A tabela a seguir especifica a cor e a ampliação para cada unidade analisada.



| Unidade analisada        | Cor              | Aumento de pixels |
|----------------------|--------------------|-------------------|
| Word<br/>      | Verde<br/>   | 1<br/>      |
| Linha<br/>      | Magenta<br/> | 3<br/>      |
| Paragraph<br/> | Azul<br/>    | 5<br/>      |
| Desenho<br/>   | Vermelho<br/>     | 1<br/>      |



 

## <a name="setting-up-the-form"></a>Configurando o formulário

Quando o formulário é carregado, um objeto [divisor](/previous-versions/ms839398(v=msdn.10)) é criado. Um objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) é criado e associado a um painel no formulário. Em seguida, os manipuladores de eventos são anexados ao objeto InkOverlay para controlar quando os traços são adicionados e excluídos. Em seguida, se os reconhecedores estiverem disponíveis, um objeto [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) para o reconhecedor padrão será atribuído ao divisor. Em seguida, a propriedade [LineHeight](/previous-versions/ms839409(v=msdn.10)) do objeto divisória é definida e a coleção [Strokes](/previous-versions/ms827799(v=msdn.10)) do objeto InkOverlay é atribuída ao divisor. Por fim, o objeto InkOverlay está habilitado.


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



A coleção [Strokes](/previous-versions/ms839422(v=msdn.10)) do objeto [divisória](/previous-versions/ms839398(v=msdn.10)) deve ser mantida em sincronia com a coleção [Strokes](/previous-versions/ms827799(v=msdn.10)) do objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) (acessada por meio da propriedade [Ink](/previous-versions/ms833110(v=msdn.10)) do objeto InkOverlay). Para garantir que isso aconteça, o manipulador de eventos [Stroke](/previous-versions/ms835344(v=msdn.10)) do objeto InkOverlay é escrito da seguinte maneira. Observe que o manipulador de eventos primeiro testa para ver se o [EditingMode](/previous-versions/ms833105(v=msdn.10)) está definido como **Ink** para filtrar os traços de borracha. Se o usuário tiver solicitado a análise automática de layout, o aplicativo chamará o método DivideInk do formulário e atualizará a área de desenho.


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



## <a name="dividing-the-ink"></a>Dividindo a tinta

Quando o usuário clica em dividir no menu arquivo, o método de [divisão](/previous-versions/ms839461(v=msdn.10)) é chamado no objeto [divisória](/previous-versions/ms839398(v=msdn.10)) . O reconhecedor padrão é usado, se disponível.


```C++
DivisionResult divResult = myInkDivider.Divide();
```



O objeto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) resultante, referenciado pela variável `divResult` , é passado para uma função de utilitário, `getUnitBBBoxes()` . A função utilitário retorna uma matriz de retângulos para qualquer tipo de divisão solicitado: segmentos, linhas, parágrafos ou desenhos.


```C++
myWordBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Segment, 1);
myLineBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Line, 3);
myParagraphBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Paragraph, 5);
myDrawingBoundingBoxes = getUnitBBoxes(divResult, InkDivisionType.Drawing, 1);
```



Por fim, o painel formulário é forçado a redesenhar para que os retângulos delimitadores sejam exibidos.


```C++
DrawArea.Refresh();
```



## <a name="ink-analysis-results"></a>Resultados da análise de tinta

Na função do utilitário, o objeto [DivisionResult](/previous-versions/ms839371(v=msdn.10)) é consultado em busca de seus resultados usando o método [ResultByType](/previous-versions/ms839388(v=msdn.10)) , com base no tipo de divisão solicitado pelo chamador. O método ResultByType retorna uma coleção [DivisionUnits](/previous-versions/ms837954(v=msdn.10)) . Cada [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) na coleção representa um desenho, um único segmento de reconhecimento de manuscrito, uma linha de manuscrito ou um bloco de manuscrito, dependendo do que foi especificado quando a função do utilitário foi chamada.


```C++
DivisionUnits units = divResult.ResultByType(divType);
```



Se houver pelo menos um [DivisionUnit](/previous-versions/ms837976(v=msdn.10)), uma matriz de retângulos será criada contendo um retângulo delimitador por unidade. (Os retângulos são inalterados por valores diferentes para cada tipo de unidade, mantidos na variável de inflação, para evitar sobreposição.)


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



## <a name="redrawing-the-form"></a>Redesenhando o formulário

Quando o redesenho é forçado acima, o código a seguir é executado para pintar as caixas delimitadoras para cada [DivisionUnit](/previous-versions/ms837976(v=msdn.10)) no formulário em volta da tinta.


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



## <a name="closing-the-form"></a>Fechando o formulário

O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta os objetos [InkOverlay](/previous-versions/ms833057(v=msdn.10)), [divisor](/previous-versions/ms839398(v=msdn.10)), [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) e a coleção [Strokes](/previous-versions/ms827799(v=msdn.10)) usada no exemplo.

 

