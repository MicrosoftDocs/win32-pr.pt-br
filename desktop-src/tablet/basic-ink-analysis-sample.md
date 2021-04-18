---
description: O exemplo de análise de tinta básica mostra como a classe InkAnalyzer divide a tinta em vários segmentos de desenho e de palavras. Este exemplo é uma versão atualizada do exemplo de divisor de tinta.
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: Exemplo de análise de tinta básica
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e94ac73ca9049169c6e406059665a66e8eaa6f3b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105780728"
---
# <a name="basic-ink-analysis-sample"></a><span data-ttu-id="7ed63-103">Exemplo de análise de tinta básica</span><span class="sxs-lookup"><span data-stu-id="7ed63-103">Basic Ink Analysis Sample</span></span>

<span data-ttu-id="7ed63-104">O exemplo de análise de tinta básica mostra como a classe [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) divide a tinta em vários segmentos de desenho e de palavras.</span><span class="sxs-lookup"><span data-stu-id="7ed63-104">The Basic Ink Analysis sample shows how the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) class divides ink into various word and drawing segments.</span></span>

<span data-ttu-id="7ed63-105">Este exemplo é uma versão atualizada do [exemplo de divisor de tinta](ink-divider-sample.md).</span><span class="sxs-lookup"><span data-stu-id="7ed63-105">This sample is an updated version of the [Ink Divider Sample](ink-divider-sample.md).</span></span> <span data-ttu-id="7ed63-106">Enquanto o exemplo de divisória de tinta usa a classe [divisória](/previous-versions/ms839398(v=msdn.10)) , este exemplo usa a API InkAnalysis mais recente e preferencial.</span><span class="sxs-lookup"><span data-stu-id="7ed63-106">Whereas the Ink Divider Sample uses the [Divider](/previous-versions/ms839398(v=msdn.10)) class, this sample uses the newer and preferred InkAnalysis API.</span></span> <span data-ttu-id="7ed63-107">A API InkAnalysis combina o [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) e o divisor em uma API e expande a funcionalidade de ambos.</span><span class="sxs-lookup"><span data-stu-id="7ed63-107">The InkAnalysis API combines the [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) and Divider into one API and expands on the functionality of both.</span></span>

<span data-ttu-id="7ed63-108">Quando você atualiza o formulário, o exemplo desenha um retângulo em volta de cada unidade analisada: palavras, linhas, parágrafos, regiões de escrita, desenhos e marcadores.</span><span class="sxs-lookup"><span data-stu-id="7ed63-108">When you update the form, the sample draws a rectangle around each analyzed unit: words, lines, paragraphs, writing regions, drawings and bullets.</span></span> <span data-ttu-id="7ed63-109">O formulário usa cores diferentes para as diferentes unidades.</span><span class="sxs-lookup"><span data-stu-id="7ed63-109">The form uses different colors for the different units.</span></span> <span data-ttu-id="7ed63-110">Os retângulos também são ampliados por valores diferentes para garantir que nenhum retângulo seja obscurecido por outros.</span><span class="sxs-lookup"><span data-stu-id="7ed63-110">The rectangles are also enlarged by different amounts to ensure that no one rectangle is obscured by any others.</span></span>

<span data-ttu-id="7ed63-111">A tabela a seguir especifica a cor e a ampliação para cada unidade analisada.</span><span class="sxs-lookup"><span data-stu-id="7ed63-111">The following table specifies the color and enlargement for each analyzed unit.</span></span>



