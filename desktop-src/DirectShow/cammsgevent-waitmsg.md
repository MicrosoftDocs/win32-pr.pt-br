---
description: O método WaitMsg aguarda o evento ser sinalizado, enquanto envia mensagens enviadas.
ms.assetid: 5cab98ca-f9f3-4c7c-9ce2-8e16109d8fbb
title: Método CAMMsgEvent. WaitMsg (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent.WaitMsg
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9622e962f130a082a5c1206367f4850cebb6ce02
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752313"
---
# <a name="cammsgeventwaitmsg-method"></a><span data-ttu-id="1d583-103">Método CAMMsgEvent. WaitMsg</span><span class="sxs-lookup"><span data-stu-id="1d583-103">CAMMsgEvent.WaitMsg method</span></span>

<span data-ttu-id="1d583-104">O `WaitMsg` método aguarda que o evento seja sinalizado, enquanto envia mensagens enviadas.</span><span class="sxs-lookup"><span data-stu-id="1d583-104">The `WaitMsg` method waits for the event to be signaled, while dispatching sent messages.</span></span>

## <a name="syntax"></a><span data-ttu-id="1d583-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="1d583-105">Syntax</span></span>


```C++
BOOL WaitMsg(
   DWORD dwTimeOut = INFINITE
);
```



## <a name="parameters"></a><span data-ttu-id="1d583-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="1d583-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1d583-107">*dwTimeOut*</span><span class="sxs-lookup"><span data-stu-id="1d583-107">*dwTimeOut*</span></span> 
</dt> <dd>

<span data-ttu-id="1d583-108">Valor de tempo limite opcional, em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="1d583-108">Optional time-out value, in milliseconds.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1d583-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="1d583-109">Return value</span></span>

<span data-ttu-id="1d583-110">Retornará **true** se o evento for sinalizado ou **false** se o tempo limite tiver ocorrido.</span><span class="sxs-lookup"><span data-stu-id="1d583-110">Returns **TRUE** if the event is signaled, or **FALSE** if the time-out occurred.</span></span>

## <a name="remarks"></a><span data-ttu-id="1d583-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="1d583-111">Remarks</span></span>

<span data-ttu-id="1d583-112">Esse método chama a função PeekMessage para processar mensagens.</span><span class="sxs-lookup"><span data-stu-id="1d583-112">This method calls the PeekMessage function to process messages.</span></span> <span data-ttu-id="1d583-113">Chame esse método em vez de [**CAMEvent:: Wait**](camevent-wait.md) se seu thread precisar processar mensagens enquanto aguarda um evento.</span><span class="sxs-lookup"><span data-stu-id="1d583-113">Call this method instead of [**CAMEvent::Wait**](camevent-wait.md) if your thread needs to process messages while waiting for an event.</span></span> <span data-ttu-id="1d583-114">Se o thread não processar mensagens e outro thread enviar uma mensagem, o deadlock poderá ocorrer.</span><span class="sxs-lookup"><span data-stu-id="1d583-114">If the thread does not process messages and another thread sends a message, deadlock could occur.</span></span>

<span data-ttu-id="1d583-115">Por exemplo, suponha que você crie um thread e, em seguida, bloqueie até que o thread seja inicializado.</span><span class="sxs-lookup"><span data-stu-id="1d583-115">For example, suppose you create a thread and then block until the thread initializes.</span></span> <span data-ttu-id="1d583-116">Se o thread enviar uma mensagem à sua janela chamando a função SendMessage, isso resultará em um deadlock.</span><span class="sxs-lookup"><span data-stu-id="1d583-116">If the thread sends a message to your window by calling the SendMessage function, it will result in a deadlock.</span></span> <span data-ttu-id="1d583-117">Isso ocorre porque SendMessage não retorna até que a mensagem seja processada.</span><span class="sxs-lookup"><span data-stu-id="1d583-117">This is because SendMessage does not return until the message has been processed.</span></span> <span data-ttu-id="1d583-118">Chamar WaitMsg permite que a chamada SendMessage seja retornada, impedindo o deadlock.</span><span class="sxs-lookup"><span data-stu-id="1d583-118">Calling WaitMsg allows the SendMessage call to return, preventing the deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="1d583-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1d583-119">Requirements</span></span>



| <span data-ttu-id="1d583-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="1d583-120">Requirement</span></span> | <span data-ttu-id="1d583-121">Valor</span><span class="sxs-lookup"><span data-stu-id="1d583-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1d583-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1d583-122">Header</span></span><br/>  | <dl> <span data-ttu-id="1d583-123"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1d583-123"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1d583-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1d583-124">Library</span></span><br/> | <dl> <span data-ttu-id="1d583-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1d583-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1d583-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="1d583-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1d583-127">**Classe CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="1d583-127">**CAMMsgEvent Class**</span></span>](cammsgevent.md)
</dt> </dl>

 

 




