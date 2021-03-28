---
title: 'Função RWByteAddressBuffer:: InterlockedXor'
description: Executa um XOR atômico no valor.
ms.assetid: 692f8b5e-a81e-4700-8a8d-3594aba85671
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
ms.openlocfilehash: 920ae912c599b66a03a25d7bc8ecc9b199036b26
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "103917325"
---
# <a name="interlockedxor-function"></a><span data-ttu-id="3268b-104">Função InterlockedXor</span><span class="sxs-lookup"><span data-stu-id="3268b-104">InterlockedXor function</span></span>

<span data-ttu-id="3268b-105">Executa um **XOR** atômico no valor.</span><span class="sxs-lookup"><span data-stu-id="3268b-105">Performs an atomic **XOR** on the value.</span></span>

## <a name="syntax"></a><span data-ttu-id="3268b-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3268b-106">Syntax</span></span>

``` syntax
void InterlockedXor(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="3268b-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3268b-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3268b-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="3268b-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3268b-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3268b-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3268b-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="3268b-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="3268b-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="3268b-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3268b-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3268b-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3268b-113">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="3268b-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="3268b-114">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="3268b-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3268b-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="3268b-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="3268b-116">O valor original.</span><span class="sxs-lookup"><span data-stu-id="3268b-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3268b-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3268b-117">Return value</span></span>

<span data-ttu-id="3268b-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="3268b-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="3268b-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="3268b-119">Remarks</span></span>

<span data-ttu-id="3268b-120">Esta operação só pode ser executada em recursos tipados **int** ou **uint** e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="3268b-120">This operation can be performed only on **INT** or **UINT** typed resources and shared memory variables.</span></span> <span data-ttu-id="3268b-121">Há três usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="3268b-121">There are three possible uses for this function.</span></span> <span data-ttu-id="3268b-122">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="3268b-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="3268b-123">Nesse caso, a função executa um **XOR** atômico com o valor do registro de memória compartilhada referenciado pelo *dest*.</span><span class="sxs-lookup"><span data-stu-id="3268b-123">In this case, the function performs an atomic **XOR** with the value of the shared memory register referenced by *dest*.</span></span> <span data-ttu-id="3268b-124">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="3268b-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="3268b-125">Nesse cenário, a função executa um **XOR** atômico com o valor do local do recurso referenciado pelo *dest*.</span><span class="sxs-lookup"><span data-stu-id="3268b-125">In this scenario, the function performs an atomic **XOR** with the value of the resource location referenced by *dest*.</span></span> <span data-ttu-id="3268b-126">Por fim, o terceiro cenário é quando R é um tipo de variável local.</span><span class="sxs-lookup"><span data-stu-id="3268b-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="3268b-127">Nesse cenário, a função reduz para um **XOR** dos valores de *dest* e *Value*.</span><span class="sxs-lookup"><span data-stu-id="3268b-127">In this scenario, the function reduces to an **XOR** of the values of *dest* and *value*.</span></span> <span data-ttu-id="3268b-128">O resultado da operação substitui o valor no *dest*.</span><span class="sxs-lookup"><span data-stu-id="3268b-128">The result of the operation replaces the value in *dest*.</span></span> <span data-ttu-id="3268b-129">A função sobrecarregada tem uma variável de saída adicional que será definida com o valor original de *dest*.</span><span class="sxs-lookup"><span data-stu-id="3268b-129">The overloaded function has an additional output variable which will be set to the original value of *dest*.</span></span> <span data-ttu-id="3268b-130">Essa operação sobrecarregada está disponível somente quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="3268b-130">This overloaded operation is available only when R is readable and writable.</span></span>

<span data-ttu-id="3268b-131">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="3268b-131">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="3268b-132">VS</span><span class="sxs-lookup"><span data-stu-id="3268b-132">VS</span></span>  | <span data-ttu-id="3268b-133">HS</span><span class="sxs-lookup"><span data-stu-id="3268b-133">HS</span></span>  | <span data-ttu-id="3268b-134">DS</span><span class="sxs-lookup"><span data-stu-id="3268b-134">DS</span></span>  | <span data-ttu-id="3268b-135">GS</span><span class="sxs-lookup"><span data-stu-id="3268b-135">GS</span></span>  | <span data-ttu-id="3268b-136">PS</span><span class="sxs-lookup"><span data-stu-id="3268b-136">PS</span></span>  | <span data-ttu-id="3268b-137">CS</span><span class="sxs-lookup"><span data-stu-id="3268b-137">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="3268b-138">x</span><span class="sxs-lookup"><span data-stu-id="3268b-138">x</span></span>   |  <span data-ttu-id="3268b-139">x</span><span class="sxs-lookup"><span data-stu-id="3268b-139">x</span></span>  | <span data-ttu-id="3268b-140">x</span><span class="sxs-lookup"><span data-stu-id="3268b-140">x</span></span>   | <span data-ttu-id="3268b-141">x</span><span class="sxs-lookup"><span data-stu-id="3268b-141">x</span></span>   | <span data-ttu-id="3268b-142">x</span><span class="sxs-lookup"><span data-stu-id="3268b-142">x</span></span>   | <span data-ttu-id="3268b-143">x</span><span class="sxs-lookup"><span data-stu-id="3268b-143">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="3268b-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="3268b-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3268b-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="3268b-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="3268b-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="3268b-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 