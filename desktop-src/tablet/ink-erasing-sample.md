---
description: 'Esse aplicativo se baseia no exemplo de amostra de coleção de tinta demonstrando a exclusão de traços de tinta. O exemplo fornece ao usuário um menu que tem quatro modos para escolher: habilitado para tinta, apagando em Cusp, apagando em interseções e apagando traços.'
ms.assetid: cec912ee-1645-47e1-8988-626719549e55
title: Exemplo de apagamento de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46040781d778f936815e57ba96b4ca516617d9a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104501402"
---
# <a name="ink-erasing-sample"></a><span data-ttu-id="906e6-104">Exemplo de apagamento de tinta</span><span class="sxs-lookup"><span data-stu-id="906e6-104">Ink Erasing Sample</span></span>

<span data-ttu-id="906e6-105">Esse aplicativo se baseia no exemplo de amostra de [coleção de tinta](ink-collection-sample.md) demonstrando a exclusão de traços de tinta.</span><span class="sxs-lookup"><span data-stu-id="906e6-105">This application builds on the [Ink Collection Sample](ink-collection-sample.md) sample by demonstrating ink strokes deletion.</span></span> <span data-ttu-id="906e6-106">O exemplo fornece ao usuário um menu que tem quatro modos para escolher: habilitado para tinta, apagando em Cusp, apagando em interseções e apagando traços.</span><span class="sxs-lookup"><span data-stu-id="906e6-106">The sample provides the user with a menu that has four modes to choose from: ink-enabled, erasing at cusp, erasing at intersections, and erasing strokes.</span></span>

<span data-ttu-id="906e6-107">No modo habilitado para tinta, o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) coleta tinta conforme mostrado no [exemplo de coleção de tinta](ink-collection-sample.md).</span><span class="sxs-lookup"><span data-stu-id="906e6-107">In ink-enabled mode, the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object collects ink as shown in [Ink Collection Sample](ink-collection-sample.md).</span></span>

<span data-ttu-id="906e6-108">Em um modo de apagamento, os segmentos de traços de tinta existentes que o usuário toca com o cursor são apagados.</span><span class="sxs-lookup"><span data-stu-id="906e6-108">In an erasing mode, segments of existing ink strokes that the user touches with the cursor are erased.</span></span> <span data-ttu-id="906e6-109">Além disso, o cusps ou as interseções podem ser marcadas com um círculo vermelho.</span><span class="sxs-lookup"><span data-stu-id="906e6-109">Also, the cusps or intersections may be marked with a red circle.</span></span>

<span data-ttu-id="906e6-110">As partes mais interessantes deste exemplo se encontram no `InkErase` manipulador de eventos do formulário `OnPaint` e nas funções de apagamento que são chamadas do manipulador de eventos do formulário `OnMouseMove` .</span><span class="sxs-lookup"><span data-stu-id="906e6-110">The most interesting parts of this sample lie in the `InkErase` form's `OnPaint` event handler and in the erasing functions that are called from the form's `OnMouseMove` event handler.</span></span>

## <a name="circling-the-cusps-and-intersections"></a><span data-ttu-id="906e6-111">Destacando o Cusps e as interseções</span><span class="sxs-lookup"><span data-stu-id="906e6-111">Circling the Cusps and Intersections</span></span>

<span data-ttu-id="906e6-112">O manipulador de `OnPaint` eventos do formulário primeiro pinta os traços e, dependendo do modo do aplicativo, pode localizar e marcar todas as cusps ou interseções com um pequeno círculo vermelho.</span><span class="sxs-lookup"><span data-stu-id="906e6-112">The form's `OnPaint` event handler first paints the strokes, and depending on the application mode, may find and mark all of the cusps or intersections with a small red circle.</span></span> <span data-ttu-id="906e6-113">Um Cusp marca o ponto em que um traço muda de direção abruptamente.</span><span class="sxs-lookup"><span data-stu-id="906e6-113">A cusp marks the point where a stroke changes direction abruptly.</span></span> <span data-ttu-id="906e6-114">Uma interseção marca um ponto em que um traço faz interseção com ele mesmo ou com outro traço.</span><span class="sxs-lookup"><span data-stu-id="906e6-114">An intersection marks a point where one stroke intersects with itself or another stroke.</span></span>

<span data-ttu-id="906e6-115">O evento de [pintura](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) ocorre sempre que um controle é redesenhado.</span><span class="sxs-lookup"><span data-stu-id="906e6-115">The [Paint](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) event occurs whenever a control is redrawn.</span></span>

