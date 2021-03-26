---
title: dcl_tgsm_structured (SM5-ASM)
description: Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação. A memória é exibida como uma matriz de estruturas.
ms.assetid: C42CD506-58EB-4740-8403-3F9BF29F0CAE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a639d31c4449a0dfeb152c06b35cfb86c5cc30a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988573"
---
# <a name="dcl_tgsm_structured-sm5---asm"></a><span data-ttu-id="47787-104">DCL \_ tgsm \_ estruturado (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="47787-104">dcl\_tgsm\_structured (sm5 - asm)</span></span>

<span data-ttu-id="47787-105">Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="47787-105">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span> <span data-ttu-id="47787-106">A memória é exibida como uma matriz de estruturas.</span><span class="sxs-lookup"><span data-stu-id="47787-106">The memory is viewed as an array of structures.</span></span>



| <span data-ttu-id="47787-107">DCL \_ tgsm \_ estruturado g \# , structByteStride, structCount</span><span class="sxs-lookup"><span data-stu-id="47787-107">dcl\_tgsm\_structured g\#, structByteStride, structCount</span></span> |
|----------------------------------------------------------|



 



| <span data-ttu-id="47787-108">Item</span><span class="sxs-lookup"><span data-stu-id="47787-108">Item</span></span>                                                                                                                                   | <span data-ttu-id="47787-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="47787-109">Description</span></span>                                                                                                   |
|----------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47787-110"><span id="g_"></span><span id="G_"></span>*m\#*</span><span class="sxs-lookup"><span data-stu-id="47787-110"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                                             | <span data-ttu-id="47787-111">\[em \] uma referência a um bloco de memória compartilhada de tamanho *structByteStride* \* *structCount* bytes.</span><span class="sxs-lookup"><span data-stu-id="47787-111">\[in\] A reference to a block of shared memory of size *structByteStride* \* *structCount* bytes.</span></span> <br/> |
| <span data-ttu-id="47787-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span><span class="sxs-lookup"><span data-stu-id="47787-112"><span id="structByteStride"></span><span id="structbytestride"></span><span id="STRUCTBYTESTRIDE"></span>*structByteStride*</span></span><br/> | <span data-ttu-id="47787-113">\[no \] Stride da estrutura.</span><span class="sxs-lookup"><span data-stu-id="47787-113">\[in\] The structure stride.</span></span> <span data-ttu-id="47787-114">Esse valor é um UINT em bytes e deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="47787-114">This value is a uint in bytes and must be a multiple of 4.</span></span> <br/>           |
| <span data-ttu-id="47787-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span><span class="sxs-lookup"><span data-stu-id="47787-115"><span id="structCount"></span><span id="structcount"></span><span id="STRUCTCOUNT"></span>*structCount*</span></span><br/>                     | <span data-ttu-id="47787-116">\[no \] número de estruturas.</span><span class="sxs-lookup"><span data-stu-id="47787-116">\[in\] The number of structures.</span></span><br/>                                                                   |



 

## <a name="remarks"></a><span data-ttu-id="47787-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="47787-117">Remarks</span></span>

<span data-ttu-id="47787-118">O armazenamento total para todos os g \# deve ser <= a quantidade de memória compartilhada disponível por grupo de threads, que é 32 KB ou escalares de 8192 32 bits.</span><span class="sxs-lookup"><span data-stu-id="47787-118">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB, or 8192 32-bit scalars.</span></span>

<span data-ttu-id="47787-119">Em um caso extremo, você pode declarar o total de 8192 g \# s, se cada um tiver um *structByteStride* de 4 e um *structCount* de 1.</span><span class="sxs-lookup"><span data-stu-id="47787-119">In an extreme case, you can declare 8192 total g\# s, if each has a *structByteStride* of 4 and a *structCount* of 1.</span></span>

<span data-ttu-id="47787-120">No lado oposto, você pode declarar um g único \# com um stride de estrutura de 32 KB e uma contagem de estrutura de 1.</span><span class="sxs-lookup"><span data-stu-id="47787-120">In the opposite extreme, you can declare a single g\# with a structure stride of 32kB and a structure count of 1.</span></span>

<span data-ttu-id="47787-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="47787-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="47787-122">Vértice</span><span class="sxs-lookup"><span data-stu-id="47787-122">Vertex</span></span> | <span data-ttu-id="47787-123">Envoltória</span><span class="sxs-lookup"><span data-stu-id="47787-123">Hull</span></span> | <span data-ttu-id="47787-124">Domínio</span><span class="sxs-lookup"><span data-stu-id="47787-124">Domain</span></span> | <span data-ttu-id="47787-125">Geometria</span><span class="sxs-lookup"><span data-stu-id="47787-125">Geometry</span></span> | <span data-ttu-id="47787-126">16x16</span><span class="sxs-lookup"><span data-stu-id="47787-126">Pixel</span></span> | <span data-ttu-id="47787-127">Computação</span><span class="sxs-lookup"><span data-stu-id="47787-127">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="47787-128">X</span><span class="sxs-lookup"><span data-stu-id="47787-128">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="47787-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="47787-129">Minimum Shader Model</span></span>

<span data-ttu-id="47787-130">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="47787-130">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="47787-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="47787-131">Shader Model</span></span>                                              | <span data-ttu-id="47787-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="47787-132">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="47787-133">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="47787-133">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="47787-134">sim</span><span class="sxs-lookup"><span data-stu-id="47787-134">yes</span></span>       |
| [<span data-ttu-id="47787-135">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="47787-135">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="47787-136">não</span><span class="sxs-lookup"><span data-stu-id="47787-136">no</span></span>        |
| [<span data-ttu-id="47787-137">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="47787-137">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="47787-138">não</span><span class="sxs-lookup"><span data-stu-id="47787-138">no</span></span>        |
| [<span data-ttu-id="47787-139">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47787-139">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="47787-140">não</span><span class="sxs-lookup"><span data-stu-id="47787-140">no</span></span>        |
| [<span data-ttu-id="47787-141">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47787-141">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="47787-142">não</span><span class="sxs-lookup"><span data-stu-id="47787-142">no</span></span>        |
| [<span data-ttu-id="47787-143">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47787-143">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="47787-144">não</span><span class="sxs-lookup"><span data-stu-id="47787-144">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="47787-145">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="47787-145">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47787-146">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="47787-146">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





