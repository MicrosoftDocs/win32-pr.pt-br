---
description: Este exemplo ilustra dois métodos para encontrar tinta, dado um local de tela.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Exemplo de teste de colisão de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9d25e6cbc0ed471384bea0cc1977dd38d3ae4830
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "105812381"
---
# <a name="ink-hit-test-sample"></a><span data-ttu-id="a841a-103">Exemplo de teste de colisão de tinta</span><span class="sxs-lookup"><span data-stu-id="a841a-103">Ink Hit Test Sample</span></span>

<span data-ttu-id="a841a-104">Este exemplo ilustra dois métodos para encontrar tinta, dado um local de tela.</span><span class="sxs-lookup"><span data-stu-id="a841a-104">This sample illustrates two methods to find ink, given a screen location.</span></span>

<span data-ttu-id="a841a-105">Os recursos a seguir são usados neste exemplo:</span><span class="sxs-lookup"><span data-stu-id="a841a-105">The following features are used in this sample:</span></span>

-   <span data-ttu-id="a841a-106">Usando um coletor de tinta</span><span class="sxs-lookup"><span data-stu-id="a841a-106">Using an ink collector</span></span>
-   <span data-ttu-id="a841a-107">Executando um teste de clique</span><span class="sxs-lookup"><span data-stu-id="a841a-107">Performing a hit test</span></span>
-   <span data-ttu-id="a841a-108">Localizando o ponto mais próximo</span><span class="sxs-lookup"><span data-stu-id="a841a-108">Locating the nearest point</span></span>

## <a name="accessing-the-ink-api"></a><span data-ttu-id="a841a-109">Acessando a API de tinta</span><span class="sxs-lookup"><span data-stu-id="a841a-109">Accessing the Ink API</span></span>

<span data-ttu-id="a841a-110">Primeiro, referencie as classes do Tablet PC, localizadas no SDK (Software Development Kit) do Windows Vista ou do Windows XP Tablet PC Edition.</span><span class="sxs-lookup"><span data-stu-id="a841a-110">First, reference the Tablet PC classes, located in the Windows Vista or Windows XP Tablet PC Edition Software Development Kit (SDK).</span></span>


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a><span data-ttu-id="a841a-111">Manipulando eventos de carga e de pintura de formulário</span><span class="sxs-lookup"><span data-stu-id="a841a-111">Handling Form Load and Paint Events</span></span>

<span data-ttu-id="a841a-112">O manipulador de eventos Load do formulário:</span><span class="sxs-lookup"><span data-stu-id="a841a-112">The form's Load event handler:</span></span>

