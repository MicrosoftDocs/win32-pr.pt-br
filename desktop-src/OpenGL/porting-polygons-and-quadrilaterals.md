---
title: Como portar polígonos e Quadrilaterals
description: Tenha os seguintes pontos em mente ao portar polígonos e quadrilaterals
ms.assetid: 2b752437-caf9-4336-a906-d06b2aa8bb04
keywords:
- Portabilidade do íris GL, quadrilaterals
- portando do íris GL, quadrilaterals
- portando para OpenGL do íris GL, quadrilaterals
- Portabilidade OpenGL do íris GL, quadrilaterals
- funções de desenho, quadrilaterals
- quadrilaterals
- Portabilidade do íris GL, polígonos
- portando do íris GL, polígonos
- portando para OpenGL do íris GL, polígonos
- Portabilidade OpenGL do íris GL, polígonos
- funções de desenho, polígonos
- polígonos, portando do íris GL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c95d654b101c5eeb86cfcc4ea342e8196b8749e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636569"
---
# <a name="porting-polygons-and-quadrilaterals"></a><span data-ttu-id="0b02a-115">Como portar polígonos e Quadrilaterals</span><span class="sxs-lookup"><span data-stu-id="0b02a-115">Porting Polygons and Quadrilaterals</span></span>

<span data-ttu-id="0b02a-116">Tenha os seguintes pontos em mente ao portar polígonos e quadrilaterals:</span><span class="sxs-lookup"><span data-stu-id="0b02a-116">Keep the following points in mind when porting polygons and quadrilaterals:</span></span>

-   <span data-ttu-id="0b02a-117">Não há equivalente direto para **côncavo**(**true**).</span><span class="sxs-lookup"><span data-stu-id="0b02a-117">There is no direct equivalent for **concave**(**TRUE**).</span></span> <span data-ttu-id="0b02a-118">Em vez disso, você pode usar as rotinas de mosaico na GLU, descritas em [polígonos do inclusão](tessellating-polygons.md).</span><span class="sxs-lookup"><span data-stu-id="0b02a-118">Instead you can use the tessellation routines in the GLU, described in [Tessellating Polygons](tessellating-polygons.md).</span></span>
-   <span data-ttu-id="0b02a-119">Os modos de polígono são definidos de forma diferente.</span><span class="sxs-lookup"><span data-stu-id="0b02a-119">Polygon modes are set differently.</span></span>
-   <span data-ttu-id="0b02a-120">Essas funções de desenho de polígono não têm equivalentes diretos em OpenGL: The **Polyline** Family of rotinas; a família de rotinas **polf** ; **PMV**, **Laos** e **PCLOS**; **rpmv** e **rpdr**; **splf**; e **spclos**.</span><span class="sxs-lookup"><span data-stu-id="0b02a-120">These polygon drawing functions have no direct equivalents in OpenGL: the **poly** family of routines; the **polf** family of routines; **pmv**, **pdr**, and **pclos**; **rpmv** and **rpdr**; **splf**; and **spclos**.</span></span>

<span data-ttu-id="0b02a-121">Se o código do íris GL usar essas funções, você terá que reescrever o código usando [**glBegin**](glbegin.md)(polígono do GL \_ ).</span><span class="sxs-lookup"><span data-stu-id="0b02a-121">If your IRIS GL code uses these functions, you'll have to rewrite the code using [**glBegin**](glbegin.md)( GL\_POLYGON ).</span></span>

