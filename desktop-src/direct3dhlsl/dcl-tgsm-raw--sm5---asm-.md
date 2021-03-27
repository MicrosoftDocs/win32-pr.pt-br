---
title: dcl_tgsm_raw (SM5-ASM)
description: Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação.
ms.assetid: 8EA6931C-5B13-431F-A886-04F8C73CD22D
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dd20d8a0d8d2309b9b895a5cb5439877bb10d31a
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638890"
---
# <a name="dcl_tgsm_raw-sm5---asm"></a><span data-ttu-id="8d7be-103">DCL \_ tgsm \_ bruto (SM5-ASM)</span><span class="sxs-lookup"><span data-stu-id="8d7be-103">dcl\_tgsm\_raw (sm5 - asm)</span></span>

<span data-ttu-id="8d7be-104">Declare uma referência a uma região de espaço de memória compartilhada disponível para o grupo de threads do sombreador de computação.</span><span class="sxs-lookup"><span data-stu-id="8d7be-104">Declare a reference to a region of shared memory space available to the compute shader s thread group.</span></span>



| <span data-ttu-id="8d7be-105">DCL \_ tgsm \_ bruto g \# , byteCount</span><span class="sxs-lookup"><span data-stu-id="8d7be-105">dcl\_tgsm\_raw g\#, byteCount</span></span> |
|-------------------------------|



 



| <span data-ttu-id="8d7be-106">Item</span><span class="sxs-lookup"><span data-stu-id="8d7be-106">Item</span></span>                                                                                                       | <span data-ttu-id="8d7be-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="8d7be-107">Description</span></span>                                                                             |
|------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="8d7be-108"><span id="g_"></span><span id="G_"></span>*m\#*</span><span class="sxs-lookup"><span data-stu-id="8d7be-108"><span id="g_"></span><span id="G_"></span>*g\#*</span></span><br/>                                                 | <span data-ttu-id="8d7be-109">\[em \] uma referência a um bloco de tamanho *byteCount* de memória compartilhada não tipada.</span><span class="sxs-lookup"><span data-stu-id="8d7be-109">\[in\] A reference to a block of size *byteCount* of untyped shared memory.</span></span> <br/> |
| <span data-ttu-id="8d7be-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span><span class="sxs-lookup"><span data-stu-id="8d7be-110"><span id="byteCount"></span><span id="bytecount"></span><span id="BYTECOUNT"></span>*byteCount*</span></span><br/> | <span data-ttu-id="8d7be-111">\[in \] deve ser um múltiplo de 4.</span><span class="sxs-lookup"><span data-stu-id="8d7be-111">\[in\] Must be a multiple of 4.</span></span> <br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="8d7be-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8d7be-112">Remarks</span></span>

<span data-ttu-id="8d7be-113">O armazenamento total para todos os g \# deve ser <= a quantidade de memória compartilhada disponível por grupo de threads, que é 32 KB.</span><span class="sxs-lookup"><span data-stu-id="8d7be-113">The total storage for all g\# must be <= the amount of shared memory available per thread group, which is 32kB.</span></span>

<span data-ttu-id="8d7be-114">Em um caso extremo, você pode declarar o total de 8192 g \# s, cada um com um *byteCount* de 4.</span><span class="sxs-lookup"><span data-stu-id="8d7be-114">In an extreme case, you can declare 8192 total g\# s, each with a *byteCount* of 4.</span></span>

<span data-ttu-id="8d7be-115">No lado oposto, você pode declarar um g único \# com um *byteCount* de 32768.</span><span class="sxs-lookup"><span data-stu-id="8d7be-115">In the opposite extreme, you can declare a single g\# with a *byteCount* of 32768.</span></span>

> [!Note]  
> <span data-ttu-id="8d7be-116">o cs \_ 4 \_ 0 e o cs \_ 4 \_ 1 dão suporte ao [ \_ tgsm DCL \_ estruturado](dcl-tgsm-structured--sm5---asm-.md), mas não ao **DCL \_ tgsm \_ RAW**.</span><span class="sxs-lookup"><span data-stu-id="8d7be-116">cs\_4\_0 and cs\_4\_1 supports [dcl\_tgsm\_structured](dcl-tgsm-structured--sm5---asm-.md), but not **dcl\_tgsm\_raw**.</span></span>

 

<span data-ttu-id="8d7be-117">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8d7be-117">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="8d7be-118">Vértice</span><span class="sxs-lookup"><span data-stu-id="8d7be-118">Vertex</span></span> | <span data-ttu-id="8d7be-119">Envoltória</span><span class="sxs-lookup"><span data-stu-id="8d7be-119">Hull</span></span> | <span data-ttu-id="8d7be-120">Domínio</span><span class="sxs-lookup"><span data-stu-id="8d7be-120">Domain</span></span> | <span data-ttu-id="8d7be-121">Geometria</span><span class="sxs-lookup"><span data-stu-id="8d7be-121">Geometry</span></span> | <span data-ttu-id="8d7be-122">16x16</span><span class="sxs-lookup"><span data-stu-id="8d7be-122">Pixel</span></span> | <span data-ttu-id="8d7be-123">Computação</span><span class="sxs-lookup"><span data-stu-id="8d7be-123">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|        |      |        |          |       | <span data-ttu-id="8d7be-124">X</span><span class="sxs-lookup"><span data-stu-id="8d7be-124">X</span></span>       |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="8d7be-125">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="8d7be-125">Minimum Shader Model</span></span>

<span data-ttu-id="8d7be-126">Essa instrução tem suporte nos seguintes modelos de sombreador:</span><span class="sxs-lookup"><span data-stu-id="8d7be-126">This instruction is supported in the following shader models:</span></span>



| <span data-ttu-id="8d7be-127">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="8d7be-127">Shader Model</span></span>                                              | <span data-ttu-id="8d7be-128">Com suporte</span><span class="sxs-lookup"><span data-stu-id="8d7be-128">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="8d7be-129">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8d7be-129">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="8d7be-130">sim</span><span class="sxs-lookup"><span data-stu-id="8d7be-130">yes</span></span>       |
| [<span data-ttu-id="8d7be-131">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="8d7be-131">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="8d7be-132">não</span><span class="sxs-lookup"><span data-stu-id="8d7be-132">no</span></span>        |
| [<span data-ttu-id="8d7be-133">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="8d7be-133">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="8d7be-134">não</span><span class="sxs-lookup"><span data-stu-id="8d7be-134">no</span></span>        |
| [<span data-ttu-id="8d7be-135">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d7be-135">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="8d7be-136">não</span><span class="sxs-lookup"><span data-stu-id="8d7be-136">no</span></span>        |
| [<span data-ttu-id="8d7be-137">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d7be-137">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="8d7be-138">não</span><span class="sxs-lookup"><span data-stu-id="8d7be-138">no</span></span>        |
| [<span data-ttu-id="8d7be-139">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d7be-139">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="8d7be-140">não</span><span class="sxs-lookup"><span data-stu-id="8d7be-140">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="8d7be-141">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="8d7be-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="8d7be-142">Assembly do Shader Model 5 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="8d7be-142">Shader Model 5 Assembly (DirectX HLSL)</span></span>](shader-model-5-assembly--directx-hlsl-.md)
</dt> </dl>

 

 





