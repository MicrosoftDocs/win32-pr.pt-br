---
description: Os demarcadores são formados combinando linhas, retângulos e curvas simples. Lembre-se da Visão geral dos gráficos vetoriais de que os seguintes blocos de construção básicos provaram ser os mais úteis para desenhar imagens.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Caminhos (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f54dae290138314cac3dae8d259591939490764d371e9a2caf9423801e985ec2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "117695472"
---
# <a name="paths-gdi"></a>Caminhos (GDI+)

Os demarcadores são formados combinando linhas, retângulos e curvas simples. Lembre-se da [Visão geral dos gráficos vetoriais](-gdiplus-overview-of-vector-graphics-about.md) de que os seguintes blocos de construção básicos provaram ser os mais úteis para desenhar imagens.

-   Linhas
-   Retângulos
-   Elipses
-   Arcos
-   Polígonos
-   Splines cardinais
-   Splines de Bézier

No Windows GDI+, o [**objeto GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) permite coletar uma sequência desses blocos de construção em uma única unidade. Toda a sequência de linhas, retângulos, polígonos e curvas pode ser desenhada com uma chamada para o método [**Graphics::D rawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) da [**classe Graphics.**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) A ilustração a seguir mostra um demarcador criado pela combinação de uma linha, um arco, uma spline de Bézier e uma spline cardinal.

![ilustração de um caminho que combina uma linha, um arco, um spline de bezier e um spline cardinal](images/aboutgdip02-art14.png)

A [**classe GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) fornece os seguintes métodos para criar uma sequência de itens a serem desenhados: [AddLine,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) [AddRectangle,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)) [AddEllipse,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)) [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (para splines cardinales) e [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)). Cada um desses métodos está sobrecarregado; ou seja, cada método vem em várias variações com listas de parâmetros diferentes. Por exemplo, uma variação do método AddLine recebe quatro inteiros e outra variação do método AddLine recebe dois [**objetos Point.**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point)

Os métodos para adicionar linhas, retângulos e splines Bézier a um caminho têm métodos de complemento plural que adicionam vários itens ao caminho em uma única chamada: [AddLines,](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)) [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))e [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)). Além disso, [o método AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) tem um método de complemento, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), que adiciona uma curva fechada ao caminho.

Para desenhar um caminho, você precisa de [**um objeto Graphics,**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) um [**objeto Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e um [**objeto GraphicsPath.**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) O **objeto Graphics** fornece o [**método Graphics::D rawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) e o objeto **Caneta** armazena atributos do caminho, como largura e cor da linha. O **objeto GraphicsPath** armazena a sequência de linhas, retângulos e curvas que compõe o caminho. Os endereços do **objeto Pen** e do **objeto GraphicsPath** são passados como argumentos para o **método Graphics::D rawPath.** O exemplo a seguir desenha um caminho que consiste em uma linha, uma elipse e um spline Bézier.


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



A ilustração a seguir mostra o demarcador.

![ilustração de um caminho com uma linha, uma elipse e um spline de bezier](images/aboutgdip02-art15.png)

Além de adicionar linhas, retângulos e curvas a um demarcador, você pode adicionar demarcadores a um demarcador. Isso permite combinar os demarcadores existentes para formar demarcadores grandes e complexos. O código a seguir **adiciona graphicsPath1** **e graphicsPath2** **a myGraphicsPath.** O segundo parâmetro do [**método GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) especifica se o caminho adicionado está conectado ao caminho existente.


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



Há dois outros itens que você pode adicionar a um demarcador: cadeias de caracteres e pizzas. Uma pizza é uma parte do interior de uma elipse. O exemplo a seguir cria um caminho de um arco, um spline cardinal, uma cadeia de caracteres e uma pizza.


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



A ilustração a seguir mostra o demarcador. Observe que um demarcador não precisa estar conectado; o arco, spline cardinal, cadeia de caracteres e pizza são separados.

![ilustração de um caminho com linhas desconectadas: um arco, um spline cardinal, uma cadeia de caracteres e uma pizza](images/aboutgdip02-art16.png)

 

 



