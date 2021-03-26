---
title: Função InterlockedAnd (referência de HLSL)
description: Executa uma atomicidade garantida e.
ms.assetid: 7dc5185a-ea37-493d-975d-dbb803c886d3
keywords:
- HLSL da função InterlockedAnd
topic_type:
- apiref
api_name:
- InterlockedAnd
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 487a7daaffe25e4e8bb22aec5805ded2a8091161
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104988641"
---
# <a name="interlockedand-function-hlsl-reference"></a><span data-ttu-id="2dc4d-104">Função InterlockedAnd (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="2dc4d-104">InterlockedAnd function (HLSL reference)</span></span>

<span data-ttu-id="2dc4d-105">Executa uma atomicidade garantida e.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-105">Performs a guaranteed atomic and.</span></span>

## <a name="syntax"></a><span data-ttu-id="2dc4d-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2dc4d-106">Syntax</span></span>

``` syntax
void InterlockedAnd(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="2dc4d-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2dc4d-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2dc4d-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="2dc4d-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc4d-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="2dc4d-109">Type: **R**</span></span>

<span data-ttu-id="2dc4d-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="2dc4d-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="2dc4d-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc4d-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="2dc4d-112">Type: **T**</span></span>

<span data-ttu-id="2dc4d-113">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="2dc4d-114">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="2dc4d-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2dc4d-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="2dc4d-115">Type: **T**</span></span>

<span data-ttu-id="2dc4d-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-116">Optional.</span></span> <span data-ttu-id="2dc4d-117">O valor de entrada original.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2dc4d-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2dc4d-118">Return value</span></span>

<span data-ttu-id="2dc4d-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="2dc4d-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="2dc4d-120">Remarks</span></span>

<span data-ttu-id="2dc4d-121">Esta operação só pode ser executada em recursos tipados int ou uint e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="2dc4d-122">Há dois usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-122">There are two possible uses for this function.</span></span> <span data-ttu-id="2dc4d-123">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="2dc4d-124">Nesse caso, a função executa um Atomic e de valor para o registro de memória compartilhada referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-124">In this case, the function performs an atomic and of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="2dc4d-125">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="2dc4d-126">Nesse cenário, a função executa um Atomic e de valor para o local do recurso referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-126">In this scenario, the function performs an atomic and of value to the resource location referenced by dest.</span></span> <span data-ttu-id="2dc4d-127">A função sobrecarregada tem uma variável de saída adicional que será definida com o valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="2dc4d-128">Essa operação sobrecarregada só está disponível quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="2dc4d-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="2dc4d-129">Minimum Shader Model</span></span>

<span data-ttu-id="2dc4d-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="2dc4d-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="2dc4d-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="2dc4d-131">Shader Model</span></span>                                                                | <span data-ttu-id="2dc4d-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="2dc4d-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="2dc4d-133">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="2dc4d-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="2dc4d-134">sim</span><span class="sxs-lookup"><span data-stu-id="2dc4d-134">yes</span></span>       |



 

<span data-ttu-id="2dc4d-135">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="2dc4d-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="2dc4d-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="2dc4d-136">Vertex</span></span> | <span data-ttu-id="2dc4d-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="2dc4d-137">Hull</span></span> | <span data-ttu-id="2dc4d-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="2dc4d-138">Domain</span></span> | <span data-ttu-id="2dc4d-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="2dc4d-139">Geometry</span></span> | <span data-ttu-id="2dc4d-140">16x16</span><span class="sxs-lookup"><span data-stu-id="2dc4d-140">Pixel</span></span> | <span data-ttu-id="2dc4d-141">Computação</span><span class="sxs-lookup"><span data-stu-id="2dc4d-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="2dc4d-142">x</span><span class="sxs-lookup"><span data-stu-id="2dc4d-142">x</span></span>      |  <span data-ttu-id="2dc4d-143">x</span><span class="sxs-lookup"><span data-stu-id="2dc4d-143">x</span></span>   |  <span data-ttu-id="2dc4d-144">x</span><span class="sxs-lookup"><span data-stu-id="2dc4d-144">x</span></span>     |  <span data-ttu-id="2dc4d-145">x</span><span class="sxs-lookup"><span data-stu-id="2dc4d-145">x</span></span>       | <span data-ttu-id="2dc4d-146">x</span><span class="sxs-lookup"><span data-stu-id="2dc4d-146">x</span></span>     | <span data-ttu-id="2dc4d-147">x</span><span class="sxs-lookup"><span data-stu-id="2dc4d-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="2dc4d-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="2dc4d-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2dc4d-149">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="2dc4d-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="2dc4d-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="2dc4d-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




