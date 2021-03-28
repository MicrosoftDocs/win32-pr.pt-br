---
title: f32tof16 (SM5-ASM)
description: Float16 de componente para conversão de float32. | f32tof16 (SM5-ASM)
ms.assetid: 36BCCFC5-722A-45EB-8A66-7544833BBBA5
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54a101f370f9c53d1d3f43f9e1cf6c4da82933d
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104968525"
---
# <a name="f32tof16-sm5---asm"></a><span data-ttu-id="9c22c-104">f32tof16 (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="9c22c-104">f32tof16 (sm5 - asm)</span></span>

<span data-ttu-id="9c22c-105">Float16 de componente para conversão de float32.</span><span class="sxs-lookup"><span data-stu-id="9c22c-105">Component-wise float16 to float32 conversion.</span></span>



| <span data-ttu-id="9c22c-106">f32tof16 dest \[ . Mask \] , \[ - \] src \[ . swizzle\]</span><span class="sxs-lookup"><span data-stu-id="9c22c-106">f32tof16 dest\[.mask\], \[-\]src\[.swizzle\]</span></span> |
|----------------------------------------------|



 



| <span data-ttu-id="9c22c-107">Item</span><span class="sxs-lookup"><span data-stu-id="9c22c-107">Item</span></span>                                                            | <span data-ttu-id="9c22c-108">Descrição</span><span class="sxs-lookup"><span data-stu-id="9c22c-108">Description</span></span>                                      |
|-----------------------------------------------------------------|--------------------------------------------------|
| <span data-ttu-id="9c22c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span><span class="sxs-lookup"><span data-stu-id="9c22c-109"><span id="dest"></span><span id="DEST"></span>*dest*</span></span><br/> | <span data-ttu-id="9c22c-110">\[no \] endereço do resultado de float16.</span><span class="sxs-lookup"><span data-stu-id="9c22c-110">\[in\] The address of float16 result.</span></span><br/> |
| <span data-ttu-id="9c22c-111"><span id="src"></span><span id="SRC"></span>*orig*</span><span class="sxs-lookup"><span data-stu-id="9c22c-111"><span id="src"></span><span id="SRC"></span>*src*</span></span><br/>    | <span data-ttu-id="9c22c-112">\[no \] valor float32 a ser convertido.</span><span class="sxs-lookup"><span data-stu-id="9c22c-112">\[in\] The float32 value to convert.</span></span><br/>  |



 

## <a name="remarks"></a><span data-ttu-id="9c22c-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="9c22c-113">Remarks</span></span>

<span data-ttu-id="9c22c-114">Essa instrução executa uma conversão por componente de um valor de float32 em um resultado de valor float16 colocado em LSB 16 bits.</span><span class="sxs-lookup"><span data-stu-id="9c22c-114">This instruction performs a component-wise conversion of a float32 value to a float16 value result placed in LSB 16 bits.</span></span>

<span data-ttu-id="9c22c-115">Essa instrução segue as regras do D3D para conversão de ponto flutuante.</span><span class="sxs-lookup"><span data-stu-id="9c22c-115">This instruction follows D3D rules for floating point conversion.</span></span>

<span data-ttu-id="9c22c-116">Use esta instrução para compactação de dados orientada por sombreador.</span><span class="sxs-lookup"><span data-stu-id="9c22c-116">Use this instruction for shader-driven data compression.</span></span>

<span data-ttu-id="9c22c-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9c22c-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="9c22c-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="9c22c-118">Vertex</span></span> | <span data-ttu-id="9c22c-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="9c22c-119">Hull</span></span> | <span data-ttu-id="9c22c-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="9c22c-120">Domain</span></span> | <span data-ttu-id="9c22c-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="9c22c-121">Geometry</span></span> | <span data-ttu-id="9c22c-122">16x16</span><span class="sxs-lookup"><span data-stu-id="9c22c-122">Pixel</span></span> | <span data-ttu-id="9c22c-123">Computação</span><span class="sxs-lookup"><span data-stu-id="9c22c-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="9c22c-124">X</span><span class="sxs-lookup"><span data-stu-id="9c22c-124">X</span></span>      | <span data-ttu-id="9c22c-125">X</span><span class="sxs-lookup"><span data-stu-id="9c22c-125">X</span></span>    | <span data-ttu-id="9c22c-126">X</span><span class="sxs-lookup"><span data-stu-id="9c22c-126">X</span></span>      | <span data-ttu-id="9c22c-127">X</span><span class="sxs-lookup"><span data-stu-id="9c22c-127">X</span></span>        | <span data-ttu-id="9c22c-128">X</span><span class="sxs-lookup"><span data-stu-id="9c22c-128">X</span></span>     | <span data-ttu-id="9c22c-129">X</span><span class="sxs-lookup"><span data-stu-id="9c22c-129">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="9c22c-130">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="9c22c-130">Minimum Shader Model</span></span>

<span data-ttu-id="9c22c-131">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="9c22c-131">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="9c22c-132">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="9c22c-132">Shader Model</span></span>                                              | <span data-ttu-id="9c22c-133">Com suporte</span><span class="sxs-lookup"><span data-stu-id="9c22c-133">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="9c22c-134">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="9c22c-134">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="9c22c-135">sim</span><span class="sxs-lookup"><span data-stu-id="9c22c-135">yes</span></span>       |
| [<span data-ttu-id="9c22c-136">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="9c22c-136">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="9c22c-137">não</span><span class="sxs-lookup"><span data-stu-id="9c22c-137">no</span></span>        |
| [<span data-ttu-id="9c22c-138">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="9c22c-138">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="9c22c-139">não</span><span class="sxs-lookup"><span data-stu-id="9c22c-139">no</span></span>        |
| [<span data-ttu-id="9c22c-140">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c22c-140">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="9c22c-141">não</span><span class="sxs-lookup"><span data-stu-id="9c22c-141">no</span></span>        |
| [<span data-ttu-id="9c22c-142">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c22c-142">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="9c22c-143">não</span><span class="sxs-lookup"><span data-stu-id="9c22c-143">no</span></span>        |
| [<span data-ttu-id="9c22c-144">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c22c-144">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="9c22c-145">não</span><span class="sxs-lookup"><span data-stu-id="9c22c-145">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="9c22c-146">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="9c22c-146">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="9c22c-147">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="9c22c-147">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





