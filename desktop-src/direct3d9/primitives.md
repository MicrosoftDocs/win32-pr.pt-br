---
description: Um primitivo 3D é uma coleção de vértices que forma uma única entidade 3D. A primitiva mais simples é uma coleção de pontos em um sistema de coordenadas 3D, que é chamada de lista de pontos.
ms.assetid: vs|directx_sdk|~\primitives.htm
title: Primitivos (gráficos do Direct3D 9)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38916e85add69574a2437b0e48c209b14a341e44
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/06/2021
ms.locfileid: "104087243"
---
# <a name="primitives-direct3d-9-graphics"></a><span data-ttu-id="cd264-104">Primitivos (gráficos do Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cd264-104">Primitives (Direct3D 9 Graphics)</span></span>

<span data-ttu-id="cd264-105">Um primitivo 3D é uma coleção de vértices que forma uma única entidade 3D.</span><span class="sxs-lookup"><span data-stu-id="cd264-105">A 3D primitive is a collection of vertices that form a single 3D entity.</span></span> <span data-ttu-id="cd264-106">A primitiva mais simples é uma coleção de pontos em um sistema de coordenadas 3D, que é chamada de lista de pontos.</span><span class="sxs-lookup"><span data-stu-id="cd264-106">The simplest primitive is a collection of points in a 3D coordinate system, which is called a point list.</span></span>

<span data-ttu-id="cd264-107">Geralmente, os primitivos 3D são polígonos.</span><span class="sxs-lookup"><span data-stu-id="cd264-107">Often, 3D primitives are polygons.</span></span> <span data-ttu-id="cd264-108">Um polígono é uma figura 3D fechada delineada por pelo menos três vértices.</span><span class="sxs-lookup"><span data-stu-id="cd264-108">A polygon is a closed 3D figure delineated by at least three vertices.</span></span> <span data-ttu-id="cd264-109">O polígono mais simples é um triângulo.</span><span class="sxs-lookup"><span data-stu-id="cd264-109">The simplest polygon is a triangle.</span></span> <span data-ttu-id="cd264-110">O Microsoft Direct3D usa triângulos para compor a maior parte de seus polígonos porque é garantido que todos os três vértices de um triângulo serão coplanares.</span><span class="sxs-lookup"><span data-stu-id="cd264-110">Microsoft Direct3D uses triangles to compose most of its polygons because all three vertices in a triangle are guaranteed to be coplanar.</span></span> <span data-ttu-id="cd264-111">Renderizar vértices que não são planares é ineficiente.</span><span class="sxs-lookup"><span data-stu-id="cd264-111">Rendering nonplanar vertices is inefficient.</span></span> <span data-ttu-id="cd264-112">Você pode combinar triângulos para formar malhas e polígonos grandes e complexos.</span><span class="sxs-lookup"><span data-stu-id="cd264-112">You can combine triangles to form large, complex polygons and meshes.</span></span>

<span data-ttu-id="cd264-113">A ilustração a seguir mostra um cubo.</span><span class="sxs-lookup"><span data-stu-id="cd264-113">The following illustration shows a cube.</span></span> <span data-ttu-id="cd264-114">Dois triângulos formam cada face do cubo.</span><span class="sxs-lookup"><span data-stu-id="cd264-114">Two triangles form each face of the cube.</span></span> <span data-ttu-id="cd264-115">Todo o conjunto de triângulos constitui um primitivo cúbico.</span><span class="sxs-lookup"><span data-stu-id="cd264-115">The entire set of triangles forms one cubic primitive.</span></span> <span data-ttu-id="cd264-116">Você pode aplicar texturas e materiais às superfícies de primitivos para que pareçam ser um único Formulário sólido.</span><span class="sxs-lookup"><span data-stu-id="cd264-116">You can apply textures and materials to the surfaces of primitives to make them appear to be a single solid form.</span></span> <span data-ttu-id="cd264-117">Para obter detalhes, confira [materiais (Direct3D 9)](materials.md) e [texturas do Direct3D (Direct3D 9)](direct3d-textures.md).</span><span class="sxs-lookup"><span data-stu-id="cd264-117">For details, see [Materials (Direct3D 9)](materials.md) and [Direct3D Textures (Direct3D 9)](direct3d-textures.md).</span></span>

