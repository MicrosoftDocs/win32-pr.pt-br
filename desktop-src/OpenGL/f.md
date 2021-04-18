---
title: F (OpenGL)
description: Definições de termos OpenGL que começam com a letra F.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: ba960409-84e0-4ece-967b-97f0e1183956
keywords:
- faces
- sombreamento simples
- neblina
- fontes
- fragmentos
- framebuffers
- face frontal
- frustum
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7085765a5585268acb2f20a77c72bdd7cf1b4b81
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "105758585"
---
# <a name="f-opengl"></a><span data-ttu-id="65096-111">F (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="65096-111">F (OpenGL)</span></span>

<span data-ttu-id="65096-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="65096-112">[A](a.md) [B](b.md) [C](c.md) [D](d.md) [E](e.md) F [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="65096-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**sorridente**</span><span class="sxs-lookup"><span data-stu-id="65096-113"><span id="opengl_face"></span><span id="OPENGL_FACE"></span>**face**</span></span>
</dt> <dd>

<span data-ttu-id="65096-114">Um lado de um polígono.</span><span class="sxs-lookup"><span data-stu-id="65096-114">One side of a polygon.</span></span> <span data-ttu-id="65096-115">Cada polígono tem duas faces: uma face frontal e uma face de fundo.</span><span class="sxs-lookup"><span data-stu-id="65096-115">Each polygon has two faces: a front face and a back face.</span></span> <span data-ttu-id="65096-116">Apenas uma face está visível na janela.</span><span class="sxs-lookup"><span data-stu-id="65096-116">Only one face is ever visible in the window.</span></span> <span data-ttu-id="65096-117">Se a face traseira ou frontal está visível é efetivamente determinada depois que o polígono é projetado na janela.</span><span class="sxs-lookup"><span data-stu-id="65096-117">Whether the back or front face is visible is effectively determined after the polygon is projected onto the window.</span></span> <span data-ttu-id="65096-118">Após essa projeção, se as bordas do polígono forem direcionadas para o sentido horário, uma das faces será visível; Se for direcionado no sentido anti-horário, a outra face estará visível.</span><span class="sxs-lookup"><span data-stu-id="65096-118">After this projection, if the polygon's edges are directed clockwise, one of the faces is visible; if directed counterclockwise, the other face is visible.</span></span> <span data-ttu-id="65096-119">Se o sentido horário corresponde à frente ou ao verso (e o sentido anti-horário corresponde à parte traseira ou frontal) é determinado pelo programador OpenGL.</span><span class="sxs-lookup"><span data-stu-id="65096-119">Whether clockwise corresponds to front or back (and counterclockwise corresponds to back or front) is determined by the OpenGL programmer.</span></span>

</dd> <dt>

<span data-ttu-id="65096-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**sombreamento simples**</span><span class="sxs-lookup"><span data-stu-id="65096-120"><span id="opengl_flat_shading"></span><span id="OPENGL_FLAT_SHADING"></span>**flat shading**</span></span>
</dt> <dd>

<span data-ttu-id="65096-121">Refere-se à coloração de uma primitiva com uma única cor constante em sua extensão, em vez de interpolar cores suavemente em todo o primitivo.</span><span class="sxs-lookup"><span data-stu-id="65096-121">Refers to coloring a primitive with a single, constant color across its extent, rather than smoothly interpolating colors across the primitive.</span></span> <span data-ttu-id="65096-122">Consulte [sombreamento Gouraud](g.md).</span><span class="sxs-lookup"><span data-stu-id="65096-122">See [Gouraud shading](g.md).</span></span>

</dd> <dt>

<span data-ttu-id="65096-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**neblina**</span><span class="sxs-lookup"><span data-stu-id="65096-123"><span id="opengl_fog"></span><span id="OPENGL_FOG"></span>**fog**</span></span>
</dt> <dd>

