---
title: Endereçamento relativo (referência de PS HLSL)
description: Para sombreadores de pixel, a sintaxe \ pode ser usada somente em tipos de registro que podem ser relativamente abordados em determinados modelos de sombreador.
ms.assetid: 37e2bab9-f6fe-438a-8a2d-c963634ef8c3
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 8bdafe23696c460da75d87cf1f6d5a968c89ed28
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 06/19/2021
ms.locfileid: "112405479"
---
# <a name="relative-addressing-hlsl-ps-reference"></a><span data-ttu-id="40a7e-103">Endereçamento relativo (referência de PS HLSL)</span><span class="sxs-lookup"><span data-stu-id="40a7e-103">Relative addressing (HLSL PS reference)</span></span>

<span data-ttu-id="40a7e-104">A sintaxe pode ser usada somente em tipos de registro que podem ser relativamente abordados \[ \] em determinados modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="40a7e-104">The \[ \] syntax can be used only in register types that can be relatively addressed in certain shader models.</span></span> <span data-ttu-id="40a7e-105">As formas de sintaxe com \[ \] suporte são listadas da seguinte forma:</span><span class="sxs-lookup"><span data-stu-id="40a7e-105">The supported forms of \[ \] syntax are listed as follows:</span></span>

<span data-ttu-id="40a7e-106">Em que:</span><span class="sxs-lookup"><span data-stu-id="40a7e-106">Where:</span></span>

-   <span data-ttu-id="40a7e-107">"R" indica qualquer tipo de registro que possa ser relativamente resolvido.</span><span class="sxs-lookup"><span data-stu-id="40a7e-107">"R" denotes any register type that can be relatively addressed.</span></span>
-   <span data-ttu-id="40a7e-108">"A" indica qualquer registro que possa ser usado como um índice para resolver relativamente outros registros.</span><span class="sxs-lookup"><span data-stu-id="40a7e-108">"A" denotes any register that can be used as an index to relatively address other registers.</span></span>
-   <span data-ttu-id="40a7e-109">n0 - ni, m0 - mj e k são inteiros >= 0.</span><span class="sxs-lookup"><span data-stu-id="40a7e-109">n0 - ni, m0 - mj, and k are integers >= 0.</span></span>



