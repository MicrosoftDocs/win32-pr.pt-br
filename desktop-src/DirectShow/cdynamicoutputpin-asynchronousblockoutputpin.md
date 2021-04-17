---
description: O método AsynchronousBlockOutputPin bloqueia o PIN. O método pode retornar antes de o PIN ser bloqueado.
ms.assetid: 14cdc973-f0d3-4d1b-8491-67c1421f630b
title: Método CDynamicOutputPin. AsynchronousBlockOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.AsynchronousBlockOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 67232bf1081f9c9ea088968cb6c5d02667b00eeb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752290"
---
# <a name="cdynamicoutputpinasynchronousblockoutputpin-method"></a><span data-ttu-id="c4c37-104">Método CDynamicOutputPin. AsynchronousBlockOutputPin</span><span class="sxs-lookup"><span data-stu-id="c4c37-104">CDynamicOutputPin.AsynchronousBlockOutputPin method</span></span>

<span data-ttu-id="c4c37-105">O `AsynchronousBlockOutputPin` método bloqueia o PIN.</span><span class="sxs-lookup"><span data-stu-id="c4c37-105">The `AsynchronousBlockOutputPin` method blocks the pin.</span></span> <span data-ttu-id="c4c37-106">O método pode retornar antes de o PIN ser bloqueado.</span><span class="sxs-lookup"><span data-stu-id="c4c37-106">The method might return before the pin is blocked.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4c37-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c4c37-107">Syntax</span></span>


```C++
HRESULT AsynchronousBlockOutputPin(
   HANDLE hNotifyCallerPinBlockedEvent
);
```



## <a name="parameters"></a><span data-ttu-id="c4c37-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c4c37-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4c37-109">*hNotifyCallerPinBlockedEvent*</span><span class="sxs-lookup"><span data-stu-id="c4c37-109">*hNotifyCallerPinBlockedEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="c4c37-110">Identificador para um evento.</span><span class="sxs-lookup"><span data-stu-id="c4c37-110">Handle to an event.</span></span> <span data-ttu-id="c4c37-111">O evento é sinalizado quando o pino de saída é bloqueado ou se o chamador cancela a operação de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="c4c37-111">The event is signaled when the output pin is blocked, or if the caller cancels the block operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4c37-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c4c37-112">Return value</span></span>

<span data-ttu-id="c4c37-113">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c4c37-113">Returns an **HRESULT** value.</span></span> <span data-ttu-id="c4c37-114">Os valores possíveis incluem os mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="c4c37-114">Possible values include those shown in the following table.</span></span>



| <span data-ttu-id="c4c37-115">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="c4c37-115">Return code</span></span>                                                                                                                    | <span data-ttu-id="c4c37-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="c4c37-116">Description</span></span>                                              |
|--------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------|
| <dl> <span data-ttu-id="c4c37-117"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c37-117"><dt>**S\_OK**</dt></span></span> </dl>                                           | <span data-ttu-id="c4c37-118">Êxito.</span><span class="sxs-lookup"><span data-stu-id="c4c37-118">Success.</span></span><br/>                                      |
| <dl> <span data-ttu-id="c4c37-119"><dt>**VFW \_ E \_ PIN \_ já \_ bloqueados**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c37-119"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED**</dt></span></span> </dl>                   | <span data-ttu-id="c4c37-120">O PIN já está bloqueado em outro thread.</span><span class="sxs-lookup"><span data-stu-id="c4c37-120">Pin is already blocked on another thread.</span></span><br/>     |
| <dl> <span data-ttu-id="c4c37-121"><dt>**VFW \_ E \_ PIN \_ já \_ bloqueados neste \_ \_ \_ thread**</dt></span><span class="sxs-lookup"><span data-stu-id="c4c37-121"><dt>**VFW\_E\_PIN\_ALREADY\_BLOCKED\_ON\_THIS\_THREAD**</dt></span></span> </dl> | <span data-ttu-id="c4c37-122">O PIN já está bloqueado no thread de chamada.</span><span class="sxs-lookup"><span data-stu-id="c4c37-122">Pin is already blocked on the calling thread.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="c4c37-123">Comentários</span><span class="sxs-lookup"><span data-stu-id="c4c37-123">Remarks</span></span>

<span data-ttu-id="c4c37-124">Não chame esse método do thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="c4c37-124">Do not call this method from the streaming thread.</span></span>

<span data-ttu-id="c4c37-125">Se nenhum thread de streaming estiver usando o PIN, esse método bloqueará imediatamente o PIN.</span><span class="sxs-lookup"><span data-stu-id="c4c37-125">If no streaming thread is using the pin, this method immediately blocks the pin.</span></span> <span data-ttu-id="c4c37-126">Caso contrário, ele define o status do PIN como "Pending" e retorna.</span><span class="sxs-lookup"><span data-stu-id="c4c37-126">Otherwise, it sets the pin status to "pending" and returns.</span></span> <span data-ttu-id="c4c37-127">Quando a operação de streaming é concluída, o thread de streaming chama o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) , que bloqueia o PIN e sinaliza o evento **hNotifyCallerPinBlockedEvent** .</span><span class="sxs-lookup"><span data-stu-id="c4c37-127">When the streaming operation completes, the streaming thread calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method, which blocks the pin and signals the **hNotifyCallerPinBlockedEvent** event.</span></span> <span data-ttu-id="c4c37-128">Para cancelar um bloco pendente, chame o método [**CDynamicOutputPin:: UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="c4c37-128">To cancel a pending block, call the [**CDynamicOutputPin::UnblockOutputPin**](cdynamicoutputpin-unblockoutputpin.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4c37-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c4c37-129">Requirements</span></span>



| <span data-ttu-id="c4c37-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="c4c37-130">Requirement</span></span> | <span data-ttu-id="c4c37-131">Valor</span><span class="sxs-lookup"><span data-stu-id="c4c37-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c4c37-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c4c37-132">Header</span></span><br/>  | <dl> <span data-ttu-id="c4c37-133"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c37-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c4c37-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c4c37-134">Library</span></span><br/> | <dl> <span data-ttu-id="c4c37-135"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c4c37-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c4c37-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="c4c37-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4c37-137">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="c4c37-137">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