<span data-ttu-id="0b02a-122">A tabela a seguir lista as funções de desenho de polígono do íris GL e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="0b02a-122">The following table lists the IRIS GL polygon drawing functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0b02a-123">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="0b02a-123">IRIS GL function</span></span>         | <span data-ttu-id="0b02a-124">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="0b02a-124">OpenGL function</span></span>                                                    | <span data-ttu-id="0b02a-125">Significado</span><span class="sxs-lookup"><span data-stu-id="0b02a-125">Meaning</span></span>                                                 |
|--------------------------|--------------------------------------------------------------------|---------------------------------------------------------|
| <span data-ttu-id="0b02a-126">**bgnpolygonendpolygon**</span><span class="sxs-lookup"><span data-stu-id="0b02a-126">**bgnpolygonendpolygon**</span></span> | <span data-ttu-id="0b02a-127">[**glBegin**](glbegin.md) (polígono do GL \_ )[**glEnd**](glend.md)</span><span class="sxs-lookup"><span data-stu-id="0b02a-127">[**glBegin**](glbegin.md) ( GL\_POLYGON )[**glEnd**](glend.md)</span></span>   | <span data-ttu-id="0b02a-128">Os vértices definem o limite de um polígono convexa simples.</span><span class="sxs-lookup"><span data-stu-id="0b02a-128">Vertices define boundary of a simple convex polygon.</span></span>    |
|                          | <span data-ttu-id="0b02a-129">**glBegin**(GL \_ quádruplos)**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0b02a-129">**glBegin**( GL\_QUADS )**glEnd**</span></span><br/>                       | <span data-ttu-id="0b02a-130">Interpreta os quádruplos de vértices como quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="0b02a-130">Interprets quadruples of vertices as quadrilaterals.</span></span>    |
| <span data-ttu-id="0b02a-131">**bgnqstripendqstrip**</span><span class="sxs-lookup"><span data-stu-id="0b02a-131">**bgnqstripendqstrip**</span></span>   | <span data-ttu-id="0b02a-132">[**glBegin**](glbegin.md) (GL \_ Quad \_ strip)**glEnd**</span><span class="sxs-lookup"><span data-stu-id="0b02a-132">[**glBegin**](glbegin.md) ( GL\_QUAD\_STRIP )**glEnd**</span></span><br/> | <span data-ttu-id="0b02a-133">Interpreta vértices como faixas vinculadas de quadrilaterals.</span><span class="sxs-lookup"><span data-stu-id="0b02a-133">Interprets vertices as linked strips of quadrilaterals.</span></span> |
|                          | [<span data-ttu-id="0b02a-134">glEdgeFlag</span><span class="sxs-lookup"><span data-stu-id="0b02a-134">glEdgeFlag</span></span>](gledgeflag-functions.md)                             |                                                         |
| <span data-ttu-id="0b02a-135">**polimodo**</span><span class="sxs-lookup"><span data-stu-id="0b02a-135">**polymode**</span></span>             | [<span data-ttu-id="0b02a-136">**glPolygonMode**</span><span class="sxs-lookup"><span data-stu-id="0b02a-136">**glPolygonMode**</span></span>](glpolygonmode.md)                             | <span data-ttu-id="0b02a-137">Define o modo de desenho do polígono.</span><span class="sxs-lookup"><span data-stu-id="0b02a-137">Sets polygon drawing mode.</span></span>                              |
| <span data-ttu-id="0b02a-138">**rectrectf**</span><span class="sxs-lookup"><span data-stu-id="0b02a-138">**rectrectf**</span></span><br/> | [<span data-ttu-id="0b02a-139">glRect</span><span class="sxs-lookup"><span data-stu-id="0b02a-139">glRect</span></span>](glrect-functions.md)                                     | <span data-ttu-id="0b02a-140">Desenha um retângulo.</span><span class="sxs-lookup"><span data-stu-id="0b02a-140">Draws a rectangle.</span></span>                                      |
| <span data-ttu-id="0b02a-141">**sboxsboxf**</span><span class="sxs-lookup"><span data-stu-id="0b02a-141">**sboxsboxf**</span></span><br/> |                                                                    | <span data-ttu-id="0b02a-142">Desenha um retângulo alinhado à tela.</span><span class="sxs-lookup"><span data-stu-id="0b02a-142">Draws a screen-aligned rectangle.</span></span>                       |



 

<span data-ttu-id="0b02a-143">??</span><span class="sxs-lookup"><span data-stu-id="0b02a-143">??</span></span>

## <a name="porting-polygon-modes"></a><span data-ttu-id="0b02a-144">Modos de polígono de portabilidade</span><span class="sxs-lookup"><span data-stu-id="0b02a-144">Porting Polygon Modes</span></span>

<span data-ttu-id="0b02a-145">A função OpenGL [**glPolygonMode**](glpolygonmode.md) permite especificar qual lado de um polígono (na parte posterior ou frontal) ao qual o modo se aplica.</span><span class="sxs-lookup"><span data-stu-id="0b02a-145">The OpenGL function [**glPolygonMode**](glpolygonmode.md) lets you specify which side of a polygon (the back or the front) the mode applies to.</span></span> <span data-ttu-id="0b02a-146">Sua sintaxe é:</span><span class="sxs-lookup"><span data-stu-id="0b02a-146">Its syntax is:</span></span>

