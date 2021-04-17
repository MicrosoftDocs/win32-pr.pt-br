---
description: O método GetDefaultTimerResolution retorna a resolução atual do temporizador do relógio de referência.
ms.assetid: 14176f9c-7fa1-47f6-a261-9c66e271a3f2
title: Método CBaseReferenceClock. GetDefaultTimerResolution (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.GetDefaultTimerResolution
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40a1c430f95b13086d50811e63cc2e411b3bf377
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752510"
---
# <a name="cbasereferenceclockgetdefaulttimerresolution-method"></a><span data-ttu-id="ae7f7-103">Método CBaseReferenceClock. GetDefaultTimerResolution</span><span class="sxs-lookup"><span data-stu-id="ae7f7-103">CBaseReferenceClock.GetDefaultTimerResolution method</span></span>

<span data-ttu-id="ae7f7-104">O `GetDefaultTimerResolution` método retorna a resolução atual do temporizador do relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-104">The `GetDefaultTimerResolution` method returns the current resolution of the reference clock's timer.</span></span>

## <a name="syntax"></a><span data-ttu-id="ae7f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ae7f7-105">Syntax</span></span>


```C++
STDMETHODIMP GetDefaultTimerResolution(
   REFERENCE_TIME *pTimerResolution
);
```



## <a name="parameters"></a><span data-ttu-id="ae7f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ae7f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ae7f7-107">*pTimerResolution*</span><span class="sxs-lookup"><span data-stu-id="ae7f7-107">*pTimerResolution*</span></span> 
</dt> <dd>

<span data-ttu-id="ae7f7-108">Recebe a resolução do temporizador solicitada, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="ae7f7-108">Receives the requested timer resolution, in 100-nanosecond units.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ae7f7-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ae7f7-109">Return value</span></span>

<span data-ttu-id="ae7f7-110">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ae7f7-110">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ae7f7-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ae7f7-111">Remarks</span></span>

<span data-ttu-id="ae7f7-112">Esse método implementa o método [**IReferenceClockTimerControl:: GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) .</span><span class="sxs-lookup"><span data-stu-id="ae7f7-112">This method implements the [**IReferenceClockTimerControl::GetDefaultTimerResolution**](/windows/desktop/api/Strmif/nf-strmif-ireferenceclocktimercontrol-getdefaulttimerresolution) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ae7f7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ae7f7-113">Requirements</span></span>



| <span data-ttu-id="ae7f7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ae7f7-114">Requirement</span></span> | <span data-ttu-id="ae7f7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ae7f7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ae7f7-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ae7f7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ae7f7-117"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ae7f7-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ae7f7-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ae7f7-118">Library</span></span><br/> | <dl> <span data-ttu-id="ae7f7-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ae7f7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ae7f7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ae7f7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ae7f7-121">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="ae7f7-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




