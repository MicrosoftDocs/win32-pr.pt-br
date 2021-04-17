---
description: O método inativo notifica o PIN de que o filtro foi interrompido.
ms.assetid: f7efb67b-cc3f-47c4-a8ba-b2365aef0d96
title: Método CDynamicOutputPin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4501025e844056a83be3e20a19f8ad52f935097f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787408"
---
# <a name="cdynamicoutputpininactive-method"></a><span data-ttu-id="33ffb-103">Método CDynamicOutputPin. Inactive</span><span class="sxs-lookup"><span data-stu-id="33ffb-103">CDynamicOutputPin.Inactive method</span></span>

<span data-ttu-id="33ffb-104">O `Inactive` método notifica o PIN de que o filtro foi interrompido.</span><span class="sxs-lookup"><span data-stu-id="33ffb-104">The `Inactive` method notifies the pin that the filter has stopped.</span></span>

## <a name="syntax"></a><span data-ttu-id="33ffb-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33ffb-105">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="33ffb-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33ffb-106">Parameters</span></span>

<span data-ttu-id="33ffb-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="33ffb-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="33ffb-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33ffb-108">Return value</span></span>

<span data-ttu-id="33ffb-109">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="33ffb-109">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="33ffb-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="33ffb-110">Remarks</span></span>

<span data-ttu-id="33ffb-111">Esse método substitui o método [**CBaseOutputPin:: Inactive**](cbaseoutputpin-inactive.md) .</span><span class="sxs-lookup"><span data-stu-id="33ffb-111">This method overrides the [**CBaseOutputPin::Inactive**](cbaseoutputpin-inactive.md) method.</span></span> <span data-ttu-id="33ffb-112">Ele define o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="33ffb-112">It sets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="33ffb-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33ffb-113">Requirements</span></span>



| <span data-ttu-id="33ffb-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="33ffb-114">Requirement</span></span> | <span data-ttu-id="33ffb-115">Valor</span><span class="sxs-lookup"><span data-stu-id="33ffb-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33ffb-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33ffb-116">Header</span></span><br/>  | <dl> <span data-ttu-id="33ffb-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33ffb-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33ffb-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33ffb-118">Library</span></span><br/> | <dl> <span data-ttu-id="33ffb-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="33ffb-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33ffb-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="33ffb-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33ffb-121">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="33ffb-121">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




