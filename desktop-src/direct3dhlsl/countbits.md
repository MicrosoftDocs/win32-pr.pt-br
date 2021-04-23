---
title: Função countbits
description: Conta o número de bits (por componente) definido no número inteiro de entrada.
ms.assetid: c4fafbc8-e21c-48cb-b433-8241a989ec85
keywords:
- HLSL da função countbits
topic_type:
- apiref
api_name:
- countbits
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 357aceca6e2aea261a9e94212b58ff6308c99560
ms.sourcegitcommit: 435ea8f5bf06808ffa7dce39afb0ee6de842ba2f
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/23/2021
ms.locfileid: "107925619"
---
# <a name="countbits-function"></a><span data-ttu-id="218cf-104">Função countbits</span><span class="sxs-lookup"><span data-stu-id="218cf-104">countbits function</span></span>

<span data-ttu-id="218cf-105">Conta o número de bits (por componente) definido no número inteiro de entrada.</span><span class="sxs-lookup"><span data-stu-id="218cf-105">Counts the number of bits (per component) set in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="218cf-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="218cf-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="218cf-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="218cf-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="218cf-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="218cf-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="218cf-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="218cf-109">Type: **uint**</span></span>

<span data-ttu-id="218cf-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="218cf-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="218cf-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="218cf-111">Return value</span></span>

<span data-ttu-id="218cf-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="218cf-112">Type: **uint**</span></span>

<span data-ttu-id="218cf-113">O número de bits.</span><span class="sxs-lookup"><span data-stu-id="218cf-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="218cf-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="218cf-114">Remarks</span></span>

<span data-ttu-id="218cf-115">As seguintes versões sobrecarregadas também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="218cf-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="218cf-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="218cf-116">Minimum Shader Model</span></span>

<span data-ttu-id="218cf-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="218cf-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="218cf-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="218cf-118">Shader Model</span></span>                                                                | <span data-ttu-id="218cf-119">Suportado</span><span class="sxs-lookup"><span data-stu-id="218cf-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="218cf-120">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="218cf-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="218cf-121">sim</span><span class="sxs-lookup"><span data-stu-id="218cf-121">yes</span></span>       |



 

<span data-ttu-id="218cf-122">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="218cf-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="218cf-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="218cf-123">Vertex</span></span> | <span data-ttu-id="218cf-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="218cf-124">Hull</span></span> | <span data-ttu-id="218cf-125">Domain</span><span class="sxs-lookup"><span data-stu-id="218cf-125">Domain</span></span> | <span data-ttu-id="218cf-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="218cf-126">Geometry</span></span> | <span data-ttu-id="218cf-127">16x16</span><span class="sxs-lookup"><span data-stu-id="218cf-127">Pixel</span></span> | <span data-ttu-id="218cf-128">Computação</span><span class="sxs-lookup"><span data-stu-id="218cf-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="218cf-129">x</span><span class="sxs-lookup"><span data-stu-id="218cf-129">x</span></span>      | <span data-ttu-id="218cf-130">x</span><span class="sxs-lookup"><span data-stu-id="218cf-130">x</span></span>    | <span data-ttu-id="218cf-131">x</span><span class="sxs-lookup"><span data-stu-id="218cf-131">x</span></span>      | <span data-ttu-id="218cf-132">x</span><span class="sxs-lookup"><span data-stu-id="218cf-132">x</span></span>        | <span data-ttu-id="218cf-133">x</span><span class="sxs-lookup"><span data-stu-id="218cf-133">x</span></span>     | <span data-ttu-id="218cf-134">x</span><span class="sxs-lookup"><span data-stu-id="218cf-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="218cf-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="218cf-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="218cf-136">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="218cf-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="218cf-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="218cf-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




