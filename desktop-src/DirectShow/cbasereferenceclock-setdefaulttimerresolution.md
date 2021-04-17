---
description: O método SetDefaultTimerResolution define a resolução do timer do relógio de referência.
ms.assetid: 891b809a-15d3-41f3-853e-aca9ddcd56e8
title: Método CBaseReferenceClock. SetDefaultTimerResolution (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.SetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 146162784ad52a7f7930613ec5c648e40d22900f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754555"
---
# <a name="cbasereferenceclocksetdefaulttimerresolution-method"></a><span data-ttu-id="ba0ea-103">Método CBaseReferenceClock. SetDefaultTimerResolution</span><span class="sxs-lookup"><span data-stu-id="ba0ea-103">CBaseReferenceClock.SetDefaultTimerResolution method</span></span>

<span data-ttu-id="ba0ea-104">O `SetDefaultTimerResolution` método define a resolução do temporizador do relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="ba0ea-104">The `SetDefaultTimerResolution` method sets the resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba0ea-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba0ea-105">Syntax</span></span>


```C++
STDMETHODIMP SetDefaultTimerResolution(
   REFERENCE_TIME timerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="ba0ea-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba0ea-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba0ea-107">*timerResolution*</span><span class="sxs-lookup"><span data-stu-id="ba0ea-107">*timerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="ba0ea-108">Resolução mínima do temporizador, em unidades de 100 nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="ba0ea-108">Minimum timer resolution, in 100-nanosecond units.</span></span> <span data-ttu-id="ba0ea-109">Se o valor for zero, o relógio de referência cancelará sua solicitação anterior.</span><span class="sxs-lookup"><span data-stu-id="ba0ea-109">If the value is zero, the reference clock cancels its previous request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba0ea-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba0ea-110">Return value</span></span>

<span data-ttu-id="ba0ea-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ba0ea-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba0ea-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba0ea-112">Remarks</span></span>

<span data-ttu-id="ba0ea-113">Esse método implementa o método [**IReferenceClockTimerControl:: SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="ba0ea-113">This method implements the [**IReferenceClockTimerControl::SetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-setdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba0ea-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba0ea-114">Requirements</span></span>



| <span data-ttu-id="ba0ea-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba0ea-115">Requirement</span></span> | <span data-ttu-id="ba0ea-116">Valor</span><span class="sxs-lookup"><span data-stu-id="ba0ea-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba0ea-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba0ea-117">Header</span></span><br/>  | <dl> <span data-ttu-id="ba0ea-118"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba0ea-118"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba0ea-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba0ea-119">Library</span></span><br/> | <dl> <span data-ttu-id="ba0ea-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ba0ea-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba0ea-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba0ea-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba0ea-122">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="ba0ea-122">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




