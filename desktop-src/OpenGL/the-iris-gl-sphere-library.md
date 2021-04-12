---
title: A biblioteca de Sphere do íris GL
description: O OpenGL não dá suporte à biblioteca de Sphere do íris GL. Você pode substituir suas chamadas de biblioteca de Sphere por rotinas quadrics da biblioteca GLU. Para obter mais informações sobre a biblioteca GLU, consulte o guia de programação Open GL e a biblioteca de utilitários OpenGL.
ms.assetid: 2b7e6a3d-d2d0-4b54-8dff-8c4d6b113007
keywords:
- Portabilidade do íris GL, biblioteca de Sphere
- portando do íris GL, biblioteca de Sphere
- portando para OpenGL do íris GL, biblioteca de Sphere
- Portabilidade do OpenGL do íris GL, biblioteca de Sphere
- funções de desenho, biblioteca de Sphere
- biblioteca de Sphere
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 586974c5874aee73121e536cbadca4564a18c250
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292349"
---
# <a name="the-iris-gl-sphere-library"></a><span data-ttu-id="96cbc-111">A biblioteca de Sphere do íris GL</span><span class="sxs-lookup"><span data-stu-id="96cbc-111">The IRIS GL Sphere Library</span></span>

<span data-ttu-id="96cbc-112">O OpenGL não dá suporte à biblioteca de Sphere do íris GL.</span><span class="sxs-lookup"><span data-stu-id="96cbc-112">OpenGL does not support the IRIS GL sphere library.</span></span> <span data-ttu-id="96cbc-113">Você pode substituir suas chamadas de biblioteca de Sphere por rotinas quadrics da biblioteca GLU.</span><span class="sxs-lookup"><span data-stu-id="96cbc-113">You can replace your sphere library calls with quadrics routines from the GLU library.</span></span> <span data-ttu-id="96cbc-114">Para obter mais informações sobre a biblioteca GLU, consulte o *Guia de programação Open GL* e a [biblioteca de utilitários OpenGL](opengl-utility-library.md).</span><span class="sxs-lookup"><span data-stu-id="96cbc-114">For more information about the GLU library, see the *Open GL Programming Guide* and [OpenGL Utility Library](opengl-utility-library.md).</span></span>

<span data-ttu-id="96cbc-115">A tabela a seguir lista as funções OpenGL quadrics.</span><span class="sxs-lookup"><span data-stu-id="96cbc-115">The following table lists the OpenGL quadrics functions.</span></span>