``` syntax
void glPolygonMode( GLenum face, GLenum mode ); 
 
```

<span data-ttu-id="0b02a-147">onde a face é uma de:</span><span class="sxs-lookup"><span data-stu-id="0b02a-147">where face is one of:</span></span>



|                      |                                                            |
|----------------------|------------------------------------------------------------|
| <span data-ttu-id="0b02a-148">frente do GL \_</span><span class="sxs-lookup"><span data-stu-id="0b02a-148">GL\_FRONT</span></span>            | <span data-ttu-id="0b02a-149">modo que se aplica a polígonos front-face</span><span class="sxs-lookup"><span data-stu-id="0b02a-149">mode which applies to front-facing polygons</span></span>                |
| <span data-ttu-id="0b02a-150">GL \_ regressivo</span><span class="sxs-lookup"><span data-stu-id="0b02a-150">GL\_BACK</span></span>             | <span data-ttu-id="0b02a-151">modo que se aplica a polígonos traseiros</span><span class="sxs-lookup"><span data-stu-id="0b02a-151">mode which applies to back-facing polygons</span></span>                 |
| <span data-ttu-id="0b02a-152">GL \_ frontal \_ e \_ posterior</span><span class="sxs-lookup"><span data-stu-id="0b02a-152">GL\_FRONT\_AND\_BACK</span></span> | <span data-ttu-id="0b02a-153">modo que se aplica a polígonos frente e verso</span><span class="sxs-lookup"><span data-stu-id="0b02a-153">mode which applies to both front- and back-facing polygons</span></span> |



 

<span data-ttu-id="0b02a-154">O \_ modo de frente e de trás do GL \_ \_ é equivalente à função de **polimodo** do íris GL.</span><span class="sxs-lookup"><span data-stu-id="0b02a-154">The GL\_FRONT\_AND\_BACK mode is equivalent to the IRIS GL **polymode** function.</span></span> <span data-ttu-id="0b02a-155">A tabela a seguir lista os modos de polígono do íris GL e seus modos OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="0b02a-155">The following table lists IRIS GL polygon modes and their equivalent OpenGL modes.</span></span>



| <span data-ttu-id="0b02a-156">Modo GL de íris</span><span class="sxs-lookup"><span data-stu-id="0b02a-156">IRIS GL mode</span></span> | <span data-ttu-id="0b02a-157">Modo OpenGL</span><span class="sxs-lookup"><span data-stu-id="0b02a-157">OpenGL mode</span></span> | <span data-ttu-id="0b02a-158">Significado</span><span class="sxs-lookup"><span data-stu-id="0b02a-158">Meaning</span></span>                                       |
|--------------|-------------|-----------------------------------------------|
| <span data-ttu-id="0b02a-159">ponto de PYM \_</span><span class="sxs-lookup"><span data-stu-id="0b02a-159">PYM\_POINT</span></span>   | <span data-ttu-id="0b02a-160">\_ponto GL</span><span class="sxs-lookup"><span data-stu-id="0b02a-160">GL\_POINT</span></span>   | <span data-ttu-id="0b02a-161">Desenha vértices como pontos.</span><span class="sxs-lookup"><span data-stu-id="0b02a-161">Draws vertices as points.</span></span>                     |
| <span data-ttu-id="0b02a-162">PYM \_ linha</span><span class="sxs-lookup"><span data-stu-id="0b02a-162">PYM\_LINE</span></span>    | <span data-ttu-id="0b02a-163">\_linha GL</span><span class="sxs-lookup"><span data-stu-id="0b02a-163">GL\_LINE</span></span>    | <span data-ttu-id="0b02a-164">Desenha bordas de limite como segmentos de linha.</span><span class="sxs-lookup"><span data-stu-id="0b02a-164">Draws boundary edges as line segments.</span></span>        |
| <span data-ttu-id="0b02a-165">preenchimento de PYM \_</span><span class="sxs-lookup"><span data-stu-id="0b02a-165">PYM\_FILL</span></span>    | <span data-ttu-id="0b02a-166">preenchimento do GL \_</span><span class="sxs-lookup"><span data-stu-id="0b02a-166">GL\_FILL</span></span>    | <span data-ttu-id="0b02a-167">Desenha o interior do polígono cheio.</span><span class="sxs-lookup"><span data-stu-id="0b02a-167">Draws polygon interior filled.</span></span>                |
| <span data-ttu-id="0b02a-168">PYM \_ vazado</span><span class="sxs-lookup"><span data-stu-id="0b02a-168">PYM\_HOLLOW</span></span>  |             | <span data-ttu-id="0b02a-169">Preenche somente os pixels interiores nos limites.</span><span class="sxs-lookup"><span data-stu-id="0b02a-169">Fills only interior pixels at the boundaries.</span></span> |



 