> [!Note]  
> <span data-ttu-id="906e6-116">O exemplo força o formulário a ser redesenhado sempre que um traço é apagado ou quando o modo do aplicativo é alterado, usando o método [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) do formulário.</span><span class="sxs-lookup"><span data-stu-id="906e6-116">The sample forces the form to redraw itself whenever a stroke is erased, or when the application mode changes, using the form's [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) method.</span></span>

 


```C++
private void InkErase_OnPaint(object sender, PaintEventArgs e)
{
    Strokes strokesToPaint = myInkCollector.Ink.Strokes;

    myInkCollector.Renderer.Draw(e.Graphics, strokesToPaint);

    switch (mode)
    {
        case ApplicationMode.CuspErase:
            PaintCusps(e.Graphics, strokesToPaint);
            break;
        case ApplicationMode.IntersectErase:
            PaintIntersections(e.Graphics, strokesToPaint);
            break;
    }
}
```



<span data-ttu-id="906e6-117">No `PaintCusps` , o código faz a iteração por cada Cusp em cada traço e desenha um círculo vermelho em torno dele.</span><span class="sxs-lookup"><span data-stu-id="906e6-117">In `PaintCusps`, the code iterates through each cusp in each stroke, and draws a red circle around it.</span></span> <span data-ttu-id="906e6-118">A propriedade [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) do traço retorna os índices dos pontos em um atiçar que correspondem a cusps.</span><span class="sxs-lookup"><span data-stu-id="906e6-118">The stroke's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) property returns the indices of the points within a stoke that correspond to cusps.</span></span> <span data-ttu-id="906e6-119">Além disso, observe o método [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) , que converte o ponto em coordenadas relevantes para o método DrawEllipse.</span><span class="sxs-lookup"><span data-stu-id="906e6-119">Also, note the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) method, which converts the point to coordinates relevant to the DrawEllipse method.</span></span>


```C++
private void PaintCusps(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        int[] cusps = currentStroke.PolylineCusps;

        foreach (int i in cusps)
        {
            Point pt = currentStroke.GetPoint(i);

            // Convert the X, Y position to Window based pixel coordinates
            myInkCollector.Renderer.InkSpaceToPixel(g, ref pt);

            // Draw a red circle as the cusp position
            g.DrawEllipse(Pens.Red, pt.X-3, pt.Y-3, 6, 6);
        }
    }
}
```



<span data-ttu-id="906e6-120">No `PaintIntersections` , o código é iterado em cada traço para localizar suas interseções com o conjunto inteiro de traços.</span><span class="sxs-lookup"><span data-stu-id="906e6-120">In `PaintIntersections`, the code iterates through each stroke to find its intersections with the entire set of strokes.</span></span> <span data-ttu-id="906e6-121">Observe que o método [FindIntersections](/previous-versions/ms827856(v=msdn.10)) do traço é passado como uma coleção [Strokes](/previous-versions/ms827799(v=msdn.10)) e retorna uma matriz de valores de índice de ponto flutuante que representa as interseções.</span><span class="sxs-lookup"><span data-stu-id="906e6-121">Note that the stroke's [FindIntersections](/previous-versions/ms827856(v=msdn.10)) method is passed a [Strokes](/previous-versions/ms827799(v=msdn.10)) collection and returns an array of floating point index values representing the intersections.</span></span> <span data-ttu-id="906e6-122">Em seguida, o código calcula uma coordenada X-Y para cada interseção e desenha um círculo vermelho em torno dele.</span><span class="sxs-lookup"><span data-stu-id="906e6-122">The code then calculates an X-Y coordinate for each intersection, and draws a red circle around it.</span></span>


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a><span data-ttu-id="906e6-123">Manipulando uma caneta que tem duas extremidades</span><span class="sxs-lookup"><span data-stu-id="906e6-123">Handling a Pen That Has Two Ends</span></span>

