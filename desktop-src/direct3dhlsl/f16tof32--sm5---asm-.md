---
title: f16tof32 (SM5-ASM)
description: Float16 de componente para conversão de float32. | f16tof32 (SM5-ASM)
ms.assetid: CFAA1350-DA7F-4105-A90A-72052C5E2FB3
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d53af1f2eab1f50dfded820bf27b2cda8f23e6b4
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968396"
---
# <a name="f16tof32-sm5---asm"></a><span data-ttu-id="f9de1-104">f16tof32 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="f9de1-104">f16tof32 (sm5 - asm)</span></span>

<span data-ttu-id="f9de1-105">Float16 de componente para conversão de float32.</span><span class="sxs-lookup"><span data-stu-id="f9de1-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="f9de1-106">f16tof32 dest \[ . Mask \] , \[ - \] src \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="f9de1-106">f16tof32 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="f9de1-107">Item</span><span class="sxs-lookup"><span data-stu-id="f9de1-107">Item</span></span>                                                            | <span data-ttu-id="f9de1-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="f9de1-108">Description</span></span>                                          |
|-----------------------------------------------------------------|------------------------------------------------------|
| <span data-ttu-id="f9de1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="f9de1-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="f9de1-110">\[no \] endereço do resultado de float32.</span><span class="sxs-lookup"><span data-stu-id="f9de1-110">\[in\] The address of the float32 result.</span></span><br/> |
| <span data-ttu-id="f9de1-111"><span id="src"></span><span id="SRC"></span>*orig*</span><span class="sxs-lookup"><span data-stu-id="f9de1-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="f9de1-112">\[no \] valor float16 a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="f9de1-112">\[in\] The float16 value to convert.</span></span><br/>      |



 

## <a name="remarks"></a><span data-ttu-id="f9de1-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="f9de1-113">Remarks</span></span>

<span data-ttu-id="f9de1-114">Esta operação executa uma conversão por componente de um valor de float16 de LSB bits para um resultado de float32.</span><span class="sxs-lookup"><span data-stu-id="f9de1-114">This operation performs a component-wise conversion of a float16 value from LSB bits to a float32 result.</span></span>

<span data-ttu-id="f9de1-115">Esta operação segue as regras do D3D para conversão de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="f9de1-115">This operation follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="f9de1-116">Use esta instrução para descompactação de dados orientada por sombreador.</span><span class="sxs-lookup"><span data-stu-id="f9de1-116">Use this instruction for shader-driven data decompression.</span></span>

<span data-ttu-id="f9de1-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f9de1-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f9de1-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="f9de1-118">Vertex</span></span> | <span data-ttu-id="f9de1-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="f9de1-119">Hull</span></span> | <span data-ttu-id="f9de1-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="f9de1-120">Domain</span></span> | <span data-ttu-id="f9de1-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="f9de1-121">Geometry</span></span> | <span data-ttu-id="f9de1-122">16x16</span><span class="sxs-lookup"><span data-stu-id="f9de1-122">Pixel</span></span> | <span data-ttu-id="f9de1-123">Computação</span><span class="sxs-lookup"><span data-stu-id="f9de1-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="f9de1-124">X</span><span class="sxs-lookup"><span data-stu-id="f9de1-124">X</span></span>      | <span data-ttu-id="f9de1-125">X</span><span class="sxs-lookup"><span data-stu-id="f9de1-125">X</span></span>    | <span data-ttu-id="f9de1-126">X</span><span class="sxs-lookup"><span data-stu-id="f9de1-126">X</span></span>      | <span data-ttu-id="f9de1-127">X</span><span class="sxs-lookup"><span data-stu-id="f9de1-127">X</span></span>        | <span data-ttu-id="f9de1-128">X</span><span class="sxs-lookup"><span data-stu-id="f9de1-128">X</span></span>     | <span data-ttu-id="f9de1-129">X</span><span class="sxs-lookup"><span data-stu-id="f9de1-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f9de1-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f9de1-130">Minimum Shader Model</span></span>

<span data-ttu-id="f9de1-131">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f9de1-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="f9de1-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f9de1-132">Shader Model</span></span>                                              | <span data-ttu-id="f9de1-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f9de1-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f9de1-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f9de1-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f9de1-135">sim</span><span class="sxs-lookup"><span data-stu-id="f9de1-135">yes</span></span>       |
| [<span data-ttu-id="f9de1-136">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f9de1-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f9de1-137">não</span><span class="sxs-lookup"><span data-stu-id="f9de1-137">no</span></span>        |
| [<span data-ttu-id="f9de1-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f9de1-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f9de1-139">não</span><span class="sxs-lookup"><span data-stu-id="f9de1-139">no</span></span>        |
| [<span data-ttu-id="f9de1-140">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9de1-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f9de1-141">não</span><span class="sxs-lookup"><span data-stu-id="f9de1-141">no</span></span>        |
| [<span data-ttu-id="f9de1-142">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9de1-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f9de1-143">não</span><span class="sxs-lookup"><span data-stu-id="f9de1-143">no</span></span>        |
| [<span data-ttu-id="f9de1-144">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9de1-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f9de1-145">não</span><span class="sxs-lookup"><span data-stu-id="f9de1-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f9de1-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f9de1-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f9de1-147">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f9de1-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





