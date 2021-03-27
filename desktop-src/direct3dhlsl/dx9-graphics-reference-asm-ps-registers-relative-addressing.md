---
title: Endereçamento relativo (referência do HLSL PS)
description: A sintaxe \ \ pode ser usada somente em tipos de registro que podem ser relativamente endereçados em determinados modelos de sombreador.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 38c7be68245cfedbb27898e0fbb689e9e43755ca
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "103638911"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="6a4df-103">Endereçamento relativo (referência do HLSL PS)</span><span class="sxs-lookup"><span data-stu-id="6a4df-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="6a4df-104">A \[ \] sintaxe pode ser usada somente em tipos de registro que podem ser relativamente endereçados em determinados modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6a4df-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="6a4df-105">As formas de sintaxe com suporte \[ \] são listadas da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="6a4df-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="6a4df-106">Em que:</span><span class="sxs-lookup"><span data-stu-id="6a4df-106">Where:</span></span>

-   <span data-ttu-id="6a4df-107">"R" denota qualquer tipo de registro que possa ser relativamente endereçado.</span><span class="sxs-lookup"><span data-stu-id="6a4df-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="6a4df-108">"A" denota qualquer registro que possa ser usado como um índice para endereçar relativamente outros registros.</span><span class="sxs-lookup"><span data-stu-id="6a4df-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="6a4df-109">N0-Ni, M0-MJ e k são inteiros >= 0.</span><span class="sxs-lookup"><span data-stu-id="6a4df-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="6a4df-110">\[\]sintaxe do</span><span class="sxs-lookup"><span data-stu-id="6a4df-110">\[ \] syntax</span></span>                              | <span data-ttu-id="6a4df-111">Índice efetivo</span><span class="sxs-lookup"><span data-stu-id="6a4df-111">Effective index</span></span>                       | <span data-ttu-id="6a4df-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="6a4df-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="6a4df-113">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="6a4df-114">A + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="6a4df-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="6a4df-115">c \[ a0 x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="6a4df-116">R \[ k \] (= r)</span><span class="sxs-lookup"><span data-stu-id="6a4df-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="6a4df-117">k</span><span class="sxs-lookup"><span data-stu-id="6a4df-117">k</span></span>                                     | <span data-ttu-id="6a4df-118">c \[ 10 \] (= C10)</span><span class="sxs-lookup"><span data-stu-id="6a4df-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="6a4df-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-119">R\[ A \]</span></span>                                  | <span data-ttu-id="6a4df-120">Um</span><span class="sxs-lookup"><span data-stu-id="6a4df-120">A</span></span>                                     | <span data-ttu-id="6a4df-121">c \[ a0. y \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="6a4df-122">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="6a4df-123">A + k + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="6a4df-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="6a4df-124">C8 \[ 3 + 2 + a0. w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="6a4df-125">R \[ N0 +... + ni + A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="6a4df-126">A + N0 +... + ni + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="6a4df-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="6a4df-127">c \[ 2 + 1 + al + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="6a4df-128">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="6a4df-129">A + k</span><span class="sxs-lookup"><span data-stu-id="6a4df-129">A + k</span></span>                                 | <span data-ttu-id="6a4df-130">C12 \[ Al \] , C0 \[ a0. z \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="6a4df-131">R \[ A + M0 +... + MJ \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="6a4df-132">A + k + M0 +... + MJ</span><span class="sxs-lookup"><span data-stu-id="6a4df-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="6a4df-133">v1 \[ al + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="6a4df-134">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="6a4df-135">A + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="6a4df-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="6a4df-136">o \[ 3 + 1 + al \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="6a4df-137">R \[ N0 +... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="6a4df-138">A + k + N0 +... + ni</span><span class="sxs-lookup"><span data-stu-id="6a4df-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="6a4df-139">O1 \[ 2 + 1 + 3 + Al \]</span><span class="sxs-lookup"><span data-stu-id="6a4df-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="6a4df-140">Os registros estão disponíveis nas seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="6a4df-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="6a4df-141">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="6a4df-141">Register type</span></span>                                                                                   | <span data-ttu-id="6a4df-142">Versões do sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="6a4df-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="6a4df-143">[contador de loop](dx9-graphics-reference-asm-ps-registers-loop-counter.md): Al nos registros de entrada</span><span class="sxs-lookup"><span data-stu-id="6a4df-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="6a4df-144">PS \_ 3 \_ 0 e superior</span><span class="sxs-lookup"><span data-stu-id="6a4df-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="6a4df-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a4df-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a4df-146">Register</span><span class="sxs-lookup"><span data-stu-id="6a4df-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