## <a name="porting-polygon-stipples"></a><span data-ttu-id="0b02a-170">Stipples polígono de porta</span><span class="sxs-lookup"><span data-stu-id="0b02a-170">Porting Polygon Stipples</span></span>

<span data-ttu-id="0b02a-171">Ao portar stipples Polygon do íris GL, tenha os seguintes pontos em mente:</span><span class="sxs-lookup"><span data-stu-id="0b02a-171">When porting IRIS GL polygon stipples, keep the following points in mind:</span></span>

-   <span data-ttu-id="0b02a-172">O OpenGL não usa tabelas para polígono stipples; apenas um padrão Stipple é mantido.</span><span class="sxs-lookup"><span data-stu-id="0b02a-172">OpenGL doesn't use tables for polygon stipples; only one stipple pattern is kept.</span></span> <span data-ttu-id="0b02a-173">Você pode usar listas de exibição para armazenar diferentes padrões de Stipple.</span><span class="sxs-lookup"><span data-stu-id="0b02a-173">You can use display lists to store different stipple patterns.</span></span>
-   <span data-ttu-id="0b02a-174">O tamanho do bitmap Stipple do polígono do OpenGL é sempre um padrão de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="0b02a-174">The OpenGL polygon stipple bitmap size is always a 32x32 bit pattern.</span></span>
-   <span data-ttu-id="0b02a-175">A codificação Stipple é afetada por [**glPixelStore**](glpixelstore-functions.md).</span><span class="sxs-lookup"><span data-stu-id="0b02a-175">Stipple encoding is affected by [**glPixelStore**](glpixelstore-functions.md).</span></span>

<span data-ttu-id="0b02a-176">Para obter mais informações sobre como portar stipples Polygon, consulte [portando operações de pixel](porting-pixel-operations.md).</span><span class="sxs-lookup"><span data-stu-id="0b02a-176">For more information on porting polygon stipples, see [Porting Pixel Operations](porting-pixel-operations.md).</span></span>

<span data-ttu-id="0b02a-177">A tabela a seguir lista as funções Stipple de polígono do íris GL e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="0b02a-177">The following table lists IRIS GL polygon stipple functions and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="0b02a-178">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="0b02a-178">IRIS GL function</span></span> | <span data-ttu-id="0b02a-179">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="0b02a-179">OpenGL function</span></span>                                    | <span data-ttu-id="0b02a-180">Significado</span><span class="sxs-lookup"><span data-stu-id="0b02a-180">Meaning</span></span>                                               |
|------------------|----------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="0b02a-181">**defpattern**</span><span class="sxs-lookup"><span data-stu-id="0b02a-181">**defpattern**</span></span>   | [<span data-ttu-id="0b02a-182">**glPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="0b02a-182">**glPolygonStipple**</span></span>](glpolygonstipple.md)       | <span data-ttu-id="0b02a-183">Define o padrão Stipple.</span><span class="sxs-lookup"><span data-stu-id="0b02a-183">Sets the stipple pattern.</span></span>                             |
| <span data-ttu-id="0b02a-184">**setpattern**</span><span class="sxs-lookup"><span data-stu-id="0b02a-184">**setpattern**</span></span>   |                                                    | <span data-ttu-id="0b02a-185">O OpenGL mantém apenas um padrão Stipple de polígono.</span><span class="sxs-lookup"><span data-stu-id="0b02a-185">OpenGL keeps only one polygon stipple pattern.</span></span>        |
| <span data-ttu-id="0b02a-186">**GetPattern**</span><span class="sxs-lookup"><span data-stu-id="0b02a-186">**getpattern**</span></span>   | [<span data-ttu-id="0b02a-187">**glGetPolygonStipple**</span><span class="sxs-lookup"><span data-stu-id="0b02a-187">**glGetPolygonStipple**</span></span>](glgetpolygonstipple.md) | <span data-ttu-id="0b02a-188">Retorna o bitmap Stipple (usado para retornar um índice).</span><span class="sxs-lookup"><span data-stu-id="0b02a-188">Returns the stipple bitmap (used to return an index).</span></span> |



 

