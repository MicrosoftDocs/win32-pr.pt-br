---
title: Registros-vs_4_1
description: Esta seção contém informações de referência para os registros de entrada e saída implementados pelo vertex shader versão 4 \_ 1.
ms.assetid: ea449195-d012-4a14-9760-b738a8623343
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: df2254c111303129327d255f94727a5e42ac1c0c
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 09/16/2019
ms.locfileid: "104159998"
---
# <a name="registers---vs_4_1"></a><span data-ttu-id="354a5-103">Registros-vs \_ 4 \_ 1</span><span class="sxs-lookup"><span data-stu-id="354a5-103">Registers - vs\_4\_1</span></span>

<span data-ttu-id="354a5-104">Esta seção contém informações de referência para os registros de entrada e saída implementados pelo vertex shader versão 4 \_ 1.</span><span class="sxs-lookup"><span data-stu-id="354a5-104">This section contains reference information for the input and output registers implemented by vertex shader version 4\_1.</span></span>

## <a name="input-registers"></a><span data-ttu-id="354a5-105">Registros de entrada</span><span class="sxs-lookup"><span data-stu-id="354a5-105">Input Registers</span></span>



| <span data-ttu-id="354a5-106">Registre-se</span><span class="sxs-lookup"><span data-stu-id="354a5-106">Register</span></span>      | <span data-ttu-id="354a5-107">Name</span><span class="sxs-lookup"><span data-stu-id="354a5-107">Name</span></span> | <span data-ttu-id="354a5-108">Contagem</span><span class="sxs-lookup"><span data-stu-id="354a5-108">Count</span></span>              | <span data-ttu-id="354a5-109">R/W</span><span class="sxs-lookup"><span data-stu-id="354a5-109">R/W</span></span> | <span data-ttu-id="354a5-110">Dimensão</span><span class="sxs-lookup"><span data-stu-id="354a5-110">Dimension</span></span> | <span data-ttu-id="354a5-111">Indexável por r\#</span><span class="sxs-lookup"><span data-stu-id="354a5-111">Indexable by r\#</span></span> | <span data-ttu-id="354a5-112">Padrões</span><span class="sxs-lookup"><span data-stu-id="354a5-112">Defaults</span></span> | <span data-ttu-id="354a5-113">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="354a5-113">Requires DCL</span></span> |
|---------------|------|--------------------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="354a5-114">d\#</span><span class="sxs-lookup"><span data-stu-id="354a5-114">r\#</span></span>           |      | <span data-ttu-id="354a5-115">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="354a5-115">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="354a5-116">R/W</span><span class="sxs-lookup"><span data-stu-id="354a5-116">R/W</span></span> | <span data-ttu-id="354a5-117">4</span><span class="sxs-lookup"><span data-stu-id="354a5-117">4</span></span>         | <span data-ttu-id="354a5-118">Não</span><span class="sxs-lookup"><span data-stu-id="354a5-118">No</span></span>               | <span data-ttu-id="354a5-119">Nenhum</span><span class="sxs-lookup"><span data-stu-id="354a5-119">None</span></span>     | <span data-ttu-id="354a5-120">Yes</span><span class="sxs-lookup"><span data-stu-id="354a5-120">Yes</span></span>          |
| <span data-ttu-id="354a5-121">x \# \[ n\]</span><span class="sxs-lookup"><span data-stu-id="354a5-121">x\#\[n\]</span></span>      |      | <span data-ttu-id="354a5-122">4096 (r \# + x \# \[ n \] )</span><span class="sxs-lookup"><span data-stu-id="354a5-122">4096(r\#+x\#\[n\])</span></span> | <span data-ttu-id="354a5-123">R/W</span><span class="sxs-lookup"><span data-stu-id="354a5-123">R/W</span></span> | <span data-ttu-id="354a5-124">4</span><span class="sxs-lookup"><span data-stu-id="354a5-124">4</span></span>         | <span data-ttu-id="354a5-125">Sim</span><span class="sxs-lookup"><span data-stu-id="354a5-125">Yes</span></span>              | <span data-ttu-id="354a5-126">Nenhum</span><span class="sxs-lookup"><span data-stu-id="354a5-126">None</span></span>     | <span data-ttu-id="354a5-127">Yes</span><span class="sxs-lookup"><span data-stu-id="354a5-127">Yes</span></span>          |
| <span data-ttu-id="354a5-128">l\#</span><span class="sxs-lookup"><span data-stu-id="354a5-128">v\#</span></span>           |      | <span data-ttu-id="354a5-129">32</span><span class="sxs-lookup"><span data-stu-id="354a5-129">32</span></span>                 | <span data-ttu-id="354a5-130">R</span><span class="sxs-lookup"><span data-stu-id="354a5-130">R</span></span>   | <span data-ttu-id="354a5-131">4</span><span class="sxs-lookup"><span data-stu-id="354a5-131">4</span></span>         | <span data-ttu-id="354a5-132">Sim</span><span class="sxs-lookup"><span data-stu-id="354a5-132">Yes</span></span>              | <span data-ttu-id="354a5-133">Nenhum</span><span class="sxs-lookup"><span data-stu-id="354a5-133">None</span></span>     | <span data-ttu-id="354a5-134">Yes</span><span class="sxs-lookup"><span data-stu-id="354a5-134">Yes</span></span>          |
| <span data-ttu-id="354a5-135">t\#</span><span class="sxs-lookup"><span data-stu-id="354a5-135">t\#</span></span>           |      | <span data-ttu-id="354a5-136">128</span><span class="sxs-lookup"><span data-stu-id="354a5-136">128</span></span>                | <span data-ttu-id="354a5-137">R</span><span class="sxs-lookup"><span data-stu-id="354a5-137">R</span></span>   | <span data-ttu-id="354a5-138">1</span><span class="sxs-lookup"><span data-stu-id="354a5-138">1</span></span>         | <span data-ttu-id="354a5-139">Não</span><span class="sxs-lookup"><span data-stu-id="354a5-139">No</span></span>               | <span data-ttu-id="354a5-140">Nenhum</span><span class="sxs-lookup"><span data-stu-id="354a5-140">None</span></span>     | <span data-ttu-id="354a5-141">Yes</span><span class="sxs-lookup"><span data-stu-id="354a5-141">Yes</span></span>          |
| <span data-ttu-id="354a5-142">s\#</span><span class="sxs-lookup"><span data-stu-id="354a5-142">s\#</span></span>           |      | <span data-ttu-id="354a5-143">16</span><span class="sxs-lookup"><span data-stu-id="354a5-143">16</span></span>                 | <span data-ttu-id="354a5-144">R</span><span class="sxs-lookup"><span data-stu-id="354a5-144">R</span></span>   | <span data-ttu-id="354a5-145">1</span><span class="sxs-lookup"><span data-stu-id="354a5-145">1</span></span>         | <span data-ttu-id="354a5-146">Não</span><span class="sxs-lookup"><span data-stu-id="354a5-146">No</span></span>               | <span data-ttu-id="354a5-147">Nenhum</span><span class="sxs-lookup"><span data-stu-id="354a5-147">None</span></span>     | <span data-ttu-id="354a5-148">Yes</span><span class="sxs-lookup"><span data-stu-id="354a5-148">Yes</span></span>          |
| <span data-ttu-id="354a5-149">\# \[ índice CB\]</span><span class="sxs-lookup"><span data-stu-id="354a5-149">cb\#\[index\]</span></span> |      | <span data-ttu-id="354a5-150">15</span><span class="sxs-lookup"><span data-stu-id="354a5-150">15</span></span>                 | <span data-ttu-id="354a5-151">R</span><span class="sxs-lookup"><span data-stu-id="354a5-151">R</span></span>   | <span data-ttu-id="354a5-152">4</span><span class="sxs-lookup"><span data-stu-id="354a5-152">4</span></span>         | <span data-ttu-id="354a5-153">Sim (conteúdo)</span><span class="sxs-lookup"><span data-stu-id="354a5-153">Yes(Contents)</span></span>    | <span data-ttu-id="354a5-154">Nenhum</span><span class="sxs-lookup"><span data-stu-id="354a5-154">None</span></span>     | <span data-ttu-id="354a5-155">Yes</span><span class="sxs-lookup"><span data-stu-id="354a5-155">Yes</span></span>          |
| <span data-ttu-id="354a5-156">índice de ICB \[\]</span><span class="sxs-lookup"><span data-stu-id="354a5-156">icb\[index\]</span></span>  |      | <span data-ttu-id="354a5-157">1</span><span class="sxs-lookup"><span data-stu-id="354a5-157">1</span></span>                  | <span data-ttu-id="354a5-158">R</span><span class="sxs-lookup"><span data-stu-id="354a5-158">R</span></span>   | <span data-ttu-id="354a5-159">4</span><span class="sxs-lookup"><span data-stu-id="354a5-159">4</span></span>         | <span data-ttu-id="354a5-160">Sim (conteúdo)</span><span class="sxs-lookup"><span data-stu-id="354a5-160">Yes(Contents)</span></span>    | <span data-ttu-id="354a5-161">Nenhum</span><span class="sxs-lookup"><span data-stu-id="354a5-161">None</span></span>     | <span data-ttu-id="354a5-162">Yes</span><span class="sxs-lookup"><span data-stu-id="354a5-162">Yes</span></span>          |



 

