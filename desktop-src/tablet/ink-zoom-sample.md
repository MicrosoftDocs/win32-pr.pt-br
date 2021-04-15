---
description: Este programa de exemplo demonstra como aplicar zoom e rolar a tinta.
ms.assetid: d3b5668a-29bf-4846-8ab0-1bda7b6160f9
title: Exemplo de zoom de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f20253a3f56b2a03b5a6dad45ab9a8b72090b5ea
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501400"
---
# <a name="ink-zoom-sample"></a><span data-ttu-id="51436-103">Exemplo de zoom de tinta</span><span class="sxs-lookup"><span data-stu-id="51436-103">Ink Zoom Sample</span></span>

<span data-ttu-id="51436-104">Este programa de exemplo demonstra como aplicar zoom e rolar a tinta.</span><span class="sxs-lookup"><span data-stu-id="51436-104">This sample program demonstrates how to zoom and scroll ink.</span></span> <span data-ttu-id="51436-105">Em particular, ele permite que o usuário amplie e reduza a tinta em incrementos.</span><span class="sxs-lookup"><span data-stu-id="51436-105">In particular, it enables the user to zoom in and out of ink in increments.</span></span> <span data-ttu-id="51436-106">Ele também demonstra como aplicar zoom em uma região específica usando um retângulo de zoom.</span><span class="sxs-lookup"><span data-stu-id="51436-106">It also demonstrates how to zoom into a particular region using a zoom rectangle.</span></span> <span data-ttu-id="51436-107">Por fim, este exemplo ilustra como coletar tinta em taxas de zoom diferentes e como configurar a rolagem na área de desenho com zoom.</span><span class="sxs-lookup"><span data-stu-id="51436-107">Finally, this sample illustrates how to collect ink at different zoom ratios and how to set up scrolling within the zoomed drawing area.</span></span>

<span data-ttu-id="51436-108">No exemplo, a exibição do objeto de [processador](/previous-versions/ms828481(v=msdn.10)) e as transformações de objeto são usadas para executar o zoom e a rolagem.</span><span class="sxs-lookup"><span data-stu-id="51436-108">In the sample, the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's view and object transforms are used to perform zooming and scrolling.</span></span> <span data-ttu-id="51436-109">A transformação exibir aplica-se aos pontos e à largura da caneta.</span><span class="sxs-lookup"><span data-stu-id="51436-109">The view transform applies to the points and the pen width.</span></span> <span data-ttu-id="51436-110">A transformação do objeto se aplica somente aos pontos.</span><span class="sxs-lookup"><span data-stu-id="51436-110">The object transform applies only to the points.</span></span> <span data-ttu-id="51436-111">O usuário pode controlar qual transformação é usada alterando o item dimensionar largura da caneta no menu modo.</span><span class="sxs-lookup"><span data-stu-id="51436-111">The user can control which transform is used by changing the Scale Pen Width item on the Mode menu.</span></span>

> [!Note]  
> <span data-ttu-id="51436-112">É problemático executar algumas chamadas COM em determinados métodos de interface ([**InkRenderer. SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) e [**InkRenderer. SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), por exemplo) quando uma mensagem é enviada.</span><span class="sxs-lookup"><span data-stu-id="51436-112">It is problematic to perform some COM calls on certain interface methods ([**InkRenderer.SetViewTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setviewtransform) and [**InkRenderer.SetObjectTransform**](/windows/desktop/api/msinkaut/nf-msinkaut-iinkrenderer-setobjecttransform), for example) when a message has been SENT.</span></span> <span data-ttu-id="51436-113">Quando as mensagens são enviadas, elas precisam ser marshalled para a fila de mensagens POST.</span><span class="sxs-lookup"><span data-stu-id="51436-113">When messages are SENT, they need to be marshalled to the POST message queue.</span></span> <span data-ttu-id="51436-114">Para resolver esse cenário, teste se você está tratando uma mensagem do POST chamando [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) e poste a mensagem para você mesmo se a mensagem foi enviada.</span><span class="sxs-lookup"><span data-stu-id="51436-114">To address this scenario, test whether you are handling a message from POST by calling [**InSendMesssageEx**](/windows/desktop/api/winuser/nf-winuser-insendmessageex) and POST the message to yourself if the message was SENT.</span></span>

 

