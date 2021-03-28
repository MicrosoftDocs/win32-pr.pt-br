---
title: Saturação (referência de HLSL)
description: Coloca o resultado de uma operação aritmética de ponto flutuante de precisão simples ou dupla para \ 0,0 f... 1,0 f \ intervalo.
ms.assetid: ce3e79c7-c3e6-4a2c-910a-2cd568aece50
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- apiref
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 05b6048777ac7b6ecd2c4b59ff3c9e0287380949
ms.sourcegitcommit: cba7f424a292fd7f3a8518947b9466439b455419
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/23/2019
ms.locfileid: "104365325"
---
# <a name="saturate-hlsl-reference"></a><span data-ttu-id="fa768-103">Saturação (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa768-103">Saturate (HLSL reference)</span></span>

<span data-ttu-id="fa768-104">Coloca o resultado de uma operação aritmética de ponto flutuante de precisão única ou dupla para \[ 0,0 f... 1,0 intervalo de f \] .</span><span class="sxs-lookup"><span data-stu-id="fa768-104">Clamps the result of a single or double precision floating point arithmetic operation to \[0.0f...1.0f\] range.</span></span>



| <span data-ttu-id="fa768-105">\_saturação</span><span class="sxs-lookup"><span data-stu-id="fa768-105">\_sat</span></span> |
|-------|



 

<span data-ttu-id="fa768-106">O modificador de resultado de instrução **saturação** executa a seguinte operação nos valores de resultado de uma operação aritmética de ponto flutuante que se comparou \_ com ela:</span><span class="sxs-lookup"><span data-stu-id="fa768-106">The **saturate** instruction result modifier performs the following operation on the result values(s) from a floating point arithmetic operation that has \_sat applied to it:</span></span>

`min(1.0f, max(0.0f, value))`

<span data-ttu-id="fa768-107">em que min () e Max () na expressão acima se comportam de forma que [mín](min--sm4---asm-.md)., [máx](max--sm4---asm-.md)., [DMín](dmin--sm5---asm-.md)ou [DMáx](dmax--sm5---asm-.md) operem.</span><span class="sxs-lookup"><span data-stu-id="fa768-107">where min() and max() in the above expression behave in the way [min](min--sm4---asm-.md), [max](max--sm4---asm-.md), [dmin](dmin--sm5---asm-.md), or [dmax](dmax--sm5---asm-.md) operate.</span></span>

<span data-ttu-id="fa768-108">`_sat(NaN)` Retorna 0, pelas regras para min e Max.</span><span class="sxs-lookup"><span data-stu-id="fa768-108">`_sat(NaN)` returns 0, by the rules for min and max.</span></span>

## <a name="minimum-shader-model"></a><span data-ttu-id="fa768-109">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="fa768-109">Minimum Shader Model</span></span>

<span data-ttu-id="fa768-110">Esse modificador tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fa768-110">This modifier is supported in the following shader models.</span></span>



| <span data-ttu-id="fa768-111">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="fa768-111">Shader Model</span></span>                                              | <span data-ttu-id="fa768-112">Com suporte</span><span class="sxs-lookup"><span data-stu-id="fa768-112">Supported</span></span> |
|-----------------------------------------------------------|-----------|
| [<span data-ttu-id="fa768-113">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fa768-113">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)        | <span data-ttu-id="fa768-114">sim</span><span class="sxs-lookup"><span data-stu-id="fa768-114">yes</span></span>       |
| [<span data-ttu-id="fa768-115">Modelo do sombreador 4,1</span><span class="sxs-lookup"><span data-stu-id="fa768-115">Shader Model 4.1</span></span>](dx-graphics-hlsl-sm4.md)              | <span data-ttu-id="fa768-116">sim</span><span class="sxs-lookup"><span data-stu-id="fa768-116">yes</span></span>       |
| [<span data-ttu-id="fa768-117">Modelo de sombreador 4</span><span class="sxs-lookup"><span data-stu-id="fa768-117">Shader Model 4</span></span>](dx-graphics-hlsl-sm4.md)                | <span data-ttu-id="fa768-118">sim</span><span class="sxs-lookup"><span data-stu-id="fa768-118">yes</span></span>       |
| [<span data-ttu-id="fa768-119">Modelo de sombreador 3 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa768-119">Shader Model 3 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm3.md) | <span data-ttu-id="fa768-120">não</span><span class="sxs-lookup"><span data-stu-id="fa768-120">no</span></span>        |
| [<span data-ttu-id="fa768-121">Modelo de sombreador 2 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa768-121">Shader Model 2 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm2.md) | <span data-ttu-id="fa768-122">não</span><span class="sxs-lookup"><span data-stu-id="fa768-122">no</span></span>        |
| [<span data-ttu-id="fa768-123">Modelo de sombreador 1 (DirectX HLSL)</span><span class="sxs-lookup"><span data-stu-id="fa768-123">Shader Model 1 (DirectX HLSL)</span></span>](dx-graphics-hlsl-sm1.md) | <span data-ttu-id="fa768-124">não</span><span class="sxs-lookup"><span data-stu-id="fa768-124">no</span></span>        |



 

## <a name="related-topics"></a><span data-ttu-id="fa768-125">Tópicos relacionados</span><span class="sxs-lookup"><span data-stu-id="fa768-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="fa768-126">Modificadores de instrução</span><span class="sxs-lookup"><span data-stu-id="fa768-126">Instruction Modifiers</span></span>](instruction-modifiers.md)
</dt> </dl>

 

 




