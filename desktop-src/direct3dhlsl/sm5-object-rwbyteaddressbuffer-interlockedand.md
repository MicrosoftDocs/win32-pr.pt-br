---
title: 'Função RWByteAddressBuffer:: InterlockedAnd'
description: Ands o valor, atomicamente.
ms.assetid: c4024be0-3884-4af9-8075-76774c7c6178
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
ms.openlocfilehash: a389da886b193815c7d4b2c1fe0a86db1f068fc7
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104366195"
---
# <a name="interlockedand-function"></a><span data-ttu-id="692da-104">Função InterlockedAnd</span><span class="sxs-lookup"><span data-stu-id="692da-104">InterlockedAnd function</span></span>

<span data-ttu-id="692da-105">Ands o valor, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="692da-105">Ands the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="692da-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="692da-106">Syntax</span></span>

``` syntax
void InterlockedAnd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="692da-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="692da-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="692da-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="692da-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="692da-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="692da-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="692da-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="692da-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="692da-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="692da-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="692da-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="692da-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="692da-113">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="692da-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="692da-114">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="692da-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="692da-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="692da-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="692da-116">O valor original.</span><span class="sxs-lookup"><span data-stu-id="692da-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="692da-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="692da-117">Return value</span></span>

<span data-ttu-id="692da-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="692da-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="692da-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="692da-119">Remarks</span></span>

<span data-ttu-id="692da-120">Esta operação só pode ser executada em recursos tipados int ou uint e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="692da-120">This operation can only be performed on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="692da-121">Há três usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="692da-121">There are three possible uses for this function.</span></span> <span data-ttu-id="692da-122">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="692da-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="692da-123">Nesse caso, a função executa um Atomic e de valor para o registro de memória compartilhada referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="692da-123">In this case, the function performs an atomic and of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="692da-124">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="692da-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="692da-125">Nesse cenário, a função executa um Atomic e de valor para o local do recurso referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="692da-125">In this scenario, the function performs an atomic and of value to the resource location referenced by dest.</span></span> <span data-ttu-id="692da-126">Por fim, o terceiro cenário é quando R é um tipo de variável local.</span><span class="sxs-lookup"><span data-stu-id="692da-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="692da-127">Nesse cenário, a função reduz para um e do valor de dest e Value, armazenado no dest.</span><span class="sxs-lookup"><span data-stu-id="692da-127">In this scenario, the function reduces to an and of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="692da-128">A função sobrecarregada tem uma variável de saída adicional que será definida com o valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="692da-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="692da-129">Essa operação sobrecarregada só está disponível quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="692da-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="692da-130">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="692da-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="692da-131">VS</span><span class="sxs-lookup"><span data-stu-id="692da-131">VS</span></span>  | <span data-ttu-id="692da-132">HS</span><span class="sxs-lookup"><span data-stu-id="692da-132">HS</span></span>  | <span data-ttu-id="692da-133">DS</span><span class="sxs-lookup"><span data-stu-id="692da-133">DS</span></span>  | <span data-ttu-id="692da-134">GS</span><span class="sxs-lookup"><span data-stu-id="692da-134">GS</span></span>  | <span data-ttu-id="692da-135">PS</span><span class="sxs-lookup"><span data-stu-id="692da-135">PS</span></span>  | <span data-ttu-id="692da-136">CS</span><span class="sxs-lookup"><span data-stu-id="692da-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="692da-137">x</span><span class="sxs-lookup"><span data-stu-id="692da-137">x</span></span>   | <span data-ttu-id="692da-138">x</span><span class="sxs-lookup"><span data-stu-id="692da-138">x</span></span>   |  <span data-ttu-id="692da-139">x</span><span class="sxs-lookup"><span data-stu-id="692da-139">x</span></span>  | <span data-ttu-id="692da-140">x</span><span class="sxs-lookup"><span data-stu-id="692da-140">x</span></span>   | <span data-ttu-id="692da-141">x</span><span class="sxs-lookup"><span data-stu-id="692da-141">x</span></span>   | <span data-ttu-id="692da-142">x</span><span class="sxs-lookup"><span data-stu-id="692da-142">x</span></span>   |



 

## <a name="see-also"></a><span data-ttu-id="692da-143">Confira também</span><span class="sxs-lookup"><span data-stu-id="692da-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="692da-144">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="692da-144">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="692da-145">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="692da-145">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

 