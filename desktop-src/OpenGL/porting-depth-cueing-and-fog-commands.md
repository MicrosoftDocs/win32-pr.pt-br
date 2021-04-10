---
title: Advertência de profundidade de portabilidade e comandos de neblina
description: Advertência de profundidade de portabilidade e comandos de neblina
ms.assetid: 16982d11-88a1-4a35-960f-28f10491e0ac
keywords:
- Portabilidade do íris GL, advertência de profundidade
- portando do íris GL, Depth advertência
- portando para OpenGL do íris GL, Depth advertência
- Portabilidade OpenGL do íris GL, Depth advertência
- Portabilidade do íris GL, neblina
- portando do íris GL, neblina
- portando para OpenGL do íris GL, neblina
- Portabilidade OpenGL do íris GL, neblina
- advertência de profundidade
- neblina
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fd9f65a29e0ae594bf9344cd960d3fc2b9aa646
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104160207"
---
# <a name="porting-depth-cueing-and-fog-commands"></a><span data-ttu-id="50026-113">Advertência de profundidade de portabilidade e comandos de neblina</span><span class="sxs-lookup"><span data-stu-id="50026-113">Porting Depth Cueing and Fog Commands</span></span>

<span data-ttu-id="50026-114">Ao portar comandos de profundidade-advertência e sombra, tenha os seguintes pontos em mente:</span><span class="sxs-lookup"><span data-stu-id="50026-114">When porting depth-cueing and fog commands, keep the following points in mind:</span></span>

-   <span data-ttu-id="50026-115">A chamada do íris GL, **fogvertex**, define um modo e os parâmetros que afetam esse modo.</span><span class="sxs-lookup"><span data-stu-id="50026-115">The IRIS GL call, **fogvertex**, sets a mode and the parameters affecting that mode.</span></span> <span data-ttu-id="50026-116">No OpenGL, você chama [**glFog**](glfog.md) uma vez para definir o modo e, em seguida, duas vezes ou mais para definir vários parâmetros.</span><span class="sxs-lookup"><span data-stu-id="50026-116">In OpenGL, you call [**glFog**](glfog.md) once to set the mode, and then again twice or more to set various parameters.</span></span>
-   <span data-ttu-id="50026-117">No OpenGL, advertência de profundidade não é um recurso separado.</span><span class="sxs-lookup"><span data-stu-id="50026-117">In OpenGL, depth cueing is not a separate feature.</span></span> <span data-ttu-id="50026-118">Use a neblina linear em vez de profundidade advertência.</span><span class="sxs-lookup"><span data-stu-id="50026-118">Use linear fog instead of depth cueing.</span></span> <span data-ttu-id="50026-119">(Esta seção fornece um exemplo de como fazer isso.) As seguintes funções do íris GL não têm equivalente a OpenGL direto:</span><span class="sxs-lookup"><span data-stu-id="50026-119">(This section gives an example of how to do this.) The following IRIS GL functions have no direct OpenGL equivalent:</span></span>

    <span data-ttu-id="50026-120">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="50026-120">**depthcue**</span></span>

    <span data-ttu-id="50026-121">**lRGBrange**</span><span class="sxs-lookup"><span data-stu-id="50026-121">**lRGBrange**</span></span>

    <span data-ttu-id="50026-122">**lshaderange**</span><span class="sxs-lookup"><span data-stu-id="50026-122">**lshaderange**</span></span>

    <span data-ttu-id="50026-123">**getdcm**</span><span class="sxs-lookup"><span data-stu-id="50026-123">**getdcm**</span></span>

