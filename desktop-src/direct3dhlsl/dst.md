---
title: função de DST
description: Calcula um vetor de distância. | função de DST
ms.assetid: 24d22743-5867-49db-8d0a-55cc3625c947
keywords:
- função de DST HLSL
topic_type:
- apiref
api_name:
- dst
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 58ce243cf9a9f3e6118763368445e5bcf26ba4cc
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/09/2021
ms.locfileid: "103837742"
---
# <a name="dst-function"></a><span data-ttu-id="8c306-105">função de DST</span><span class="sxs-lookup"><span data-stu-id="8c306-105">dst function</span></span>

<span data-ttu-id="8c306-106">Calcula um vetor de distância.</span><span class="sxs-lookup"><span data-stu-id="8c306-106">Calculates a distance vector.</span></span>

## <a name="syntax"></a><span data-ttu-id="8c306-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8c306-107">Syntax</span></span>

``` syntax
fVector dst(
  in fVector src0,
  in fVector src1
);
```

## <a name="parameters"></a><span data-ttu-id="8c306-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8c306-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8c306-109">*src0* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c306-109">*src0* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c306-110">Tipo: **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="8c306-110">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="8c306-111">O primeiro vetor.</span><span class="sxs-lookup"><span data-stu-id="8c306-111">The first vector.</span></span>

</dd> <dt>

<span data-ttu-id="8c306-112">*src1* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8c306-112">*src1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8c306-113">Tipo: **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="8c306-113">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="8c306-114">O segundo vetor.</span><span class="sxs-lookup"><span data-stu-id="8c306-114">The second vector.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8c306-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8c306-115">Return value</span></span>

<span data-ttu-id="8c306-116">Tipo: **[fVector](dx-graphics-hlsl-vector.md)**</span><span class="sxs-lookup"><span data-stu-id="8c306-116">Type: **[fVector](dx-graphics-hlsl-vector.md)**</span></span>

<span data-ttu-id="8c306-117">O vetor de distância computada.</span><span class="sxs-lookup"><span data-stu-id="8c306-117">The computed distance vector.</span></span>

## <a name="remarks"></a><span data-ttu-id="8c306-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="8c306-118">Remarks</span></span>

<span data-ttu-id="8c306-119">Essa função intrínseca fornece a mesma funcionalidade que o [DST](dst---vs.md)de instrução do sombreador de vértice.</span><span class="sxs-lookup"><span data-stu-id="8c306-119">This intrinsic function provides the same functionality as the Vertex Shader instruction [dst](dst---vs.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="8c306-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="8c306-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8c306-121">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="8c306-121">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> </dl>

 

 




