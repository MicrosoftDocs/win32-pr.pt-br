---
title: Funções de portabilidade que obtêm matrizes e transformações
description: A tabela a seguir lista as funções da íris GL que obtêm o estado de matrizes e transformações e seus equivalentes em OpenGL.
ms.assetid: 53546bc0-ce1d-47e0-ab5e-5d6789c6db2a
keywords:
- Portabilidade do íris GL, matrizes
- portando do íris GL, matrizes
- portando para OpenGL do íris GL, matrizes
- Portabilidade OpenGL do íris GL, matrizes
- matrizes
- Portabilidade do íris GL, transformações
- portando do íris GL, transformações
- portando para OpenGL do íris GL, transformações
- Portabilidade do OpenGL do íris GL, transformações
- transformações
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93b32ab017e81c9875666785786b29d9c94c7fd1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "103916378"
---
# <a name="porting-functions-that-get-matrices-and-transformations"></a><span data-ttu-id="d7307-113">Funções de portabilidade que obtêm matrizes e transformações</span><span class="sxs-lookup"><span data-stu-id="d7307-113">Porting Functions that Get Matrices and Transformations</span></span>

<span data-ttu-id="d7307-114">A tabela a seguir lista as funções da íris GL que obtêm o estado de matrizes e transformações e seus equivalentes em OpenGL.</span><span class="sxs-lookup"><span data-stu-id="d7307-114">The following table lists the IRIS GL functions that get the state of matrices and transformations and their OpenGL equivalents.</span></span>



