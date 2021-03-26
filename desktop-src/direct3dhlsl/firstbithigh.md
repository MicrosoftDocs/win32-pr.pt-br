---
title: Função firstbithigh
description: Obtém o local do primeiro bit de conjunto começando do bit de ordem mais alto e trabalhando para baixo, por componente.
ms.assetid: 0fa89a9e-1706-44f7-8dd3-c37af5c11ddc
keywords:
- HLSL da função firstbithigh
topic_type:
- apiref
api_name:
- firstbithigh
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 4da4956aa3a12d064566a3767423f42039b01355
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366200"
---
# <a name="firstbithigh-function"></a><span data-ttu-id="4142f-104">Função firstbithigh</span><span class="sxs-lookup"><span data-stu-id="4142f-104">firstbithigh function</span></span>

<span data-ttu-id="4142f-105">Obtém o local do primeiro bit de conjunto começando do bit de ordem mais alto e trabalhando para baixo, por componente.</span><span class="sxs-lookup"><span data-stu-id="4142f-105">Gets the location of the first set bit starting from the highest order bit and working downward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="4142f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4142f-106">Syntax</span></span>

``` syntax
int firstbithigh(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="4142f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4142f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4142f-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="4142f-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4142f-109">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4142f-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4142f-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="4142f-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4142f-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="4142f-111">Return value</span></span>

<span data-ttu-id="4142f-112">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="4142f-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="4142f-113">O local do primeiro bit definido.</span><span class="sxs-lookup"><span data-stu-id="4142f-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="4142f-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4142f-114">Remarks</span></span>

<span data-ttu-id="4142f-115">Para um inteiro assinado, o primeiro bit significativo é zero para um número negativo.</span><span class="sxs-lookup"><span data-stu-id="4142f-115">For a signed integer, the first significant bit is zero for a negative number.</span></span>

<span data-ttu-id="4142f-116">As seguintes versões sobrecarregadas também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="4142f-116">The following overloaded versions are also available:</span></span>

``` syntax
int2 firstbithigh(int2 value);
int3 firstbithigh(int3 value);
int4 firstbithigh(int4 value);
uint firstbithigh(uint value);
uint2 firstbithigh(uint2 value);
uint3 firstbithigh(uint3 value);
uint4 firstbithigh(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="4142f-117">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="4142f-117">Minimum Shader Model</span></span>

<span data-ttu-id="4142f-118">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="4142f-118">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="4142f-119">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="4142f-119">Shader Model</span></span>                                                                | <span data-ttu-id="4142f-120">Com suporte</span><span class="sxs-lookup"><span data-stu-id="4142f-120">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="4142f-121">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="4142f-121">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="4142f-122">sim</span><span class="sxs-lookup"><span data-stu-id="4142f-122">yes</span></span>       |



 

<span data-ttu-id="4142f-123">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="4142f-123">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="4142f-124">Vértice</span><span class="sxs-lookup"><span data-stu-id="4142f-124">Vertex</span></span> | <span data-ttu-id="4142f-125">Envoltória</span><span class="sxs-lookup"><span data-stu-id="4142f-125">Hull</span></span> | <span data-ttu-id="4142f-126">Domínio</span><span class="sxs-lookup"><span data-stu-id="4142f-126">Domain</span></span> | <span data-ttu-id="4142f-127">Geometria</span><span class="sxs-lookup"><span data-stu-id="4142f-127">Geometry</span></span> | <span data-ttu-id="4142f-128">16x16</span><span class="sxs-lookup"><span data-stu-id="4142f-128">Pixel</span></span> | <span data-ttu-id="4142f-129">Computação</span><span class="sxs-lookup"><span data-stu-id="4142f-129">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="4142f-130">x</span><span class="sxs-lookup"><span data-stu-id="4142f-130">x</span></span>      | <span data-ttu-id="4142f-131">x</span><span class="sxs-lookup"><span data-stu-id="4142f-131">x</span></span>    | <span data-ttu-id="4142f-132">x</span><span class="sxs-lookup"><span data-stu-id="4142f-132">x</span></span>      | <span data-ttu-id="4142f-133">x</span><span class="sxs-lookup"><span data-stu-id="4142f-133">x</span></span>        | <span data-ttu-id="4142f-134">x</span><span class="sxs-lookup"><span data-stu-id="4142f-134">x</span></span>     | <span data-ttu-id="4142f-135">x</span><span class="sxs-lookup"><span data-stu-id="4142f-135">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="4142f-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="4142f-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4142f-137">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="4142f-137">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="4142f-138">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="4142f-138">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 