| <span data-ttu-id="7ed63-112">Unidade analisada</span><span class="sxs-lookup"><span data-stu-id="7ed63-112">Analyzed unit</span></span>             | <span data-ttu-id="7ed63-113">Cor do retângulo</span><span class="sxs-lookup"><span data-stu-id="7ed63-113">Color of rectangle</span></span> | <span data-ttu-id="7ed63-114">Ampliação do retângulo (pixels)</span><span class="sxs-lookup"><span data-stu-id="7ed63-114">Rectangle enlargement (pixels)</span></span> |
|---------------------------|--------------------|--------------------------------|
| <span data-ttu-id="7ed63-115">Word</span><span class="sxs-lookup"><span data-stu-id="7ed63-115">Word</span></span><br/>           | <span data-ttu-id="7ed63-116">Verde</span><span class="sxs-lookup"><span data-stu-id="7ed63-116">Green</span></span><br/>   | <span data-ttu-id="7ed63-117">1</span><span class="sxs-lookup"><span data-stu-id="7ed63-117">1</span></span><br/>                   |
| <span data-ttu-id="7ed63-118">Linha</span><span class="sxs-lookup"><span data-stu-id="7ed63-118">Line</span></span><br/>           | <span data-ttu-id="7ed63-119">Magenta</span><span class="sxs-lookup"><span data-stu-id="7ed63-119">Magenta</span></span><br/> | <span data-ttu-id="7ed63-120">3</span><span class="sxs-lookup"><span data-stu-id="7ed63-120">3</span></span><br/>                   |
| <span data-ttu-id="7ed63-121">Paragraph</span><span class="sxs-lookup"><span data-stu-id="7ed63-121">Paragraph</span></span><br/>      | <span data-ttu-id="7ed63-122">Azul</span><span class="sxs-lookup"><span data-stu-id="7ed63-122">Blue</span></span><br/>    | <span data-ttu-id="7ed63-123">5</span><span class="sxs-lookup"><span data-stu-id="7ed63-123">5</span></span><br/>                   |
| <span data-ttu-id="7ed63-124">Região de escrita</span><span class="sxs-lookup"><span data-stu-id="7ed63-124">Writing region</span></span><br/> | <span data-ttu-id="7ed63-125">Amarelo</span><span class="sxs-lookup"><span data-stu-id="7ed63-125">Yellow</span></span><br/>  | <span data-ttu-id="7ed63-126">7</span><span class="sxs-lookup"><span data-stu-id="7ed63-126">7</span></span><br/>                   |
| <span data-ttu-id="7ed63-127">Desenho</span><span class="sxs-lookup"><span data-stu-id="7ed63-127">Drawing</span></span><br/>        | <span data-ttu-id="7ed63-128">Vermelho</span><span class="sxs-lookup"><span data-stu-id="7ed63-128">Red</span></span><br/>     | <span data-ttu-id="7ed63-129">1</span><span class="sxs-lookup"><span data-stu-id="7ed63-129">1</span></span><br/>                   |
| <span data-ttu-id="7ed63-130">Listas</span><span class="sxs-lookup"><span data-stu-id="7ed63-130">Bullet</span></span><br/>         | <span data-ttu-id="7ed63-131">Laranja</span><span class="sxs-lookup"><span data-stu-id="7ed63-131">Orange</span></span><br/>  | <span data-ttu-id="7ed63-132">1</span><span class="sxs-lookup"><span data-stu-id="7ed63-132">1</span></span><br/>                   |



 

<span data-ttu-id="7ed63-133">Você pode apagar os traços no formulário.</span><span class="sxs-lookup"><span data-stu-id="7ed63-133">You can erase strokes in the form.</span></span> <span data-ttu-id="7ed63-134">No aplicativo de exemplo, você pode alternar entre o modo de tinta e de apagamento para alterar a função da caneta.</span><span class="sxs-lookup"><span data-stu-id="7ed63-134">In the sample application, you can toggle between Ink and Erase mode to change the function of the pen.</span></span>


```C++
        private void miInk_Click(object sender, System.EventArgs e)
        {
            // Turn on the inking mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Ink;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = true;
            miErase.Checked = false;

            // Update the UI
            this.Refresh();
        }

        private void miErase_Click(object sender, System.EventArgs e)
        {
            // Turn on the ink deletion mode
            myInkOverlay.EditingMode = InkOverlayEditingMode.Delete;

            // Update the state of the Ink and Erase menu items
            miInk.Checked = false;
            miErase.Checked = true;

            // Update the UI
            this.Refresh();
        }
```



