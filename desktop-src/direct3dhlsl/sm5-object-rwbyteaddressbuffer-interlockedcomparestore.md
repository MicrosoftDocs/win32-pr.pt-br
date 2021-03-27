---
title: 'Função RWByteAddressBuffer:: InterlockedCompareStore'
description: Ccompares a entrada para o valor de comparação, atomicamente.
ms.assetid: d82a73b6-24a5-4eb3-9f20-15ba263c93d0
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
ms.openlocfilehash: abaa390ba74657e42b54a5147a7bc4006564a5fb
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103823900"
---
# <a name="interlockedcomparestore-function"></a><span data-ttu-id="980ea-104">Função InterlockedCompareStore</span><span class="sxs-lookup"><span data-stu-id="980ea-104">InterlockedCompareStore function</span></span>

<span data-ttu-id="980ea-105">Ccompares a entrada para o valor de comparação, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="980ea-105">Ccompares the input to the comparison value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="980ea-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="980ea-106">Syntax</span></span>

``` syntax
void InterlockedCompareStore(
  in UINT dest,
  in UINT compare_value,
  in UINT value
);
```

## <a name="parameters"></a><span data-ttu-id="980ea-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="980ea-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="980ea-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="980ea-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="980ea-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="980ea-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="980ea-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="980ea-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="980ea-111">*comparar \_ valor* \[ em\]</span><span class="sxs-lookup"><span data-stu-id="980ea-111">*compare\_value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="980ea-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="980ea-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="980ea-113">O valor de comparação.</span><span class="sxs-lookup"><span data-stu-id="980ea-113">The comparison value.</span></span>

</dd> <dt>

<span data-ttu-id="980ea-114">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="980ea-114">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="980ea-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="980ea-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="980ea-116">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="980ea-116">The input value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="980ea-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="980ea-117">Return value</span></span>

<span data-ttu-id="980ea-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="980ea-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="980ea-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="980ea-119">Remarks</span></span>

<span data-ttu-id="980ea-120">Esta operação só pode ser executada em recursos tipados int ou uint e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="980ea-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="980ea-121">Há três usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="980ea-121">There are three possible uses for this function.</span></span> <span data-ttu-id="980ea-122">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="980ea-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="980ea-123">Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="980ea-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="980ea-124">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="980ea-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="980ea-125">Nesse cenário, a função executa a operação no local do recurso referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="980ea-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="980ea-126">Por fim, o terceiro cenário é quando R é um tipo de variável local.</span><span class="sxs-lookup"><span data-stu-id="980ea-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="980ea-127">Nesse cenário, a função reduz para a operação executada usando operações locais.</span><span class="sxs-lookup"><span data-stu-id="980ea-127">In this scenario, the function reduces to the operation performed using local operations.</span></span>

<span data-ttu-id="980ea-128">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="980ea-128">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="980ea-129">VS</span><span class="sxs-lookup"><span data-stu-id="980ea-129">VS</span></span>  | <span data-ttu-id="980ea-130">HS</span><span class="sxs-lookup"><span data-stu-id="980ea-130">HS</span></span>  | <span data-ttu-id="980ea-131">DS</span><span class="sxs-lookup"><span data-stu-id="980ea-131">DS</span></span>  | <span data-ttu-id="980ea-132">GS</span><span class="sxs-lookup"><span data-stu-id="980ea-132">GS</span></span>  | <span data-ttu-id="980ea-133">PS</span><span class="sxs-lookup"><span data-stu-id="980ea-133">PS</span></span>  | <span data-ttu-id="980ea-134">CS</span><span class="sxs-lookup"><span data-stu-id="980ea-134">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="980ea-135">x</span><span class="sxs-lookup"><span data-stu-id="980ea-135">x</span></span>   | <span data-ttu-id="980ea-136">x</span><span class="sxs-lookup"><span data-stu-id="980ea-136">x</span></span>   | <span data-ttu-id="980ea-137">x</span><span class="sxs-lookup"><span data-stu-id="980ea-137">x</span></span>   | <span data-ttu-id="980ea-138">x</span><span class="sxs-lookup"><span data-stu-id="980ea-138">x</span></span>   | <span data-ttu-id="980ea-139">x</span><span class="sxs-lookup"><span data-stu-id="980ea-139">x</span></span>   | <span data-ttu-id="980ea-140">x</span><span class="sxs-lookup"><span data-stu-id="980ea-140">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="980ea-141">Confira também</span><span class="sxs-lookup"><span data-stu-id="980ea-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="980ea-142">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="980ea-142">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="980ea-143">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="980ea-143">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 