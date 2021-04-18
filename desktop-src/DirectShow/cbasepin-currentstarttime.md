---
description: 'O método CurrentStartTime recupera a hora de início do segmento, definida pelo método CBasePin:: NewSegment.'
ms.assetid: 6bf7407e-0b23-47cf-925e-3fed183c76fa
title: Método CBasePin. CurrentStartTime (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentStartTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5f413419992d66f8de3a28bb7e39368564ce0803
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764579"
---
# <a name="cbasepincurrentstarttime-method"></a><span data-ttu-id="195bc-103">Método CBasePin. CurrentStartTime</span><span class="sxs-lookup"><span data-stu-id="195bc-103">CBasePin.CurrentStartTime method</span></span>

<span data-ttu-id="195bc-104">O `CurrentStartTime` método recupera a hora de início do segmento, definida pelo método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="195bc-104">The `CurrentStartTime` method retrieves the segment start time, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="195bc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="195bc-105">Syntax</span></span>


```C++
REFERENCE_TIME CurrentStartTime();
```



## <a name="parameters"></a><span data-ttu-id="195bc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="195bc-106">Parameters</span></span>

<span data-ttu-id="195bc-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="195bc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="195bc-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="195bc-108">Return value</span></span>

<span data-ttu-id="195bc-109">Retorna o valor de [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md).</span><span class="sxs-lookup"><span data-stu-id="195bc-109">Returns the value of [**CBasePin::m\_tStart**](cbasepin-m-tstart.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="195bc-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="195bc-110">Requirements</span></span>



| <span data-ttu-id="195bc-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="195bc-111">Requirement</span></span> | <span data-ttu-id="195bc-112">Valor</span><span class="sxs-lookup"><span data-stu-id="195bc-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="195bc-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="195bc-113">Header</span></span><br/>  | <dl> <span data-ttu-id="195bc-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="195bc-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="195bc-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="195bc-115">Library</span></span><br/> | <dl> <span data-ttu-id="195bc-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="195bc-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="195bc-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="195bc-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="195bc-118">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="195bc-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




