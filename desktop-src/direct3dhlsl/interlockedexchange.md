---
title: Função InterlockedExchange (referência de HLSL)
description: Atribui o valor ao dest e retorna o valor original.
ms.assetid: 1e7ce7ff-9e23-47fa-8e76-713f6bf57abf
keywords:
- HLSL da função InterlockedExchange
topic_type:
- apiref
api_name:
- InterlockedExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 7c39dc4f68429fa3f070d446f998fd528a99af01
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104967158"
---
# <a name="interlockedexchange-function-hlsl-reference"></a><span data-ttu-id="92a12-104">Função InterlockedExchange (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="92a12-104">InterlockedExchange function (HLSL reference)</span></span>

<span data-ttu-id="92a12-105">Atribui o valor ao dest e retorna o valor original.</span><span class="sxs-lookup"><span data-stu-id="92a12-105">Assigns value to dest and returns the original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="92a12-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="92a12-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="92a12-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="92a12-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92a12-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="92a12-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a12-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="92a12-109">Type: **R**</span></span>

<span data-ttu-id="92a12-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="92a12-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="92a12-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="92a12-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92a12-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="92a12-112">Type: **T**</span></span>

<span data-ttu-id="92a12-113">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="92a12-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="92a12-114">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="92a12-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="92a12-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="92a12-115">Type: **T**</span></span>

<span data-ttu-id="92a12-116">O valor original.</span><span class="sxs-lookup"><span data-stu-id="92a12-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92a12-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="92a12-117">Return value</span></span>

<span data-ttu-id="92a12-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="92a12-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="92a12-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="92a12-119">Remarks</span></span>

<span data-ttu-id="92a12-120">Esta operação só pode ser executada em recursos de tipo escalar e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="92a12-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="92a12-121">Há dois usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="92a12-121">There are two possible uses for this function.</span></span> <span data-ttu-id="92a12-122">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="92a12-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="92a12-123">Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="92a12-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="92a12-124">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="92a12-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="92a12-125">Nesse cenário, a função executa a operação no local do recurso referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="92a12-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="92a12-126">Esta operação só está disponível quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="92a12-126">This operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="92a12-127">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="92a12-127">Minimum Shader Model</span></span>

<span data-ttu-id="92a12-128">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="92a12-128">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="92a12-129">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="92a12-129">Shader Model</span></span>                                                                | <span data-ttu-id="92a12-130">Com suporte</span><span class="sxs-lookup"><span data-stu-id="92a12-130">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="92a12-131">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="92a12-131">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="92a12-132">sim</span><span class="sxs-lookup"><span data-stu-id="92a12-132">yes</span></span>       |



 

<span data-ttu-id="92a12-133">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="92a12-133">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="92a12-134">Vértice</span><span class="sxs-lookup"><span data-stu-id="92a12-134">Vertex</span></span> | <span data-ttu-id="92a12-135">Envoltória</span><span class="sxs-lookup"><span data-stu-id="92a12-135">Hull</span></span> | <span data-ttu-id="92a12-136">Domínio</span><span class="sxs-lookup"><span data-stu-id="92a12-136">Domain</span></span> | <span data-ttu-id="92a12-137">Geometria</span><span class="sxs-lookup"><span data-stu-id="92a12-137">Geometry</span></span> | <span data-ttu-id="92a12-138">16x16</span><span class="sxs-lookup"><span data-stu-id="92a12-138">Pixel</span></span> | <span data-ttu-id="92a12-139">Computação</span><span class="sxs-lookup"><span data-stu-id="92a12-139">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="92a12-140">x</span><span class="sxs-lookup"><span data-stu-id="92a12-140">x</span></span>      |  <span data-ttu-id="92a12-141">x</span><span class="sxs-lookup"><span data-stu-id="92a12-141">x</span></span>   | <span data-ttu-id="92a12-142">x</span><span class="sxs-lookup"><span data-stu-id="92a12-142">x</span></span>      |  <span data-ttu-id="92a12-143">x</span><span class="sxs-lookup"><span data-stu-id="92a12-143">x</span></span>       | <span data-ttu-id="92a12-144">x</span><span class="sxs-lookup"><span data-stu-id="92a12-144">x</span></span>     | <span data-ttu-id="92a12-145">x</span><span class="sxs-lookup"><span data-stu-id="92a12-145">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="92a12-146">Confira também</span><span class="sxs-lookup"><span data-stu-id="92a12-146">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92a12-147">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="92a12-147">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="92a12-148">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="92a12-148">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




