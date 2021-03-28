---
title: endswitch (sm4-ASM)
description: Finaliza uma instrução switch.
ms.assetid: ECAEECFD-B955-4356-B5C9-1D6A04C71D8F
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 523a4008ab976ee299758349d57c6e32a3f336b2
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104365177"
---
# <a name="endswitch-sm4---asm"></a><span data-ttu-id="6a74b-103">endswitch (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="6a74b-103">endswitch (sm4 - asm)</span></span>

<span data-ttu-id="6a74b-104">Finaliza uma instrução [switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="6a74b-104">Ends a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="6a74b-105">troca de</span><span class="sxs-lookup"><span data-stu-id="6a74b-105">endswitch</span></span> |
|-----------|



 

## <a name="remarks"></a><span data-ttu-id="6a74b-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="6a74b-106">Remarks</span></span>

<span data-ttu-id="6a74b-107">O formato do token contém o deslocamento da instrução switch correspondente no sombreador como uma conveniência.</span><span class="sxs-lookup"><span data-stu-id="6a74b-107">The token format contains the offset of the corresponding switch instruction in the Shader as a convenience.</span></span>

<span data-ttu-id="6a74b-108">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="6a74b-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="6a74b-109">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="6a74b-109">Vertex Shader</span></span> | <span data-ttu-id="6a74b-110">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="6a74b-110">Geometry Shader</span></span> | <span data-ttu-id="6a74b-111">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="6a74b-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="6a74b-112">x</span><span class="sxs-lookup"><span data-stu-id="6a74b-112">x</span></span>             | <span data-ttu-id="6a74b-113">x</span><span class="sxs-lookup"><span data-stu-id="6a74b-113">x</span></span>               | <span data-ttu-id="6a74b-114">x</span><span class="sxs-lookup"><span data-stu-id="6a74b-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="6a74b-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="6a74b-115">Minimum Shader Model</span></span>

<span data-ttu-id="6a74b-116">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="6a74b-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="6a74b-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="6a74b-117">Shader Model</span></span>                                              | <span data-ttu-id="6a74b-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="6a74b-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="6a74b-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="6a74b-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="6a74b-120">sim</span><span class="sxs-lookup"><span data-stu-id="6a74b-120">yes</span></span>       |
| [<span data-ttu-id="6a74b-121">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="6a74b-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="6a74b-122">sim</span><span class="sxs-lookup"><span data-stu-id="6a74b-122">yes</span></span>       |
| [<span data-ttu-id="6a74b-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="6a74b-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="6a74b-124">sim</span><span class="sxs-lookup"><span data-stu-id="6a74b-124">yes</span></span>       |
| [<span data-ttu-id="6a74b-125">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a74b-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="6a74b-126">não</span><span class="sxs-lookup"><span data-stu-id="6a74b-126">no</span></span>        |
| [<span data-ttu-id="6a74b-127">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a74b-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="6a74b-128">não</span><span class="sxs-lookup"><span data-stu-id="6a74b-128">no</span></span>        |
| [<span data-ttu-id="6a74b-129">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a74b-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="6a74b-130">não</span><span class="sxs-lookup"><span data-stu-id="6a74b-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="6a74b-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="6a74b-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6a74b-132">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="6a74b-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




