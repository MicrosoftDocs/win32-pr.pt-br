---
title: Função WaveGetLaneCount
description: Retorna o número de pistas em uma onda nessa arquitetura.
ms.assetid: 04059B5E-0F62-4623-84AD-E41FF7166B34
keywords:
- HLSL da função WaveGetLaneCount
topic_type:
- apiref
api_name:
- WaveGetLaneCount
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0bfdb3ce2dfde84b070fee57e7fc587a71d5f948
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104366924"
---
# <a name="wavegetlanecount-function"></a><span data-ttu-id="bf511-104">Função WaveGetLaneCount</span><span class="sxs-lookup"><span data-stu-id="bf511-104">WaveGetLaneCount function</span></span>

<span data-ttu-id="bf511-105">Retorna o número de pistas em uma onda nessa arquitetura.</span><span class="sxs-lookup"><span data-stu-id="bf511-105">Returns the number of lanes in a wave on this architecture.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf511-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf511-106">Syntax</span></span>

``` syntax
uint WaveGetLaneCount(void);
```

## <a name="parameters"></a><span data-ttu-id="bf511-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf511-107">Parameters</span></span>

<span data-ttu-id="bf511-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bf511-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bf511-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="bf511-109">Return value</span></span>

<span data-ttu-id="bf511-110">O resultado será entre 4 e 128 e incluirá todas as ondas: as pistas ativas, inativas e/ou auxiliares.</span><span class="sxs-lookup"><span data-stu-id="bf511-110">The result will be between 4 and 128, and includes all waves: active, inactive, and/or helper lanes.</span></span> <span data-ttu-id="bf511-111">O resultado retornado por essa função pode variar significativamente dependendo da implementação do driver.</span><span class="sxs-lookup"><span data-stu-id="bf511-111">The result returned from this function may vary significantly depending on the driver implementation.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf511-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf511-112">Remarks</span></span>

<span data-ttu-id="bf511-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="bf511-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="bf511-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="bf511-114">Examples</span></span>

``` syntax
 uint laneCount = WaveGetLaneCount();    // number of lanes in wave
```

## <a name="see-also"></a><span data-ttu-id="bf511-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf511-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf511-116">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="bf511-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="bf511-117">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="bf511-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




