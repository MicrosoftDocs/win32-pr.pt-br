---
title: Portando para cá
description: Ao portar para o OpenGL, tenha os seguintes pontos em mente
ms.assetid: ca6bb515-076d-45fc-bcdd-3d71877560fb
keywords:
- Portabilidade do íris GL,
- portando do íris GL,
- portando para OpenGL do íris GL,
- Portabilidade OpenGL do íris GL,
- funções de desenho,
- esferas
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9f48ac31c0204111173d9eb2d31a3119873ef45b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364171"
---
# <a name="porting-spheres"></a><span data-ttu-id="cda77-109">Portando para cá</span><span class="sxs-lookup"><span data-stu-id="cda77-109">Porting Spheres</span></span>

<span data-ttu-id="cda77-110">Ao portar para o OpenGL, tenha em mente os seguintes pontos:</span><span class="sxs-lookup"><span data-stu-id="cda77-110">When porting spheres to OpenGL, keep the following points in mind:</span></span>

-   <span data-ttu-id="cda77-111">Você não pode controlar o tipo de primitivas usadas para desenhar a esfera.</span><span class="sxs-lookup"><span data-stu-id="cda77-111">You cannot control the type of primitives used to draw the sphere.</span></span> <span data-ttu-id="cda77-112">Você pode controlar a precisão do desenho de outra maneira: Use os parâmetros Slices e Stacks.</span><span class="sxs-lookup"><span data-stu-id="cda77-112">You can control drawing precision in another way: use the slices and stacks parameters.</span></span> <span data-ttu-id="cda77-113">As fatias são longitudinal; as pilhas são latitudinais.</span><span class="sxs-lookup"><span data-stu-id="cda77-113">Slices are longitudinal; stacks are latitudinal.</span></span>
-   <span data-ttu-id="cda77-114">As difiram são desenhadas centralizadas na origem.</span><span class="sxs-lookup"><span data-stu-id="cda77-114">Spheres are drawn centered at the origin.</span></span> <span data-ttu-id="cda77-115">Em vez de especificar o local, como você faz com a função **sphdraw** do íris GL, preceda uma chamada para a função [**gluSphere**](glusphere.md) do Glu com uma tradução.</span><span class="sxs-lookup"><span data-stu-id="cda77-115">Instead of specifying the location, as you do with the IRIS GL **sphdraw** function, precede a call to the GLU [**gluSphere**](glusphere.md) function with a translation.</span></span>
-   <span data-ttu-id="cda77-116">A biblioteca de Sphere ainda não está disponível para OpenGL.</span><span class="sxs-lookup"><span data-stu-id="cda77-116">The sphere library is not yet available for OpenGL.</span></span>

<span data-ttu-id="cda77-117">A tabela a seguir lista as funções do íris GL para desenhar por meio das suas funções GLU equivalentes, quando disponíveis.</span><span class="sxs-lookup"><span data-stu-id="cda77-117">The following table lists the IRIS GL functions for drawing spheres and their equivalent GLU functions where available.</span></span>



| <span data-ttu-id="cda77-118">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="cda77-118">IRIS GL function</span></span> | <span data-ttu-id="cda77-119">Função GLU</span><span class="sxs-lookup"><span data-stu-id="cda77-119">GLU function</span></span>                                 | <span data-ttu-id="cda77-120">Significado</span><span class="sxs-lookup"><span data-stu-id="cda77-120">Meaning</span></span>                                       |
|------------------|----------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="cda77-121">**sphobj**</span><span class="sxs-lookup"><span data-stu-id="cda77-121">**sphobj**</span></span>       | [<span data-ttu-id="cda77-122">**gluNewQuadric**</span><span class="sxs-lookup"><span data-stu-id="cda77-122">**gluNewQuadric**</span></span>](glunewquadric.md)       | <span data-ttu-id="cda77-123">Cria um novo objeto de esfera.</span><span class="sxs-lookup"><span data-stu-id="cda77-123">Creates a new sphere object.</span></span>                  |
| <span data-ttu-id="cda77-124">**sphfree**</span><span class="sxs-lookup"><span data-stu-id="cda77-124">**sphfree**</span></span>      | [<span data-ttu-id="cda77-125">**gluDeleteQuadric**</span><span class="sxs-lookup"><span data-stu-id="cda77-125">**gluDeleteQuadric**</span></span>](gludeletequadric.md) | <span data-ttu-id="cda77-126">Exclui o objeto de esfera e a memória livre usada.</span><span class="sxs-lookup"><span data-stu-id="cda77-126">Deletes sphere object and free memory used.</span></span>   |
| <span data-ttu-id="cda77-127">**sphdraw**</span><span class="sxs-lookup"><span data-stu-id="cda77-127">**sphdraw**</span></span>      | [<span data-ttu-id="cda77-128">**gluSphere**</span><span class="sxs-lookup"><span data-stu-id="cda77-128">**gluSphere**</span></span>](glusphere.md)               | <span data-ttu-id="cda77-129">Desenha uma esfera.</span><span class="sxs-lookup"><span data-stu-id="cda77-129">Draws a sphere.</span></span>                               |
| <span data-ttu-id="cda77-130">**sphmode**</span><span class="sxs-lookup"><span data-stu-id="cda77-130">**sphmode**</span></span>      |                                              | <span data-ttu-id="cda77-131">Define os atributos de Sphere.</span><span class="sxs-lookup"><span data-stu-id="cda77-131">Sets sphere attributes.</span></span>                       |
| <span data-ttu-id="cda77-132">**sphrotmatrix**</span><span class="sxs-lookup"><span data-stu-id="cda77-132">**sphrotmatrix**</span></span> |                                              | <span data-ttu-id="cda77-133">Controla a orientação da esfera.</span><span class="sxs-lookup"><span data-stu-id="cda77-133">Controls sphere orientation.</span></span>                  |
| <span data-ttu-id="cda77-134">**sphgnpolys**</span><span class="sxs-lookup"><span data-stu-id="cda77-134">**sphgnpolys**</span></span>   |                                              | <span data-ttu-id="cda77-135">Retorna o número de polígonos na esfera atual.</span><span class="sxs-lookup"><span data-stu-id="cda77-135">Returns number of polygons in current sphere.</span></span> |



 

<span data-ttu-id="cda77-136">??</span><span class="sxs-lookup"><span data-stu-id="cda77-136">??</span></span>

 

 




