---
description: O método NotifyEvent envia uma notificação de evento para o Gerenciador do grafo de filtro.
ms.assetid: 79587b72-4152-4443-9fde-c2746bf06191
title: Método CBaseFilter. NotifyEvent (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.NotifyEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 49fa689262d8f9b584c93a4b0485bbeaaacbf9a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748827"
---
# <a name="cbasefilternotifyevent-method"></a><span data-ttu-id="6f45b-103">Método CBaseFilter. NotifyEvent</span><span class="sxs-lookup"><span data-stu-id="6f45b-103">CBaseFilter.NotifyEvent method</span></span>

<span data-ttu-id="6f45b-104">O `NotifyEvent` método envia uma notificação de evento para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="6f45b-104">The `NotifyEvent` method sends an event notification to the filter graph manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="6f45b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6f45b-105">Syntax</span></span>


```C++
HRESULT NotifyEvent(
   long     EventCode,
   LONG_PTR EventParam1,
   LONG_PTR EventParam2
);
```



## <a name="parameters"></a><span data-ttu-id="6f45b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6f45b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6f45b-107">*EventCode*</span><span class="sxs-lookup"><span data-stu-id="6f45b-107">*EventCode*</span></span> 
</dt> <dd>

<span data-ttu-id="6f45b-108">Código de notificação de eventos.</span><span class="sxs-lookup"><span data-stu-id="6f45b-108">Event notification code.</span></span>

</dd> <dt>

<span data-ttu-id="6f45b-109">*EventParam1*</span><span class="sxs-lookup"><span data-stu-id="6f45b-109">*EventParam1*</span></span> 
</dt> <dd>

<span data-ttu-id="6f45b-110">Primeiro parâmetro do evento.</span><span class="sxs-lookup"><span data-stu-id="6f45b-110">First parameter of the event.</span></span>

</dd> <dt>

<span data-ttu-id="6f45b-111">*EventParam2*</span><span class="sxs-lookup"><span data-stu-id="6f45b-111">*EventParam2*</span></span> 
</dt> <dd>

<span data-ttu-id="6f45b-112">Segundo parâmetro do evento.</span><span class="sxs-lookup"><span data-stu-id="6f45b-112">Second parameter of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6f45b-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6f45b-113">Return value</span></span>

<span data-ttu-id="6f45b-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6f45b-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="6f45b-115">Os valores possíveis incluem os da tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="6f45b-115">Possible values include those in the following table.</span></span>



| <span data-ttu-id="6f45b-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="6f45b-116">Return code</span></span>                                                                               | <span data-ttu-id="6f45b-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="6f45b-117">Description</span></span>                                                                                            |
|-------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="6f45b-118"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="6f45b-118"><dt>**S\_FALSE**</dt></span></span> </dl>   | <span data-ttu-id="6f45b-119">O Gerenciador do grafo de filtro não está aceitando notificações de eventos.</span><span class="sxs-lookup"><span data-stu-id="6f45b-119">The filter graph manager is not accepting event notifications.</span></span><br/>                              |
| <dl> <span data-ttu-id="6f45b-120"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="6f45b-120"><dt>**S\_OK**</dt></span></span> </dl>      | <span data-ttu-id="6f45b-121">Êxito.</span><span class="sxs-lookup"><span data-stu-id="6f45b-121">Success.</span></span><br/>                                                                                    |
| <dl> <span data-ttu-id="6f45b-122"><dt>**E \_ NOTIMPL**</dt></span><span class="sxs-lookup"><span data-stu-id="6f45b-122"><dt>**E\_NOTIMPL**</dt></span></span> </dl> | <span data-ttu-id="6f45b-123">O filtro não tem um ponteiro para a interface [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) .</span><span class="sxs-lookup"><span data-stu-id="6f45b-123">Filter does not have a pointer to the [**IMediaEventSink**](/windows/desktop/api/Strmif/nn-strmif-imediaeventsink) interface.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="6f45b-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="6f45b-124">Remarks</span></span>

<span data-ttu-id="6f45b-125">Para obter uma lista de códigos de notificação e valores de parâmetros, consulte [códigos de notificação de eventos](event-notification-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6f45b-125">For a list of notification codes and parameter values, see [Event Notification Codes](event-notification-codes.md).</span></span>

<span data-ttu-id="6f45b-126">Na classe base, se o código do evento for EC \_ Complete, o método definirá o parâmetro *EventParam2* como um ponteiro para a interface [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) do filtro.</span><span class="sxs-lookup"><span data-stu-id="6f45b-126">In the base class, if the event code is EC\_COMPLETE, the method sets the *EventParam2* parameter to a pointer to the filter's [**IBaseFilter**](/windows/desktop/api/Strmif/nn-strmif-ibasefilter) interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="6f45b-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6f45b-127">Requirements</span></span>



| <span data-ttu-id="6f45b-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6f45b-128">Requirement</span></span> | <span data-ttu-id="6f45b-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6f45b-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6f45b-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6f45b-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6f45b-131"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6f45b-131"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6f45b-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6f45b-132">Library</span></span><br/> | <dl> <span data-ttu-id="6f45b-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6f45b-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6f45b-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6f45b-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6f45b-135">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="6f45b-135">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




