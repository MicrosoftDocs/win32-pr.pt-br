---
description: A classe CBaseReferenceClock Implementa um relógio de referência.
ms.assetid: 898e1968-a9ab-4bb9-abf0-943bfae502e2
title: Classe CBaseReferenceClock (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1da55a57faac201a2dbf0ef4d8a9774157d9215d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770293"
---
# <a name="cbasereferenceclock-class"></a><span data-ttu-id="5a460-103">Classe CBaseReferenceClock</span><span class="sxs-lookup"><span data-stu-id="5a460-103">CBaseReferenceClock class</span></span>

![hierarquia de classe CBaseReferenceClock](images/rclock01.png)

<span data-ttu-id="5a460-105">A `CBaseReferenceClock` classe implementa um relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="5a460-105">The `CBaseReferenceClock` class implements a reference clock.</span></span>



| <span data-ttu-id="5a460-106">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="5a460-106">Protected Member Variables</span></span>                                                         | <span data-ttu-id="5a460-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a460-107">Description</span></span>                                                                            |
|------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="5a460-108">**\_pSchedule m**</span><span class="sxs-lookup"><span data-stu-id="5a460-108">**m\_pSchedule**</span></span>](cbasereferenceclock-m-pschedule.md)                            | <span data-ttu-id="5a460-109">Objeto [**CAMSchedule**](camschedule.md) que lida com tarefas de agendamento para o relógio.</span><span class="sxs-lookup"><span data-stu-id="5a460-109">[**CAMSchedule**](camschedule.md) object that handles scheduling tasks for the clock.</span></span> |
| <span data-ttu-id="5a460-110">Métodos Protegidos</span><span class="sxs-lookup"><span data-stu-id="5a460-110">Protected Methods</span></span>                                                                  | <span data-ttu-id="5a460-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a460-111">Description</span></span>                                                                            |
| [<span data-ttu-id="5a460-112">**~ CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="5a460-112">**~CBaseReferenceClock**</span></span>](cbasereferenceclock--cbasereferenceclock.md)           | <span data-ttu-id="5a460-113">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="5a460-113">Destructor method.</span></span>                                                                     |
| <span data-ttu-id="5a460-114">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="5a460-114">Public Methods</span></span>                                                                     | <span data-ttu-id="5a460-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a460-115">Description</span></span>                                                                            |
| [<span data-ttu-id="5a460-116">**CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="5a460-116">**CBaseReferenceClock**</span></span>](cbasereferenceclock-cbasereferenceclock.md)             | <span data-ttu-id="5a460-117">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="5a460-117">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="5a460-118">**Getparticulartime**</span><span class="sxs-lookup"><span data-stu-id="5a460-118">**GetPrivateTime**</span></span>](cbasereferenceclock-getprivatetime.md)                       | <span data-ttu-id="5a460-119">Recupera o tempo real do relógio.</span><span class="sxs-lookup"><span data-stu-id="5a460-119">Retrieves the real time from the clock.</span></span>                                                |
| [<span data-ttu-id="5a460-120">**SetTimeDelta**</span><span class="sxs-lookup"><span data-stu-id="5a460-120">**SetTimeDelta**</span></span>](cbasereferenceclock-settimedelta.md)                           | <span data-ttu-id="5a460-121">Ajusta a hora interna do relógio.</span><span class="sxs-lookup"><span data-stu-id="5a460-121">Adjusts the internal clock time.</span></span>                                                       |
| [<span data-ttu-id="5a460-122">**Getschedule**</span><span class="sxs-lookup"><span data-stu-id="5a460-122">**GetSchedule**</span></span>](cbasereferenceclock-getschedule.md)                             | <span data-ttu-id="5a460-123">Recupera um ponteiro para o objeto de agendamento do relógio.</span><span class="sxs-lookup"><span data-stu-id="5a460-123">Retrieves a pointer to the clock's scheduling object.</span></span>                                  |
| [<span data-ttu-id="5a460-124">**TriggerThread**</span><span class="sxs-lookup"><span data-stu-id="5a460-124">**TriggerThread**</span></span>](cbasereferenceclock-triggerthread.md)                         | <span data-ttu-id="5a460-125">Ativa o thread de trabalho que lida com o agendamento.</span><span class="sxs-lookup"><span data-stu-id="5a460-125">Wakes up the worker thread that handles scheduling.</span></span>                                    |
| <span data-ttu-id="5a460-126">Métodos IReferenceClock</span><span class="sxs-lookup"><span data-stu-id="5a460-126">IReferenceClock Methods</span></span>                                                            | <span data-ttu-id="5a460-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a460-127">Description</span></span>                                                                            |
| [<span data-ttu-id="5a460-128">**GetTime**</span><span class="sxs-lookup"><span data-stu-id="5a460-128">**GetTime**</span></span>](cbasereferenceclock-gettime.md)                                     | <span data-ttu-id="5a460-129">Recupera o tempo de referência atual.</span><span class="sxs-lookup"><span data-stu-id="5a460-129">Retrieves the current reference time.</span></span>                                                  |
| [<span data-ttu-id="5a460-130">**Aviso de**</span><span class="sxs-lookup"><span data-stu-id="5a460-130">**AdviseTime**</span></span>](cbasereferenceclock-advisetime.md)                               | <span data-ttu-id="5a460-131">Cria uma solicitação de aviso de uma imagem.</span><span class="sxs-lookup"><span data-stu-id="5a460-131">Creates a one-shot advise request.</span></span>                                                     |
| [<span data-ttu-id="5a460-132">**AdvisePeriodic**</span><span class="sxs-lookup"><span data-stu-id="5a460-132">**AdvisePeriodic**</span></span>](cbasereferenceclock-adviseperiodic.md)                       | <span data-ttu-id="5a460-133">Cria uma solicitação de aviso periódica.</span><span class="sxs-lookup"><span data-stu-id="5a460-133">Creates a periodic advise request.</span></span>                                                     |
| [<span data-ttu-id="5a460-134">**Cancelar**</span><span class="sxs-lookup"><span data-stu-id="5a460-134">**Unadvise**</span></span>](cbasereferenceclock-unadvise.md)                                   | <span data-ttu-id="5a460-135">Remove uma solicitação de aviso pendente.</span><span class="sxs-lookup"><span data-stu-id="5a460-135">Removes a pending advise request.</span></span>                                                      |
| <span data-ttu-id="5a460-136">Métodos IReferenceClockTimerControl</span><span class="sxs-lookup"><span data-stu-id="5a460-136">IReferenceClockTimerControl Methods</span></span>                                                | <span data-ttu-id="5a460-137">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a460-137">Description</span></span>                                                                            |
| [<span data-ttu-id="5a460-138">**GetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="5a460-138">**GetDefaultTimerResolution**</span></span>](cbasereferenceclock-getdefaulttimerresolution.md) | <span data-ttu-id="5a460-139">Retorna a resolução atual do temporizador do relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="5a460-139">Returns the current resolution of the reference clock's timer.</span></span>                         |
| [<span data-ttu-id="5a460-140">**SetDefaultTimerResolution**</span><span class="sxs-lookup"><span data-stu-id="5a460-140">**SetDefaultTimerResolution**</span></span>](cbasereferenceclock-setdefaulttimerresolution.md) | <span data-ttu-id="5a460-141">Define a resolução do timer do relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="5a460-141">Sets the resolution of the reference clock's timer.</span></span>                                    |
| <span data-ttu-id="5a460-142">Funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="5a460-142">Helper Functions</span></span>                                                                   | <span data-ttu-id="5a460-143">Descrição</span><span class="sxs-lookup"><span data-stu-id="5a460-143">Description</span></span>                                                                            |
| [<span data-ttu-id="5a460-144">**ConvertToMilliseconds**</span><span class="sxs-lookup"><span data-stu-id="5a460-144">**ConvertToMilliseconds**</span></span>](converttomilliseconds.md)                             | <span data-ttu-id="5a460-145">Converte um tempo de referência em milissegundos.</span><span class="sxs-lookup"><span data-stu-id="5a460-145">Converts a reference time to milliseconds.</span></span>                                             |



 

