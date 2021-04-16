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
# <a name="ink-erasing-sample"></a>Exemplo de apagamento de tinta

Esse aplicativo se baseia no exemplo de amostra de [coleção de tinta](ink-collection-sample.md) demonstrando a exclusão de traços de tinta. O exemplo fornece ao usuário um menu que tem quatro modos para escolher: habilitado para tinta, apagando em Cusp, apagando em interseções e apagando traços.

No modo habilitado para tinta, o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) coleta tinta conforme mostrado no [exemplo de coleção de tinta](ink-collection-sample.md).

Em um modo de apagamento, os segmentos de traços de tinta existentes que o usuário toca com o cursor são apagados. Além disso, o cusps ou as interseções podem ser marcadas com um círculo vermelho.

As partes mais interessantes deste exemplo se encontram no `InkErase` manipulador de eventos do formulário `OnPaint` e nas funções de apagamento que são chamadas do manipulador de eventos do formulário `OnMouseMove` .

## <a name="circling-the-cusps-and-intersections"></a>Destacando o Cusps e as interseções

O manipulador de `OnPaint` eventos do formulário primeiro pinta os traços e, dependendo do modo do aplicativo, pode localizar e marcar todas as cusps ou interseções com um pequeno círculo vermelho. Um Cusp marca o ponto em que um traço muda de direção abruptamente. Uma interseção marca um ponto em que um traço faz interseção com ele mesmo ou com outro traço.

O evento de [pintura](/dotnet/api/system.windows.forms.control.paint?view=netcore-3.1) ocorre sempre que um controle é redesenhado.

> [!Note]  
> O exemplo força o formulário a ser redesenhado sempre que um traço é apagado ou quando o modo do aplicativo é alterado, usando o método [Refresh](/dotnet/api/system.windows.forms.control.refresh?view=netcore-3.1) do formulário.

 


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



No `PaintCusps` , o código faz a iteração por cada Cusp em cada traço e desenha um círculo vermelho em torno dele. A propriedade [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) do traço retorna os índices dos pontos em um atiçar que correspondem a cusps. Além disso, observe o método [InkSpaceToPixel](/previous-versions/ms828495(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) , que converte o ponto em coordenadas relevantes para o método DrawEllipse.


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



No `PaintIntersections` , o código é iterado em cada traço para localizar suas interseções com o conjunto inteiro de traços. Observe que o método [FindIntersections](/previous-versions/ms827856(v=msdn.10)) do traço é passado como uma coleção [Strokes](/previous-versions/ms827799(v=msdn.10)) e retorna uma matriz de valores de índice de ponto flutuante que representa as interseções. Em seguida, o código calcula uma coordenada X-Y para cada interseção e desenha um círculo vermelho em torno dele.


```C++
private void PaintIntersections(Graphics g, Strokes strokesToPaint)
{
    foreach (Stroke currentStroke in strokesToPaint)
    {
        float[] intersections =            currentStroke.FindIntersections(strokesToPaint);
    }
}
```



## <a name="handling-a-pen-that-has-two-ends"></a>Manipulando uma caneta que tem duas extremidades

Três manipuladores de eventos são definidos para o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) para os eventos [CursorDown](/previous-versions/ms567611(v=vs.100)), [NewPackets](/previous-versions/ms567621(v=vs.100))e [Stroke](/previous-versions/ms567622(v=vs.100)) . Cada manipulador de eventos verifica a propriedade [invertida](/previous-versions/ms839525(v=msdn.10)) do objeto [cursor](/previous-versions/ms839521(v=msdn.10)) para ver qual extremidade da caneta está sendo usada. Quando a caneta é invertida:

-   O `myInkCollector_CursorDown` método torna o traço transparente.
-   O `myInkCollector_NewPackets` método apaga os traços.
-   O `myInkCollector_Stroke` método cancela o evento. Os eventos [NewPackets](/previous-versions/ms567621(v=vs.100)) são gerados antes do evento [Stroke](/previous-versions/ms567622(v=vs.100)) .

## <a name="tracking-the-cursor"></a>Acompanhando o cursor

Se o usuário estiver usando uma caneta ou um mouse, os eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) serão gerados. O manipulador de eventos MouseMove primeiro verifica para determinar se o modo atual é um modo de apagamento e se qualquer botão do mouse é pressionado e ignora o evento se esses Estados não estiverem presentes. Em seguida, o manipulador de eventos converte as coordenadas de pixel do cursor em coordenadas de espaço de tinta usando o método [PixelToInkSpace](/previous-versions/ms828505(v=msdn.10)) do objeto [Renderer](/previous-versions/ms828481(v=msdn.10)) e chama um dos métodos erase do código, dependendo do modo de apagamento atual.

## <a name="erasing-strokes"></a>Apagando traços

O `EraseStrokes` método usa o local do cursor no espaço de tinta e gera uma coleção de traços que estão dentro de `HitTestRadius` unidades. O `currentStroke` parâmetro especifica um objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) que não deve ser excluído. Em seguida, a coleção Strokes é excluída do coletor e o formulário é redesenhado.


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



## <a name="erasing-at-intersections"></a>Apagando em interseções

O `EraseAtIntersections` método itera em cada traço que está dentro do raio de teste e gera uma matriz de interseções entre esse traço e todos os outros traços na coleção. Se nenhuma interseção for encontrada, esse traço inteiro será excluído; caso contrário, o ponto mais próximo no traço para o ponto de teste está localizado e, a partir disso, as interseções em cada lado do ponto estão localizadas, descrevendo o segmento a ser removido.

O método [Split](/previous-versions/ms828477(v=msdn.10)) do objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) é usado para separar o segmento do restante do traço e, em seguida, o segmento é excluído, deixando o restante do traço intacto. Como no `EraseStrokes` , o formulário é redesenhado antes de o método retornar.


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



## <a name="erasing-at-cusps"></a>Apagando em Cusps

Para cada traço que está dentro do raio de teste, o `EraseAtCusps` método recupera a matriz de cusps do método [PolylineCusps](/previous-versions/ms827853(v=msdn.10)) do objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) . Cada extremidade do traço também é um Cusp, portanto, se o traço tiver apenas dois cusps, o traço inteiro será excluído; caso contrário, o ponto mais próximo no traço para o ponto de teste está localizado e, a partir disso, as interseções em cada lado do ponto estão localizadas, descrevendo o segmento a ser removido.

O método [Split](/previous-versions/ms828477(v=msdn.10)) do objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) é usado para separar o segmento do restante do traço e, em seguida, o segmento é excluído, deixando o restante do traço intacto. Como no `EraseStrokes` , o formulário é redesenhado antes de o método retornar.


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



## <a name="closing-the-form"></a>Fechando o formulário

O método [Dispose](/dotnet/api/system.windows.forms.form.dispose?view=netcore-3.1) do formulário descarta o objeto [InkCollector](/previous-versions/ms836493(v=msdn.10)) , `myInkCollector` .

 

 
