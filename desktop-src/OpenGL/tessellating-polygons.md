---
title: Polígonos inclusão
description: Polígonos inclusão
ms.assetid: 3b219af0-96c3-4a83-8a40-bd7966d58398
keywords:
- Utilitário OpenGL (GLU), mosaico
- GLU (utilitário OpenGL), mosaico
- Utilitário OpenGL (GLU), polígonos simples
- GLU (utilitário OpenGL), polígonos simples
- polígonos simples OpenGL
- Utilitário OpenGL (GLU), polígonos complexos
- GLU (utilitário OpenGL), polígonos complexos
- polígonos complexos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 475076f6372042d61c1662b445b7573709134c65
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "105783256"
---
# <a name="tessellating-polygons"></a><span data-ttu-id="75fc6-111">Polígonos inclusão</span><span class="sxs-lookup"><span data-stu-id="75fc6-111">Tessellating Polygons</span></span>

<span data-ttu-id="75fc6-112">O OpenGL pode exibir diretamente apenas polígonos convexa simples.</span><span class="sxs-lookup"><span data-stu-id="75fc6-112">OpenGL can directly display only simple convex polygons.</span></span> <span data-ttu-id="75fc6-113">Um polígono é simples se:</span><span class="sxs-lookup"><span data-stu-id="75fc6-113">A polygon is simple if:</span></span>

-   <span data-ttu-id="75fc6-114">As bordas se cruzam somente em vértices.</span><span class="sxs-lookup"><span data-stu-id="75fc6-114">The edges intersect only at vertices.</span></span>
-   <span data-ttu-id="75fc6-115">Não há vértices duplicados.</span><span class="sxs-lookup"><span data-stu-id="75fc6-115">There are no duplicate vertices.</span></span>
-   <span data-ttu-id="75fc6-116">Exatamente duas bordas se encontram em qualquer vértice.</span><span class="sxs-lookup"><span data-stu-id="75fc6-116">Exactly two edges meet at any vertex.</span></span>

<span data-ttu-id="75fc6-117">Para exibir polígonos nonconvex simples ou polígonos simples contendo buracos, você deve primeiro triangular os polígonos (subdividir-os em polígonos do convexa).</span><span class="sxs-lookup"><span data-stu-id="75fc6-117">To display simple nonconvex polygons or simple polygons containing holes, you must first triangulate the polygons (subdivide them into convex polygons).</span></span> <span data-ttu-id="75fc6-118">Essa subdivisão é chamada de *mosaico*.</span><span class="sxs-lookup"><span data-stu-id="75fc6-118">Such subdivision is called *tessellation*.</span></span> <span data-ttu-id="75fc6-119">O GLU fornece uma coleção de funções que executam mosaico.</span><span class="sxs-lookup"><span data-stu-id="75fc6-119">GLU provides a collection of functions that perform tessellation.</span></span> <span data-ttu-id="75fc6-120">Observe que as funções de mosaico GLU não podem manipular polígonos não simples; Não há nenhum método OpenGL padrão para lidar com esses polígonos.</span><span class="sxs-lookup"><span data-stu-id="75fc6-120">Note that the GLU tessellation functions can't handle nonsimple polygons; there is no standard OpenGL method to handle such polygons.</span></span>

<span data-ttu-id="75fc6-121">Como o mosaico geralmente é necessário e pode ser bastante complicado, esta seção descreve as funções de mosaico GLU em detalhes.</span><span class="sxs-lookup"><span data-stu-id="75fc6-121">Because tessellation is often required and can be rather tricky, this section describes the GLU tessellation functions in detail.</span></span> <span data-ttu-id="75fc6-122">Essas funções utilizam como entrada polígonos simples arbitrários que podem incluir buracos e retornam alguma combinação de triângulos, malhas de triângulo e ventiladores de triângulo.</span><span class="sxs-lookup"><span data-stu-id="75fc6-122">These functions take as input arbitrary simple polygons that might include holes, and they return some combination of triangles, triangle meshes, and triangle fans.</span></span> <span data-ttu-id="75fc6-123">Se você não quiser lidar com malhas ou fãs, poderá especificar que as funções de mosaico retornem apenas triângulos.</span><span class="sxs-lookup"><span data-stu-id="75fc6-123">If you don't want to deal with meshes or fans, you can specify that the tessellation functions return only triangles.</span></span> <span data-ttu-id="75fc6-124">No entanto, as informações de malha e ventilador melhoram o desempenho.</span><span class="sxs-lookup"><span data-stu-id="75fc6-124">However, mesh and fan information improves performance.</span></span> <span data-ttu-id="75fc6-125">As funções de mosaico Polygon triangulam um polígono côncavo com um ou mais contornos.</span><span class="sxs-lookup"><span data-stu-id="75fc6-125">The polygon tessellation functions triangulate a concave polygon with one or more contours.</span></span>

<span data-ttu-id="75fc6-126">**Para usar o mosaico Polygon**</span><span class="sxs-lookup"><span data-stu-id="75fc6-126">**To use polygon tessellation**</span></span>

1.  <span data-ttu-id="75fc6-127">Crie um objeto de mosaico com [**gluNewTess**](glunewtess.md).</span><span class="sxs-lookup"><span data-stu-id="75fc6-127">Create a tessellation object with [**gluNewTess**](glunewtess.md).</span></span>
2.  <span data-ttu-id="75fc6-128">Use [*gluTessCallBack*](glutess.md) para definir as funções de retorno de chamada que serão usadas para processar os triângulos gerados pelo Tessellator.</span><span class="sxs-lookup"><span data-stu-id="75fc6-128">Use [*gluTessCallBack*](glutess.md) to define callback functions you will use to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="75fc6-129">Com [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md)e [**gluEndPolygon**](gluendpolygon.md), especifique o polígono com buracos ou o polígono côncavo para ser mosaico.</span><span class="sxs-lookup"><span data-stu-id="75fc6-129">With [**gluBeginPolygon**](glubeginpolygon.md), [**gluTessVertex**](glutessvertex.md), [**gluNextContour**](glunextcontour.md), and [**gluEndPolygon**](gluendpolygon.md), specify the polygon with holes or the concave polygon to be tessellated.</span></span>

    <span data-ttu-id="75fc6-130">Quando a descrição do polígono for concluída, o recurso de mosaico invocará suas funções de retorno de chamada conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="75fc6-130">When the polygon description is complete, the tessellation facility invokes your callback functions as necessary.</span></span>

    <span data-ttu-id="75fc6-131">Você pode destruir objetos de mosaico desnecessários com [**gluDeleteTess**](gludeletetess.md).</span><span class="sxs-lookup"><span data-stu-id="75fc6-131">You can destroy unneeded tessellation objects with [**gluDeleteTess**](gludeletetess.md).</span></span>

<span data-ttu-id="75fc6-132">Para obter mais informações sobre como salvar os dados de mosaico, consulte [usando funções de retorno de chamada](using-callback-functions.md).</span><span class="sxs-lookup"><span data-stu-id="75fc6-132">For more information on saving the tessellation data, see [Using Callback Functions](using-callback-functions.md).</span></span>

 

 