<span data-ttu-id="906e6-124">Três manipuladores de eventos são definidos para o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) para os eventos [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100))e [Stroke](/previous-versions/ms567622(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="906e6-124">Three event handlers are defined for the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object for the [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100)), and [Stroke](/previous-versions/ms567622(v=vs.100)) events.</span></span> <span data-ttu-id="906e6-125">Cada manipulador de eventos verifica a propriedade [invertida](/previous-versions/ms839525(v=msdn.10)) do objeto [cursor](/previous-versions/ms839521(v=msdn.10)) para ver qual extremidade da caneta está sendo usada.</span><span class="sxs-lookup"><span data-stu-id="906e6-125">Each event handler checks the [Cursor](/previous-versions/ms839521(v=msdn.10)) object's [Inverted](/previous-versions/ms839525(v=msdn.10)) property to see which end of the pen is being used.</span></span> <span data-ttu-id="906e6-126">Quando a caneta é invertida:</span><span class="sxs-lookup"><span data-stu-id="906e6-126">When the pen is inverted:</span></span>

-   <span data-ttu-id="906e6-127">O `myInkCollector_CursorDown` método torna o traço transparente.</span><span class="sxs-lookup"><span data-stu-id="906e6-127">The `myInkCollector_CursorDown` method makes the stroke transparent.</span></span>
-   <span data-ttu-id="906e6-128">O `myInkCollector_NewPackets` método apaga os traços.</span><span class="sxs-lookup"><span data-stu-id="906e6-128">The `myInkCollector_NewPackets` method erases strokes.</span></span>
-   <span data-ttu-id="906e6-129">O `myInkCollector_Stroke` método cancela o evento.</span><span class="sxs-lookup"><span data-stu-id="906e6-129">The `myInkCollector_Stroke` method cancels the event.</span></span> <span data-ttu-id="906e6-130">Os eventos [NewPackets](/previous-versions/ms567621(v=vs.100)) são gerados antes do evento [Stroke](/previous-versions/ms567622(v=vs.100)) .</span><span class="sxs-lookup"><span data-stu-id="906e6-130">[NewPackets](/previous-versions/ms567621(v=vs.100)) events are generated prior to the [Stroke](/previous-versions/ms567622(v=vs.100)) event.</span></span>

## <a name="tracking-the-cursor"></a><span data-ttu-id="906e6-131">Acompanhando o cursor</span><span class="sxs-lookup"><span data-stu-id="906e6-131">Tracking the Cursor</span></span>

<span data-ttu-id="906e6-132">Se o usuário estiver usando uma caneta ou um mouse, os eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) serão gerados.</span><span class="sxs-lookup"><span data-stu-id="906e6-132">Whether the user is using a pen or a mouse, [MouseMove](/previous-versions/ms567617(v=vs.100)) events are generated.</span></span> <span data-ttu-id="906e6-133">O manipulador de eventos MouseMove primeiro verifica para determinar se o modo atual é um modo de apagamento e se qualquer botão do mouse é pressionado e ignora o evento se esses Estados não estiverem presentes.</span><span class="sxs-lookup"><span data-stu-id="906e6-133">The MouseMove event handler first checks to determine whether the current mode is an erase mode and if any mouse button is pressed, and ignores the event if these states are not present.</span></span> <span data-ttu-id="906e6-134">Em seguida, o manipulador de eventos converte as coordenadas de pixel do cursor em coordenadas de espaço de tinta usando o método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) e chama um dos métodos erase do código, dependendo do modo de apagamento atual.</span><span class="sxs-lookup"><span data-stu-id="906e6-134">Then, the event handler converts the pixel coordinates for the cursor into ink space coordinates by using the [Renderer](/previous-versions/ms828481(v=msdn.10)) object's [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) method, and calls one of the code's erase methods depending on the current erase mode.</span></span>

## <a name="erasing-strokes"></a><span data-ttu-id="906e6-135">Apagando traços</span><span class="sxs-lookup"><span data-stu-id="906e6-135">Erasing Strokes</span></span>

<span data-ttu-id="906e6-136">O `EraseStrokes` método usa o local do cursor no espaço de tinta e gera uma coleção de traços que estão dentro de `HitTestRadius` unidades.</span><span class="sxs-lookup"><span data-stu-id="906e6-136">The `EraseStrokes` method takes the cursor's location in ink space and generates a collection of strokes that are within `HitTestRadius` units.</span></span> <span data-ttu-id="906e6-137">O `currentStroke` parâmetro especifica um objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) que não deve ser excluído.</span><span class="sxs-lookup"><span data-stu-id="906e6-137">The `currentStroke` parameter specifies a [Stroke](/previous-versions/ms827842(v=msdn.10)) object that should not be deleted.</span></span> <span data-ttu-id="906e6-138">Em seguida, a coleção Strokes é excluída do coletor e o formulário é redesenhado.</span><span class="sxs-lookup"><span data-stu-id="906e6-138">Then the strokes collection is deleted from the collector, and the form is redrawn.</span></span>


```C++
private void EraseStrokes(Point pt, Stroke currentStroke)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    if (null!=currentStroke && strokesHit.Contains(currentStroke))
    {
        strokesHit.Remove(currentStroke);
    }

    myInkCollector.Ink.DeleteStrokes(strokesHit);

    if (strokesHit.Count > 0)
    {
        this.Refresh();
    }
}
```



## <a name="erasing-at-intersections"></a><span data-ttu-id="906e6-139">Apagando em interseções</span><span class="sxs-lookup"><span data-stu-id="906e6-139">Erasing at Intersections</span></span>