<span data-ttu-id="65096-124">Uma técnica de renderização que pode ser usada para simular efeitos atmosféricas, como criações, neblina e smog, esmaecidas cores de objetos para uma cor de plano de fundo com base na distância do visualizador.</span><span class="sxs-lookup"><span data-stu-id="65096-124">A rendering technique that can be used to simulate atmospheric effects such as haze, fog, and smog by fading object colors to a background color based on distance from the viewer.</span></span> <span data-ttu-id="65096-125">A neblina também ajuda na percepção da distância do visualizador, dando uma indicação de profundidade.</span><span class="sxs-lookup"><span data-stu-id="65096-125">Fog also aids in the perception of distance from the viewer, giving a depth cue.</span></span> <span data-ttu-id="65096-126">Consulte também [Depth-advertência](d.md).</span><span class="sxs-lookup"><span data-stu-id="65096-126">See also [depth-cueing](d.md).</span></span>

</dd> <dt>

<span data-ttu-id="65096-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**la**</span><span class="sxs-lookup"><span data-stu-id="65096-127"><span id="opengl_font"></span><span id="OPENGL_FONT"></span>**font**</span></span>
</dt> <dd>

<span data-ttu-id="65096-128">Um grupo de representações de caractere gráfico geralmente usado para exibir cadeias de caracteres de texto.</span><span class="sxs-lookup"><span data-stu-id="65096-128">A group of graphical character representations usually used to display strings of text.</span></span> <span data-ttu-id="65096-129">Os caracteres podem ser letras romanos, símbolos matemáticos, ideograms asiático, egípcio hieroglyphs e assim por diante.</span><span class="sxs-lookup"><span data-stu-id="65096-129">The characters may be roman letters, mathematical symbols, Asian ideograms, Egyptian hieroglyphs, and so on.</span></span>

</dd> <dt>

<span data-ttu-id="65096-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**fragmento**</span><span class="sxs-lookup"><span data-stu-id="65096-130"><span id="opengl_fragment"></span><span id="OPENGL_FRAGMENT"></span>**fragment**</span></span>
</dt> <dd>

<span data-ttu-id="65096-131">Dados gráficos gerados pela rasterização de primitivos.</span><span class="sxs-lookup"><span data-stu-id="65096-131">Graphic data generated by the rasterization of primitives.</span></span> <span data-ttu-id="65096-132">Cada fragmento corresponde a um único pixel e inclui valores de coordenadas de cor, profundidade e, às vezes, de textura.</span><span class="sxs-lookup"><span data-stu-id="65096-132">Each fragment corresponds to a single pixel and includes color, depth, and sometimes texture-coordinate values.</span></span>

</dd> <dt>

<span data-ttu-id="65096-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**framebuffer**</span><span class="sxs-lookup"><span data-stu-id="65096-133"><span id="opengl_framebuffer"></span><span id="OPENGL_FRAMEBUFFER"></span>**framebuffer**</span></span>
</dt> <dd>

<span data-ttu-id="65096-134">Uma pilha de bitplanes.</span><span class="sxs-lookup"><span data-stu-id="65096-134">A stack of bitplanes.</span></span> <span data-ttu-id="65096-135">Todos os buffers de uma determinada janela ou contexto.</span><span class="sxs-lookup"><span data-stu-id="65096-135">All the buffers of a given window or context.</span></span> <span data-ttu-id="65096-136">Às vezes inclui toda a memória de pixel do acelerador de hardware de gráficos.</span><span class="sxs-lookup"><span data-stu-id="65096-136">Sometimes includes all the pixel memory of the graphics hardware accelerator.</span></span> <span data-ttu-id="65096-137">Consulte também [Bitplane](b.md).</span><span class="sxs-lookup"><span data-stu-id="65096-137">See also [bitplane](b.md).</span></span>

</dd> <dt>

<span data-ttu-id="65096-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**face frontal**</span><span class="sxs-lookup"><span data-stu-id="65096-138"><span id="opengl_front_face"></span><span id="OPENGL_FRONT_FACE"></span>**front face**</span></span>
</dt> <dd>

<span data-ttu-id="65096-139">Consulte face.</span><span class="sxs-lookup"><span data-stu-id="65096-139">See face.</span></span>

</dd> <dt>

<span data-ttu-id="65096-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span><span class="sxs-lookup"><span data-stu-id="65096-140"><span id="opengl_frustum"></span><span id="OPENGL_FRUSTUM"></span>**frustum**</span></span>
</dt> <dd>

<span data-ttu-id="65096-141">O volume de exibição distorcido por divisão em perspectiva.</span><span class="sxs-lookup"><span data-stu-id="65096-141">The view volume warped by perspective division.</span></span>

</dd> </dl>

 

 




