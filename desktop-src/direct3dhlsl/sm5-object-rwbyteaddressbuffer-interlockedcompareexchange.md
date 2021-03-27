---
title: 'Função RWByteAddressBuffer:: InterlockedCompareExchange'
description: Compara a entrada com o valor de comparação e troca o resultado, atomicamente.
ms.assetid: 9d6e8d95-5157-49a7-8a79-f3ca6ba87ebb
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
ms.openlocfilehash: 18c7e5d58fe926d09e7ec48ee12a2336627d5db2
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103641560"
---
# <a name="interlockedcompareexchange-function"></a><span data-ttu-id="8484f-104">Função InterlockedCompareExchange</span><span class="sxs-lookup"><span data-stu-id="8484f-104">InterlockedCompareExchange function</span></span>

<span data-ttu-id="8484f-105">Compara a entrada com o valor de comparação e troca o resultado, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="8484f-105">Compares the input to the comparison value and exchanges the result, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="8484f-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8484f-106">Syntax</span></span>

``` syntax
void InterlockedCompareExchange(
  in  UINT dest,
  in  UINT compare_value,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="8484f-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8484f-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8484f-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="8484f-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8484f-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8484f-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8484f-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="8484f-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="8484f-111">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="8484f-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8484f-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8484f-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8484f-113">O valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="8484f-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="8484f-114">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="8484f-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8484f-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8484f-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8484f-116">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="8484f-116">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="8484f-117">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="8484f-117">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8484f-118">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="8484f-118">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="8484f-119">O valor original.</span><span class="sxs-lookup"><span data-stu-id="8484f-119">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8484f-120">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8484f-120">Return value</span></span>

<span data-ttu-id="8484f-121">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8484f-121">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8484f-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="8484f-122">Remarks</span></span>

<span data-ttu-id="8484f-123">Compara atomicamente o valor no *dest* para *comparar \_* o valor, armazena o valor no *dest* se os valores corresponderem, retorna o valor original do *dest* no *\_ valor original*.</span><span class="sxs-lookup"><span data-stu-id="8484f-123">Atomically compares the value in *dest* to *compare\_value*, stores value in *dest* if the values match, returns the original value of *dest* in *original\_value*.</span></span> <span data-ttu-id="8484f-124">Esta operação só pode ser executada em recursos tipados **int** ou *uint* e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="8484f-124">This operation can only be performed on **int** or *uint* typed resources and shared memory variables.</span></span> <span data-ttu-id="8484f-125">Há três usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="8484f-125">There are three possible uses for this function.</span></span> <span data-ttu-id="8484f-126">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="8484f-126">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="8484f-127">Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo *dest*.</span><span class="sxs-lookup"><span data-stu-id="8484f-127">In this case, the function performs the operation on the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="8484f-128">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="8484f-128">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="8484f-129">Nesse cenário, a função executa a operação no local do recurso referenciado pelo *dest*.</span><span class="sxs-lookup"><span data-stu-id="8484f-129">In this scenario, the function performs the operation on the resource location referenced by *dest*.</span></span> <span data-ttu-id="8484f-130">Por fim, o terceiro cenário é quando R é um tipo de variável local.</span><span class="sxs-lookup"><span data-stu-id="8484f-130">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="8484f-131">Nesse cenário, a função reduz para a operação executada usando operações locais.</span><span class="sxs-lookup"><span data-stu-id="8484f-131">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="8484f-132">Esta operação só está disponível quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="8484f-132">This operation is only available when R is readable and writable.</span></span>

> [!Note]  
> <span data-ttu-id="8484f-133">Se você chamar **InterlockedCompareExchange** em um loop [**for**](dx-graphics-hlsl-for.md) ou [**while**](dx-graphics-hlsl-while.md) Compute Shader, para compilar corretamente, você deverá usar o atributo **\[ Allow \_ UAV \_ Condition \]** nesse loop.</span><span class="sxs-lookup"><span data-stu-id="8484f-133">If you call **InterlockedCompareExchange** in a [**for**](dx-graphics-hlsl-for.md) or [**while**](dx-graphics-hlsl-while.md) compute shader loop, to properly compile, you must use the **\[allow\_uav\_condition\]** attribute on that loop.</span></span>

 

<span data-ttu-id="8484f-134">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="8484f-134">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="8484f-135">VS</span><span class="sxs-lookup"><span data-stu-id="8484f-135">VS</span></span>  | <span data-ttu-id="8484f-136">HS</span><span class="sxs-lookup"><span data-stu-id="8484f-136">HS</span></span>  | <span data-ttu-id="8484f-137">DS</span><span class="sxs-lookup"><span data-stu-id="8484f-137">DS</span></span>  | <span data-ttu-id="8484f-138">GS</span><span class="sxs-lookup"><span data-stu-id="8484f-138">GS</span></span>  | <span data-ttu-id="8484f-139">PS</span><span class="sxs-lookup"><span data-stu-id="8484f-139">PS</span></span>  | <span data-ttu-id="8484f-140">CS</span><span class="sxs-lookup"><span data-stu-id="8484f-140">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="8484f-141">x</span><span class="sxs-lookup"><span data-stu-id="8484f-141">x</span></span>   | <span data-ttu-id="8484f-142">x</span><span class="sxs-lookup"><span data-stu-id="8484f-142">x</span></span>   | <span data-ttu-id="8484f-143">x</span><span class="sxs-lookup"><span data-stu-id="8484f-143">x</span></span>   | <span data-ttu-id="8484f-144">x</span><span class="sxs-lookup"><span data-stu-id="8484f-144">x</span></span>   | <span data-ttu-id="8484f-145">x</span><span class="sxs-lookup"><span data-stu-id="8484f-145">x</span></span>   | <span data-ttu-id="8484f-146">x</span><span class="sxs-lookup"><span data-stu-id="8484f-146">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="8484f-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="8484f-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8484f-148">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="8484f-148">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="8484f-149">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="8484f-149">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 