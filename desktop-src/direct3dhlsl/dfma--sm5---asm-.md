---
title: dfma (SM5-ASM)
description: Executa uma adição de multiplicação de fusível.
ms.assetid: 5BE96CDB-1756-4EBE-B4CC-69EFF098A4F1
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b2e6cafc71dbc7d57655524b1b87c9c5b9ba20f3
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104293565"
---
# <a name="dfma-sm5---asm"></a><span data-ttu-id="ce9a3-103">dfma (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="ce9a3-103">dfma (sm5 - asm)</span></span>

<span data-ttu-id="ce9a3-104">Executa uma adição de multiplicação de fusível.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-104">Performs a fused-multiply add.</span></span>



| <span data-ttu-id="ce9a3-105">dfma \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src2 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="ce9a3-105">dfma\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\],\[-\]src2\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------------------------------------------------|



 



| <span data-ttu-id="ce9a3-106">Item</span><span class="sxs-lookup"><span data-stu-id="ce9a3-106">Item</span></span>                                                            | <span data-ttu-id="ce9a3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="ce9a3-107">Description</span></span>                                                                                                                                               |
|-----------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ce9a3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="ce9a3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="ce9a3-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-109">\[in\] The address of the result of the operation.</span></span> <span data-ttu-id="ce9a3-110">O valor do resultado deve ser preciso para o 0,5 ULP.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-110">The result value must be accurate to 0.5 ULP.</span></span><br/> <span data-ttu-id="ce9a3-111">*dest*  =  *src0* \* *src1*  +  *src2*</span><span class="sxs-lookup"><span data-stu-id="ce9a3-111">*dest* = *src0* \* *src1* + *src2*</span></span><br/> |
| <span data-ttu-id="ce9a3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="ce9a3-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="ce9a3-113">\[nos \] componentes para multiplicar com *src1*.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-113">\[in\] The components to multiply with *src1*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="ce9a3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="ce9a3-114"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="ce9a3-115">\[nos \] componentes para multiplicar com *src0*.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-115">\[in\] The components to multiply with *src0*.</span></span><br/>                                                                                                 |
| <span data-ttu-id="ce9a3-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span><span class="sxs-lookup"><span data-stu-id="ce9a3-116"><span id="src2"></span><span id="SRC2"></span>*src2*</span></span><br/> | <span data-ttu-id="ce9a3-117">\[nos \] componentes a serem adicionados ao *src0* \* *src1*.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-117">\[in\] The components to add to *src0* \* *src1*.</span></span><br/>                                                                                               |



 

## <a name="remarks"></a><span data-ttu-id="ce9a3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="ce9a3-118">Remarks</span></span>

<span data-ttu-id="ce9a3-119">Os sombreadores que usam essa instrução serão marcados com um sinalizador de sombreador que fará com que eles não sejam associados, a menos que todas as condições a seguir sejam atendidas.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-119">Shaders that use this instruction will be marked with a shader flag that will cause them to fail to bind unless all the following conditions are met.</span></span>

-   <span data-ttu-id="ce9a3-120">O sistema dá suporte ao DirectX 11,1.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-120">The system supports DirectX 11.1.</span></span>
-   <span data-ttu-id="ce9a3-121">O sistema inclui um Driver WDDM 1,2.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-121">The system includes a WDDM 1.2 driver.</span></span>
-   <span data-ttu-id="ce9a3-122">O driver fornece suporte para essa instrução por meio de **Opções de D3D11 de dados de recursos do D3D11 \_ \_ \_ \_ . ExtendedDoublesShaderInstructions** definido como **true**.</span><span class="sxs-lookup"><span data-stu-id="ce9a3-122">The driver reports support for this instruction via **D3D11\_FEATURE\_DATA\_D3D11\_OPTIONS.ExtendedDoublesShaderInstructions** set to **TRUE**.</span></span>

<span data-ttu-id="ce9a3-123">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ce9a3-123">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="ce9a3-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="ce9a3-124">Vertex</span></span> | <span data-ttu-id="ce9a3-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="ce9a3-125">Hull</span></span> | <span data-ttu-id="ce9a3-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="ce9a3-126">Domain</span></span> | <span data-ttu-id="ce9a3-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="ce9a3-127">Geometry</span></span> | <span data-ttu-id="ce9a3-128">16x16</span><span class="sxs-lookup"><span data-stu-id="ce9a3-128">Pixel</span></span> | <span data-ttu-id="ce9a3-129">Computação</span><span class="sxs-lookup"><span data-stu-id="ce9a3-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="ce9a3-130">X</span><span class="sxs-lookup"><span data-stu-id="ce9a3-130">X</span></span>      | <span data-ttu-id="ce9a3-131">X</span><span class="sxs-lookup"><span data-stu-id="ce9a3-131">X</span></span>    | <span data-ttu-id="ce9a3-132">X</span><span class="sxs-lookup"><span data-stu-id="ce9a3-132">X</span></span>      | <span data-ttu-id="ce9a3-133">X</span><span class="sxs-lookup"><span data-stu-id="ce9a3-133">X</span></span>        | <span data-ttu-id="ce9a3-134">X</span><span class="sxs-lookup"><span data-stu-id="ce9a3-134">X</span></span>     | <span data-ttu-id="ce9a3-135">X</span><span class="sxs-lookup"><span data-stu-id="ce9a3-135">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="ce9a3-136">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="ce9a3-136">Minimum Shader Model</span></span>

<span data-ttu-id="ce9a3-137">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="ce9a3-137">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="ce9a3-138">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="ce9a3-138">Shader Model</span></span>                                              | <span data-ttu-id="ce9a3-139">Com suporte</span><span class="sxs-lookup"><span data-stu-id="ce9a3-139">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="ce9a3-140">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="ce9a3-140">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="ce9a3-141">sim</span><span class="sxs-lookup"><span data-stu-id="ce9a3-141">yes</span></span>       |
| [<span data-ttu-id="ce9a3-142">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="ce9a3-142">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="ce9a3-143">não</span><span class="sxs-lookup"><span data-stu-id="ce9a3-143">no</span></span>        |
| [<span data-ttu-id="ce9a3-144">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="ce9a3-144">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="ce9a3-145">não</span><span class="sxs-lookup"><span data-stu-id="ce9a3-145">no</span></span>        |
| [<span data-ttu-id="ce9a3-146">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce9a3-146">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="ce9a3-147">não</span><span class="sxs-lookup"><span data-stu-id="ce9a3-147">no</span></span>        |
| [<span data-ttu-id="ce9a3-148">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce9a3-148">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="ce9a3-149">não</span><span class="sxs-lookup"><span data-stu-id="ce9a3-149">no</span></span>        |
| [<span data-ttu-id="ce9a3-150">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce9a3-150">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="ce9a3-151">não</span><span class="sxs-lookup"><span data-stu-id="ce9a3-151">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="ce9a3-152">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="ce9a3-152">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce9a3-153">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="ce9a3-153">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





