---
title: Portando funções do v
description: No íris GL, você usa variações na função v para especificar vértices. A função OpenGL equivalente é glVertex abaixo são exemplos de glVertex.
ms.assetid: b4ac0c41-983a-4387-a69f-530c9094dc33
keywords:
- Portabilidade do íris GL, vértices
- portando do íris GL, vértices
- portando para OpenGL do íris GL, vértices
- Portabilidade OpenGL do íris GL, vértices
- funções de desenho, vértices
- vértices, portando do íris GL
- Portabilidade do íris GL, funções do v
- portando do íris GL, funções do v
- portando para OpenGL do íris GL, funções do v
- Portabilidade OpenGL do íris GL, funções do v
- funções de desenho, funções do v
- funções do v
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfd5e40915f891817606ac8517c0b3b980b436be
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104292044"
---
# <a name="porting-v-functions"></a><span data-ttu-id="9c7c2-116">Portando funções do v</span><span class="sxs-lookup"><span data-stu-id="9c7c2-116">Porting v Functions</span></span>

<span data-ttu-id="9c7c2-117">No íris GL, você usa variações na função **v** para especificar vértices.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-117">In IRIS GL, you use variations on the **v** function to specify vertices.</span></span> <span data-ttu-id="9c7c2-118">A função OpenGL equivalente é [glVertex](glvertex-functions.md): abaixo estão exemplos de **glVertex**.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-118">The equivalent OpenGL function is [glVertex](glvertex-functions.md): Below are examples of **glVertex**.</span></span>

``` syntax
glVertex2[d|f|i|s][v]( x, y ); 
glVertex3[d|f|i|s][v]( x, y, z); 
glVertex4[d|f|i|s][v]( x, y, z, w);
```

<span data-ttu-id="9c7c2-119">A função **glVertex** tem sufixos da mesma maneira que outras chamadas OpenGL.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-119">The **glVertex** function takes suffixes the same way other OpenGL calls do.</span></span> <span data-ttu-id="9c7c2-120">As versões de vetor da chamada assumem matrizes do tamanho adequado como argumentos.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-120">The vector versions of the call take arrays of the proper size as arguments.</span></span> <span data-ttu-id="9c7c2-121">Na versão 2-D, z = 0 e w = 1.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-121">In the 2-D version, z=0 and w=1.</span></span> <span data-ttu-id="9c7c2-122">Na versão 3-D, w = 1.</span><span class="sxs-lookup"><span data-stu-id="9c7c2-122">In the 3-D version, w=1.</span></span>

 

 




