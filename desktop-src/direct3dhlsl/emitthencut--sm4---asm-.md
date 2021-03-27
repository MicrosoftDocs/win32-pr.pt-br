---
title: emitThenCut (sm4-ASM)
description: Equivalente a um comando Emit seguido por um comando Cut. | emitThenCut (sm4-ASM)
ms.assetid: 80DE112A-790A-4DDF-A5BE-51F70BD7872C
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eb5b413ca11e22c7cfc17691fc0a39fe96bf7c0f
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "104298421"
---
# <a name="emitthencut-sm4---asm"></a><span data-ttu-id="f8e14-104">emitThenCut (sm4-ASM)</span><span class="sxs-lookup"><span data-stu-id="f8e14-104">emitThenCut (sm4 - asm)</span></span>

<span data-ttu-id="f8e14-105">Equivalente a um comando [Emit](emit--sm4---asm-.md) seguido por um comando [Cut](cut--sm4---asm-.md) .</span><span class="sxs-lookup"><span data-stu-id="f8e14-105">Equivalent to an [emit](emit--sm4---asm-.md) command followed by a [cut](cut--sm4---asm-.md) command.</span></span>



| <span data-ttu-id="f8e14-106">emitThenCut</span><span class="sxs-lookup"><span data-stu-id="f8e14-106">emitThenCut</span></span> |
|-------------|



 

## <a name="remarks"></a><span data-ttu-id="f8e14-107">Comentários</span><span class="sxs-lookup"><span data-stu-id="f8e14-107">Remarks</span></span>

<span data-ttu-id="f8e14-108">Esse comando é útil ao produzir a saída do último vértice em uma topologia de forma consciente.</span><span class="sxs-lookup"><span data-stu-id="f8e14-108">This command is useful when knowingly outputting the last vertex in a topology.</span></span>

<span data-ttu-id="f8e14-109">Se os fluxos tiverem sido declarados, você deverá usar o [ \_ fluxo emitthencut](emitthencut-stream--sm5---asm-.md).</span><span class="sxs-lookup"><span data-stu-id="f8e14-109">If streams have been declared, you must use [emitthencut\_stream](emitthencut-stream--sm5---asm-.md).</span></span>

<span data-ttu-id="f8e14-110">Essa instrução se aplica aos seguintes estágios de sombreador:</span><span class="sxs-lookup"><span data-stu-id="f8e14-110">This instruction applies to the following shader stages:</span></span>



| <span data-ttu-id="f8e14-111">Sombreador de vértice</span><span class="sxs-lookup"><span data-stu-id="f8e14-111">Vertex Shader</span></span> | <span data-ttu-id="f8e14-112">Sombreador de geometria</span><span class="sxs-lookup"><span data-stu-id="f8e14-112">Geometry Shader</span></span> | <span data-ttu-id="f8e14-113">Sombreador de pixel</span><span class="sxs-lookup"><span data-stu-id="f8e14-113">Pixel Shader</span></span> |
|---------------|-----------------|--------------|
|               | <span data-ttu-id="f8e14-114">x</span><span class="sxs-lookup"><span data-stu-id="f8e14-114">x</span></span>               |              |



 

## <a name="minimum-shader-model"></a><span data-ttu-id="f8e14-115">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="f8e14-115">Minimum Shader Model</span></span>

<span data-ttu-id="f8e14-116">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="f8e14-116">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="f8e14-117">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="f8e14-117">Shader Model</span></span>                                              | <span data-ttu-id="f8e14-118">Com suporte</span><span class="sxs-lookup"><span data-stu-id="f8e14-118">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="f8e14-119">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="f8e14-119">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="f8e14-120">sim</span><span class="sxs-lookup"><span data-stu-id="f8e14-120">yes</span></span>       |
| [<span data-ttu-id="f8e14-121">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="f8e14-121">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="f8e14-122">sim</span><span class="sxs-lookup"><span data-stu-id="f8e14-122">yes</span></span>       |
| [<span data-ttu-id="f8e14-123">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="f8e14-123">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="f8e14-124">sim</span><span class="sxs-lookup"><span data-stu-id="f8e14-124">yes</span></span>       |
| [<span data-ttu-id="f8e14-125">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8e14-125">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="f8e14-126">não</span><span class="sxs-lookup"><span data-stu-id="f8e14-126">no</span></span>        |
| [<span data-ttu-id="f8e14-127">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8e14-127">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="f8e14-128">não</span><span class="sxs-lookup"><span data-stu-id="f8e14-128">no</span></span>        |
| [<span data-ttu-id="f8e14-129">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8e14-129">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="f8e14-130">não</span><span class="sxs-lookup"><span data-stu-id="f8e14-130">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="f8e14-131">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="f8e14-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f8e14-132">Assembly do Shader Model 4 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="f8e14-132">Shader Model 4 Assembly (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm4-asm.md)
</dt> </dl>

 

 




