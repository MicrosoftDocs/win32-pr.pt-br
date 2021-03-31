---
title: Portando superfícies NURBS
description: A tabela a seguir lista as funções do íris GL para desenhar superfícies NURBS e suas funções OpenGL equivalentes.
ms.assetid: d34ac6af-55d7-4128-bcd9-3c910607895f
keywords:
- Portabilidade do íris GL, superfícies NURBS
- portando do íris GL, superfícies NURBS
- portando para OpenGL do íris GL, superfícies NURBS
- Portabilidade do OpenGL do íris GL, superfícies NURBS
- Superfícies NURBS
- NURBS (B racional não uniforme-spline)
- B-spline racional não uniforme (NURBS)
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f7260750db4d221743d3e764d6dd30e2de499383
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103636573"
---
# <a name="porting-nurbs-surfaces"></a><span data-ttu-id="b6c3c-110">Portando superfícies NURBS</span><span class="sxs-lookup"><span data-stu-id="b6c3c-110">Porting NURBS Surfaces</span></span>

<span data-ttu-id="b6c3c-111">A tabela a seguir lista as funções do íris GL para desenhar superfícies NURBS e suas funções OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-111">The following table lists the IRIS GL functions for drawing NURBS surfaces and their equivalent OpenGL functions.</span></span>



| <span data-ttu-id="b6c3c-112">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="b6c3c-112">IRIS GL function</span></span> | <span data-ttu-id="b6c3c-113">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="b6c3c-113">OpenGL function</span></span>                            | <span data-ttu-id="b6c3c-114">Significado</span><span class="sxs-lookup"><span data-stu-id="b6c3c-114">Meaning</span></span>                       |
|------------------|--------------------------------------------|-------------------------------|
| <span data-ttu-id="b6c3c-115">**bgnsurface**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-115">**bgnsurface**</span></span>   | [<span data-ttu-id="b6c3c-116">**gluBeginSurface**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-116">**gluBeginSurface**</span></span>](glubeginsurface.md) | <span data-ttu-id="b6c3c-117">Inicia uma definição de superfície.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-117">Begins a surface definition.</span></span>  |
| <span data-ttu-id="b6c3c-118">**nurbssurface**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-118">**nurbssurface**</span></span> | [<span data-ttu-id="b6c3c-119">**gluNurbsSurface**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-119">**gluNurbsSurface**</span></span>](glunurbssurface.md) | <span data-ttu-id="b6c3c-120">Especifica os atributos da superfície.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-120">Specifies surface attributes.</span></span> |
| <span data-ttu-id="b6c3c-121">**área de fim**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-121">**endsurface**</span></span>   | [<span data-ttu-id="b6c3c-122">**gluEndSurface**</span><span class="sxs-lookup"><span data-stu-id="b6c3c-122">**gluEndSurface**</span></span>](gluendsurface.md)     | <span data-ttu-id="b6c3c-123">Finaliza uma definição de superfície.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-123">Ends a surface definition.</span></span>    |



 

<span data-ttu-id="b6c3c-124">A tabela a seguir lista os parâmetros do íris GL para tipos de superfície e seus parâmetros OpenGL equivalentes.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-124">The following table lists IRIS GL parameters for surface types and their equivalent OpenGL parameters.</span></span>



