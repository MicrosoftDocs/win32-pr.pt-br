---
title: IgE (sm4-ASM)
description: Comparação de inteiro de vetor por componente, maior que ou-igual.
ms.assetid: 3A3225D1-9A3D-4928-9041-38CB6DE16E2A
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8709ebedb054dffe227340f2ccd3de572d92ffce
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104084258"
---
# <a name="ige-sm4---asm"></a><span data-ttu-id="16fe3-103">IgE (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="16fe3-103">ige (sm4 - asm)</span></span>

<span data-ttu-id="16fe3-104">Comparação de inteiro de vetor por componente, maior que ou-igual.</span><span class="sxs-lookup"><span data-stu-id="16fe3-104">Component-wise vector integer greater-than-or-equal comparison.</span></span>



| <span data-ttu-id="16fe3-105">IgE dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="16fe3-105">ige dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|-------------------------------------------------------|



 



| <span data-ttu-id="16fe3-106">Item</span><span class="sxs-lookup"><span data-stu-id="16fe3-106">Item</span></span>                                                            | <span data-ttu-id="16fe3-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="16fe3-107">Description</span></span>                                           |
|-----------------------------------------------------------------|-------------------------------------------------------|
| <span data-ttu-id="16fe3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="16fe3-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="16fe3-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="16fe3-109">\[in\] The result of the operation.</span></span><br/>        |
| <span data-ttu-id="16fe3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="16fe3-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="16fe3-111">\[no \] componente a ser comparado com *src1*.</span><span class="sxs-lookup"><span data-stu-id="16fe3-111">\[in\] The component to compare to *src1*.</span></span><br/> |
| <span data-ttu-id="16fe3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="16fe3-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="16fe3-113">\[no \] componente a ser comparado com *src0*.</span><span class="sxs-lookup"><span data-stu-id="16fe3-113">\[in\] The component to compare to *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="16fe3-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="16fe3-114">Remarks</span></span>

<span data-ttu-id="16fe3-115">Executa a comparação de inteiros (*src0*  >=  *src1*) para cada componente e grava o resultado em *dest*.</span><span class="sxs-lookup"><span data-stu-id="16fe3-115">Performs the integer comparison (*src0* >= *src1*) for each component, and writes the result to *dest*.</span></span>

<span data-ttu-id="16fe3-116">Se a comparação for verdadeira, 0xFFFFFFFF será retornado para esse componente.</span><span class="sxs-lookup"><span data-stu-id="16fe3-116">If the comparison is true, then 0xFFFFFFFF is returned for that component.</span></span> <span data-ttu-id="16fe3-117">Caso contrário, 0x0000000 será retornado.</span><span class="sxs-lookup"><span data-stu-id="16fe3-117">Otherwise 0x0000000 is returned.</span></span>

<span data-ttu-id="16fe3-118">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="16fe3-118">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="16fe3-119">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="16fe3-119">Vertex Shader</span></span> | <span data-ttu-id="16fe3-120">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="16fe3-120">Geometry Shader</span></span> | <span data-ttu-id="16fe3-121">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="16fe3-121">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="16fe3-122">x</span><span class="sxs-lookup"><span data-stu-id="16fe3-122">x</span></span>             | <span data-ttu-id="16fe3-123">x</span><span class="sxs-lookup"><span data-stu-id="16fe3-123">x</span></span>               | <span data-ttu-id="16fe3-124">x</span><span class="sxs-lookup"><span data-stu-id="16fe3-124">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="16fe3-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="16fe3-125">Minimum Shader Model</span></span>

<span data-ttu-id="16fe3-126">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="16fe3-126">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="16fe3-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="16fe3-127">Shader Model</span></span>                                              | <span data-ttu-id="16fe3-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="16fe3-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="16fe3-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="16fe3-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="16fe3-130">sim</span><span class="sxs-lookup"><span data-stu-id="16fe3-130">yes</span></span>       |
| [<span data-ttu-id="16fe3-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="16fe3-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="16fe3-132">sim</span><span class="sxs-lookup"><span data-stu-id="16fe3-132">yes</span></span>       |
| [<span data-ttu-id="16fe3-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="16fe3-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="16fe3-134">sim</span><span class="sxs-lookup"><span data-stu-id="16fe3-134">yes</span></span>       |
| [<span data-ttu-id="16fe3-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16fe3-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="16fe3-136">não</span><span class="sxs-lookup"><span data-stu-id="16fe3-136">no</span></span>        |
| [<span data-ttu-id="16fe3-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16fe3-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="16fe3-138">não</span><span class="sxs-lookup"><span data-stu-id="16fe3-138">no</span></span>        |
| [<span data-ttu-id="16fe3-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16fe3-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="16fe3-140">não</span><span class="sxs-lookup"><span data-stu-id="16fe3-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="16fe3-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="16fe3-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="16fe3-142">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="16fe3-142">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