| <span data-ttu-id="40a7e-110">\[\]sintaxe</span><span class="sxs-lookup"><span data-stu-id="40a7e-110">\[ \] syntax</span></span>                              | <span data-ttu-id="40a7e-111">Índice efetivo</span><span class="sxs-lookup"><span data-stu-id="40a7e-111">Effective index</span></span>                       | <span data-ttu-id="40a7e-112">Exemplos</span><span class="sxs-lookup"><span data-stu-id="40a7e-112">Examples</span></span>                         |
|-------------------------------------------|---------------------------------------|----------------------------------|
| <span data-ttu-id="40a7e-113">R \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-113">R\[ A + m0 + ... + mj \]</span></span>                  | <span data-ttu-id="40a7e-114">A + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="40a7e-114">A + m0 + ... + mj</span></span>                     | <span data-ttu-id="40a7e-115">c \[ a0.x + 3 + 7 \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-115">c\[ a0.x + 3 + 7 \]</span></span>              |
| <span data-ttu-id="40a7e-116">R \[ k ( = \] Rk )</span><span class="sxs-lookup"><span data-stu-id="40a7e-116">R\[ k \] ( = Rk )</span></span>                         | <span data-ttu-id="40a7e-117">k</span><span class="sxs-lookup"><span data-stu-id="40a7e-117">k</span></span>                                     | <span data-ttu-id="40a7e-118">c \[ 10 \] ( = c10 )</span><span class="sxs-lookup"><span data-stu-id="40a7e-118">c\[ 10 \] ( = c10 )</span></span>              |
| <span data-ttu-id="40a7e-119">R \[ A \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-119">R\[ A \]</span></span>                                  | <span data-ttu-id="40a7e-120">Um</span><span class="sxs-lookup"><span data-stu-id="40a7e-120">A</span></span>                                     | <span data-ttu-id="40a7e-121">c \[ a0.y \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-121">c\[ a0.y \]</span></span>                      |
| <span data-ttu-id="40a7e-122">Rk \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-122">Rk\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span> | <span data-ttu-id="40a7e-123">A + k + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="40a7e-123">A + k + n0 + ... + ni + m0 + ... + mj</span></span> | <span data-ttu-id="40a7e-124">c8 \[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-124">c8\[ 3 + 2 + a0.w + 5 + 6 + 1 \]</span></span> |
| <span data-ttu-id="40a7e-125">R \[ n0 + ... + ni + A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-125">R\[ n0 + ... + ni + A + m0 + ... + mj \]</span></span>  | <span data-ttu-id="40a7e-126">A + n0 + ... + ni + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="40a7e-126">A + n0 + ... + ni + m0 + ... + mj</span></span>     | <span data-ttu-id="40a7e-127">c \[ 2 + 1 + aL + 3 + 4 + 5 \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-127">c\[ 2 + 1 + aL + 3 + 4 + 5 \]</span></span>    |
| <span data-ttu-id="40a7e-128">Rk \[ A \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-128">Rk\[ A \]</span></span>                                 | <span data-ttu-id="40a7e-129">A + k</span><span class="sxs-lookup"><span data-stu-id="40a7e-129">A + k</span></span>                                 | <span data-ttu-id="40a7e-130">c12 \[ aL \] , c0 \[ a0.z \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-130">c12\[ aL \], c0\[ a0.z \]</span></span>        |
| <span data-ttu-id="40a7e-131">Rk \[ A + m0 + ... + mj \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-131">Rk\[ A + m0 + ... + mj \]</span></span>                 | <span data-ttu-id="40a7e-132">A + k + m0 + ... + mj</span><span class="sxs-lookup"><span data-stu-id="40a7e-132">A + k + m0 + ... + mj</span></span>                 | <span data-ttu-id="40a7e-133">v1 \[ aL + 4 + 8 \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-133">v1\[ aL + 4 + 8 \]</span></span>               |
| <span data-ttu-id="40a7e-134">R \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-134">R\[ n0 + ... + ni + A \]</span></span>                  | <span data-ttu-id="40a7e-135">A + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="40a7e-135">A + n0 + ... + ni</span></span>                     | <span data-ttu-id="40a7e-136">o \[ 3 + 1 + aL \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-136">o\[ 3 + 1 + aL \]</span></span>                |
| <span data-ttu-id="40a7e-137">Rk \[ n0 + ... + ni + A \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-137">Rk\[ n0 + ... + ni + A \]</span></span>                 | <span data-ttu-id="40a7e-138">A + k + n0 + ... + ni</span><span class="sxs-lookup"><span data-stu-id="40a7e-138">A + k + n0 + ... + ni</span></span>                 | <span data-ttu-id="40a7e-139">o1 \[ 2 + 1 + 3 + aL \]</span><span class="sxs-lookup"><span data-stu-id="40a7e-139">o1\[ 2 + 1 + 3 + aL \]</span></span>           |



 

<span data-ttu-id="40a7e-140">Os registros estão disponíveis nas seguintes versões:</span><span class="sxs-lookup"><span data-stu-id="40a7e-140">The registers are available in the following versions:</span></span>



| <span data-ttu-id="40a7e-141">Tipo de registro</span><span class="sxs-lookup"><span data-stu-id="40a7e-141">Register type</span></span>                                                                                   | <span data-ttu-id="40a7e-142">Versões do Sombreador de Pixel</span><span class="sxs-lookup"><span data-stu-id="40a7e-142">Pixel Shader Versions</span></span> |
|-------------------------------------------------------------------------------------------------|-----------------------|
| <span data-ttu-id="40a7e-143">[contador de loop:](dx9-graphics-reference-asm-ps-registers-loop-counter.md)aL em registros de entrada</span><span class="sxs-lookup"><span data-stu-id="40a7e-143">[loop counter](dx9-graphics-reference-asm-ps-registers-loop-counter.md): aL on input registers</span></span> | <span data-ttu-id="40a7e-144">ps \_ 3 \_ 0 e superior</span><span class="sxs-lookup"><span data-stu-id="40a7e-144">ps\_3\_0 and higher</span></span>   |



 

## <a name="related-topics"></a><span data-ttu-id="40a7e-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="40a7e-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="40a7e-146">Registros</span><span class="sxs-lookup"><span data-stu-id="40a7e-146">Registers</span></span>](dx9-graphics-reference-asm-ps-registers.md)
</dt> </dl>

 

 