| <span data-ttu-id="d7307-115">Consulta de matriz do íris GL</span><span class="sxs-lookup"><span data-stu-id="d7307-115">IRIS GL matrix query</span></span>                  | <span data-ttu-id="d7307-116">Consulta de matriz de glGet OpenGL</span><span class="sxs-lookup"><span data-stu-id="d7307-116">OpenGL glGet matrix query</span></span>         | <span data-ttu-id="d7307-117">Significado</span><span class="sxs-lookup"><span data-stu-id="d7307-117">Meaning</span></span>                                                         |
|---------------------------------------|-----------------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="d7307-118">**getmmode**</span><span class="sxs-lookup"><span data-stu-id="d7307-118">**getmmode**</span></span>                          | <span data-ttu-id="d7307-119">\_modo de matriz GL \_</span><span class="sxs-lookup"><span data-stu-id="d7307-119">GL\_MATRIX\_MODE</span></span>                  | <span data-ttu-id="d7307-120">Retorna o modo de matriz atual.</span><span class="sxs-lookup"><span data-stu-id="d7307-120">Returns the current matrix mode.</span></span>                                |
| <span data-ttu-id="d7307-121">**getmatrix** no modo de **MVIEWING**</span><span class="sxs-lookup"><span data-stu-id="d7307-121">**getmatrix** in **MVIEWING** mode</span></span>    | <span data-ttu-id="d7307-122">\_MODELVIEW \_ matriz GL</span><span class="sxs-lookup"><span data-stu-id="d7307-122">GL\_MODELVIEW\_MATRIX</span></span>             | <span data-ttu-id="d7307-123">Retorna uma cópia da matriz de exibição de modelo atual.</span><span class="sxs-lookup"><span data-stu-id="d7307-123">Returns a copy of the current model-view matrix.</span></span>                |
| <span data-ttu-id="d7307-124">**getmatrix** no modo de **MPROJECTION**</span><span class="sxs-lookup"><span data-stu-id="d7307-124">**getmatrix** in **MPROJECTION** mode</span></span> | <span data-ttu-id="d7307-125">\_matriz de projeção GL \_</span><span class="sxs-lookup"><span data-stu-id="d7307-125">GL\_PROJECTION\_MATRIX</span></span>            | <span data-ttu-id="d7307-126">Retorna uma cópia da matriz de projeção atual.</span><span class="sxs-lookup"><span data-stu-id="d7307-126">Returns a copy of the current projection matrix.</span></span>                |
| <span data-ttu-id="d7307-127">**getmatrix** no modo de **MTEXTURE**</span><span class="sxs-lookup"><span data-stu-id="d7307-127">**getmatrix** in **MTEXTURE** mode</span></span>    | <span data-ttu-id="d7307-128">\_matriz de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="d7307-128">GL\_TEXTURE\_MATRIX</span></span>               | <span data-ttu-id="d7307-129">Retorna uma cópia da matriz de textura atual.</span><span class="sxs-lookup"><span data-stu-id="d7307-129">Returns a copy of the current texture matrix.</span></span>                   |
| <span data-ttu-id="d7307-130">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d7307-130">Not applicable.</span></span>                       | <span data-ttu-id="d7307-131">\_profundidade máxima \_ de \_ pilha de MODELVIEW \_ GL</span><span class="sxs-lookup"><span data-stu-id="d7307-131">GL\_MAX\_MODELVIEW\_STACK\_DEPTH</span></span>  | <span data-ttu-id="d7307-132">Retorna a profundidade máxima com suporte da pilha de matriz de exibição de modelo.</span><span class="sxs-lookup"><span data-stu-id="d7307-132">Returns maximum supported depth of the model-view matrix stack.</span></span> |
| <span data-ttu-id="d7307-133">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d7307-133">Not applicable.</span></span>                       | <span data-ttu-id="d7307-134">\_profundidade máxima \_ da \_ pilha de projeção GL \_</span><span class="sxs-lookup"><span data-stu-id="d7307-134">GL\_MAX\_PROJECTION\_STACK\_DEPTH</span></span> | <span data-ttu-id="d7307-135">Retorna a profundidade máxima com suporte da pilha da matriz de projeção.</span><span class="sxs-lookup"><span data-stu-id="d7307-135">Returns maximum supported depth of the projection matrix stack.</span></span> |
| <span data-ttu-id="d7307-136">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d7307-136">Not applicable.</span></span>                       | <span data-ttu-id="d7307-137">\_profundidade máxima \_ da \_ pilha de textura \_ GL</span><span class="sxs-lookup"><span data-stu-id="d7307-137">GL\_MAX\_TEXTURE\_STACK\_DEPTH</span></span>    | <span data-ttu-id="d7307-138">Retorna a profundidade máxima com suporte da pilha de matriz de textura.</span><span class="sxs-lookup"><span data-stu-id="d7307-138">Returns maximum supported depth of the texture matrix stack.</span></span>    |
| <span data-ttu-id="d7307-139">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d7307-139">Not applicable.</span></span>                       | <span data-ttu-id="d7307-140">\_profundidade de \_ pilha \_ MODELVIEW GL</span><span class="sxs-lookup"><span data-stu-id="d7307-140">GL\_MODELVIEW\_STACK\_DEPTH</span></span>       | <span data-ttu-id="d7307-141">Retorna o número de matrizes na pilha de exibição do modelo.</span><span class="sxs-lookup"><span data-stu-id="d7307-141">Returns number of matrices on the model view stack.</span></span>             |
| <span data-ttu-id="d7307-142">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d7307-142">Not applicable.</span></span>                       | <span data-ttu-id="d7307-143">\_profundidade da pilha de projeção GL \_ \_</span><span class="sxs-lookup"><span data-stu-id="d7307-143">GL\_PROJECTION\_STACK\_DEPTH</span></span>      | <span data-ttu-id="d7307-144">Retorna o número de matrizes na pilha de projeção.</span><span class="sxs-lookup"><span data-stu-id="d7307-144">Returns number of matrices on the projection stack.</span></span>             |
| <span data-ttu-id="d7307-145">Não aplicável.</span><span class="sxs-lookup"><span data-stu-id="d7307-145">Not applicable.</span></span>                       | <span data-ttu-id="d7307-146">\_profundidade da \_ pilha de textura GL \_</span><span class="sxs-lookup"><span data-stu-id="d7307-146">GL\_TEXTURE\_STACK\_DEPTH</span></span>         | <span data-ttu-id="d7307-147">Retorna o número de matrizes na pilha de textura.</span><span class="sxs-lookup"><span data-stu-id="d7307-147">Returns number of matrices on the texture stack.</span></span>                |



 

<span data-ttu-id="d7307-148">??</span><span class="sxs-lookup"><span data-stu-id="d7307-148">??</span></span>

 

 




