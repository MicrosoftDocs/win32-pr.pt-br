---
description: 'O método SetClockDelta ajusta a hora do relógio. Esse método implementa o método IAMClockAdjust:: SetClockDelta.'
ms.assetid: 2bb9266f-3866-4b2e-92a8-cde31a501047
title: Método CSystemClock. SetClockDelta (Sysclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSystemClock.SetClockDelta
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cc1027081cc8713cffd2979e20627c037d0799f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751678"
---
# <a name="csystemclocksetclockdelta-method"></a><span data-ttu-id="90049-104">Método CSystemClock. SetClockDelta</span><span class="sxs-lookup"><span data-stu-id="90049-104">CSystemClock.SetClockDelta method</span></span>

<span data-ttu-id="90049-105">O `SetClockDelta` método ajusta a hora do relógio.</span><span class="sxs-lookup"><span data-stu-id="90049-105">The `SetClockDelta` method adjusts the clock time.</span></span> <span data-ttu-id="90049-106">Esse método implementa o método [**IAMClockAdjust:: SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) .</span><span class="sxs-lookup"><span data-stu-id="90049-106">This method implements the [**IAMClockAdjust::SetClockDelta**](/windows/desktop/api/Strmif/nf-strmif-iamclockadjust-setclockdelta) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="90049-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="90049-107">Syntax</span></span>


```C++
HRESULT SetClockDelta(
   REFERENCE_TIME rtDelta
);
```



## <a name="parameters"></a><span data-ttu-id="90049-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="90049-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="90049-109">*rtDelta*</span><span class="sxs-lookup"><span data-stu-id="90049-109">*rtDelta*</span></span> 
</dt> <dd>

<span data-ttu-id="90049-110">Especifica o valor pelo qual ajustar o relógio, como um valor [**de \_ tempo de referência**](reference-time.md) .</span><span class="sxs-lookup"><span data-stu-id="90049-110">Specifies the amount by which to adjust the clock, as a [**REFERENCE\_TIME**](reference-time.md) value.</span></span> <span data-ttu-id="90049-111">Um valor positivo move o relógio para a frente e um valor negativo move o relógio para trás.</span><span class="sxs-lookup"><span data-stu-id="90049-111">A positive value moves the clock forward, and a negative value moves the clock backward.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="90049-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="90049-112">Return value</span></span>

<span data-ttu-id="90049-113">Retorna S \_ OK ou um código de erro **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="90049-113">Returns S\_OK or an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="90049-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="90049-114">Remarks</span></span>

<span data-ttu-id="90049-115">Esse método simplesmente chama [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span><span class="sxs-lookup"><span data-stu-id="90049-115">This method simply calls [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).</span></span>

<span data-ttu-id="90049-116">Os valores de tempo retornados por [**IReferenceClock:: getTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) são monotônicos aumentando.</span><span class="sxs-lookup"><span data-stu-id="90049-116">The time values returned by [**IReferenceClock::GetTime**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclock-gettime) are monotonically increasing.</span></span> <span data-ttu-id="90049-117">Se você definir o relógio de volta, **getTime** continuará relatando o tempo antigo até que o relógio interno se ajuste.</span><span class="sxs-lookup"><span data-stu-id="90049-117">If you set the clock back, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

## <a name="requirements"></a><span data-ttu-id="90049-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="90049-118">Requirements</span></span>



| <span data-ttu-id="90049-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="90049-119">Requirement</span></span> | <span data-ttu-id="90049-120">Valor</span><span class="sxs-lookup"><span data-stu-id="90049-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="90049-121">Versão</span><span class="sxs-lookup"><span data-stu-id="90049-121">Version</span></span><br/> | <span data-ttu-id="90049-122">Classe CSystemClock</span><span class="sxs-lookup"><span data-stu-id="90049-122">CSystemClock Class</span></span><br/>                                                                                                                                                              |
| <span data-ttu-id="90049-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="90049-123">Header</span></span><br/>  | <dl> <span data-ttu-id="90049-124"><dt>Sysclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="90049-124"><dt>Sysclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="90049-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="90049-125">Library</span></span><br/> | <dl> <span data-ttu-id="90049-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="90049-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