-   <span data-ttu-id="a841a-113">Cria um objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) , IC, para o formulário.</span><span class="sxs-lookup"><span data-stu-id="a841a-113">Creates an [InkCollector](/previous-versions/ms583683(v=vs.100)) object, ic, for the form.</span></span>
-   <span data-ttu-id="a841a-114">Define a propriedade [CollectionMode](/previous-versions/ms836497(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para ignorar gestos.</span><span class="sxs-lookup"><span data-stu-id="a841a-114">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [CollectionMode](/previous-versions/ms836497(v=msdn.10)) property to ignore gestures.</span></span>
-   <span data-ttu-id="a841a-115">Habilita o [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="a841a-115">Enables the [InkCollector](/previous-versions/ms583683(v=vs.100)).</span></span>
-   <span data-ttu-id="a841a-116">Define a propriedade [redesenhar](/previous-versions/ms836495(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) como **true**.</span><span class="sxs-lookup"><span data-stu-id="a841a-116">Sets the [InkCollector](/previous-versions/ms583683(v=vs.100)) object's [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property to **TRUE**.</span></span>


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



<span data-ttu-id="a841a-117">O manipulador de eventos de pintura do formulário verifica o modo do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="a841a-117">The form's Paint event handler checks the application mode:</span></span>

-   <span data-ttu-id="a841a-118">No modo HitTest, ele pinta um círculo em volta do cursor.</span><span class="sxs-lookup"><span data-stu-id="a841a-118">In the HitTest mode, it paints a circle around the cursor.</span></span> <span data-ttu-id="a841a-119">A caneta ativa é definida no método handleHitTest do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a841a-119">The active pen is set in the application's handleHitTest method.</span></span>
-   <span data-ttu-id="a841a-120">No modo NearestPoint, ele pinta uma linha vermelha entre o cursor e o ponto próximo ao cursor.</span><span class="sxs-lookup"><span data-stu-id="a841a-120">In the NearestPoint mode, it paints a red line between the cursor and the point nearest the cursor.</span></span> <span data-ttu-id="a841a-121">O ponto mais próximo é calculado no método handleNearestPoint do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a841a-121">The nearest point is calculated in the application's handleNearestPoint method.</span></span>


```C++
if( mode == ApplicationMode.HitTest)
{
    e.Graphics.DrawEllipse(activepen, penPt.X - HitSize/2, penPt.Y - HitSize/2, HitSize, HitSize);
}
else if( mode == ApplicationMode.NearestPoint )
{
    e.Graphics.DrawLine(redPen, penPt, nearestPt);
}
```



<span data-ttu-id="a841a-122">Este exemplo tem um algoritmo redesenhado muito direto.</span><span class="sxs-lookup"><span data-stu-id="a841a-122">This sample has a very straightforward repaint algorithm.</span></span> <span data-ttu-id="a841a-123">Com sua propriedade [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) definida como **true**, o coletor de tinta redesenha a si mesmo quando o formulário é redesenhado.</span><span class="sxs-lookup"><span data-stu-id="a841a-123">With its [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) property set to **TRUE**, the ink collector repaints itself when the form is redrawn.</span></span> <span data-ttu-id="a841a-124">Para simplificar o redesenho do formulário, o aplicativo rastreia uma caixa delimitadora, a variável de membro invalidateRect, para a área em que o Paint é adicionado, o que é invalidado sempre que o formulário é redesenhado.</span><span class="sxs-lookup"><span data-stu-id="a841a-124">To simplify redrawing the form, the application tracks a bounding box, the invalidateRect member variable, for the area where paint is added, which is invalidated each time the form is redrawn.</span></span>

## <a name="handling-menu-events"></a><span data-ttu-id="a841a-125">Manipulando eventos de menu</span><span class="sxs-lookup"><span data-stu-id="a841a-125">Handling Menu Events</span></span>

<span data-ttu-id="a841a-126">O comando exit desabilita o [InkCollector](/previous-versions/ms583683(v=vs.100)) antes de sair do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a841a-126">The Exit command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) before exiting the application.</span></span>

<span data-ttu-id="a841a-127">O comando de tinta atualiza o modo de aplicativo e o status do menu, habilita o coletor de tinta e invalida a região pintada anteriormente do formulário.</span><span class="sxs-lookup"><span data-stu-id="a841a-127">The Ink command updates the application mode and menu status, enables the ink collector, and invalidates the previously painted region of the form.</span></span>

<span data-ttu-id="a841a-128">Os comandos de teste de clique e de ponto mais próximo alteram o cursor, atualizam o modo de aplicativo e o status do menu, desabilitam o coletor de tinta e invalidam a região pintada anteriormente do formulário.</span><span class="sxs-lookup"><span data-stu-id="a841a-128">Both the Hit Test and Nearest Point commands change the cursor, update the application mode and menu status, disable the ink collector, and invalidate the previously painted region of the form.</span></span>

<span data-ttu-id="a841a-129">O claro!</span><span class="sxs-lookup"><span data-stu-id="a841a-129">The Clear!</span></span> <span data-ttu-id="a841a-130">o comando desabilita o [InkCollector](/previous-versions/ms583683(v=vs.100)) ao substituir a propriedade [Ink](/previous-versions/ms836505(v=msdn.10)) do objeto InkCollector por um novo objeto de [tinta](/previous-versions/ms571716(v=vs.100)) , gera um evento de comando de tinta e força uma atualização no controle.</span><span class="sxs-lookup"><span data-stu-id="a841a-130">command disables the [InkCollector](/previous-versions/ms583683(v=vs.100)) while replacing InkCollector object's [Ink](/previous-versions/ms836505(v=msdn.10)) property with a new [Ink](/previous-versions/ms571716(v=vs.100)) object, generates an Ink command event, and forces a refresh on the control.</span></span>

## <a name="handling-mouse-events"></a><span data-ttu-id="a841a-131">Manipulando eventos do mouse</span><span class="sxs-lookup"><span data-stu-id="a841a-131">Handling Mouse Events</span></span>

<span data-ttu-id="a841a-132">O manipulador de eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) verifica o modo do aplicativo:</span><span class="sxs-lookup"><span data-stu-id="a841a-132">The [MouseMove](/previous-versions/ms567617(v=vs.100)) event handler checks the application mode:</span></span>

-   <span data-ttu-id="a841a-133">No modo de tinta, ele não faz nada, permitindo que a tinta seja coletada normalmente pelo coletor de tinta.</span><span class="sxs-lookup"><span data-stu-id="a841a-133">In Ink mode, it does nothing, allowing ink to be collected normally by the ink collector.</span></span>
-   <span data-ttu-id="a841a-134">No modo HitTest, ele envia os argumentos do evento para o método handleHitTest do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a841a-134">In HitTest mode, it sends the event arguments to the application's handleHitTest method.</span></span>
-   <span data-ttu-id="a841a-135">No modo NearestPoint, ele envia os argumentos do evento para o método handleNearestPoint do aplicativo.</span><span class="sxs-lookup"><span data-stu-id="a841a-135">In NearestPoint mode, it sends the event arguments to the application's handleNearestPoint method.</span></span>

## <a name="performing-a-hit-test"></a><span data-ttu-id="a841a-136">Executando um teste de clique</span><span class="sxs-lookup"><span data-stu-id="a841a-136">Performing a Hit Test</span></span>

<span data-ttu-id="a841a-137">O método handleHitTest do aplicativo cria dois pontos, o local do cursor e um ponto atinge os pixels distantes do cursor e, em seguida, converte esses dois pontos de pixels em coordenadas de espaço de tinta.</span><span class="sxs-lookup"><span data-stu-id="a841a-137">The application's handleHitTest method creates two points, the cursor location and a point HitSize pixels distant from the cursor, and then converts these two points from pixels to ink space coordinates.</span></span>


```C++
penPt = new Point(e.X, e.Y);
Point pt2 = new Point(e.X, e.Y);
Point pt3 = new Point(e.X + HitSize/2, e.Y);

using (Graphics g = CreateGraphics())
{
    ic.Renderer.PixelToInkSpace(g, ref pt1);
    ic.Renderer.PixelToInkSpace(g, ref pt2);
}
```



<span data-ttu-id="a841a-138">Em seguida, o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) usa o método [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para localizar os traços que estão dentro de PT3. X-PT2. X unidades de espaço de tinta do cursor, PT2.</span><span class="sxs-lookup"><span data-stu-id="a841a-138">Then, the [InkCollector](/previous-versions/ms583683(v=vs.100)) object uses the [Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) method to find any strokes that are within pt3.X - pt2.X ink space units of the cursor, pt2.</span></span>


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



<span data-ttu-id="a841a-139">Em seguida, o método handleHitTest define a cor da caneta com base em se os traços foram encontrados, invalida a região invalidateRect, calcula uma nova região em que o círculo do teste de clique é desenhado e, em seguida, invalida a nova região.</span><span class="sxs-lookup"><span data-stu-id="a841a-139">The handleHitTest method then sets the pen color based on whether strokes were found, invalidates the invalidateRect region, calculates a new region that the hit test circle is drawn in, and then invalidates the new region.</span></span>

## <a name="locating-the-nearest-point"></a><span data-ttu-id="a841a-140">Localizando o ponto mais próximo</span><span class="sxs-lookup"><span data-stu-id="a841a-140">Locating the Nearest Point</span></span>

<span data-ttu-id="a841a-141">O método handleNearestPoint do aplicativo cria dois pontos iguais ao local do cursor, um desses pontos, pt, é convertido em espaço de tinta e usado na chamada para o método NearestPoint do objeto de [tinta](/previous-versions/ms836505(v=msdn.10)) do [InkCollector](/previous-versions/ms583683(v=vs.100)).</span><span class="sxs-lookup"><span data-stu-id="a841a-141">The application's handleNearestPoint method creates two points both equal to the cursor's location, one of these points, pt, is converted to ink space and used in the call to the NearestPoint method of the [InkCollector](/previous-versions/ms583683(v=vs.100))'s [Ink](/previous-versions/ms836505(v=msdn.10)) object.</span></span> <span data-ttu-id="a841a-142">O método NearestPoint retorna o objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) mais próximo do ponto e define o parâmetro de saída do índice de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="a841a-142">The NearestPoint method returns the [Stroke](/previous-versions/ms827842(v=msdn.10)) object closest to the point, and sets the floating point index output parameter.</span></span>


```C++
using (Graphics g = CreateGraphics())
{

   // Remeber pen location
    Point inkPenPt = new Point(e.X, e.Y);

    // Convert the pen location into a location in ink space
    ic.Renderer.PixelToInkSpace(g, ref inkPenPt);

    // ...

    float fIndex;
    Stroke stroke = ic.Ink.NearestPoint(inkPenPt, out fIndex);
```



<span data-ttu-id="a841a-143">Se nenhum traço estiver presente, o método NearestPoint retornará **NULL** e o local do cursor será usado como o ponto mais próximo.</span><span class="sxs-lookup"><span data-stu-id="a841a-143">If no strokes are present, the NearestPoint method returns **NULL**, and the cursor location is used as the nearest point.</span></span> <span data-ttu-id="a841a-144">Caso contrário, o local no traço que corresponde ao índice de ponto flutuante será calculado.</span><span class="sxs-lookup"><span data-stu-id="a841a-144">Otherwise, the location on the stroke that corresponds to the floating point index is calculated.</span></span>

<span data-ttu-id="a841a-145">As coordenadas de ponto mais próximo são então convertidas em pixels do espaço de tinta, o método handleNearestPoint, em seguida, invalida a região invalidateRect, calcula uma nova região na qual a linha para o ponto mais próximo é desenhada e invalida também a nova região.</span><span class="sxs-lookup"><span data-stu-id="a841a-145">The nearest point coordinates are then converted to pixels from ink space, The handleNearestPoint method then invalidates the invalidateRect region, calculates a new region the line to the nearest point is drawn in, and invalidates the new region, too.</span></span>

## <a name="closing-the-form"></a><span data-ttu-id="a841a-146">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="a841a-146">Closing the Form</span></span>

<span data-ttu-id="a841a-147">O método Dispose do formulário descarta o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="a841a-147">The form's Dispose method disposes the [InkCollector](/previous-versions/ms583683(v=vs.100)) object.</span></span>

 

 
