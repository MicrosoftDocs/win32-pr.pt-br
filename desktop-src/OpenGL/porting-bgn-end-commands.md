---
title: Portando comandos BGN/end
description: A íris GL usa o paradigma de início/término, mas tem uma função diferente para cada primitivo de elementos gráficos.
ms.assetid: 4191344b-614a-42d6-8a31-7a708f17371e
keywords:
- Portabilidade do íris GL, comandos BGN/end
- portando dos comandos íris GL, BGN/end
- portando para OpenGL dos comandos íris GL, BGN/end
- Portabilidade do OpenGL dos comandos íris GL, BGN/end
- funções de desenho, comandos BGN/end
- comandos BGN/end
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c25118d4e5050ea22d4b18fab596dfb9c92f562e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364322"
---
# <a name="porting-bgnend-commands"></a><span data-ttu-id="bbdd9-109">Portando comandos BGN/end</span><span class="sxs-lookup"><span data-stu-id="bbdd9-109">Porting bgn/end Commands</span></span>

<span data-ttu-id="bbdd9-110">A íris GL usa o paradigma de início/término, mas tem uma função diferente para cada primitivo de elementos gráficos.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-110">IRIS GL uses the begin/end paradigm but has a different function for each graphics primitive.</span></span> <span data-ttu-id="bbdd9-111">Por exemplo, você provavelmente usará **bgnpolygon** e **endpolygon** para desenhar polígonos e **bgnline** e **EndLine** para desenhar linhas.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-111">For example, you probably use **bgnpolygon** and **endpolygon** to draw polygons, and **bgnline** and **endline** to draw lines.</span></span> <span data-ttu-id="bbdd9-112">No OpenGL, você usa a estrutura [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) para ambos.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-112">In OpenGL, you use the [**glBegin**](glbegin.md) / [**glEnd**](glend.md) structure for both.</span></span> <span data-ttu-id="bbdd9-113">No OpenGL, você desenha a maioria dos objetos geométricos delimitando uma série de funções que especificam vértices, normais, texturas e cores entre pares de chamadas **glBegin** e **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="bbdd9-113">In OpenGL you draw most geometric objects by enclosing a series of functions that specify vertices, normals, textures, and colors between pairs of **glBegin** and **glEnd** calls.</span></span> <span data-ttu-id="bbdd9-114">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="bbdd9-114">For example:</span></span>

``` syntax
void glBegin( GLenum mode) ; 
   /* vertex list, colors, normals, textures, materials */ 
void glEnd( void );
```

<span data-ttu-id="bbdd9-115">A função **glBegin** usa um único parâmetro que especifica o modo de desenho e, portanto, o primitivo.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-115">The **glBegin** function takes a single parameter that specifies the drawing mode, and thus the primitive.</span></span> <span data-ttu-id="bbdd9-116">Aqui está um exemplo de código OpenGL que desenha um polígono e uma linha:</span><span class="sxs-lookup"><span data-stu-id="bbdd9-116">Here's an OpenGL code sample that draws a polygon and then a line:</span></span>

``` syntax
glBegin( GL_POLYGON ) ; 
   glVertex2f(20.0, 10.0); 
   glVertex2f(10.0, 30.0); 
   glVertex2f(20.0, 50.0); 
   glVertex2f(40.0, 50.0); 
   glVertex2f(50.0, 30.0); 
   glVertex2f(40.0, 10.0); 
glEnd(); 
glBegin( GL_LINES ) ; 
   glVertex2i(100,100); 
   glVertex2i(500,500); 
glEnd();
```

<span data-ttu-id="bbdd9-117">Com o OpenGL, você desenha diferentes objetos geométricos especificando parâmetros diferentes para [**glBegin**](glbegin.md).</span><span class="sxs-lookup"><span data-stu-id="bbdd9-117">With OpenGL, you draw different geometric objects by specifying different parameters for [**glBegin**](glbegin.md).</span></span> <span data-ttu-id="bbdd9-118">A tabela a seguir lista os parâmetros OpenGL **glBegin** que correspondem às funções do íris GL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-118">The following table lists the OpenGL **glBegin** parameters that correspond to equivalent IRIS GL functions.</span></span>



