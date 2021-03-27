---
title: FRC (sm4-ASM)
description: Componente-Wise, extraia o componente fracionário.
ms.assetid: 17C88BCE-7F2F-446C-9BB4-860098B5E42A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c4abcfd56e7d6051e9c476097b3e5eef4d97563e
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967120"
---
# <a name="frc-sm4---asm"></a><span data-ttu-id="0608c-103">FRC (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="0608c-103">frc (sm4 - asm)</span></span>

<span data-ttu-id="0608c-104">Componente-Wise, extraia o componente fracionário.</span><span class="sxs-lookup"><span data-stu-id="0608c-104">Component-wise, extract fractional component.</span></span>



| <span data-ttu-id="0608c-105">FRC \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="0608c-105">frc\[\_sat\] dest\[.mask\], \[-\] src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------|



 



| <span data-ttu-id="0608c-106">Item</span><span class="sxs-lookup"><span data-stu-id="0608c-106">Item</span></span>                                                            | <span data-ttu-id="0608c-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="0608c-107">Description</span></span>                                                                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0608c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="0608c-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="0608c-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="0608c-109">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="0608c-110">*dest*  =  *src0*  -  [ \_ Ni arredondado](round-ni--sm4---asm-.md)(*src0*)</span><span class="sxs-lookup"><span data-stu-id="0608c-110">*dest* = *src0* - [round\_ni](round-ni--sm4---asm-.md)(*src0*)</span></span><br/> |
| <span data-ttu-id="0608c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="0608c-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="0608c-112">\[no \] componente na operação.</span><span class="sxs-lookup"><span data-stu-id="0608c-112">\[in\] The component in the operation.</span></span><br/>                                                                                        |



 

## <a name="remarks"></a><span data-ttu-id="0608c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0608c-113">Remarks</span></span>

<span data-ttu-id="0608c-114">A tabela a seguir mostra os resultados obtidos ao executar a instrução com várias classes de números.</span><span class="sxs-lookup"><span data-stu-id="0608c-114">The following table shows the results obtained when executing the instruction with various classes of numbers.</span></span>



|          |          |            |             |        |        |             |            |          |         |
|----------|----------|------------|-------------|--------|--------|-------------|------------|----------|---------|
| <span data-ttu-id="0608c-115">**src**</span><span class="sxs-lookup"><span data-stu-id="0608c-115">**src**</span></span>  | <span data-ttu-id="0608c-116">**-INF**</span><span class="sxs-lookup"><span data-stu-id="0608c-116">**-inf**</span></span> | <span data-ttu-id="0608c-117">**-F**</span><span class="sxs-lookup"><span data-stu-id="0608c-117">**-F**</span></span>     | <span data-ttu-id="0608c-118">**-desnorma**</span><span class="sxs-lookup"><span data-stu-id="0608c-118">**-denorm**</span></span> | <span data-ttu-id="0608c-119">**-0**</span><span class="sxs-lookup"><span data-stu-id="0608c-119">**-0**</span></span> | <span data-ttu-id="0608c-120">**+0**</span><span class="sxs-lookup"><span data-stu-id="0608c-120">**+0**</span></span> | <span data-ttu-id="0608c-121">**+ desnormativo**</span><span class="sxs-lookup"><span data-stu-id="0608c-121">**+denorm**</span></span> | <span data-ttu-id="0608c-122">**+ F**</span><span class="sxs-lookup"><span data-stu-id="0608c-122">**+F**</span></span>     | <span data-ttu-id="0608c-123">**+ INF**</span><span class="sxs-lookup"><span data-stu-id="0608c-123">**+inf**</span></span> | <span data-ttu-id="0608c-124">**NaN**</span><span class="sxs-lookup"><span data-stu-id="0608c-124">**NaN**</span></span> |
| <span data-ttu-id="0608c-125">**dest**</span><span class="sxs-lookup"><span data-stu-id="0608c-125">**dest**</span></span> | <span data-ttu-id="0608c-126">NaN</span><span class="sxs-lookup"><span data-stu-id="0608c-126">NaN</span></span>      | <span data-ttu-id="0608c-127">\[+ 0 a 1)</span><span class="sxs-lookup"><span data-stu-id="0608c-127">\[+0 to 1)</span></span> | <span data-ttu-id="0608c-128">+0</span><span class="sxs-lookup"><span data-stu-id="0608c-128">+0</span></span>          | <span data-ttu-id="0608c-129">+0</span><span class="sxs-lookup"><span data-stu-id="0608c-129">+0</span></span>     | <span data-ttu-id="0608c-130">+0</span><span class="sxs-lookup"><span data-stu-id="0608c-130">+0</span></span>     | <span data-ttu-id="0608c-131">+0</span><span class="sxs-lookup"><span data-stu-id="0608c-131">+0</span></span>          | <span data-ttu-id="0608c-132">\[+ 0 a 1)</span><span class="sxs-lookup"><span data-stu-id="0608c-132">\[+0 to 1)</span></span> | <span data-ttu-id="0608c-133">NaN</span><span class="sxs-lookup"><span data-stu-id="0608c-133">NaN</span></span>      | <span data-ttu-id="0608c-134">NaN</span><span class="sxs-lookup"><span data-stu-id="0608c-134">NaN</span></span>     |



 

<span data-ttu-id="0608c-135">F significa número real finito.</span><span class="sxs-lookup"><span data-stu-id="0608c-135">F means finite-real number.</span></span>

<span data-ttu-id="0608c-136">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="0608c-136">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="0608c-137">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="0608c-137">Vertex Shader</span></span> | <span data-ttu-id="0608c-138">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="0608c-138">Geometry Shader</span></span> | <span data-ttu-id="0608c-139">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="0608c-139">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="0608c-140">x</span><span class="sxs-lookup"><span data-stu-id="0608c-140">x</span></span>             | <span data-ttu-id="0608c-141">x</span><span class="sxs-lookup"><span data-stu-id="0608c-141">x</span></span>               | <span data-ttu-id="0608c-142">x</span><span class="sxs-lookup"><span data-stu-id="0608c-142">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="0608c-143">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="0608c-143">Minimum Shader Model</span></span>

<span data-ttu-id="0608c-144">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="0608c-144">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="0608c-145">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="0608c-145">Shader Model</span></span>                                              | <span data-ttu-id="0608c-146">Com suporte</span><span class="sxs-lookup"><span data-stu-id="0608c-146">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="0608c-147">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="0608c-147">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="0608c-148">sim</span><span class="sxs-lookup"><span data-stu-id="0608c-148">yes</span></span>       |
| [<span data-ttu-id="0608c-149">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="0608c-149">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="0608c-150">sim</span><span class="sxs-lookup"><span data-stu-id="0608c-150">yes</span></span>       |
| [<span data-ttu-id="0608c-151">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="0608c-151">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="0608c-152">sim</span><span class="sxs-lookup"><span data-stu-id="0608c-152">yes</span></span>       |
| [<span data-ttu-id="0608c-153">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0608c-153">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="0608c-154">não</span><span class="sxs-lookup"><span data-stu-id="0608c-154">no</span></span>        |
| [<span data-ttu-id="0608c-155">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0608c-155">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="0608c-156">não</span><span class="sxs-lookup"><span data-stu-id="0608c-156">no</span></span>        |
| [<span data-ttu-id="0608c-157">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0608c-157">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="0608c-158">não</span><span class="sxs-lookup"><span data-stu-id="0608c-158">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="0608c-159">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="0608c-159">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="0608c-160">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="0608c-160">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





