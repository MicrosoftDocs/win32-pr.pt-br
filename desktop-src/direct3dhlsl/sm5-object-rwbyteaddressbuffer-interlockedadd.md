---
title: 'Função RWByteAddressBuffer:: InterlockedAdd'
description: Adiciona o valor, atomicamente.
ms.assetid: 27274aae-1e75-4626-9997-57c4e9393000
keywords:
- HLSL da função InterlockedAdd
topic_type:
- apiref
api_name:
- InterlockedAdd
api_location:
- winnt.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d352ed97df15ce076c10950c6da94aaeaff0f2d0
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/20/2020
ms.locfileid: "104988666"
---
# <a name="interlockedadd-function"></a><span data-ttu-id="732fa-104">Função InterlockedAdd</span><span class="sxs-lookup"><span data-stu-id="732fa-104">InterlockedAdd function</span></span>

<span data-ttu-id="732fa-105">Adiciona o valor, atomicamente.</span><span class="sxs-lookup"><span data-stu-id="732fa-105">Adds the value, atomically.</span></span>

## <a name="syntax"></a><span data-ttu-id="732fa-106">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="732fa-106">Syntax</span></span>

``` syntax
void InterlockedAdd(
  in  UINT dest,
  in  UINT value,
  out UINT original_value
);
```

## <a name="parameters"></a><span data-ttu-id="732fa-107">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="732fa-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="732fa-108">*dest* \[ no\]</span><span class="sxs-lookup"><span data-stu-id="732fa-108">*dest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="732fa-109">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="732fa-109">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="732fa-110">O endereço de destino.</span><span class="sxs-lookup"><span data-stu-id="732fa-110">The destination address.</span></span>

</dd> <dt>

<span data-ttu-id="732fa-111">*valor* \[ do no\]</span><span class="sxs-lookup"><span data-stu-id="732fa-111">*value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="732fa-112">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="732fa-112">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="732fa-113">O valor de entrada.</span><span class="sxs-lookup"><span data-stu-id="732fa-113">The input value.</span></span>

</dd> <dt>

<span data-ttu-id="732fa-114">*\_ valor original* \[\]</span><span class="sxs-lookup"><span data-stu-id="732fa-114">*original\_value* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="732fa-115">Tipo: **[ **uint**](/windows/desktop/WinProg/windows-data-types)**</span><span class="sxs-lookup"><span data-stu-id="732fa-115">Type: **[**UINT**](/windows/desktop/WinProg/windows-data-types)**</span></span>

<span data-ttu-id="732fa-116">O valor original.</span><span class="sxs-lookup"><span data-stu-id="732fa-116">The original value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="732fa-117">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="732fa-117">Return value</span></span>

<span data-ttu-id="732fa-118">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="732fa-118">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="732fa-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="732fa-119">Remarks</span></span>

