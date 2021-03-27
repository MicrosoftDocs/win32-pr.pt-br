---
description: 'Um B&\# 233; o spline zier é definido por quatro pontos: um ponto de partida, dois pontos de controle e um ponto de extremidade.'
ms.assetid: af19e82b-0d13-4fb0-981e-8d5dd1bbfb36
title: Desenho de linhas de Bézier
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5ea97d25f482372c387239e8f9083b31e3b2d912
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103661935"
---
# <a name="drawing-bezier-splines"></a>Desenho de linhas de Bézier

Uma spline de Bézier é definida por quatro pontos: um ponto de partida, dois pontos de controle e um ponto de extremidade. O exemplo a seguir desenha um spline Bézier com ponto inicial (10, 100) e ponto final (200, 100). Os pontos de controle são (100, 10) e (150, 150):


```
Point p1(10, 100);   // start point
Point c1(100, 10);   // first control point
Point c2(150, 150);  // second control point
Point p2(200, 100);  // end point
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBezier(&pen, p1, c1, c2, p2);
```



A ilustração a seguir mostra o spline Bézier resultante junto com seu ponto de partida, pontos de controle e ponto de extremidade. A ilustração também mostra o convexa envoltória da spline, que é um polígono formado pela conexão dos quatro pontos com linhas retas.

![ilustração mostrando um spline de Bézier com dois pontos de extremidade e dois pontos de controle](images/bezierspline1.png)

Você pode usar o método [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar uma sequência de linhas de Bézier conectadas. O exemplo a seguir desenha uma curva que consiste em duas linhas de Bézier conectadas. O ponto final da primeira spline Bézier é o ponto inicial da segunda spline Bézier.


```
Point p[] = {
   Point(10, 100),   // start point of first spline
   Point(75, 10),    // first control point of first spline
   Point(80, 50),    // second control point of first spline
   Point(100, 150),  // end point of first spline and 
                     // start point of second spline
   Point(125, 80),   // first control point of second spline
   Point(175, 200),  // second control point of second spline
   Point(200, 80)};  // end point of second spline
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBeziers(&pen, p, 7);
```



A ilustração a seguir mostra as próprias linhas conectadas junto com os sete pontos.

![ilustração mostrando pontos de extremidade e pontos de controle de duas linhas que compartilham um dos pontos de extremidade](images/bezierspline2.png)

 

 



