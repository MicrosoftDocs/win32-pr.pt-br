---
title: C (OpenGL)
description: Definições de termos OpenGL que começam com a letra C.
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 037c39b1-b728-41d3-a664-c0aa6c487103
keywords:
- computadores cliente
- memória do cliente
- coordenadas do clipe
- recorte
- índice de cores
- modo de índice de cor
- mapas de cores
- components
- contextos
- convexa
- forma convexa
- sistema de coordenadas
- escolhidos
- matriz atual
- posição de rasterização atual
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 73c9534052533745b1037aa80f26f435a163ee46
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 12/10/2020
ms.locfileid: "104008760"
---
# <a name="c-opengl"></a><span data-ttu-id="a8c78-118">C (OpenGL)</span><span class="sxs-lookup"><span data-stu-id="a8c78-118">C (OpenGL)</span></span>

<span data-ttu-id="a8c78-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [i](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span><span class="sxs-lookup"><span data-stu-id="a8c78-119">[A](a.md) [B](b.md) C [D](d.md) [E](e.md) [F](f.md) [G](g.md) [H](h.md) [I](i.md) [J K](jk.md) [L](l.md) [M](m.md) [N](n.md) [O](o.md) [P](p.md) [Q](q.md) [R](r.md) [S](s.md) [T](t.md) [U V](u-v.md) [W](w.md) [X Y Z](x-y-z.md)</span></span>

<dl> <dt>

