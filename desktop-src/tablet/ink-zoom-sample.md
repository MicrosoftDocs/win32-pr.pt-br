---
description: Este programa de exemplo demonstra como aplicar zoom e rolar a tinta.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Exemplo de zoom de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3d786fe502e1510a44df39049e845f05694a1befae0d4a21bcfa2ba2bd2b19b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119939436"
---
# <a name="ink-zoom-sample"></a>Exemplo de zoom de tinta

Este programa de exemplo demonstra como aplicar zoom e rolar a tinta. Em particular, ele permite que o usuário amplie e reduza a tinta em incrementos. Ele também demonstra como aplicar zoom em uma região específica usando um retângulo de zoom. Por fim, este exemplo ilustra como coletar tinta em taxas de zoom diferentes e como configurar a rolagem na área de desenho com zoom.

No exemplo, a exibição do objeto de [processador](/previous-versions/ms828481(v=msdn.10)) e as transformações de objeto são usadas para executar o zoom e a rolagem. A transformação exibir aplica-se aos pontos e à largura da caneta. A transformação do objeto se aplica somente aos pontos. O usuário pode controlar qual transformação é usada alterando o item dimensionar largura da caneta no menu modo.

> [!Note]  
> É problemático executar algumas chamadas COM em determinados métodos de interface ([**InkRenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) e [**InkRenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), por exemplo) quando uma mensagem é enviada. Quando as mensagens são enviadas, elas precisam ser marshalled para a fila de mensagens POST. Para resolver esse cenário, teste se você está tratando uma mensagem do POST chamando [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) e poste a mensagem para você mesmo se a mensagem foi enviada.

 

Os recursos a seguir são usados neste exemplo:

-   O objeto [InkCollector](/previous-versions/ms583683(v=vs.100))
-   O método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10))
-   O método [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10))

## <a name="initializing-the-form"></a>Inicializando o formulário

primeiro, o exemplo faz referência às interfaces de automação do tablet pc, que são fornecidas no SDK (Kit de desenvolvimento de Software) do Windows Vista ou Windows XP tablet pc Edition.


```C++
using Microsoft.Ink;
```



