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
# <a name="drawing-bezier-splines"></a><span data-ttu-id="48e42-103">Desenho de linhas de Bézier</span><span class="sxs-lookup"><span data-stu-id="48e42-103">Drawing Bezier Splines</span></span>

<span data-ttu-id="48e42-104">Uma spline de Bézier é definida por quatro pontos: um ponto de partida, dois pontos de controle e um ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="48e42-104">A Bézier spline is defined by four points: a start point, two control points, and an end point.</span></span> <span data-ttu-id="48e42-105">O exemplo a seguir desenha um spline Bézier com ponto inicial (10, 100) e ponto final (200, 100).</span><span class="sxs-lookup"><span data-stu-id="48e42-105">The following example draws a Bézier spline with start point (10, 100) and end point (200, 100).</span></span> <span data-ttu-id="48e42-106">Os pontos de controle são (100, 10) e (150, 150):</span><span class="sxs-lookup"><span data-stu-id="48e42-106">The control points are (100, 10) and (150, 150):</span></span>


```
Point p1(10, 100);   // start point
Point c1(100, 10);   // first control point
Point c2(150, 150);  // second control point
Point p2(200, 100);  // end point
Pen pen(Color(255, 0, 0, 255));
graphics.DrawBezier(&pen, p1, c1, c2, p2);
```



<span data-ttu-id="48e42-107">A ilustração a seguir mostra o spline Bézier resultante junto com seu ponto de partida, pontos de controle e ponto de extremidade.</span><span class="sxs-lookup"><span data-stu-id="48e42-107">The following illustration shows the resulting Bézier spline along with its start point, control points, and end point.</span></span> <span data-ttu-id="48e42-108">A ilustração também mostra o convexa envoltória da spline, que é um polígono formado pela conexão dos quatro pontos com linhas retas.</span><span class="sxs-lookup"><span data-stu-id="48e42-108">The illustration also shows the spline's convex hull, which is a polygon formed by connecting the four points with straight lines.</span></span>

![ilustração mostrando um spline de Bézier com dois pontos de extremidade e dois pontos de controle](images/bezierspline1.png)

<span data-ttu-id="48e42-110">Você pode usar o método [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar uma sequência de linhas de Bézier conectadas.</span><span class="sxs-lookup"><span data-stu-id="48e42-110">You can use the [DrawBeziers](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawbeziers(inconstpen_inconstpoint_inint)) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a sequence of connected Bézier splines.</span></span> <span data-ttu-id="48e42-111">O exemplo a seguir desenha uma curva que consiste em duas linhas de Bézier conectadas.</span><span class="sxs-lookup"><span data-stu-id="48e42-111">The following example draws a curve that consists of two connected Bézier splines.</span></span> <span data-ttu-id="48e42-112">O ponto final da primeira spline Bézier é o ponto inicial da segunda spline Bézier.</span><span class="sxs-lookup"><span data-stu-id="48e42-112">The end point of the first Bézier spline is the start point of the second Bézier spline.</span></span>


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



<span data-ttu-id="48e42-113">A ilustração a seguir mostra as próprias linhas conectadas junto com os sete pontos.</span><span class="sxs-lookup"><span data-stu-id="48e42-113">The following illustration shows the connected splines along with the seven points.</span></span>

![ilustração mostrando pontos de extremidade e pontos de controle de duas linhas que compartilham um dos pontos de extremidade](images/bezierspline2.png)

 

 



