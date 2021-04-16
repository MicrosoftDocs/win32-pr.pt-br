---
description: A função Int64x32Div32 implementa a fórmula ((a \* b) + Rnd)/c, em que um é um valor de 64 bits e b, c e Rnd são valores de 32 bits.
ms.assetid: 566ac194-5b15-43b7-aa7c-0c18c6f69691
title: Função Int64x32Div32 (Wxutil. h)
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
ms.openlocfilehash: de60ca08b262dbf97aa118bd115bd6dc58576a1d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758467"
---
# <a name="int64x32div32-function"></a><span data-ttu-id="35ceb-103">Função Int64x32Div32</span><span class="sxs-lookup"><span data-stu-id="35ceb-103">Int64x32Div32 function</span></span>

<span data-ttu-id="35ceb-104">A `Int64x32Div32` função implementa a fórmula `((a*b)+rnd)/c` em que *um* é um valor de 64 bits e *b*, *c* e *Rnd* são valores de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="35ceb-104">The `Int64x32Div32` function implements the formula `((a*b)+rnd)/c` where *a* is a 64-bit value and *b*, *c*, and *rnd* are 32-bit values.</span></span>

## <a name="syntax"></a><span data-ttu-id="35ceb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="35ceb-105">Syntax</span></span>


```C++
LONGLONG WINAPI Int64x32Div32(
   LONGLONG a,
   LONG     b,
   LONG     c,
   LONG     rnd
);
```



## <a name="parameters"></a><span data-ttu-id="35ceb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="35ceb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="35ceb-107">*um*</span><span class="sxs-lookup"><span data-stu-id="35ceb-107">*a*</span></span> 
</dt> <dd>

<span data-ttu-id="35ceb-108">Multiplicando.</span><span class="sxs-lookup"><span data-stu-id="35ceb-108">Multiplicand.</span></span>

</dd> <dt>

<span data-ttu-id="35ceb-109">*b*</span><span class="sxs-lookup"><span data-stu-id="35ceb-109">*b*</span></span> 
</dt> <dd>

<span data-ttu-id="35ceb-110">Multiplicador.</span><span class="sxs-lookup"><span data-stu-id="35ceb-110">Multiplier.</span></span>

</dd> <dt>

<span data-ttu-id="35ceb-111">*c*</span><span class="sxs-lookup"><span data-stu-id="35ceb-111">*c*</span></span> 
</dt> <dd>

<span data-ttu-id="35ceb-112">Divisor.</span><span class="sxs-lookup"><span data-stu-id="35ceb-112">Divisor.</span></span>

</dd> <dt>

<span data-ttu-id="35ceb-113">*Rnd*</span><span class="sxs-lookup"><span data-stu-id="35ceb-113">*rnd*</span></span> 
</dt> <dd>

<span data-ttu-id="35ceb-114">Fator de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="35ceb-114">Rounding factor.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="35ceb-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="35ceb-115">Return value</span></span>

<span data-ttu-id="35ceb-116">Retorna o `(a * b + rnd)/c` cálculo ou um dos valores a seguir.</span><span class="sxs-lookup"><span data-stu-id="35ceb-116">Returns either the `(a * b + rnd)/c` calculation or one of the following values.</span></span>



| <span data-ttu-id="35ceb-117">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="35ceb-117">Return code</span></span>                                                                                       | <span data-ttu-id="35ceb-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="35ceb-118">Description</span></span>                                                              |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="35ceb-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span><span class="sxs-lookup"><span data-stu-id="35ceb-119"><dt>**0x7FFFFFFFFFFFFFFF**</dt></span></span> </dl> | <span data-ttu-id="35ceb-120">Ocorreu um estouro porque o resultado é muito grande (positivo).</span><span class="sxs-lookup"><span data-stu-id="35ceb-120">Overflow occurred because the result is too large (positive).</span></span><br/> |
| <dl> <span data-ttu-id="35ceb-121"><dt>**0x8000000000000000**</dt></span><span class="sxs-lookup"><span data-stu-id="35ceb-121"><dt>**0x8000000000000000**</dt></span></span> </dl> | <span data-ttu-id="35ceb-122">Ocorreu um estouro porque o resultado é muito grande (negativo).</span><span class="sxs-lookup"><span data-stu-id="35ceb-122">Overflow occurred because the result is too large (negative).</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="35ceb-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="35ceb-123">Remarks</span></span>

