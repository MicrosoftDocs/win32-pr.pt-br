---
description: 'O GDI+ dá suporte a vários tipos de curvas: reticências, arcos, Cardeal Cardinals e B&\# 233; ziers de linha.'
ms.assetid: 97a1342c-4edb-4671-b36d-b6992efad498
title: Construindo e desenhando curvas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f61c1aa12e3152ed65cca2da6911d2d53def81b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104988890"
---
# <a name="constructing-and-drawing-curves"></a><span data-ttu-id="91376-103">Construindo e desenhando curvas</span><span class="sxs-lookup"><span data-stu-id="91376-103">Constructing and Drawing Curves</span></span>

<span data-ttu-id="91376-104">O GDI+ dá suporte a vários tipos de curvas: elipses, arcos, polilinhas cardeal e linhas de Bézier.</span><span class="sxs-lookup"><span data-stu-id="91376-104">GDI+ supports several types of curves: ellipses, arcs, cardinal splines, and Bézier splines.</span></span> <span data-ttu-id="91376-105">Uma elipse é definida por seu retângulo delimitador; um arco é uma parte de uma elipse definida por um ângulo inicial e um ângulo de flecha.</span><span class="sxs-lookup"><span data-stu-id="91376-105">An ellipse is defined by its bounding rectangle; an arc is a portion of an ellipse defined by a starting angle and a sweep angle.</span></span> <span data-ttu-id="91376-106">Um spline cardinal é definido por uma matriz de pontos e um parâmetro de tensão – a curva passa suavemente por cada ponto na matriz e o parâmetro de tensão influencia a maneira como a curva se dobra.</span><span class="sxs-lookup"><span data-stu-id="91376-106">A cardinal spline is defined by an array of points and a tension parameter — the curve passes smoothly through each point in the array, and the tension parameter influences the way the curve bends.</span></span> <span data-ttu-id="91376-107">Uma spline de Bézier é definida por dois pontos de extremidade e dois pontos de controle — a curva não passa pelos pontos de controle, mas os pontos de controle influenciam a direção e a curva à medida que ela passa de um ponto de extremidade para o outro.</span><span class="sxs-lookup"><span data-stu-id="91376-107">A Bézier spline is defined by two end points and two control points — the curve does not pass through the control points, but the control points influence the direction and bend as the curve goes from one end point to the other.</span></span>

<span data-ttu-id="91376-108">Os tópicos a seguir abordam as polilinhas cardeal e as linhas de Bézier em mais detalhes:</span><span class="sxs-lookup"><span data-stu-id="91376-108">The following topics cover cardinal splines and Bézier splines in more detail:</span></span>

-   [<span data-ttu-id="91376-109">Desenhando as linhas Cardeal</span><span class="sxs-lookup"><span data-stu-id="91376-109">Drawing Cardinal Splines</span></span>](-gdiplus-drawing-cardinal-splines-use.md)
-   [<span data-ttu-id="91376-110">Desenhando splines de Bézier</span><span class="sxs-lookup"><span data-stu-id="91376-110">Drawing Bézier Splines</span></span>](-gdiplus-drawing-bezier-splines-use.md)

 

 