<span data-ttu-id="906e6-140">O `EraseAtIntersections` método itera em cada traço que está dentro do raio de teste e gera uma matriz de interseções entre esse traço e todos os outros traços na coleção.</span><span class="sxs-lookup"><span data-stu-id="906e6-140">The `EraseAtIntersections` method iterates over each stroke that falls within the test radius and generates an array of intersections between that stroke and all the other strokes in the collection.</span></span> <span data-ttu-id="906e6-141">Se nenhuma interseção for encontrada, esse traço inteiro será excluído; caso contrário, o ponto mais próximo no traço para o ponto de teste está localizado e, a partir disso, as interseções em cada lado do ponto estão localizadas, descrevendo o segmento a ser removido.</span><span class="sxs-lookup"><span data-stu-id="906e6-141">If no intersections are found, then that entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="906e6-142">O método [Split](/previous-versions/ms828477(v=msdn.10)) do objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) é usado para separar o segmento do restante do traço e, em seguida, o segmento é excluído, deixando o restante do traço intacto.</span><span class="sxs-lookup"><span data-stu-id="906e6-142">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="906e6-143">Como no `EraseStrokes` , o formulário é redesenhado antes de o método retornar.</span><span class="sxs-lookup"><span data-stu-id="906e6-143">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtIntersections(Point pt)
{
    Strokes strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);

    foreach (Stroke currentStroke in strokesHit)
    {
        float[] intersections = currentStroke.FindIntersections(myInkCollector.Ink.Strokes);
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(intersections[i]);
        ...
    }
    ...
}
```



## <a name="erasing-at-cusps"></a><span data-ttu-id="906e6-144">Apagando em Cusps</span><span class="sxs-lookup"><span data-stu-id="906e6-144">Erasing at Cusps</span></span>

<span data-ttu-id="906e6-145">Para cada traço que está dentro do raio de teste, o `EraseAtCusps` método recupera a matriz de cusps do método [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) do objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) .</span><span class="sxs-lookup"><span data-stu-id="906e6-145">For each stroke that falls within the test radius, the `EraseAtCusps` method retrieves the array of cusps from the [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) method.</span></span> <span data-ttu-id="906e6-146">Cada extremidade do traço também é um Cusp, portanto, se o traço tiver apenas dois cusps, o traço inteiro será excluído; caso contrário, o ponto mais próximo no traço para o ponto de teste está localizado e, a partir disso, as interseções em cada lado do ponto estão localizadas, descrevendo o segmento a ser removido.</span><span class="sxs-lookup"><span data-stu-id="906e6-146">Each end of the stroke is also a cusp, so if the stroke only has two cusps, then the entire stroke is deleted; otherwise, the nearest point on the stroke to the test point is located, and from that, the intersections on either side of the point are located, describing the segment to be removed.</span></span>

<span data-ttu-id="906e6-147">O método [Split](/previous-versions/ms828477(v=msdn.10)) do objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) é usado para separar o segmento do restante do traço e, em seguida, o segmento é excluído, deixando o restante do traço intacto.</span><span class="sxs-lookup"><span data-stu-id="906e6-147">The [Stroke](/previous-versions/ms827842(v=msdn.10)) object's [Split](/previous-versions/ms828477(v=msdn.10)) method is used to separate the segment from the rest of the stroke, and then the segment is deleted, leaving the rest of the stroke intact.</span></span> <span data-ttu-id="906e6-148">Como no `EraseStrokes` , o formulário é redesenhado antes de o método retornar.</span><span class="sxs-lookup"><span data-stu-id="906e6-148">As in `EraseStrokes`, the form is redrawn before the method returns.</span></span>


```C++
private void EraseAtCusps(Point pt)
{
    ...
    strokesHit = myInkCollector.Ink.HitTest(pt, HitTestRadius);
    
    foreach (Stroke currentStroke in strokesHit)
    {
        int[] cusps = currentStroke.PolylineCusps;
        ...
        float findex = currentStroke.NearestPoint(pt);
        ...
        strokeToDelete = currentStroke.Split(cusps[i]); 
        myInkCollector.Ink.DeleteStroke(strokeToDelete);
        ...
    }
    ...
}
```



## <a name="closing-the-form"></a><span data-ttu-id="906e6-149">Fechando o formulário</span><span class="sxs-lookup"><span data-stu-id="906e6-149">Closing the Form</span></span>

<span data-ttu-id="906e6-150">O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .</span><span class="sxs-lookup"><span data-stu-id="906e6-150">The form's [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) method disposes the [InkCollector](/previous-versions/ms836493(v=msdn.10)) object, `myInkCollector`.</span></span>

 

 
