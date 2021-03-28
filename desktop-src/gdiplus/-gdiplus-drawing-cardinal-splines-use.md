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
# <a name="drawing-cardinal-splines"></a><span data-ttu-id="d86b2-103">Desenhando as linhas Cardeal</span><span class="sxs-lookup"><span data-stu-id="d86b2-103">Drawing Cardinal Splines</span></span>

<span data-ttu-id="d86b2-104">Um spline cardinal é uma curva que passa suavemente por um determinado conjunto de pontos.</span><span class="sxs-lookup"><span data-stu-id="d86b2-104">A cardinal spline is a curve that passes smoothly through a given set of points.</span></span> <span data-ttu-id="d86b2-105">Para desenhar uma spline Cardeal, crie um objeto [**gráfico**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e passe o endereço de uma matriz de pontos para o método [**Graphics::D rawcurve**](/previous-versions//ms536070(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d86b2-105">To draw a cardinal spline, create a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object and pass the address of an array of points to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="d86b2-106">O exemplo a seguir desenha uma spline cardeal em forma de sino que passa por cinco pontos designados:</span><span class="sxs-lookup"><span data-stu-id="d86b2-106">The following example draws a bell-shaped cardinal spline that passes through five designated points:</span></span>


```
Point points[] = {Point(0, 100),
                  Point(50, 80),
                  Point(100, 20),
                  Point(150, 80),
                  Point(200, 100)};

Pen pen(Color(255, 0, 0, 255));
graphics.DrawCurve(&pen, points, 5);
```



<span data-ttu-id="d86b2-107">A ilustração a seguir mostra a curva e cinco pontos.</span><span class="sxs-lookup"><span data-stu-id="d86b2-107">The following illustration shows the curve and five points.</span></span>

![ilustração de um spline Cardinal que passa por um conjunto de cinco pontos](images/cardinalspline1.png)

<span data-ttu-id="d86b2-109">Você pode usar o método [**Graphics::D rawclosedcurve**](/previous-versions//ms536143(v=vs.85)) da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) para desenhar uma spline Cardeal fechada.</span><span class="sxs-lookup"><span data-stu-id="d86b2-109">You can use the [**Graphics::DrawClosedCurve**](/previous-versions//ms536143(v=vs.85)) method of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class to draw a closed cardinal spline.</span></span> <span data-ttu-id="d86b2-110">Em um spline cardinal fechado, a curva continua durante o último ponto na matriz e se conecta com o primeiro ponto na matriz.</span><span class="sxs-lookup"><span data-stu-id="d86b2-110">In a closed cardinal spline, the curve continues through the last point in the array and connects with the first point in the array.</span></span>

<span data-ttu-id="d86b2-111">O exemplo a seguir desenha um spline cardinal fechado que passa por seis pontos designados.</span><span class="sxs-lookup"><span data-stu-id="d86b2-111">The following example draws a closed cardinal spline that passes through six designated points.</span></span>


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



<span data-ttu-id="d86b2-112">A ilustração a seguir mostra o spline fechado junto com os seis pontos:</span><span class="sxs-lookup"><span data-stu-id="d86b2-112">The following illustration shows the closed spline along with the six points:</span></span>

![ilustração de uma spline Cardeal fechada que passa por um conjunto de seis pontos](images/cardinalspline1a.png)

<span data-ttu-id="d86b2-114">Você pode alterar o modo como um spline Cardeal se curva passando um argumento de tensão para o método [**Graphics::D rawcurve**](/previous-versions//ms536070(v=vs.85)) .</span><span class="sxs-lookup"><span data-stu-id="d86b2-114">You can change the way a cardinal spline bends by passing a tension argument to the [**Graphics::DrawCurve**](/previous-versions//ms536070(v=vs.85)) method.</span></span> <span data-ttu-id="d86b2-115">O exemplo a seguir desenha três linhas cardeal que passam pelo mesmo conjunto de pontos:</span><span class="sxs-lookup"><span data-stu-id="d86b2-115">The following example draws three cardinal splines that pass through the same set of points:</span></span>


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



<span data-ttu-id="d86b2-116">A ilustração a seguir mostra os três splines junto com seus valores de tensão.</span><span class="sxs-lookup"><span data-stu-id="d86b2-116">The following illustration shows the three splines along with their tension values.</span></span> <span data-ttu-id="d86b2-117">Observe que, quando a tensão for 0, os pontos são conectados por linhas retas.</span><span class="sxs-lookup"><span data-stu-id="d86b2-117">Note that when the tension is 0, the points are connected by straight lines.</span></span>

![ilustração de três casas cardeal que passam pelo mesmo conjunto de pontos, mas em tensãos diferentes](images/cardinalspline2.png)

 

 