![ilustração de um cubo com dois triângulos em cada face](images/cube3d.png)

<span data-ttu-id="cd264-119">Você também pode usar triângulos para criar primitivos cujas superfícies parecem ser curvas suaves.</span><span class="sxs-lookup"><span data-stu-id="cd264-119">You can also use triangles to create primitives whose surfaces appear to be smooth curves.</span></span> <span data-ttu-id="cd264-120">A ilustração a seguir mostra como uma esfera pode ser simulada com triângulos.</span><span class="sxs-lookup"><span data-stu-id="cd264-120">The following illustration shows how a sphere can be simulated with triangles.</span></span> <span data-ttu-id="cd264-121">Depois que um material é aplicado, a esfera é curvada quando é renderizada.</span><span class="sxs-lookup"><span data-stu-id="cd264-121">After a material is applied, the sphere looks curved when it is rendered.</span></span> <span data-ttu-id="cd264-122">Isso é especialmente verdadeiro se você usar o sombreamento Gouraud.</span><span class="sxs-lookup"><span data-stu-id="cd264-122">This is especially true if you use Gouraud shading.</span></span> <span data-ttu-id="cd264-123">Para obter detalhes, consulte [sombreamento Gouraud](shading-modes.md).</span><span class="sxs-lookup"><span data-stu-id="cd264-123">For details, see [Gouraud Shading](shading-modes.md).</span></span>

![ilustração de uma esfera simulada usando triângulos](images/sphere3d.png)

<span data-ttu-id="cd264-125">Os dispositivos Direct3D podem criar e manipular os seguintes tipos de primitivos.</span><span class="sxs-lookup"><span data-stu-id="cd264-125">Direct3D devices can create and manipulate the following types of primitives.</span></span>

-   [<span data-ttu-id="cd264-126">Listas de pontos</span><span class="sxs-lookup"><span data-stu-id="cd264-126">Point Lists</span></span>](point-lists.md)
-   [<span data-ttu-id="cd264-127">Listas de linhas</span><span class="sxs-lookup"><span data-stu-id="cd264-127">Line Lists</span></span>](line-lists.md)
-   [<span data-ttu-id="cd264-128">Faixas de linha</span><span class="sxs-lookup"><span data-stu-id="cd264-128">Line Strips</span></span>](line-strips.md)
-   [<span data-ttu-id="cd264-129">Listas de triângulo</span><span class="sxs-lookup"><span data-stu-id="cd264-129">Triangle Lists</span></span>](triangle-lists.md)
-   [<span data-ttu-id="cd264-130">Faixas de triângulo</span><span class="sxs-lookup"><span data-stu-id="cd264-130">Triangle Strips</span></span>](triangle-strips.md)
-   [<span data-ttu-id="cd264-131">Ventiladores de triângulo (Direct3D 9)</span><span class="sxs-lookup"><span data-stu-id="cd264-131">Triangle Fans (Direct3D 9)</span></span>](triangle-fans.md)

<span data-ttu-id="cd264-132">Você pode renderizar tipos primitivos de um aplicativo C++ com qualquer um dos métodos de renderização da interface [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) .</span><span class="sxs-lookup"><span data-stu-id="cd264-132">You can render primitive types from a C++ application with any of the rendering methods of the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface.</span></span>

## <a name="related-topics"></a><span data-ttu-id="cd264-133">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cd264-133">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cd264-134">Dispositivos Direct3D</span><span class="sxs-lookup"><span data-stu-id="cd264-134">Direct3D Devices</span></span>](direct3d-devices.md)
</dt> </dl>

 

 