| <span data-ttu-id="bbdd9-119">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="bbdd9-119">IRIS GL function</span></span>  | <span data-ttu-id="bbdd9-120">Valor do modo glBegin</span><span class="sxs-lookup"><span data-stu-id="bbdd9-120">Value of glBegin mode</span></span> | <span data-ttu-id="bbdd9-121">Significado</span><span class="sxs-lookup"><span data-stu-id="bbdd9-121">Meaning</span></span>                                                                                  |
|-------------------|-----------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="bbdd9-122">**bgnpoint**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-122">**bgnpoint**</span></span>      | <span data-ttu-id="bbdd9-123">\_pontos GL</span><span class="sxs-lookup"><span data-stu-id="bbdd9-123">GL\_POINTS</span></span>            | <span data-ttu-id="bbdd9-124">Pontos individuais.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-124">Individual points.</span></span>                                                                       |
| <span data-ttu-id="bbdd9-125">**bgnline**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-125">**bgnline**</span></span>       | <span data-ttu-id="bbdd9-126">\_faixa de linha gl \_</span><span class="sxs-lookup"><span data-stu-id="bbdd9-126">GL\_LINE\_STRIP</span></span>       | <span data-ttu-id="bbdd9-127">Série de segmentos de linha conectados.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-127">Series of connected line segments.</span></span>                                                       |
| <span data-ttu-id="bbdd9-128">**bgnclosedline**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-128">**bgnclosedline**</span></span> | <span data-ttu-id="bbdd9-129">\_loop de linha gl \_</span><span class="sxs-lookup"><span data-stu-id="bbdd9-129">GL\_LINE\_LOOP</span></span>        | <span data-ttu-id="bbdd9-130">Série de segmentos de linha conectados, com um segmento adicionado entre o primeiro e o último vértice.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-130">Series of connected line segments, with a segment added between first and last vertices.</span></span> |
|                   | <span data-ttu-id="bbdd9-131">\_linhas GL</span><span class="sxs-lookup"><span data-stu-id="bbdd9-131">GL\_LINES</span></span>             | <span data-ttu-id="bbdd9-132">Pares de vértices interpretados como segmentos de linha individuais.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-132">Pairs of vertices interpreted as individual line segments.</span></span>                               |
| <span data-ttu-id="bbdd9-133">**bgnpolygon**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-133">**bgnpolygon**</span></span>    | <span data-ttu-id="bbdd9-134">polígono do GL \_</span><span class="sxs-lookup"><span data-stu-id="bbdd9-134">GL\_POLYGON</span></span>           | <span data-ttu-id="bbdd9-135">Limite de um polígono convexa simples.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-135">Boundary of a simple convex polygon.</span></span>                                                     |
|                   | <span data-ttu-id="bbdd9-136">\_TRIângulos GL</span><span class="sxs-lookup"><span data-stu-id="bbdd9-136">GL\_TRIANGLES</span></span>         | <span data-ttu-id="bbdd9-137">As corridas de vértices interpretadas como triângulos.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-137">Triples of vertices interpreted as triangles.</span></span>                                            |
| <span data-ttu-id="bbdd9-138">**bgntmesh**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-138">**bgntmesh**</span></span>      | <span data-ttu-id="bbdd9-139">\_faixa de triângulo GL \_</span><span class="sxs-lookup"><span data-stu-id="bbdd9-139">GL\_TRIANGLE\_STRIP</span></span>   | <span data-ttu-id="bbdd9-140">Faixas vinculadas de triângulos.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-140">Linked strips of triangles.</span></span>                                                              |
|                   | <span data-ttu-id="bbdd9-141">\_ \_ ventilador do triângulo GL</span><span class="sxs-lookup"><span data-stu-id="bbdd9-141">GL\_TRIANGLE\_FAN</span></span>     | <span data-ttu-id="bbdd9-142">Ventiladores vinculados de triângulos.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-142">Linked fans of triangles.</span></span>                                                                |
|                   | <span data-ttu-id="bbdd9-143">GL \_ quádruplos</span><span class="sxs-lookup"><span data-stu-id="bbdd9-143">GL\_QUADS</span></span>             | <span data-ttu-id="bbdd9-144">Quádruplos de vértices interpretados como quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-144">Quadruples of vertices interpreted as quadrilaterals.</span></span>                                    |
| <span data-ttu-id="bbdd9-145">**bgnqstrip**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-145">**bgnqstrip**</span></span>     | <span data-ttu-id="bbdd9-146">extensão do GL \_ Quad \_</span><span class="sxs-lookup"><span data-stu-id="bbdd9-146">GL\_QUAD\_STRIP</span></span>       | <span data-ttu-id="bbdd9-147">Faixas vinculadas de quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-147">Linked strips of quadrilaterals.</span></span>                                                         |



 

<span data-ttu-id="bbdd9-148">Para obter uma discussão detalhada das diferenças entre malhas de triângulo, faixas e ventiladores, confira [triângulos de portabilidade](porting-triangles.md).</span><span class="sxs-lookup"><span data-stu-id="bbdd9-148">For a detailed discussion of the differences between triangle meshes, strips, and fans, see [Porting Triangles](porting-triangles.md).</span></span>

<span data-ttu-id="bbdd9-149">Não há nenhum limite para o número de vértices que você pode especificar entre um par [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) .</span><span class="sxs-lookup"><span data-stu-id="bbdd9-149">There is no limit to the number of vertices you can specify between a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair.</span></span>

<span data-ttu-id="bbdd9-150">Além de especificar vértices dentro de um par **glBegin**  /  **glEnd** , você pode especificar uma atual coordenadas atuais, atuais e uma cor atual.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-150">In addition to specifying vertices inside a **glBegin** / **glEnd** pair, you can specify a current normal, current texture coordinates, and a current color.</span></span> <span data-ttu-id="bbdd9-151">A tabela a seguir lista os comandos válidos dentro de um par **glBegin**  /  **glEnd** .</span><span class="sxs-lookup"><span data-stu-id="bbdd9-151">The following table lists the commands valid inside a **glBegin** / **glEnd** pair.</span></span>



