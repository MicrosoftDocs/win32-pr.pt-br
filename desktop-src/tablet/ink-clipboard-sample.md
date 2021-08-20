---
description: Este programa demonstra como copiar e colar tinta em outro aplicativo. Ele também permite que o usuário copie uma seleção de traços e copie o resultado no objeto de tinta existente.
ms.assetid: a0c42f1c-543d-44f8-83d9-fe810de410ff
title: Exemplo de área de transferência de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73aa8acdf785321dc01706d4a4de50e0a2673a31250edbfa4316a27aecd0ce3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119032324"
---
# <a name="ink-clipboard-sample"></a>Exemplo de área de transferência de tinta

Este programa demonstra como copiar e colar tinta em outro aplicativo. Ele também permite que o usuário copie uma seleção de traços e copie o resultado no objeto de tinta existente.

Os seguintes modos de área de transferência estão disponíveis:

-   Formato serializado de tinta (ISF)
-   Metarquivo
-   EMF (Metarquivo Avançado)
-   Bitmap
-   Tinta de texto
-   Esboço de tinta

Tinta de texto e tinta de esboço são dois tipos de controles de tinta usados como texto ou desenho, respectivamente. É possível colar ISF, tinta de texto e esboço de tinta em tinta existente.

Além da área de transferência, este exemplo também ilustra como selecionar traços com a ferramenta de laço. O usuário pode mover traços selecionados e modificar seus atributos de desenho. Essa funcionalidade é um subconjunto da funcionalidade de seleção já fornecida pelo controle de sobreposição de tinta; ele é implementado aqui para fins ilustrativos.

Os seguintes recursos são usados neste exemplo:

-   O [objeto InkCollector.](/previous-versions/ms583683(v=vs.100))
-   Suporte à área de transferência de tinta.
-   O uso do laço com o [método Microsoft.Ink.Ink.HitTest.](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90))

Este exemplo demonstra como renderizar tinta, copiar essa tinta e colar a tinta em outro aplicativo, como Microsoft Paint.

## <a name="collecting-ink-and-setting-up-the-form"></a>Coletando tinta e configurando o formulário

Primeiro, consulte as interfaces de Automação de Tablet PC, que são instaladas com o SDK (Software Development Kit) do Microsoft Windows <entity type="reg"/> XP Tablet Edition.


```C++
using Microsoft.Ink;
```



Em seguida, o formulário declara algumas constantes e campos que serão notados posteriormente neste exemplo.


```C++
// Declare constant for the size of the border around selected strokes
private const int SelectedInkWidthIncrease = 105;

// Declare constant for the size of a lasso point
private const int DotSize = 6;

// Declare constant for the spacing between lasso points
private const int DotSpacing = 7;

// Declare constant for the selection rectangle padding
private const int SelectionRectBuffer = 8;

// Declare constant for the lasso hit test percent (specifies how much
// of the stoke must fall within the lasso in order to be selected).
private const float LassoPercent = 50;
...
// Declare the InkCollector object
private InkCollector myInkCollector = null;

// The points in the selection lasso
private ArrayList lassoPoints = null;

// The array of rectangle selection handles
private PictureBox[] selectionHandles;

// The rectangle that bounds the selected strokes
private Rectangle selectionRect = Rectangle.Empty;

// The strokes that have been selected by the lasso
private Strokes selectedStrokes = null;
...
// Declare the colors used in the selection lasso
private Color dotEdgeColor = Color.White;
private Color dotColor = SystemColors.Highlight;
private Color connectorColor = Color.Black;

// Declare the pens used to draw the selection lasso
private Pen connectorPen = null;
private Pen dotEdgePen = null;
private Pen dotPen = null;
```



Por fim, no [](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) manipulador de eventos Load do formulário, o formulário é inicializado, um objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para o formulário é criado e o coletor de tinta está habilitado.


```C++
// Create an ink collector and assign it to this form's window
myInkCollector = new InkCollector(this.Handle);

// Turn the ink collector on
myInkCollector.Enabled = true;
```



## <a name="handling-menu-events"></a>Manipulando eventos de menu

Os manipuladores de eventos do item de menu atualizam principalmente o estado do formulário.

O comando Clear remove o retângulo de seleção e exclui os traços do objeto Ink do coletor [de](/previous-versions/ms583670(v=vs.100)) tinta.

O comando Exit desabilita o coletor de tinta antes de sair do aplicativo.