<span data-ttu-id="a8c78-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**computador cliente**</span><span class="sxs-lookup"><span data-stu-id="a8c78-120"><span id="opengl_client_computer"></span><span id="OPENGL_CLIENT_COMPUTER"></span>**client computer**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-121">O computador do qual os comandos OpenGL são emitidos.</span><span class="sxs-lookup"><span data-stu-id="a8c78-121">The computer from which OpenGL commands are issued.</span></span> <span data-ttu-id="a8c78-122">O computador que emite comandos OpenGL pode ser conectado por meio de uma rede a um computador diferente que executa os comandos, ou os comandos podem ser emitidos e executados no mesmo computador.</span><span class="sxs-lookup"><span data-stu-id="a8c78-122">The computer that issues OpenGL commands can be connected through a network to a different computer that executes the commands, or commands can be issued and executed on the same computer.</span></span> <span data-ttu-id="a8c78-123">Consulte também [servidor](s.md).</span><span class="sxs-lookup"><span data-stu-id="a8c78-123">See also [server](s.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**memória do cliente**</span><span class="sxs-lookup"><span data-stu-id="a8c78-124"><span id="opengl_client_memory"></span><span id="OPENGL_CLIENT_MEMORY"></span>**client memory**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-125">A memória principal (onde as variáveis do programa são armazenadas) do computador cliente.</span><span class="sxs-lookup"><span data-stu-id="a8c78-125">The main memory (where program variables are stored) of the client computer.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**coordenadas do clipe**</span><span class="sxs-lookup"><span data-stu-id="a8c78-126"><span id="opengl_clip_coordinates"></span><span id="OPENGL_CLIP_COORDINATES"></span>**clip coordinates**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-127">O sistema de coordenadas que segue a transformação pela matriz de projeção e precede a divisão em perspectiva.</span><span class="sxs-lookup"><span data-stu-id="a8c78-127">The coordinate system that follows transformation by the projection matrix and precedes perspective division.</span></span> <span data-ttu-id="a8c78-128">Exibição-o recorte de volume é feito em coordenadas de clipe, mas o recorte específico do aplicativo não é.</span><span class="sxs-lookup"><span data-stu-id="a8c78-128">View-volume clipping is done in clip coordinates, but application-specific clipping is not.</span></span> <span data-ttu-id="a8c78-129">Consulte também [recorte específico do aplicativo](a.md).</span><span class="sxs-lookup"><span data-stu-id="a8c78-129">See also [application-specific clipping](a.md).</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**recorte**</span><span class="sxs-lookup"><span data-stu-id="a8c78-130"><span id="opengl_clipping"></span><span id="OPENGL_CLIPPING"></span>**clipping**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-131">Eliminar a parte de um primitivo Geométrico que está fora do meio de espaço definido por um plano de recorte.</span><span class="sxs-lookup"><span data-stu-id="a8c78-131">Eliminating the portion of a geometric primitive that is outside the half-space defined by a clipping plane.</span></span> <span data-ttu-id="a8c78-132">Os pontos são simplesmente rejeitados se estiverem fora do.</span><span class="sxs-lookup"><span data-stu-id="a8c78-132">Points are simply rejected if outside.</span></span> <span data-ttu-id="a8c78-133">A parte de uma linha ou de um polígono que está fora do espaço é eliminada e os vértices adicionais são gerados conforme a necessidade para concluir o primitivo dentro do espaço de recorte.</span><span class="sxs-lookup"><span data-stu-id="a8c78-133">The portion of a line or of a polygon that is outside the half-space is eliminated, and additional vertices are generated as necessary to complete the primitive within the clipping half-space.</span></span> <span data-ttu-id="a8c78-134">Primitivos geométricos e a posição atual de rasterização (quando especificado) são sempre recortados em relação aos seis espaços de meia definição pelos planos esquerdo, direito, inferior, superior, próximo e distante do volume de exibição.</span><span class="sxs-lookup"><span data-stu-id="a8c78-134">Geometric primitives and the current raster position (when specified) are always clipped against the six half-spaces defined by the left, right, bottom, top, near, and far planes of the view volume.</span></span> <span data-ttu-id="a8c78-135">Os aplicativos podem especificar planos opcionais de recorte específicos do aplicativo a serem aplicados em coordenadas de olho.</span><span class="sxs-lookup"><span data-stu-id="a8c78-135">Applications can specify optional application-specific clipping planes to be applied in eye coordinates.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**índice de cores**</span><span class="sxs-lookup"><span data-stu-id="a8c78-136"><span id="opengl_color_index"></span><span id="OPENGL_COLOR_INDEX"></span>**color index**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-137">Um único valor que representa uma cor por nome, em vez de por valor.</span><span class="sxs-lookup"><span data-stu-id="a8c78-137">A single value that represents a color by name, rather than by value.</span></span> <span data-ttu-id="a8c78-138">Os índices de cores OpenGL são tratados como valores contínuos (por exemplo, números de ponto flutuante) enquanto operações como interpolação e pontilhamento são executadas neles.</span><span class="sxs-lookup"><span data-stu-id="a8c78-138">OpenGL color indexes are treated as continuous values (for example, floating-point numbers) while operations such as interpolation and dithering are performed on them.</span></span> <span data-ttu-id="a8c78-139">No entanto, os índices de cores armazenados no buffer de quadros são sempre valores inteiros.</span><span class="sxs-lookup"><span data-stu-id="a8c78-139">Color indexes stored in the frame buffer are always integer values, however.</span></span> <span data-ttu-id="a8c78-140">Os índices de ponto flutuante são convertidos em inteiros arredondando para o valor inteiro mais próximo.</span><span class="sxs-lookup"><span data-stu-id="a8c78-140">Floating-point indexes are converted to integers by rounding to the nearest integer value.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**modo de índice de cor**</span><span class="sxs-lookup"><span data-stu-id="a8c78-141"><span id="opengl_color_index_mode"></span><span id="OPENGL_COLOR_INDEX_MODE"></span>**color-index mode**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-142">Modo de um contexto OpenGL no qual seus buffers de cor armazenam índices de cores, em vez de componentes de cores vermelho, verde, azul e alfa.</span><span class="sxs-lookup"><span data-stu-id="a8c78-142">Mode of an OpenGL context in which its color buffers store color indexes, rather than red, green, blue, and alpha color components.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**mapa de cores**</span><span class="sxs-lookup"><span data-stu-id="a8c78-143"><span id="opengl_color_map"></span><span id="OPENGL_COLOR_MAP"></span>**color map**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-144">Uma tabela de mapeamentos de índice para RGB que é acessada pelo hardware de vídeo.</span><span class="sxs-lookup"><span data-stu-id="a8c78-144">A table of index-to-RGB mappings that is accessed by the display hardware.</span></span> <span data-ttu-id="a8c78-145">Cada índice de cor é lido do buffer de cores, convertido em um triplo RGB por pesquisa no mapa de cores e enviado ao monitor.</span><span class="sxs-lookup"><span data-stu-id="a8c78-145">Each color index is read from the color buffer, converted to an RGB triple by lookup in the color map, and sent to the monitor.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**componente**</span><span class="sxs-lookup"><span data-stu-id="a8c78-146"><span id="opengl_component"></span><span id="OPENGL_COMPONENT"></span>**component**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-147">Um valor único, contínuo (por exemplo, ponto flutuante) que representa uma intensidade ou quantidade.</span><span class="sxs-lookup"><span data-stu-id="a8c78-147">A single, continuous (for example, floating-point) value that represents an intensity or quantity.</span></span> <span data-ttu-id="a8c78-148">Normalmente, um valor de componente igual a zero representa o valor mínimo ou intensidade, e um valor de componente de um representa o valor máximo ou intensidade, embora outras normalizações sejam usadas às vezes.</span><span class="sxs-lookup"><span data-stu-id="a8c78-148">Usually, a component value of zero represents the minimum value or intensity, and a component value of one represents the maximum value or intensity, though other normalizations are sometimes used.</span></span> <span data-ttu-id="a8c78-149">Como os valores de componente são interpretados em um intervalo normalizado, eles são especificados independentemente da resolução real.</span><span class="sxs-lookup"><span data-stu-id="a8c78-149">Because component values are interpreted in a normalized range, they are specified independently of actual resolution.</span></span> <span data-ttu-id="a8c78-150">Por exemplo, o RGB triplo (1, 1, 1) é branco, independentemente se os buffers de cor armazenam 4, 8 ou 12 bits cada.</span><span class="sxs-lookup"><span data-stu-id="a8c78-150">For example, the RGB triple (1, 1, 1) is white, regardless of whether the color buffers store 4, 8, or 12 bits each.</span></span> <span data-ttu-id="a8c78-151">Os componentes fora do intervalo normalmente são clampeds ao intervalo normalizado, não truncado ou interpretado de outra forma.</span><span class="sxs-lookup"><span data-stu-id="a8c78-151">Out-of-range components are typically clamped to the normalized range, not truncated or otherwise interpreted.</span></span> <span data-ttu-id="a8c78-152">Por exemplo, o triplo RGB (1,4, 1,5, 0,9) é clamped para (1,0, 1,0, 0,9) antes de ser usado para atualizar o buffer de cores.</span><span class="sxs-lookup"><span data-stu-id="a8c78-152">For example, the RGB triple (1.4, 1.5, 0.9) is clamped to (1.0, 1.0, 0.9) before it's used to update the color buffer.</span></span> <span data-ttu-id="a8c78-153">Vermelho, verde, azul, alfa e profundidade são sempre tratados como componentes, nunca como índices.</span><span class="sxs-lookup"><span data-stu-id="a8c78-153">Red, green, blue, alpha, and depth are always treated as components, never as indexes.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**noticioso**</span><span class="sxs-lookup"><span data-stu-id="a8c78-154"><span id="opengl_context"></span><span id="OPENGL_CONTEXT"></span>**context**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-155">Um conjunto completo de variáveis de estado OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a8c78-155">A complete set of OpenGL state variables.</span></span> <span data-ttu-id="a8c78-156">Observe que o conteúdo do framebuffer não faz parte do estado do OpenGL, mas que a configuração do framebuffer é.</span><span class="sxs-lookup"><span data-stu-id="a8c78-156">Note that framebuffer contents are not part of the OpenGL state, but that the configuration of the framebuffer is.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**convexa**</span><span class="sxs-lookup"><span data-stu-id="a8c78-157"><span id="opengl_convex"></span><span id="OPENGL_CONVEX"></span>**convex**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-158">Condição de um polígono no qual nenhuma linha reta no plano do polígono intersecciona o polígono mais de duas vezes.</span><span class="sxs-lookup"><span data-stu-id="a8c78-158">Condition of a polygon in which no straight line in the plane of the polygon intersects the polygon more than twice.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convexa envoltória**</span><span class="sxs-lookup"><span data-stu-id="a8c78-159"><span id="opengl_convex_hull"></span><span id="OPENGL_CONVEX_HULL"></span>**convex hull**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-160">A menor região convexa que envolve um grupo de pontos especificado.</span><span class="sxs-lookup"><span data-stu-id="a8c78-160">The smallest convex region enclosing a specified group of points.</span></span> <span data-ttu-id="a8c78-161">Em duas dimensões, o convexa envoltória é encontrado conceitualmente ao esticar uma faixa de borracha ao lado dos pontos para que todos os pontos estejam dentro da banda.</span><span class="sxs-lookup"><span data-stu-id="a8c78-161">In two dimensions, the convex hull is found conceptually by stretching a rubber band around the points so that all of the points lie within the band.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**sistema de coordenadas**</span><span class="sxs-lookup"><span data-stu-id="a8c78-162"><span id="opengl_coordinate_system"></span><span id="OPENGL_COORDINATE_SYSTEM"></span>**coordinate system**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-163">No espaço n-dimensional, um conjunto de n vetores independentes linearmente ancorados a um ponto (denominado a origem).</span><span class="sxs-lookup"><span data-stu-id="a8c78-163">In n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="a8c78-164">Um grupo de coordenadas especifica um ponto no espaço n-dimensional, um conjunto de n vetores independentes lineares ancorados a um ponto (chamado de origem).</span><span class="sxs-lookup"><span data-stu-id="a8c78-164">A group of coordinates specifies a point in spaceIn n-dimensional space, a set of n linearly independent vectors anchored to a point (called the origin).</span></span> <span data-ttu-id="a8c78-165">Um grupo de coordenadas especifica um ponto no espaço (ou um vetor da origem) indicando a distância em cada vetor para alcançar o ponto (ou a ponta do vetor).</span><span class="sxs-lookup"><span data-stu-id="a8c78-165">A group of coordinates specifies a point in space (or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span> <span data-ttu-id="a8c78-166">(ou um vetor da origem), indicando a distância de viagem em cada vetor para alcançar o ponto (ou a ponta do vetor).</span><span class="sxs-lookup"><span data-stu-id="a8c78-166">(or a vector from the origin) by indicating how far to travel along each vector to reach the point (or tip of the vector).</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**escolhidos**</span><span class="sxs-lookup"><span data-stu-id="a8c78-167"><span id="opengl_culling"></span><span id="OPENGL_CULLING"></span>**culling**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-168">O processo de eliminar uma face frontal ou um verso de um polígono para que a face não seja desenhada.</span><span class="sxs-lookup"><span data-stu-id="a8c78-168">The process of eliminating a front face or back face of a polygon so that the face isn't drawn.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**matriz atual**</span><span class="sxs-lookup"><span data-stu-id="a8c78-169"><span id="opengl_current_matrix"></span><span id="OPENGL_CURRENT_MATRIX"></span>**current matrix**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-170">Uma matriz que transforma coordenadas em um sistema de coordenadas para coordenadas de outro sistema.</span><span class="sxs-lookup"><span data-stu-id="a8c78-170">A matrix that transforms coordinates in one coordinate system to coordinates of another system.</span></span> <span data-ttu-id="a8c78-171">Há três matrizes atuais no OpenGL: a matriz modelview, que transforma coordenadas de objetos (coordenadas especificadas pelo programador) em coordenadas de olho; a matriz de perspectiva, que transforma as coordenadas de olho em coordenadas do clipe; e a matriz de textura, que transforma as coordenadas de textura especificadas ou geradas conforme descrito pela matriz.</span><span class="sxs-lookup"><span data-stu-id="a8c78-171">There are three current matrices in OpenGL: the modelview matrix, which transforms object coordinates (coordinates specified by the programmer) to eye coordinates; the perspective matrix, which transforms eye coordinates to clip coordinates; and the texture matrix, which transforms specified or generated texture coordinates as described by the matrix.</span></span> <span data-ttu-id="a8c78-172">Cada matriz atual é o elemento superior em uma pilha de matrizes.</span><span class="sxs-lookup"><span data-stu-id="a8c78-172">Each current matrix is the top element on a stack of matrices.</span></span> <span data-ttu-id="a8c78-173">Cada uma das três pilhas pode ser manipulada com comandos de manipulação de matriz OpenGL.</span><span class="sxs-lookup"><span data-stu-id="a8c78-173">Each of the three stacks can be manipulated with OpenGL matrix-manipulation commands.</span></span>

</dd> <dt>

<span data-ttu-id="a8c78-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**posição de rasterização atual**</span><span class="sxs-lookup"><span data-stu-id="a8c78-174"><span id="opengl_current_raster_position"></span><span id="OPENGL_CURRENT_RASTER_POSITION"></span>**current raster position**</span></span>
</dt> <dd>

<span data-ttu-id="a8c78-175">Uma posição de coordenada de janela que especifica o posicionamento de uma imagem primitiva quando ela é rasterizada.</span><span class="sxs-lookup"><span data-stu-id="a8c78-175">A window coordinate position that specifies the placement of an image primitive when it's rasterized.</span></span> <span data-ttu-id="a8c78-176">A posição de rasterização atual e outros parâmetros de rasterização atuais são atualizados quando glRasterpos é chamado.</span><span class="sxs-lookup"><span data-stu-id="a8c78-176">The current raster position, and other current raster parameters, are updated when glRasterpos is called.</span></span>

</dd> </dl>

 

 




