---
description: 'O método CurrentStopTime recupera a hora de parada do segmento, definida pelo método CBasePin:: NewSegment.'
ms.assetid: 2066c4a5-2d39-4a2e-b2d6-48c615862aec
title: Método CBasePin. CurrentStopTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStopTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 74fb25184bbcd0778268f74a4c40ccfb0722287f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755612"
---
# <a name="cbasepincurrentstoptime-method"></a><span data-ttu-id="37c75-103">Método CBasePin. CurrentStopTime</span><span class="sxs-lookup"><span data-stu-id="37c75-103">CBasePin.CurrentStopTime method</span></span>

<span data-ttu-id="37c75-104">O `CurrentStopTime` método recupera a hora de parada do segmento, definida pelo método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="37c75-104">The `CurrentStopTime` method retrieves the segment stop time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="37c75-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="37c75-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStopTime();
```



## <a name="parameters"></a><span data-ttu-id="37c75-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="37c75-106">Parameters</span></span>

<span data-ttu-id="37c75-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="37c75-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="37c75-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="37c75-108">Return value</span></span>

<span data-ttu-id="37c75-109">Retorna o valor de [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md).</span><span class="sxs-lookup"><span data-stu-id="37c75-109">Returns the value of [**CBasePin::m\_tStop**](cbasepin-m-tstop.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="37c75-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="37c75-110">Requirements</span></span>



| <span data-ttu-id="37c75-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="37c75-111">Requirement</span></span> | <span data-ttu-id="37c75-112">Valor</span><span class="sxs-lookup"><span data-stu-id="37c75-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="37c75-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="37c75-113">Header</span></span><br/>  | <dl> <span data-ttu-id="37c75-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="37c75-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="37c75-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="37c75-115">Library</span></span><br/> | <dl> <span data-ttu-id="37c75-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="37c75-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="37c75-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="37c75-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="37c75-118">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="37c75-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