O menu Editar habilita os comandos Recortar e Copiar com base no estado de seleção do formulário e habilita o comando Colar com base no conteúdo da área de transferência, determinado pelo uso do método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) do objeto [Ink.](/previous-versions/ms583670(v=vs.100))

Os comandos Recortar e Copiar usam um método auxiliar para copiar tinta para a área de transferência. O comando Cut usa um método auxiliar para excluir os traços selecionados.

O comando Colar primeiro verifica o método [CanPaste](/previous-versions/dotnet/netframework-3.5/ms571314(v=vs.90)) do objeto [Ink](/previous-versions/ms583670(v=vs.100)) para ver se o objeto na área de transferência pode ser colar. Em seguida, o comando Colar calcula o canto superior esquerdo da região de colar, converte as coordenadas de pixels em espaço de tinta e cole os traços da área de transferência para o coletor de tinta. Por fim, a caixa de seleção é atualizada.


```C++
if (myInkCollector.Ink.CanPaste())
{
   // Compute the location where the ink should be pasted;
    // this location should be shifted from the origin
    // to account for the width of the selection rectangle's handle.
    Point offset = new Point(leftTopHandle.Width+1,leftTopHandle.Height+1);
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref offset);
    }
    // Use Ink API to paste the clipboard data into the Ink
    Strokes pastedStrokes = myInkCollector.Ink.ClipboardPaste(offset);

    // If the contents of the clipboard were a valid format 
    // (Ink Serialized Format or Embeddable OLE Object) and at
    // least one stroke was pasted into the ink, use a helper 
    // method to update the stroke selection.  Otherwise,
    // the result is null and this paste becomes a no-op.  
    if (null != pastedStrokes)
    {
        SetSelection(pastedStrokes);
    }
}
```



Os comandos Selecionar e Tinta atualizam o modo de aplicativo e os atributos de desenho padrão, limpam a seleção atual, atualizem o estado do menu e atualizem o formulário. Outros manipuladores dependem do estado do aplicativo para executar a função correta, sejassoando ou colocando tinta. Além disso, o comando Select adiciona os manipuladores de eventos [NewPackets](/previous-versions/ms567621(v=vs.100)) e [Stroke](/previous-versions/ms567622(v=vs.100)) ao coletor de tinta e o comando Ink remove esses manipuladores de eventos do coletor de tinta.

Os formatos disponíveis na Área de Transferência quando os traços são copiados são listados no menu Formatar e o usuário seleciona o formato para copiar a tinta dessa lista. Os tipos de formatos disponíveis incluem ISF (formato ISF), metarquivo, metarquivo aprimorado e bitmap. Os formatos de tinta de esboço e tinta de texto são mutuamente exclusivos e dependem da tinta sendo copiada para a área de transferência como um objeto OLE.

O menu Estilo permite que o usuário altere as propriedades de cor e largura da caneta e quaisquer traços selecionados.

Por exemplo, o comando Vermelho define a propriedade [Color](/previous-versions/ms582103(v=vs.100)) da propriedade [DefaultDrawingAttributes](/previous-versions/ms571711(v=vs.100)) do coletor de tinta para a cor vermelha. Como a [propriedade DrawingAttributes](/previous-versions/ms581965(v=vs.100)) do objeto [Cursor](/previous-versions/ms552104(v=vs.100)) não foi definida, qualquer nova tinta desenhada para o coletor de tinta herda para a cor de desenho padrão. Além disso, se algum traço estiver selecionado no momento, a propriedade Color de atributos de desenho de cada traço também será atualizada.


```C++
private void SetColor(Color newColor)
{
    myInkCollector.DefaultDrawingAttributes.Color = newColor;

    // In addition to updating the ink collector, also update
    // the drawing attributes of all selected strokes.
    if (HasSelection())
    {
        foreach (Stroke s in selectedStrokes)
        {
            s.DrawingAttributes.Color = newColor;
        }
    }

    Refresh();
}
```



## <a name="handling-mouse-events"></a>Manipulando eventos do mouse

O [manipulador de eventos MouseMove](/previous-versions/ms567617(v=vs.100)) verifica o modo do aplicativo. Se o modo for MoveInk e um botão do mouse estiver para baixo, o manipulador moverá os traços usando o método Move da coleção [Strokes](/previous-versions/ms552701(v=vs.100)) e atualizará a caixa de seleção. Caso contrário, o manipulador verifica se o retângulo de seleção contém o cursor, habilita a coleta de tinta de acordo e também define o cursor de acordo.

