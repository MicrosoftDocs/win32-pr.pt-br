---
description: Método CDynamicOutputPin. active – o método ativo notifica o PIN de que o filtro está ativo agora.
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
ms.openlocfilehash: 1d9544c0fd125146b10f008565fcfbe330d18de1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099324"
---
# <a name="cdynamicoutputpinactive-method"></a><span data-ttu-id="0cc81-103">Método CDynamicOutputPin. active</span><span class="sxs-lookup"><span data-stu-id="0cc81-103">CDynamicOutputPin.Active method</span></span>

<span data-ttu-id="0cc81-104">O `Active` método notifica o PIN de que o filtro está ativo agora.</span><span class="sxs-lookup"><span data-stu-id="0cc81-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="0cc81-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0cc81-105">Syntax</span></span>


```C++
HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="0cc81-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0cc81-106">Parameters</span></span>

<span data-ttu-id="0cc81-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0cc81-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0cc81-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0cc81-108">Return value</span></span>

<span data-ttu-id="0cc81-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0cc81-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="0cc81-110">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="0cc81-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="0cc81-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="0cc81-111">Return code</span></span>                                                                            | <span data-ttu-id="0cc81-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="0cc81-112">Description</span></span>                                                                                                     |
|----------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="0cc81-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="0cc81-113"><dt>**S\_OK**</dt></span></span> </dl>   | <span data-ttu-id="0cc81-114">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="0cc81-114">Success.</span></span><br/>                                                                                             |
| <dl> <span data-ttu-id="0cc81-115"><dt>**E \_ falha**</dt></span><span class="sxs-lookup"><span data-stu-id="0cc81-115"><dt>**E\_FAIL**</dt></span></span> </dl> | <span data-ttu-id="0cc81-116">Falha.</span><span class="sxs-lookup"><span data-stu-id="0cc81-116">Failure.</span></span> <span data-ttu-id="0cc81-117">[**CDynamicOutputPin:: SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) não foi chamado.</span><span class="sxs-lookup"><span data-stu-id="0cc81-117">[**CDynamicOutputPin::SetConfigInfo**](cdynamicoutputpin-setconfiginfo.md) was not called.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="0cc81-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="0cc81-118">Remarks</span></span>

<span data-ttu-id="0cc81-119">Esse método substitui o método [**CBaseOutputPin:: active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="0cc81-119">This method overrides the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span> <span data-ttu-id="0cc81-120">Ele redefine o evento [**CDynamicOutputPin:: m \_ hStopEvent**](cdynamicoutputpin-m-hstopevent.md) .</span><span class="sxs-lookup"><span data-stu-id="0cc81-120">It resets the [**CDynamicOutputPin::m\_hStopEvent**](cdynamicoutputpin-m-hstopevent.md) event.</span></span> <span data-ttu-id="0cc81-121">Se o filtro proprietário não tiver chamado **SetConfigInfo**, esse método retornará E \_ falhará.</span><span class="sxs-lookup"><span data-stu-id="0cc81-121">If the owning filter has not called **SetConfigInfo**, this method returns E\_FAIL.</span></span>

## <a name="requirements"></a><span data-ttu-id="0cc81-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0cc81-122">Requirements</span></span>



| <span data-ttu-id="0cc81-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0cc81-123">Requirement</span></span> | <span data-ttu-id="0cc81-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0cc81-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0cc81-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0cc81-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0cc81-126"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0cc81-126"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0cc81-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0cc81-127">Library</span></span><br/> | <dl> <span data-ttu-id="0cc81-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0cc81-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0cc81-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0cc81-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0cc81-130">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="0cc81-130">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




