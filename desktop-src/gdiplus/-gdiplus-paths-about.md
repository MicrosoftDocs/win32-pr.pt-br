---
description: Os demarcadores são formados combinando linhas, retângulos e curvas simples. Lembre-se da visão geral dos gráficos vetoriais que os seguintes blocos de construção básicos provaram ser os mais úteis para desenhar imagens.
ms.assetid: 88fea2ec-7b53-44bb-841d-486c5c879c68
title: Caminhos (GDI+)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 768d01d2d945c8252125a43ee2dc79f985703da1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104556704"
---
# <a name="paths-gdi"></a><span data-ttu-id="ebbff-104">Caminhos (GDI+)</span><span class="sxs-lookup"><span data-stu-id="ebbff-104">Paths (GDI+)</span></span>

<span data-ttu-id="ebbff-105">Os demarcadores são formados combinando linhas, retângulos e curvas simples.</span><span class="sxs-lookup"><span data-stu-id="ebbff-105">Paths are formed by combining lines, rectangles, and simple curves.</span></span> <span data-ttu-id="ebbff-106">Lembre-se da [visão geral dos gráficos vetoriais](-gdiplus-overview-of-vector-graphics-about.md) que os seguintes blocos de construção básicos provaram ser os mais úteis para desenhar imagens.</span><span class="sxs-lookup"><span data-stu-id="ebbff-106">Recall from the [Overview of Vector Graphics](-gdiplus-overview-of-vector-graphics-about.md) that the following basic building blocks have proven to be the most useful for drawing pictures.</span></span>

-   <span data-ttu-id="ebbff-107">Linhas</span><span class="sxs-lookup"><span data-stu-id="ebbff-107">Lines</span></span>
-   <span data-ttu-id="ebbff-108">Retângulos</span><span class="sxs-lookup"><span data-stu-id="ebbff-108">Rectangles</span></span>
-   <span data-ttu-id="ebbff-109">Elipses</span><span class="sxs-lookup"><span data-stu-id="ebbff-109">Ellipses</span></span>
-   <span data-ttu-id="ebbff-110">Arcos</span><span class="sxs-lookup"><span data-stu-id="ebbff-110">Arcs</span></span>
-   <span data-ttu-id="ebbff-111">Polígonos</span><span class="sxs-lookup"><span data-stu-id="ebbff-111">Polygons</span></span>
-   <span data-ttu-id="ebbff-112">Splines cardinais</span><span class="sxs-lookup"><span data-stu-id="ebbff-112">Cardinal splines</span></span>
-   <span data-ttu-id="ebbff-113">Splines de Bézier</span><span class="sxs-lookup"><span data-stu-id="ebbff-113">Bézier splines</span></span>