<span data-ttu-id="7ed63-135">Quando você adiciona ou exclui traços, os exemplos atualizam o [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="7ed63-135">When you add or delete strokes, the samples updates the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)).</span></span>


```C++
        private void myInkOverlay_Stroke(object sender, InkCollectorStrokeEventArgs e)
        {
            // Filter out the eraser stroke.
            if (InkOverlayEditingMode.Ink == myInkOverlay.EditingMode)
            {

                // Add the new stroke to the InkAnalyzer's stroke collection
                myInkAnalyzer.AddStroke(e.Stroke);

                if (miAutomaticLayoutAnalysis.Checked)
                {
                    // Invoke an analysis operation on the background thread
                    myInkAnalyzer.BackgroundAnalyze();
                }
            }
        }

        void myInkOverlay_StrokeDeleting(object sender, InkOverlayStrokesDeletingEventArgs e)
        {
            // Remove the strokes to be deleted from the InkAnalyzer's stroke collection
            myInkAnalyzer.RemoveStrokes(e.StrokesToDelete);

            // If automatic layout analysis is turned on, analyze the ink on the background thread
            if ( miAutomaticLayoutAnalysis.Checked )
            {
                // Invoke an analysis operation on the background thread
                myInkAnalyzer.BackgroundAnalyze ( );
            }
        }
```



<span data-ttu-id="7ed63-136">Observe que, no menu modo, a análise de layout automática está ativada por padrão.</span><span class="sxs-lookup"><span data-stu-id="7ed63-136">Notice that in the Mode menu, Automatic Layout Analysis is on by default.</span></span> <span data-ttu-id="7ed63-137">Com essa opção selecionada, os manipuladores de eventos [Stroke](/previous-versions/ms835344(v=msdn.10)) e [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) do objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) chamam o método [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) toda vez que um traço é criado ou excluído.</span><span class="sxs-lookup"><span data-stu-id="7ed63-137">With this option selected, the [InkOverlay](/previous-versions/ms833057(v=msdn.10)) object's [Stroke](/previous-versions/ms835344(v=msdn.10)) and [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) event handlers call the [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method every time a stroke is created or deleted.</span></span>

> [!Note]  
> <span data-ttu-id="7ed63-138">Chamar o método [Analyze](/previous-versions/ms568971(v=vs.100)) do objeto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) com mais de alguns traços presentes cria um atraso perceptível em um aplicativo.</span><span class="sxs-lookup"><span data-stu-id="7ed63-138">Calling the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) object's [Analyze](/previous-versions/ms568971(v=vs.100)) method with more than a few strokes present creates a noticeable delay in an application.</span></span> <span data-ttu-id="7ed63-139">Isso ocorre porque Analyze é uma operação de análise de tinta síncrona.</span><span class="sxs-lookup"><span data-stu-id="7ed63-139">This is because Analyze is a synchronous ink analysis operation.</span></span> <span data-ttu-id="7ed63-140">Na prática, chame o método Analyze somente quando você precisar do resultado.</span><span class="sxs-lookup"><span data-stu-id="7ed63-140">In practice, call the Analyze method only when you need the result.</span></span> <span data-ttu-id="7ed63-141">Caso contrário, use o método [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) assíncrono, conforme mostrado no exemplo.</span><span class="sxs-lookup"><span data-stu-id="7ed63-141">Otherwise use the asynchronous [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) method, as shown in the sample.</span></span>

 

## <a name="handling-the-analysis-results"></a><span data-ttu-id="7ed63-142">Manipulando os resultados da análise</span><span class="sxs-lookup"><span data-stu-id="7ed63-142">Handling the Analysis Results</span></span>

