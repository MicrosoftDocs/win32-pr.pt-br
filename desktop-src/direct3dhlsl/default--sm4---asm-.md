---
title: padrão (sm4-ASM)
description: Um rótulo opcional em uma instrução switch.
ms.assetid: DB10F654-4A98-4ED8-A3B4-CA9FE1DFE6CD
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b92364212e4d20a6e9229c057ba424f43f8f8556
ms.sourcegitcommit: fe03c5d92ca6a0d66a114b2303e99c0a19241ffb
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/20/2019
ms.locfileid: "104967097"
---
# <a name="default-sm4---asm"></a><span data-ttu-id="cf5dd-103">padrão (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="cf5dd-103">default (sm4 - asm)</span></span>

<span data-ttu-id="cf5dd-104">Um rótulo opcional em uma instrução [switch](switch--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="cf5dd-104">An optional label in a [switch](switch--sm4---asm-.md) statement.</span></span>



| <span data-ttu-id="cf5dd-105">padrão</span><span class="sxs-lookup"><span data-stu-id="cf5dd-105">default</span></span> |
|---------|



 

## <a name="remarks"></a><span data-ttu-id="cf5dd-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="cf5dd-106">Remarks</span></span>

<span data-ttu-id="cf5dd-107">Essa instrução funciona exatamente como o **padrão** em C. a passagem é válida somente se não houver nenhum código adicionado, de modo que vários casos (incluindo o **padrão**) possam compartilhar o mesmo bloco de código.</span><span class="sxs-lookup"><span data-stu-id="cf5dd-107">This instruction operates just like **default** in C. Falling through is valid only if there is no code added, so multiple cases (including **default**) can share the same code block.</span></span>

<span data-ttu-id="cf5dd-108">Apenas uma instrução **Default** é permitida em uma construção de **comutador** .</span><span class="sxs-lookup"><span data-stu-id="cf5dd-108">Only one **default** statement is permitted in a **switch** construct.</span></span>

<span data-ttu-id="cf5dd-109">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="cf5dd-109">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="cf5dd-110">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="cf5dd-110">Vertex Shader</span></span> | <span data-ttu-id="cf5dd-111">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="cf5dd-111">Geometry Shader</span></span> | <span data-ttu-id="cf5dd-112">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="cf5dd-112">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
| <span data-ttu-id="cf5dd-113">x</span><span class="sxs-lookup"><span data-stu-id="cf5dd-113">x</span></span>             | <span data-ttu-id="cf5dd-114">x</span><span class="sxs-lookup"><span data-stu-id="cf5dd-114">x</span></span>               | <span data-ttu-id="cf5dd-115">x</span><span class="sxs-lookup"><span data-stu-id="cf5dd-115">x</span></span>            |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="cf5dd-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="cf5dd-116">Minimum Shader Model</span></span>

<span data-ttu-id="cf5dd-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="cf5dd-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="cf5dd-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="cf5dd-118">Shader Model</span></span>                                              | <span data-ttu-id="cf5dd-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="cf5dd-119">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="cf5dd-120">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="cf5dd-120">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="cf5dd-121">sim</span><span class="sxs-lookup"><span data-stu-id="cf5dd-121">yes</span></span>       |
| [<span data-ttu-id="cf5dd-122">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="cf5dd-122">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="cf5dd-123">sim</span><span class="sxs-lookup"><span data-stu-id="cf5dd-123">yes</span></span>       |
| [<span data-ttu-id="cf5dd-124">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="cf5dd-124">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="cf5dd-125">sim</span><span class="sxs-lookup"><span data-stu-id="cf5dd-125">yes</span></span>       |
| [<span data-ttu-id="cf5dd-126">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf5dd-126">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="cf5dd-127">não</span><span class="sxs-lookup"><span data-stu-id="cf5dd-127">no</span></span>        |
| [<span data-ttu-id="cf5dd-128">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf5dd-128">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="cf5dd-129">não</span><span class="sxs-lookup"><span data-stu-id="cf5dd-129">no</span></span>        |
| [<span data-ttu-id="cf5dd-130">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf5dd-130">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="cf5dd-131">não</span><span class="sxs-lookup"><span data-stu-id="cf5dd-131">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="cf5dd-132">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="cf5dd-132">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cf5dd-133">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="cf5dd-133">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




