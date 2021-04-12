---
title: Usando curvas e superfícies NURBS
description: As funções de B-spline racional não uniformes (NURBS) fornecem descrições gerais e poderosas de curvas e superfícies em duas e três dimensões, convertendo as curvas e superfícies em avaliadores OpenGL.
ms.assetid: 0b55659d-9fa2-47fc-ae15-0c296bd94dcb
keywords:
- Utilitário OpenGL (GLU), B-spline racional não uniforme (NURBS)
- GLU (utilitário OpenGL), B-spline racional não uniforme (NURBS)
- B-spline racional não uniforme (NURBS) OpenGL
- NURBS (B-spline racional não uniforme) OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8f85e9a2045c417007c34d714ae6635ebfaf1180
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104291989"
---
# <a name="using-nurbs-curves-and-surfaces"></a><span data-ttu-id="8cb1b-107">Usando curvas e superfícies NURBS</span><span class="sxs-lookup"><span data-stu-id="8cb1b-107">Using NURBS Curves and Surfaces</span></span>

<span data-ttu-id="8cb1b-108">As funções de B-spline racional não uniformes (NURBS) fornecem descrições gerais e poderosas de curvas e superfícies em duas e três dimensões, convertendo as curvas e superfícies em avaliadores OpenGL.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-108">Non-Uniform Rational B-Spline (NURBS) functions provide general and powerful descriptions of curves and surfaces in two and three dimensions, converting the curves and surfaces to OpenGL evaluators.</span></span> <span data-ttu-id="8cb1b-109">As funções NURBS podem representar geometria em vários sistemas de design mecânico auxiliados por computador.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-109">The NURBS functions can represent geometry in many computer-aided mechanical design systems.</span></span> <span data-ttu-id="8cb1b-110">Eles podem renderizar curvas e superfícies em uma variedade de estilos, e podem lidar automaticamente com a subdivisão adaptável que tessellates o domínio em triângulos menores em regiões de alta curvatura e bordas de silhueta próxima.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-110">They can render curves and surfaces in a variety of styles, and they can automatically handle adaptive subdivision that tessellates the domain into smaller triangles in regions of high curvature and near silhouette edges.</span></span> <span data-ttu-id="8cb1b-111">As funções NURBS se enquadram nas categorias a seguir.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-111">NURBS functions fall into the following categories.</span></span>

<span data-ttu-id="8cb1b-112">Para gerenciar um objeto NURBS, use:</span><span class="sxs-lookup"><span data-stu-id="8cb1b-112">To manage a NURBS object, use:</span></span>

-   <span data-ttu-id="8cb1b-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (criar um objeto NURBS)</span><span class="sxs-lookup"><span data-stu-id="8cb1b-113">[**gluNewNurbsRenderer**](glunewnurbsrenderer.md) (create a NURBS object)</span></span>
-   <span data-ttu-id="8cb1b-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (exclui um objeto NURBS)</span><span class="sxs-lookup"><span data-stu-id="8cb1b-114">[**gluDeleteNurbsRenderer**](gludeletenurbsrenderer.md) (deletes a NURBS object)</span></span>
-   <span data-ttu-id="8cb1b-115">[*gluNurbsCallback*](glunurbs.md) (estabelece uma função de tratamento de erros)</span><span class="sxs-lookup"><span data-stu-id="8cb1b-115">[*gluNurbsCallback*](glunurbs.md) (establishes an error-handling function)</span></span>

<span data-ttu-id="8cb1b-116">Para especificar as curvas desejadas, use:</span><span class="sxs-lookup"><span data-stu-id="8cb1b-116">To specify the desired curves, use:</span></span>

