---
description: O método Run notifica o PIN de que o filtro agora está em execução.
ms.assetid: 74aafc89-2d3c-4259-a5b7-d4fb7628f539
title: Método CBasePin. Run (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Run
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 35d66f6d504a96c1146bc15285762d83faa6de3b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771864"
---
# <a name="cbasepinrun-method"></a><span data-ttu-id="6db95-103">Método CBasePin. Run</span><span class="sxs-lookup"><span data-stu-id="6db95-103">CBasePin.Run method</span></span>

<span data-ttu-id="6db95-104">O `Run` método notifica o PIN de que o filtro agora está em execução.</span><span class="sxs-lookup"><span data-stu-id="6db95-104">The `Run` method notifies the pin that the filter is now running.</span></span>

## <a name="syntax"></a><span data-ttu-id="6db95-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6db95-105">Syntax</span></span>


```C++
HRESULT Run(
   REFERENCE_TIME tStart
);
```



## <a name="parameters"></a><span data-ttu-id="6db95-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6db95-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6db95-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="6db95-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="6db95-108">Hora de início como passada para o método [**IMediaFilter:: Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) do filtro.</span><span class="sxs-lookup"><span data-stu-id="6db95-108">Start time as passed to the filter's [**IMediaFilter::Run**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-run) method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6db95-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6db95-109">Return value</span></span>

<span data-ttu-id="6db95-110">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6db95-110">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6db95-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="6db95-111">Remarks</span></span>

<span data-ttu-id="6db95-112">Quando o filtro passa de pausado para em execução, a classe [**CBaseFilter**](cbasefilter.md) chama esse método em todos os Pins do filtro.</span><span class="sxs-lookup"><span data-stu-id="6db95-112">When the filter goes from paused to running, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's pins.</span></span>

<span data-ttu-id="6db95-113">Esse método não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="6db95-113">This method does nothing in the base class.</span></span> <span data-ttu-id="6db95-114">Classes derivadas podem substituir esse método.</span><span class="sxs-lookup"><span data-stu-id="6db95-114">Derived classes can override this method.</span></span> <span data-ttu-id="6db95-115">Por exemplo, um PIN pode iniciar um thread de trabalho que fornece exemplos.</span><span class="sxs-lookup"><span data-stu-id="6db95-115">For example, a pin might start a worker thread that delivers samples.</span></span>

<span data-ttu-id="6db95-116">O estado interno do Gerenciador de grafo de filtro não é atualizado até que essa função de membro retorne, portanto, não teste o estado desse método.</span><span class="sxs-lookup"><span data-stu-id="6db95-116">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6db95-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6db95-117">Requirements</span></span>



| <span data-ttu-id="6db95-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="6db95-118">Requirement</span></span> | <span data-ttu-id="6db95-119">Valor</span><span class="sxs-lookup"><span data-stu-id="6db95-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6db95-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6db95-120">Header</span></span><br/>  | <dl> <span data-ttu-id="6db95-121"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6db95-121"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6db95-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6db95-122">Library</span></span><br/> | <dl> <span data-ttu-id="6db95-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6db95-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6db95-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="6db95-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6db95-125">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="6db95-125">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