-   <span data-ttu-id="50026-124">Para ajustar a qualidade da neblina, use [**glHint**](glhint.md)(dica de neblina do GL \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="50026-124">To adjust fog quality, use [**glHint**](glhint.md)( GL\_FOG\_HINT ).</span></span>

<span data-ttu-id="50026-125">A tabela a seguir lista as funções do íris GL para gerenciar a neblina e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="50026-125">The following table lists the IRIS GL functions for managing fog and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="50026-126">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="50026-126">IRIS GL function</span></span>         | <span data-ttu-id="50026-127">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="50026-127">OpenGL function</span></span>                                     | <span data-ttu-id="50026-128">Significado</span><span class="sxs-lookup"><span data-stu-id="50026-128">Meaning</span></span>                           |
|--------------------------|-----------------------------------------------------|-----------------------------------|
| <span data-ttu-id="50026-129">**fogvertex**</span><span class="sxs-lookup"><span data-stu-id="50026-129">**fogvertex**</span></span>            | [<span data-ttu-id="50026-130">**glFog**</span><span class="sxs-lookup"><span data-stu-id="50026-130">**glFog**</span></span>](glfog.md)                              | <span data-ttu-id="50026-131">Define vários parâmetros de neblina.</span><span class="sxs-lookup"><span data-stu-id="50026-131">Sets various fog parameters.</span></span>      |
| <span data-ttu-id="50026-132">**fogvertex**(FG \_ ligado)</span><span class="sxs-lookup"><span data-stu-id="50026-132">**fogvertex**( FG\_ON )</span></span>  | <span data-ttu-id="50026-133">[**glEnable**](glenable.md) (neblina do GL \_ )</span><span class="sxs-lookup"><span data-stu-id="50026-133">[**glEnable**](glenable.md) ( GL\_FOG )</span></span>            | <span data-ttu-id="50026-134">Ativa a neblina.</span><span class="sxs-lookup"><span data-stu-id="50026-134">Turns on fog.</span></span>                     |
| <span data-ttu-id="50026-135">**fogvertex**(FG \_ desativado)</span><span class="sxs-lookup"><span data-stu-id="50026-135">**fogvertex**( FG\_OFF )</span></span> | <span data-ttu-id="50026-136">[**glDisable**](gldisable.md) (neblina do GL \_ )</span><span class="sxs-lookup"><span data-stu-id="50026-136">[**glDisable**](gldisable.md) ( GL\_FOG )</span></span>          | <span data-ttu-id="50026-137">Desativa a neblina.</span><span class="sxs-lookup"><span data-stu-id="50026-137">Turns off fog.</span></span>                    |
| <span data-ttu-id="50026-138">**depthcue**</span><span class="sxs-lookup"><span data-stu-id="50026-138">**depthcue**</span></span>             | <span data-ttu-id="50026-139">[**glFog**](glfog.md) (GL \_ neblina \_ mod, GL \_ linear)</span><span class="sxs-lookup"><span data-stu-id="50026-139">[**glFog**](glfog.md) ( GL\_FOG\_MOD, GL\_LINEAR )</span></span> | <span data-ttu-id="50026-140">Usa a neblina linear para advertência de profundidade.</span><span class="sxs-lookup"><span data-stu-id="50026-140">Uses linear fog for depth cueing.</span></span> |



 

<span data-ttu-id="50026-141">A tabela a seguir lista os parâmetros que você pode passar para **glFog**.</span><span class="sxs-lookup"><span data-stu-id="50026-141">The following table lists the parameters you can pass to **glFog**.</span></span>



| <span data-ttu-id="50026-142">Parâmetro de neblina</span><span class="sxs-lookup"><span data-stu-id="50026-142">Fog parameter</span></span>    | <span data-ttu-id="50026-143">Significado</span><span class="sxs-lookup"><span data-stu-id="50026-143">Meaning</span></span>                       | <span data-ttu-id="50026-144">Padrão</span><span class="sxs-lookup"><span data-stu-id="50026-144">Default</span></span>                  |
|------------------|-------------------------------|--------------------------|
| <span data-ttu-id="50026-145">\_densidade de neblina GL \_</span><span class="sxs-lookup"><span data-stu-id="50026-145">GL\_FOG\_DENSITY</span></span> | <span data-ttu-id="50026-146">Densidade da neblina.</span><span class="sxs-lookup"><span data-stu-id="50026-146">Fog density.</span></span>                  | <span data-ttu-id="50026-147">1,0</span><span class="sxs-lookup"><span data-stu-id="50026-147">1.0</span></span>                      |
| <span data-ttu-id="50026-148">\_início da neblina do GL \_</span><span class="sxs-lookup"><span data-stu-id="50026-148">GL\_FOG\_START</span></span>   | <span data-ttu-id="50026-149">Perto da distância para a neblina linear.</span><span class="sxs-lookup"><span data-stu-id="50026-149">Near distance for linear fog.</span></span> | <span data-ttu-id="50026-150">0.0</span><span class="sxs-lookup"><span data-stu-id="50026-150">0.0</span></span>                      |
| <span data-ttu-id="50026-151">\_fim da neblina do GL \_</span><span class="sxs-lookup"><span data-stu-id="50026-151">GL\_FOG\_END</span></span>     | <span data-ttu-id="50026-152">Distância distante para a neblina linear.</span><span class="sxs-lookup"><span data-stu-id="50026-152">Far distance for linear fog.</span></span>  | <span data-ttu-id="50026-153">1,0</span><span class="sxs-lookup"><span data-stu-id="50026-153">1.0</span></span>                      |
| <span data-ttu-id="50026-154">\_índice de neblina GL \_</span><span class="sxs-lookup"><span data-stu-id="50026-154">GL\_FOG\_INDEX</span></span>   | <span data-ttu-id="50026-155">Índice de cores de neblina.</span><span class="sxs-lookup"><span data-stu-id="50026-155">Fog color index.</span></span>              | <span data-ttu-id="50026-156">0.0</span><span class="sxs-lookup"><span data-stu-id="50026-156">0.0</span></span>                      |
| <span data-ttu-id="50026-157">\_cor da neblina do GL \_</span><span class="sxs-lookup"><span data-stu-id="50026-157">GL\_FOG\_COLOR</span></span>   | <span data-ttu-id="50026-158">Cor RGBA de neblina.</span><span class="sxs-lookup"><span data-stu-id="50026-158">Fog RGBA color.</span></span>               | <span data-ttu-id="50026-159">(0, 0, 0, 0)</span><span class="sxs-lookup"><span data-stu-id="50026-159">(0, 0, 0, 0)</span></span>             |
| <span data-ttu-id="50026-160">\_modo de neblina GL \_</span><span class="sxs-lookup"><span data-stu-id="50026-160">GL\_FOG\_MODE</span></span>    | <span data-ttu-id="50026-161">Modo de neblina.</span><span class="sxs-lookup"><span data-stu-id="50026-161">Fog mode.</span></span>                     | <span data-ttu-id="50026-162">Confira a tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="50026-162">See the following table.</span></span> |



 

<span data-ttu-id="50026-163">O parâmetro de densidade de neblina do OpenGL difere do um no íris GL.</span><span class="sxs-lookup"><span data-stu-id="50026-163">The fog-density parameter of OpenGL differs from the one in IRIS GL.</span></span> <span data-ttu-id="50026-164">Eles estão relacionados da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="50026-164">They are related as follows:</span></span>

-   <span data-ttu-id="50026-165">Se *fogMode* = EXP2</span><span class="sxs-lookup"><span data-stu-id="50026-165">if *fogMode* = EXP2</span></span>
     

    <span data-ttu-id="50026-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** (1/255)))</span><span class="sxs-lookup"><span data-stu-id="50026-166">*openGLfogDensity* = (*irisGLfogDensity* ) ( **sqrt** ( **log** ( 1 / 255 ) ))</span></span>
-   <span data-ttu-id="50026-167">Se *fogMode* = exp</span><span class="sxs-lookup"><span data-stu-id="50026-167">if *fogMode* = EXP</span></span>
     

    <span data-ttu-id="50026-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** (1/255))</span><span class="sxs-lookup"><span data-stu-id="50026-168">*openGLfogDensity* = (*irisGLfogDensity* ) ( **log** ( 1 / 255 ) )</span></span>

<span data-ttu-id="50026-169">em que **sqrt** é a operação raiz quadrada, o **log** é o logaritmo natural, *irisGLfogDensity* é a densidade de neblina do íris GL e *OpenGLfogDensity* é a densidade de neblina do OpenGL.</span><span class="sxs-lookup"><span data-stu-id="50026-169">where **sqrt** is the square root operation, **log** is the natural logarithm, *irisGLfogDensity* is the IRIS GL fog density, and *openGLfogDensity* is the OpenGL fog density.</span></span>

<span data-ttu-id="50026-170">Para alternar entre calcular a sombra no modo por pixel e por vértice, use [**glHint**](glhint.md)( \_ dica de neblina do GL \_ , *hintmode*).</span><span class="sxs-lookup"><span data-stu-id="50026-170">To switch between calculating fog in per-pixel mode and per-vertex mode, use [**glHint**](glhint.md)( GL\_FOG\_HINT, *hintMode*).</span></span> <span data-ttu-id="50026-171">Dois modos de dica estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="50026-171">Two hint modes are available:</span></span>

-   <span data-ttu-id="50026-172">RAZÃO \_ de cálculo de neblina por pixel mais interessante</span><span class="sxs-lookup"><span data-stu-id="50026-172">GL\_NICEST per-pixel fog calculation</span></span>
-   <span data-ttu-id="50026-173">\_Redirecionamento rápido por vértice de cálculo de neblina</span><span class="sxs-lookup"><span data-stu-id="50026-173">GL\_FASTEST per-vertex fog calculation</span></span>

<span data-ttu-id="50026-174">A tabela a seguir lista os modos de neblina do íris GL e seus equivalentes em OpenGL.</span><span class="sxs-lookup"><span data-stu-id="50026-174">The following table lists the IRIS GL fog modes and their OpenGL equivalents.</span></span>



| <span data-ttu-id="50026-175">Modo de neblina GL de íris</span><span class="sxs-lookup"><span data-stu-id="50026-175">IRIS GL fog mode</span></span>                       | <span data-ttu-id="50026-176">Modo de neblina OpenGL</span><span class="sxs-lookup"><span data-stu-id="50026-176">OpenGL fog mode</span></span> | <span data-ttu-id="50026-177">Modo de dica</span><span class="sxs-lookup"><span data-stu-id="50026-177">Hint mode</span></span>                         | <span data-ttu-id="50026-178">Significado</span><span class="sxs-lookup"><span data-stu-id="50026-178">Meaning</span></span>                                  |
|----------------------------------------|-----------------|-----------------------------------|------------------------------------------|
| <span data-ttu-id="50026-179">FG \_ VTX \_ exp, FG \_ PIX \_ exp</span><span class="sxs-lookup"><span data-stu-id="50026-179">FG\_VTX\_EXP,FG\_PIX\_EXP</span></span><br/>   | <span data-ttu-id="50026-180">GL \_ exp</span><span class="sxs-lookup"><span data-stu-id="50026-180">GL\_EXP</span></span>         | <span data-ttu-id="50026-181">GL \_ mais rápido, GL mais \_ interessante</span><span class="sxs-lookup"><span data-stu-id="50026-181">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="50026-182">Modo de neblina pesada (padrão).</span><span class="sxs-lookup"><span data-stu-id="50026-182">Heavy fog mode (default).</span></span>                |
| <span data-ttu-id="50026-183">FG \_ VTX \_ EXP2, FG \_ PIX \_ EXP2</span><span class="sxs-lookup"><span data-stu-id="50026-183">FG\_VTX\_EXP2,FG\_PIX\_EXP2</span></span><br/> | <span data-ttu-id="50026-184">\_EXP2 GL</span><span class="sxs-lookup"><span data-stu-id="50026-184">GL\_EXP2</span></span>        | <span data-ttu-id="50026-185">GL \_ mais rápido, GL mais \_ interessante</span><span class="sxs-lookup"><span data-stu-id="50026-185">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="50026-186">Modo de criações.</span><span class="sxs-lookup"><span data-stu-id="50026-186">Haze mode.</span></span>                               |
| <span data-ttu-id="50026-187">FG \_ VTX \_ Lin, FG \_ PIX \_ Lin</span><span class="sxs-lookup"><span data-stu-id="50026-187">FG\_VTX\_LIN,FG\_PIX\_LIN</span></span><br/>   | <span data-ttu-id="50026-188">GL \_ linear</span><span class="sxs-lookup"><span data-stu-id="50026-188">GL\_LINEAR</span></span>      | <span data-ttu-id="50026-189">GL \_ mais rápido, GL mais \_ interessante</span><span class="sxs-lookup"><span data-stu-id="50026-189">GL\_FASTEST,GL\_NICEST</span></span><br/> | <span data-ttu-id="50026-190">Modo de neblina linear.</span><span class="sxs-lookup"><span data-stu-id="50026-190">Linear fog mode.</span></span> <span data-ttu-id="50026-191">(Use para advertência de profundidade.)</span><span class="sxs-lookup"><span data-stu-id="50026-191">(Use for depth cueing.)</span></span> |



 

<span data-ttu-id="50026-192">O exemplo de código a seguir demonstra advertência de profundidade em OpenGL:</span><span class="sxs-lookup"><span data-stu-id="50026-192">The following code example demonstrates depth cueing in OpenGL:</span></span>


```C++
/* 
 *  depthcue.c 
 *  This program draws a wire frame model, which uses 
 *  intensity (brightness) to give clues to distance 
 *  Fog is used to achieve this effect 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
/*  Initialize linear fog for depth cueing 
 */ 
void myinit(void) 
{ 
    GLfloat fogColor[4] = {0.0, 0.0, 0.0, 1.0}; 
 
    glEnable(GL_FOG); 
    glFogi (GL_FOG_MODE, GL_LINEAR); 
    glHint (GL_FOG_HINT, GL_NICEST);  /*  per pixel  */ 
    glFogf (GL_FOG_START, 3.0); 
    glFogf (GL_FOG_END, 5.0); 
    glFogfv (GL_FOG_COLOR, fogColor); 
    glClearColor(0.0, 0.0, 0.0, 1.0); 
 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glShadeModel(GL_FLAT); 
} 
 
/*  display() draws an icosahedron 
 */ 
void display(void) 
{ 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glColor3f (1.0, 1.0, 1.0); 
    auxWireIcosahedron(1.0); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLfloat) w/(GLfloat) h, 3.0, 5.0); 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity (); 
    glTranslatef (0.0, 0.0, -4.0); /*move object into view*/ 
} 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 400, 400); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 





