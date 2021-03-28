---
title: MOV (sm4-ASM)
description: Movimentação por componentes. | MOV (sm4-ASM)
ms.assetid: A8865237-59D3-4332-9F09-157E10C4FFC6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f029cd8a31a9348e729681878773c225b87b9fbb
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104172625"
---
# <a name="mov-sm4---asm"></a><span data-ttu-id="1815b-104">MOV (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="1815b-104">mov (sm4 - asm)</span></span>

<span data-ttu-id="1815b-105">Movimentação por componentes.</span><span class="sxs-lookup"><span data-stu-id="1815b-105">Component-wise move.</span></span>



| <span data-ttu-id="1815b-106">Instrução: mov \[ \_ SAT \] dest \[ . Mask \] , \[ - \] src0 \[ \_ ABS \] \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="1815b-106">Instruction: mov\[\_sat\] dest\[.mask\], \[-\]src0\[\_abs\]\[.swizzle\]</span></span> |
|-------------------------------------------------------------------------|



 



| <span data-ttu-id="1815b-107">Item</span><span class="sxs-lookup"><span data-stu-id="1815b-107">Item</span></span>                                                            | <span data-ttu-id="1815b-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="1815b-108">Description</span></span>                                                                              |
|-----------------------------------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1815b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="1815b-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="1815b-110">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="1815b-110">\[in\] The address of the result of the operation.</span></span><br/> <span data-ttu-id="1815b-111">*dest*  =  *src0*</span><span class="sxs-lookup"><span data-stu-id="1815b-111">*dest* = *src0*</span></span><br/> |
| <span data-ttu-id="1815b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="1815b-112"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="1815b-113">\[nos \] componentes a serem movidos.</span><span class="sxs-lookup"><span data-stu-id="1815b-113">\[in\] The components to move.</span></span><br/>                                                |



 

## <a name="remarks"></a><span data-ttu-id="1815b-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="1815b-114">Remarks</span></span>

<span data-ttu-id="1815b-115">Os modificadores, exceto swizzle, assumem que os dados são de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="1815b-115">The modifiers, other than swizzle, assume the data is floating point.</span></span> <span data-ttu-id="1815b-116">A ausência de modificadores apenas move dados sem alterar bits.</span><span class="sxs-lookup"><span data-stu-id="1815b-116">The absence of modifiers just moves data without altering bits.</span></span>

<span data-ttu-id="1815b-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="1815b-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="1815b-118">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="1815b-118">Vertex Shader</span></span> | <span data-ttu-id="1815b-119">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="1815b-119">Geometry Shader</span></span> | <span data-ttu-id="1815b-120">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="1815b-120">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="1815b-121">x</span><span class="sxs-lookup"><span data-stu-id="1815b-121">x</span></span>             | <span data-ttu-id="1815b-122">x</span><span class="sxs-lookup"><span data-stu-id="1815b-122">x</span></span>               | <span data-ttu-id="1815b-123">x</span><span class="sxs-lookup"><span data-stu-id="1815b-123">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="1815b-124">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="1815b-124">Minimum Shader Model</span></span>

<span data-ttu-id="1815b-125">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1815b-125">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1815b-126">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="1815b-126">Shader Model</span></span>                                              | <span data-ttu-id="1815b-127">Com suporte</span><span class="sxs-lookup"><span data-stu-id="1815b-127">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="1815b-128">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1815b-128">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="1815b-129">sim</span><span class="sxs-lookup"><span data-stu-id="1815b-129">yes</span></span>       |
| [<span data-ttu-id="1815b-130">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="1815b-130">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="1815b-131">sim</span><span class="sxs-lookup"><span data-stu-id="1815b-131">yes</span></span>       |
| [<span data-ttu-id="1815b-132">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="1815b-132">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="1815b-133">sim</span><span class="sxs-lookup"><span data-stu-id="1815b-133">yes</span></span>       |
| [<span data-ttu-id="1815b-134">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1815b-134">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="1815b-135">não</span><span class="sxs-lookup"><span data-stu-id="1815b-135">no</span></span>        |
| [<span data-ttu-id="1815b-136">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1815b-136">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="1815b-137">não</span><span class="sxs-lookup"><span data-stu-id="1815b-137">no</span></span>        |
| [<span data-ttu-id="1815b-138">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1815b-138">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="1815b-139">não</span><span class="sxs-lookup"><span data-stu-id="1815b-139">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="1815b-140">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="1815b-140">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="1815b-141">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="1815b-141">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





