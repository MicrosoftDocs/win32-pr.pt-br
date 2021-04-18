---
description: O método ativo notifica o PIN de que o filtro está ativo agora.
ms.assetid: c2b8eb54-1bae-4f52-8324-dc70e3cac577
title: Método CDynamicOutputPin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8f1765d0aa524c0dafd03a3fe4133af71e32fa70
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778626"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="1d6dc-103">Método CDynamicOutputPin. active</span><span class="sxs-lookup"><span data-stu-id="1d6dc-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="1d6dc-104">O `Active` método notifica o PIN de que o filtro está ativo agora.</span><span class="sxs-lookup"><span data-stu-id="1d6dc-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d6dc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d6dc-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="1d6dc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d6dc-106">Parameters</span></span>

<span data-ttu-id="1d6dc-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="1d6dc-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="1d6dc-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d6dc-108">Return value</span></span>

<span data-ttu-id="1d6dc-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="1d6dc-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="1d6dc-110">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="1d6dc-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="1d6dc-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="1d6dc-111">Return code</span></span>                                                                            | <span data-ttu-id="1d6dc-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="1d6dc-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="1d6dc-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="1d6dc-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="1d6dc-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="1d6dc-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="1d6dc-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="1d6dc-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="1d6dc-116">Falha.</span><span class="sxs-lookup"><span data-stu-id="1d6dc-116">Failure.</span></span> <span data-ttu-id="1d6dc-117">[**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) não foi chamado.</span><span class="sxs-lookup"><span data-stu-id="1d6dc-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="1d6dc-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d6dc-118">Remarks</span></span>

<span data-ttu-id="1d6dc-119">Esse método substitui o método [**CBaseOutputPin:: active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="1d6dc-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="1d6dc-120">Ele redefine o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="1d6dc-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="1d6dc-121">Se o filtro proprietário não tiver chamado **SetConfigInfo**, esse método retornará E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="1d6dc-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d6dc-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d6dc-122">Requirements</span></span>



| <span data-ttu-id="1d6dc-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d6dc-123">Requirement</span></span> | <span data-ttu-id="1d6dc-124">Valor</span><span class="sxs-lookup"><span data-stu-id="1d6dc-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d6dc-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d6dc-125">Header</span></span><br/>  | <dl> <span data-ttu-id="1d6dc-126"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d6dc-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="1d6dc-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d6dc-127">Library</span></span><br/> | <dl> <span data-ttu-id="1d6dc-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1d6dc-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d6dc-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d6dc-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d6dc-130">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="1d6dc-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




