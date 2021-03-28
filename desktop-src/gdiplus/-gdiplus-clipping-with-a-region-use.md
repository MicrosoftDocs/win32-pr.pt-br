---
description: Uma das propriedades da classe Graphics é a região de recorte. Todo o desenho feito por um determinado objeto gráfico é restrito à região de recorte desse objeto gráfico. Você pode definir a região de recorte chamando o método SetClip.
ms.assetid: 816a5845-ca03-46c6-bdda-e6a7d02ff614
title: Recorte com uma região
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa19426d62d5d3af99150bf9ac8e8099628fe2f8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104557140"
---
# <a name="clipping-with-a-region"></a><span data-ttu-id="b42e7-105">Recorte com uma região</span><span class="sxs-lookup"><span data-stu-id="b42e7-105">Clipping with a Region</span></span>

<span data-ttu-id="b42e7-106">Uma das propriedades da classe [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) é a região de recorte.</span><span class="sxs-lookup"><span data-stu-id="b42e7-106">One of the properties of the [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class is the clipping region.</span></span> <span data-ttu-id="b42e7-107">Todo o desenho feito por um determinado objeto **gráfico** é restrito à região de recorte desse objeto **gráfico** .</span><span class="sxs-lookup"><span data-stu-id="b42e7-107">All drawing done by a given **Graphics** object is restricted to the clipping region of that **Graphics** object.</span></span> <span data-ttu-id="b42e7-108">Você pode definir a região de recorte chamando o método **SetClip** .</span><span class="sxs-lookup"><span data-stu-id="b42e7-108">You can set the clipping region by calling the **SetClip** method.</span></span>

<span data-ttu-id="b42e7-109">O exemplo a seguir constrói um caminho que consiste em um único polígono.</span><span class="sxs-lookup"><span data-stu-id="b42e7-109">The following example constructs a path that consists of a single polygon.</span></span> <span data-ttu-id="b42e7-110">Em seguida, o código constrói uma região com base nesse caminho.</span><span class="sxs-lookup"><span data-stu-id="b42e7-110">Then the code constructs a region based on that path.</span></span> <span data-ttu-id="b42e7-111">O endereço da região é passado para o método **SetClip** de um objeto [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) e, em seguida, duas cadeias de caracteres são desenhadas.</span><span class="sxs-lookup"><span data-stu-id="b42e7-111">The address of the region is passed to the **SetClip** method of a [**Graphics**](/windows/desktop/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, and then two strings are drawn.</span></span>


```
// Create a path that consists of a single polygon.
Point polyPoints[] = {Point(10, 10), Point(150, 10), 
   Point(100, 75), Point(100, 150)};
GraphicsPath path;
path.AddPolygon(polyPoints, 4);
// Construct a region based on the path.
Region region(&path);
// Draw the outline of the region.
Pen pen(Color(255, 0, 0, 0));
graphics.DrawPath(&pen, &path);
// Set the clipping region of the Graphics object.
graphics.SetClip(&region);
// Draw some clipped strings.
FontFamily fontFamily(L"Arial");
Font font(&fontFamily, 36, FontStyleBold, UnitPixel);
SolidBrush solidBrush(Color(255, 255, 0, 0));
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 25), &solidBrush);
graphics.DrawString(L"A Clipping Region", 20, &font, 
   PointF(15, 68), &solidBrush);
```



<span data-ttu-id="b42e7-112">A ilustração a seguir mostra as cadeias de caracteres recortadas.</span><span class="sxs-lookup"><span data-stu-id="b42e7-112">The following illustration shows the clipped strings.</span></span>

![ilustração mostrando partes de duas frases que aparecem dentro de uma forma de quatro lados](images/clip1.png)

 

 



