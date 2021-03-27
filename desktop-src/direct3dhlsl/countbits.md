---
title: Função countbits
description: Conta o número de bits (por componente) no número inteiro de entrada.
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
ms.openlocfilehash: 60d3cd63502c6217e6fb0b0ff17685b2d2b5bf25
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 10/25/2019
ms.locfileid: "104006680"
---
# <a name="countbits-function"></a><span data-ttu-id="3fa6a-104">Função countbits</span><span class="sxs-lookup"><span data-stu-id="3fa6a-104">countbits function</span></span>

<span data-ttu-id="3fa6a-105">Conta o número de bits (por componente) no número inteiro de entrada.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-105">Counts the number of bits (per component) in the input integer.</span></span>

## <a name="syntax"></a><span data-ttu-id="3fa6a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3fa6a-106">Syntax</span></span>

``` syntax
uint countbits(
  in uint value
);
```

## <a name="parameters"></a><span data-ttu-id="3fa6a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3fa6a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3fa6a-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3fa6a-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3fa6a-109">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3fa6a-109">Type: **uint**</span></span>

<span data-ttu-id="3fa6a-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3fa6a-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3fa6a-111">Return value</span></span>

<span data-ttu-id="3fa6a-112">Tipo: **uint**</span><span class="sxs-lookup"><span data-stu-id="3fa6a-112">Type: **uint**</span></span>

<span data-ttu-id="3fa6a-113">O número de bits.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-113">The number of bits.</span></span>

## <a name="remarks"></a><span data-ttu-id="3fa6a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="3fa6a-114">Remarks</span></span>

<span data-ttu-id="3fa6a-115">As seguintes versões sobrecarregadas também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="3fa6a-115">The following overloaded versions are also available:</span></span>

``` syntax
uint count_bits(uint value);
uint2 count_bits(uint2 value);
uint3 count_bits(uint3 value);
uint4 count_bits(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="3fa6a-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="3fa6a-116">Minimum Shader Model</span></span>

<span data-ttu-id="3fa6a-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="3fa6a-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="3fa6a-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="3fa6a-118">Shader Model</span></span>                                                                | <span data-ttu-id="3fa6a-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="3fa6a-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="3fa6a-120">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="3fa6a-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="3fa6a-121">sim</span><span class="sxs-lookup"><span data-stu-id="3fa6a-121">yes</span></span>       |



 

<span data-ttu-id="3fa6a-122">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3fa6a-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3fa6a-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="3fa6a-123">Vertex</span></span> | <span data-ttu-id="3fa6a-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="3fa6a-124">Hull</span></span> | <span data-ttu-id="3fa6a-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="3fa6a-125">Domain</span></span> | <span data-ttu-id="3fa6a-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="3fa6a-126">Geometry</span></span> | <span data-ttu-id="3fa6a-127">16x16</span><span class="sxs-lookup"><span data-stu-id="3fa6a-127">Pixel</span></span> | <span data-ttu-id="3fa6a-128">Computação</span><span class="sxs-lookup"><span data-stu-id="3fa6a-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="3fa6a-129">x</span><span class="sxs-lookup"><span data-stu-id="3fa6a-129">x</span></span>      | <span data-ttu-id="3fa6a-130">x</span><span class="sxs-lookup"><span data-stu-id="3fa6a-130">x</span></span>    | <span data-ttu-id="3fa6a-131">x</span><span class="sxs-lookup"><span data-stu-id="3fa6a-131">x</span></span>      | <span data-ttu-id="3fa6a-132">x</span><span class="sxs-lookup"><span data-stu-id="3fa6a-132">x</span></span>        | <span data-ttu-id="3fa6a-133">x</span><span class="sxs-lookup"><span data-stu-id="3fa6a-133">x</span></span>     | <span data-ttu-id="3fa6a-134">x</span><span class="sxs-lookup"><span data-stu-id="3fa6a-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="3fa6a-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fa6a-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fa6a-136">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="3fa6a-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="3fa6a-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3fa6a-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




