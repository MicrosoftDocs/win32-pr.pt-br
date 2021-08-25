---
description: Este exemplo ilustra dois métodos para localizar tinta, considerando um local de tela.
ms.assetid: fc581da4-0a7b-4c31-8f73-0784066fcc56
title: Amostra de teste de acerto de tinta
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 995bd6f14b4a0a014452ae9392fa744ab93f01f9047c79e5dc30652c243473db
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119713076"
---
# <a name="ink-hit-test-sample"></a>Amostra de teste de acerto de tinta

Este exemplo ilustra dois métodos para localizar tinta, considerando um local de tela.

Os seguintes recursos são usados neste exemplo:

-   Usando um coletor de tinta
-   Executando um teste de acerto
-   Localizando o ponto mais próximo

## <a name="accessing-the-ink-api"></a>Acessando a API de Tinta

Primeiro, consulte as classes de tablet pc, localizadas no Windows Vista ou Windows SDK (Software Development Kit) do PC Edition do XP.


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>Manipulando a carga de formulário e Paint eventos

Manipulador de eventos Load do formulário:

-   Cria um [objeto InkCollector,](/previous-versions/ms583683(v=vs.100)) ic, para o formulário.
-   Define a propriedade [CollectionMode](/previous-versions/ms836497(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para ignorar gestos.
-   Habilita [o InkCollector.](/previous-versions/ms583683(v=vs.100))
-   Define a propriedade [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) como **TRUE.**


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



O manipulador de eventos Paint formulário verifica o modo do aplicativo:

-   No modo HitTest, ele pinta um círculo em torno do cursor. A caneta ativa é definida no método handleHitTest do aplicativo.
-   No modo NearestPoint, ele pinta uma linha vermelha entre o cursor e o ponto mais próximo do cursor. O ponto mais próximo é calculado no método handleNe guidPoint do aplicativo.


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



Este exemplo tem um algoritmo de repinção muito simples. Com sua [propriedade AutoRedraw](/previous-versions/ms836495(v=msdn.10)) definida como **TRUE,** o coletor de tinta é reintgido quando o formulário é redesenhado. Para simplificar o redesenho do formulário, o aplicativo rastreia uma caixa delimitador, a variável membro invalidateRect, para a área em que a pintura é adicionada, que é invalidada sempre que o formulário é redesenhado.

## <a name="handling-menu-events"></a>Manipulando eventos de menu

O comando Exit desabilita o [InkCollector](/previous-versions/ms583683(v=vs.100)) antes de sair do aplicativo.

O comando Ink atualiza o modo de aplicativo e o status do menu, habilita o coletor de tinta e invalida a região pintada anteriormente do formulário.

Os comandos Teste de Clique e Ponto Mais Próximo alteram o cursor, atualizem o modo de aplicativo e o status do menu, desabilitem o coletor de tinta e invalidem a região pintada anteriormente do formulário.

O Clear! O comando desabilita [o InkCollector](/previous-versions/ms583683(v=vs.100)) ao substituir [](/previous-versions/ms836505(v=msdn.10)) a propriedade Ink do objeto InkCollector por um novo objeto [Ink,](/previous-versions/ms571716(v=vs.100)) gera um evento de comando Ink e força uma atualização no controle.

## <a name="handling-mouse-events"></a>Manipulando eventos do mouse

O [manipulador de eventos MouseMove](/previous-versions/ms567617(v=vs.100)) verifica o modo do aplicativo:

-   No modo tinta, ele não faz nada, permitindo que a tinta seja coletada normalmente pelo coletor de tinta.
-   No modo HitTest, ele envia os argumentos de evento para o método handleHitTest do aplicativo.
-   No modo NearestPoint, ele envia os argumentos de evento para o método handleNe operaçãopoint do aplicativo.

## <a name="performing-a-hit-test"></a>Executando um teste de acerto

O método handleHitTest do aplicativo cria dois pontos, o local do cursor e um ponto Pixels HitSize distantes do cursor e, em seguida, converte esses dois pontos de pixels em coordenadas de espaço em tinta.


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



Em seguida, [o objeto InkCollector](/previous-versions/ms583683(v=vs.100)) usa o [método Microsoft.Ink.Ink.HitTest()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para encontrar quaisquer traços que estão dentro de pt3. X – pt2. X unidades de espaço em tinta do cursor, pt2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



Em seguida, o método handleHitTest define a cor da caneta com base em se os traços foram encontrados, invalida a região invalidateRect, calcula uma nova região em que o círculo de teste de acerto é desenhado e invalida a nova região.

## <a name="locating-the-nearest-point"></a>Localizando o ponto mais próximo

O método handleNectorPoint do aplicativo cria dois pontos iguais ao local do cursor, um desses pontos, pt, é convertido em espaço de tinta e usado na chamada para o método NearestPoint do objeto [InkCollector's](/previous-versions/ms583683(v=vs.100)) [Ink.](/previous-versions/ms836505(v=msdn.10)) O método NearestPoint retorna o [objeto Stroke](/previous-versions/ms827842(v=msdn.10)) mais próximo do ponto e define o parâmetro de saída do índice de ponto flutuante.


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



Se nenhum traço estiver presente, o método NearestPoint retornará **NULL** e o local do cursor será usado como o ponto mais próximo. Caso contrário, o local no traço que corresponde ao índice de ponto flutuante será calculado.

Em seguida, as coordenadas de ponto mais próximas são convertidas em pixels do espaço de tinta. O método handleNeegerPoint invalida a região invalidateRect, calcula uma nova região em que a linha para o ponto mais próximo é desenhada e invalida a nova região também.

## <a name="closing-the-form"></a>Fechando o formulário

O método Dispose do formulário descarta o [objeto InkCollector.](/previous-versions/ms583683(v=vs.100))

 

 
