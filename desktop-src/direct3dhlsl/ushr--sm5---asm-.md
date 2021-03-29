---
title: ushr (SM5-ASM)
description: Deslocar para a direita. | ushr (SM5-ASM)
ms.assetid: C695CB6C-A6C9-4DC8-8EBE-70A0CFFC4981
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f33c627ec4aa985b5ac8a27cf0babd6219c9247c
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968434"
---
# <a name="ushr-sm5---asm"></a><span data-ttu-id="beb1f-104">ushr (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="beb1f-104">ushr (sm5 - asm)</span></span>

<span data-ttu-id="beb1f-105">Deslocar para a direita.</span><span class="sxs-lookup"><span data-stu-id="beb1f-105">Shift right.</span></span>



| <span data-ttu-id="beb1f-106">ubfe dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="beb1f-106">ubfe dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="beb1f-107">Item</span><span class="sxs-lookup"><span data-stu-id="beb1f-107">Item</span></span>                                                            | <span data-ttu-id="beb1f-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="beb1f-108">Description</span></span>                                                                  |
|-----------------------------------------------------------------|------------------------------------------------------------------------------|
| <span data-ttu-id="beb1f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="beb1f-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="beb1f-110">\[in \] contém os resultados da instrução.</span><span class="sxs-lookup"><span data-stu-id="beb1f-110">\[in\] Contains the results of the instruction.</span></span><br/>                   |
| <span data-ttu-id="beb1f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="beb1f-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="beb1f-112">\[nos \] valores de 32 bits para Shift.</span><span class="sxs-lookup"><span data-stu-id="beb1f-112">\[in\] The 32-bit values to shift.</span></span><br/>                                |
| <span data-ttu-id="beb1f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="beb1f-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="beb1f-114">\[nos \] bits LSB 5, forneça o número de bits a serem deslocados (0-31).</span><span class="sxs-lookup"><span data-stu-id="beb1f-114">\[in\] The LSB 5 bits provide the number of bits to shift (0-31).</span></span><br/> |



 

<span data-ttu-id="beb1f-115">Essa instrução executa uma mudança de componente de cada valor de 32 bits em *src0* à direita por um número de bits de inteiro sem sinal fornecido pelo LSB de 5 bits (0-31 intervalo) em *src1*, inserindo 0.</span><span class="sxs-lookup"><span data-stu-id="beb1f-115">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="beb1f-116">Os resultados de 32 bits por componente são colocados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="beb1f-116">The 32-bit per component results is placed in *dest*.</span></span>

<span data-ttu-id="beb1f-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="beb1f-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="beb1f-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="beb1f-118">Vertex</span></span> | <span data-ttu-id="beb1f-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="beb1f-119">Hull</span></span> | <span data-ttu-id="beb1f-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="beb1f-120">Domain</span></span> | <span data-ttu-id="beb1f-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="beb1f-121">Geometry</span></span> | <span data-ttu-id="beb1f-122">16x16</span><span class="sxs-lookup"><span data-stu-id="beb1f-122">Pixel</span></span> | <span data-ttu-id="beb1f-123">Computação</span><span class="sxs-lookup"><span data-stu-id="beb1f-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="beb1f-124">X</span><span class="sxs-lookup"><span data-stu-id="beb1f-124">X</span></span>      | <span data-ttu-id="beb1f-125">X</span><span class="sxs-lookup"><span data-stu-id="beb1f-125">X</span></span>    | <span data-ttu-id="beb1f-126">X</span><span class="sxs-lookup"><span data-stu-id="beb1f-126">X</span></span>      | <span data-ttu-id="beb1f-127">X</span><span class="sxs-lookup"><span data-stu-id="beb1f-127">X</span></span>        | <span data-ttu-id="beb1f-128">X</span><span class="sxs-lookup"><span data-stu-id="beb1f-128">X</span></span>     | <span data-ttu-id="beb1f-129">X</span><span class="sxs-lookup"><span data-stu-id="beb1f-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="beb1f-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="beb1f-130">Minimum Shader Model</span></span>

<span data-ttu-id="beb1f-131">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="beb1f-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="beb1f-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="beb1f-132">Shader Model</span></span>                                              | <span data-ttu-id="beb1f-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="beb1f-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="beb1f-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="beb1f-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="beb1f-135">sim</span><span class="sxs-lookup"><span data-stu-id="beb1f-135">yes</span></span>       |
| [<span data-ttu-id="beb1f-136">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="beb1f-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="beb1f-137">não</span><span class="sxs-lookup"><span data-stu-id="beb1f-137">no</span></span>        |
| [<span data-ttu-id="beb1f-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="beb1f-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="beb1f-139">não</span><span class="sxs-lookup"><span data-stu-id="beb1f-139">no</span></span>        |
| [<span data-ttu-id="beb1f-140">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="beb1f-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="beb1f-141">não</span><span class="sxs-lookup"><span data-stu-id="beb1f-141">no</span></span>        |
| [<span data-ttu-id="beb1f-142">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="beb1f-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="beb1f-143">não</span><span class="sxs-lookup"><span data-stu-id="beb1f-143">no</span></span>        |
| [<span data-ttu-id="beb1f-144">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="beb1f-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="beb1f-145">não</span><span class="sxs-lookup"><span data-stu-id="beb1f-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="beb1f-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="beb1f-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="beb1f-147">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="beb1f-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