O exemplo declara um [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` e alguns membros privados para ajudar no dimensionamento.


```C++
// Declare the Ink Collector object
private InkCollector myInkCollector = null;
...
// The starting and ending points of the zoom rectangle
private Rectangle zoomRectangle = Rectangle.Empty;

// The current zoom factor (1 = 100% zoom level)
private float zoomFactor = 1;

// Declare constants for the width and height of the 
// drawing area (in ink space coordinates).
private const int InkSpaceWidth = 50000;
private const int InkSpaceHeight = 50000;
...
// Declare constant for the pen width used by this application
private const float MediumInkWidth = 100;
```



Em seguida, o exemplo cria e habilita o [InkCollector](/previous-versions/ms583683(v=vs.100)) no manipulador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário. Além disso, a propriedade [Width](/previous-versions/ms837941(v=msdn.10)) da propriedade [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) do objeto InkCollector é definida. Por fim, os intervalos da barra de rolagem são definidos e o método do aplicativo `UpdateZoomAndScroll` é chamado.


```C++
private void InkZoom_Load(object sender, System.EventArgs e)
{
   // Create the pen used to draw the zoom rectangle
    blackPen = new Pen(Color.Black, 1);

    // Create the ink collector and associate it with the form
    myInkCollector = new InkCollector(pnlDrawingArea.Handle);

    // Set the pen width
    myInkCollector.DefaultDrawingAttributes.Width = MediumInkWidth;

    // Enable ink collection
    myInkCollector.Enabled = true;

    // Define ink space size - note that the scroll bars
    // map directly to ink space
    hScrollBar.Minimum = 0;
    hScrollBar.Maximum = InkSpaceWidth;
    vScrollBar.Minimum = 0;
    vScrollBar.Maximum = InkSpaceHeight;

    // Set the scroll bars to map to the current zoom level
    UpdateZoomAndScroll();
}
```



## <a name="updating-the-zoom-and-scroll-values"></a>Atualizando os valores de zoom e rolagem

A área de desenho do coletor de tinta é afetada por muitos eventos. No `UpdateZoomAndScroll` método, uma matriz de transformação é usada para dimensionar e converter o coletor de tinta na janela.

> [!Note]  
> O método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) aplica a transformação aos traços e à largura da caneta, enquanto o método [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) aplica apenas a transformação aos traços.

 

Por fim, o método do aplicativo `UpdateScrollBars` é chamado e o formulário é forçado a atualizar.


```C++
// Create a transformation matrix
Matrix m = new Matrix();

// Apply the current scale factor
m.Scale(zoomFactor,zoomFactor);

// Apply the current translation factor - note that since 
// the scroll bars map directly to ink space, their values
// can be used directly.
m.Translate(-hScrollBar.Value, -vScrollBar.Value);

// ...
if (miScalePenWidth.Checked)
{
    myInkCollector.Renderer.SetViewTransform(m);
}
else
{
    myInkCollector.Renderer.SetObjectTransform(m);
}

// Set the scroll bars to map to the current zoom level
UpdateScrollBars();

Refresh();
```



## <a name="managing-the-scroll-bars"></a>Gerenciando as barras de rolagem

O `UpdateScrollBars` método configura as barras de rolagem para funcionar corretamente com o tamanho da janela atual, a configuração de zoom e o local de rolagem dentro do [InkCollector](/previous-versions/ms583683(v=vs.100)). Esse método calcula a alteração grande e os valores pequenos de alteração para as barras de rolagem vertical e horizontal. Ele também calcula o valor atual das barras de rolagem e se elas devem estar visíveis. O método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) manipula a conversão de pixels para o espaço de coordenadas com zoom e as contas para qualquer escala e rolagem que é aplicada por meio da exibição e transformações de objeto.


```C++
// Create a point representing the top left of the drawing area (in pixels)
Point ptUpperLeft = new Point(0, 0);

// Create a point representing the size of a small change
Point ptSmallChange = new Point(SmallChangeSize, SmallChangeSize);

// Create a point representing the lower right of the drawing area (in pixels)
Point ptLowerRight = new Point(hScrollBar.Width, vScrollBar.Height);

using (Graphics g = CreateGraphics())
{
    // Convert each of the points to ink space
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptUpperLeft);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptLowerRight);
    myInkCollector.Renderer.PixelToInkSpace(g, ref ptSmallChange);
}

// Set the SmallChange values (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.SmallChange = ptSmallChange.X - ptUpperLeft.X;
vScrollBar.SmallChange = ptSmallChange.Y - ptUpperLeft.Y;

// Set the LargeChange values to the drawing area width (in ink space)
// Note that it is necessary to subract the upper-left point
// value to account for scrolling.
hScrollBar.LargeChange = ptLowerRight.X - ptUpperLeft.X;
vScrollBar.LargeChange = ptLowerRight.Y - ptUpperLeft.Y;

// If the scroll bars are not needed, hide them
hScrollBar.Visible = hScrollBar.LargeChange < hScrollBar.Maximum;
vScrollBar.Visible = vScrollBar.LargeChange < vScrollBar.Maximum;

// If the horizontal scroll bar value would run off of the drawing area, 
// adjust it
if(hScrollBar.Visible && (hScrollBar.Value + hScrollBar.LargeChange > hScrollBar.Maximum)) 
{
    hScrollBar.Value = hScrollBar.Maximum - hScrollBar.LargeChange;
}

// If the vertical scroll bar value would run off of the drawing area, 
// adjust it
if(vScrollBar.Visible && (vScrollBar.Value + vScrollBar.LargeChange > vScrollBar.Maximum))
{
    vScrollBar.Value = vScrollBar.Maximum - vScrollBar.LargeChange;
}
```



## <a name="zooming-to-a-rectangle"></a>Aplicando zoom a um retângulo

Os `pnlDrawingArea` manipuladores de eventos do painel gerenciam o desenho do retângulo para a janela. Se o comando zoom para rect estiver marcado no menu modo, o manipulador de eventos [MouseUp](/previous-versions/ms567618(v=vs.100)) chamará o método do aplicativo `ZoomToRectangle` . O `ZoomToRectangle` método calcula a largura e a altura do retângulo, verifica as condições de limite, atualiza os valores da barra de rolagem e o fator de escala e, em seguida, chama o método do aplicativo `UpdateZoomAndScroll` para aplicar as novas configurações.

## <a name="closing-the-form"></a>Fechando o formulário

O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
