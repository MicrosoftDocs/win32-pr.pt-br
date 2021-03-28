---
title: GE (sm4-ASM)
description: Comparação de ponto flutuante de vetor por componente, maior que ou igual.
ms.assetid: 658AF249-4935-41AF-972A-D8CDEABA76AA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c93d21d9ac044e2ad4d63e954a4732a15794b123
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365213"
---
# <a name="ge-sm4---asm"></a><span data-ttu-id="8bf29-103">GE (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="8bf29-103">ge (sm4 - asm)</span></span>

<span data-ttu-id="8bf29-104">Comparação de ponto flutuante de vetor por componente, maior que ou igual.</span><span class="sxs-lookup"><span data-stu-id="8bf29-104">Component-wise vector floating point greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="8bf29-105">GE dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle \] , \[ - \] src1 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="8bf29-105">ge dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\], \[-\]src1\[\_abs\]\[.swizzle\]</span></span> |
|----------------------------------------------------------------------------------|



 



| <span data-ttu-id="8bf29-106">Item</span><span class="sxs-lookup"><span data-stu-id="8bf29-106">Item</span></span>                                                            | <span data-ttu-id="8bf29-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8bf29-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="8bf29-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="8bf29-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="8bf29-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="8bf29-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="8bf29-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="8bf29-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="8bf29-111">\[no \] componente a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="8bf29-111">\[in\] The component to compare to *src1*.</span></span><br/>         |
| <span data-ttu-id="8bf29-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="8bf29-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="8bf29-113">\[no \] componente a ser comparado com *src0*.</span><span class="sxs-lookup"><span data-stu-id="8bf29-113">\[in\] The component to compare to *src0*.</span></span><br/>         |



 

## <a name="remarks"></a><span data-ttu-id="8bf29-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="8bf29-114">Remarks</span></span>

<span data-ttu-id="8bf29-115">Executa a comparação de float (*src0*  >=  *src1*) para cada componente e grava o resultado em *dest*.</span><span class="sxs-lookup"><span data-stu-id="8bf29-115">Performs the float comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="8bf29-116">Se a comparação for verdadeira, 0xFFFFFFFF será retornado para esse componente.</span><span class="sxs-lookup"><span data-stu-id="8bf29-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="8bf29-117">Caso contrário, 0x0000000 será retornado.</span><span class="sxs-lookup"><span data-stu-id="8bf29-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="8bf29-118">As normas são liberadas antes da comparação, e os registros de origem originais são inalterados.</span><span class="sxs-lookup"><span data-stu-id="8bf29-118">Denorms are flushed before comparison, and original source registers are untouched.</span></span> <span data-ttu-id="8bf29-119">+ 0 é igual a-0.</span><span class="sxs-lookup"><span data-stu-id="8bf29-119">+0 equals -0.</span></span> <span data-ttu-id="8bf29-120">A comparação com NaN retorna false.</span><span class="sxs-lookup"><span data-stu-id="8bf29-120">Comparison with NaN returns false.</span></span>

<span data-ttu-id="8bf29-121">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8bf29-121">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8bf29-122">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="8bf29-122">Vertex Shader</span></span> | <span data-ttu-id="8bf29-123">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="8bf29-123">Geometry Shader</span></span> | <span data-ttu-id="8bf29-124">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="8bf29-124">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="8bf29-125">x</span><span class="sxs-lookup"><span data-stu-id="8bf29-125">x</span></span>             | <span data-ttu-id="8bf29-126">x</span><span class="sxs-lookup"><span data-stu-id="8bf29-126">x</span></span>               | <span data-ttu-id="8bf29-127">x</span><span class="sxs-lookup"><span data-stu-id="8bf29-127">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8bf29-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8bf29-128">Minimum Shader Model</span></span>

<span data-ttu-id="8bf29-129">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="8bf29-129">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="8bf29-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8bf29-130">Shader Model</span></span>                                              | <span data-ttu-id="8bf29-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8bf29-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8bf29-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8bf29-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8bf29-133">sim</span><span class="sxs-lookup"><span data-stu-id="8bf29-133">yes</span></span>       |
| [<span data-ttu-id="8bf29-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8bf29-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8bf29-135">sim</span><span class="sxs-lookup"><span data-stu-id="8bf29-135">yes</span></span>       |
| [<span data-ttu-id="8bf29-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8bf29-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8bf29-137">sim</span><span class="sxs-lookup"><span data-stu-id="8bf29-137">yes</span></span>       |
| [<span data-ttu-id="8bf29-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bf29-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8bf29-139">não</span><span class="sxs-lookup"><span data-stu-id="8bf29-139">no</span></span>        |
| [<span data-ttu-id="8bf29-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bf29-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8bf29-141">não</span><span class="sxs-lookup"><span data-stu-id="8bf29-141">no</span></span>        |
| [<span data-ttu-id="8bf29-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bf29-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8bf29-143">não</span><span class="sxs-lookup"><span data-stu-id="8bf29-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8bf29-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8bf29-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8bf29-145">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8bf29-145">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





