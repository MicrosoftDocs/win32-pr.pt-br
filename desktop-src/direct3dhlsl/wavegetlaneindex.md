---
title: Função WaveGetLaneIndex
description: Retorna o índice da pista atual dentro da onda atual.
ms.assetid: C05BD814-23DF-432F-8669-C03842B77AC7
keywords:
- HLSL da função WaveGetLaneIndex
topic_type:
- apiref
api_name:
- WaveGetLaneIndex
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 8adea1091739981523ab19b69158ead9aafa600c
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104988717"
---
# <a name="wavegetlaneindex-function"></a><span data-ttu-id="dd736-104">Função WaveGetLaneIndex</span><span class="sxs-lookup"><span data-stu-id="dd736-104">WaveGetLaneIndex function</span></span>

<span data-ttu-id="dd736-105">Retorna o índice da pista atual dentro da onda atual.</span><span class="sxs-lookup"><span data-stu-id="dd736-105">Returns the index of the current lane within the current wave.</span></span>

## <a name="syntax"></a><span data-ttu-id="dd736-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="dd736-106">Syntax</span></span>

``` syntax
uint WaveGetLaneIndex(void);
```

## <a name="parameters"></a><span data-ttu-id="dd736-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="dd736-107">Parameters</span></span>

<span data-ttu-id="dd736-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="dd736-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="dd736-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="dd736-109">Return value</span></span>

<span data-ttu-id="dd736-110">O índice de raia atual.</span><span class="sxs-lookup"><span data-stu-id="dd736-110">The current lane index.</span></span> <span data-ttu-id="dd736-111">O resultado será entre 0 e o resultado retornado de [**WaveGetLaneCount**](wavegetlanecount.md).</span><span class="sxs-lookup"><span data-stu-id="dd736-111">The result will be between 0 and the result returned from [**WaveGetLaneCount**](wavegetlanecount.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dd736-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="dd736-112">Remarks</span></span>

<span data-ttu-id="dd736-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="dd736-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="see-also"></a><span data-ttu-id="dd736-114">Confira também</span><span class="sxs-lookup"><span data-stu-id="dd736-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dd736-115">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="dd736-115">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="dd736-116">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="dd736-116">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




