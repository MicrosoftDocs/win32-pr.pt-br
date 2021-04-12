---
title: Portando arcos e círculos
description: Com o OpenGL, arcos e círculos preenchidos são desenhados com as mesmas chamadas como arcos e círculos não preenchidos. A tabela a seguir lista as funções de arco e de círculo da íris GL e suas funções OpenGL (GLU) equivalentes.
ms.assetid: b3458192-9cb6-4376-8136-45467584d3d4
keywords:
- Portabilidade do íris GL, arcos
- portando do íris GL, arcos
- portando para OpenGL do íris GL, arcos
- Portabilidade do OpenGL do íris GL, arcos
- funções de desenho, arcos
- Portabilidade do íris GL, círculos
- portando do íris GL, círculos
- portando para OpenGL do íris GL, círculos
- Portabilidade OpenGL do íris GL, círculos
- funções de desenho, círculos
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7ce17546ce17f24adf80641549d8843a473c8754
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104364425"
---
# <a name="porting-arcs-and-circles"></a><span data-ttu-id="a66c9-114">Portando arcos e círculos</span><span class="sxs-lookup"><span data-stu-id="a66c9-114">Porting Arcs and Circles</span></span>

<span data-ttu-id="a66c9-115">Com o OpenGL, arcos e círculos preenchidos são desenhados com as mesmas chamadas como arcos e círculos não preenchidos.</span><span class="sxs-lookup"><span data-stu-id="a66c9-115">With OpenGL, filled arcs and circles are drawn with the same calls as unfilled arcs and circles.</span></span> <span data-ttu-id="a66c9-116">A tabela a seguir lista as funções de arco e de círculo da íris GL e suas funções OpenGL (GLU) equivalentes.</span><span class="sxs-lookup"><span data-stu-id="a66c9-116">The following table lists the IRIS GL arc and circle functions and their equivalent OpenGL (GLU) functions.</span></span>



| <span data-ttu-id="a66c9-117">Função GL de íris</span><span class="sxs-lookup"><span data-stu-id="a66c9-117">IRIS GL function</span></span> | <span data-ttu-id="a66c9-118">Função OpenGL</span><span class="sxs-lookup"><span data-stu-id="a66c9-118">OpenGL function</span></span>                          | <span data-ttu-id="a66c9-119">Significado</span><span class="sxs-lookup"><span data-stu-id="a66c9-119">Meaning</span></span>                 |
|------------------|------------------------------------------|-------------------------|
| <span data-ttu-id="a66c9-120">**arcarcf**</span><span class="sxs-lookup"><span data-stu-id="a66c9-120">**arcarcf**</span></span>      | [<span data-ttu-id="a66c9-121">**gluPartialDisk**</span><span class="sxs-lookup"><span data-stu-id="a66c9-121">**gluPartialDisk**</span></span>](glupartialdisk.md) | <span data-ttu-id="a66c9-122">Desenha um arco.</span><span class="sxs-lookup"><span data-stu-id="a66c9-122">Draws an arc.</span></span>           |
| <span data-ttu-id="a66c9-123">**circcircf**</span><span class="sxs-lookup"><span data-stu-id="a66c9-123">**circcircf**</span></span>    | [<span data-ttu-id="a66c9-124">**gluDisk**</span><span class="sxs-lookup"><span data-stu-id="a66c9-124">**gluDisk**</span></span>](gludisk.md)               | <span data-ttu-id="a66c9-125">Desenha um círculo ou disco.</span><span class="sxs-lookup"><span data-stu-id="a66c9-125">Draws a circle or disk.</span></span> |



 

<span data-ttu-id="a66c9-126">Você pode fazer algumas coisas com arcos e círculos OpenGL que não pode fazer com o íris GL.</span><span class="sxs-lookup"><span data-stu-id="a66c9-126">You can do some things with OpenGL arcs and circles that you can't do with IRIS GL.</span></span> <span data-ttu-id="a66c9-127">O OpenGL chama arcos e círculos, discos e discos parciais, respectivamente.</span><span class="sxs-lookup"><span data-stu-id="a66c9-127">OpenGL calls arcs and circles, disks and partial disks respectively.</span></span>

<span data-ttu-id="a66c9-128">Ao portar arcos e círculos, mantenha os seguintes pontos sobre o OpenGL em mente:</span><span class="sxs-lookup"><span data-stu-id="a66c9-128">When porting arcs and circles, keep the following points about OpenGL in mind:</span></span>

-   <span data-ttu-id="a66c9-129">Os ângulos são medidos em graus e não em décimos de graus.</span><span class="sxs-lookup"><span data-stu-id="a66c9-129">Angles are measured in degrees, and not in tenths of degrees.</span></span>
-   <span data-ttu-id="a66c9-130">O ângulo inicial é medido a partir do eixo y positivo e não do eixo x.</span><span class="sxs-lookup"><span data-stu-id="a66c9-130">The start angle is measured from the positive y-axis, and not from the x-axis.</span></span>
-   <span data-ttu-id="a66c9-131">O ângulo de flecha agora está no sentido horário, em vez de no sentido anti-horário.</span><span class="sxs-lookup"><span data-stu-id="a66c9-131">The sweep angle is now clockwise instead of counterclockwise.</span></span>

<span data-ttu-id="a66c9-132">??</span><span class="sxs-lookup"><span data-stu-id="a66c9-132">??</span></span>

 

 




