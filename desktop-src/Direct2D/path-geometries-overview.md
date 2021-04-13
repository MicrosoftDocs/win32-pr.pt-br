---
title: Visão geral de geometrias de caminho
description: Descreve como usar geometrias de caminho para definir formas complexas.
ms.assetid: 38a290be-b915-4317-b9b1-0e49e40dc8ec
ms.topic: article
ms.date: 05/31/2018
ms.custom: seodec18
ms.openlocfilehash: 0189c46f50e2ccc9ecc4523a4bb6f34006e59139
ms.sourcegitcommit: ee06501cc29132927ade9813e0888aaa4decc487
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/28/2021
ms.locfileid: "104552100"
---
# <a name="path-geometries-overview"></a><span data-ttu-id="fac08-103">Visão geral de geometrias de caminho</span><span class="sxs-lookup"><span data-stu-id="fac08-103">Path Geometries Overview</span></span>

<span data-ttu-id="fac08-104">Este tópico descreve como usar geometrias de caminho Direct2D para criar desenhos complexos.</span><span class="sxs-lookup"><span data-stu-id="fac08-104">This topic describes how to use Direct2D path geometries to create complex drawings.</span></span> <span data-ttu-id="fac08-105">Ele contém as seguintes seções:</span><span class="sxs-lookup"><span data-stu-id="fac08-105">It contains the following sections.</span></span>

