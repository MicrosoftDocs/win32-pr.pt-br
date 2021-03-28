---
title: Função WaveActiveBallot
description: Retorna um uint4 contendo uma bitmask da avaliação da expressão booliana para todas as pistas ativas na onda atual.
ms.assetid: 67FE28E0-F397-431A-8CF8-64E4AD88CDBC
keywords:
- HLSL da função WaveActiveBallot
topic_type:
- apiref
api_name:
- WaveActiveBallot
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: e3cdd89fad7da1e4ba7f3d5e032370834166a114
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104499185"
---
# <a name="waveactiveballot-function"></a><span data-ttu-id="1a304-104">Função WaveActiveBallot</span><span class="sxs-lookup"><span data-stu-id="1a304-104">WaveActiveBallot function</span></span>

<span data-ttu-id="1a304-105">Retorna um uint4 contendo uma bitmask da avaliação da expressão booliana para todas as pistas ativas na onda atual.</span><span class="sxs-lookup"><span data-stu-id="1a304-105">Returns a uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> 

## <a name="syntax"></a><span data-ttu-id="1a304-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1a304-106">Syntax</span></span>

``` syntax
uint4 WaveBallot(
   bool expr
);
```

## <a name="parameters"></a><span data-ttu-id="1a304-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1a304-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1a304-108">*expr*</span><span class="sxs-lookup"><span data-stu-id="1a304-108">*expr*</span></span> 
</dt> <dd>

<span data-ttu-id="1a304-109">A expressão booliana a ser avaliada.</span><span class="sxs-lookup"><span data-stu-id="1a304-109">The boolean expression to evaluate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1a304-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1a304-110">Return value</span></span>

<span data-ttu-id="1a304-111">Um uint4 que contém um bitmask da avaliação da expressão booliana para todas as pistas ativas na onda atual.</span><span class="sxs-lookup"><span data-stu-id="1a304-111">A uint4 containing a bitmask of the evaluation of the Boolean expression for all active lanes in the current wave.</span></span> <span data-ttu-id="1a304-112">O bit menos significativo corresponde à pista com o índice zero.</span><span class="sxs-lookup"><span data-stu-id="1a304-112">The least-significant bit corresponds to the lane with index zero.</span></span> <span data-ttu-id="1a304-113">Os bits correspondentes a pistas inativas serão zero.</span><span class="sxs-lookup"><span data-stu-id="1a304-113">The bits corresponding to inactive lanes will be zero.</span></span> <span data-ttu-id="1a304-114">Os bits maiores ou iguais a [**WaveGetLaneCount**](wavegetlanecount.md) serão zero.</span><span class="sxs-lookup"><span data-stu-id="1a304-114">The bits that are greater than or equal to [**WaveGetLaneCount**](wavegetlanecount.md) will be zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="1a304-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="1a304-115">Remarks</span></span>

<span data-ttu-id="1a304-116">GPUs diferentes têm larguras de processador SIMD diferentes (contagens de raia).</span><span class="sxs-lookup"><span data-stu-id="1a304-116">Different GPUs have different SIMD processor widths (lane counts).</span></span> <span data-ttu-id="1a304-117">A maioria dessas funções do **WaveXXX** é capaz de operar no nível de abstração em que a largura da máquina SIMD é ocultada.</span><span class="sxs-lookup"><span data-stu-id="1a304-117">Most of these **WaveXXX** functions are able to operate at level of abstraction where SIMD machine width is concealed.</span></span> <span data-ttu-id="1a304-118">Para maximizar a portabilidade do código entre GPUs, use os intrínsecos que não dependem da largura da máquina.</span><span class="sxs-lookup"><span data-stu-id="1a304-118">To maximize portability of code across GPUs, use the intrinsics that don’t rely on machine width.</span></span> <span data-ttu-id="1a304-119">Por exemplo, use:</span><span class="sxs-lookup"><span data-stu-id="1a304-119">For example, use:</span></span>

``` syntax
uint result = WaveActiveCountBits( bBit );
```

<span data-ttu-id="1a304-120">Em vez de:</span><span class="sxs-lookup"><span data-stu-id="1a304-120">Instead of:</span></span>

``` syntax
uint result = countbits( WaveActiveBallot( bBit ) );
```

<span data-ttu-id="1a304-121">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1a304-121">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="1a304-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1a304-122">Examples</span></span>

``` syntax
// get a bitwise representation of the number of currently active lanes:
uint4 waveBits = WaveActiveBallot( true ); // convert to bits 
```

## <a name="see-also"></a><span data-ttu-id="1a304-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="1a304-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1a304-124">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="1a304-124">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="1a304-125">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="1a304-125">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




