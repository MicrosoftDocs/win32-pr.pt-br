---
title: dcl_thread_group (SM5-ASM)
description: Declare o tamanho do grupo de threads.
ms.assetid: CB8192C4-100D-49B6-94E7-6CD3AEC28149
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b8141c80e82f1dfd1ae5a4d360d04fac32ba5221
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104006916"
---
# <a name="dcl_thread_group-sm5---asm"></a><span data-ttu-id="e519a-103">\_grupo de threads DCL \_ (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="e519a-103">dcl\_thread\_group (sm5 - asm)</span></span>

<span data-ttu-id="e519a-104">Declare o tamanho do grupo de threads.</span><span class="sxs-lookup"><span data-stu-id="e519a-104">Declare thread group size.</span></span>



| <span data-ttu-id="e519a-105">\_grupo de threads DCL \_ x, y, z</span><span class="sxs-lookup"><span data-stu-id="e519a-105">dcl\_thread\_group x, y, z</span></span> |
|----------------------------|



 



| <span data-ttu-id="e519a-106">Item</span><span class="sxs-lookup"><span data-stu-id="e519a-106">Item</span></span>                                                   | <span data-ttu-id="e519a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="e519a-107">Description</span></span>                                                        |
|--------------------------------------------------------|--------------------------------------------------------------------|
| <span data-ttu-id="e519a-108"><span id="x"></span><span id="X"></span>*w.x.y.*</span><span class="sxs-lookup"><span data-stu-id="e519a-108"><span id="x"></span><span id="X"></span>*x*</span></span><br/> | <span data-ttu-id="e519a-109">\[em \] um número inteiro de usigned de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e519a-109">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="e519a-110">1 <= x <= 1024</span><span class="sxs-lookup"><span data-stu-id="e519a-110">1 <= x <= 1024</span></span> <br/> |
| <span data-ttu-id="e519a-111"><span id="y"></span><span id="Y"></span>*Iar*</span><span class="sxs-lookup"><span data-stu-id="e519a-111"><span id="y"></span><span id="Y"></span>*y*</span></span><br/> | <span data-ttu-id="e519a-112">\[em \] um número inteiro de usigned de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e519a-112">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="e519a-113">1 <= y <= 1024</span><span class="sxs-lookup"><span data-stu-id="e519a-113">1 <= y <= 1024</span></span><br/>  |
| <span data-ttu-id="e519a-114"><span id="z"></span><span id="Z"></span>*z*</span><span class="sxs-lookup"><span data-stu-id="e519a-114"><span id="z"></span><span id="Z"></span>*z*</span></span><br/> | <span data-ttu-id="e519a-115">\[em \] um número inteiro de usigned de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="e519a-115">\[in\] An usigned 32-bit integer.</span></span> <span data-ttu-id="e519a-116">1 <= z <= 64</span><span class="sxs-lookup"><span data-stu-id="e519a-116">1 <= z <= 64</span></span><br/>    |



 

## <a name="remarks"></a><span data-ttu-id="e519a-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="e519a-117">Remarks</span></span>

<span data-ttu-id="e519a-118">x \* y \* z <= 1024</span><span class="sxs-lookup"><span data-stu-id="e519a-118">x\*y\*z <= 1024</span></span>

<span data-ttu-id="e519a-119">Essa declaração de grupo de threads deve aparecer uma vez em um sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="e519a-119">This thread group declaration must appear once in a compute shader.</span></span>

<span data-ttu-id="e519a-120">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e519a-120">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="e519a-121">Vértice</span><span class="sxs-lookup"><span data-stu-id="e519a-121">Vertex</span></span> | <span data-ttu-id="e519a-122">Envoltória</span><span class="sxs-lookup"><span data-stu-id="e519a-122">Hull</span></span> | <span data-ttu-id="e519a-123">Domínio</span><span class="sxs-lookup"><span data-stu-id="e519a-123">Domain</span></span> | <span data-ttu-id="e519a-124">Geometria</span><span class="sxs-lookup"><span data-stu-id="e519a-124">Geometry</span></span> | <span data-ttu-id="e519a-125">16x16</span><span class="sxs-lookup"><span data-stu-id="e519a-125">Pixel</span></span> | <span data-ttu-id="e519a-126">Computação</span><span class="sxs-lookup"><span data-stu-id="e519a-126">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="e519a-127">X</span><span class="sxs-lookup"><span data-stu-id="e519a-127">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="e519a-128">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="e519a-128">Minimum Shader Model</span></span>

<span data-ttu-id="e519a-129">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="e519a-129">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="e519a-130">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="e519a-130">Shader Model</span></span>                                              | <span data-ttu-id="e519a-131">Com suporte</span><span class="sxs-lookup"><span data-stu-id="e519a-131">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="e519a-132">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="e519a-132">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="e519a-133">sim</span><span class="sxs-lookup"><span data-stu-id="e519a-133">yes</span></span>       |
| [<span data-ttu-id="e519a-134">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="e519a-134">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="e519a-135">não</span><span class="sxs-lookup"><span data-stu-id="e519a-135">no</span></span>        |
| [<span data-ttu-id="e519a-136">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="e519a-136">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="e519a-137">não</span><span class="sxs-lookup"><span data-stu-id="e519a-137">no</span></span>        |
| [<span data-ttu-id="e519a-138">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e519a-138">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="e519a-139">não</span><span class="sxs-lookup"><span data-stu-id="e519a-139">no</span></span>        |
| [<span data-ttu-id="e519a-140">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e519a-140">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="e519a-141">não</span><span class="sxs-lookup"><span data-stu-id="e519a-141">no</span></span>        |
| [<span data-ttu-id="e519a-142">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e519a-142">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="e519a-143">não</span><span class="sxs-lookup"><span data-stu-id="e519a-143">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="e519a-144">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="e519a-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e519a-145">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="e519a-145">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





