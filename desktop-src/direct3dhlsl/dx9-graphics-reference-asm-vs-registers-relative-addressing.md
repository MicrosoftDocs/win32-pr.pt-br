---
title: Endereçamento relativo (referência de HLSL VS)
description: Para sombreadores de vértice, a sintaxe \ \ pode ser usada somente em tipos de registro que podem ser relativamente endereçados em determinados modelos de sombreador.
ms.assetid: 9f9d2499-73a5-4c9d-9dce-94c914933334
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 2bbba694878ba84ac3c2fa9c4e8058bb0d91830e
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112406689"
---
# <a name="relative-addressing-hlsl-vs-reference"></a><span data-ttu-id="67fdd-103">Endereçamento relativo (referência de HLSL VS)</span><span class="sxs-lookup"><span data-stu-id="67fdd-103">Relative Addressing (HLSL VS reference)</span></span>

<span data-ttu-id="67fdd-104">A \[ \] sintaxe pode ser usada somente em tipos de registro que podem ser relativamente endereçados em determinados modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="67fdd-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="67fdd-105">As formas de sintaxe com suporte \[ \] são listadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="67fdd-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="67fdd-106">Em que:</span><span class="sxs-lookup"><span data-stu-id="67fdd-106">Where:</span></span>

-   <span data-ttu-id="67fdd-107">"R" denota qualquer tipo de registro que possa ser relativamente endereçado.</span><span class="sxs-lookup"><span data-stu-id="67fdd-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="67fdd-108">"A" denota qualquer registro que possa ser usado como um índice para endereçar relativamente outros registros.</span><span class="sxs-lookup"><span data-stu-id="67fdd-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="67fdd-109">N0-Ni, M0-MJ e k são inteiros >= 0.</span><span class="sxs-lookup"><span data-stu-id="67fdd-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="67fdd-110">\[\]sintaxe do</span><span class="sxs-lookup"><span data-stu-id="67fdd-110">\[ \] syntax</span></span>                              | <span data-ttu-id="67fdd-111">Índice efetivo</span><span class="sxs-lookup"><span data-stu-id="67fdd-111">Effective index</span></span>                       | <span data-ttu-id="67fdd-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="67fdd-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="67fdd-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="67fdd-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="67fdd-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="67fdd-115">c \[ a0 x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="67fdd-116">R \[ k \] (= r)</span><span class="sxs-lookup"><span data-stu-id="67fdd-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="67fdd-117">k</span><span class="sxs-lookup"><span data-stu-id="67fdd-117">k</span></span>                                     | <span data-ttu-id="67fdd-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="67fdd-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="67fdd-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-119">R\[ A \]</span></span>                                  | <span data-ttu-id="67fdd-120">Um</span><span class="sxs-lookup"><span data-stu-id="67fdd-120">A</span></span>                                     | <span data-ttu-id="67fdd-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="67fdd-122">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="67fdd-123">A + k + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="67fdd-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="67fdd-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="67fdd-125">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="67fdd-126">A + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="67fdd-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="67fdd-127">c \[ 2 + 1 + al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="67fdd-128">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="67fdd-129">A + k</span><span class="sxs-lookup"><span data-stu-id="67fdd-129">A + k</span></span>                                 | <span data-ttu-id="67fdd-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="67fdd-131">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="67fdd-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="67fdd-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="67fdd-133">v1 \[ al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="67fdd-134">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="67fdd-135">A + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="67fdd-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="67fdd-136">o \[ 3 + 1 + al \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="67fdd-137">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="67fdd-138">A + k + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="67fdd-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="67fdd-139">O1 \[ 2 + 1 + 3 + Al \]</span><span class="sxs-lookup"><span data-stu-id="67fdd-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="67fdd-140">Os registros estão disponíveis nas seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="67fdd-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="67fdd-141">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="67fdd-141">Register type</span></span> | <span data-ttu-id="67fdd-142">Versões do sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="67fdd-142">Vertex Shader Versions</span></span> |
|---------------|------------------------|
| <span data-ttu-id="67fdd-143">a0</span><span class="sxs-lookup"><span data-stu-id="67fdd-143">a0</span></span>            | <span data-ttu-id="67fdd-144">Tudo</span><span class="sxs-lookup"><span data-stu-id="67fdd-144">All</span></span>                    |
| <span data-ttu-id="67fdd-145">&</span><span class="sxs-lookup"><span data-stu-id="67fdd-145">aL</span></span>            | <span data-ttu-id="67fdd-146">vs \_ 2 \_ 0 e superior</span><span class="sxs-lookup"><span data-stu-id="67fdd-146">vs\_2\_0 and higher</span></span>    |
| <span data-ttu-id="67fdd-147">cn</span><span class="sxs-lookup"><span data-stu-id="67fdd-147">cn</span></span>            | <span data-ttu-id="67fdd-148">vs \_ 1 \_ 1 e superior</span><span class="sxs-lookup"><span data-stu-id="67fdd-148">vs\_1\_1 and higher</span></span>    |
| <span data-ttu-id="67fdd-149">on</span><span class="sxs-lookup"><span data-stu-id="67fdd-149">on</span></span>            | <span data-ttu-id="67fdd-150">vs \_ 3 \_ 0</span><span class="sxs-lookup"><span data-stu-id="67fdd-150">vs\_3\_0</span></span>               |



 

## <a name="related-topics"></a><span data-ttu-id="67fdd-151">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="67fdd-151">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="67fdd-152">Registros de sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="67fdd-152">Vertex Shader Registers</span></span>](dx9-graphics-reference-asm-vs-registers.md)
</dt> </dl>

 

 




