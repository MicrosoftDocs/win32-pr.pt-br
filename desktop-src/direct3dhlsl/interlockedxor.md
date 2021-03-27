---
title: Função InterlockedXor (referência de HLSL)
description: Executa um XOR atômico garantido.
ms.assetid: 844ca31f-d051-4713-b9e1-dd6712ad36ca
keywords:
- HLSL da função InterlockedXor
topic_type:
- apiref
api_name:
- InterlockedXor
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: b8ecaf0aa78a3bd2c1d79d10bea1e97299605398
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "103639094"
---
# <a name="interlockedxor-function-hlsl-reference"></a><span data-ttu-id="1b7d4-104">Função InterlockedXor (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="1b7d4-104">InterlockedXor function (HLSL reference)</span></span>

<span data-ttu-id="1b7d4-105">Executa um XOR atômico garantido.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-105">Performs a guaranteed atomic xor.</span></span>

## <a name="syntax"></a><span data-ttu-id="1b7d4-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1b7d4-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="1b7d4-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1b7d4-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1b7d4-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="1b7d4-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7d4-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="1b7d4-109">Type: **R**</span></span>

<span data-ttu-id="1b7d4-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="1b7d4-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="1b7d4-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7d4-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="1b7d4-112">Type: **T**</span></span>

<span data-ttu-id="1b7d4-113">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="1b7d4-114">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="1b7d4-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1b7d4-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="1b7d4-115">Type: **T**</span></span>

<span data-ttu-id="1b7d4-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-116">Optional.</span></span> <span data-ttu-id="1b7d4-117">O valor de entrada original.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1b7d4-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1b7d4-118">Return value</span></span>

<span data-ttu-id="1b7d4-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="1b7d4-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="1b7d4-120">Remarks</span></span>

<span data-ttu-id="1b7d4-121">Esta operação só pode ser executada em recursos tipados int ou uint e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-121">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="1b7d4-122">Há dois usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-122">There are two possible uses for this function.</span></span> <span data-ttu-id="1b7d4-123">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="1b7d4-124">Nesse caso, a função executa um XOR atômico de valor para o registro de memória compartilhada referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-124">In this case, the function performs an atomic XOR of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="1b7d4-125">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="1b7d4-126">Nesse cenário, a função executa um valor XORof atômico para o local do recurso referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-126">In this scenario, the function performs an atomic XORof value to the resource location referenced by dest.</span></span> <span data-ttu-id="1b7d4-127">A função sobrecarregada tem uma variável de saída adicional que será definida com o valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="1b7d4-128">Essa operação sobrecarregada só está disponível quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="1b7d4-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="1b7d4-129">Minimum Shader Model</span></span>

<span data-ttu-id="1b7d4-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="1b7d4-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="1b7d4-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="1b7d4-131">Shader Model</span></span>                                                                | <span data-ttu-id="1b7d4-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="1b7d4-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="1b7d4-133">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="1b7d4-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="1b7d4-134">sim</span><span class="sxs-lookup"><span data-stu-id="1b7d4-134">yes</span></span>       |



 

<span data-ttu-id="1b7d4-135">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="1b7d4-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="1b7d4-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="1b7d4-136">Vertex</span></span> | <span data-ttu-id="1b7d4-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="1b7d4-137">Hull</span></span> | <span data-ttu-id="1b7d4-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="1b7d4-138">Domain</span></span> | <span data-ttu-id="1b7d4-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="1b7d4-139">Geometry</span></span> | <span data-ttu-id="1b7d4-140">16x16</span><span class="sxs-lookup"><span data-stu-id="1b7d4-140">Pixel</span></span> | <span data-ttu-id="1b7d4-141">Computação</span><span class="sxs-lookup"><span data-stu-id="1b7d4-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="1b7d4-142">x</span><span class="sxs-lookup"><span data-stu-id="1b7d4-142">x</span></span>     |  <span data-ttu-id="1b7d4-143">x</span><span class="sxs-lookup"><span data-stu-id="1b7d4-143">x</span></span>   | <span data-ttu-id="1b7d4-144">x</span><span class="sxs-lookup"><span data-stu-id="1b7d4-144">x</span></span>      |  <span data-ttu-id="1b7d4-145">x</span><span class="sxs-lookup"><span data-stu-id="1b7d4-145">x</span></span>       | <span data-ttu-id="1b7d4-146">x</span><span class="sxs-lookup"><span data-stu-id="1b7d4-146">x</span></span>     | <span data-ttu-id="1b7d4-147">x</span><span class="sxs-lookup"><span data-stu-id="1b7d4-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="1b7d4-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="1b7d4-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1b7d4-149">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="1b7d4-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="1b7d4-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="1b7d4-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




