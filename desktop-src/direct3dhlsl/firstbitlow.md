---
title: Função firstbitlow
description: Retorna o local do primeiro bit definido começando do bit mais baixo e trabalhando para cima, por componente.
ms.assetid: 204250f3-1a9b-445d-bd16-4cc9a5d9d60a
keywords:
- HLSL da função firstbitlow
topic_type:
- apiref
api_name:
- firstbitlow
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a647314383bc022b7c3b3e1b5a255a42a099c620
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104007741"
---
# <a name="firstbitlow-function"></a><span data-ttu-id="56b20-104">Função firstbitlow</span><span class="sxs-lookup"><span data-stu-id="56b20-104">firstbitlow function</span></span>

<span data-ttu-id="56b20-105">Retorna o local do primeiro bit definido começando do bit mais baixo e trabalhando para cima, por componente.</span><span class="sxs-lookup"><span data-stu-id="56b20-105">Returns the location of the first set bit starting from the lowest order bit and working upward, per component.</span></span>

## <a name="syntax"></a><span data-ttu-id="56b20-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="56b20-106">Syntax</span></span>

``` syntax
int firstbitlow(
  in int value
);
```

## <a name="parameters"></a><span data-ttu-id="56b20-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="56b20-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="56b20-108">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="56b20-108">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="56b20-109">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="56b20-109">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="56b20-110">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="56b20-110">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="56b20-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="56b20-111">Return value</span></span>

<span data-ttu-id="56b20-112">Tipo: **[ **int**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="56b20-112">Type: **[**int**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="56b20-113">O local do primeiro bit definido.</span><span class="sxs-lookup"><span data-stu-id="56b20-113">The location of the first set bit.</span></span>

## <a name="remarks"></a><span data-ttu-id="56b20-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="56b20-114">Remarks</span></span>

<span data-ttu-id="56b20-115">As seguintes versões sobrecarregadas também estão disponíveis:</span><span class="sxs-lookup"><span data-stu-id="56b20-115">The following overloaded versions are also available:</span></span>

``` syntax
uint2 firstbitlow(uint2 value);
uint3 firstbitlow(uint3 value);
uint4 firstbitlow(uint4 value);
```

### <a name="minimum-shader-model"></a><span data-ttu-id="56b20-116">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="56b20-116">Minimum Shader Model</span></span>

<span data-ttu-id="56b20-117">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="56b20-117">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="56b20-118">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="56b20-118">Shader Model</span></span>                                                                | <span data-ttu-id="56b20-119">Com suporte</span><span class="sxs-lookup"><span data-stu-id="56b20-119">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="56b20-120">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="56b20-120">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="56b20-121">sim</span><span class="sxs-lookup"><span data-stu-id="56b20-121">yes</span></span>       |



 

<span data-ttu-id="56b20-122">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="56b20-122">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="56b20-123">Vértice</span><span class="sxs-lookup"><span data-stu-id="56b20-123">Vertex</span></span> | <span data-ttu-id="56b20-124">Envoltória</span><span class="sxs-lookup"><span data-stu-id="56b20-124">Hull</span></span> | <span data-ttu-id="56b20-125">Domínio</span><span class="sxs-lookup"><span data-stu-id="56b20-125">Domain</span></span> | <span data-ttu-id="56b20-126">Geometria</span><span class="sxs-lookup"><span data-stu-id="56b20-126">Geometry</span></span> | <span data-ttu-id="56b20-127">16x16</span><span class="sxs-lookup"><span data-stu-id="56b20-127">Pixel</span></span> | <span data-ttu-id="56b20-128">Computação</span><span class="sxs-lookup"><span data-stu-id="56b20-128">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="56b20-129">x</span><span class="sxs-lookup"><span data-stu-id="56b20-129">x</span></span>      | <span data-ttu-id="56b20-130">x</span><span class="sxs-lookup"><span data-stu-id="56b20-130">x</span></span>    | <span data-ttu-id="56b20-131">x</span><span class="sxs-lookup"><span data-stu-id="56b20-131">x</span></span>      | <span data-ttu-id="56b20-132">x</span><span class="sxs-lookup"><span data-stu-id="56b20-132">x</span></span>        | <span data-ttu-id="56b20-133">x</span><span class="sxs-lookup"><span data-stu-id="56b20-133">x</span></span>     | <span data-ttu-id="56b20-134">x</span><span class="sxs-lookup"><span data-stu-id="56b20-134">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="56b20-135">Confira também</span><span class="sxs-lookup"><span data-stu-id="56b20-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="56b20-136">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="56b20-136">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="56b20-137">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="56b20-137">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 