<span data-ttu-id="0b02a-189">No OpenGL, você habilita e desabilita o polígono stippling ao passar \_ \_ o Polygon do GL STIPPLE como um parâmetro para [**glEnable**](glenable.md) e [**glDisable**](gldisable.md).</span><span class="sxs-lookup"><span data-stu-id="0b02a-189">In OpenGL, you enable and disable polygon stippling by passing GL\_POLYGON\_STIPPLE as a parameter for [**glEnable**](glenable.md) and [**glDisable**](gldisable.md).</span></span>

<span data-ttu-id="0b02a-190">O exemplo de código OpenGL a seguir demonstra o polígono stippling:</span><span class="sxs-lookup"><span data-stu-id="0b02a-190">The following OpenGL code sample demonstrates polygon stippling:</span></span>


```C++
void display(void) 
{ 
    GLubyte fly[] = { 
      0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 0x00, 
      0x03, 0x80, 0x01, 0xC0, 0x06, 0xC0, 0x03, 0x60, 
      0x04, 0x60, 0x06, 0x20, 0x04, 0x30, 0x0C, 0x20, 
      0x04, 0x18, 0x18, 0x20, 0x04, 0x0C, 0x30, 0x20, 
      0x04, 0x06, 0x60, 0x20, 0x44, 0x03, 0xC0, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x44, 0x01, 0x80, 0x22, 0x44, 0x01, 0x80, 0x22, 
      0x66, 0x01, 0x80, 0x66, 0x33, 0x01, 0x80, 0xCC, 
      0x19, 0x81, 0x81, 0x98, 0x0C, 0xC1, 0x83, 0x30, 
      0x07, 0xe1, 0x87, 0xe0, 0x03, 0x3f, 0xfc, 0xc0, 
      0x03, 0x31, 0x8c, 0xc0, 0x03, 0x33, 0xcc, 0xc0, 
      0x06, 0x64, 0x26, 0x60, 0x0c, 0xcc, 0x33, 0x30, 
      0x18, 0xcc, 0x33, 0x18, 0x10, 0xc4, 0x23, 0x08, 
      0x10, 0x63, 0xC6, 0x08, 0x10, 0x30, 0x0c, 0x08, 
      0x10, 0x18, 0x18, 0x08, 0x10, 0x00, 0x00, 0x08 
    }; 
    GLubyte halftone[] = { 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55, 
      0xAA, 0xAA, 0xAA, 0xAA, 0x55, 0x55, 0x55, 0x55 
    }; 
 
    glClear (GL_COLOR_BUFFER_BIT); 
 
/*  draw all polygons in white*/ 
    glColor3f (1.0, 1.0, 1.0); 
 
/*  draw one solid, unstippled rectangle,*/ 
/*  then two stippled rectangles*/ 
    glRectf (25.0, 25.0, 125.0, 125.0); 
    glEnable (GL_POLYGON_STIPPLE); 
    glPolygonStipple (fly); 
    glRectf (125.0, 25.0, 225.0, 125.0); 
    glPolygonStipple (halftone); 
    glRectf (225.0, 25.0, 325.0, 125.0); 
    glDisable (GL_POLYGON_STIPPLE); 
 
    glFlush (); 
}
```



## <a name="porting-tessellated-polygons"></a><span data-ttu-id="0b02a-191">Portando polígonos mosaico</span><span class="sxs-lookup"><span data-stu-id="0b02a-191">Porting Tessellated Polygons</span></span>

<span data-ttu-id="0b02a-192">No íris GL, você usa o **côncavo**(**true**) e, em seguida, **bgnpolygon** para desenhar polígonos côncavos.</span><span class="sxs-lookup"><span data-stu-id="0b02a-192">In IRIS GL, you use **concave**(**TRUE**) and then **bgnpolygon** to draw concave polygons.</span></span> <span data-ttu-id="0b02a-193">O OpenGL GLU inclui funções que você pode usar para desenhar polígonos côncavos.</span><span class="sxs-lookup"><span data-stu-id="0b02a-193">The OpenGL GLU includes functions you can use to draw concave polygons.</span></span>

