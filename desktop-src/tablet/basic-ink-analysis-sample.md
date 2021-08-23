---
description: O exemplo análise de tinta básica mostra como a classe InkAnalyzer divide a tinta em vários segmentos de palavras e desenho. Este exemplo é uma versão atualizada do Exemplo de Divisor de Tinta.
ms.assetid: cb9a28d9-f8c6-478e-ae43-2d30106edc7b
title: Exemplo básico de análise de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ab307deac8ac58a741b0c7f332986b09074f4f5c6a8afa53f0156a94916bf16
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660826"
---
# <a name="basic-ink-analysis-sample"></a>Exemplo básico de análise de tinta

O exemplo análise de tinta básica mostra como a [classe InkAnalyzer](/previous-versions/ms583671(v=vs.100)) divide a tinta em vários segmentos de palavras e desenho.

Este exemplo é uma versão atualizada do Exemplo [de Divisor de Tinta.](ink-divider-sample.md) Enquanto o Exemplo de Divisor de Tinta Usa a [classe Divisor,](/previous-versions/ms839398(v=msdn.10)) este exemplo usa a API InkAnalysis mais nova e preferencial. A API inkAnalysis combina o [RecognizerContext](/previous-versions/ms828542(v=msdn.10)) e o Divisor em uma API e expande a funcionalidade de ambos.

Quando você atualiza o formulário, o exemplo desenha um retângulo em torno de cada unidade analisada: palavras, linhas, parágrafos, regiões de escrita, desenhos e marcadores. O formulário usa cores diferentes para as unidades diferentes. Os retângulos também são ampliados por quantidades diferentes para garantir que nenhum retângulo seja obscurecido por nenhum outro.

A tabela a seguir especifica a cor e o ampliação de cada unidade analisada.



| Unidade analisada             | Cor do retângulo | Ampliação de retângulo (pixels) |
|---------------------------|--------------------|--------------------------------|
| Word<br/>           | Verde<br/>   | 1<br/>                   |
| Linha<br/>           | Magenta<br/> | 3<br/>                   |
| Paragraph<br/>      | Azul<br/>    | 5<br/>                   |
| Escrevendo região<br/> | Amarelo<br/>  | 7<br/>                   |
| Desenho<br/>        | Vermelho<br/>     | 1<br/>                   |
| Bala<br/>         | Laranja<br/>  | 1<br/>                   |



 

Você pode apagar traços no formulário. No aplicativo de exemplo, você pode alternar entre o modo Tinta e Apagar para alterar a função da caneta.


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



Quando você adiciona ou exclui traços, os exemplos atualiza o [InkAnalyzer.](/previous-versions/ms583671(v=vs.100))


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



Observe que, no menu Modo, a Análise Automática de Layout está em por padrão. Com essa opção selecionada, os manipuladores de eventos [Stroke](/previous-versions/ms835344(v=msdn.10)) e [StrokesDeleting](/previous-versions/ms835360(v=msdn.10)) do objeto [InkOverlay](/previous-versions/ms833057(v=msdn.10)) chamam o método [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) sempre que um traço é criado ou excluído.

> [!Note]  
> Chamar o método Analyze do [](/previous-versions/ms568971(v=vs.100)) objeto [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) com mais de alguns traços presentes cria um atraso perceptível em um aplicativo. Isso ocorre porque Analisar é uma operação de análise de tinta síncrona. Na prática, chame o método Analisar somente quando precisar do resultado. Caso contrário, use o método [BackgroundAnalyze](/previous-versions/ms568972(v=vs.100)) assíncrono, conforme mostrado no exemplo.

 

## <a name="handling-the-analysis-results"></a>Manipulando os resultados da análise

O exemplo cria duas matrizes para manter os vários retângulos, horizontais ou girados. Use uma caixa delimitada girada para obter o ângulo no qual uma linha de palavras é escrita. O exemplo mostra as propriedades retornadas pelo [InkAnalyzer](/previous-versions/ms583671(v=vs.100)) e exibe a caixa delimitador ou a caixa delimitador girada (dependendo da seleção do menu).


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



O analisador calcula [GetRotatedBoundingBox durante](/previous-versions/ms569544(v=vs.100)) a análise. Você pode acessar as informações das caixas delimitadas giradas em seu aplicativo por vários motivos úteis:

-   Detectar ou desenhar os limites de uma única linha, parágrafo ou outra unidade.
-   Determine o ângulo no qual uma linha ou parágrafo é gravado.
-   Implemente recursos como seleção para uma linha, parágrafo ou outra unidade.

## <a name="related-topics"></a>Tópicos relacionados

<dl> <dt>

[Reconhecimento básico e análise de tinta](basic-recognition-and-ink-analysis.md)
</dt> <dt>

[Exemplo de formulário de papel digitalizado](scanned-paper-form-sample.md)
</dt> <dt>

[Exemplo de divisor de tinta](ink-divider-sample.md)
</dt> </dl>

 