<span data-ttu-id="732fa-120">Esta operação só pode ser executada em recursos tipados int ou uint e variáveis de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="732fa-120">This operation can be performed only on int or uint typed resources and shared memory variables.</span></span> <span data-ttu-id="732fa-121">Há três usos possíveis para essa função.</span><span class="sxs-lookup"><span data-stu-id="732fa-121">There are three possible uses for this function.</span></span> <span data-ttu-id="732fa-122">A primeira é quando R é um tipo de variável de memória compartilhada.</span><span class="sxs-lookup"><span data-stu-id="732fa-122">The first is when R is a shared memory variable type.</span></span> <span data-ttu-id="732fa-123">Nesse caso, a função executa uma adição atômica de valor para o registro de memória compartilhada referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="732fa-123">In this case, the function performs an atomic add of value to the shared memory register referenced by dest.</span></span> <span data-ttu-id="732fa-124">O segundo cenário é quando R é um tipo de variável de recurso.</span><span class="sxs-lookup"><span data-stu-id="732fa-124">The second scenario is when R is a resource variable type.</span></span> <span data-ttu-id="732fa-125">Nesse cenário, a função executa uma adição atômica do valor para o local do recurso referenciado pelo dest.</span><span class="sxs-lookup"><span data-stu-id="732fa-125">In this scenario, the function performs an atomic add of the value to the resource location referenced by dest.</span></span> <span data-ttu-id="732fa-126">Por fim, o terceiro cenário é quando R é um tipo de variável local.</span><span class="sxs-lookup"><span data-stu-id="732fa-126">Finally, the third scenario is when R is a local variable type.</span></span> <span data-ttu-id="732fa-127">Nesse cenário, a função reduz para uma soma do valor de dest e Value, armazenado no dest.</span><span class="sxs-lookup"><span data-stu-id="732fa-127">In this scenario, the function reduces to a sum of the value of dest and value, stored in dest.</span></span> <span data-ttu-id="732fa-128">A função sobrecarregada tem uma variável de saída adicional que será definida com o valor original de dest.</span><span class="sxs-lookup"><span data-stu-id="732fa-128">The overloaded function has an additional output variable which will be set to the original value of dest.</span></span> <span data-ttu-id="732fa-129">Essa operação sobrecarregada só está disponível quando o R é legível e gravável.</span><span class="sxs-lookup"><span data-stu-id="732fa-129">This overloaded operation is only available when R is readable and writable.</span></span>

<span data-ttu-id="732fa-130">Essa função tem suporte nos seguintes tipos de sombreadores:</span><span class="sxs-lookup"><span data-stu-id="732fa-130">This function is supported in the following types of shaders:</span></span>



| <span data-ttu-id="732fa-131">VS</span><span class="sxs-lookup"><span data-stu-id="732fa-131">VS</span></span>  | <span data-ttu-id="732fa-132">HS</span><span class="sxs-lookup"><span data-stu-id="732fa-132">HS</span></span>  | <span data-ttu-id="732fa-133">DS</span><span class="sxs-lookup"><span data-stu-id="732fa-133">DS</span></span>  | <span data-ttu-id="732fa-134">GS</span><span class="sxs-lookup"><span data-stu-id="732fa-134">GS</span></span>  | <span data-ttu-id="732fa-135">PS</span><span class="sxs-lookup"><span data-stu-id="732fa-135">PS</span></span>  | <span data-ttu-id="732fa-136">CS</span><span class="sxs-lookup"><span data-stu-id="732fa-136">CS</span></span>  |
|-----|-----|-----|-----|-----|-----|
| <span data-ttu-id="732fa-137">x</span><span class="sxs-lookup"><span data-stu-id="732fa-137">x</span></span>   | <span data-ttu-id="732fa-138">x</span><span class="sxs-lookup"><span data-stu-id="732fa-138">x</span></span>   | <span data-ttu-id="732fa-139">x</span><span class="sxs-lookup"><span data-stu-id="732fa-139">x</span></span>   | <span data-ttu-id="732fa-140">x</span><span class="sxs-lookup"><span data-stu-id="732fa-140">x</span></span>   | <span data-ttu-id="732fa-141">x</span><span class="sxs-lookup"><span data-stu-id="732fa-141">x</span></span>   | <span data-ttu-id="732fa-142">x</span><span class="sxs-lookup"><span data-stu-id="732fa-142">x</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="732fa-143">Requisitos</span><span class="sxs-lookup"><span data-stu-id="732fa-143">Requirements</span></span>




## <a name="see-also"></a><span data-ttu-id="732fa-144">Confira também</span><span class="sxs-lookup"><span data-stu-id="732fa-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="732fa-145">RWByteAddressBuffer</span><span class="sxs-lookup"><span data-stu-id="732fa-145">RWByteAddressBuffer</span></span>](sm5-object-rwbyteaddressbuffer.md)
</dt> <dt>

[<span data-ttu-id="732fa-146">Modelo de sombreador 5</span><span class="sxs-lookup"><span data-stu-id="732fa-146">Shader Model 5</span></span>](d3d11-graphics-reference-sm5.md)
</dt> </dl>

 

