---
title: Portando funções de matriz e transformação
description: A íris GL e o OpenGL lidam com as matrizes e as transformações de maneira semelhante.
ms.assetid: 732ba65a-d776-43ea-a605-0f59209c9a46
keywords:
- Portabilidade do íris GL, matrizes
- portando do íris GL, matrizes
- portando para OpenGL do íris GL, matrizes
- Portabilidade OpenGL do íris GL, matrizes
- matrizes
- Portabilidade do íris GL, transformações
- portando do íris GL, transformações
- portando para OpenGL do íris GL, transformações
- Portabilidade do OpenGL do íris GL, transformações
- transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a1c6219640085370202b8dbebad9a2e9d4992b4f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292443"
---
# <a name="porting-matrix-and-transformation-functions"></a><span data-ttu-id="c20c0-113">Portando funções de matriz e transformação</span><span class="sxs-lookup"><span data-stu-id="c20c0-113">Porting Matrix and Transformation Functions</span></span>

<span data-ttu-id="c20c0-114">A íris GL e o OpenGL lidam com as matrizes e as transformações de maneira semelhante.</span><span class="sxs-lookup"><span data-stu-id="c20c0-114">IRIS GL and OpenGL handle matrices and transformations in a similar manner.</span></span> <span data-ttu-id="c20c0-115">Mas há várias diferenças a serem consideradas ao portar o código do íris GL:</span><span class="sxs-lookup"><span data-stu-id="c20c0-115">But there are several differences to keep in mind when porting code from IRIS GL:</span></span>

-   <span data-ttu-id="c20c0-116">No OpenGL, você está sempre no modo de matriz dupla; Não há um modo de matriz única.</span><span class="sxs-lookup"><span data-stu-id="c20c0-116">In OpenGL you are always in double-matrix mode; there is no single-matrix mode.</span></span>
-   <span data-ttu-id="c20c0-117">Os ângulos são medidos em graus, em vez de décimos de graus.</span><span class="sxs-lookup"><span data-stu-id="c20c0-117">Angles are measured in degrees, instead of tenths of degrees.</span></span>
-   <span data-ttu-id="c20c0-118">As chamadas de matriz de projeção, como [**glFrustum**](glfrustum.md) e [**glOrtho**](glortho.md), agora são multiplicadas na matriz atual, em vez de serem carregadas na matriz atual.</span><span class="sxs-lookup"><span data-stu-id="c20c0-118">Projection matrix calls, like [**glFrustum**](glfrustum.md) and [**glOrtho**](glortho.md), now multiply onto the current matrix, instead of being loaded onto the current matrix.</span></span>
-   <span data-ttu-id="c20c0-119">A função OpenGL, [**glRotate**](glrotate.md), é muito diferente da **rotação**.</span><span class="sxs-lookup"><span data-stu-id="c20c0-119">The OpenGL function, [**glRotate**](glrotate.md), is very different from **rotate**.</span></span> <span data-ttu-id="c20c0-120">Você pode girar em qualquer eixo arbitrário, em vez de ser confinado nos eixos x, y e z.</span><span class="sxs-lookup"><span data-stu-id="c20c0-120">You can rotate around any arbitrary axis, instead of being confined to the x-, y-, and z- axes.</span></span> <span data-ttu-id="c20c0-121">Por exemplo, você pode traduzir:</span><span class="sxs-lookup"><span data-stu-id="c20c0-121">For example, you can translate:</span></span>

    ```C++
    rotate(200*(i+1), 'z');
    ```

    

    <span data-ttu-id="c20c0-122">para:</span><span class="sxs-lookup"><span data-stu-id="c20c0-122">to:</span></span>

    ```C++
    glRotate(.1*(200*(i+1), 0.0, 0.0, 1.0);
    ```

    

    <span data-ttu-id="c20c0-123">Ao converter de **Rotate** para **glRotate** , você muda para graus de décimos de graus e substitui ' z ' por um vetor para o eixo z.</span><span class="sxs-lookup"><span data-stu-id="c20c0-123">When translating from **rotate** to **glRotate** you switch to degrees from tenths of degrees and replace 'z' with a vector for the z-axis.</span></span>