<span data-ttu-id="35ceb-124">O arredondamento na divisão é diferente de zero.</span><span class="sxs-lookup"><span data-stu-id="35ceb-124">Rounding on the division is toward zero.</span></span> <span data-ttu-id="35ceb-125">A divisão por zero é contada como uma condição de estouro.</span><span class="sxs-lookup"><span data-stu-id="35ceb-125">Division by zero is counted as an overflow condition.</span></span>

<span data-ttu-id="35ceb-126">Carimbos de data/hora e tempos de busca são valores de 64 bits, portanto, essa função é útil para executar conversões em sistemas de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="35ceb-126">Time stamps and seek times are 64-bit values, so this function is useful for performing conversions on 32-bit systems.</span></span> <span data-ttu-id="35ceb-127">Por exemplo, em MPEG-1, a referência do relógio do sistema é 90-kHz ou 90.000 tiques por segundo.</span><span class="sxs-lookup"><span data-stu-id="35ceb-127">For example, in MPEG-1 the system clock reference is 90-kHz, or 90,000 ticks per second.</span></span> <span data-ttu-id="35ceb-128">A fórmula para converter isso em tempo de referência (unidades de 100 a nanossegundos) é</span><span class="sxs-lookup"><span data-stu-id="35ceb-128">The formula to convert this to reference time (100-nanosecond units) is</span></span>


```C++
(timestamp * 1000) / 9
```



<span data-ttu-id="35ceb-129">que pode ser calculado como `Int64x32Div32(timestamp, 1000, 9, 0)` .</span><span class="sxs-lookup"><span data-stu-id="35ceb-129">which can be calculated as `Int64x32Div32(timestamp, 1000, 9, 0)`.</span></span> <span data-ttu-id="35ceb-130">Use o parâmetro *Rnd* como um fator de arredondamento.</span><span class="sxs-lookup"><span data-stu-id="35ceb-130">Use the *rnd* parameter as a rounding factor.</span></span>

## <a name="requirements"></a><span data-ttu-id="35ceb-131">Requisitos</span><span class="sxs-lookup"><span data-stu-id="35ceb-131">Requirements</span></span>



| <span data-ttu-id="35ceb-132">Requisito</span><span class="sxs-lookup"><span data-stu-id="35ceb-132">Requirement</span></span> | <span data-ttu-id="35ceb-133">Valor</span><span class="sxs-lookup"><span data-stu-id="35ceb-133">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="35ceb-134">parâmetro</span><span class="sxs-lookup"><span data-stu-id="35ceb-134">Header</span></span><br/>  | <dl> <span data-ttu-id="35ceb-135"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="35ceb-135"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="35ceb-136">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="35ceb-136">Library</span></span><br/> | <dl> <span data-ttu-id="35ceb-137"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="35ceb-137"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="35ceb-138">Confira também</span><span class="sxs-lookup"><span data-stu-id="35ceb-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="35ceb-139">Funções auxiliares diversas</span><span class="sxs-lookup"><span data-stu-id="35ceb-139">Miscellaneous Helper Functions</span></span>](miscellaneous-helper-functions.md)
</dt> <dt>

[<span data-ttu-id="35ceb-140">**llMulDiv**</span><span class="sxs-lookup"><span data-stu-id="35ceb-140">**llMulDiv**</span></span>](llmuldiv.md)
</dt> </dl>

 

 