-   [<span data-ttu-id="fac08-106">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="fac08-106">Prerequisites</span></span>](#prerequisites)
-   [<span data-ttu-id="fac08-107">Geometrias de caminho em Direct2D</span><span class="sxs-lookup"><span data-stu-id="fac08-107">Path Geometries in Direct2D</span></span>](#path-geometries-in-direct2d)
-   [<span data-ttu-id="fac08-108">Usando um ID2D1GeometrySink para popular uma geometria de caminho</span><span class="sxs-lookup"><span data-stu-id="fac08-108">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>](#using-an-id2d1geometrysink-to-populate-a-path-geometry)
-   [<span data-ttu-id="fac08-109">Exemplo: criar um desenho complexo</span><span class="sxs-lookup"><span data-stu-id="fac08-109">Example: Create a Complex Drawing</span></span>](#example-create-a-complex-drawing)
    -   [<span data-ttu-id="fac08-110">Criar uma geometria de caminho para as montanhas à esquerda</span><span class="sxs-lookup"><span data-stu-id="fac08-110">Create a Path Geometry for the Left Mountain</span></span>](#create-a-path-geometry-for-the-left-mountain)
    -   [<span data-ttu-id="fac08-111">Criar uma geometria de caminho para as montanhas certas</span><span class="sxs-lookup"><span data-stu-id="fac08-111">Create a Path Geometry for the Right Mountain</span></span>](#create-a-path-geometry-for-the-right-mountain)
    -   [<span data-ttu-id="fac08-112">Criar uma geometria de caminho para o Sun</span><span class="sxs-lookup"><span data-stu-id="fac08-112">Create a Path Geometry for the Sun</span></span>](#create-a-path-geometry-for-the-sun)
    -   [<span data-ttu-id="fac08-113">Criar uma geometria de caminho para o rio</span><span class="sxs-lookup"><span data-stu-id="fac08-113">Create a Path Geometry for the River</span></span>](#create-a-path-geometry-for-the-river)
    -   [<span data-ttu-id="fac08-114">Renderizar as geometrias de caminho na exibição</span><span class="sxs-lookup"><span data-stu-id="fac08-114">Render the Path Geometries onto the Display</span></span>](#render-the-path-geometries-onto-the-display)
-   [<span data-ttu-id="fac08-115">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fac08-115">Related topics</span></span>](#related-topics)

## <a name="prerequisites"></a><span data-ttu-id="fac08-116">Pré-requisitos</span><span class="sxs-lookup"><span data-stu-id="fac08-116">Prerequisites</span></span>

<span data-ttu-id="fac08-117">Esta visão geral pressupõe que você esteja familiarizado com a criação de aplicativos Direct2D básicos, conforme descrito em [criando um aplicativo Direct2D simples](direct2d-quickstart.md).</span><span class="sxs-lookup"><span data-stu-id="fac08-117">This overview assumes that you are familiar with creating basic Direct2D applications, as described in [Creating a Simple Direct2D Application](direct2d-quickstart.md).</span></span> <span data-ttu-id="fac08-118">Ele também pressupõe que você esteja familiarizado com os recursos básicos das geometrias de Direct2D, conforme descrito na [visão geral de geometrias](direct2d-geometries-overview.md).</span><span class="sxs-lookup"><span data-stu-id="fac08-118">It also assumes that you are familiar with the basic features of Direct2D geometries, as described in the [Geometries Overview](direct2d-geometries-overview.md).</span></span>

## <a name="path-geometries-in-direct2d"></a><span data-ttu-id="fac08-119">Geometrias de caminho em Direct2D</span><span class="sxs-lookup"><span data-stu-id="fac08-119">Path Geometries in Direct2D</span></span>

<span data-ttu-id="fac08-120">As geometrias de caminho são representadas pela interface [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="fac08-120">Path geometries are represented by the [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) interface.</span></span> <span data-ttu-id="fac08-121">Para criar uma instância de uma geometria de caminho, chame o método [**ID2D1Factory:: createpathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) .</span><span class="sxs-lookup"><span data-stu-id="fac08-121">To instantiate a path geometry, call the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method.</span></span> <span data-ttu-id="fac08-122">Esses objetos podem ser usados para descrever valores geométricos complexos compostos de segmentos como arcos, curvas e linhas.</span><span class="sxs-lookup"><span data-stu-id="fac08-122">These objects can be used to describe complex geometric figures composed of segments such as arcs, curves, and lines.</span></span> <span data-ttu-id="fac08-123">Para preencher uma geometria de caminho com figuras e segmentos, chame o método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para recuperar um [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) e use os métodos do coletor de geometria para adicionar figuras e segmentos à geometria do caminho.</span><span class="sxs-lookup"><span data-stu-id="fac08-123">To populate a path geometry with figures and segments, call the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to retrieve an [**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) and use the geometry sink's methods to add figures and segments to the path geometry.</span></span>

## <a name="using-an-id2d1geometrysink-to-populate-a-path-geometry"></a><span data-ttu-id="fac08-124">Usando um ID2D1GeometrySink para popular uma geometria de caminho</span><span class="sxs-lookup"><span data-stu-id="fac08-124">Using an ID2D1GeometrySink to Populate a Path Geometry</span></span>

<span data-ttu-id="fac08-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) descreve um caminho geométrico que pode conter linhas, arcos, curvas Bézier cúbicas e curvas de Bézier quadráticas.</span><span class="sxs-lookup"><span data-stu-id="fac08-125">[**ID2D1GeometrySink**](/windows/win32/api/d2d1/nn-d2d1-id2d1geometrysink) describes a geometric path that can contain lines, arcs, cubic Bezier curves, and quadratic Bezier curves.</span></span>

<span data-ttu-id="fac08-126">Um coletor de geometria consiste em uma ou mais figuras.</span><span class="sxs-lookup"><span data-stu-id="fac08-126">A geometry sink consists of one or more figures.</span></span> <span data-ttu-id="fac08-127">Cada figura é composta por um ou mais segmentos de linha, curva ou arco.</span><span class="sxs-lookup"><span data-stu-id="fac08-127">Each figure is made up of one or more line, curve, or arc segments.</span></span> <span data-ttu-id="fac08-128">Para criar uma figura, chame o método [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) , passando o ponto inicial da figura e, em seguida, use seus métodos Add (como [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) e [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) para adicionar segmentos.</span><span class="sxs-lookup"><span data-stu-id="fac08-128">To create a figure, call the [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure) method, passing in the figure's starting point, and then use its Add methods (such as [**AddLine**](/windows/win32/api/d2d1/nf-d2d1-id2d1geometrysink-addline) and [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget)) to add segments.</span></span> <span data-ttu-id="fac08-129">Quando você terminar de adicionar segmentos, chame o método [**endfigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) .</span><span class="sxs-lookup"><span data-stu-id="fac08-129">When you are finished adding segments, call the [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure) method.</span></span> <span data-ttu-id="fac08-130">Você pode repetir essa sequência para criar figuras adicionais.</span><span class="sxs-lookup"><span data-stu-id="fac08-130">You can repeat this sequence to create additional figures.</span></span> <span data-ttu-id="fac08-131">Quando você terminar de criar figuras, chame o método [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) .</span><span class="sxs-lookup"><span data-stu-id="fac08-131">When you are finished creating figures, call the [**Close**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-close) method.</span></span>

## <a name="example-create-a-complex-drawing"></a><span data-ttu-id="fac08-132">Exemplo: criar um desenho complexo</span><span class="sxs-lookup"><span data-stu-id="fac08-132">Example: Create a Complex Drawing</span></span>

<span data-ttu-id="fac08-133">A ilustração a seguir mostra um desenho complexo com linhas, arcos e curvas de Bézier.</span><span class="sxs-lookup"><span data-stu-id="fac08-133">The following illustration shows a complex drawing with lines, arcs, and Bezier curves.</span></span> <span data-ttu-id="fac08-134">O exemplo de código a seguir mostra como criar o desenho usando quatro objetos Geometry de caminho, um para a montanha esquerda, um para as montanhas corretas, um para o rio e outro para o sol com flares.</span><span class="sxs-lookup"><span data-stu-id="fac08-134">The code example that follows shows how to create the drawing by using four path geometry objects, one for the left mountain, one for the right mountain, one for the river, and one for the sun with flares.</span></span>

![ilustração de um rio, montanhas e sol, usando geometrias de caminho](images/path-geo-mnts.png)

### <a name="create-a-path-geometry-for-the-left-mountain"></a><span data-ttu-id="fac08-136">Criar uma geometria de caminho para as montanhas à esquerda</span><span class="sxs-lookup"><span data-stu-id="fac08-136">Create a Path Geometry for the Left Mountain</span></span>

<span data-ttu-id="fac08-137">O exemplo primeiro cria uma geometria de caminho para as montanhas à esquerda, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="fac08-137">The example first creates a path geometry for the left mountain as shown in the following illustration.</span></span>

![Mostra um desenho complexo de um polígono que mostra uma montanha.](images/path-geo-leftmnt.png)

<span data-ttu-id="fac08-139">Para criar a montanha à esquerda, o exemplo chama o método [**ID2D1Factory:: createpathgeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) para criar um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span><span class="sxs-lookup"><span data-stu-id="fac08-139">To create the left mountain, the example calls the [**ID2D1Factory::CreatePathGeometry**](/windows/win32/api/d2d1/nf-d2d1-id2d1factory-createpathgeometry) method to create an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry).</span></span>


```C++
hr = m_pD2DFactory->CreatePathGeometry(&m_pLeftMountainGeometry);
```



<span data-ttu-id="fac08-140">Em seguida, o exemplo usa o método [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) para obter um coletor de geometria de um [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) e o armazena na variável *pSink* .</span><span class="sxs-lookup"><span data-stu-id="fac08-140">The example then uses the [**Open**](/windows/win32/api/d2d1/nf-d2d1-id2d1pathgeometry-open) method to obtain a geometry sink from an [**ID2D1PathGeometry**](/windows/win32/api/d2d1/nn-d2d1-id2d1pathgeometry) and stores it in the *pSink* variable.</span></span>


```C++
ID2D1GeometrySink *pSink = NULL;
hr = m_pLeftMountainGeometry->Open(&pSink);
```



<span data-ttu-id="fac08-141">Em seguida, o exemplo chama [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passando a [**Figura d2d1 de \_ \_ início \_ preenchido**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) que indica que esta figura está preenchida e, em seguida, chama [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passando uma matriz de pontos de [**d2d1 do \_ ponto \_ 2F**](d2d1-point-2f.md) , (267, 177), (236, 192), (212, 160), (156, 255) e (346, 255).</span><span class="sxs-lookup"><span data-stu-id="fac08-141">The example then calls [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), passing in [**D2D1\_FIGURE\_BEGIN\_FILLED**](/windows/desktop/api/d2d1/ne-d2d1-d2d1_figure_begin) that indicates this figure is filled, then calls [**AddLines**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-addlines), passing in an array of [**D2D1\_POINT\_2F**](d2d1-point-2f.md) points, (267, 177), (236, 192), (212, 160), (156, 255) and (346, 255).</span></span>

<span data-ttu-id="fac08-142">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="fac08-142">The following code shows how to do this.</span></span>


```C++
pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

pSink->BeginFigure(
    D2D1::Point2F(346,255),
    D2D1_FIGURE_BEGIN_FILLED
    );
D2D1_POINT_2F points[5] = {
   D2D1::Point2F(267, 177),
   D2D1::Point2F(236, 192),
   D2D1::Point2F(212, 160),
   D2D1::Point2F(156, 255),
   D2D1::Point2F(346, 255), 
   };
pSink->AddLines(points, ARRAYSIZE(points));
pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
```



### <a name="create-a-path-geometry-for-the-right-mountain"></a><span data-ttu-id="fac08-143">Criar uma geometria de caminho para as montanhas certas</span><span class="sxs-lookup"><span data-stu-id="fac08-143">Create a Path Geometry for the Right Mountain</span></span>

<span data-ttu-id="fac08-144">Em seguida, o exemplo cria outra geometria de caminho para a montanha correta com pontos (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263) e (575, 263).</span><span class="sxs-lookup"><span data-stu-id="fac08-144">The example then creates another path geometry for the right mountain with points (481, 146), (449, 181), (433, 159), (401, 214), (381, 199), (323, 263), and (575, 263).</span></span> <span data-ttu-id="fac08-145">A ilustração a seguir mostra como as montanhas certas são exibidas.</span><span class="sxs-lookup"><span data-stu-id="fac08-145">The following illustration shows how the right mountain is displayed.</span></span>

![ilustração de um polígono que mostra uma montanha](images/path-geo-rightmnt.png)

<span data-ttu-id="fac08-147">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="fac08-147">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRightMountainGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRightMountainGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);

                pSink->BeginFigure(
                    D2D1::Point2F(575,263),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                D2D1_POINT_2F points[] = {
                   D2D1::Point2F(481, 146),
                   D2D1::Point2F(449, 181),
                   D2D1::Point2F(433, 159),
                   D2D1::Point2F(401, 214),
                   D2D1::Point2F(381, 199), 
                   D2D1::Point2F(323, 263), 
                   D2D1::Point2F(575, 263)
                   };
                pSink->AddLines(points, ARRAYSIZE(points));
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-sun"></a><span data-ttu-id="fac08-148">Criar uma geometria de caminho para o Sun</span><span class="sxs-lookup"><span data-stu-id="fac08-148">Create a Path Geometry for the Sun</span></span>

<span data-ttu-id="fac08-149">Em seguida, o exemplo popula outra geometria de caminho para o sol, conforme mostrado na ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="fac08-149">The example then populates another path geometry for the sun as shown in the following illustration.</span></span>

![ilustração de curvas de arco e Bézier que mostram o sol](images/path-geo-sun.png)

<span data-ttu-id="fac08-151">Para fazer isso, a geometria do caminho cria um coletor e adiciona uma figura para o arco e uma figura para cada clarão para o coletor.</span><span class="sxs-lookup"><span data-stu-id="fac08-151">To do this, the path geometry creates a sink, and adds a figure for the arc and a figure for each flare to the sink.</span></span> <span data-ttu-id="fac08-152">Repetindo a sequência de [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), seus métodos Add (como [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) e [**enddefinem**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), várias figuras são adicionadas ao coletor.</span><span class="sxs-lookup"><span data-stu-id="fac08-152">By repeating the sequence of [**BeginFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-beginfigure), its Add (such as [**AddBezier**](/windows/desktop/api/d2d1/nf-d2d1-id2d1factory-createdxgisurfacerendertarget(idxgisurface_constd2d1_render_target_properties__id2d1rendertarget))) methods, and [**EndFigure**](/windows/win32/api/d2d1/nf-d2d1-id2d1simplifiedgeometrysink-endfigure), multiple figures are added to the sink.</span></span>

<span data-ttu-id="fac08-153">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="fac08-153">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pSunGeometry);
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pSunGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
            
                pSink->BeginFigure(
                    D2D1::Point2F(270, 255),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddArc(
                    D2D1::ArcSegment(
                        D2D1::Point2F(440, 255), // end point
                        D2D1::SizeF(85, 85),
                        0.0f, // rotation angle
                        D2D1_SWEEP_DIRECTION_CLOCKWISE,
                        D2D1_ARC_SIZE_SMALL
                        ));            
                pSink->EndFigure(D2D1_FIGURE_END_CLOSED);

                pSink->BeginFigure(
                    D2D1::Point2F(299, 182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(299, 182),
                       D2D1::Point2F(294, 176),
                       D2D1::Point2F(285, 178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(276, 179),
                       D2D1::Point2F(272, 173),
                       D2D1::Point2F(272, 173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(354, 156),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(354, 156),
                       D2D1::Point2F(358, 149),
                       D2D1::Point2F(354, 142)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(349, 134),
                       D2D1::Point2F(354, 127),
                       D2D1::Point2F(354, 127)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(322,164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(322, 164),
                       D2D1::Point2F(322, 156),
                       D2D1::Point2F(314, 152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(306, 149),
                       D2D1::Point2F(305, 141),
                       D2D1::Point2F(305, 141)
                       ));              
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(385, 164),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(385,164),
                       D2D1::Point2F(392,161),
                       D2D1::Point2F(394,152)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(395,144),
                       D2D1::Point2F(402,141),
                       D2D1::Point2F(402,142)
                       ));                
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);

                pSink->BeginFigure(
                    D2D1::Point2F(408,182),
                    D2D1_FIGURE_BEGIN_HOLLOW
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(408,182),
                       D2D1::Point2F(416,184),
                       D2D1::Point2F(422,178)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(428,171),
                       D2D1::Point2F(435,173),
                       D2D1::Point2F(435,173)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
            hr = pSink->Close();

            SafeRelease(&pSink);
       }
```



### <a name="create-a-path-geometry-for-the-river"></a><span data-ttu-id="fac08-154">Criar uma geometria de caminho para o rio</span><span class="sxs-lookup"><span data-stu-id="fac08-154">Create a Path Geometry for the River</span></span>

<span data-ttu-id="fac08-155">Em seguida, o exemplo cria outro caminho de geometria para o rio que contém curvas de Bézier.</span><span class="sxs-lookup"><span data-stu-id="fac08-155">The example then creates another geometry path for the river that contains Bezier curves.</span></span> <span data-ttu-id="fac08-156">A ilustração a seguir mostra como o rio é exibido.</span><span class="sxs-lookup"><span data-stu-id="fac08-156">The following illustration shows how the river is displayed.</span></span>

![ilustração de curvas de Bézier que mostram um rio](images/path-geo-river.png)

<span data-ttu-id="fac08-158">O código a seguir mostra como fazer isso.</span><span class="sxs-lookup"><span data-stu-id="fac08-158">The following code shows how to do this.</span></span>


```C++
        hr = m_pD2DFactory->CreatePathGeometry(&m_pRiverGeometry);
    
        if(SUCCEEDED(hr))
        {
            ID2D1GeometrySink *pSink = NULL;

            hr = m_pRiverGeometry->Open(&pSink);
            if (SUCCEEDED(hr))
            {
                pSink->SetFillMode(D2D1_FILL_MODE_WINDING);
                pSink->BeginFigure(
                    D2D1::Point2F(183, 392),
                    D2D1_FIGURE_BEGIN_FILLED
                    );
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(238, 284),
                       D2D1::Point2F(472, 345),
                       D2D1::Point2F(356, 303)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(237, 261),
                       D2D1::Point2F(333, 256),
                       D2D1::Point2F(333, 256)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(335, 257),
                       D2D1::Point2F(241, 261),
                       D2D1::Point2F(411, 306)
                       ));
                pSink->AddBezier(
                   D2D1::BezierSegment(
                       D2D1::Point2F(574, 350),
                       D2D1::Point2F(288, 324),
                       D2D1::Point2F(296, 392)
                       ));
                pSink->EndFigure(D2D1_FIGURE_END_OPEN);
            }
```



### <a name="render-the-path-geometries-onto-the-display"></a><span data-ttu-id="fac08-159">Renderizar as geometrias de caminho na exibição</span><span class="sxs-lookup"><span data-stu-id="fac08-159">Render the Path Geometries onto the Display</span></span>

<span data-ttu-id="fac08-160">O código a seguir mostra como renderizar as geometrias de caminho populadas na exibição.</span><span class="sxs-lookup"><span data-stu-id="fac08-160">The following code shows how to render the populated path geometries on the display.</span></span> <span data-ttu-id="fac08-161">Ele primeiro desenha e pinta a geometria Sun, a próxima da geometria da montanha esquerda, a geometria de rio e, por fim, a geometria de montanha correta.</span><span class="sxs-lookup"><span data-stu-id="fac08-161">It first draws and paints the sun geometry, next the left mountain geometry, then the river geometry, and finally the right mountain geometry.</span></span>


```C++
 m_pRenderTarget->BeginDraw();

 m_pRenderTarget->SetTransform(D2D1::Matrix3x2F::Identity());

 m_pRenderTarget->Clear(D2D1::ColorF(D2D1::ColorF::White));

 D2D1_SIZE_F rtSize = m_pRenderTarget->GetSize();
 m_pRenderTarget->FillRectangle(
     D2D1::RectF(0, 0, rtSize.width, rtSize.height),
     m_pGridPatternBitmapBrush
     );

 m_pRenderTarget->FillGeometry(m_pSunGeometry, m_pRadialGradientBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pSunGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::OliveDrab, 1.f));
 m_pRenderTarget->FillGeometry(m_pLeftMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pLeftMountainGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::LightSkyBlue, 1.f));
 m_pRenderTarget->FillGeometry(m_pRiverGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRiverGeometry, m_pSceneBrush, 1.f);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::YellowGreen, 1.f));
 m_pRenderTarget->FillGeometry(m_pRightMountainGeometry, m_pSceneBrush);

 m_pSceneBrush->SetColor(D2D1::ColorF(D2D1::ColorF::Black, 1.f));
 m_pRenderTarget->DrawGeometry(m_pRightMountainGeometry, m_pSceneBrush, 1.f);


 hr = m_pRenderTarget->EndDraw();
```



<span data-ttu-id="fac08-162">O exemplo completo gera a ilustração a seguir.</span><span class="sxs-lookup"><span data-stu-id="fac08-162">The complete example outputs the following illustration.</span></span>

![ilustração de um rio, montanhas e sol, usando geometrias de caminho](images/path-geo-mnts.png)

## <a name="related-topics"></a><span data-ttu-id="fac08-164">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fac08-164">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fac08-165">Criando um aplicativo Direct2D simples</span><span class="sxs-lookup"><span data-stu-id="fac08-165">Creating a Simple Direct2D Application</span></span>](direct2d-quickstart.md)
</dt> <dt>

[<span data-ttu-id="fac08-166">Visão geral de geometrias</span><span class="sxs-lookup"><span data-stu-id="fac08-166">Geometries Overview</span></span>](direct2d-geometries-overview.md)
</dt> </dl>

 

 