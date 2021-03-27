---
title: Não (sm4-ASM)
description: Não é possível.
ms.assetid: AC7EBBC2-4B52-4793-812C-B25897FB8D05
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0bf224e6e5af7f2db6bcbaf7ae287ba2d399727
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967125"
---
# <a name="not-sm4---asm"></a><span data-ttu-id="55382-103">Não (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="55382-103">not (sm4 - asm)</span></span>

<span data-ttu-id="55382-104">Não é possível.</span><span class="sxs-lookup"><span data-stu-id="55382-104">Bitwise not.</span></span>



| <span data-ttu-id="55382-105">Não dest \[ . Mask \] , src0 \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="55382-105">not dest\[.mask\], src0\[.swizzle\]</span></span> |
|-------------------------------------|



 



| <span data-ttu-id="55382-106">Item</span><span class="sxs-lookup"><span data-stu-id="55382-106">Item</span></span>                                                            | <span data-ttu-id="55382-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="55382-107">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="55382-108"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="55382-108"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="55382-109">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="55382-109">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="55382-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="55382-110"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="55382-111">\[nos \] componentes originais.</span><span class="sxs-lookup"><span data-stu-id="55382-111">\[in\] The original components.</span></span><br/>                    |



 

## <a name="remarks"></a><span data-ttu-id="55382-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="55382-112">Remarks</span></span>

<span data-ttu-id="55382-113">Essa instrução executa um complemento de um componente de cada valor de 32 bits em *src0*.</span><span class="sxs-lookup"><span data-stu-id="55382-113">This instruction performs a component-wise one's complement of each 32-bit value in *src0*.</span></span> <span data-ttu-id="55382-114">Os resultados de 32 bits são armazenados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="55382-114">The 32-bit results are stored in *dest*.</span></span>

<span data-ttu-id="55382-115">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="55382-115">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="55382-116">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="55382-116">Vertex Shader</span></span> | <span data-ttu-id="55382-117">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="55382-117">Geometry Shader</span></span> | <span data-ttu-id="55382-118">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="55382-118">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="55382-119">x</span><span class="sxs-lookup"><span data-stu-id="55382-119">x</span></span>             | <span data-ttu-id="55382-120">x</span><span class="sxs-lookup"><span data-stu-id="55382-120">x</span></span>               | <span data-ttu-id="55382-121">x</span><span class="sxs-lookup"><span data-stu-id="55382-121">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="55382-122">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="55382-122">Minimum Shader Model</span></span>

<span data-ttu-id="55382-123">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="55382-123">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="55382-124">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="55382-124">Shader Model</span></span>                                              | <span data-ttu-id="55382-125">Com suporte</span><span class="sxs-lookup"><span data-stu-id="55382-125">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="55382-126">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="55382-126">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="55382-127">sim</span><span class="sxs-lookup"><span data-stu-id="55382-127">yes</span></span>       |
| [<span data-ttu-id="55382-128">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="55382-128">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="55382-129">sim</span><span class="sxs-lookup"><span data-stu-id="55382-129">yes</span></span>       |
| [<span data-ttu-id="55382-130">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="55382-130">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="55382-131">sim</span><span class="sxs-lookup"><span data-stu-id="55382-131">yes</span></span>       |
| [<span data-ttu-id="55382-132">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="55382-132">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="55382-133">não</span><span class="sxs-lookup"><span data-stu-id="55382-133">no</span></span>        |
| [<span data-ttu-id="55382-134">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="55382-134">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="55382-135">não</span><span class="sxs-lookup"><span data-stu-id="55382-135">no</span></span>        |
| [<span data-ttu-id="55382-136">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="55382-136">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="55382-137">não</span><span class="sxs-lookup"><span data-stu-id="55382-137">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="55382-138">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="55382-138">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="55382-139">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="55382-139">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





