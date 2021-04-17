---
description: O método StartUsingOutputPin obtém acesso ao PIN para uma operação de streaming.
ms.assetid: afa627a9-00fd-4ad0-b674-9c54a5a1be55
title: Método CDynamicOutputPin. StartUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.StartUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1c5ea7386c896f6b989a47c2574dfa4d61eacb5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748811"
---
# <a name="cdynamicoutputpinstartusingoutputpin-method"></a><span data-ttu-id="7cb1c-103">Método CDynamicOutputPin. StartUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="7cb1c-103">CDynamicOutputPin.StartUsingOutputPin method</span></span>

<span data-ttu-id="7cb1c-104">O `StartUsingOutputPin` método obtém acesso ao PIN para uma operação de streaming.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-104">The `StartUsingOutputPin` method obtains access to the pin for a streaming operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="7cb1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7cb1c-105">Syntax</span></span>


```C++
virtual HRESULT StartUsingOutputPin();
```



## <a name="parameters"></a><span data-ttu-id="7cb1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7cb1c-106">Parameters</span></span>

<span data-ttu-id="7cb1c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7cb1c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7cb1c-108">Return value</span></span>

<span data-ttu-id="7cb1c-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="7cb1c-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="7cb1c-110">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-110">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="7cb1c-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7cb1c-111">Return code</span></span>                                                                                           | <span data-ttu-id="7cb1c-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="7cb1c-112">Description</span></span>                                                       |
|-------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------|
| <dl> <span data-ttu-id="7cb1c-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7cb1c-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="7cb1c-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-114">Success.</span></span><br/>                                               |
| <dl> <span data-ttu-id="7cb1c-115"><dt>**E \_ inesperado**</dt></span><span class="sxs-lookup"><span data-stu-id="7cb1c-115"><dt>**E\_UNEXPECTED**</dt></span></span> </dl>          | <span data-ttu-id="7cb1c-116">Erro inesperado.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-116">Unexpected error.</span></span><br/>                                      |
| <dl> <span data-ttu-id="7cb1c-117"><dt>**VFW \_ E \_ estado \_ alterado**</dt></span><span class="sxs-lookup"><span data-stu-id="7cb1c-117"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="7cb1c-118">O filtro foi interrompido ou o PIN começou a ser liberado.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-118">The filter was stopped, or the pin has begun flushing.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7cb1c-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="7cb1c-119">Remarks</span></span>

<span data-ttu-id="7cb1c-120">Chame esse método antes de chamar quaisquer métodos que entreguem dados ao PIN de entrada conectado ou que alterem o tipo de mídia da conexão.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-120">Call this method before calling any methods that deliver data to the connected input pin or that change the connection's media type.</span></span> <span data-ttu-id="7cb1c-121">Por exemplo, essa regra se aplica aos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="7cb1c-121">For example, this rule applies to the following methods:</span></span>

