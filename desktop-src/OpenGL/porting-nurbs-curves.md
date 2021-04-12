---
title: Portando curvas NURBS
description: As funções OpenGL para desenhar curvas NURBS são muito semelhantes às funções do íris GL. Você especifica sequências de nós e pontos de controle usando uma função gluNurbsCurve, que deve estar contida em um par gluBeginCurve/gluEndCurve.
ms.assetid: 954e8029-06bd-4072-9b84-53ecba1d05da
keywords:
- Portabilidade do íris GL, curvas NURBS
- portando do íris GL, curvas NURBS
- portando para OpenGL do íris GL, curvas NURBS
- Portabilidade do OpenGL do íris GL, curvas NURBS
- Curvas NURBS
- curvas
- Portabilidade do íris GL, curvas
- portando do íris GL, curvas
- portando para OpenGL do íris GL, curvas
- Portabilidade OpenGL do íris GL, curvas
- NURBS (B racional não uniforme-spline)
- B-spline racional não uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f539e466ce8ade17d135c9369e1f641831792e2
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364176"
---
# <a name="porting-nurbs-curves"></a><span data-ttu-id="a9f92-116">Portando curvas NURBS</span><span class="sxs-lookup"><span data-stu-id="a9f92-116">Porting NURBS Curves</span></span>

<span data-ttu-id="a9f92-117">As funções OpenGL para desenhar curvas NURBS são muito semelhantes às funções do íris GL.</span><span class="sxs-lookup"><span data-stu-id="a9f92-117">The OpenGL functions for drawing NURBS curves are very similar to the IRIS GL functions.</span></span> <span data-ttu-id="a9f92-118">Você especifica sequências de nós e pontos de controle usando uma função [**gluNurbsCurve**](glunurbscurve.md) , que deve estar contida em um par [**gluBeginCurve**](glubegincurve.md)  /  [**gluEndCurve**](gluendcurve.md) .</span><span class="sxs-lookup"><span data-stu-id="a9f92-118">You specify knot sequences and control points using a [**gluNurbsCurve**](glunurbscurve.md) function, which must be contained within a [**gluBeginCurve**](glubegincurve.md) / [**gluEndCurve**](gluendcurve.md) pair.</span></span>

<span data-ttu-id="a9f92-119">A tabela a seguir lista as funções do íris GL para desenhar curvas NURBS e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="a9f92-119">The following table lists the IRIS GL functions for drawing NURBS curves and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="a9f92-120">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="a9f92-120">IRIS GL function</span></span> | <span data-ttu-id="a9f92-121">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="a9f92-121">OpenGL function</span></span>                        | <span data-ttu-id="a9f92-122">Significado</span><span class="sxs-lookup"><span data-stu-id="a9f92-122">Meaning</span></span>                     |
|------------------|----------------------------------------|-----------------------------|
| <span data-ttu-id="a9f92-123">**bgncurve**</span><span class="sxs-lookup"><span data-stu-id="a9f92-123">**bgncurve**</span></span>     | [<span data-ttu-id="a9f92-124">**gluBeginCurve**</span><span class="sxs-lookup"><span data-stu-id="a9f92-124">**gluBeginCurve**</span></span>](glubegincurve.md) | <span data-ttu-id="a9f92-125">Inicia uma definição de curva.</span><span class="sxs-lookup"><span data-stu-id="a9f92-125">Begins a curve definition.</span></span>  |
| <span data-ttu-id="a9f92-126">**nurbscurve**</span><span class="sxs-lookup"><span data-stu-id="a9f92-126">**nurbscurve**</span></span>   | [<span data-ttu-id="a9f92-127">**gluNurbsCurve**</span><span class="sxs-lookup"><span data-stu-id="a9f92-127">**gluNurbsCurve**</span></span>](glunurbscurve.md) | <span data-ttu-id="a9f92-128">Especifica atributos de curva.</span><span class="sxs-lookup"><span data-stu-id="a9f92-128">Specifies curve attributes.</span></span> |
| <span data-ttu-id="a9f92-129">**curva de fim**</span><span class="sxs-lookup"><span data-stu-id="a9f92-129">**endcurve**</span></span>     | [<span data-ttu-id="a9f92-130">**gluEndCurve**</span><span class="sxs-lookup"><span data-stu-id="a9f92-130">**gluEndCurve**</span></span>](gluendcurve.md)     | <span data-ttu-id="a9f92-131">Termina uma definição de curva.</span><span class="sxs-lookup"><span data-stu-id="a9f92-131">Ends a curve definition.</span></span>    |



 

