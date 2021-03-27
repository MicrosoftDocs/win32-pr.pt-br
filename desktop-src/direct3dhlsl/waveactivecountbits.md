---
title: Função WaveActiveCountBits
description: Conta o número de variáveis boolianas que são avaliadas como true em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda.
ms.assetid: 053E100C-7E09-4F9D-9F38-9D5E208A38CE
keywords:
- HLSL da função WaveActiveCountBits
topic_type:
- apiref
api_name:
- WaveActiveCountBits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4c4d2db55e9e3a0ad8f0a66be183d6e39d2a8b9c
ms.sourcegitcommit: a232805e6c618673f2df904111cc4f5a33e15504
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/07/2020
ms.locfileid: "104294637"
---
# <a name="waveactivecountbits-function"></a><span data-ttu-id="b7799-104">Função WaveActiveCountBits</span><span class="sxs-lookup"><span data-stu-id="b7799-104">WaveActiveCountBits function</span></span>

<span data-ttu-id="b7799-105">Conta o número de variáveis boolianas que são avaliadas como true em todas as pistas ativas na onda atual e replica o resultado para todas as pistas na onda.</span><span class="sxs-lookup"><span data-stu-id="b7799-105">Counts the number of boolean variables which evaluate to true across all active lanes in the current wave, and replicates the result to all lanes in the wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="b7799-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b7799-106">Syntax</span></span>


``` syntax
uint WaveActiveCountBits(
   bool bBit
);
```



## <a name="parameters"></a><span data-ttu-id="b7799-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b7799-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b7799-108">*bBit*</span><span class="sxs-lookup"><span data-stu-id="b7799-108">*bBit*</span></span> 
</dt> <dd>

<span data-ttu-id="b7799-109">As variáveis Booleanas a serem avaliadas.</span><span class="sxs-lookup"><span data-stu-id="b7799-109">The boolean variables to evaluate.</span></span> <span data-ttu-id="b7799-110">Fornecer um valor booliano verdadeiro explícito retorna o número de pistas ativas.</span><span class="sxs-lookup"><span data-stu-id="b7799-110">Providing an explicit true Boolean value returns the number of active lanes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b7799-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b7799-111">Return value</span></span>

<span data-ttu-id="b7799-112">O número de que é avaliado como true em todas as pistas ativas na onda atual.</span><span class="sxs-lookup"><span data-stu-id="b7799-112">The number of which evaluate to true across all active lanes in the current wave.</span></span>

## <a name="remarks"></a><span data-ttu-id="b7799-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="b7799-113">Remarks</span></span>

<span data-ttu-id="b7799-114">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="b7799-114">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="b7799-115">Exemplos</span><span class="sxs-lookup"><span data-stu-id="b7799-115">Examples</span></span>

<span data-ttu-id="b7799-116">Isso pode ser implementado com mais eficiência do que um WaveActiveSum completo, conforme descrito no exemplo a seguir:</span><span class="sxs-lookup"><span data-stu-id="b7799-116">This can be implemented more efficiently than a full WaveActiveSum, as described in the following example:</span></span>

``` syntax
result = WaveActiveCountBits( WaveActiveBallot( bBit ) );
```

## <a name="see-also"></a><span data-ttu-id="b7799-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="b7799-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b7799-118">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="b7799-118">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="b7799-119">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="b7799-119">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




