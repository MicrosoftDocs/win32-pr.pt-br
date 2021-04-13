---
title: ishl (sm4-ASM)
description: Deslocar para a esquerda. | ishl (sm4-ASM)
ms.assetid: FA0213B8-8A76-4916-8B2F-0983C404A838
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8e14225f8c8b0e46cf0ba6eda61f96e4563a904e
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104989208"
---
# <a name="ishl-sm4---asm"></a><span data-ttu-id="148c8-104">ishl (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="148c8-104">ishl (sm4 - asm)</span></span>

<span data-ttu-id="148c8-105">Deslocar para a esquerda.</span><span class="sxs-lookup"><span data-stu-id="148c8-105">Shift left.</span></span>



| <span data-ttu-id="148c8-106">dest \[ . Mask \] , src0 \[ . swizzle \] , o componente src1. Select \_</span><span class="sxs-lookup"><span data-stu-id="148c8-106">dest\[.mask\], src0\[.swizzle\], src1.select\_component</span></span> |
|---------------------------------------------------------|



 



| <span data-ttu-id="148c8-107">Item</span><span class="sxs-lookup"><span data-stu-id="148c8-107">Item</span></span>                                                            | <span data-ttu-id="148c8-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="148c8-108">Description</span></span>                                                   |
|-----------------------------------------------------------------|---------------------------------------------------------------|
| <span data-ttu-id="148c8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="148c8-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="148c8-110">\[no \] endereço do resultado da operação.</span><span class="sxs-lookup"><span data-stu-id="148c8-110">\[in\] The address of the result of the operation.</span></span><br/> |
| <span data-ttu-id="148c8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span><span class="sxs-lookup"><span data-stu-id="148c8-111"><span id="src0"></span><span id="SRC0"></span>*src0*</span></span><br/> | <span data-ttu-id="148c8-112">\[in \] contém os valores a serem deslocados.</span><span class="sxs-lookup"><span data-stu-id="148c8-112">\[in\] Contains the values to be shifted.</span></span><br/>          |
| <span data-ttu-id="148c8-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span><span class="sxs-lookup"><span data-stu-id="148c8-113"><span id="src1"></span><span id="SRC1"></span>*src1*</span></span><br/> | <span data-ttu-id="148c8-114">\[in \] contém o valor de deslocamento.</span><span class="sxs-lookup"><span data-stu-id="148c8-114">\[in\] Contains the shift amount.</span></span><br/>                  |



 

## <a name="remarks"></a><span data-ttu-id="148c8-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="148c8-115">Remarks</span></span>

<span data-ttu-id="148c8-116">Essa instrução executa uma mudança de componente de cada valor de 32 bits no *src0* Left por um número de bits de inteiro sem sinal fornecido pelo LSB 5 bits (0-31 intervalo) no *\_ componente src1. Select*, inserindo 0.</span><span class="sxs-lookup"><span data-stu-id="148c8-116">This instruction performs a component-wise shift of each 32-bit value in *src0* left by an unsigned integer bit count provided by the LSB 5 bits (0-31 range) in *src1.select\_component*, inserting 0.</span></span> <span data-ttu-id="148c8-117">Os resultados de 32 bits por componente são colocados no *dest*.</span><span class="sxs-lookup"><span data-stu-id="148c8-117">The 32-bit per component results are placed in *dest*.</span></span> <span data-ttu-id="148c8-118">A contagem é um valor escalar aplicado a todos os componentes.</span><span class="sxs-lookup"><span data-stu-id="148c8-118">The count is a scalar value applied to all components.</span></span>

<span data-ttu-id="148c8-119">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="148c8-119">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="148c8-120">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="148c8-120">Vertex Shader</span></span> | <span data-ttu-id="148c8-121">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="148c8-121">Geometry Shader</span></span> | <span data-ttu-id="148c8-122">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="148c8-122">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="148c8-123">x</span><span class="sxs-lookup"><span data-stu-id="148c8-123">x</span></span>             | <span data-ttu-id="148c8-124">x</span><span class="sxs-lookup"><span data-stu-id="148c8-124">x</span></span>               | <span data-ttu-id="148c8-125">x</span><span class="sxs-lookup"><span data-stu-id="148c8-125">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="148c8-126">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="148c8-126">Minimum Shader Model</span></span>

<span data-ttu-id="148c8-127">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="148c8-127">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="148c8-128">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="148c8-128">Shader Model</span></span>                                              | <span data-ttu-id="148c8-129">Com suporte</span><span class="sxs-lookup"><span data-stu-id="148c8-129">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="148c8-130">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="148c8-130">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="148c8-131">sim</span><span class="sxs-lookup"><span data-stu-id="148c8-131">yes</span></span>       |
| [<span data-ttu-id="148c8-132">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="148c8-132">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="148c8-133">sim</span><span class="sxs-lookup"><span data-stu-id="148c8-133">yes</span></span>       |
| [<span data-ttu-id="148c8-134">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="148c8-134">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="148c8-135">sim</span><span class="sxs-lookup"><span data-stu-id="148c8-135">yes</span></span>       |
| [<span data-ttu-id="148c8-136">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="148c8-136">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="148c8-137">não</span><span class="sxs-lookup"><span data-stu-id="148c8-137">no</span></span>        |
| [<span data-ttu-id="148c8-138">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="148c8-138">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="148c8-139">não</span><span class="sxs-lookup"><span data-stu-id="148c8-139">no</span></span>        |
| [<span data-ttu-id="148c8-140">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="148c8-140">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="148c8-141">não</span><span class="sxs-lookup"><span data-stu-id="148c8-141">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="148c8-142">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="148c8-142">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="148c8-143">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="148c8-143">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 





