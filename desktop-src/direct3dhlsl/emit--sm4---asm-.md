---
title: emissão (sm4-ASM)
description: Emitir um vértice.
ms.assetid: FDD18CCD-8088-46BD-897C-434B77FF81E6
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b17711b6f9cf5d707fb8eae3465100a78620c0c
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "103638854"
---
# <a name="emit-sm4---asm"></a><span data-ttu-id="82545-103">emissão (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="82545-103">emit (sm4 - asm)</span></span>

<span data-ttu-id="82545-104">Emitir um vértice.</span><span class="sxs-lookup"><span data-stu-id="82545-104">Emit a vertex.</span></span>



| <span data-ttu-id="82545-105">reflexão</span><span class="sxs-lookup"><span data-stu-id="82545-105">emit</span></span> |
|------|



 

## <a name="remarks"></a><span data-ttu-id="82545-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="82545-106">Remarks</span></span>

<span data-ttu-id="82545-107">**Emit** faz com que todos os registros de o declarados \# sejam lidos do sombreador de geometria para gerar um vértice.</span><span class="sxs-lookup"><span data-stu-id="82545-107">**emit** causes all declared o\# registers to be read out of the Geometry Shader to generate a vertex.</span></span>

<span data-ttu-id="82545-108">À medida que várias chamadas de **emissão** são emitidas, os primitivos são gerados.</span><span class="sxs-lookup"><span data-stu-id="82545-108">As multiple **emit** calls are issued, primitives are generated.</span></span>

<span data-ttu-id="82545-109">a **emissão** pode aparecer qualquer número de vezes em um sombreador de geometria, incluindo dentro do controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="82545-109">**emit** can appear any number of times in a Geometry Shader, including within flow control.</span></span>

<span data-ttu-id="82545-110">Se os fluxos tiverem sido declarados, você deverá usar o [ \_ fluxo de emissão](emit-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="82545-110">If streams have been declared, you must use [emit\_stream](emit-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="82545-111">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="82545-111">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="82545-112">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="82545-112">Vertex Shader</span></span> | <span data-ttu-id="82545-113">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="82545-113">Geometry Shader</span></span> | <span data-ttu-id="82545-114">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="82545-114">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="82545-115">x</span><span class="sxs-lookup"><span data-stu-id="82545-115">x</span></span>               |              |



 

### <a name="minimum-shader-model"></a><span data-ttu-id="82545-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="82545-116">Minimum Shader Model</span></span>

<span data-ttu-id="82545-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="82545-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="82545-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="82545-118">Shader Model</span></span>                                              | <span data-ttu-id="82545-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="82545-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="82545-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="82545-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="82545-121">sim</span><span class="sxs-lookup"><span data-stu-id="82545-121">yes</span></span>       |
| [<span data-ttu-id="82545-122">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="82545-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="82545-123">sim</span><span class="sxs-lookup"><span data-stu-id="82545-123">yes</span></span>       |
| [<span data-ttu-id="82545-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="82545-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="82545-125">sim</span><span class="sxs-lookup"><span data-stu-id="82545-125">yes</span></span>       |
| [<span data-ttu-id="82545-126">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82545-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="82545-127">não</span><span class="sxs-lookup"><span data-stu-id="82545-127">no</span></span>        |
| [<span data-ttu-id="82545-128">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82545-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="82545-129">não</span><span class="sxs-lookup"><span data-stu-id="82545-129">no</span></span>        |
| [<span data-ttu-id="82545-130">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82545-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="82545-131">não</span><span class="sxs-lookup"><span data-stu-id="82545-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="82545-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="82545-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="82545-133">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="82545-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