## <a name="remarks"></a><span data-ttu-id="5a460-146">Comentários</span><span class="sxs-lookup"><span data-stu-id="5a460-146">Remarks</span></span>

<span data-ttu-id="5a460-147">Essa classe implementa um relógio de referência que dá suporte às interfaces [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) e [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) .</span><span class="sxs-lookup"><span data-stu-id="5a460-147">This class implements a reference clock that supports the [**IReferenceClock**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclock) and [**IReferenceClockTimerControl**](/windows/desktop/api/Strmif/nn-strmif-ireferenceclocktimercontrol) interfaces.</span></span> <span data-ttu-id="5a460-148">Se um filtro puder fornecer um relógio de referência para o grafo de filtro, por exemplo, ao acessar um dispositivo de hardware, ele poderá usar essa classe para implementar o relógio.</span><span class="sxs-lookup"><span data-stu-id="5a460-148">If a filter can provide a reference clock for the filter graph for example, by accessing a hardware device it can use this class to implement the clock.</span></span>

<span data-ttu-id="5a460-149">O `CBaseReferenceClock` objeto mantém dois valores de hora distintos:</span><span class="sxs-lookup"><span data-stu-id="5a460-149">The `CBaseReferenceClock` object maintains two distinct time values:</span></span>

-   <span data-ttu-id="5a460-150">Internamente, o método [**CBaseReferenceClock:: Getparticulartime**](cbasereferenceclock-getprivatetime.md) retorna o tempo real mantido pelo relógio.</span><span class="sxs-lookup"><span data-stu-id="5a460-150">Internally, the [**CBaseReferenceClock::GetPrivateTime**](cbasereferenceclock-getprivatetime.md) method returns the actual time kept by the clock.</span></span>
-   <span data-ttu-id="5a460-151">Externamente, o método [**CBaseReferenceClock:: getTime**](cbasereferenceclock-gettime.md) retorna o tempo de referência para o grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="5a460-151">Externally, the [**CBaseReferenceClock::GetTime**](cbasereferenceclock-gettime.md) method returns the reference time for the filter graph.</span></span>