O [manipulador de eventos MouseDown](/previous-versions/ms567616(v=vs.100)) verifica a configuração do cursor. Se o cursor for definido como [SizeAll](/dotnet/api/system.windows.forms.cursors.sizeall?view=netcore-3.1), o manipulador definirá o modo de aplicativo como MoveInk e registra o local do cursor. Caso contrário, se houver uma seleção atual, limpe-a.

O [manipulador de eventos MouseUp](/previous-versions/ms567618(v=vs.100)) verifica o modo do aplicativo. Se o modo for MoveInk, o manipulador define o modo de aplicativo com base no estado selecionado do comando Select.

O [evento NewPackets](/previous-versions/ms567621(v=vs.100)) é gerado no modo de seleção quando o coletor de tinta recebe novos dados de pacote. Se o aplicativo estiver no modo de seleção, será necessário interceptar os novos pacotes e usá-los para desenhar o laço de seleção.

A coordenada de cada pacote é convertida em pixels, restrita à área de desenho e adicionada à coleção de pontos do laço. Um método auxiliar é chamado para desenhar o laço no formulário.

## <a name="handling-a-new-stroke"></a>Manipulando um novo traço

O [evento Stroke](/previous-versions/ms567622(v=vs.100)) é gerado no modo de seleção quando um novo traço é desenhado. Se o aplicativo estiver no modo de seleção, esse traço corresponderá ao laço e será necessário atualizar as informações dos traços selecionados.

O manipulador cancela o evento [Stroke,](/previous-versions/ms567622(v=vs.100)) verifica se há mais de dois pontos desso, copia a coleção Points para uma matriz de objetos [Point](/dotnet/api/system.drawing.point?view=netcore-3.1) e converte as coordenadas dos pontos na matriz de pixels em espaço de tinta. Em seguida, o manipulador usa o método [HitTest](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) do objeto [Ink](/previous-versions/ms583670(v=vs.100)) para obter os traços selecionados pelos pontos desso e atualiza o estado de seleção do formulário. Por fim, o traço que gerou o evento é removido da coleção de traços selecionados, a coleção de pontos desso é esvaziada e um método auxiliar desenha o retângulo de seleção.


```C++
// This stroke corresponds to the lasso - 
// cancel it so that it is not added into the ink
e.Cancel = true;  

Strokes hitStrokes = null;

// If there are enough lasso points, perform a hit test
// to determine which strokes were selected. 
if (lassoPoints.Count > 2)
{

    // Convert the lasso points from pixels to ink space
    Point[] inkLassoPoints = (Point[])lassoPoints.ToArray(typeof(Point));
    using (Graphics g = CreateGraphics())
    {
        myInkCollector.Renderer.PixelToInkSpace(g, ref inkLassoPoints);
    }
    // Perform a hit test on this ink collector's ink to
    // determine which points were selected by the lasso stroke.
    //
    // Note that there is a slight inefficiency here since the
    // lasso stroke is part of the ink and, therefore, part of the
    // hit test - even though we don't need it.   It would have 
    // been more efficient to remove the stroke from the ink before 
    // calling HitTest.  However, it is not good practice to modify 
    // the stroke inside of its own event handler.
    hitStrokes = myInkCollector.Ink.HitTest(inkLassoPoints, LassoPercent);
    hitStrokes.Remove(e.Stroke);
}

// Reset the lasso points
lassoPoints.Clear();
lastDrawnLassoDot = Point.Empty;

// Use helper method to set the selection
SetSelection(hitStrokes);
```



## <a name="copying-ink-to-the-clipboard"></a>Copiando tinta para a área de transferência

O método auxiliar CopyInkToClipboard cria um valor [InkClipboardFormats,](/previous-versions/ms583681(v=vs.100)) verifica o estado do menu Formatar para [](/previous-versions/ms583670(v=vs.100)) atualizar os formatos a colocar na área de transferência e usa o método [ClipboardCopy](/previous-versions/dotnet/netframework-3.5/ms571316(v=vs.90)) do objeto Ink para copiar os traços para a área de transferência.


```C++
// Declare the ink clipboard formats to put on the clipboard
InkClipboardFormats formats = new InkClipboardFormats();

// Use selected format menu items to set the clipboard 
// formats
...

// If at least one format was selected, invoke the Ink
// API's ClipboardCopy method.  Note that selectedStrokes
// could be null, but that this is ok - if selectedStrokes
// is null, all of the ink is copied.
if (formats != InkClipboardFormats.None)
{
    myInkCollector.Ink.ClipboardCopy(selectedStrokes,formats,clipboardModes);
}
else
{
    MessageBox.Show("No clipboard formats selected");
}
```