<span data-ttu-id="51436-115">Os recursos a seguir são usados neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="51436-115">The following features are used in this sample:</span></span>

-   <span data-ttu-id="51436-116">O objeto [InkCollector](/previous-versions/ms583683(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="51436-116">The [InkCollector](/previous-versions/ms583683(v=vs.100)) object</span></span>
-   <span data-ttu-id="51436-117">O método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="51436-117">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method</span></span>
-   <span data-ttu-id="51436-118">O método [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10))</span><span class="sxs-lookup"><span data-stu-id="51436-118">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method</span></span>

## <a name="initializing-the-form"></a><span data-ttu-id="51436-119">Inicializando o formulário</span><span class="sxs-lookup"><span data-stu-id="51436-119">Initializing the Form</span></span>

<span data-ttu-id="51436-120">Primeiro, o exemplo faz referência às interfaces de automação do Tablet PC, que são fornecidas no SDK (Software Development Kit) do Windows Vista ou do Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="51436-120">First, the sample references the Tablet PC Automation interfaces, which are provided in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



<span data-ttu-id="51436-121">O exemplo declara um [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector` e alguns membros privados para ajudar no dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="51436-121">The sample declares an [InkCollector](/previous-versions/ms583683(v=vs.100)), `myInkCollector`, and some private members to help with scaling.</span></span>


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



<span data-ttu-id="51436-122">Em seguida, o exemplo cria e habilita o [InkCollector](/previous-versions/ms583683(v=vs.100)) no manipulador de eventos [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) do formulário.</span><span class="sxs-lookup"><span data-stu-id="51436-122">Then the sample creates and enables the [InkCollector](/previous-versions/ms583683(v=vs.100)) in the form's [Load](/dotnet/api/system.windows.forms.form.load?view=netcore-3.1) event handler.</span></span> <span data-ttu-id="51436-123">Além disso, a propriedade [Width](/previous-versions/ms837941(v=msdn.10)) da propriedade [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) do objeto InkCollector é definida.</span><span class="sxs-lookup"><span data-stu-id="51436-123">Also, the [Width](/previous-versions/ms837941(v=msdn.10)) property of the InkCollector object's [DefaultDrawingAttributes](/previous-versions/ms836500(v=msdn.10)) property is set.</span></span> <span data-ttu-id="51436-124">Por fim, os intervalos da barra de rolagem são definidos e o método do aplicativo `UpdateZoomAndScroll` é chamado.</span><span class="sxs-lookup"><span data-stu-id="51436-124">Finally, the scroll bar ranges are defined and the application's `UpdateZoomAndScroll` method is called.</span></span>


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



## <a name="updating-the-zoom-and-scroll-values"></a><span data-ttu-id="51436-125">Atualizando os valores de zoom e rolagem</span><span class="sxs-lookup"><span data-stu-id="51436-125">Updating the Zoom and Scroll Values</span></span>

<span data-ttu-id="51436-126">A área de desenho do coletor de tinta é afetada por muitos eventos.</span><span class="sxs-lookup"><span data-stu-id="51436-126">The drawing area of the ink collector is affected by many events.</span></span> <span data-ttu-id="51436-127">No `UpdateZoomAndScroll` método, uma matriz de transformação é usada para dimensionar e converter o coletor de tinta na janela.</span><span class="sxs-lookup"><span data-stu-id="51436-127">In the `UpdateZoomAndScroll` method, a transformation matrix is used to both scale and translate the ink collector within the window.</span></span>

> [!Note]  
> <span data-ttu-id="51436-128">O método [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) aplica a transformação aos traços e à largura da caneta, enquanto o método [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) aplica apenas a transformação aos traços.</span><span class="sxs-lookup"><span data-stu-id="51436-128">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [SetViewTransform](/previous-versions/ms828514(v=msdn.10)) method applies the transform to both the strokes and the pen width, while the [SetObjectTransform](/previous-versions/ms828513(v=msdn.10)) method only applies the transform to the strokes.</span></span>

 

<span data-ttu-id="51436-129">Por fim, o método do aplicativo `UpdateScrollBars` é chamado e o formulário é forçado a atualizar.</span><span class="sxs-lookup"><span data-stu-id="51436-129">Finally, the application's `UpdateScrollBars` method is called and the form is forced to refresh.</span></span>


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



## <a name="managing-the-scroll-bars"></a><span data-ttu-id="51436-130">Gerenciando as barras de rolagem</span><span class="sxs-lookup"><span data-stu-id="51436-130">Managing the Scroll Bars</span></span>

<span data-ttu-id="51436-131">O `UpdateScrollBars` método configura as barras de rolagem para funcionar corretamente com o tamanho da janela atual, a configuração de zoom e o local de rolagem dentro do [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="51436-131">The `UpdateScrollBars` method sets up the scroll bars to work correctly with the current window size, zoom setting, and scroll location within the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span> <span data-ttu-id="51436-132">Esse método calcula a alteração grande e os valores pequenos de alteração para as barras de rolagem vertical e horizontal.</span><span class="sxs-lookup"><span data-stu-id="51436-132">This method calculates the large change and small change values for the vertical and horizontal scroll bars.</span></span> <span data-ttu-id="51436-133">Ele também calcula o valor atual das barras de rolagem e se elas devem estar visíveis.</span><span class="sxs-lookup"><span data-stu-id="51436-133">It also calculates the current value of the scroll bars and whether they should be visible.</span></span> <span data-ttu-id="51436-134">O método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) manipula a conversão de pixels para o espaço de coordenadas com zoom e as contas para qualquer escala e rolagem que é aplicada por meio da exibição e transformações de objeto.</span><span class="sxs-lookup"><span data-stu-id="51436-134">The [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method handles the conversion from pixels to the zoomed coordinate space and accounts for any scaling and scrolling that is applied through the view and object transforms.</span></span>


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



## <a name="zooming-to-a-rectangle"></a><span data-ttu-id="51436-135">Aplicando zoom a um retângulo</span><span class="sxs-lookup"><span data-stu-id="51436-135">Zooming to a Rectangle</span></span>

<span data-ttu-id="51436-136">Os `pnlDrawingArea` manipuladores de eventos do painel gerenciam o desenho do retângulo para a janela.</span><span class="sxs-lookup"><span data-stu-id="51436-136">The `pnlDrawingArea` panel event handlers manage drawing the rectangle to the window.</span></span> <span data-ttu-id="51436-137">Se o comando zoom para rect estiver marcado no menu modo, o manipulador de eventos [MouseUp](/previous-versions/ms567618(v=vs.100)) chamará o método do aplicativo `ZoomToRectangle` .</span><span class="sxs-lookup"><span data-stu-id="51436-137">If the Zoom To Rect command is checked on the Mode menu, then the [MouseUp](/previous-versions/ms567618(v=vs.100)) event handler calls the application's `ZoomToRectangle` method.</span></span> <span data-ttu-id="51436-138">O `ZoomToRectangle` método calcula a largura e a altura do retângulo, verifica as condições de limite, atualiza os valores da barra de rolagem e o fator de escala e, em seguida, chama o método do aplicativo `UpdateZoomAndScroll` para aplicar as novas configurações.</span><span class="sxs-lookup"><span data-stu-id="51436-138">The `ZoomToRectangle` method calculates the width and height of the rectangle, checks for boundary conditions, updates the scroll bar values and the scale factor, and then calls the application's `UpdateZoomAndScroll` method to apply the new settings.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="51436-139">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="51436-139">Closing the Form</span></span>

<span data-ttu-id="51436-140">O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="51436-140">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