<span data-ttu-id="ebbff-114">No Windows GDI+, o objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) permite que você colete uma sequência desses blocos de construção em uma única unidade.</span><span class="sxs-lookup"><span data-stu-id="ebbff-114">In Windows GDI+, the [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object allows you to collect a sequence of these building blocks into a single unit.</span></span> <span data-ttu-id="ebbff-115">Toda a sequência de linhas, retângulos, polígonos e curvas pode ser desenhada com uma chamada para o método [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) da classe [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) .</span><span class="sxs-lookup"><span data-stu-id="ebbff-115">The entire sequence of lines, rectangles, polygons, and curves can then be drawn with one call to the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method of the [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) class.</span></span> <span data-ttu-id="ebbff-116">A ilustração a seguir mostra um demarcador criado pela combinação de uma linha, um arco, uma spline de Bézier e uma spline cardinal.</span><span class="sxs-lookup"><span data-stu-id="ebbff-116">The following illustration shows a path created by combining a line, an arc, a Bézier spline, and a cardinal spline.</span></span>

![ilustração de um caminho que combina uma linha, um arco, um spline de Bézier e um spline Cardinal](images/aboutgdip02-art14.png)

<span data-ttu-id="ebbff-118">A classe [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) fornece os seguintes métodos para criar uma sequência de itens a serem desenhados: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [addelipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [addpolígono](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (para as polilinhas Cardeal) e [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span><span class="sxs-lookup"><span data-stu-id="ebbff-118">The [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) class provides the following methods for creating a sequence of items to be drawn: [AddLine](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addline(inint_inint_inint_inint)), [AddRectangle](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangle(inconstrectf_)), [AddEllipse](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addellipse(inint_inint_inint_inint)), [AddArc](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addarc(inint_inint_inint_inint_inreal_inreal)), [AddPolygon](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addpolygon(inconstpointf_inint)), [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) (for cardinal splines), and [AddBezier](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbezier(inint_inint_inint_inint_inint_inint_inint_inint)).</span></span> <span data-ttu-id="ebbff-119">Cada um desses métodos é sobrecarregado; ou seja, cada método vem em várias variações com diferentes listas de parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ebbff-119">Each of these methods is overloaded; that is, each method comes in several variations with different parameter lists.</span></span> <span data-ttu-id="ebbff-120">Por exemplo, uma variação do método AddLine recebe quatro inteiros e outra variação do método AddLine recebe dois objetos [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) .</span><span class="sxs-lookup"><span data-stu-id="ebbff-120">For example, one variation of the AddLine method receives four integers, and another variation of the AddLine method receives two [**Point**](/windows/win32/api/gdiplustypes/nl-gdiplustypes-point) objects.</span></span>

<span data-ttu-id="ebbff-121">Os métodos para adicionar linhas, retângulos e polilinhados de Bézier a um caminho têm métodos de complemento no plural que adicionam vários itens ao caminho em uma única chamada: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [addretângulos](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint))e [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span><span class="sxs-lookup"><span data-stu-id="ebbff-121">The methods for adding lines, rectangles, and Bézier splines to a path have plural companion methods that add several items to the path in a single call: [AddLines](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addlines(inconstpoint_inint)), [AddRectangles](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addrectangles(inconstrectf_inint)), and [AddBeziers](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addbeziers(inconstpointf_inint)).</span></span> <span data-ttu-id="ebbff-122">Além disso, o método [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) tem um método complementar, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), que adiciona uma curva fechada ao caminho.</span><span class="sxs-lookup"><span data-stu-id="ebbff-122">Also, the [AddCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addcurve(inconstpoint_inint)) method has a companion method, [AddClosedCurve](/windows/win32/api/gdipluspath/nf-gdipluspath-graphicspath-addclosedcurve(inconstpointf_inint)), that adds a closed curve to the path.</span></span>

<span data-ttu-id="ebbff-123">Para desenhar um caminho, você precisa de um objeto [**gráfico**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) , um objeto de [**caneta**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) e um objeto [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) .</span><span class="sxs-lookup"><span data-stu-id="ebbff-123">To draw a path, you need a [**Graphics**](/windows/win32/api/gdiplusgraphics/nl-gdiplusgraphics-graphics) object, a [**Pen**](/windows/win32/api/gdipluspen/nl-gdipluspen-pen) object, and a [**GraphicsPath**](/windows/win32/api/gdipluspath/nl-gdipluspath-graphicspath) object.</span></span> <span data-ttu-id="ebbff-124">O objeto **Graphics** fornece o método [**Graphics::D rawpath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) e o objeto **Pen** armazena os atributos do caminho, como largura e cor da linha.</span><span class="sxs-lookup"><span data-stu-id="ebbff-124">The **Graphics** object provides the [**Graphics::DrawPath**](/windows/win32/api/Gdiplusgraphics/nf-gdiplusgraphics-graphics-drawpath) method, and the **Pen** object stores attributes of the path, such as line width and color.</span></span> <span data-ttu-id="ebbff-125">O objeto **GraphicsPath** armazena a sequência de linhas, retângulos e curvas que compõem o caminho.</span><span class="sxs-lookup"><span data-stu-id="ebbff-125">The **GraphicsPath** object stores the sequence of lines, rectangles, and curves that make up the path.</span></span> <span data-ttu-id="ebbff-126">Os endereços do objeto **Pen** e do objeto **GraphicsPath** são passados como argumentos para o método **Graphics::D rawpath** .</span><span class="sxs-lookup"><span data-stu-id="ebbff-126">The addresses of the **Pen** object and the **GraphicsPath** object are passed as arguments to the **Graphics::DrawPath** method.</span></span> <span data-ttu-id="ebbff-127">O exemplo a seguir desenha um caminho que consiste em uma linha, uma elipse e um spline Bézier.</span><span class="sxs-lookup"><span data-stu-id="ebbff-127">The following example draws a path that consists of a line, an ellipse, and a Bézier spline.</span></span>


```
myGraphicsPath.AddLine(0, 0, 30, 20);
myGraphicsPath.AddEllipse(20, 20, 20, 40);
myGraphicsPath.AddBezier(30, 60, 70, 60, 50, 30, 100, 10);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="ebbff-128">A ilustração a seguir mostra o demarcador.</span><span class="sxs-lookup"><span data-stu-id="ebbff-128">The following illustration shows the path.</span></span>

![ilustração de um caminho composto por uma linha, uma elipse e um spline de Bézier](images/aboutgdip02-art15.png)

<span data-ttu-id="ebbff-130">Além de adicionar linhas, retângulos e curvas a um demarcador, você pode adicionar demarcadores a um demarcador.</span><span class="sxs-lookup"><span data-stu-id="ebbff-130">In addition to adding lines, rectangles, and curves to a path, you can add paths to a path.</span></span> <span data-ttu-id="ebbff-131">Isso permite combinar os demarcadores existentes para formar demarcadores grandes e complexos.</span><span class="sxs-lookup"><span data-stu-id="ebbff-131">This allows you to combine existing paths to form large, complex paths.</span></span> <span data-ttu-id="ebbff-132">O código a seguir adiciona **graphicsPath1** e **graphicsPath2** a **myGraphicsPath**.</span><span class="sxs-lookup"><span data-stu-id="ebbff-132">The following code adds **graphicsPath1** and **graphicsPath2** to **myGraphicsPath**.</span></span> <span data-ttu-id="ebbff-133">O segundo parâmetro do método [**GraphicsPath:: addcaminho**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) especifica se o caminho adicionado está conectado ao caminho existente.</span><span class="sxs-lookup"><span data-stu-id="ebbff-133">The second parameter of the [**GraphicsPath::AddPath**](/windows/win32/api/Gdipluspath/nf-gdipluspath-graphicspath-addpath) method specifies whether the added path is connected to the existing path.</span></span>


```
myGraphicsPath.AddPath(&graphicsPath1, FALSE);
myGraphicsPath.AddPath(&graphicsPath2, TRUE);
```



<span data-ttu-id="ebbff-134">Há dois outros itens que você pode adicionar a um demarcador: cadeias de caracteres e pizzas.</span><span class="sxs-lookup"><span data-stu-id="ebbff-134">There are two other items you can add to a path: strings and pies.</span></span> <span data-ttu-id="ebbff-135">Uma pizza é uma parte do interior de uma elipse.</span><span class="sxs-lookup"><span data-stu-id="ebbff-135">A pie is a portion of the interior of an ellipse.</span></span> <span data-ttu-id="ebbff-136">O exemplo a seguir cria um caminho de um arco, um spline Cardeal, uma cadeia de caracteres e uma pizza.</span><span class="sxs-lookup"><span data-stu-id="ebbff-136">The following example creates a path from an arc, a cardinal spline, a string, and a pie.</span></span>


```
myGraphicsPath.AddArc(0, 0, 30, 20, -90, 180);
myGraphicsPath.AddCurve(myPointArray, 3);
myGraphicsPath.AddString(L"a string in a path", 18, &myFontFamily, 
   0, 24, myPointF, &myStringFormat);
myGraphicsPath.AddPie(230, 10, 40, 40, 40, 110);
myGraphics.DrawPath(&myPen, &myGraphicsPath);
```



<span data-ttu-id="ebbff-137">A ilustração a seguir mostra o demarcador.</span><span class="sxs-lookup"><span data-stu-id="ebbff-137">The following illustration shows the path.</span></span> <span data-ttu-id="ebbff-138">Observe que um demarcador não precisa estar conectado; o arco, spline cardinal, cadeia de caracteres e pizza são separados.</span><span class="sxs-lookup"><span data-stu-id="ebbff-138">Note that a path does not have to be connected; the arc, cardinal spline, string, and pie are separated.</span></span>

![ilustração de um caminho composto por linhas desconectadas: um arco, um spline Cardinal, uma cadeia de caracteres e uma pizza](images/aboutgdip02-art16.png)

 

 



