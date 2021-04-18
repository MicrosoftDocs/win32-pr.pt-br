---
description: A classe CAMSchedule implementa um Agendador para relógios de referência.
ms.assetid: 67aacffb-b781-4323-8973-355a76821401
title: Classe CAMSchedule (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bef8ad07347284c53a3490c21032070788fa3ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764589"
---
# <a name="camschedule-class"></a><span data-ttu-id="7f423-103">Classe CAMSchedule</span><span class="sxs-lookup"><span data-stu-id="7f423-103">CAMSchedule class</span></span>

<span data-ttu-id="7f423-104">A `CAMSchedule` classe implementa um Agendador para relógios de referência.</span><span class="sxs-lookup"><span data-stu-id="7f423-104">The `CAMSchedule` class implements a scheduler for reference clocks.</span></span>



| <span data-ttu-id="7f423-105">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="7f423-105">Public Methods</span></span>                                             | <span data-ttu-id="7f423-106">Descrição</span><span class="sxs-lookup"><span data-stu-id="7f423-106">Description</span></span>                                                                          |
|------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="7f423-107">**CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="7f423-107">**CAMSchedule**</span></span>](camschedule-camschedule.md)             | <span data-ttu-id="7f423-108">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="7f423-108">Constructor method.</span></span>                                                                  |
| [<span data-ttu-id="7f423-109">**~ CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="7f423-109">**~CAMSchedule**</span></span>](camschedule--camschedule.md)           | <span data-ttu-id="7f423-110">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="7f423-110">Destructor method.</span></span> <span data-ttu-id="7f423-111">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="7f423-111">Virtual.</span></span>                                                          |
| [<span data-ttu-id="7f423-112">**GetAdviseCount**</span><span class="sxs-lookup"><span data-stu-id="7f423-112">**GetAdviseCount**</span></span>](camschedule-getadvisecount.md)       | <span data-ttu-id="7f423-113">Recupera o número de solicitações de aviso pendentes.</span><span class="sxs-lookup"><span data-stu-id="7f423-113">Retrieves the number of pending advise requests.</span></span>                                     |
| [<span data-ttu-id="7f423-114">**GetNextAdviseTime**</span><span class="sxs-lookup"><span data-stu-id="7f423-114">**GetNextAdviseTime**</span></span>](camschedule-getnextadvisetime.md) | <span data-ttu-id="7f423-115">Recupera a hora da próxima solicitação de aviso.</span><span class="sxs-lookup"><span data-stu-id="7f423-115">Retrieves the time of the next advise request.</span></span>                                       |
| [<span data-ttu-id="7f423-116">**AddAdvisePacket**</span><span class="sxs-lookup"><span data-stu-id="7f423-116">**AddAdvisePacket**</span></span>](camschedule-addadvisepacket.md)     | <span data-ttu-id="7f423-117">Adiciona uma solicitação de aviso à lista de solicitações pendentes.</span><span class="sxs-lookup"><span data-stu-id="7f423-117">Adds an advise request to the list of pending requests.</span></span>                              |
| [<span data-ttu-id="7f423-118">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="7f423-118">**Unadvise**</span></span>](camschedule-unadvise.md)                   | <span data-ttu-id="7f423-119">Remove uma solicitação de aviso.</span><span class="sxs-lookup"><span data-stu-id="7f423-119">Removes an advise request.</span></span>                                                           |
| [<span data-ttu-id="7f423-120">**Aconselhamos**</span><span class="sxs-lookup"><span data-stu-id="7f423-120">**Advise**</span></span>](camschedule-advise.md)                       | <span data-ttu-id="7f423-121">Despacha todas as solicitações agendadas para um período especificado ou anterior.</span><span class="sxs-lookup"><span data-stu-id="7f423-121">Dispatches all requests that are scheduled for a specified time or earlier.</span></span>          |
| [<span data-ttu-id="7f423-122">**GetEvent**</span><span class="sxs-lookup"><span data-stu-id="7f423-122">**GetEvent**</span></span>](camschedule-getevent.md)                   | <span data-ttu-id="7f423-123">Recupera um identificador de evento, que é usado para sinalizar uma alteração no próximo horário de aviso.</span><span class="sxs-lookup"><span data-stu-id="7f423-123">Retrieves an event handle, which is used to signal a change in the next advise time.</span></span> |



 

## <a name="remarks"></a><span data-ttu-id="7f423-124">Comentários</span><span class="sxs-lookup"><span data-stu-id="7f423-124">Remarks</span></span>

<span data-ttu-id="7f423-125">Esse objeto auxiliar mantém uma lista de solicitações de aviso para um relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="7f423-125">This helper object maintains a list of advise requests for a reference clock.</span></span> <span data-ttu-id="7f423-126">A classe [**CBaseReferenceClock**](cbasereferenceclock.md) a usa para ajudar a agendar solicitações de aviso.</span><span class="sxs-lookup"><span data-stu-id="7f423-126">The [**CBaseReferenceClock**](cbasereferenceclock.md) class uses it to help schedule advise requests.</span></span> <span data-ttu-id="7f423-127">Os relógios usam esse objeto da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="7f423-127">Clocks use this object in the following manner:</span></span>