| <span data-ttu-id="b6c3c-125">Tipo de GL de íris</span><span class="sxs-lookup"><span data-stu-id="b6c3c-125">IRIS GL type</span></span> | <span data-ttu-id="b6c3c-126">Tipo OpenGL</span><span class="sxs-lookup"><span data-stu-id="b6c3c-126">OpenGL type</span></span>                 | <span data-ttu-id="b6c3c-127">Significado</span><span class="sxs-lookup"><span data-stu-id="b6c3c-127">Meaning</span></span>                                                |
|--------------|-----------------------------|--------------------------------------------------------|
| <span data-ttu-id="b6c3c-128">N \_ V3D</span><span class="sxs-lookup"><span data-stu-id="b6c3c-128">N\_V3D</span></span>       | <span data-ttu-id="b6c3c-129">GL \_ map2 \_ Vertex \_ 3</span><span class="sxs-lookup"><span data-stu-id="b6c3c-129">GL\_MAP2\_VERTEX\_3</span></span>         | <span data-ttu-id="b6c3c-130">Curva polinomial.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-130">Polynomial curve.</span></span>                                      |
| <span data-ttu-id="b6c3c-131">N \_ V3DR</span><span class="sxs-lookup"><span data-stu-id="b6c3c-131">N\_V3DR</span></span>      | <span data-ttu-id="b6c3c-132">Map2 do GL de \_ \_ vértice \_ 4</span><span class="sxs-lookup"><span data-stu-id="b6c3c-132">GL\_MAP2\_VERTEX\_4</span></span>         | <span data-ttu-id="b6c3c-133">Curva racional.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-133">Rational curve.</span></span>                                        |
| <span data-ttu-id="b6c3c-134">N \_ C4D</span><span class="sxs-lookup"><span data-stu-id="b6c3c-134">N\_C4D</span></span>       | <span data-ttu-id="b6c3c-135">GL \_ map2 \_ cor \_ 4</span><span class="sxs-lookup"><span data-stu-id="b6c3c-135">GL\_MAP2\_COLOR\_4</span></span>          | <span data-ttu-id="b6c3c-136">Os pontos de controle definem A superfície de cores no formulário (R, G, B, A).</span><span class="sxs-lookup"><span data-stu-id="b6c3c-136">Control points define color surface in (R,G,B,A) form.</span></span> |
| <span data-ttu-id="b6c3c-137">N \_ C4DR</span><span class="sxs-lookup"><span data-stu-id="b6c3c-137">N\_C4DR</span></span>      |                             |                                                        |
| <span data-ttu-id="b6c3c-138">N \_ T2D</span><span class="sxs-lookup"><span data-stu-id="b6c3c-138">N\_T2D</span></span>       | <span data-ttu-id="b6c3c-139">GL \_ map2 \_ Texture \_ coord \_ 2</span><span class="sxs-lookup"><span data-stu-id="b6c3c-139">GL\_MAP2\_TEXTURE\_COORD\_2</span></span> | <span data-ttu-id="b6c3c-140">Pontos de controle são coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-140">Control points are texture coordinates.</span></span>                |
| <span data-ttu-id="b6c3c-141">N \_ T2DR</span><span class="sxs-lookup"><span data-stu-id="b6c3c-141">N\_T2DR</span></span>      | <span data-ttu-id="b6c3c-142">GL \_ map2 \_ Texture \_ coord \_ 3</span><span class="sxs-lookup"><span data-stu-id="b6c3c-142">GL\_MAP2\_TEXTURE\_COORD\_3</span></span> | <span data-ttu-id="b6c3c-143">Pontos de controle são coordenadas de textura.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-143">Control points are texture coordinates.</span></span>                |
|              | <span data-ttu-id="b6c3c-144">GL \_ map2 \_ normal</span><span class="sxs-lookup"><span data-stu-id="b6c3c-144">GL\_MAP2\_NORMAL</span></span>            | <span data-ttu-id="b6c3c-145">Os pontos de controle são normais.</span><span class="sxs-lookup"><span data-stu-id="b6c3c-145">Control points are normals.</span></span>                            |



 

<span data-ttu-id="b6c3c-146">Para obter mais informações sobre os tipos de avaliadores disponíveis, consulte [**glMap2**](glmap2.md).</span><span class="sxs-lookup"><span data-stu-id="b6c3c-146">For more information on available evaluator types, see [**glMap2**](glmap2.md).</span></span>

<span data-ttu-id="b6c3c-147">O exemplo de código a seguir desenha uma superfície NURBS cortada:</span><span class="sxs-lookup"><span data-stu-id="b6c3c-147">The following code sample draws a trimmed NURBS surface:</span></span>