<span data-ttu-id="5a460-152">É válido para a execução do relógio interno em breves períodos.</span><span class="sxs-lookup"><span data-stu-id="5a460-152">It is valid for the internal clock to run backward over brief periods.</span></span> <span data-ttu-id="5a460-153">Por exemplo, se o relógio for para frente, o filtro poderá ajustá-lo para trás.</span><span class="sxs-lookup"><span data-stu-id="5a460-153">For example, if the clock drifts forward, the filter can adjust it backward.</span></span> <span data-ttu-id="5a460-154">(Consulte [**CBaseReferenceClock:: SetTimeDelta**](cbasereferenceclock-settimedelta.md).) O método **getTime** usa os valores de tempo relatados por **getprivadotime**.</span><span class="sxs-lookup"><span data-stu-id="5a460-154">(See [**CBaseReferenceClock::SetTimeDelta**](cbasereferenceclock-settimedelta.md).) The **GetTime** method uses the time values reported by **GetPrivateTime**.</span></span> <span data-ttu-id="5a460-155">No entanto, o tempo de referência é um aumento monotônico; em outras palavras, ele nunca é executado retroativamente.</span><span class="sxs-lookup"><span data-stu-id="5a460-155">However, the reference time is monotonically increasing; in other words, it never runs backward.</span></span> <span data-ttu-id="5a460-156">Portanto, se o relógio interno for executado retroativamente, **getTime** continuará relatando o tempo antigo até que o relógio interno se ajuste.</span><span class="sxs-lookup"><span data-stu-id="5a460-156">Therefore, if the internal clock runs backward, **GetTime** continues to report the old time until the internal clock catches up.</span></span>

<span data-ttu-id="5a460-157">Por exemplo, os dois métodos podem retornar as seguintes sequências:</span><span class="sxs-lookup"><span data-stu-id="5a460-157">For example, the two methods might return the following sequences:</span></span>

``` syntax
GetPrivateTime: 105, 106, 103, 104, 105, 106, 107, 108
GetTime:        105, 106, 106, 106, 106, 106, 107, 108
```

<span data-ttu-id="5a460-158">No terceiro tique do relógio, o relógio interno salta para o 103.</span><span class="sxs-lookup"><span data-stu-id="5a460-158">On the third clock tick, the internal clock jumps backward to 103.</span></span> <span data-ttu-id="5a460-159">O método **getTime** continua a relatar 106 até que o relógio interno seja atualizado.</span><span class="sxs-lookup"><span data-stu-id="5a460-159">The **GetTime** method continues to report 106 until the internal clock catches up.</span></span>

<span data-ttu-id="5a460-160">Por padrão, **GetPrivateTime** retorna a hora do sistema, por meio de uma chamada para a função **timeGetTime** .</span><span class="sxs-lookup"><span data-stu-id="5a460-160">By default, **GetPrivateTime** returns the system time, through a call to the **timeGetTime** function.</span></span> <span data-ttu-id="5a460-161">Um filtro que está fornecendo um relógio de referência de um dispositivo externo pode executar um dos seguintes procedimentos:</span><span class="sxs-lookup"><span data-stu-id="5a460-161">A filter that is providing a reference clock from an external device can do one of the following:</span></span>

-   <span data-ttu-id="5a460-162">Substitua **GetPrivateTime** para retornar a hora do dispositivo.</span><span class="sxs-lookup"><span data-stu-id="5a460-162">Override **GetPrivateTime** to return the time from the device.</span></span>
-   <span data-ttu-id="5a460-163">Monitore a discrepância entre a hora do dispositivo e a hora do sistema e chame **SetTimeDelta** para fazer correções.</span><span class="sxs-lookup"><span data-stu-id="5a460-163">Monitor the discrepancy between the device time and the system time, and call **SetTimeDelta** to make corrections.</span></span>

<span data-ttu-id="5a460-164">Essa classe usa um objeto [**CAMSchedule**](camschedule.md) para lidar com o agendamento de solicitações de aviso.</span><span class="sxs-lookup"><span data-stu-id="5a460-164">This class uses a [**CAMSchedule**](camschedule.md) object to handle scheduling of advise requests.</span></span> <span data-ttu-id="5a460-165">Para obter detalhes, consulte a documentação da classe **CAMSchedule** .</span><span class="sxs-lookup"><span data-stu-id="5a460-165">For details, see the documentation for the **CAMSchedule** class.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a460-166">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5a460-166">Requirements</span></span>



| <span data-ttu-id="5a460-167">Requisito</span><span class="sxs-lookup"><span data-stu-id="5a460-167">Requirement</span></span> | <span data-ttu-id="5a460-168">Valor</span><span class="sxs-lookup"><span data-stu-id="5a460-168">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a460-169">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5a460-169">Header</span></span><br/>  | <dl> <span data-ttu-id="5a460-170"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5a460-170"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5a460-171">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5a460-171">Library</span></span><br/> | <dl> <span data-ttu-id="5a460-172"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5a460-172"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




