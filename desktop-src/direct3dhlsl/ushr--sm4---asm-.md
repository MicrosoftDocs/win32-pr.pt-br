---
title: ushr (sm4-ASM)
description: Deslocar para a direita. | ushr (sm4-ASM)
ms.assetid: 3E7CB515-9D0F-44C7-A770-AD0584631BFE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9c48b706afb1223a5289f93b5ca393a89c36e915
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172660"
---
# <a name="ushr-sm4---asm"></a><span data-ttu-id="baa0e-104">ushr (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="baa0e-104">ushr (sm4 - asm)</span></span>

<span data-ttu-id="baa0e-105">Deslocar para a direita.</span><span class="sxs-lookup"><span data-stu-id="baa0e-105">Shift right.</span></span>



| <span data-ttu-id="baa0e-106">ushr dest \[ . Mask \] , src0 \[ . swizzle \] , o componente src1. Select \_</span><span class="sxs-lookup"><span data-stu-id="baa0e-106">ushr dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|--------------------------------------------------------------|



 



| <span data-ttu-id="baa0e-107">Item</span><span class="sxs-lookup"><span data-stu-id="baa0e-107">Item</span></span>                                                            | <span data-ttu-id="baa0e-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="baa0e-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="baa0e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="baa0e-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="baa0e-110">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="baa0e-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="baa0e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="baa0e-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="baa0e-112">\[nos \] componentes a serem deslocados.</span><span class="sxs-lookup"><span data-stu-id="baa0e-112">\[in\] The components to shift.</span></span><br/>                    |
| <span data-ttu-id="baa0e-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="baa0e-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="baa0e-114">\[no \] valor para SHIFT *src0*.</span><span class="sxs-lookup"><span data-stu-id="baa0e-114">\[in\] The amount to shift *src0*.</span></span><br/>                 |



 

## <a name="remarks"></a><span data-ttu-id="baa0e-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="baa0e-115">Remarks</span></span>

<span data-ttu-id="baa0e-116">Essa instrução executa uma mudança de componente de cada valor de 32 bits em *src0* à direita por uma contagem de bits de inteiro sem sinal fornecida pelo LSB de 5 bits (0-31 intervalo) no *\_ componente src1. Select*, inserindo 0.</span><span class="sxs-lookup"><span data-stu-id="baa0e-116">This instruction performs a component-wise shift of each 32-bit value in *src0* right by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="baa0e-117">O resultado de 32 bits por componente é colocado no *dest*.</span><span class="sxs-lookup"><span data-stu-id="baa0e-117">The 32-bit per component result is placed in *dest*.</span></span> <span data-ttu-id="baa0e-118">A contagem é um valor escalar aplicado a todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="baa0e-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="baa0e-119">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="baa0e-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="baa0e-120">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="baa0e-120">Vertex Shader</span></span> | <span data-ttu-id="baa0e-121">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="baa0e-121">Geometry Shader</span></span> | <span data-ttu-id="baa0e-122">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="baa0e-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="baa0e-123">x</span><span class="sxs-lookup"><span data-stu-id="baa0e-123">x</span></span>             | <span data-ttu-id="baa0e-124">x</span><span class="sxs-lookup"><span data-stu-id="baa0e-124">x</span></span>               | <span data-ttu-id="baa0e-125">x</span><span class="sxs-lookup"><span data-stu-id="baa0e-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="baa0e-126">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="baa0e-126">Minimum Shader Model</span></span>

<span data-ttu-id="baa0e-127">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="baa0e-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="baa0e-128">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="baa0e-128">Shader Model</span></span>                                              | <span data-ttu-id="baa0e-129">Com suporte</span><span class="sxs-lookup"><span data-stu-id="baa0e-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="baa0e-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="baa0e-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="baa0e-131">sim</span><span class="sxs-lookup"><span data-stu-id="baa0e-131">yes</span></span>       |
| [<span data-ttu-id="baa0e-132">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="baa0e-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="baa0e-133">sim</span><span class="sxs-lookup"><span data-stu-id="baa0e-133">yes</span></span>       |
| [<span data-ttu-id="baa0e-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="baa0e-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="baa0e-135">sim</span><span class="sxs-lookup"><span data-stu-id="baa0e-135">yes</span></span>       |
| [<span data-ttu-id="baa0e-136">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baa0e-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="baa0e-137">não</span><span class="sxs-lookup"><span data-stu-id="baa0e-137">no</span></span>        |
| [<span data-ttu-id="baa0e-138">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baa0e-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="baa0e-139">não</span><span class="sxs-lookup"><span data-stu-id="baa0e-139">no</span></span>        |
| [<span data-ttu-id="baa0e-140">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baa0e-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="baa0e-141">não</span><span class="sxs-lookup"><span data-stu-id="baa0e-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="baa0e-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="baa0e-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="baa0e-143">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="baa0e-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