1.  <span data-ttu-id="7f423-128">O relógio cria um thread de trabalho para lidar com o agendamento.</span><span class="sxs-lookup"><span data-stu-id="7f423-128">The clock creates a worker thread to handle scheduling.</span></span>
2.  <span data-ttu-id="7f423-129">O thread de trabalho chama o método [**CAMSchedule:: getuniforme**](camschedule-getevent.md) para recuperar um identificador de evento do Agendador.</span><span class="sxs-lookup"><span data-stu-id="7f423-129">The worker thread calls the [**CAMSchedule::GetEvent**](camschedule-getevent.md) method to retrieve an event handle from the scheduler.</span></span> <span data-ttu-id="7f423-130">Ele aguarda esse evento, inicialmente com um tempo limite infinito.</span><span class="sxs-lookup"><span data-stu-id="7f423-130">It waits on this event, initially with an infinite time-out.</span></span>
3.  <span data-ttu-id="7f423-131">Para agendar uma nova solicitação de aviso, o relógio chama o método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="7f423-131">To schedule a new advise request, the clock calls the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span> <span data-ttu-id="7f423-132">Uma solicitação de aviso pode ser uma única imagem ou periódica.</span><span class="sxs-lookup"><span data-stu-id="7f423-132">An advise request can be one-shot or periodic.</span></span> <span data-ttu-id="7f423-133">O Agendador mantém a lista de solicitações na ordem de tempo.</span><span class="sxs-lookup"><span data-stu-id="7f423-133">The scheduler keeps the list of requests in time order.</span></span>
4.  <span data-ttu-id="7f423-134">Se uma solicitação for adicionada à frente da lista, o Agendador sinalizará o evento.</span><span class="sxs-lookup"><span data-stu-id="7f423-134">If a request is added to the front of the list, the scheduler signals the event.</span></span> <span data-ttu-id="7f423-135">(A lista está vazia a princípio, portanto, a primeira solicitação é garantida para sinalizar o evento.)</span><span class="sxs-lookup"><span data-stu-id="7f423-135">(The list is empty at first, so the first request is guaranteed to signal the event.)</span></span>
5.  <span data-ttu-id="7f423-136">Quando o evento é sinalizado, o thread de trabalho chama o método [**CAMSchedule:: Advise**](camschedule-advise.md) , especificando o tempo de referência atual.</span><span class="sxs-lookup"><span data-stu-id="7f423-136">When the event is signaled, the worker thread calls the [**CAMSchedule::Advise**](camschedule-advise.md) method, specifying the current reference time.</span></span> <span data-ttu-id="7f423-137">Se todas as solicitações pendentes tiverem expirado, o Agendador as expedirá.</span><span class="sxs-lookup"><span data-stu-id="7f423-137">If any pending requests have expired, the scheduler dispatches them.</span></span>
6.  <span data-ttu-id="7f423-138">O método Advise retorna a hora da próxima solicitação.</span><span class="sxs-lookup"><span data-stu-id="7f423-138">The Advise method returns the time of the next request.</span></span> <span data-ttu-id="7f423-139">O thread de trabalho usa esse valor para calcular um novo valor de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="7f423-139">The worker thread uses this value to calculate a new time-out value.</span></span>
7.  <span data-ttu-id="7f423-140">As etapas 2 6 repetim indefinidamente.</span><span class="sxs-lookup"><span data-stu-id="7f423-140">Steps 2 6 repeat indefinitely.</span></span>
8.  <span data-ttu-id="7f423-141">Para encerrar o thread de trabalho, o relógio define um sinalizador interno e sinaliza o evento.</span><span class="sxs-lookup"><span data-stu-id="7f423-141">To terminate the worker thread, the clock sets an internal flag and signals the event.</span></span>

<span data-ttu-id="7f423-142">Na etapa 2, o evento é sinalizado ou a espera atinge o tempo limite. Se o evento for sinalizado, significa que uma nova solicitação foi adicionada à frente da lista.</span><span class="sxs-lookup"><span data-stu-id="7f423-142">In step 2, either the event is signaled, or the wait times out. If the event is signaled, it means that a new request was added to the front of the list.</span></span> <span data-ttu-id="7f423-143">O thread de trabalho deve calcular um novo valor de tempo limite.</span><span class="sxs-lookup"><span data-stu-id="7f423-143">The worker thread must calculate a new time-out value.</span></span> <span data-ttu-id="7f423-144">Por outro lado, se a espera atingir o tempo limite, significa que uma solicitação de aviso já chegou e deve ser expedida.</span><span class="sxs-lookup"><span data-stu-id="7f423-144">On the other hand, if the wait times out, it means that an advise request has come due and must be dispatched.</span></span> <span data-ttu-id="7f423-145">A chamada para Advise na etapa 5 lida com ambos os casos.</span><span class="sxs-lookup"><span data-stu-id="7f423-145">The call to Advise in step 5 handles both cases.</span></span>

## <a name="requirements"></a><span data-ttu-id="7f423-146">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7f423-146">Requirements</span></span>



| <span data-ttu-id="7f423-147">Requisito</span><span class="sxs-lookup"><span data-stu-id="7f423-147">Requirement</span></span> | <span data-ttu-id="7f423-148">Valor</span><span class="sxs-lookup"><span data-stu-id="7f423-148">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7f423-149">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7f423-149">Header</span></span><br/>  | <dl> <span data-ttu-id="7f423-150"><dt>Dsschedule. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7f423-150"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="7f423-151">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7f423-151">Library</span></span><br/> | <dl> <span data-ttu-id="7f423-152"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7f423-152"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




