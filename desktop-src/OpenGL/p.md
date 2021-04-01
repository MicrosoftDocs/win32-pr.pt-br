---
title: P (OpenGL)
description: Definições de termos OpenGL que começam com a letra P.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: bc7b0c93-af06-44a4-8bb8-adc0c6fedb6e
keywords:
- parameters
- divisão em perspectiva
- pixels
- pontos
- polígonos
- primitivos
- matrizes de projeção
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9970b3eb84920184e693ace93b14120828573e30
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "103917906"
---
# <a name="p-opengl"></a><span data-ttu-id="4826c-110">P (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="4826c-110">P (OpenGL)</span></span>

<span data-ttu-id="4826c-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="4826c-111">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) P [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="4826c-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**meter**</span><span class="sxs-lookup"><span data-stu-id="4826c-112"><span id="opengl_parameter"></span><span id="OPENGL_PARAMETER"></span>**parameter**</span></span>
</dt> <dd>

<span data-ttu-id="4826c-113">Um valor passado como um argumento para um comando OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4826c-113">A value passed as an argument to an OpenGL command.</span></span> <span data-ttu-id="4826c-114">Às vezes, um dos valores passados por referência a um comando OpenGL.</span><span class="sxs-lookup"><span data-stu-id="4826c-114">Sometimes one of the values passed by reference to an OpenGL command.</span></span>

</dd> <dt>

<span data-ttu-id="4826c-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**divisão em perspectiva**</span><span class="sxs-lookup"><span data-stu-id="4826c-115"><span id="opengl_perspective_division"></span><span id="OPENGL_PERSPECTIVE_DIVISION"></span>**perspective division**</span></span>
</dt> <dd>

<span data-ttu-id="4826c-116">A divisão de x, y e z por w, realizada em coordenadas de clipes.</span><span class="sxs-lookup"><span data-stu-id="4826c-116">The division of x, y, and z by w, carried out in clip coordinates.</span></span> <span data-ttu-id="4826c-117">Consulte também as [coordenadas do clipe](c.md).</span><span class="sxs-lookup"><span data-stu-id="4826c-117">See also [clip coordinates](c.md).</span></span>

</dd> <dt>

<span data-ttu-id="4826c-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**16x16**</span><span class="sxs-lookup"><span data-stu-id="4826c-118"><span id="opengl_pixel"></span><span id="OPENGL_PIXEL"></span>**pixel**</span></span>
</dt> <dd>

<span data-ttu-id="4826c-119">Elemento de imagem.</span><span class="sxs-lookup"><span data-stu-id="4826c-119">Picture element.</span></span> <span data-ttu-id="4826c-120">Os bits no local (x, y) de todos os bitplanes no framebuffer constituem o único pixel (x, y).</span><span class="sxs-lookup"><span data-stu-id="4826c-120">The bits at location (x, y) of all the bitplanes in the framebuffer constitute the single pixel (x, y).</span></span> <span data-ttu-id="4826c-121">Em uma imagem na memória do cliente, um pixel é um grupo de elementos.</span><span class="sxs-lookup"><span data-stu-id="4826c-121">In an image in client memory, a pixel is one group of elements.</span></span> <span data-ttu-id="4826c-122">Nas coordenadas da janela OpenGL, cada pixel corresponde a uma área da tela 1.0 x 1.0.</span><span class="sxs-lookup"><span data-stu-id="4826c-122">In OpenGL window coordinates, each pixel corresponds to a 1.0x1.0 screen area.</span></span> <span data-ttu-id="4826c-123">As coordenadas do canto inferior esquerdo dos nomes de pixel x, y são (x, y) e o canto superior direito são (x + 1, y + 1).</span><span class="sxs-lookup"><span data-stu-id="4826c-123">The coordinates of the lower-left corner of the pixel names x, y are (x, y), and the upper-right corner are (x+1, y+1).</span></span>

</dd> <dt>

<span data-ttu-id="4826c-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**empresas**</span><span class="sxs-lookup"><span data-stu-id="4826c-124"><span id="opengl_point"></span><span id="OPENGL_POINT"></span>**point**</span></span>
</dt> <dd>

<span data-ttu-id="4826c-125">Um local exato no espaço, que é renderizado como um ponto de diâmetro finito.</span><span class="sxs-lookup"><span data-stu-id="4826c-125">An exact location in space, which is rendered as a finite-diameter dot.</span></span>

</dd> <dt>

<span data-ttu-id="4826c-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**Polygon**</span><span class="sxs-lookup"><span data-stu-id="4826c-126"><span id="opengl_polygon"></span><span id="OPENGL_POLYGON"></span>**polygon**</span></span>
</dt> <dd>

<span data-ttu-id="4826c-127">Uma superfície quase planar limitada por bordas especificadas por vértices.</span><span class="sxs-lookup"><span data-stu-id="4826c-127">A near-planar surface bounded by edges specified by vertices.</span></span> <span data-ttu-id="4826c-128">Cada triângulo de uma malha de triângulos é um polígono, assim como cada diamante de uma malha diamante.</span><span class="sxs-lookup"><span data-stu-id="4826c-128">Each triangle of a triangle mesh is a polygon, as is each quadrilateral of a quadrilateral mesh.</span></span> <span data-ttu-id="4826c-129">O retângulo especificado por glRect também é um polígono.</span><span class="sxs-lookup"><span data-stu-id="4826c-129">The rectangle specified by glRect is also a polygon.</span></span>

</dd> <dt>

<span data-ttu-id="4826c-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitiva**</span><span class="sxs-lookup"><span data-stu-id="4826c-130"><span id="opengl_primitive"></span><span id="OPENGL_PRIMITIVE"></span>**primitive**</span></span>
</dt> <dd>

<span data-ttu-id="4826c-131">Uma forma (como um ponto, linha, polígono, bitmap ou imagem) que pode ser desenhada, armazenada e manipulada como uma entidade discreta; elementos dos quais são criados grandes designs gráficos.</span><span class="sxs-lookup"><span data-stu-id="4826c-131">A shape (such as a point, line, polygon, bitmap, or image) that can be drawn, stored, and manipulated as a discrete entity; elements from which large graphic designs are created.</span></span>

</dd> <dt>

<span data-ttu-id="4826c-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**matriz de projeção**</span><span class="sxs-lookup"><span data-stu-id="4826c-132"><span id="opengl_projection_matrix"></span><span id="OPENGL_PROJECTION_MATRIX"></span>**projection matrix**</span></span>
</dt> <dd>

<span data-ttu-id="4826c-133">A matriz 4x4 que transforma pontos, linhas, polígonos e posições de varredura de coordenadas de olho em coordenadas de clipes.</span><span class="sxs-lookup"><span data-stu-id="4826c-133">The 4x4 matrix that transforms points, lines, polygons, and raster positions from eye coordinates to clip coordinates.</span></span>

</dd> </dl>

 

 




