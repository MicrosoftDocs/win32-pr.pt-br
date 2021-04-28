---
description: Método CBaseFilter. GetPinCount – o método GetPinCount recupera o número de Pins.
ms.assetid: 6cbeb123-d899-4f13-8b40-5666adec610f
title: Método CBaseFilter. GetPinCount (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0081b4cec45ed4cac5b4f0883032631983824cec
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099784"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="73a9f-103">Método CBaseFilter. GetPinCount</span><span class="sxs-lookup"><span data-stu-id="73a9f-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="73a9f-104">O `GetPinCount` método recupera o número de Pins.</span><span class="sxs-lookup"><span data-stu-id="73a9f-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="73a9f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="73a9f-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="73a9f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="73a9f-106">Parameters</span></span>

<span data-ttu-id="73a9f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="73a9f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="73a9f-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="73a9f-108">Return value</span></span>

<span data-ttu-id="73a9f-109">Retorna o número de Pins.</span><span class="sxs-lookup"><span data-stu-id="73a9f-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="73a9f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="73a9f-110">Remarks</span></span>

<span data-ttu-id="73a9f-111">A classe derivada deve implementar esse método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="73a9f-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="73a9f-112">Retornar o número de Pins disponíveis no momento neste filtro.</span><span class="sxs-lookup"><span data-stu-id="73a9f-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="73a9f-113">Os filtros podem criar ou destruir Pins dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="73a9f-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="73a9f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="73a9f-114">Requirements</span></span>



| <span data-ttu-id="73a9f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="73a9f-115">Requirement</span></span> | <span data-ttu-id="73a9f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="73a9f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="73a9f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="73a9f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="73a9f-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="73a9f-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="73a9f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="73a9f-119">Library</span></span><br/> | <dl> <span data-ttu-id="73a9f-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="73a9f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="73a9f-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="73a9f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="73a9f-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="73a9f-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




