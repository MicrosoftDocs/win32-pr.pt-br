---
description: A função llMulDiv implementa a fórmula ((a \* b) + Rnd)/c, em que cada termo é um valor de 64 bits.
ms.assetid: cd5073b9-27c7-42ee-8487-2d4ea29f77d4
title: função llMulDiv (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Int64x32Div32
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e45d22eec1536517bd2b57d875dd596e4a1e28db
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780859"
---
# <a name="llmuldiv-function"></a><span data-ttu-id="9caf3-103">função llMulDiv</span><span class="sxs-lookup"><span data-stu-id="9caf3-103">llMulDiv function</span></span>

<span data-ttu-id="9caf3-104">A `llMulDiv` função implementa a fórmula `((a*b)+rnd)/c` em que cada termo é um valor de 64 bits.</span><span class="sxs-lookup"><span data-stu-id="9caf3-104">The `llMulDiv` function implements the formula `((a*b)+rnd)/c` where each term is a 64-bit value.</span></span>

<span data-ttu-id="9caf3-105">Carimbos de data/hora e tempos de busca são valores de 64 bits, portanto, essa função é útil para executar conversões em sistemas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9caf3-105">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="9caf3-106">Por exemplo, a fórmula para bytes por segundo é</span><span class="sxs-lookup"><span data-stu-id="9caf3-106">For example, the formula for bytes-per-second is</span></span>


```C++
(Number of Bytes * Reference Time) / 10,000,000
```



<span data-ttu-id="9caf3-107">que pode ser calculado como `llMulDiv(nBytes, rtTime, 10000000, 0)` .</span><span class="sxs-lookup"><span data-stu-id="9caf3-107">which can be calculated as `llMulDiv(nBytes, rtTime, 10000000, 0)`.</span></span> <span data-ttu-id="9caf3-108">Use o parâmetro *Rnd* como um fator de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="9caf3-108">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="syntax"></a><span data-ttu-id="9caf3-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9caf3-109">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONGLONG b,
   LONGLONG c,
   LONGLONG rnd
);
```



## <a name="parameters"></a><span data-ttu-id="9caf3-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9caf3-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9caf3-111">*um*</span><span class="sxs-lookup"><span data-stu-id="9caf3-111">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="9caf3-112">Multiplicando.</span><span class="sxs-lookup"><span data-stu-id="9caf3-112">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-113">*b*</span><span class="sxs-lookup"><span data-stu-id="9caf3-113">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="9caf3-114">Multiplicador.</span><span class="sxs-lookup"><span data-stu-id="9caf3-114">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-115">*c*</span><span class="sxs-lookup"><span data-stu-id="9caf3-115">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="9caf3-116">Divisor.</span><span class="sxs-lookup"><span data-stu-id="9caf3-116">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="9caf3-117">*Rnd*</span><span class="sxs-lookup"><span data-stu-id="9caf3-117">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="9caf3-118">Fator de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="9caf3-118">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9caf3-119">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9caf3-119">Return value</span></span>

<span data-ttu-id="9caf3-120">Retorna o `(a * b + rnd)/c` cálculo ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="9caf3-120">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="9caf3-121">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="9caf3-121">Return code</span></span>                                                                                       | <span data-ttu-id="9caf3-122">Descrição</span><span class="sxs-lookup"><span data-stu-id="9caf3-122">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="9caf3-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="9caf3-123"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="9caf3-124">Ocorreu um estouro porque o resultado é muito grande (positivo).</span><span class="sxs-lookup"><span data-stu-id="9caf3-124">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="9caf3-125"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="9caf3-125"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="9caf3-126">Ocorreu um estouro porque o resultado é muito grande (negativo).</span><span class="sxs-lookup"><span data-stu-id="9caf3-126">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="9caf3-127">Comentários</span><span class="sxs-lookup"><span data-stu-id="9caf3-127">Remarks</span></span>

<span data-ttu-id="9caf3-128">O arredondamento na divisão é diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="9caf3-128">Rounding on the division is toward zero.</span></span> <span data-ttu-id="9caf3-129">A divisão por zero é contada como uma condição de estouro.</span><span class="sxs-lookup"><span data-stu-id="9caf3-129">Division by zero is counted as an overflow condition.</span></span>

## <a name="requirements"></a><span data-ttu-id="9caf3-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9caf3-130">Requirements</span></span>



| <span data-ttu-id="9caf3-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="9caf3-131">Requirement</span></span> | <span data-ttu-id="9caf3-132">Valor</span><span class="sxs-lookup"><span data-stu-id="9caf3-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9caf3-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9caf3-133">Header</span></span><br/>  | <dl> <span data-ttu-id="9caf3-134"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9caf3-134"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9caf3-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9caf3-135">Library</span></span><br/> | <dl> <span data-ttu-id="9caf3-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9caf3-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9caf3-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="9caf3-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9caf3-138">Funções auxiliares diversas</span><span class="sxs-lookup"><span data-stu-id="9caf3-138">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="9caf3-139">**Int64x32Div32**</span><span class="sxs-lookup"><span data-stu-id="9caf3-139">**Int64x32Div32**</span></span>](int64x32div32.md)
</dt> </dl>

 

 




