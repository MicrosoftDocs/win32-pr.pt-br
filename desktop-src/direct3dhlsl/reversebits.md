---
title: Função reversebits
description: Reverte a ordem dos bits, por componente.
ms.assetid: dad46e25-9980-4645-98eb-d834db704fc8
keywords:
- HLSL da função reversebits
topic_type:
- apiref
api_name:
- reversebits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: d98b824883ddc4f06e6c11d30c2759bb0fc2be26
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104453775"
---
# <a name="reversebits-function"></a><span data-ttu-id="59fb2-104">Função reversebits</span><span class="sxs-lookup"><span data-stu-id="59fb2-104">reversebits function</span></span>

<span data-ttu-id="59fb2-105">Reverte a ordem dos bits, por componente.</span><span class="sxs-lookup"><span data-stu-id="59fb2-105">Reverses the order of the bits, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="59fb2-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="59fb2-106">Syntax</span></span>

``` syntax
uint reversebits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="59fb2-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="59fb2-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="59fb2-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="59fb2-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="59fb2-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="59fb2-109">Type: **uint**</span></span>

<span data-ttu-id="59fb2-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="59fb2-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="59fb2-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="59fb2-111">Return value</span></span>

<span data-ttu-id="59fb2-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="59fb2-112">Type: **uint**</span></span>

<span data-ttu-id="59fb2-113">O valor de entrada, com a ordem de bits invertida.</span><span class="sxs-lookup"><span data-stu-id="59fb2-113">The input value, with the bit order reversed.</span></span>

## <a name="remarks"></a><span data-ttu-id="59fb2-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="59fb2-114">Remarks</span></span>

<span data-ttu-id="59fb2-115">As seguintes versões sobrecarregadas também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="59fb2-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 reversebits(uint2 value);
uint3 reversebits(uint3 value);
uint4 reversebits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="59fb2-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="59fb2-116">Minimum Shader Model</span></span>

<span data-ttu-id="59fb2-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="59fb2-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="59fb2-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="59fb2-118">Shader Model</span></span>                                                                | <span data-ttu-id="59fb2-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="59fb2-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="59fb2-120">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="59fb2-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="59fb2-121">sim</span><span class="sxs-lookup"><span data-stu-id="59fb2-121">yes</span></span>       |



 

<span data-ttu-id="59fb2-122">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="59fb2-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="59fb2-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="59fb2-123">Vertex</span></span> | <span data-ttu-id="59fb2-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="59fb2-124">Hull</span></span> | <span data-ttu-id="59fb2-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="59fb2-125">Domain</span></span> | <span data-ttu-id="59fb2-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="59fb2-126">Geometry</span></span> | <span data-ttu-id="59fb2-127">16x16</span><span class="sxs-lookup"><span data-stu-id="59fb2-127">Pixel</span></span> | <span data-ttu-id="59fb2-128">Computação</span><span class="sxs-lookup"><span data-stu-id="59fb2-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="59fb2-129">x</span><span class="sxs-lookup"><span data-stu-id="59fb2-129">x</span></span>      | <span data-ttu-id="59fb2-130">x</span><span class="sxs-lookup"><span data-stu-id="59fb2-130">x</span></span>    | <span data-ttu-id="59fb2-131">x</span><span class="sxs-lookup"><span data-stu-id="59fb2-131">x</span></span>      | <span data-ttu-id="59fb2-132">x</span><span class="sxs-lookup"><span data-stu-id="59fb2-132">x</span></span>        | <span data-ttu-id="59fb2-133">x</span><span class="sxs-lookup"><span data-stu-id="59fb2-133">x</span></span>     | <span data-ttu-id="59fb2-134">x</span><span class="sxs-lookup"><span data-stu-id="59fb2-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="59fb2-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="59fb2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="59fb2-136">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="59fb2-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="59fb2-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="59fb2-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




