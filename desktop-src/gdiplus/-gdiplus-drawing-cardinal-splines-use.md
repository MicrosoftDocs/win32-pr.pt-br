---
description: Um spline cardinal é uma curva que passa suavemente por um determinado conjunto de pontos.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Desenhando as linhas Cardeal
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c780cb4486f579acb57170a8eda4fd187a421ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104563382"
---
# <a name="drawing-cardinal-splines"></a>Desenhando as linhas Cardeal

Um spline cardinal é uma curva que passa suavemente por um determinado conjunto de pontos. Para desenhar uma spline Cardeal, crie um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passe o endereço de uma matriz de pontos para o método [**Graphics::D rawcurve**](/previous-versions//ms536070(v=vs.85)) . O exemplo a seguir desenha uma spline cardeal em forma de sino que passa por cinco pontos designados:


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



A ilustração a seguir mostra a curva e cinco pontos.

![ilustração de um spline Cardinal que passa por um conjunto de cinco pontos](images/cardinalspline1.png)

Você pode usar o método [**Graphics::D rawclosedcurve**](/previous-versions//ms536143(v=vs.85)) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar uma spline Cardeal fechada. Em um spline cardinal fechado, a curva continua durante o último ponto na matriz e se conecta com o primeiro ponto na matriz.

O exemplo a seguir desenha um spline cardinal fechado que passa por seis pontos designados.


```
Point points[] = {Point(60, 60),
   Point(150, 80),
   Point(200, 40),
   Point(180, 120),
   Point(120, 100),
   Point(80, 160)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawClosedCurve(&pen, points, 6);
```



A ilustração a seguir mostra o spline fechado junto com os seis pontos:

![ilustração de uma spline Cardeal fechada que passa por um conjunto de seis pontos](images/cardinalspline1a.png)

Você pode alterar o modo como um spline Cardeal se curva passando um argumento de tensão para o método [**Graphics::D rawcurve**](/previous-versions//ms536070(v=vs.85)) . O exemplo a seguir desenha três linhas cardeal que passam pelo mesmo conjunto de pontos:


```
Point points[] = {Point(20, 50),
                  Point(100, 10),
                  Point(200, 100),
                  Point(300, 50),
                  Point(400, 80)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5, 0.0f);  // tension 0.0
graphics.DrawCurve(&pen, points, 5, 0.6f);  // tension 0.6
graphics.DrawCurve(&pen, points, 5, 1.0f);  // tension 1.0
```



A ilustração a seguir mostra os três splines junto com seus valores de tensão. Observe que, quando a tensão for 0, os pontos são conectados por linhas retas.

![ilustração de três casas cardeal que passam pelo mesmo conjunto de pontos, mas em tensãos diferentes](images/cardinalspline2.png)

 

 