-   <span data-ttu-id="c20c0-124">O OpenGL não tem equivalente à função **polarview** .</span><span class="sxs-lookup"><span data-stu-id="c20c0-124">OpenGL has no equivalent to the **polarview** function.</span></span> <span data-ttu-id="c20c0-125">Você pode substituí-lo facilmente por uma tradução e três rotações.</span><span class="sxs-lookup"><span data-stu-id="c20c0-125">You can replace it easily with a translation and three rotations.</span></span> <span data-ttu-id="c20c0-126">Por exemplo, você pode traduzir:</span><span class="sxs-lookup"><span data-stu-id="c20c0-126">For example, you can translate:</span></span>

    ```C++
    polarview(distance, azimuth, incidence, twist);
     
    ```

    

    <span data-ttu-id="c20c0-127">para:</span><span class="sxs-lookup"><span data-stu-id="c20c0-127">to:</span></span>

    ```C++
    glTranslatef( 0.0, 0.0, -distance); 
    glRotatef( -twist * 10.0, 0.0, 0.0, 1.0); 
    glRotatef( -incidence * 10.0, 1.0, 0.0, 0.0); 
    glRotatef( -azimuth * 10.0, 0.0, 0.0, 1.0);
    ```

    

<span data-ttu-id="c20c0-128">A tabela a seguir lista as funções de matriz OpenGL e suas funções de íris GL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="c20c0-128">The following table lists the OpenGL matrix functions and their equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="c20c0-129">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="c20c0-129">IRIS GL function</span></span>              | <span data-ttu-id="c20c0-130">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="c20c0-130">OpenGL function</span></span>                                                                        | <span data-ttu-id="c20c0-131">Significado</span><span class="sxs-lookup"><span data-stu-id="c20c0-131">Meaning</span></span>                                                                                                                                                                        |
|-------------------------------|----------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c20c0-132">**mmode**</span><span class="sxs-lookup"><span data-stu-id="c20c0-132">**mmode**</span></span>                     | [<span data-ttu-id="c20c0-133">**glMatrixMode**</span><span class="sxs-lookup"><span data-stu-id="c20c0-133">**glMatrixMode**</span></span>](glmatrixmode.md)                                                   | <span data-ttu-id="c20c0-134">Define o modo de matriz atual.</span><span class="sxs-lookup"><span data-stu-id="c20c0-134">Sets current matrix mode.</span></span>                                                                                                                                                      |
|                               | [<span data-ttu-id="c20c0-135">**glLoadIdentity**</span><span class="sxs-lookup"><span data-stu-id="c20c0-135">**glLoadIdentity**</span></span>](glloadidentity.md)                                               | <span data-ttu-id="c20c0-136">Substitui a matriz atual pela matriz de identidade.</span><span class="sxs-lookup"><span data-stu-id="c20c0-136">Replaces current matrix with the identity matrix.</span></span>                                                                                                                              |
| <span data-ttu-id="c20c0-137">**loadmatrix**</span><span class="sxs-lookup"><span data-stu-id="c20c0-137">**loadmatrix**</span></span>                | <span data-ttu-id="c20c0-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="c20c0-138">[**glLoadMatrixf**](glloadmatrix.md),[**glLoadMatrixd**](glloadmatrix.md)</span></span><br/> | <span data-ttu-id="c20c0-139">Substitui a matriz atual pela matriz especificada.</span><span class="sxs-lookup"><span data-stu-id="c20c0-139">Replaces current matrix with the specified matrix.</span></span>                                                                                                                             |
| <span data-ttu-id="c20c0-140">**multmatrix**</span><span class="sxs-lookup"><span data-stu-id="c20c0-140">**multmatrix**</span></span>                | <span data-ttu-id="c20c0-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span><span class="sxs-lookup"><span data-stu-id="c20c0-141">[**glMultMatrixf**](glmultmatrix.md),[**glMultMatrixd**](glmultmatrix.md)</span></span><br/> | <span data-ttu-id="c20c0-142">Pós-multiplica a matriz atual pela matriz especificada (Observe que **multmatrix** pré-multiplicado).</span><span class="sxs-lookup"><span data-stu-id="c20c0-142">Post-multiplies current matrix with the specified matrix (note that **multmatrix** pre-multiplied).</span></span>                                                                            |
| <span data-ttu-id="c20c0-143">**mapw**, **mapw2**</span><span class="sxs-lookup"><span data-stu-id="c20c0-143">**mapw**, **mapw2**</span></span>           | [<span data-ttu-id="c20c0-144">**gluUnProject**</span><span class="sxs-lookup"><span data-stu-id="c20c0-144">**gluUnProject**</span></span>](gluunproject.md)                                                   | <span data-ttu-id="c20c0-145">Projetos coordenadas de espaço do mundo para espaço de objeto (consulte também [**gluProject**](gluproject.md)).</span><span class="sxs-lookup"><span data-stu-id="c20c0-145">Projects world-space coordinates to object space (see also [**gluProject**](gluproject.md)).</span></span>                                                                                  |
| <span data-ttu-id="c20c0-146">**ortho**</span><span class="sxs-lookup"><span data-stu-id="c20c0-146">**ortho**</span></span>                     | [<span data-ttu-id="c20c0-147">**glOrtho**</span><span class="sxs-lookup"><span data-stu-id="c20c0-147">**glOrtho**</span></span>](glortho.md)                                                             | <span data-ttu-id="c20c0-148">Multiplica a matriz atual por uma matriz de projeção ortográfica.</span><span class="sxs-lookup"><span data-stu-id="c20c0-148">Multiplies current matrix by an orthographic projection matrix.</span></span>                                                                                                                |
| <span data-ttu-id="c20c0-149">**ortho2**</span><span class="sxs-lookup"><span data-stu-id="c20c0-149">**ortho2**</span></span>                    | [<span data-ttu-id="c20c0-150">**gluOrtho2D**</span><span class="sxs-lookup"><span data-stu-id="c20c0-150">**gluOrtho2D**</span></span>](gluortho2d.md)                                                       | <span data-ttu-id="c20c0-151">Define uma matriz de projeção ortográfica bidimensional.</span><span class="sxs-lookup"><span data-stu-id="c20c0-151">Defines a two-dimensional orthographic projection matrix.</span></span>                                                                                                                      |
| <span data-ttu-id="c20c0-152">**perspectiva**</span><span class="sxs-lookup"><span data-stu-id="c20c0-152">**perspective**</span></span>               | [<span data-ttu-id="c20c0-153">**gluPerspective**</span><span class="sxs-lookup"><span data-stu-id="c20c0-153">**gluPerspective**</span></span>](gluperspective.md)                                               | <span data-ttu-id="c20c0-154">Define uma matriz de projeção em perspectiva.</span><span class="sxs-lookup"><span data-stu-id="c20c0-154">Defines a perspective projection matrix.</span></span>                                                                                                                                       |
| <span data-ttu-id="c20c0-155">**picksize**</span><span class="sxs-lookup"><span data-stu-id="c20c0-155">**picksize**</span></span>                  | [<span data-ttu-id="c20c0-156">**gluPickMatrix**</span><span class="sxs-lookup"><span data-stu-id="c20c0-156">**gluPickMatrix**</span></span>](glupickmatrix.md)                                                 | <span data-ttu-id="c20c0-157">Define uma região de separação.</span><span class="sxs-lookup"><span data-stu-id="c20c0-157">Defines a picking region.</span></span>                                                                                                                                                      |
| <span data-ttu-id="c20c0-158">**popmatrix**</span><span class="sxs-lookup"><span data-stu-id="c20c0-158">**popmatrix**</span></span>                 | [<span data-ttu-id="c20c0-159">**glPopMatrix**</span><span class="sxs-lookup"><span data-stu-id="c20c0-159">**glPopMatrix**</span></span>](glpopmatrix.md)                                                     | <span data-ttu-id="c20c0-160">Exibe a pilha de matriz atual, substituindo a matriz atual pela outra abaixo dela.</span><span class="sxs-lookup"><span data-stu-id="c20c0-160">Pops current matrix stack, replacing the current matrix with the one below it.</span></span>                                                                                                 |
| <span data-ttu-id="c20c0-161">**pushmatrix**</span><span class="sxs-lookup"><span data-stu-id="c20c0-161">**pushmatrix**</span></span>                | [<span data-ttu-id="c20c0-162">**glPushMatrix**</span><span class="sxs-lookup"><span data-stu-id="c20c0-162">**glPushMatrix**</span></span>](glpushmatrix.md)                                                   | <span data-ttu-id="c20c0-163">Envia por push a pilha da matriz atual por uma, duplicando a matriz atual.</span><span class="sxs-lookup"><span data-stu-id="c20c0-163">Pushes current matrix stack down by one, duplicating the current matrix.</span></span>                                                                                                       |
| <span data-ttu-id="c20c0-164">**girar**,**corrompidos**</span><span class="sxs-lookup"><span data-stu-id="c20c0-164">**rotate**,**rot**</span></span><br/> | <span data-ttu-id="c20c0-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span><span class="sxs-lookup"><span data-stu-id="c20c0-165">[**glRotated**](glrotate.md),[**glRotatef**](glrotate.md)</span></span><br/>                 | <span data-ttu-id="c20c0-166">Gira o sistema de coordenadas atual pelo ângulo fornecido sobre o vetor da origem por meio de um determinado ponto.</span><span class="sxs-lookup"><span data-stu-id="c20c0-166">Rotates current coordinate system by the given angle about the vector from the origin through the given point.</span></span> <span data-ttu-id="c20c0-167">Observe que **girar** girado apenas sobre os eixos x-, y-e z.</span><span class="sxs-lookup"><span data-stu-id="c20c0-167">Note that **rotate** rotated only about the x-, y-, and z-axes.</span></span> |
| <span data-ttu-id="c20c0-168">**scale**</span><span class="sxs-lookup"><span data-stu-id="c20c0-168">**scale**</span></span>                     | <span data-ttu-id="c20c0-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span><span class="sxs-lookup"><span data-stu-id="c20c0-169">[**glScaled**](glscale.md),[**glScalef**](glscale.md)</span></span><br/>                     | <span data-ttu-id="c20c0-170">Multiplica a matriz atual por uma matriz de dimensionamento.</span><span class="sxs-lookup"><span data-stu-id="c20c0-170">Multiplies current matrix by a scaling matrix.</span></span>                                                                                                                                 |
| <span data-ttu-id="c20c0-171">**Traduzir**</span><span class="sxs-lookup"><span data-stu-id="c20c0-171">**translate**</span></span>                 | <span data-ttu-id="c20c0-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span><span class="sxs-lookup"><span data-stu-id="c20c0-172">[**glTranslatef**](gltranslate.md),[**glTranslated**](gltranslate.md)</span></span><br/>     | <span data-ttu-id="c20c0-173">Move a origem do sistema de coordenadas para o ponto especificado, multiplicando a matriz atual por uma matriz de conversão.</span><span class="sxs-lookup"><span data-stu-id="c20c0-173">Moves coordinate-system origin to the point specified, by multiplying the current matrix by a translation matrix.</span></span>                                                              |
| <span data-ttu-id="c20c0-174">**Window**</span><span class="sxs-lookup"><span data-stu-id="c20c0-174">**window**</span></span>                    | [<span data-ttu-id="c20c0-175">**glFrustum**</span><span class="sxs-lookup"><span data-stu-id="c20c0-175">**glFrustum**</span></span>](glfrustum.md)                                                         | <span data-ttu-id="c20c0-176">As coordenadas fornecidas para os planos de recorte, multiplicam a matriz atual por uma matriz de perspectiva.</span><span class="sxs-lookup"><span data-stu-id="c20c0-176">Given coordinates for clipping planes, multiplies the current matrix by a perspective matrix.</span></span>                                                                                  |



 