| <span data-ttu-id="96cbc-116">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="96cbc-116">OpenGL function</span></span>                                        | <span data-ttu-id="96cbc-117">Significado</span><span class="sxs-lookup"><span data-stu-id="96cbc-117">Meaning</span></span>                                                          |
|--------------------------------------------------------|------------------------------------------------------------------|
| [<span data-ttu-id="96cbc-118">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="96cbc-118">**gluNewQuadric**</span></span>](glunewquadric.md)                 | <span data-ttu-id="96cbc-119">Cria um novo objeto Quadric.</span><span class="sxs-lookup"><span data-stu-id="96cbc-119">Creates a new quadric object.</span></span>                                    |
| [<span data-ttu-id="96cbc-120">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="96cbc-120">**gluDeleteQuadric**</span></span>](gludeletequadric.md)           | <span data-ttu-id="96cbc-121">Exclui um objeto Quadric.</span><span class="sxs-lookup"><span data-stu-id="96cbc-121">Deletes a quadric object.</span></span>                                        |
| [<span data-ttu-id="96cbc-122">*gluQuadricCallback*</span><span class="sxs-lookup"><span data-stu-id="96cbc-122">*gluQuadricCallback*</span></span>](gluquadric.md)                 | <span data-ttu-id="96cbc-123">Associa um retorno de chamada a um objeto Quadric, para tratamento de erros.</span><span class="sxs-lookup"><span data-stu-id="96cbc-123">Associates a callback with a quadric object, for error handling.</span></span> |
| [<span data-ttu-id="96cbc-124">**gluQuadricNormals**</span><span class="sxs-lookup"><span data-stu-id="96cbc-124">**gluQuadricNormals**</span></span>](gluquadricnormals.md)         | <span data-ttu-id="96cbc-125">Especifica Normals: não há normalidades, uma por face ou uma por vértice.</span><span class="sxs-lookup"><span data-stu-id="96cbc-125">Specifies normals: no normals, one per face, or one per vertex.</span></span>  |
| [<span data-ttu-id="96cbc-126">**gluQuadricOrientation**</span><span class="sxs-lookup"><span data-stu-id="96cbc-126">**gluQuadricOrientation**</span></span>](gluquadricorientation.md) | <span data-ttu-id="96cbc-127">Especifica a direção de Normals: para fora ou para dentro.</span><span class="sxs-lookup"><span data-stu-id="96cbc-127">Specifies direction of normals: outward or inward.</span></span>               |
| [<span data-ttu-id="96cbc-128">**gluQuadricTexture**</span><span class="sxs-lookup"><span data-stu-id="96cbc-128">**gluQuadricTexture**</span></span>](gluquadrictexture.md)         | <span data-ttu-id="96cbc-129">Ativa ou desativa a geração da coordenada de textura.</span><span class="sxs-lookup"><span data-stu-id="96cbc-129">Turns texture-coordinate generation on or off.</span></span>                   |
| [<span data-ttu-id="96cbc-130">**gluQuadricDrawstyle**</span><span class="sxs-lookup"><span data-stu-id="96cbc-130">**gluQuadricDrawstyle**</span></span>](gluquadricdrawstyle.md)     | <span data-ttu-id="96cbc-131">Especifica o estilo de desenho: polígonos, linhas, pontos e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="96cbc-131">Specifies drawing style: polygons, lines, points, and so on.</span></span>     |
| [<span data-ttu-id="96cbc-132">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="96cbc-132">**gluSphere**</span></span>](glusphere.md)                         | <span data-ttu-id="96cbc-133">Desenha uma esfera.</span><span class="sxs-lookup"><span data-stu-id="96cbc-133">Draws a sphere.</span></span>                                                  |
| [<span data-ttu-id="96cbc-134">**gluCylinder**</span><span class="sxs-lookup"><span data-stu-id="96cbc-134">**gluCylinder**</span></span>](glucylinder.md)                     | <span data-ttu-id="96cbc-135">Desenha um cilindro ou cone.</span><span class="sxs-lookup"><span data-stu-id="96cbc-135">Draws a cylinder or cone.</span></span>                                        |
| [<span data-ttu-id="96cbc-136">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="96cbc-136">**gluPartialDisk**</span></span>](glupartialdisk.md)               | <span data-ttu-id="96cbc-137">Desenha um arco.</span><span class="sxs-lookup"><span data-stu-id="96cbc-137">Draws an arc.</span></span>                                                    |
| [<span data-ttu-id="96cbc-138">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="96cbc-138">**gluDisk**</span></span>](gludisk.md)                             | <span data-ttu-id="96cbc-139">Desenha um círculo ou disco.</span><span class="sxs-lookup"><span data-stu-id="96cbc-139">Draws a circle or disk.</span></span>                                          |



 

<span data-ttu-id="96cbc-140">Você pode usar um objeto Quadric para todos os quadrics que você deseja renderizar de maneiras semelhantes.</span><span class="sxs-lookup"><span data-stu-id="96cbc-140">You can use one quadric object for all quadrics you want to render in similar ways.</span></span> <span data-ttu-id="96cbc-141">O exemplo de código a seguir usa dois objetos Quadric para desenhar quatro quadrics, dois deles texturizados.</span><span class="sxs-lookup"><span data-stu-id="96cbc-141">The following code sample uses two quadric objects to draw four quadrics, two of them textured.</span></span>


```C++
GLUquadricObj    *texturedQuad, *plainQuad; 
 
texturedQuad = gluNewQuadric(void); 
gluQuadricTexture(texturedQuad, GL_TRUE); 
gluQuadricOrientation(texturedQuad, GLU_OUTSIDE); 
gluQuadricDrawStyle(texturedQuad, GLU_FILL); 
 
plainQuad = gluNewQuadric(void); 
gluQuadricDrawStyle(plainQuad, GLU_LINE); 
 
glColor3f (1.0, 1.0, 1.0); 
 
gluSphere(texturedQuad, 5.0, 20, 20); 
glTranslatef(10.0, 10.0, 0.0); 
gluCylinder(texturedQuad, 2.5, 5, 5, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluDisk(plainQuad, 2.0, 5.0, 10, 10); 
glTranslatef(10.0, 10.0, 0.0); 
gluSphere(plainQuad, 5.0, 20, 20);
```



 

 




