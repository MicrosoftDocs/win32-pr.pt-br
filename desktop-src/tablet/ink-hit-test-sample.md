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
# <a name="ink-hit-test-sample"></a>Exemplo de teste de colisão de tinta

Este exemplo ilustra dois métodos para encontrar tinta, dado um local de tela.

Os recursos a seguir são usados neste exemplo:

-   Usando um coletor de tinta
-   Executando um teste de clique
-   Localizando o ponto mais próximo

## <a name="accessing-the-ink-api"></a>Acessando a API de tinta

Primeiro, referencie as classes do Tablet PC, localizadas no SDK (Software Development Kit) do Windows Vista ou do Windows XP Tablet PC Edition.


```C++
using Microsoft.Ink;
```



## <a name="handling-form-load-and-paint-events"></a>Manipulando eventos de carga e de pintura de formulário

O manipulador de eventos Load do formulário:

-   Cria um objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) , IC, para o formulário.
-   Define a propriedade [CollectionMode](/previous-versions/ms836497(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) para ignorar gestos.
-   Habilita o [InkCollector](/previous-versions/ms583683(v=vs.100)).
-   Define a propriedade [redesenhar](/previous-versions/ms836495(v=msdn.10)) do objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) como **true**.


```C++
// Create the InkCollector, and turn it on
ic = new InkCollector(Handle);  // attach it to the form's frame window

// default to ink-enabled mode
mode = ApplicationMode.Ink;
ic.CollectionMode = CollectionMode.InkOnly;

// turn the collector on
ic.Enabled = true;ic.AutoRedraw = true;
```



O manipulador de eventos de pintura do formulário verifica o modo do aplicativo:

-   No modo HitTest, ele pinta um círculo em volta do cursor. A caneta ativa é definida no método handleHitTest do aplicativo.
-   No modo NearestPoint, ele pinta uma linha vermelha entre o cursor e o ponto próximo ao cursor. O ponto mais próximo é calculado no método handleNearestPoint do aplicativo.


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



Este exemplo tem um algoritmo redesenhado muito direto. Com sua propriedade [AutoRedraw](/previous-versions/ms836495(v=msdn.10)) definida como **true**, o coletor de tinta redesenha a si mesmo quando o formulário é redesenhado. Para simplificar o redesenho do formulário, o aplicativo rastreia uma caixa delimitadora, a variável de membro invalidateRect, para a área em que o Paint é adicionado, o que é invalidado sempre que o formulário é redesenhado.

## <a name="handling-menu-events"></a>Manipulando eventos de menu

O comando exit desabilita o [InkCollector](/previous-versions/ms583683(v=vs.100)) antes de sair do aplicativo.

O comando de tinta atualiza o modo de aplicativo e o status do menu, habilita o coletor de tinta e invalida a região pintada anteriormente do formulário.

Os comandos de teste de clique e de ponto mais próximo alteram o cursor, atualizam o modo de aplicativo e o status do menu, desabilitam o coletor de tinta e invalidam a região pintada anteriormente do formulário.

O claro! o comando desabilita o [InkCollector](/previous-versions/ms583683(v=vs.100)) ao substituir a propriedade [Ink](/previous-versions/ms836505(v=msdn.10)) do objeto InkCollector por um novo objeto de [tinta](/previous-versions/ms571716(v=vs.100)) , gera um evento de comando de tinta e força uma atualização no controle.

## <a name="handling-mouse-events"></a>Manipulando eventos do mouse

O manipulador de eventos [MouseMove](/previous-versions/ms567617(v=vs.100)) verifica o modo do aplicativo:

-   No modo de tinta, ele não faz nada, permitindo que a tinta seja coletada normalmente pelo coletor de tinta.
-   No modo HitTest, ele envia os argumentos do evento para o método handleHitTest do aplicativo.
-   No modo NearestPoint, ele envia os argumentos do evento para o método handleNearestPoint do aplicativo.

## <a name="performing-a-hit-test"></a>Executando um teste de clique

O método handleHitTest do aplicativo cria dois pontos, o local do cursor e um ponto atinge os pixels distantes do cursor e, em seguida, converte esses dois pontos de pixels em coordenadas de espaço de tinta.


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



Em seguida, o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) usa o método [Microsoft. Ink. Ink. HitTest ()](/previous-versions/dotnet/netframework-3.5/ms571330(v=vs.90)) para localizar os traços que estão dentro de PT3. X-PT2. X unidades de espaço de tinta do cursor, PT2.


```C++
Strokes strokes = ic.Ink.HitTest(pt2, (float)(pt3.X - pt2.X));
```



Em seguida, o método handleHitTest define a cor da caneta com base em se os traços foram encontrados, invalida a região invalidateRect, calcula uma nova região em que o círculo do teste de clique é desenhado e, em seguida, invalida a nova região.

## <a name="locating-the-nearest-point"></a>Localizando o ponto mais próximo

O método handleNearestPoint do aplicativo cria dois pontos iguais ao local do cursor, um desses pontos, pt, é convertido em espaço de tinta e usado na chamada para o método NearestPoint do objeto de [tinta](/previous-versions/ms836505(v=msdn.10)) do [InkCollector](/previous-versions/ms583683(v=vs.100)). O método NearestPoint retorna o objeto [Stroke](/previous-versions/ms827842(v=msdn.10)) mais próximo do ponto e define o parâmetro de saída do índice de ponto flutuante.


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

As coordenadas de ponto mais próximo são então convertidas em pixels do espaço de tinta, o método handleNearestPoint, em seguida, invalida a região invalidateRect, calcula uma nova região na qual a linha para o ponto mais próximo é desenhada e invalida também a nova região.

## <a name="closing-the-form"></a>Fechando o formulário

O método Dispose do formulário descarta o objeto [InkCollector](/previous-versions/ms583683(v=vs.100)) .

 

 
