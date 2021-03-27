---
title: 'Função RWByteAddressBuffer:: InterlockedExchange'
description: Troca um valor, atomicamente.
ms.assetid: a50f4cba-a7a2-44b0-9de7-003b4c7a947f
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
ms.openlocfilehash: 47c51374b7dcd62ac208e0aa8811a8d693ce0ac6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988651"
---
# <a name="interlockedexchange-function"></a><span data-ttu-id="da0dd-104">Função InterlockedExchange</span><span class="sxs-lookup"><span data-stu-id="da0dd-104">InterlockedExchange function</span></span>

<span data-ttu-id="da0dd-105">Troca um valor, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="da0dd-105">Exchanges a value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="da0dd-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="da0dd-106">Syntax</span></span>

``` syntax
void InterlockedExchange(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="da0dd-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="da0dd-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="da0dd-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="da0dd-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0dd-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="da0dd-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="da0dd-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="da0dd-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="da0dd-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="da0dd-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="da0dd-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="da0dd-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="da0dd-113">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="da0dd-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="da0dd-114">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="da0dd-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="da0dd-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="da0dd-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="da0dd-116">O valor original.</span><span class="sxs-lookup"><span data-stu-id="da0dd-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="da0dd-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="da0dd-117">Return value</span></span>

<span data-ttu-id="da0dd-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="da0dd-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="da0dd-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="da0dd-119">Remarks</span></span>

<span data-ttu-id="da0dd-120">Esta operação só pode ser executada em recursos de tipo escalar e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="da0dd-120">This operation can only be performed on scalar-typed resources and shared memory variables.</span></span> <span data-ttu-id="da0dd-121">Há três usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="da0dd-121">There are three possible uses for this function.</span></span> <span data-ttu-id="da0dd-122">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="da0dd-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="da0dd-123">Nesse caso, a função executa a operação no registro de memória compartilhada referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="da0dd-123">In this case, the function performs the operation on the shared memory register referenced by dest.</span></span> <span data-ttu-id="da0dd-124">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="da0dd-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="da0dd-125">Nesse cenário, a função executa a operação no local do recurso referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="da0dd-125">In this scenario, the function performs the operation on the resource location referenced by dest.</span></span> <span data-ttu-id="da0dd-126">Por fim, o terceiro cenário é quando R é um tipo de variável local.</span><span class="sxs-lookup"><span data-stu-id="da0dd-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="da0dd-127">Nesse cenário, a função reduz para a operação executada usando operações locais.</span><span class="sxs-lookup"><span data-stu-id="da0dd-127">In this scenario, the function reduces to the operation performed using local operations.</span></span> <span data-ttu-id="da0dd-128">Esta operação só está disponível quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="da0dd-128">This operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="da0dd-129">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="da0dd-129">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="da0dd-130">VS</span><span class="sxs-lookup"><span data-stu-id="da0dd-130">VS</span></span>  | <span data-ttu-id="da0dd-131">HS</span><span class="sxs-lookup"><span data-stu-id="da0dd-131">HS</span></span>  | <span data-ttu-id="da0dd-132">DS</span><span class="sxs-lookup"><span data-stu-id="da0dd-132">DS</span></span>  | <span data-ttu-id="da0dd-133">GS</span><span class="sxs-lookup"><span data-stu-id="da0dd-133">GS</span></span>  | <span data-ttu-id="da0dd-134">PS</span><span class="sxs-lookup"><span data-stu-id="da0dd-134">PS</span></span>  | <span data-ttu-id="da0dd-135">CS</span><span class="sxs-lookup"><span data-stu-id="da0dd-135">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
|  <span data-ttu-id="da0dd-136">x</span><span class="sxs-lookup"><span data-stu-id="da0dd-136">x</span></span>  |  <span data-ttu-id="da0dd-137">x</span><span class="sxs-lookup"><span data-stu-id="da0dd-137">x</span></span>  |  <span data-ttu-id="da0dd-138">x</span><span class="sxs-lookup"><span data-stu-id="da0dd-138">x</span></span>  |  <span data-ttu-id="da0dd-139">x</span><span class="sxs-lookup"><span data-stu-id="da0dd-139">x</span></span>  | <span data-ttu-id="da0dd-140">x</span><span class="sxs-lookup"><span data-stu-id="da0dd-140">x</span></span>   | <span data-ttu-id="da0dd-141">x</span><span class="sxs-lookup"><span data-stu-id="da0dd-141">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="da0dd-142">Confira também</span><span class="sxs-lookup"><span data-stu-id="da0dd-142">See also</span></span>

<dl> <dt>

[<span data-ttu-id="da0dd-143">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="da0dd-143">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="da0dd-144">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="da0dd-144">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 