| <span data-ttu-id="bbdd9-152">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="bbdd9-152">IRIS GL function</span></span>        | <span data-ttu-id="bbdd9-153">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="bbdd9-153">OpenGL function</span></span>                                                      | <span data-ttu-id="bbdd9-154">Significado</span><span class="sxs-lookup"><span data-stu-id="bbdd9-154">Meaning</span></span>                                          |
|-------------------------|----------------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="bbdd9-155">**v2**, **v3**, **v4**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-155">**v2**, **v3**, **v4**</span></span>  | [<span data-ttu-id="bbdd9-156">glVertex</span><span class="sxs-lookup"><span data-stu-id="bbdd9-156">glVertex</span></span>](glvertex-functions.md)                                   | <span data-ttu-id="bbdd9-157">Define as coordenadas do vértice.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-157">Sets vertex coordinates.</span></span>                         |
| <span data-ttu-id="bbdd9-158">**RGBcolor**, **cpack**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-158">**RGBcolor**, **cpack**</span></span> | [<span data-ttu-id="bbdd9-159">glColor</span><span class="sxs-lookup"><span data-stu-id="bbdd9-159">glColor</span></span>](glcolor-functions.md)                                     | <span data-ttu-id="bbdd9-160">Define a cor atual.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-160">Sets current color.</span></span>                              |
| <span data-ttu-id="bbdd9-161">**color**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-161">**color**</span></span>               | [<span data-ttu-id="bbdd9-162">glIndex</span><span class="sxs-lookup"><span data-stu-id="bbdd9-162">glIndex</span></span>](glindex-functions.md)                                     | <span data-ttu-id="bbdd9-163">Define o índice de cores atual.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-163">Sets current color index.</span></span>                        |
| <span data-ttu-id="bbdd9-164">**n3f**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-164">**n3f**</span></span>                 | [<span data-ttu-id="bbdd9-165">glNormal</span><span class="sxs-lookup"><span data-stu-id="bbdd9-165">glNormal</span></span>](glnormal-functions.md)                                   | <span data-ttu-id="bbdd9-166">Define coordenadas de vetor normais.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-166">Sets normal vector coordinates.</span></span>                  |
|                         | [<span data-ttu-id="bbdd9-167">glEvalCoord</span><span class="sxs-lookup"><span data-stu-id="bbdd9-167">glEvalCoord</span></span>](glevalcoord-functions.md)                             | <span data-ttu-id="bbdd9-168">Avalia os mapas único e bidimensionais habilitados.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-168">Evaluates enabled one- and two-dimensional maps.</span></span> |
| <span data-ttu-id="bbdd9-169">**callobj**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-169">**callobj**</span></span>             | <span data-ttu-id="bbdd9-170">[**glCallList**](glcalllist.md), [ **glCallLists**](glcalllists.md)</span><span class="sxs-lookup"><span data-stu-id="bbdd9-170">[**glCallList**](glcalllist.md), [**glCallLists**](glcalllists.md)</span></span> | <span data-ttu-id="bbdd9-171">Executa lista (s) de exibição.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-171">Executes display list(s).</span></span>                        |
| <span data-ttu-id="bbdd9-172">**T2**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-172">**t2**</span></span>                  | [<span data-ttu-id="bbdd9-173">glTexCoord</span><span class="sxs-lookup"><span data-stu-id="bbdd9-173">glTexCoord</span></span>](gltexcoord-functions.md)                               | <span data-ttu-id="bbdd9-174">Define coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-174">Sets texture coordinates.</span></span>                        |
|                         | [<span data-ttu-id="bbdd9-175">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="bbdd9-175">glEdgeFlag</span></span>](gledgeflag-functions.md)                               | <span data-ttu-id="bbdd9-176">Controla bordas de desenho.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-176">Controls drawing edges.</span></span>                          |
| <span data-ttu-id="bbdd9-177">**lmbind**</span><span class="sxs-lookup"><span data-stu-id="bbdd9-177">**lmbind**</span></span>              | [<span data-ttu-id="bbdd9-178">glMaterial</span><span class="sxs-lookup"><span data-stu-id="bbdd9-178">glMaterial</span></span>](glmaterial-functions.md)                               | <span data-ttu-id="bbdd9-179">Define as propriedades do material.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-179">Sets material properties.</span></span>                        |



 

> [!Note]
>
> <span data-ttu-id="bbdd9-180">Se você usar qualquer função OpenGL diferente daquelas listadas na tabela anterior dentro de um par [**glBegin**](glbegin.md)  /  [**glEnd**](glend.md) , você obterá resultados imprevisíveis ou possivelmente um erro.</span><span class="sxs-lookup"><span data-stu-id="bbdd9-180">If you use any OpenGL function other than those listed in the preceding table inside a [**glBegin**](glbegin.md) / [**glEnd**](glend.md) pair, you'll get unpredictable results, or possibly an error.</span></span>

 

 

 