<span data-ttu-id="7ed63-143">O exemplo cria duas matrizes para manter os vários retângulos, horizontal ou girado.</span><span class="sxs-lookup"><span data-stu-id="7ed63-143">The sample creates two arrays to hold the various rectangles, either horizontal or rotated.</span></span> <span data-ttu-id="7ed63-144">Use uma caixa delimitadora girada para obter o ângulo no qual uma linha de palavras é escrita.</span><span class="sxs-lookup"><span data-stu-id="7ed63-144">Use a rotated bounding box to get the angle on which a line of words is written.</span></span> <span data-ttu-id="7ed63-145">O exemplo mostra as propriedades retornadas pelo [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) e exibe a caixa delimitadora ou a caixa delimitadora girada (dependendo da seleção de menu).</span><span class="sxs-lookup"><span data-stu-id="7ed63-145">The sample shows the properties returned by the [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) and displays the bounding box or the rotated bounding box (depending on the menu selection).</span></span>


```C++
      private Rectangle[] GetHorizontalBBoxes(Guid nodeType, int inflate)
        {
            // Declare the array of rectangles to hold the result
            Rectangle[] analysisRects;

            // Get the division units from the division result of division type
            ContextNodeCollection nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // If there is at least one unit, we construct the rectangles
            if ((null != nodes) && (0 < nodes.Count))
            {
                // We need to convert rectangles from ink units to
                // pixel units. For that, we need Graphics object
                // to pass to InkRenderer.InkSpaceToPixel method
                using (Graphics g = drawArea.CreateGraphics())
                {
                    // Construct the rectangles
                    analysisRects = new Rectangle[nodes.Count];

                    // InkRenderer.InkSpaceToPixel takes Point as parameter. 
                    // Create two Point objects to point to (Top, Left) and
                    // (Width, Height) properties of rectangle. (Width, Height)
                    // is used instead of (Right, Bottom) because (Right, Bottom)
                    // are read-only properties on Rectangle
                    Point ptLocation = new Point();
                    Point ptSize = new Point();

                    // Index into the bounding boxes
                    int i = 0;

                    // Iterate through the collection of division units to obtain the bounding boxes
                    foreach (ContextNode node in nodes)
                    {
                        // Get the bounding box of the strokes of the division unit
                        analysisRects[i] = node.Location.GetBounds();

                        // The bounding box is in ink space unit. Convert them into pixel unit. 
                        ptLocation = analysisRects[i].Location;
                        ptSize.X = analysisRects[i].Width;
                        ptSize.Y = analysisRects[i].Height;

                        // Convert the Location from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptLocation);

                        // Convert the Size from Ink Space to Pixel Space
                        myInkOverlay.Renderer.InkSpaceToPixel(g, ref ptSize);

                        // Assign the result back to the corresponding properties
                        analysisRects[i].Location = ptLocation;
                        analysisRects[i].Width = ptSize.X;
                        analysisRects[i].Height = ptSize.Y;

                        // Inflate the rectangle by inflate pixels in both directions
                        analysisRects[i].Inflate(inflate, inflate);

                        // Increment the index
                        ++i;
                    }

                } // Relinquish the Graphics object
            }
            else
            {
                // Otherwise we return null
                analysisRects = null;
            }

            // Return the Rectangle[] object
            return analysisRects;
        }

        private System.Collections.ArrayList GetRotatedBBoxes(Guid nodeType, int inflate)
        {
            //Find the correct collection of results nodes.
            ContextNodeCollection Nodes = myInkAnalyzer.FindNodesOfType(nodeType);

            // Declare the array list to hold the results; 
            // This array represents the four points of a rectangle, with the first point
            // copied again to complete the cycle of points.

            ArrayList polygonPoints = new ArrayList(Nodes.Count);

            // Cycle through each results node, get and convert the
            // rotated bounding box points
            foreach (ContextNode node in Nodes)
            {
                //Declare the point array
                Point[] rotatedBoundingBox = null;

                //Switch on the type of ContextNode to cast into the
                //appropriate type.  This is required to access the 
                //type specific property "RotatedBoundingBox" which
                //is not found on all ContextNode types.
                if (nodeType == ContextNodeType.InkWord)
                {
                    rotatedBoundingBox = ((InkWordNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Line)
                {
                    rotatedBoundingBox = ((LineNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.Paragraph)
                {
                    rotatedBoundingBox = ((ParagraphNode)node).GetRotatedBoundingBox();
                }
                else if (nodeType == ContextNodeType.WritingRegion ||
                         nodeType == ContextNodeType.InkDrawing ||
                         nodeType == ContextNodeType.InkBullet )
                {

                    // Rotated Bounding Boxes are not a supported option for 
                    // Writing Regions or Drawings.  We return the axis aligned 
                    // bounding box instead
                    Rectangle rect = node.Location.GetBounds();

                    // We need to create a looped list of 4 points to be consistent
                    // with the way InkAnalysis represents rotated bounding boxes.  
                    rotatedBoundingBox = new Point[4];

                    rotatedBoundingBox[0] = new Point(rect.X, rect.Y);
                    rotatedBoundingBox[1] = new Point(rect.Right, rect.Y);
                    rotatedBoundingBox[2] = new Point(rect.Right, rect.Bottom);
                    rotatedBoundingBox[3] = new Point(rect.X, rect.Bottom);

                }


                if (null != rotatedBoundingBox)
                {
                    // We need to convert rectangles from ink units to
                    // pixel units. For that, we need Graphics object
                    // to pass to InkRenderer.InkSpaceToPixel method
                    using (Graphics g = drawArea.CreateGraphics())
                    {
                        // convert each of the points from ink space to pixel space
                        for (int i = 0; i < rotatedBoundingBox.Length; i++)
                        {
                            myInkOverlay.Renderer.InkSpaceToPixel(g, ref rotatedBoundingBox[i]);
                        }

                        //inflate the points by calling helper method
                        InflateHelperMethod(ref rotatedBoundingBox, inflate);

                        // increment the node portion of the polygonPoints array
                        polygonPoints.Add(rotatedBoundingBox);
                    }
                }
            }
            //Return the results
            return polygonPoints;
        }
```



