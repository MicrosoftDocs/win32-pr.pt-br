---
title: Renderizando superfícies simples
description: A biblioteca GLU inclui um conjunto de funções para desenhar várias superfícies simples (diferir, cilindros, discos e partes de discos) em uma variedade de estilos e orientações. Essas funções são descritas em detalhes no manual de referência do OpenGL.
ms.assetid: 403bdf8d-de4c-49e2-87d0-11109061b4c2
keywords:
- Utilitário OpenGL (GLU), superfícies simples
- GLU (utilitário OpenGL), superfícies simples
- superfícies simples OpenGL
- Utilitário OpenGL (GLU),
- GLU (utilitário OpenGL),
- por meio do OpenGL
- Utilitário OpenGL (GLU), cilindros
- GLU (utilitário OpenGL), cilindros
- cilindros OpenGL
- Utilitário OpenGL (GLU), discos
- GLU (utilitário OpenGL), discos
- discos OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab766c661f89cbdec30b3295dfef8dc85b59f7fe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364475"
---
# <a name="rendering-simple-surfaces"></a><span data-ttu-id="f2440-116">Renderizando superfícies simples</span><span class="sxs-lookup"><span data-stu-id="f2440-116">Rendering Simple Surfaces</span></span>

<span data-ttu-id="f2440-117">A biblioteca GLU inclui um conjunto de funções para desenhar várias superfícies simples (diferir, cilindros, discos e partes de discos) em uma variedade de estilos e orientações.</span><span class="sxs-lookup"><span data-stu-id="f2440-117">The GLU library includes a set of functions for drawing various simple surfaces (spheres, cylinders, disks, and parts of disks) in a variety of styles and orientations.</span></span> <span data-ttu-id="f2440-118">Essas funções são descritas em detalhes no *manual de referência do OpenGL*.</span><span class="sxs-lookup"><span data-stu-id="f2440-118">These functions are described in detail in the *OpenGL Reference Manual*.</span></span>

<span data-ttu-id="f2440-119">**Para renderizar superfícies simples**</span><span class="sxs-lookup"><span data-stu-id="f2440-119">**To render simple surfaces**</span></span>

1.  <span data-ttu-id="f2440-120">Crie um objeto Quadric com [**gluNewQuadric**](glunewquadric.md).</span><span class="sxs-lookup"><span data-stu-id="f2440-120">Create a quadric object with [**gluNewQuadric**](glunewquadric.md).</span></span>

    <span data-ttu-id="f2440-121">Para destruir esse objeto quando tiver terminado, use [**gluDeleteQuadric**](gludeletequadric.md).</span><span class="sxs-lookup"><span data-stu-id="f2440-121">To destroy this object when you're finished with it, use [**gluDeleteQuadric**](gludeletequadric.md).</span></span>

2.  <span data-ttu-id="f2440-122">Especifique o estilo de renderização desejado, conforme listado abaixo, com a função apropriada (a menos que você esteja satisfeito com os valores padrão):</span><span class="sxs-lookup"><span data-stu-id="f2440-122">Specify the desired rendering style, as listed below, with the appropriate function (unless you're satisfied with the default values):</span></span>
    -   <span data-ttu-id="f2440-123">Se os normais da superfície devem ser gerados e, nesse caso, se deve haver um normal por vértice ou um normal por face: [ **gluQuadricNormals**](gluquadricnormals.md)</span><span class="sxs-lookup"><span data-stu-id="f2440-123">Whether surface normals should be generated, and if so, whether there should be one normal per vertex or one normal per face: [**gluQuadricNormals**](gluquadricnormals.md)</span></span>
    -   <span data-ttu-id="f2440-124">Se as coordenadas de textura devem ser geradas: [ **gluQuadricTexture**](gluquadrictexture.md)</span><span class="sxs-lookup"><span data-stu-id="f2440-124">Whether texture coordinates should be generated: [**gluQuadricTexture**](gluquadrictexture.md)</span></span>
    -   <span data-ttu-id="f2440-125">Qual lado do Quadric deve ser considerado o exterior e qual o interior: [ **gluQuadricOrientation**](gluquadricorientation.md)</span><span class="sxs-lookup"><span data-stu-id="f2440-125">Which side of the quadric should be considered the outside and which the inside: [**gluQuadricOrientation**](gluquadricorientation.md)</span></span>
    -   <span data-ttu-id="f2440-126">Se o Quadric deve ser desenhado como um conjunto de polígonos, linhas ou pontos: [ **gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span><span class="sxs-lookup"><span data-stu-id="f2440-126">Whether the quadric should be drawn as a set of polygons, lines, or points: [**gluQuadricDrawStyle**](gluquadricdrawstyle.md)</span></span>
3.  <span data-ttu-id="f2440-127">Depois de especificar o estilo de renderização, invoque a função de renderização para o tipo desejado de objeto Quadric: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md)ou [**gluPartialDisk**](glupartialdisk.md).</span><span class="sxs-lookup"><span data-stu-id="f2440-127">After specifying the rendering style, invoke the rendering function for the desired type of quadric object: [**gluSphere**](glusphere.md), [**gluCylinder**](glucylinder.md), [**gluDisk**](gludisk.md), or [**gluPartialDisk**](glupartialdisk.md).</span></span>

    <span data-ttu-id="f2440-128">Se ocorrer um erro durante a renderização, a função de tratamento de erros que você especificou com [*gluQuadricCallBack*](gluquadric.md) será invocada.</span><span class="sxs-lookup"><span data-stu-id="f2440-128">If an error occurs during rendering, the error-handling function you've specified with [*gluQuadricCallBack*](gluquadric.md) is invoked.</span></span>

<span data-ttu-id="f2440-129">Use os argumentos *\* RADIUS*, *Height* e similar, em vez da função [**glScale**](glscale.md) , para dimensionar o quadrics, para que você não precise renormalizar qualquer normal de comprimento de unidade gerado.</span><span class="sxs-lookup"><span data-stu-id="f2440-129">Use the *\*Radius*, *height*, and similar arguments, rather than the [**glScale**](glscale.md) function, to scale the quadrics, so that you don't have to renormalize any unit-length normals that are generated.</span></span> <span data-ttu-id="f2440-130">Para forçar cálculos de iluminação com uma granularidade mais refinada, especialmente se a especulação de material for alta, defina os argumentos *loops* e *pilhas* para valores diferentes de 1.</span><span class="sxs-lookup"><span data-stu-id="f2440-130">To force lighting calculations at a finer granularity, especially if the material specularity is high, set the *loops* and *stacks* arguments to values other than 1.</span></span>

 

 




