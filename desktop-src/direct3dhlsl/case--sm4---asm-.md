---
title: caso (sm4-ASM)
description: Um rótulo em uma instrução switch.
ms.assetid: 456BB918-327E-4E15-8D38-F53850CAF666
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0278b8492575b1ef54fd64fc24b031fdec6cfb21
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967105"
---
# <a name="case-sm4---asm"></a><span data-ttu-id="12a0c-103">caso (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="12a0c-103">case (sm4 - asm)</span></span>

<span data-ttu-id="12a0c-104">Um rótulo em uma instrução switch.</span><span class="sxs-lookup"><span data-stu-id="12a0c-104">A label in a switch instruction.</span></span>



| <span data-ttu-id="12a0c-105">caso \[ 32-bit imediato\]</span><span class="sxs-lookup"><span data-stu-id="12a0c-105">case \[32-bit immediate\]</span></span> |
|---------------------------|



 

## <a name="remarks"></a><span data-ttu-id="12a0c-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="12a0c-106">Remarks</span></span>

<span data-ttu-id="12a0c-107">Como os **casos** de queda são válidos somente se não houver nenhum código adicionado, vários **casos** (incluindo o [padrão](default--sm4---asm-.md)) podem compartilhar o mesmo bloco de código.</span><span class="sxs-lookup"><span data-stu-id="12a0c-107">Because falling through **cases** is valid only if there is no code added, multiple **cases** (including [default](default--sm4---asm-.md)) can share the same code block.</span></span>

<span data-ttu-id="12a0c-108">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="12a0c-108">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="12a0c-109">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="12a0c-109">Vertex Shader</span></span> | <span data-ttu-id="12a0c-110">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="12a0c-110">Geometry Shader</span></span> | <span data-ttu-id="12a0c-111">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="12a0c-111">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="12a0c-112">x</span><span class="sxs-lookup"><span data-stu-id="12a0c-112">x</span></span>             | <span data-ttu-id="12a0c-113">x</span><span class="sxs-lookup"><span data-stu-id="12a0c-113">x</span></span>               | <span data-ttu-id="12a0c-114">x</span><span class="sxs-lookup"><span data-stu-id="12a0c-114">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="12a0c-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="12a0c-115">Minimum Shader Model</span></span>

<span data-ttu-id="12a0c-116">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="12a0c-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="12a0c-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="12a0c-117">Shader Model</span></span>                                              | <span data-ttu-id="12a0c-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="12a0c-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="12a0c-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="12a0c-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="12a0c-120">sim</span><span class="sxs-lookup"><span data-stu-id="12a0c-120">yes</span></span>       |
| [<span data-ttu-id="12a0c-121">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="12a0c-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="12a0c-122">sim</span><span class="sxs-lookup"><span data-stu-id="12a0c-122">yes</span></span>       |
| [<span data-ttu-id="12a0c-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="12a0c-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="12a0c-124">sim</span><span class="sxs-lookup"><span data-stu-id="12a0c-124">yes</span></span>       |
| [<span data-ttu-id="12a0c-125">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12a0c-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="12a0c-126">não</span><span class="sxs-lookup"><span data-stu-id="12a0c-126">no</span></span>        |
| [<span data-ttu-id="12a0c-127">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12a0c-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="12a0c-128">não</span><span class="sxs-lookup"><span data-stu-id="12a0c-128">no</span></span>        |
| [<span data-ttu-id="12a0c-129">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12a0c-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="12a0c-130">não</span><span class="sxs-lookup"><span data-stu-id="12a0c-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="12a0c-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="12a0c-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="12a0c-132">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="12a0c-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