<span data-ttu-id="7ed63-146">O analisador calcula o [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) durante a análise.</span><span class="sxs-lookup"><span data-stu-id="7ed63-146">The parser calculates [GetRotatedBoundingBox](/previous-versions/ms569544(v=vs.100)) during analysis.</span></span> <span data-ttu-id="7ed63-147">Você pode acessar as informações das caixas delimitadora giradas em seu aplicativo por vários motivos úteis:</span><span class="sxs-lookup"><span data-stu-id="7ed63-147">You can access the information from the rotated bounding boxes in your application for a number of useful reasons:</span></span>

-   <span data-ttu-id="7ed63-148">Detecte ou desenhe os limites de uma única linha, parágrafo ou outra unidade.</span><span class="sxs-lookup"><span data-stu-id="7ed63-148">Detect or draw the bounds of a single line, paragraph, or other unit.</span></span>
-   <span data-ttu-id="7ed63-149">Determine o ângulo no qual uma linha ou parágrafo é escrito.</span><span class="sxs-lookup"><span data-stu-id="7ed63-149">Determine the angle at which a line or paragraph is written.</span></span>
-   <span data-ttu-id="7ed63-150">Implemente recursos como a seleção de uma linha, um parágrafo ou outra unidade.</span><span class="sxs-lookup"><span data-stu-id="7ed63-150">Implement features such as selection for a line, paragraph, or other unit.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7ed63-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="7ed63-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7ed63-152">Reconhecimento básico e análise de tinta</span><span class="sxs-lookup"><span data-stu-id="7ed63-152">Basic Recognition and Ink Analysis</span></span>](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[<span data-ttu-id="7ed63-153">Exemplo de formulário de papel digitalizado</span><span class="sxs-lookup"><span data-stu-id="7ed63-153">Scanned Paper Form Sample</span></span>](scanned-paper-form-sample.md)
</dt> <dt>

[<span data-ttu-id="7ed63-154">Exemplo de divisória de tinta</span><span class="sxs-lookup"><span data-stu-id="7ed63-154">Ink Divider Sample</span></span>](ink-divider-sample.md)
</dt> </dl>

 

