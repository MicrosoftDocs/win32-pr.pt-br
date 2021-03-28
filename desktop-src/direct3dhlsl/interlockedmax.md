---
title: Função InterlockedMax (referência de HLSL)
description: Executa um Atomic Max garantido.
ms.assetid: ea2c67ef-3133-424d-9cc3-81da79aee87e
keywords:
- HLSL da função InterlockedMax
topic_type:
- apiref
api_name:
- InterlockedMax
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 997641b086625532b99e3ae8d17be49cd71ae21f
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104365457"
---
# <a name="interlockedmax-function-hlsl-reference"></a><span data-ttu-id="fad5a-104">Função InterlockedMax (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="fad5a-104">InterlockedMax function (HLSL reference)</span></span>

<span data-ttu-id="fad5a-105">Executa um Atomic Max garantido.</span><span class="sxs-lookup"><span data-stu-id="fad5a-105">Performs a guaranteed atomic max.</span></span>

## <a name="syntax"></a><span data-ttu-id="fad5a-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fad5a-106">Syntax</span></span>

``` syntax
void InterlockedMax(
  in  R dest,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="fad5a-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fad5a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fad5a-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="fad5a-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad5a-109">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="fad5a-109">Type: **R**</span></span>

<span data-ttu-id="fad5a-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="fad5a-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="fad5a-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="fad5a-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="fad5a-112">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="fad5a-112">Type: **T**</span></span>

<span data-ttu-id="fad5a-113">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="fad5a-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="fad5a-114">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="fad5a-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fad5a-115">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="fad5a-115">Type: **T**</span></span>

<span data-ttu-id="fad5a-116">Opcional.</span><span class="sxs-lookup"><span data-stu-id="fad5a-116">Optional.</span></span> <span data-ttu-id="fad5a-117">O valor de entrada original.</span><span class="sxs-lookup"><span data-stu-id="fad5a-117">The original input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fad5a-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fad5a-118">Return value</span></span>

<span data-ttu-id="fad5a-119">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="fad5a-119">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="fad5a-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="fad5a-120">Remarks</span></span>

<span data-ttu-id="fad5a-121">Esta operação só pode ser executada em recursos tipados int e uint e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="fad5a-121">This operation can only be performed on int and uint typed resources and shared memory variables.</span></span> <span data-ttu-id="fad5a-122">Há dois usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="fad5a-122">There are two possible uses for this function.</span></span> <span data-ttu-id="fad5a-123">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="fad5a-123">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="fad5a-124">Nesse caso, a função executa um máximo atômico de valor para o registro de memória compartilhada referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="fad5a-124">In this case, the function performs an atomic max of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="fad5a-125">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="fad5a-125">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="fad5a-126">Nesse cenário, a função executa um máximo atômico de valor para o local do recurso referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="fad5a-126">In this scenario, the function performs an atomic max of value to the resource location referenced by dest.</span></span> <span data-ttu-id="fad5a-127">A função sobrecarregada tem uma variável de saída adicional que será definida com o valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="fad5a-127">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="fad5a-128">Essa operação sobrecarregada só está disponível quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="fad5a-128">This overloaded operation is only available when R is readable and writable.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="fad5a-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="fad5a-129">Minimum Shader Model</span></span>

<span data-ttu-id="fad5a-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="fad5a-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="fad5a-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="fad5a-131">Shader Model</span></span>                                                                | <span data-ttu-id="fad5a-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="fad5a-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="fad5a-133">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="fad5a-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="fad5a-134">sim</span><span class="sxs-lookup"><span data-stu-id="fad5a-134">yes</span></span>       |



 

<span data-ttu-id="fad5a-135">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="fad5a-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="fad5a-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="fad5a-136">Vertex</span></span> | <span data-ttu-id="fad5a-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="fad5a-137">Hull</span></span> | <span data-ttu-id="fad5a-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="fad5a-138">Domain</span></span> | <span data-ttu-id="fad5a-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="fad5a-139">Geometry</span></span> | <span data-ttu-id="fad5a-140">16x16</span><span class="sxs-lookup"><span data-stu-id="fad5a-140">Pixel</span></span> | <span data-ttu-id="fad5a-141">Computação</span><span class="sxs-lookup"><span data-stu-id="fad5a-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="fad5a-142">x</span><span class="sxs-lookup"><span data-stu-id="fad5a-142">x</span></span>      |  <span data-ttu-id="fad5a-143">x</span><span class="sxs-lookup"><span data-stu-id="fad5a-143">x</span></span>   |  <span data-ttu-id="fad5a-144">x</span><span class="sxs-lookup"><span data-stu-id="fad5a-144">x</span></span>     |  <span data-ttu-id="fad5a-145">x</span><span class="sxs-lookup"><span data-stu-id="fad5a-145">x</span></span>       | <span data-ttu-id="fad5a-146">x</span><span class="sxs-lookup"><span data-stu-id="fad5a-146">x</span></span>     | <span data-ttu-id="fad5a-147">x</span><span class="sxs-lookup"><span data-stu-id="fad5a-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="fad5a-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="fad5a-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fad5a-149">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="fad5a-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="fad5a-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="fad5a-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




