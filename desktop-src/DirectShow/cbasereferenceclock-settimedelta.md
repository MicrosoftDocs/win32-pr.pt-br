---
description: O método SetTimeDelta ajusta a hora interna do relógio.
ms.assetid: 51534c92-5573-4e2a-baeb-b1a82ccf88de
title: Método CBaseReferenceClock. SetTimeDelta (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetTimeDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: de58363119dc08c21d2cab0070b438ad6b4331e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105811750"
---
# <a name="cbasereferenceclocksettimedelta-method"></a><span data-ttu-id="ee032-103">Método CBaseReferenceClock. SetTimeDelta</span><span class="sxs-lookup"><span data-stu-id="ee032-103">CBaseReferenceClock.SetTimeDelta method</span></span>

<span data-ttu-id="ee032-104">O `SetTimeDelta` método ajusta a hora interna do relógio.</span><span class="sxs-lookup"><span data-stu-id="ee032-104">The `SetTimeDelta` method adjusts the internal clock time.</span></span>

## <a name="syntax"></a><span data-ttu-id="ee032-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ee032-105">Syntax</span></span>


```C++
HRESULT SetTimeDelta(
  [ref] const REFERENCE_TIME &TimeDelta
);
```



## <a name="parameters"></a><span data-ttu-id="ee032-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ee032-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ee032-107">*Timedelta* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="ee032-107">*TimeDelta* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="ee032-108">Valor para ajustar a hora do relógio, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="ee032-108">Amount to adjust the clock time, in 100-nanosecond units.</span></span> <span data-ttu-id="ee032-109">Um valor positivo move o relógio para a frente e um valor negativo move o relógio para trás.</span><span class="sxs-lookup"><span data-stu-id="ee032-109">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ee032-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ee032-110">Return value</span></span>

<span data-ttu-id="ee032-111">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ee032-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ee032-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ee032-112">Remarks</span></span>

<span data-ttu-id="ee032-113">A classe derivada pode usar esse método para ajustar o relógio interno, caso ele se descompasso do dispositivo que está fornecendo informações de tempo.</span><span class="sxs-lookup"><span data-stu-id="ee032-113">The derived class can use this method to adjust the internal clock, if it drifts from the device that is providing timing information.</span></span>

<span data-ttu-id="ee032-114">O método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) nunca retorna valores decrescentes.</span><span class="sxs-lookup"><span data-stu-id="ee032-114">The [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method never returns decreasing values.</span></span> <span data-ttu-id="ee032-115">Se você ajustar o relógio para trás, **getTime** retornará o valor anterior até que o relógio atinja esse valor novamente.</span><span class="sxs-lookup"><span data-stu-id="ee032-115">If you adjust the clock backward, **GetTime** returns the previous value until the clock reaches that value again.</span></span>

## <a name="requirements"></a><span data-ttu-id="ee032-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ee032-116">Requirements</span></span>



| <span data-ttu-id="ee032-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ee032-117">Requirement</span></span> | <span data-ttu-id="ee032-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ee032-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ee032-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ee032-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ee032-120"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ee032-120"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ee032-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ee032-121">Library</span></span><br/> | <dl> <span data-ttu-id="ee032-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ee032-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ee032-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="ee032-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ee032-124">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="ee032-124">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




