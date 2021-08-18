---
description: Um spline cardinal é uma curva que passa suavemente por um determinado conjunto de pontos.
ms.assetid: 0bb84f55-18d0-4a4c-bc5b-7803aa807954
title: Desenhando splines cardinais
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f9124e27254fc77135d265d9bab98d2332c02d345e60add1fcd96fc68c814df
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119036814"
---
# <a name="drawing-cardinal-splines"></a>Desenhando splines cardinais

Um spline cardinal é uma curva que passa suavemente por um determinado conjunto de pontos. Para desenhar um spline cardinal, crie um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passe o endereço de uma matriz de pontos para o [**método Graphics::D rawCurve.**](/previous-versions//ms536070(v=vs.85)) O exemplo a seguir desenha um spline cardinal em forma de sino que passa por cinco pontos designados:


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

![ilustração de um spline cardinal que passa por um conjunto de cinco pontos](images/cardinalspline1.png)

Você pode usar [**o método Graphics::D rawClosedCurve**](/previous-versions//ms536143(v=vs.85)) da [**classe Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar um spline cardinal fechado. Em um spline cardinal fechado, a curva continua durante o último ponto na matriz e se conecta com o primeiro ponto na matriz.

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

![ilustração de um spline cardinal fechado que passa por um conjunto de seis pontos](images/cardinalspline1a.png)

Você pode alterar a maneira como um spline cardinal se inclina passando um argumento de tensão para o [**método Graphics::D rawCurve.**](/previous-versions//ms536070(v=vs.85)) O exemplo a seguir desenha três splines cardinais que passam pelo mesmo conjunto de pontos:


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

![ilustração de três splines cardinais passando pelo mesmo conjunto de pontos, mas em diferentes tensão](images/cardinalspline2.png)

 

 