-   [<span data-ttu-id="8cb1b-117">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-117">**gluBeginCurve**</span></span>](glubegincurve.md)
-   [<span data-ttu-id="8cb1b-118">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-118">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="8cb1b-119">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-119">**gluEndCurve**</span></span>](gluendcurve.md)

<span data-ttu-id="8cb1b-120">Para especificar as superfícies desejadas, use:</span><span class="sxs-lookup"><span data-stu-id="8cb1b-120">To specify the desired surfaces, use:</span></span>

-   [<span data-ttu-id="8cb1b-121">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-121">**gluBeginSurface**</span></span>](glubeginsurface.md)
-   [<span data-ttu-id="8cb1b-122">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-122">**gluNurbsSurface**</span></span>](glunurbssurface.md)
-   [<span data-ttu-id="8cb1b-123">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-123">**gluEndSurface**</span></span>](gluendsurface.md)

<span data-ttu-id="8cb1b-124">Você também pode especificar uma região de corte, que define um subconjunto do domínio de superfície NURBS a ser avaliado para que você possa criar superfícies com limites suaves ou que contenham buracos.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-124">You can also specify a trimming region, which defines a subset of the NURBS surface domain to be evaluated so you can create surfaces that have smooth boundaries or that contain holes.</span></span>

<span data-ttu-id="8cb1b-125">Para especificar a região de corte, use:</span><span class="sxs-lookup"><span data-stu-id="8cb1b-125">To specify the trimming region, use:</span></span>

-   [<span data-ttu-id="8cb1b-126">**gluBeginTrim**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-126">**gluBeginTrim**</span></span>](glubegintrim.md)
-   [<span data-ttu-id="8cb1b-127">**gluPwlCurve**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-127">**gluPwlCurve**</span></span>](glupwlcurve.md)
-   [<span data-ttu-id="8cb1b-128">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-128">**gluNurbsCurve**</span></span>](glunurbscurve.md)
-   [<span data-ttu-id="8cb1b-129">**gluEndTrim**</span><span class="sxs-lookup"><span data-stu-id="8cb1b-129">**gluEndTrim**</span></span>](gluendtrim.md)

<span data-ttu-id="8cb1b-130">Assim como acontece com objetos Quadric, você pode controlar como as curvas NURBS e as superfícies são renderizadas.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-130">As with quadric objects, you can control how NURBS curves and surfaces are rendered.</span></span> <span data-ttu-id="8cb1b-131">Você pode determinar:</span><span class="sxs-lookup"><span data-stu-id="8cb1b-131">You can determine:</span></span>

-   <span data-ttu-id="8cb1b-132">Se deve-se descartar uma curva ou superfície cujo controle poliedde está fora do visor atual.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-132">Whether to discard a curve or surface whose control polyhedron lies outside the current viewport.</span></span>
-   <span data-ttu-id="8cb1b-133">O comprimento máximo (em pixels) das bordas dos polígonos usados para renderizar curvas e superfícies.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-133">The maximum length (in pixels) of edges of polygons used to render curves and surfaces.</span></span>
-   <span data-ttu-id="8cb1b-134">Se você vai pegar a matriz de projeção, a matriz modelview e o visor do servidor OpenGL ou fornecê-las explicitamente com [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span><span class="sxs-lookup"><span data-stu-id="8cb1b-134">Whether you will take the projection matrix, modelview matrix, and viewport from the OpenGL server or supply them explictly with [**gluLoadSamplingMatrices**](gluloadsamplingmatrices.md).</span></span>

<span data-ttu-id="8cb1b-135">Use [**gluNurbsProperty**](glunurbsproperty.md) para definir essas propriedades ou use os valores padrão.</span><span class="sxs-lookup"><span data-stu-id="8cb1b-135">Use [**gluNurbsProperty**](glunurbsproperty.md) to set these properties, or use the default values.</span></span> <span data-ttu-id="8cb1b-136">Você pode consultar um objeto NURBS sobre seu estilo de renderização com [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span><span class="sxs-lookup"><span data-stu-id="8cb1b-136">You can query a NURBS object about its rendering style with [**gluGetNurbsProperty**](glugetnurbsproperty.md).</span></span>

 

 




