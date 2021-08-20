---
description: Para criar um caminho, construa um objeto GraphicsPath e, em seguida, chame métodos, como AddLine e AddCurve, para adicionar primitivos ao caminho.
ms.assetid: 66faeb73-16fb-4b7f-a4d5-a90ec2590d8c
title: Criar figuras usando linhas, curvas e formas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cd2c0d2914eb1edb740d7a9bca6a8b521aed6a0443b6dcd1ee92c68326f748af
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "118067603"
---
# <a name="creating-figures-from-lines-curves-and-shapes"></a>Criar figuras usando linhas, curvas e formas

Para criar um caminho, construa um objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) e, em seguida, chame métodos, como [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)) e [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)), para adicionar primitivos ao caminho.

O exemplo a seguir cria um caminho que tem um único arco. O arco tem um ângulo de flecha de – 180 graus, que é no sentido anti-horário no sistema de coordenadas padrão.


```
Pen pen(Color(255, 255, 0, 0));
GraphicsPath path;
path.AddArc(175, 50, 50, 50, 0, -180);
graphics.DrawPath(&pen, &path);
```



O exemplo a seguir cria um caminho que tem duas figuras. A primeira figura é um arco seguido por uma linha. A segunda figura é uma linha seguida por uma curva, seguida por uma linha. A primeira figura foi deixada aberta e a segunda figura está fechada.


```
Point points[] = {Point(40, 60), Point(50, 70), Point(30, 90)};

Pen pen(Color(255, 255, 0, 0), 2);
GraphicsPath path;

// The first figure is started automatically, so there is
// no need to call StartFigure here.
path.AddArc(175, 50, 50, 50, 0.0f, -180.0f);
path.AddLine(100, 0, 250, 20);

path.StartFigure();
path.AddLine(50, 20, 5, 90);
path.AddCurve(points, 3);
path.AddLine(50, 150, 150, 180);
path.CloseFigure();

graphics.DrawPath(&pen, &path);
```



Além de adicionar linhas e curvas a caminhos, você pode adicionar formas fechadas: retângulos, elipses, tortas e polígonos. O exemplo a seguir cria um caminho que tem duas linhas, um retângulo e uma elipse. O código usa uma caneta para desenhar o caminho e um pincel para preencher o caminho.


```
GraphicsPath path;
Pen          pen(Color(255, 255, 0, 0), 2);
SolidBrush   brush(Color(255, 0, 0, 200));

path.AddLine(10, 10, 100, 40);
path.AddLine(100, 60, 30, 60);
path.AddRectangle(Rect(50, 35, 20, 40));
path.AddEllipse(10, 75, 40, 30);

graphics.DrawPath(&pen, &path);
graphics.FillPath(&brush, &path);
```



O caminho no exemplo anterior tem três figuras. A primeira figura consiste nas duas linhas, a segunda figura consiste no retângulo e a terceira figura consiste na elipse. Mesmo quando não há chamadas para [**GraphicsPath:: CloseFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-closefigure) ou [**GraphicsPath:: StartFigure**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-startfigure), as formas intrinsecamente fechadas, como retângulos e reticências, são consideradas figuras separadas.

 

 