## <a name="output-registers"></a><span data-ttu-id="354a5-163">Registros de saída</span><span class="sxs-lookup"><span data-stu-id="354a5-163">Output Registers</span></span>



| <span data-ttu-id="354a5-164">Registre-se</span><span class="sxs-lookup"><span data-stu-id="354a5-164">Register</span></span> | <span data-ttu-id="354a5-165">Name</span><span class="sxs-lookup"><span data-stu-id="354a5-165">Name</span></span>            | <span data-ttu-id="354a5-166">Contagem</span><span class="sxs-lookup"><span data-stu-id="354a5-166">Count</span></span> | <span data-ttu-id="354a5-167">R/W</span><span class="sxs-lookup"><span data-stu-id="354a5-167">R/W</span></span> | <span data-ttu-id="354a5-168">Dimensão</span><span class="sxs-lookup"><span data-stu-id="354a5-168">Dimension</span></span> | <span data-ttu-id="354a5-169">Indexável por r\#</span><span class="sxs-lookup"><span data-stu-id="354a5-169">Indexable by r\#</span></span> | <span data-ttu-id="354a5-170">Padrões</span><span class="sxs-lookup"><span data-stu-id="354a5-170">Defaults</span></span> | <span data-ttu-id="354a5-171">Requer DCL</span><span class="sxs-lookup"><span data-stu-id="354a5-171">Requires DCL</span></span> |
|----------|-----------------|-------|-----|-----------|------------------|----------|--------------|
| <span data-ttu-id="354a5-172">NULO</span><span class="sxs-lookup"><span data-stu-id="354a5-172">NULL</span></span>     | <span data-ttu-id="354a5-173">Descartar resultado</span><span class="sxs-lookup"><span data-stu-id="354a5-173">Discard Result</span></span>  | <span data-ttu-id="354a5-174">N/D</span><span class="sxs-lookup"><span data-stu-id="354a5-174">N/A</span></span>   | <span data-ttu-id="354a5-175">W</span><span class="sxs-lookup"><span data-stu-id="354a5-175">W</span></span>   | <span data-ttu-id="354a5-176">N/D</span><span class="sxs-lookup"><span data-stu-id="354a5-176">N/A</span></span>       | <span data-ttu-id="354a5-177">N/D</span><span class="sxs-lookup"><span data-stu-id="354a5-177">N/A</span></span>              | <span data-ttu-id="354a5-178">N/D</span><span class="sxs-lookup"><span data-stu-id="354a5-178">N/A</span></span>      | <span data-ttu-id="354a5-179">Não</span><span class="sxs-lookup"><span data-stu-id="354a5-179">No</span></span>           |
| <span data-ttu-id="354a5-180">minúscula\#</span><span class="sxs-lookup"><span data-stu-id="354a5-180">o\#</span></span>      | <span data-ttu-id="354a5-181">Registro de saída</span><span class="sxs-lookup"><span data-stu-id="354a5-181">Output Register</span></span> | <span data-ttu-id="354a5-182">32</span><span class="sxs-lookup"><span data-stu-id="354a5-182">32</span></span>    | <span data-ttu-id="354a5-183">W</span><span class="sxs-lookup"><span data-stu-id="354a5-183">W</span></span>   | <span data-ttu-id="354a5-184">N/D</span><span class="sxs-lookup"><span data-stu-id="354a5-184">N/A</span></span>       | <span data-ttu-id="354a5-185">N/D</span><span class="sxs-lookup"><span data-stu-id="354a5-185">N/A</span></span>              | <span data-ttu-id="354a5-186">4</span><span class="sxs-lookup"><span data-stu-id="354a5-186">4</span></span>        | <span data-ttu-id="354a5-187">Sim</span><span class="sxs-lookup"><span data-stu-id="354a5-187">Yes</span></span>          |



 

## <a name="related-topics"></a><span data-ttu-id="354a5-188">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="354a5-188">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="354a5-189">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="354a5-189">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)
</dt> </dl>

 

 




