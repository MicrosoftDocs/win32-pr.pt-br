---
title: Função InterlockedCompareStore (referência de HLSL)
description: Compara atomicamente o destino com o valor de comparação. Se forem idênticos, o destino será substituído pelo valor de entrada.
ms.assetid: eaf7e669-5240-40c9-9840-f4e7916e51b4
keywords:
- HLSL da função InterlockedCompareStore
topic_type:
- apiref
api_name:
- InterlockedCompareStore
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: df3ffb51bbe8fe8150d19a390e62640e64ded5c9
ms.sourcegitcommit: 12e9b14501d51641b690ee0cf764e2b91eb9a140
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/06/2020
ms.locfileid: "104365458"
---
# <a name="interlockedcomparestore-function-hlsl-reference"></a><span data-ttu-id="62c13-105">Função InterlockedCompareStore (referência de HLSL)</span><span class="sxs-lookup"><span data-stu-id="62c13-105">InterlockedCompareStore function (HLSL reference)</span></span>

<span data-ttu-id="62c13-106">Compara atomicamente o destino com o valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="62c13-106">Atomically compares the destination to the comparison value.</span></span> <span data-ttu-id="62c13-107">Se forem idênticos, o destino será substituído pelo valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="62c13-107">If they are identical, the destination is overwritten with the input value.</span></span>

## <a name="syntax"></a><span data-ttu-id="62c13-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="62c13-108">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in R dest,
  in T compare_value,
  in T value
);
```

## <a name="parameters"></a><span data-ttu-id="62c13-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="62c13-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62c13-110">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="62c13-110">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c13-111">Tipo: **R**</span><span class="sxs-lookup"><span data-stu-id="62c13-111">Type: **R**</span></span>

<span data-ttu-id="62c13-112">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="62c13-112">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="62c13-113">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="62c13-113">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c13-114">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="62c13-114">Type: **T**</span></span>

<span data-ttu-id="62c13-115">O valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="62c13-115">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="62c13-116">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="62c13-116">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62c13-117">Tipo: **T**</span><span class="sxs-lookup"><span data-stu-id="62c13-117">Type: **T**</span></span>

<span data-ttu-id="62c13-118">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="62c13-118">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62c13-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="62c13-119">Return value</span></span>

<span data-ttu-id="62c13-120">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="62c13-120">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="62c13-121">Comentários</span><span class="sxs-lookup"><span data-stu-id="62c13-121">Remarks</span></span>

<span data-ttu-id="62c13-122">Compara atomicamente o valor referenciado pelo *dest* com o *\_ valor de comparação* e armazena o *valor* no local referenciado pelo *dest* se os valores correspondem.</span><span class="sxs-lookup"><span data-stu-id="62c13-122">Atomically compares the value referenced by *dest* with *compare\_value* and stores *value* in the location referenced by *dest* if the values match.</span></span> <span data-ttu-id="62c13-123">Esta operação só pode ser executada em recursos tipados **int** ou **uint** e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="62c13-123">This operation can only be performed on **int** or **uint** typed resources and shared memory variables.</span></span> <span data-ttu-id="62c13-124">Há dois usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="62c13-124">There are two possible uses for this function.</span></span> <span data-ttu-id="62c13-125">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="62c13-125">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="62c13-126">Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo *dest*.</span><span class="sxs-lookup"><span data-stu-id="62c13-126">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="62c13-127">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="62c13-127">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="62c13-128">Nesse cenário, a função executa a operação no local do recurso referenciado pelo *dest*.</span><span class="sxs-lookup"><span data-stu-id="62c13-128">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span>

### <a name="minimum-shader-model"></a><span data-ttu-id="62c13-129">Modelo de sombreamento mínimo</span><span class="sxs-lookup"><span data-stu-id="62c13-129">Minimum Shader Model</span></span>

<span data-ttu-id="62c13-130">Essa função tem suporte nos seguintes modelos de sombreador.</span><span class="sxs-lookup"><span data-stu-id="62c13-130">This function is supported in the following shader models.</span></span>



| <span data-ttu-id="62c13-131">Modelo de Sombreador</span><span class="sxs-lookup"><span data-stu-id="62c13-131">Shader Model</span></span>                                                                | <span data-ttu-id="62c13-132">Com suporte</span><span class="sxs-lookup"><span data-stu-id="62c13-132">Supported</span></span> |
|-----------------------------------------------------------------------------|-----------|
| <span data-ttu-id="62c13-133">[Modelo](d3d11-graphics-reference-sm5.md) de sombreador 5 e modelos de sombreador mais altos</span><span class="sxs-lookup"><span data-stu-id="62c13-133">[Shader Model 5](d3d11-graphics-reference-sm5.md) and higher shader models</span></span> | <span data-ttu-id="62c13-134">sim</span><span class="sxs-lookup"><span data-stu-id="62c13-134">yes</span></span>       |



 

<span data-ttu-id="62c13-135">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="62c13-135">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="62c13-136">Vértice</span><span class="sxs-lookup"><span data-stu-id="62c13-136">Vertex</span></span> | <span data-ttu-id="62c13-137">Envoltória</span><span class="sxs-lookup"><span data-stu-id="62c13-137">Hull</span></span> | <span data-ttu-id="62c13-138">Domínio</span><span class="sxs-lookup"><span data-stu-id="62c13-138">Domain</span></span> | <span data-ttu-id="62c13-139">Geometria</span><span class="sxs-lookup"><span data-stu-id="62c13-139">Geometry</span></span> | <span data-ttu-id="62c13-140">16x16</span><span class="sxs-lookup"><span data-stu-id="62c13-140">Pixel</span></span> | <span data-ttu-id="62c13-141">Computação</span><span class="sxs-lookup"><span data-stu-id="62c13-141">Compute</span></span> |
|--------|------|--------|----------|-------|---------|
|  <span data-ttu-id="62c13-142">x</span><span class="sxs-lookup"><span data-stu-id="62c13-142">x</span></span>     | <span data-ttu-id="62c13-143">x</span><span class="sxs-lookup"><span data-stu-id="62c13-143">x</span></span>    |  <span data-ttu-id="62c13-144">x</span><span class="sxs-lookup"><span data-stu-id="62c13-144">x</span></span>     |  <span data-ttu-id="62c13-145">x</span><span class="sxs-lookup"><span data-stu-id="62c13-145">x</span></span>       | <span data-ttu-id="62c13-146">x</span><span class="sxs-lookup"><span data-stu-id="62c13-146">x</span></span>     | <span data-ttu-id="62c13-147">x</span><span class="sxs-lookup"><span data-stu-id="62c13-147">x</span></span>       |



 

## <a name="see-also"></a><span data-ttu-id="62c13-148">Confira também</span><span class="sxs-lookup"><span data-stu-id="62c13-148">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62c13-149">Funções intrínsecas</span><span class="sxs-lookup"><span data-stu-id="62c13-149">Intrinsic Functions</span></span>](dx-graphics-hlsl-intrinsic-functions.md)
</dt> <dt>

[<span data-ttu-id="62c13-150">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="62c13-150">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 




