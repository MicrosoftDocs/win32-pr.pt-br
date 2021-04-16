---
description: O método GetPinCount recupera o número de Pins.
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
ms.openlocfilehash: 8da1cbc22a49b149bdccc36c3b854b44101b9bbc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750682"
---
# <a name="cbasefiltergetpincount-method"></a><span data-ttu-id="45b38-103">Método CBaseFilter. GetPinCount</span><span class="sxs-lookup"><span data-stu-id="45b38-103">CBaseFilter.GetPinCount method</span></span>

<span data-ttu-id="45b38-104">O `GetPinCount` método recupera o número de Pins.</span><span class="sxs-lookup"><span data-stu-id="45b38-104">The `GetPinCount` method retrieves the number of pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="45b38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="45b38-105">Syntax</span></span>


```C++
virtual int GetPinCount() = 0;
```



## <a name="parameters"></a><span data-ttu-id="45b38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="45b38-106">Parameters</span></span>

<span data-ttu-id="45b38-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="45b38-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="45b38-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="45b38-108">Return value</span></span>

<span data-ttu-id="45b38-109">Retorna o número de Pins.</span><span class="sxs-lookup"><span data-stu-id="45b38-109">Returns the number of pins.</span></span>

## <a name="remarks"></a><span data-ttu-id="45b38-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="45b38-110">Remarks</span></span>

<span data-ttu-id="45b38-111">A classe derivada deve implementar esse método virtual puro.</span><span class="sxs-lookup"><span data-stu-id="45b38-111">The derived class must implement this pure virtual method.</span></span> <span data-ttu-id="45b38-112">Retornar o número de Pins disponíveis no momento neste filtro.</span><span class="sxs-lookup"><span data-stu-id="45b38-112">Return the number of pins that are currently available on this filter.</span></span> <span data-ttu-id="45b38-113">Os filtros podem criar ou destruir Pins dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="45b38-113">Filters can dynamically create or destroy pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="45b38-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="45b38-114">Requirements</span></span>



| <span data-ttu-id="45b38-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="45b38-115">Requirement</span></span> | <span data-ttu-id="45b38-116">Valor</span><span class="sxs-lookup"><span data-stu-id="45b38-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="45b38-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="45b38-117">Header</span></span><br/>  | <dl> <span data-ttu-id="45b38-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="45b38-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="45b38-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="45b38-119">Library</span></span><br/> | <dl> <span data-ttu-id="45b38-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="45b38-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="45b38-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="45b38-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="45b38-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="45b38-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