<span data-ttu-id="a9f92-132">Associe as coordenadas de posição, textura e cor apresentando cada uma delas como um **gluNurbsCurve** separado dentro do par de início/término.</span><span class="sxs-lookup"><span data-stu-id="a9f92-132">Associate position, texture, and color coordinates by presenting each as a separate **gluNurbsCurve** inside the begin/end pair.</span></span> <span data-ttu-id="a9f92-133">Você pode não fazer mais do que uma chamada para **gluNurbsCurve** para cada parte dos dados de cor, posição e textura em um único par **gluBeginCurve/gluEndCurve** .</span><span class="sxs-lookup"><span data-stu-id="a9f92-133">You can make no more than one call to **gluNurbsCurve** for each piece of color, position, and texture data within a single **gluBeginCurve/gluEndCurve** pair.</span></span> <span data-ttu-id="a9f92-134">Você deve fazer exatamente uma chamada para descrever a posição da curva (uma descrição GL \_ MAP1 \_ Vertex \_ 3 ou GL \_ MAP1 \_ Vertex \_ 4).</span><span class="sxs-lookup"><span data-stu-id="a9f92-134">You must make exactly one call to describe the position of the curve (a GL\_MAP1\_VERTEX\_3 or GL\_MAP1\_VERTEX\_4 description).</span></span> <span data-ttu-id="a9f92-135">Quando você chama **gluEndCurve**, a curva é mosaico em segmentos de linha e, em seguida, renderizada.</span><span class="sxs-lookup"><span data-stu-id="a9f92-135">When you call **gluEndCurve**, the curve is tessellated into line segments and then rendered.</span></span>

<span data-ttu-id="a9f92-136">A tabela a seguir lista os tipos de curva íris GL e OpenGL NURBS.</span><span class="sxs-lookup"><span data-stu-id="a9f92-136">The following table lists IRIS GL and OpenGL NURBS curve types.</span></span>



| <span data-ttu-id="a9f92-137">Tipo de GL de íris</span><span class="sxs-lookup"><span data-stu-id="a9f92-137">IRIS GL type</span></span> | <span data-ttu-id="a9f92-138">Tipo OpenGL</span><span class="sxs-lookup"><span data-stu-id="a9f92-138">OpenGL type</span></span>                  | <span data-ttu-id="a9f92-139">Significado</span><span class="sxs-lookup"><span data-stu-id="a9f92-139">Meaning</span></span>                                 |
|--------------|------------------------------|-----------------------------------------|
| <span data-ttu-id="a9f92-140">N \_ V3D</span><span class="sxs-lookup"><span data-stu-id="a9f92-140">N\_V3D</span></span>       | <span data-ttu-id="a9f92-141">GL \_ MAP1 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="a9f92-141">GL\_MAP1\_VERTEX\_3</span></span>          | <span data-ttu-id="a9f92-142">Curva polinomial.</span><span class="sxs-lookup"><span data-stu-id="a9f92-142">Polynomial curve.</span></span>                       |
| <span data-ttu-id="a9f92-143">N \_ V3DR</span><span class="sxs-lookup"><span data-stu-id="a9f92-143">N\_V3DR</span></span>      | <span data-ttu-id="a9f92-144">MAP1 do GL de \_ \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="a9f92-144">GL\_MAP1\_VERTEX\_4</span></span>          | <span data-ttu-id="a9f92-145">Curva racional.</span><span class="sxs-lookup"><span data-stu-id="a9f92-145">Rational curve.</span></span>                         |
|              | <span data-ttu-id="a9f92-146">GL \_ MAP1 \_ Texture \_ coord\_\*</span><span class="sxs-lookup"><span data-stu-id="a9f92-146">GL\_MAP1\_TEXTURE\_COORD\_\*</span></span> | <span data-ttu-id="a9f92-147">Pontos de controle são coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="a9f92-147">Control points are texture coordinates.</span></span> |
|              | <span data-ttu-id="a9f92-148">GL \_ MAP1 \_ normal</span><span class="sxs-lookup"><span data-stu-id="a9f92-148">GL\_MAP1\_NORMAL</span></span>             | <span data-ttu-id="a9f92-149">Os pontos de controle são normais.</span><span class="sxs-lookup"><span data-stu-id="a9f92-149">Control points are normals.</span></span>             |



 

<span data-ttu-id="a9f92-150">Para obter mais informações sobre os tipos de avaliadores disponíveis, consulte [**glMap1**](glmap1.md).</span><span class="sxs-lookup"><span data-stu-id="a9f92-150">For more information on available evaluator types, see [**glMap1**](glmap1.md).</span></span>

<span data-ttu-id="a9f92-151">??</span><span class="sxs-lookup"><span data-stu-id="a9f92-151">??</span></span>

 

 




