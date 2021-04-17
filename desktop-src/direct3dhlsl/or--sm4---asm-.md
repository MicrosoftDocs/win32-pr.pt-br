---
title: ou (sm4-ASM)
description: OR-bit.
ms.assetid: BBC06F8C-4C86-4077-A1F9-383D6A8FBED3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 62064189725b246cc48bbde03a9c094d13f8b9a0
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104988601"
---
# <a name="or-sm4---asm"></a><span data-ttu-id="b277d-103">ou (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="b277d-103">or (sm4 - asm)</span></span>

<span data-ttu-id="b277d-104">OR-bit.</span><span class="sxs-lookup"><span data-stu-id="b277d-104">Bitwise or.</span></span>



| <span data-ttu-id="b277d-105">ou dest \[ . Mask \] , src0 \[ . swizzle \] , src1 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="b277d-105">or dest\[.mask\], src0\[.swizzle\], src1\[.swizzle\]</span></span> |
|------------------------------------------------------|



 



| <span data-ttu-id="b277d-106">Item</span><span class="sxs-lookup"><span data-stu-id="b277d-106">Item</span></span>                                                            | <span data-ttu-id="b277d-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="b277d-107">Description</span></span>                                         |
|-----------------------------------------------------------------|-----------------------------------------------------|
| <span data-ttu-id="b277d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="b277d-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="b277d-109">\[no \] resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="b277d-109">\[in\] The result of the operation.</span></span><br/>      |
| <span data-ttu-id="b277d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="b277d-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="b277d-111">\[nos \] componentes para ou com *src1*.</span><span class="sxs-lookup"><span data-stu-id="b277d-111">\[in\] The components to OR with *src1*.</span></span><br/> |
| <span data-ttu-id="b277d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="b277d-112"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="b277d-113">\[nos \] componentes para ou com *src0*.</span><span class="sxs-lookup"><span data-stu-id="b277d-113">\[in\] The components to OR with *src0*.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="b277d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="b277d-114">Remarks</span></span>

<span data-ttu-id="b277d-115">Essa instrução executa um componente lógico ou de cada par de valores de 32 bits de *src0* e *src1*.</span><span class="sxs-lookup"><span data-stu-id="b277d-115">This instruction performs a component-wise logical OR of each pair of 32-bit values from *src0* and *src1*.</span></span> <span data-ttu-id="b277d-116">Os resultados de 32 bits são colocados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="b277d-116">The 32-bit results are placed in *dest*.</span></span>

<span data-ttu-id="b277d-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="b277d-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="b277d-118">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="b277d-118">Vertex Shader</span></span> | <span data-ttu-id="b277d-119">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="b277d-119">Geometry Shader</span></span> | <span data-ttu-id="b277d-120">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="b277d-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="b277d-121">x</span><span class="sxs-lookup"><span data-stu-id="b277d-121">x</span></span>             | <span data-ttu-id="b277d-122">x</span><span class="sxs-lookup"><span data-stu-id="b277d-122">x</span></span>               | <span data-ttu-id="b277d-123">x</span><span class="sxs-lookup"><span data-stu-id="b277d-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="b277d-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="b277d-124">Minimum Shader Model</span></span>

<span data-ttu-id="b277d-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b277d-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="b277d-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="b277d-126">Shader Model</span></span>                                              | <span data-ttu-id="b277d-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="b277d-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="b277d-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="b277d-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="b277d-129">sim</span><span class="sxs-lookup"><span data-stu-id="b277d-129">yes</span></span>       |
| [<span data-ttu-id="b277d-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="b277d-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="b277d-131">sim</span><span class="sxs-lookup"><span data-stu-id="b277d-131">yes</span></span>       |
| [<span data-ttu-id="b277d-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="b277d-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="b277d-133">sim</span><span class="sxs-lookup"><span data-stu-id="b277d-133">yes</span></span>       |
| [<span data-ttu-id="b277d-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b277d-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="b277d-135">não</span><span class="sxs-lookup"><span data-stu-id="b277d-135">no</span></span>        |
| [<span data-ttu-id="b277d-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b277d-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="b277d-137">não</span><span class="sxs-lookup"><span data-stu-id="b277d-137">no</span></span>        |
| [<span data-ttu-id="b277d-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b277d-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="b277d-139">não</span><span class="sxs-lookup"><span data-stu-id="b277d-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="b277d-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="b277d-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b277d-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="b277d-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





