---
description: Um polígono é uma figura fechada com três ou mais lados retos.
ms.assetid: f1155341-83f3-4805-8d42-a1910515db31
title: Polígonos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fe67ec2d062579df0510c100a80d06715be4199e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103647104"
---
# <a name="polygons"></a><span data-ttu-id="a9388-103">Polígonos</span><span class="sxs-lookup"><span data-stu-id="a9388-103">Polygons</span></span>

<span data-ttu-id="a9388-104">Um polígono é uma figura fechada com três ou mais lados retos.</span><span class="sxs-lookup"><span data-stu-id="a9388-104">A polygon is a closed figure with three or more straight sides.</span></span> <span data-ttu-id="a9388-105">Por exemplo, um triângulo é um polígono com três lados, um retângulo é um polígono com quatro lados e um Pentágono é um polígono com cinco lados.</span><span class="sxs-lookup"><span data-stu-id="a9388-105">For example, a triangle is a polygon with three sides, a rectangle is a polygon with four sides, and a pentagon is a polygon with five sides.</span></span> <span data-ttu-id="a9388-106">A ilustração a seguir mostra diversos polígonos.</span><span class="sxs-lookup"><span data-stu-id="a9388-106">The following illustration shows several polygons.</span></span>

![ilustração mostrando cinco polígonos de diferentes formas, tamanhos e cores](images/aboutgdip02-art07.png)

<span data-ttu-id="a9388-108">Para desenhar um polígono, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e uma matriz de objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (ou [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)).</span><span class="sxs-lookup"><span data-stu-id="a9388-108">To draw a polygon, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and an array of [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) (or [**PointF**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-pointf)) objects.</span></span> <span data-ttu-id="a9388-109">O objeto **Graphics** fornece o método [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) .</span><span class="sxs-lookup"><span data-stu-id="a9388-109">The **Graphics** object provides the [DrawPolygon](/windows/win32/api/gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpolygon(inconstpen_inconstpoint_inint)) method.</span></span> <span data-ttu-id="a9388-110">O objeto **Pen** armazena os atributos do polígono, como largura e cor da linha, e a matriz de objetos **Point** armazena os pontos a serem conectados por linhas retas.</span><span class="sxs-lookup"><span data-stu-id="a9388-110">The **Pen** object stores attributes of the polygon, such as line width and color, and the array of **Point** objects stores the points to be connected by straight lines.</span></span> <span data-ttu-id="a9388-111">Os endereços do objeto **Pen** e a matriz de objetos **Point** são passados como argumentos para o método DrawPolygon.</span><span class="sxs-lookup"><span data-stu-id="a9388-111">The addresses of the **Pen** object and the array of **Point** objects are passed as arguments to the DrawPolygon method.</span></span> <span data-ttu-id="a9388-112">O exemplo a seguir desenha um polígono com três lados.</span><span class="sxs-lookup"><span data-stu-id="a9388-112">The following example draws a three-sided polygon.</span></span> <span data-ttu-id="a9388-113">Observe que há apenas três pontos em **myPointArray**: (0, 0), (50, 30) e (30, 60).</span><span class="sxs-lookup"><span data-stu-id="a9388-113">Note that there are only three points in **myPointArray**: (0, 0), (50, 30), and (30, 60).</span></span> <span data-ttu-id="a9388-114">O método DrawPolygon fecha automaticamente o polígono, desenhando uma linha de (30, 60) de volta para o ponto de partida (0, 0);</span><span class="sxs-lookup"><span data-stu-id="a9388-114">The DrawPolygon method automatically closes the polygon by drawing a line from (30, 60) back to the starting point (0, 0);</span></span>


```
Point myPointArray[] =
   {Point(0, 0), Point(50, 30), Point(30, 60)};
myGraphics.DrawPolygon(&myPen, myPointArray, 3);
```



<span data-ttu-id="a9388-115">A ilustração a seguir mostra o polígono.</span><span class="sxs-lookup"><span data-stu-id="a9388-115">The following illustration shows the polygon.</span></span>

![ilustração mostrando um triângulo em relação a eixos de coordenadas](images/aboutgdip02-art08.png)

 

 