## <a name="updating-a-selection"></a>Atualizando uma seleção

O método auxiliar SetSelection atualiza o selectedStrkes arquivado e, se a coleção for **NULL** ou **EMPTY,** o retângulo de seleção será definido como o retângulo vazio. Se a coleção [de Traços selecionada](/previous-versions/ms552701(v=vs.100)) não estiver vazia, o método SetSelection executará as seguintes etapas:

-   Determina o retângulo delimitado usando o [método GetBoundingBox](/previous-versions/dotnet/netframework-3.5/ms571376(v=vs.90)) da coleção de traços
-   Converte as coordenadas de retângulo do espaço de tinta em pixels
-   Infla o retângulo para fornecer algum espaço visual entre ele e os traços selecionados
-   Cria alças de seleção para a caixa de seleção atual

Por fim, o método SetSelection define a visibilidade das alças de seleção e define a propriedade [AutoRedraw](/previous-versions/ms571706(v=vs.100)) do coletor de tinta como **FALSE,** se os traços forem selecionados.


```C++
// Tracks whether the rectangle that bounds the selected
// strokes should be displayed
bool isSelectionVisible = false;

// Update the selected strokes collection
selectedStrokes = strokes;

// If no strokes are selected, set the selection rectangle
// to empty
if (!HasSelection())
{
    selectionRect = Rectangle.Empty;
}
    // Otherwise, at least one stroke is selected and it is necessary
    // to display the selection rectangle.
else
{
    isSelectionVisible = true;

    // Retrieve the bounding box of the strokes
    selectionRect = selectedStrokes.GetBoundingBox();
    using (Graphics g = CreateGraphics())
    {
        InkSpaceToPixel(g, ref selectionRect);
    }

    // Pad the selection rectangle so that the selected ink 
    // doesn't overlap with the selection rectangle's handles.
    selectionRect.Inflate(SelectionRectBuffer, SelectionRectBuffer);

    // compute the center of the rectangle that bounds the 
    // selected strokes
    int xAvg = (selectionRect.Right+selectionRect.Left)/2;
    int yAvg = (selectionRect.Top+selectionRect.Bottom)/2;

    // Draw the resize handles
    // top left
    SetLocation(selectionHandles[0],selectionRect.Left, selectionRect.Top);
    // top
    SetLocation(selectionHandles[1],xAvg, selectionRect.Top);
    // top right 
    SetLocation(selectionHandles[2],selectionRect.Right, selectionRect.Top);

    // left 
    SetLocation(selectionHandles[3],selectionRect.Left, yAvg);
    // right
    SetLocation(selectionHandles[4],selectionRect.Right, yAvg);

    // bottom left
    SetLocation(selectionHandles[5],selectionRect.Left, selectionRect.Bottom);
    // bottom
    SetLocation(selectionHandles[6],xAvg, selectionRect.Bottom);
    // bottom right
    SetLocation(selectionHandles[7],selectionRect.Right, selectionRect.Bottom);
}

// Set the visibility of each selection handle in the 
// selection rectangle.  If there is no selection, all 
// handles should be hidden.  Otherwise, all handles should
// be visible.
foreach(PictureBox pb in selectionHandles)
{
    pb.Visible = isSelectionVisible;
}

// Turn off autoredrawing if there is a selection - otherwise,
// the selected ink is not displayed as selected.
myInkCollector.AutoRedraw = !isSelectionVisible;

// Since the selection has changed, repaint the screen.
Refresh();
```



## <a name="drawing-the-lasso"></a>Desenhando o laço

O laço é desenhado como uma série de pontos abertos que seguem o caminho do traço desso e uma linha de conector tracejada entre as duas extremidades. O [evento NewPackets](/previous-versions/ms567621(v=vs.100)) é gerado à medida que o laço está sendo desenhado e o manipulador de eventos passa as informações de traço para o método DrawLasso.

O método auxiliar DrawLasso primeiro remove a linha antiga do conector e, em seguida, itera sobre os pontos no traço. Em seguida, DrawLasso calcula onde colocar os pontos ao longo do traço e os desenha. Por fim, ele desenha uma nova linha de conector.

## <a name="closing-the-form"></a>Fechando o formulário

O método [Dispose do](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) formulário descarta o [objeto InkCollector,](/previous-versions/ms583683(v=vs.100)) myInkCollector.

 

 