<span data-ttu-id="0b02a-194">**Para desenhar um polígono côncavo com OpenGL**</span><span class="sxs-lookup"><span data-stu-id="0b02a-194">**To draw a concave polygon with OpenGL**</span></span>

1.  <span data-ttu-id="0b02a-195">Crie um objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="0b02a-195">Create a tessellation object.</span></span>
2.  <span data-ttu-id="0b02a-196">Defina retornos de chamada que serão usados para processar os triângulos gerados pelo Tessellator.</span><span class="sxs-lookup"><span data-stu-id="0b02a-196">Define callbacks that will be used to process the triangles generated by the tessellator.</span></span>
3.  <span data-ttu-id="0b02a-197">Especifique o polígono côncavo a ser mosaico.</span><span class="sxs-lookup"><span data-stu-id="0b02a-197">Specify the concave polygon to be tessellated.</span></span>

<span data-ttu-id="0b02a-198">A tabela a seguir lista as funções OpenGL para desenhar polígonos mosaico.</span><span class="sxs-lookup"><span data-stu-id="0b02a-198">The following table lists the OpenGL functions for drawing tessellated polygons.</span></span>



| <span data-ttu-id="0b02a-199">Função OpenGL GLU</span><span class="sxs-lookup"><span data-stu-id="0b02a-199">OpenGL GLU function</span></span>                        | <span data-ttu-id="0b02a-200">Significado</span><span class="sxs-lookup"><span data-stu-id="0b02a-200">Meaning</span></span>                                                            |
|--------------------------------------------|--------------------------------------------------------------------|
| [<span data-ttu-id="0b02a-201">**gluNewTess**</span><span class="sxs-lookup"><span data-stu-id="0b02a-201">**gluNewTess**</span></span>](glunewtess.md)           | <span data-ttu-id="0b02a-202">Cria um novo objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="0b02a-202">Creates a new tessellation object.</span></span>                                 |
| [<span data-ttu-id="0b02a-203">**gluDeleteTess**</span><span class="sxs-lookup"><span data-stu-id="0b02a-203">**gluDeleteTess**</span></span>](gludeletetess.md)     | <span data-ttu-id="0b02a-204">Exclui um objeto de mosaico.</span><span class="sxs-lookup"><span data-stu-id="0b02a-204">Deletes a tessellation object.</span></span>                                     |
| [<span data-ttu-id="0b02a-205">*gluTessCallback*</span><span class="sxs-lookup"><span data-stu-id="0b02a-205">*gluTessCallback*</span></span>](glutess.md)           |                                                                    |
| [<span data-ttu-id="0b02a-206">**gluBeginPolygon**</span><span class="sxs-lookup"><span data-stu-id="0b02a-206">**gluBeginPolygon**</span></span>](glubeginpolygon.md) | <span data-ttu-id="0b02a-207">Inicia a especificação do polígono.</span><span class="sxs-lookup"><span data-stu-id="0b02a-207">Begins the polygon specification.</span></span>                                  |
| [<span data-ttu-id="0b02a-208">**gluTessVertex**</span><span class="sxs-lookup"><span data-stu-id="0b02a-208">**gluTessVertex**</span></span>](glutessvertex.md)     | <span data-ttu-id="0b02a-209">Especifica um vértice de polígono em uma delimitação.</span><span class="sxs-lookup"><span data-stu-id="0b02a-209">Specifies a polygon vertex in a contour.</span></span>                           |
| [<span data-ttu-id="0b02a-210">**gluNextContour**</span><span class="sxs-lookup"><span data-stu-id="0b02a-210">**gluNextContour**</span></span>](glunextcontour.md)   | <span data-ttu-id="0b02a-211">Indica que a próxima série de vértices descreve uma nova delimitação.</span><span class="sxs-lookup"><span data-stu-id="0b02a-211">Indicates that the next series of vertices describe a new contour.</span></span> |
| [<span data-ttu-id="0b02a-212">**gluEndPolygon**</span><span class="sxs-lookup"><span data-stu-id="0b02a-212">**gluEndPolygon**</span></span>](gluendpolygon.md)     | <span data-ttu-id="0b02a-213">Encerra a especificação do polígono.</span><span class="sxs-lookup"><span data-stu-id="0b02a-213">Ends the polygon specification.</span></span>                                    |



 

 

 