<span data-ttu-id="c20c0-177">O OpenGL tem três modos de matriz, que são definidos com [**glMatrixMode**](glmatrixmode.md).</span><span class="sxs-lookup"><span data-stu-id="c20c0-177">OpenGL has three matrix modes, which are set with [**glMatrixMode**](glmatrixmode.md).</span></span> <span data-ttu-id="c20c0-178">A tabela a seguir lista os modos disponíveis como parâmetros para **glMatrixMode**.</span><span class="sxs-lookup"><span data-stu-id="c20c0-178">The following table lists the modes available as parameters for **glMatrixMode**.</span></span>



| <span data-ttu-id="c20c0-179">Modo de matriz do íris GL</span><span class="sxs-lookup"><span data-stu-id="c20c0-179">IRIS GL matrix mode</span></span> | <span data-ttu-id="c20c0-180">Modo OpenGL</span><span class="sxs-lookup"><span data-stu-id="c20c0-180">OpenGL mode</span></span>    | <span data-ttu-id="c20c0-181">Significado</span><span class="sxs-lookup"><span data-stu-id="c20c0-181">Meaning</span></span>                                  | <span data-ttu-id="c20c0-182">Profundidade mínima da pilha</span><span class="sxs-lookup"><span data-stu-id="c20c0-182">Min stack depth</span></span> |
|---------------------|----------------|------------------------------------------|-----------------|
| <span data-ttu-id="c20c0-183">**MTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="c20c0-183">**MTEXTURE**</span></span>        | <span data-ttu-id="c20c0-184">\_textura GL</span><span class="sxs-lookup"><span data-stu-id="c20c0-184">GL\_TEXTURE</span></span>    | <span data-ttu-id="c20c0-185">Opera na pilha da matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="c20c0-185">Operates on the texture matrix stack.</span></span>    | <span data-ttu-id="c20c0-186">2</span><span class="sxs-lookup"><span data-stu-id="c20c0-186">2</span></span>               |
| <span data-ttu-id="c20c0-187">**MVIEWING**</span><span class="sxs-lookup"><span data-stu-id="c20c0-187">**MVIEWING**</span></span>        | <span data-ttu-id="c20c0-188">\_MODELVIEW GL</span><span class="sxs-lookup"><span data-stu-id="c20c0-188">GL\_MODELVIEW</span></span>  | <span data-ttu-id="c20c0-189">Opera na pilha de matrizes de exibição de modelo.</span><span class="sxs-lookup"><span data-stu-id="c20c0-189">Operates on the model view matrix stack.</span></span> | <span data-ttu-id="c20c0-190">32</span><span class="sxs-lookup"><span data-stu-id="c20c0-190">32</span></span>              |
| <span data-ttu-id="c20c0-191">**MPROJECTION**</span><span class="sxs-lookup"><span data-stu-id="c20c0-191">**MPROJECTION**</span></span>     | <span data-ttu-id="c20c0-192">\_projeção GL</span><span class="sxs-lookup"><span data-stu-id="c20c0-192">GL\_PROJECTION</span></span> | <span data-ttu-id="c20c0-193">Opera na pilha matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="c20c0-193">Operates on the projection matrix stack.</span></span> | <span data-ttu-id="c20c0-194">2</span><span class="sxs-lookup"><span data-stu-id="c20c0-194">2</span></span>               |



 

 

 





