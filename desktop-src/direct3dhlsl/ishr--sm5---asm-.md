---
title: ISHR (SM5-ASM)
description: Deslocamento aritmético à direita (extensão de assinatura). | ISHR (SM5-ASM)
ms.assetid: 8124B6C3-4576-4616-85A9-A2DD19EB6BB9
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 06df958b2e5c6e9cdd2a4dfb3d35c8112453ce9f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989247"
---
# <a name="ishr-sm5---asm"></a><span data-ttu-id="0fd0e-104">ISHR (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="0fd0e-104">ishr (sm5 - asm)</span></span>

<span data-ttu-id="0fd0e-105">Deslocamento aritmético à direita (extensão de assinatura).</span><span class="sxs-lookup"><span data-stu-id="0fd0e-105">Arithmetic shift right (sign extending).</span></span>



| <span data-ttu-id="0fd0e-106">ishl dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0fd0e-106">ishl dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|--------------------------------------------------------|



 



| <span data-ttu-id="0fd0e-107">Item</span><span class="sxs-lookup"><span data-stu-id="0fd0e-107">Item</span></span>                                                            | <span data-ttu-id="0fd0e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="0fd0e-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="0fd0e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0fd0e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0fd0e-110">\[in \] contém os resultados da mudança.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-110">\[in\] Contains the results of the shift.</span></span><br/> |
| <span data-ttu-id="0fd0e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0fd0e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0fd0e-112">\[no \] número de bits a serem deslocados.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-112">\[in\] The number of bits to shift.</span></span><br/>       |
| <span data-ttu-id="0fd0e-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="0fd0e-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="0fd0e-114">\[nos \] valores de 32 bits para Shift.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-114">\[in\] The 32-bit values to shift.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="0fd0e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="0fd0e-115">Remarks</span></span>

<span data-ttu-id="0fd0e-116">Essa instrução executa uma mudança aritmética de componente de cada valor de 32 bits em *src0* à direita por um número de bits de inteiro sem sinal fornecido pelo LSB 5 bits (0-31 intervalo) em *src1*, replicando o valor do bit 31.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-116">This instruction performs a component-wise arithmetic shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1*, replicating the value of bit 31.</span></span> <span data-ttu-id="0fd0e-117">O resultado de 32 bits por componente é colocado no *dest*.</span><span class="sxs-lookup"><span data-stu-id="0fd0e-117">The 32-bit per component result is placed in *dest*.</span></span>

<span data-ttu-id="0fd0e-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0fd0e-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0fd0e-119">Vértice</span><span class="sxs-lookup"><span data-stu-id="0fd0e-119">Vertex</span></span> | <span data-ttu-id="0fd0e-120">Envoltória</span><span class="sxs-lookup"><span data-stu-id="0fd0e-120">Hull</span></span> | <span data-ttu-id="0fd0e-121">Domínio</span><span class="sxs-lookup"><span data-stu-id="0fd0e-121">Domain</span></span> | <span data-ttu-id="0fd0e-122">Geometria</span><span class="sxs-lookup"><span data-stu-id="0fd0e-122">Geometry</span></span> | <span data-ttu-id="0fd0e-123">16x16</span><span class="sxs-lookup"><span data-stu-id="0fd0e-123">Pixel</span></span> | <span data-ttu-id="0fd0e-124">Computação</span><span class="sxs-lookup"><span data-stu-id="0fd0e-124">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="0fd0e-125">X</span><span class="sxs-lookup"><span data-stu-id="0fd0e-125">X</span></span>      | <span data-ttu-id="0fd0e-126">X</span><span class="sxs-lookup"><span data-stu-id="0fd0e-126">X</span></span>    | <span data-ttu-id="0fd0e-127">X</span><span class="sxs-lookup"><span data-stu-id="0fd0e-127">X</span></span>      | <span data-ttu-id="0fd0e-128">X</span><span class="sxs-lookup"><span data-stu-id="0fd0e-128">X</span></span>        | <span data-ttu-id="0fd0e-129">X</span><span class="sxs-lookup"><span data-stu-id="0fd0e-129">X</span></span>     | <span data-ttu-id="0fd0e-130">X</span><span class="sxs-lookup"><span data-stu-id="0fd0e-130">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0fd0e-131">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="0fd0e-131">Minimum Shader Model</span></span>

<span data-ttu-id="0fd0e-132">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0fd0e-132">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="0fd0e-133">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="0fd0e-133">Shader Model</span></span>                                              | <span data-ttu-id="0fd0e-134">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0fd0e-134">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0fd0e-135">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0fd0e-135">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0fd0e-136">sim</span><span class="sxs-lookup"><span data-stu-id="0fd0e-136">yes</span></span>       |
| [<span data-ttu-id="0fd0e-137">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0fd0e-137">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0fd0e-138">não</span><span class="sxs-lookup"><span data-stu-id="0fd0e-138">no</span></span>        |
| [<span data-ttu-id="0fd0e-139">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0fd0e-139">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0fd0e-140">não</span><span class="sxs-lookup"><span data-stu-id="0fd0e-140">no</span></span>        |
| [<span data-ttu-id="0fd0e-141">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fd0e-141">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0fd0e-142">não</span><span class="sxs-lookup"><span data-stu-id="0fd0e-142">no</span></span>        |
| [<span data-ttu-id="0fd0e-143">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fd0e-143">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0fd0e-144">não</span><span class="sxs-lookup"><span data-stu-id="0fd0e-144">no</span></span>        |
| [<span data-ttu-id="0fd0e-145">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fd0e-145">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0fd0e-146">não</span><span class="sxs-lookup"><span data-stu-id="0fd0e-146">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0fd0e-147">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0fd0e-147">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0fd0e-148">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0fd0e-148">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





