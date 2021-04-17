---
description: 'O método CurrentRate recupera a taxa de segmento, definida pelo método CBasePin:: NewSegment.'
ms.assetid: 19780dd2-2dcf-4e5d-8a70-a46be05e040c
title: Método CBasePin. CurrentRate (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CurrentRate
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: adffcc02aad4c5516a8e92c247e47b7dbf389d73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747832"
---
# <a name="cbasepincurrentrate-method"></a><span data-ttu-id="e4fc4-103">Método CBasePin. CurrentRate</span><span class="sxs-lookup"><span data-stu-id="e4fc4-103">CBasePin.CurrentRate method</span></span>

<span data-ttu-id="e4fc4-104">O `CurrentRate` método recupera a taxa de segmento, definida pelo método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="e4fc4-104">The `CurrentRate` method retrieves the segment rate, set by the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4fc4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4fc4-105">Syntax</span></span>


```C++
double CurrentRate();
```



## <a name="parameters"></a><span data-ttu-id="e4fc4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4fc4-106">Parameters</span></span>

<span data-ttu-id="e4fc4-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e4fc4-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4fc4-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4fc4-108">Return value</span></span>

<span data-ttu-id="e4fc4-109">Retorna o valor de [**CBasePin:: m \_ drate**](cbasepin-m-drate.md).</span><span class="sxs-lookup"><span data-stu-id="e4fc4-109">Returns the value of [**CBasePin::m\_dRate**](cbasepin-m-drate.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e4fc4-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4fc4-110">Requirements</span></span>



| <span data-ttu-id="e4fc4-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4fc4-111">Requirement</span></span> | <span data-ttu-id="e4fc4-112">Valor</span><span class="sxs-lookup"><span data-stu-id="e4fc4-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4fc4-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4fc4-113">Header</span></span><br/>  | <dl> <span data-ttu-id="e4fc4-114"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4fc4-114"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4fc4-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4fc4-115">Library</span></span><br/> | <dl> <span data-ttu-id="e4fc4-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e4fc4-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4fc4-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4fc4-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4fc4-118">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e4fc4-118">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




