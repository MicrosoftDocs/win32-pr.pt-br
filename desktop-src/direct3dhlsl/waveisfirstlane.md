---
title: Função WaveIsFirstLane
description: Retorna true somente para a pista ativa na onda atual com o menor índice.
ms.assetid: 5D90F713-08C7-4BD4-867B-2E7CA3A85E87
keywords:
- HLSL da função WaveIsFirstLane
topic_type:
- apiref
api_name:
- WaveIsFirstLane
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 49e875463d8281ff7e7699694c02d087df1a372f
ms.sourcegitcommit: f01bc6744cea55ad1aeeace7981a30b567e6fe60
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 11/04/2020
ms.locfileid: "104294607"
---
# <a name="waveisfirstlane-function"></a><span data-ttu-id="1c6f9-104">Função WaveIsFirstLane</span><span class="sxs-lookup"><span data-stu-id="1c6f9-104">WaveIsFirstLane function</span></span>

<span data-ttu-id="1c6f9-105">Retorna true somente para a pista ativa na onda atual com o menor índice.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-105">Returns true only for the active lane in the current wave with the smallest index.</span></span>

## <a name="syntax"></a><span data-ttu-id="1c6f9-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1c6f9-106">Syntax</span></span>


``` syntax
bool WaveIsFirstLane(void);
```



## <a name="parameters"></a><span data-ttu-id="1c6f9-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1c6f9-107">Parameters</span></span>

<span data-ttu-id="1c6f9-108">Essa função não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-108">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1c6f9-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="1c6f9-109">Return value</span></span>

<span data-ttu-id="1c6f9-110">True somente para a pista ativa na onda atual com o menor índice.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-110">True only for the active lane in the current wave with the smallest index.</span></span>

## <a name="remarks"></a><span data-ttu-id="1c6f9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1c6f9-111">Remarks</span></span>

<span data-ttu-id="1c6f9-112">Essa função pode ser usada para identificar as operações que devem ser executadas apenas uma vez por onda.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-112">This function can be used to identify operations that are to be executed only once per wave.</span></span>

<span data-ttu-id="1c6f9-113">Essa função tem suporte do modelo de sombreador 6,0 em todos os estágios de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1c6f9-113">This function is supported from shader model 6.0 in all shader stages.</span></span> 



 

## <a name="examples"></a><span data-ttu-id="1c6f9-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="1c6f9-114">Examples</span></span>

``` syntax
 if ( WaveIsFirstLane() )
{
    . . . // once per-wave code
}
```

## <a name="see-also"></a><span data-ttu-id="1c6f9-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="1c6f9-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1c6f9-116">Visão geral do modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="1c6f9-116">Overview of Shader Model 6</span></span>](hlsl-shader-model-6-0-features-for-direct3d-12.md)
</dt> <dt>

[<span data-ttu-id="1c6f9-117">Modelo do sombreador 6</span><span class="sxs-lookup"><span data-stu-id="1c6f9-117">Shader Model 6</span></span>](shader-model-6-0.md)
</dt> </dl>

 

 