```C++
/* 
 *  trim.c 
 *  This program draws a NURBS surface in the shape of a 
 *  symmetrical hill, using both a NURBS curve and pwl 
 *  (piecewise linear) curve to trim part of the surface 
 */ 
#include <GL/gl.h> 
#include <GL/glu.h> 
#include "aux.h" 
 
GLfloat ctlpoints[4][4][3]; 
 
GLUnurbsObj *theNurb; 
 
/* 
 *  Initializes the control points of the surface to  
 *  a small hill. The control points range from -3 to  
 *  +3 in x, y, and z 
 */ 
void init_surface(void) 
{ 
    int u, v; 
    for (u = 0; u < 4; u++) { 
        for (v = 0; v < 4; v++) { 
            ctlpoints[u][v][0] = 2.0*((GLfloat)u - 1.5); 
            ctlpoints[u][v][1] = 2.0*((GLfloat)v - 1.5); 
 
            if ( (u == 1 || u == 2) && (v == 1 || v == 2)) 
                ctlpoints[u][v][2] = 3.0; 
            else 
                ctlpoints[u][v][2] = -3.0; 
        } 
    } 
} 
 
/*  Initialize material property and depth buffer 
 */ 
void myinit(void) 
{ 
    GLfloat mat_diffuse[] = { 0.6, 0.6, 0.6, 1.0 }; 
    GLfloat mat_specular[] = { 0.9, 0.9, 0.9, 1.0 }; 
    GLfloat mat_shininess[] = { 128.0 }; 
 
    glClearColor (0.0, 0.0, 0.0, 1.0); 
    glMaterialfv(GL_FRONT, GL_DIFFUSE, mat_diffuse); 
    glMaterialfv(GL_FRONT, GL_SPECULAR, mat_specular); 
    glMaterialfv(GL_FRONT, GL_SHININESS, mat_shininess); 
 
    glEnable(GL_LIGHTING); 
    glEnable(GL_LIGHT0); 
    glDepthFunc(GL_LEQUAL); 
    glEnable(GL_DEPTH_TEST); 
    glEnable(GL_AUTO_NORMAL); 
    glEnable(GL_NORMALIZE); 
 
    init_surface(); 
 
    theNurb = gluNewNurbsRenderer(); 
    gluNurbsProperty(theNurb, GLU_SAMPLING_TOLERANCE, 50.0); 
    gluNurbsProperty(theNurb, GLU_DISPLAY_MODE, GLU_FILL); 
} 
 
void display(void) 
{ 
    GLfloat knots[8] = {0.0, 0.0, 0.0, 0.0, 1.0, 1.0, 1.0, 1.0}; 
    GLfloat edgePt[5][2] = /* counter clockwise */ 
    {{0.0, 0.0}, {1.0, 0.0}, {1.0, 1.0}, {0.0, 1.0}, 
     {0.0, 0.0}}; 
    GLfloat curvePt[4][2] = /* clockwise */ 
    {{0.25, 0.5}, {0.25, 0.75}, {0.75, 0.75}, {0.75, 0.5}}; 
    GLfloat curveKnots[8] = 
        {0.0, 0.0, 0.0, 0.0, 1.0, 1.0, 1.0, 1.0}; 
    GLfloat pwlPt[4][2] = /* clockwise */ 
        {{0.75, 0.5}, {0.5, 0.25}, {0.25, 0.5}}; 
 
    glClear(GL_COLOR_BUFFER_BIT | GL_DEPTH_BUFFER_BIT); 
    glPushMatrix(); 
    glRotatef(330.0, 1.,0.,0.); 
    glScalef (0.5, 0.5, 0.5); 
 
    gluBeginSurface(theNurb); 
    gluNurbsSurface(theNurb, 
            8, knots, 
            8, knots, 
            4 * 3, 
            3, 
            &ctlpoints[0][0][0], 
            4, 4, 
            GL_MAP2_VERTEX_3); 
    gluBeginTrim (theNurb); 
        gluPwlCurve (theNurb, 5, &edgePt[0][0], 2, 
                     GLU_MAP1_TRIM_2); 
    gluEndTrim (theNurb); 
    gluBeginTrim (theNurb); 
        gluNurbsCurve (theNurb, 8, curveKnots, 2, 
                &curvePt[0][0], 4, GLU_MAP1_TRIM_2); 
        gluPwlCurve (theNurb, 3, &pwlPt[0][0], 2, 
                     GLU_MAP1_TRIM_2); 
    gluEndTrim (theNurb); 
    gluEndSurface(theNurb); 
 
    glPopMatrix(); 
    glFlush(); 
} 
 
void myReshape(GLsizei w, GLsizei h) 
{ 
    glViewport(0, 0, w, h); 
    glMatrixMode(GL_PROJECTION); 
    glLoadIdentity(); 
    gluPerspective (45.0, (GLdouble)w/(GLdouble)h, 3.0, 8.0); 
 
    glMatrixMode(GL_MODELVIEW); 
    glLoadIdentity(); 
    glTranslatef (0.0, 0.0, -5.0); 
} 
 
/*  Main Loop 
 */ 
int main(int argc, char** argv) 
{ 
    auxInitDisplayMode (AUX_SINGLE | AUX_RGBA | AUX_DEPTH); 
    auxInitPosition (0, 0, 500, 500); 
    auxInitWindow (argv[0]); 
    myinit(); 
    auxReshapeFunc (myReshape); 
    auxMainLoop(display); 
}
```



 

 