-   [<span data-ttu-id="7cb1c-122">**CDynamicOutputPin::ChangeOutputFormat**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-122">**CDynamicOutputPin::ChangeOutputFormat**</span></span>](cdynamicoutputpin-changeoutputformat.md)
-   [<span data-ttu-id="7cb1c-123">**CDynamicOutputPin::ChangeMediaType**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-123">**CDynamicOutputPin::ChangeMediaType**</span></span>](cdynamicoutputpin-changemediatype.md)
-   [<span data-ttu-id="7cb1c-124">**CDynamicOutputPin::D ynamicReconnect**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-124">**CDynamicOutputPin::DynamicReconnect**</span></span>](cdynamicoutputpin-dynamicreconnect.md)
-   [<span data-ttu-id="7cb1c-125">**CBaseOutputPin::D eliver**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-125">**CBaseOutputPin::Deliver**</span></span>](cbaseoutputpin-deliver.md)
-   [<span data-ttu-id="7cb1c-126">**CBaseOutputPin::D eliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-126">**CBaseOutputPin::DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md)
-   [<span data-ttu-id="7cb1c-127">**CBaseOutputPin::D eliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-127">**CBaseOutputPin::DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)
-   [<span data-ttu-id="7cb1c-128">**IMemInputPin:: receber**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-128">**IMemInputPin::Receive**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive)
-   [<span data-ttu-id="7cb1c-129">**IMemInputPin::ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-129">**IMemInputPin::ReceiveMultiple**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple)
-   [<span data-ttu-id="7cb1c-130">**IPin::EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-130">**IPin::EndOfStream**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream)
-   [<span data-ttu-id="7cb1c-131">**IPin::NewSegment**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-131">**IPin::NewSegment**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment)

<span data-ttu-id="7cb1c-132">Depois, chame o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) para liberar o acesso ao PIN.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-132">Afterward, call the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method to release the access to the pin.</span></span>

<span data-ttu-id="7cb1c-133">Se o PIN estiver bloqueado, o `StartUsingOutputPin` aguardará que o PIN se torne desbloqueado.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-133">If the pin is blocked, `StartUsingOutputPin` waits for the pin to become unblocked.</span></span> <span data-ttu-id="7cb1c-134">Se o filtro for interrompido enquanto o método estiver aguardando, o método retornará imediatamente o \_ estado E VFW \_ \_ alterado.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-134">If the filter stops while the method is waiting, the method immediately returns VFW\_E\_STATE\_CHANGED.</span></span> <span data-ttu-id="7cb1c-135">O PIN mantém uma contagem de quantas vezes `StartUsingOutputPin` foi chamado sem uma chamada correspondente para **StopUsingOutputPin**.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-135">The pin maintains a count of how many times `StartUsingOutputPin` has been called without a corresponding call to **StopUsingOutputPin**.</span></span> <span data-ttu-id="7cb1c-136">Se outro thread tentar bloquear o PIN enquanto essa contagem for diferente de zero, o PIN definirá seu status de bloqueio como "pendente".</span><span class="sxs-lookup"><span data-stu-id="7cb1c-136">If another thread tries to block the pin while this count is non-zero, the pin sets its blocking status to "pending."</span></span> <span data-ttu-id="7cb1c-137">O PIN fica bloqueado depois que todas as operações de streaming são concluídas, na chamada final para **StopUsingOutputPin**.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-137">The pin becomes blocked once all of the streaming operations have completed, in the final call to **StopUsingOutputPin**.</span></span>

<span data-ttu-id="7cb1c-138">Não mantenha a seção crítica [**CDynamicOutputPin:: m \_ BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) ao chamar esse método.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-138">Do not hold the [**CDynamicOutputPin::m\_BlockStateLock**](cdynamicoutputpin-m-blockstatelock.md) critical section when you call this method.</span></span> <span data-ttu-id="7cb1c-139">Caso contrário, se o PIN for bloqueado, ele nunca poderá ser desbloqueado, causando um deadlock.</span><span class="sxs-lookup"><span data-stu-id="7cb1c-139">Otherwise, if the pin is blocked, it can never become unblocked, causing a deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="7cb1c-140">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7cb1c-140">Requirements</span></span>



| <span data-ttu-id="7cb1c-141">Requisito</span><span class="sxs-lookup"><span data-stu-id="7cb1c-141">Requirement</span></span> | <span data-ttu-id="7cb1c-142">Valor</span><span class="sxs-lookup"><span data-stu-id="7cb1c-142">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7cb1c-143">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7cb1c-143">Header</span></span><br/>  | <dl> <span data-ttu-id="7cb1c-144"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7cb1c-144"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="7cb1c-145">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7cb1c-145">Library</span></span><br/> | <dl> <span data-ttu-id="7cb1c-146"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7cb1c-146"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7cb1c-147">Confira também</span><span class="sxs-lookup"><span data-stu-id="7cb1c-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7cb1c-148">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="7cb1c-148">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




