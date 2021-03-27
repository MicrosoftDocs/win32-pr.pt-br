---
title: countbits (SM5-ASM)
description: Conta o número de bits definidos em um número.
ms.assetid: ED75487F-46FF-45F5-BEAA-7A32BEFB0571
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 55d46fe9c750790d65630a743dd9ddc347fea50e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103823448"
---
# <a name="countbits-sm5---asm"></a><span data-ttu-id="f6021-103">countbits (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f6021-103">countbits (sm5 - asm)</span></span>

<span data-ttu-id="f6021-104">Conta o número de bits definidos em um número.</span><span class="sxs-lookup"><span data-stu-id="f6021-104">Counts the number of bits set in a number.</span></span>



| <span data-ttu-id="f6021-105">countbits dest \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f6021-105">countbits dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------------|



 



| <span data-ttu-id="f6021-106">Item</span><span class="sxs-lookup"><span data-stu-id="f6021-106">Item</span></span>                                                            | <span data-ttu-id="f6021-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="f6021-107">Description</span></span>                                   |
|-----------------------------------------------------------------|-----------------------------------------------|
| <span data-ttu-id="f6021-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f6021-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f6021-109">\[no \] endereço dos resultados.</span><span class="sxs-lookup"><span data-stu-id="f6021-109">\[in\] The address of the results.</span></span><br/> |
| <span data-ttu-id="f6021-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="f6021-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="f6021-111">\[no \] número de entrada 32-bit.</span><span class="sxs-lookup"><span data-stu-id="f6021-111">\[in\] The input 32-bit number.</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="f6021-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="f6021-112">Remarks</span></span>

<span data-ttu-id="f6021-113">Essa instrução pode ser usada para calcular a porcentagem de cobertura de entrada do sombreador.</span><span class="sxs-lookup"><span data-stu-id="f6021-113">This instruction can be used to compute shader input coverage percentage.</span></span>

<span data-ttu-id="f6021-114">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f6021-114">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f6021-115">Vértice</span><span class="sxs-lookup"><span data-stu-id="f6021-115">Vertex</span></span> | <span data-ttu-id="f6021-116">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f6021-116">Hull</span></span> | <span data-ttu-id="f6021-117">Domínio</span><span class="sxs-lookup"><span data-stu-id="f6021-117">Domain</span></span> | <span data-ttu-id="f6021-118">Geometria</span><span class="sxs-lookup"><span data-stu-id="f6021-118">Geometry</span></span> | <span data-ttu-id="f6021-119">16x16</span><span class="sxs-lookup"><span data-stu-id="f6021-119">Pixel</span></span> | <span data-ttu-id="f6021-120">Computação</span><span class="sxs-lookup"><span data-stu-id="f6021-120">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f6021-121">X</span><span class="sxs-lookup"><span data-stu-id="f6021-121">X</span></span>      | <span data-ttu-id="f6021-122">X</span><span class="sxs-lookup"><span data-stu-id="f6021-122">X</span></span>    | <span data-ttu-id="f6021-123">X</span><span class="sxs-lookup"><span data-stu-id="f6021-123">X</span></span>      | <span data-ttu-id="f6021-124">X</span><span class="sxs-lookup"><span data-stu-id="f6021-124">X</span></span>        | <span data-ttu-id="f6021-125">X</span><span class="sxs-lookup"><span data-stu-id="f6021-125">X</span></span>     | <span data-ttu-id="f6021-126">X</span><span class="sxs-lookup"><span data-stu-id="f6021-126">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f6021-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f6021-127">Minimum Shader Model</span></span>

<span data-ttu-id="f6021-128">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f6021-128">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f6021-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f6021-129">Shader Model</span></span>                                              | <span data-ttu-id="f6021-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f6021-130">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f6021-131">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f6021-131">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f6021-132">sim</span><span class="sxs-lookup"><span data-stu-id="f6021-132">yes</span></span>       |
| [<span data-ttu-id="f6021-133">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f6021-133">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f6021-134">não</span><span class="sxs-lookup"><span data-stu-id="f6021-134">no</span></span>        |
| [<span data-ttu-id="f6021-135">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f6021-135">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f6021-136">não</span><span class="sxs-lookup"><span data-stu-id="f6021-136">no</span></span>        |
| [<span data-ttu-id="f6021-137">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6021-137">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f6021-138">não</span><span class="sxs-lookup"><span data-stu-id="f6021-138">no</span></span>        |
| [<span data-ttu-id="f6021-139">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6021-139">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f6021-140">não</span><span class="sxs-lookup"><span data-stu-id="f6021-140">no</span></span>        |
| [<span data-ttu-id="f6021-141">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6021-141">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f6021-142">não</span><span class="sxs-lookup"><span data-stu-id="f6021-142">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f6021-143">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f6021-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f6021-144">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f6021-144">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





