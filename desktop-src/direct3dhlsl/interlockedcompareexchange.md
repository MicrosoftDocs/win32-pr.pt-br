---
title: Função InterlockedCompareExchange (referência de HLSL)
description: Compara atomicamente o destino com o valor de comparação. Se forem idênticos, o destino será substituído pelo valor de entrada. O valor original é definido como o valor original do destino.
ms.assetid: 85d1ba58-8e79-41cd-abd6-7ffff59839c7
keywords:
- HLSL da função InterlockedCompareExchange
topic_type:
- apiref
api_name:
- InterlockedCompareExchange
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 74bc189996752d754599bf4547e8baa4d9fb74cc
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104988642"
---
# <a name="interlockedcompareexchange-function-hlsl-reference"></a><span data-ttu-id="45274-106">Função InterlockedCompareExchange (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="45274-106">InterlockedCompareExchange function (HLSL reference)</span></span>

<span data-ttu-id="45274-107">Compara atomicamente o destino com o valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="45274-107">Atomically compares the destination with the comparison value.</span></span> <span data-ttu-id="45274-108">Se forem idênticos, o destino será substituído pelo valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="45274-108">If they are identical, the destination is overwritten with the input value.</span></span> <span data-ttu-id="45274-109">O valor original é definido como o valor original do destino.</span><span class="sxs-lookup"><span data-stu-id="45274-109">The original value is set to the destination's original value.</span></span>

## <a name="syntax"></a><span data-ttu-id="45274-110">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45274-110">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  R dest,
  in  T compare_value,
  in  T value,
  out T original_value
);
```

## <a name="parameters"></a><span data-ttu-id="45274-111">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45274-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="45274-112">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="45274-112">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45274-113">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="45274-113">Type: **R**</span></span>

<span data-ttu-id="45274-114">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="45274-114">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="45274-115">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="45274-115">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45274-116">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="45274-116">Type: **T**</span></span>

<span data-ttu-id="45274-117">O valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="45274-117">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="45274-118">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="45274-118">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="45274-119">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="45274-119">Type: **T**</span></span>

<span data-ttu-id="45274-120">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="45274-120">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="45274-121">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="45274-121">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="45274-122">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="45274-122">Type: **T**</span></span>

<span data-ttu-id="45274-123">O valor original.</span><span class="sxs-lookup"><span data-stu-id="45274-123">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="45274-124">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45274-124">Return value</span></span>

<span data-ttu-id="45274-125">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="45274-125">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="45274-126">Comentários</span><span class="sxs-lookup"><span data-stu-id="45274-126">Remarks</span></span>

<span data-ttu-id="45274-127">Compara atomicamente o valor referenciado *pelo dest* com o *\_ valor de comparação* *, armazena o valor no* local referenciado pelo *dest* se os valores forem correspondentes, retorna o valor original do *dest* no *\_ valor original*.</span><span class="sxs-lookup"><span data-stu-id="45274-127">Atomically compares the value referenced by *dest* with *compare\_value*, stores *value* in the location referenced by *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="45274-128">Esta operação só pode ser executada em recursos tipados **int** ou **uint** e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="45274-128">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="45274-129">Há dois usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="45274-129">There are two possible uses for this function.</span></span> <span data-ttu-id="45274-130">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="45274-130">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="45274-131">Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo *dest*.</span><span class="sxs-lookup"><span data-stu-id="45274-131">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="45274-132">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="45274-132">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="45274-133">Nesse cenário, a função executa a operação no local do recurso referenciado pelo *dest*.</span><span class="sxs-lookup"><span data-stu-id="45274-133">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="45274-134">Esta operação só está disponível quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="45274-134">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="45274-135">Se você chamar **InterlockedCompareExchange** em um loop [**for**](dx-graphics-hlsl-for.md) ou [**while**](dx-graphics-hlsl-while.md) Compute Shader, para compilar corretamente, você deverá usar o atributo **\[ Allow \_ UAV \_ Condition \]** nesse loop.</span><span class="sxs-lookup"><span data-stu-id="45274-135">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

### <a name="minimum-shader-model"></a><span data-ttu-id="45274-136">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="45274-136">Minimum Shader Model</span></span>

<span data-ttu-id="45274-137">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="45274-137">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="45274-138">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="45274-138">Shader Model</span></span>                                                                | <span data-ttu-id="45274-139">Com suporte</span><span class="sxs-lookup"><span data-stu-id="45274-139">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="45274-140">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="45274-140">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="45274-141">sim</span><span class="sxs-lookup"><span data-stu-id="45274-141">yes</span></span>       |



 

<span data-ttu-id="45274-142">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="45274-142">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="45274-143">Vértice</span><span class="sxs-lookup"><span data-stu-id="45274-143">Vertex</span></span> | <span data-ttu-id="45274-144">Envoltória</span><span class="sxs-lookup"><span data-stu-id="45274-144">Hull</span></span> | <span data-ttu-id="45274-145">Domínio</span><span class="sxs-lookup"><span data-stu-id="45274-145">Domain</span></span> | <span data-ttu-id="45274-146">Geometria</span><span class="sxs-lookup"><span data-stu-id="45274-146">Geometry</span></span> | <span data-ttu-id="45274-147">16x16</span><span class="sxs-lookup"><span data-stu-id="45274-147">Pixel</span></span> | <span data-ttu-id="45274-148">Computação</span><span class="sxs-lookup"><span data-stu-id="45274-148">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
| <span data-ttu-id="45274-149">x</span><span class="sxs-lookup"><span data-stu-id="45274-149">x</span></span>      |  <span data-ttu-id="45274-150">x</span><span class="sxs-lookup"><span data-stu-id="45274-150">x</span></span>   |  <span data-ttu-id="45274-151">x</span><span class="sxs-lookup"><span data-stu-id="45274-151">x</span></span>     |  <span data-ttu-id="45274-152">x</span><span class="sxs-lookup"><span data-stu-id="45274-152">x</span></span>       | <span data-ttu-id="45274-153">x</span><span class="sxs-lookup"><span data-stu-id="45274-153">x</span></span>     | <span data-ttu-id="45274-154">x</span><span class="sxs-lookup"><span data-stu-id="45274-154">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="45274-155">Confira também</span><span class="sxs-lookup"><span data-stu-id="45274-155">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45274-156">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="45274-156">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="45274-157">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="45274-157">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




