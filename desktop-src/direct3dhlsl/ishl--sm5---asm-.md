---
title: ishl (sm5 – asm)
description: Deslocar para a esquerda. | ishl (SM5-ASM)
ms.assetid: 3EE669BA-252D-4617-85B0-AEBB7F7E4C5E
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 230034e66ca9adfbd6c94cc99351b485c6577fdf
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298274"
---
# <a name="ishl-sm5---asm"></a><span data-ttu-id="cac62-104">ishl (sm5 – asm)</span><span class="sxs-lookup"><span data-stu-id="cac62-104">ishl (sm5 - asm)</span></span>

<span data-ttu-id="cac62-105">Deslocar para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="cac62-105">Shift left.</span></span>



| <span data-ttu-id="cac62-106">ishl dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="cac62-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="cac62-107">Item</span><span class="sxs-lookup"><span data-stu-id="cac62-107">Item</span></span>                                                            | <span data-ttu-id="cac62-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="cac62-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="cac62-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="cac62-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="cac62-110">\[in \] contém os resultados da mudança.</span><span class="sxs-lookup"><span data-stu-id="cac62-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="cac62-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="cac62-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="cac62-112">\[nos \] valores de 32 bits para Shift.</span><span class="sxs-lookup"><span data-stu-id="cac62-112">\[in\] The 32-bit values to shift.</span></span><br/>       |
| <span data-ttu-id="cac62-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="cac62-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="cac62-114">\[no \] número de bits a serem deslocados.</span><span class="sxs-lookup"><span data-stu-id="cac62-114">\[in\] The number of bits to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="cac62-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="cac62-115">Remarks</span></span>

<span data-ttu-id="cac62-116">Essa instrução executa uma mudança de componente de cada valor de 32 bits no *src0* Left por um número de bits de inteiro sem sinal fornecido pelo LSB 5 bits (0-31 intervalo) em *src1*, inserindo 0.</span><span class="sxs-lookup"><span data-stu-id="cac62-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, inserting 0.</span></span> <span data-ttu-id="cac62-117">Os resultados de 32 bits por componente são colocados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="cac62-117">The 32-bit per component results are placed in *dest*.</span></span>

<span data-ttu-id="cac62-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="cac62-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cac62-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="cac62-119">Vertex</span></span> | <span data-ttu-id="cac62-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="cac62-120">Hull</span></span> | <span data-ttu-id="cac62-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="cac62-121">Domain</span></span> | <span data-ttu-id="cac62-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="cac62-122">Geometry</span></span> | <span data-ttu-id="cac62-123">16x16</span><span class="sxs-lookup"><span data-stu-id="cac62-123">Pixel</span></span> | <span data-ttu-id="cac62-124">Computação</span><span class="sxs-lookup"><span data-stu-id="cac62-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="cac62-125">X</span><span class="sxs-lookup"><span data-stu-id="cac62-125">X</span></span>      | <span data-ttu-id="cac62-126">X</span><span class="sxs-lookup"><span data-stu-id="cac62-126">X</span></span>    | <span data-ttu-id="cac62-127">X</span><span class="sxs-lookup"><span data-stu-id="cac62-127">X</span></span>      | <span data-ttu-id="cac62-128">X</span><span class="sxs-lookup"><span data-stu-id="cac62-128">X</span></span>        | <span data-ttu-id="cac62-129">X</span><span class="sxs-lookup"><span data-stu-id="cac62-129">X</span></span>     | <span data-ttu-id="cac62-130">X</span><span class="sxs-lookup"><span data-stu-id="cac62-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cac62-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="cac62-131">Minimum Shader Model</span></span>

<span data-ttu-id="cac62-132">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="cac62-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="cac62-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="cac62-133">Shader Model</span></span>                                              | <span data-ttu-id="cac62-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="cac62-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cac62-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="cac62-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cac62-136">sim</span><span class="sxs-lookup"><span data-stu-id="cac62-136">yes</span></span>       |
| [<span data-ttu-id="cac62-137">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="cac62-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cac62-138">não</span><span class="sxs-lookup"><span data-stu-id="cac62-138">no</span></span>        |
| [<span data-ttu-id="cac62-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="cac62-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cac62-140">não</span><span class="sxs-lookup"><span data-stu-id="cac62-140">no</span></span>        |
| [<span data-ttu-id="cac62-141">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cac62-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cac62-142">não</span><span class="sxs-lookup"><span data-stu-id="cac62-142">no</span></span>        |
| [<span data-ttu-id="cac62-143">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cac62-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cac62-144">não</span><span class="sxs-lookup"><span data-stu-id="cac62-144">no</span></span>        |
| [<span data-ttu-id="cac62-145">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cac62-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cac62-146">não</span><span class="sxs-lookup"><span data-stu-id="cac62-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cac62-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cac62-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cac62-148">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cac62-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





