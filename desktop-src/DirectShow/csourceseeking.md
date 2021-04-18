---
description: A classe CSourceSeeking é uma classe abstrata para implementar a busca em filtros de origem com um PIN de saída.
ms.assetid: 46e711e1-78d4-4e83-9df1-06032edeba6a
title: Classe CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cf9bf0ca0fabd00c27f4ef4b795af5271605fa8a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105767683"
---
# <a name="csourceseeking-class"></a><span data-ttu-id="f550d-103">Classe CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="f550d-103">CSourceSeeking class</span></span>

![hierarquia de classe CSourceSeeking](images/cutil15.png)

<span data-ttu-id="f550d-105">A classe **CSourceSeeking** é uma classe abstrata para implementar a busca em filtros de origem com um PIN de saída.</span><span class="sxs-lookup"><span data-stu-id="f550d-105">The **CSourceSeeking** class is an abstract class for implementing seeking in source filters with one output pin.</span></span>

<span data-ttu-id="f550d-106">Essa classe dá suporte à interface [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) .</span><span class="sxs-lookup"><span data-stu-id="f550d-106">This class supports the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) interface.</span></span> <span data-ttu-id="f550d-107">Ele fornece implementações padrão para todos os métodos **IMediaSeeking** .</span><span class="sxs-lookup"><span data-stu-id="f550d-107">It provides default implementations for all of the **IMediaSeeking** methods.</span></span> <span data-ttu-id="f550d-108">As variáveis de membro protegidas armazenam a hora de início, a hora de parada e a taxa atual.</span><span class="sxs-lookup"><span data-stu-id="f550d-108">Protected member variables store the start time, stop time, and current rate.</span></span> <span data-ttu-id="f550d-109">Por padrão, o único formato de tempo com suporte da classe é o formato de tempo de **\_ \_ mídia \_** (unidades de 100 a nanossegundos).</span><span class="sxs-lookup"><span data-stu-id="f550d-109">By default, the only time format supported by the class is **TIME\_FORMAT\_MEDIA\_TIME** (100-nanosecond units).</span></span> <span data-ttu-id="f550d-110">Consulte comentários para obter mais informações.</span><span class="sxs-lookup"><span data-stu-id="f550d-110">See Remarks for more information.</span></span>



| <span data-ttu-id="f550d-111">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="f550d-111">Protected Member Variables</span></span>                                          | <span data-ttu-id="f550d-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="f550d-112">Description</span></span>                                                                                 |
|---------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| [<span data-ttu-id="f550d-113">**\_rtDuration m**</span><span class="sxs-lookup"><span data-stu-id="f550d-113">**m\_rtDuration**</span></span>](csourceseeking-m-rtduration.md)                | <span data-ttu-id="f550d-114">Duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f550d-114">Duration of the stream.</span></span>                                                                     |
| [<span data-ttu-id="f550d-115">**\_rtStart m**</span><span class="sxs-lookup"><span data-stu-id="f550d-115">**m\_rtStart**</span></span>](csourceseeking-m-rtstart.md)                      | <span data-ttu-id="f550d-116">Hora de início.</span><span class="sxs-lookup"><span data-stu-id="f550d-116">Start time.</span></span>                                                                                 |
| [<span data-ttu-id="f550d-117">**\_rtStop m**</span><span class="sxs-lookup"><span data-stu-id="f550d-117">**m\_rtStop**</span></span>](csourceseeking-m-rtstop.md)                        | <span data-ttu-id="f550d-118">Hora de parada.</span><span class="sxs-lookup"><span data-stu-id="f550d-118">Stop time.</span></span>                                                                                  |
| [<span data-ttu-id="f550d-119">**\_dRateSeeking m**</span><span class="sxs-lookup"><span data-stu-id="f550d-119">**m\_dRateSeeking**</span></span>](csourceseeking-m-drateseeking.md)            | <span data-ttu-id="f550d-120">Taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f550d-120">Playback rate.</span></span>                                                                              |
| [<span data-ttu-id="f550d-121">**\_dwSeekingCaps m**</span><span class="sxs-lookup"><span data-stu-id="f550d-121">**m\_dwSeekingCaps**</span></span>](csourceseeking-m-dwseekingcaps.md)          | <span data-ttu-id="f550d-122">Buscando recursos.</span><span class="sxs-lookup"><span data-stu-id="f550d-122">Seeking capabilities.</span></span>                                                                       |
| [<span data-ttu-id="f550d-123">**\_pLock m**</span><span class="sxs-lookup"><span data-stu-id="f550d-123">**m\_pLock**</span></span>](csourceseeking-m-plock.md)                          | <span data-ttu-id="f550d-124">Ponteiro para um objeto de seção crítica para bloqueio.</span><span class="sxs-lookup"><span data-stu-id="f550d-124">Pointer to a critical section object for locking.</span></span>                                           |
| <span data-ttu-id="f550d-125">Métodos Protegidos</span><span class="sxs-lookup"><span data-stu-id="f550d-125">Protected Methods</span></span>                                                   | <span data-ttu-id="f550d-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="f550d-126">Description</span></span>                                                                                 |
| [<span data-ttu-id="f550d-127">**CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="f550d-127">**CSourceSeeking**</span></span>](csourceseeking-csourceseeking.md)             | <span data-ttu-id="f550d-128">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="f550d-128">Constructor method.</span></span>                                                                         |
| <span data-ttu-id="f550d-129">Métodos virtuais puros</span><span class="sxs-lookup"><span data-stu-id="f550d-129">Pure Virtual Methods</span></span>                                                | <span data-ttu-id="f550d-130">Descrição</span><span class="sxs-lookup"><span data-stu-id="f550d-130">Description</span></span>                                                                                 |
| [<span data-ttu-id="f550d-131">**Trocador**</span><span class="sxs-lookup"><span data-stu-id="f550d-131">**ChangeRate**</span></span>](csourceseeking-changerate.md)                     | <span data-ttu-id="f550d-132">Chamado quando a taxa de reprodução é alterada.</span><span class="sxs-lookup"><span data-stu-id="f550d-132">Called when the playback rate changes.</span></span>                                                      |
| [<span data-ttu-id="f550d-133">**Altere**</span><span class="sxs-lookup"><span data-stu-id="f550d-133">**ChangeStart**</span></span>](csourceseeking-changestart.md)                   | <span data-ttu-id="f550d-134">Chamado quando a posição inicial é alterada.</span><span class="sxs-lookup"><span data-stu-id="f550d-134">Called when the start position changes.</span></span>                                                     |
| [<span data-ttu-id="f550d-135">**ChangeStop**</span><span class="sxs-lookup"><span data-stu-id="f550d-135">**ChangeStop**</span></span>](csourceseeking-changestop.md)                     | <span data-ttu-id="f550d-136">Chamado quando a posição de parada é alterada.</span><span class="sxs-lookup"><span data-stu-id="f550d-136">Called when the stop position changes.</span></span>                                                      |
| <span data-ttu-id="f550d-137">Métodos IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="f550d-137">IMediaSeeking Methods</span></span>                                               | <span data-ttu-id="f550d-138">Descrição</span><span class="sxs-lookup"><span data-stu-id="f550d-138">Description</span></span>                                                                                 |
| [<span data-ttu-id="f550d-139">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="f550d-139">**IsFormatSupported**</span></span>](csourceseeking-isformatsupported.md)       | <span data-ttu-id="f550d-140">Determina se há suporte para um formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="f550d-140">Determines whether a specified time format is supported.</span></span>                                    |
| [<span data-ttu-id="f550d-141">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-141">**QueryPreferredFormat**</span></span>](csourceseeking-querypreferredformat.md) | <span data-ttu-id="f550d-142">Recupera o formato de hora preferencial do objeto.</span><span class="sxs-lookup"><span data-stu-id="f550d-142">Retrieves the object's preferred time format.</span></span>                                               |
| [<span data-ttu-id="f550d-143">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-143">**SetTimeFormat**</span></span>](csourceseeking-settimeformat.md)               | <span data-ttu-id="f550d-144">Define o formato de hora.</span><span class="sxs-lookup"><span data-stu-id="f550d-144">Sets the time format.</span></span>                                                                       |
| [<span data-ttu-id="f550d-145">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-145">**IsUsingTimeFormat**</span></span>](csourceseeking-isusingtimeformat.md)       | <span data-ttu-id="f550d-146">Determina se um formato de hora especificado é o formato em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="f550d-146">Determines whether a specified time format is the format currently in use.</span></span>                  |
| [<span data-ttu-id="f550d-147">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-147">**GetTimeFormat**</span></span>](csourceseeking-gettimeformat.md)               | <span data-ttu-id="f550d-148">Recupera o formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="f550d-148">Retrieves the current time format.</span></span>                                                          |
| [<span data-ttu-id="f550d-149">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="f550d-149">**GetDuration**</span></span>](csourceseeking-getduration.md)                   | <span data-ttu-id="f550d-150">Recupera a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f550d-150">Retrieves the duration of the stream.</span></span>                                                       |
| [<span data-ttu-id="f550d-151">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="f550d-151">**GetStopPosition**</span></span>](csourceseeking-getstopposition.md)           | <span data-ttu-id="f550d-152">Recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f550d-152">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span> |
| [<span data-ttu-id="f550d-153">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="f550d-153">**GetCurrentPosition**</span></span>](csourceseeking-getcurrentposition.md)     | <span data-ttu-id="f550d-154">Recupera a posição atual, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f550d-154">Retrieves the current position, relative to the total duration of the stream.</span></span>               |
| [<span data-ttu-id="f550d-155">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f550d-155">**GetCapabilities**</span></span>](csourceseeking-getcapabilities.md)           | <span data-ttu-id="f550d-156">Recupera todos os recursos de busca do fluxo.</span><span class="sxs-lookup"><span data-stu-id="f550d-156">Retrieves all the seeking capabilities of the stream.</span></span>                                       |
| [<span data-ttu-id="f550d-157">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="f550d-157">**CheckCapabilities**</span></span>](csourceseeking-checkcapabilities.md)       | <span data-ttu-id="f550d-158">Consulta se o fluxo especificou recursos de busca.</span><span class="sxs-lookup"><span data-stu-id="f550d-158">Queries whether the stream has specified seeking capabilities.</span></span>                              |
| [<span data-ttu-id="f550d-159">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-159">**ConvertTimeFormat**</span></span>](csourceseeking-converttimeformat.md)       | <span data-ttu-id="f550d-160">Converte de um formato de tempo para outro.</span><span class="sxs-lookup"><span data-stu-id="f550d-160">Converts from one time format to another.</span></span>                                                   |
| [<span data-ttu-id="f550d-161">**Setpositiones**</span><span class="sxs-lookup"><span data-stu-id="f550d-161">**SetPositions**</span></span>](csourceseeking-setpositions.md)                 | <span data-ttu-id="f550d-162">Define a posição atual e a posição de parada.</span><span class="sxs-lookup"><span data-stu-id="f550d-162">Sets the current position and the stop position.</span></span>                                            |
| [<span data-ttu-id="f550d-163">**Getpositiones**</span><span class="sxs-lookup"><span data-stu-id="f550d-163">**GetPositions**</span></span>](csourceseeking-getpositions.md)                 | <span data-ttu-id="f550d-164">Recupera a posição atual e a posição de parada.</span><span class="sxs-lookup"><span data-stu-id="f550d-164">Retrieves the current position and the stop position.</span></span>                                       |
| [<span data-ttu-id="f550d-165">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="f550d-165">**GetAvailable**</span></span>](csourceseeking-getavailable.md)                 | <span data-ttu-id="f550d-166">Recupera o intervalo de vezes em que a busca é eficiente.</span><span class="sxs-lookup"><span data-stu-id="f550d-166">Retrieves the range of times in which seeking is efficient.</span></span>                                 |
| [<span data-ttu-id="f550d-167">**SetRate**</span><span class="sxs-lookup"><span data-stu-id="f550d-167">**SetRate**</span></span>](csourceseeking-setrate.md)                           | <span data-ttu-id="f550d-168">Define a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f550d-168">Sets the playback rate.</span></span>                                                                     |
| [<span data-ttu-id="f550d-169">**GetRate**</span><span class="sxs-lookup"><span data-stu-id="f550d-169">**GetRate**</span></span>](csourceseeking-getrate.md)                           | <span data-ttu-id="f550d-170">Recupera a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="f550d-170">Retrieves the playback rate.</span></span>                                                                |
| [<span data-ttu-id="f550d-171">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="f550d-171">**GetPreroll**</span></span>](csourceseeking-getpreroll.md)                     | <span data-ttu-id="f550d-172">Recupera o tempo de preversão.</span><span class="sxs-lookup"><span data-stu-id="f550d-172">Retrieves the preroll time.</span></span>                                                                 |



 

## <a name="remarks"></a><span data-ttu-id="f550d-173">Comentários</span><span class="sxs-lookup"><span data-stu-id="f550d-173">Remarks</span></span>

<span data-ttu-id="f550d-174">Sempre que a posição inicial, a posição de parada ou a taxa de reprodução é alterada, o objeto **CSourceSeeking** chama um método virtual puro correspondente:</span><span class="sxs-lookup"><span data-stu-id="f550d-174">Whenever the start position, stop position, or playback rate changes, the **CSourceSeeking** object calls a corresponding pure virtual method:</span></span>

-   <span data-ttu-id="f550d-175">Posição inicial: [ **CSourceSeeking:: altere**](csourceseeking-changestart.md)</span><span class="sxs-lookup"><span data-stu-id="f550d-175">Start position: [**CSourceSeeking::ChangeStart**](csourceseeking-changestart.md)</span></span>
-   <span data-ttu-id="f550d-176">Posição de parada: [ **CSourceSeeking:: ChangeStop**](csourceseeking-changestop.md)</span><span class="sxs-lookup"><span data-stu-id="f550d-176">Stop position: [**CSourceSeeking::ChangeStop**](csourceseeking-changestop.md)</span></span>
-   <span data-ttu-id="f550d-177">Taxa de reprodução: [ **CSourceSeeking:: disqueteira**](csourceseeking-changerate.md)</span><span class="sxs-lookup"><span data-stu-id="f550d-177">Playback rate: [**CSourceSeeking::ChangeRate**](csourceseeking-changerate.md)</span></span>

<span data-ttu-id="f550d-178">A classe derivada deve implementar esses métodos.</span><span class="sxs-lookup"><span data-stu-id="f550d-178">The derived class must implement these methods.</span></span> <span data-ttu-id="f550d-179">Após qualquer operação de busca, um filtro deve fazer o seguinte:</span><span class="sxs-lookup"><span data-stu-id="f550d-179">After any seek operation, a filter must do the following:</span></span>

1.  <span data-ttu-id="f550d-180">Chame o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="f550d-180">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the downstream input pin.</span></span>
2.  <span data-ttu-id="f550d-181">Pare o thread de trabalho que está entregando dados.</span><span class="sxs-lookup"><span data-stu-id="f550d-181">Halt the worker thread that is delivering data.</span></span>
3.  <span data-ttu-id="f550d-182">Chame o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="f550d-182">Call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on the input pin.</span></span>
4.  <span data-ttu-id="f550d-183">Reinicie o thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f550d-183">Restart the worker thread.</span></span>
5.  <span data-ttu-id="f550d-184">Chame o método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="f550d-184">Call the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>
6.  <span data-ttu-id="f550d-185">Defina a propriedade de descontinuidade no primeiro exemplo.</span><span class="sxs-lookup"><span data-stu-id="f550d-185">Set the discontinuity property on the first sample.</span></span> <span data-ttu-id="f550d-186">Chame o método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) .</span><span class="sxs-lookup"><span data-stu-id="f550d-186">Call the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method.</span></span>

<span data-ttu-id="f550d-187">A chamada para [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) liberará o thread de trabalho, se o thread estiver bloqueado aguardando para entregar um exemplo.</span><span class="sxs-lookup"><span data-stu-id="f550d-187">The call to [**BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) frees the worker thread, if the thread is blocked waiting to deliver a sample.</span></span>

<span data-ttu-id="f550d-188">Na etapa 2, certifique-se de que o thread parou de enviar dados.</span><span class="sxs-lookup"><span data-stu-id="f550d-188">In step 2, make sure that the thread has stopped sending data.</span></span> <span data-ttu-id="f550d-189">Dependendo da implementação, talvez seja necessário aguardar a saída do thread ou para que o thread sinalize uma resposta de algum tipo.</span><span class="sxs-lookup"><span data-stu-id="f550d-189">Depending on the implementation, you might need to wait for the thread to exit, or for the thread to signal a response of some kind.</span></span> <span data-ttu-id="f550d-190">Se o filtro usar a classe [**CSourceStream**](csourcestream.md) , o método [**CSourceStream:: Stop**](csourcestream-stop.md) bloqueará até que o thread de trabalho responda.</span><span class="sxs-lookup"><span data-stu-id="f550d-190">If your filter uses the [**CSourceStream**](csourcestream.md) class, the [**CSourceStream::Stop**](csourcestream-stop.md) method blocks until the worker thread replies.</span></span>

<span data-ttu-id="f550d-191">O ideal é que o novo segmento (etapa 5) seja entregue do thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="f550d-191">Ideally, the new segment (step 5) should be delivered from the worker thread.</span></span> <span data-ttu-id="f550d-192">Ele também pode ser feito pelo objeto **CSourceSeeking** , desde que o filtro o Serialize com os exemplos.</span><span class="sxs-lookup"><span data-stu-id="f550d-192">It can also be done by the **CSourceSeeking** object, as long as the filter serializes it with the samples.</span></span>

<span data-ttu-id="f550d-193">O exemplo a seguir mostra uma implementação possível.</span><span class="sxs-lookup"><span data-stu-id="f550d-193">The following example shows a possible implementation.</span></span> <span data-ttu-id="f550d-194">Ele pressupõe que o pino de saída do filtro de origem é derivado de **CSourceSeeking** e [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="f550d-194">It assumes that the source filter's output pin is derived from **CSourceSeeking** and [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="f550d-195">Este exemplo define um método auxiliar, UpdateFromSeek, que executa as etapas 1 4.</span><span class="sxs-lookup"><span data-stu-id="f550d-195">This example defines a helper method, UpdateFromSeek, that performs steps 1 4.</span></span> <span data-ttu-id="f550d-196">O método [**CSourceStream:: OnThreadStartPlay**](csourcestream-onthreadstartplay.md) é substituído para enviar o novo segmento e para definir um sinalizador que indica a descontinuidade.</span><span class="sxs-lookup"><span data-stu-id="f550d-196">The [**CSourceStream::OnThreadStartPlay**](csourcestream-onthreadstartplay.md) method is overridden to send the new segment, and to set a flag indicating the discontinuity.</span></span> <span data-ttu-id="f550d-197">O thread de trabalho pega esse sinalizador e chama o método [**IMediaSample:: SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) :</span><span class="sxs-lookup"><span data-stu-id="f550d-197">The worker thread picks up this flag and calls the [**IMediaSample::SetDiscontinuity**](/windows/desktop/api/Strmif/nf-strmif-imediasample-setdiscontinuity) method:</span></span>


```C++
void CMyStream::UpdateFromSeek()
{
    if (ThreadExists()) 
    {
        DeliverBeginFlush();
        Stop();
        DeliverEndFlush();
        Run();
    }
}

HRESULT CMyStream::OnThreadStartPlay()
{
    m_bDiscontinuity = TRUE;
    return DeliverNewSegment(m_rtStart, m_rtStop, m_dRateSeeking);
}
```



### <a name="supporting-additional-time-formats"></a><span data-ttu-id="f550d-198">Dando suporte a formatos de tempo adicionais</span><span class="sxs-lookup"><span data-stu-id="f550d-198">Supporting Additional Time Formats</span></span>

<span data-ttu-id="f550d-199">Por padrão, essa classe dá suporte à busca apenas em unidades de tempo de referência (tempo de mídia de formato de hora \_ \_ \_ ).</span><span class="sxs-lookup"><span data-stu-id="f550d-199">By default, this class supports seeking only in units of reference time (TIME\_FORMAT\_MEDIA\_TIME).</span></span> <span data-ttu-id="f550d-200">Para dar suporte a formatos de tempo adicionais, substitua os métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) que lidam com formatos de hora:</span><span class="sxs-lookup"><span data-stu-id="f550d-200">To support additional time formats, override the [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods that deal with time formats:</span></span>

-   [<span data-ttu-id="f550d-201">**IMediaSeeking::GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-201">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="f550d-202">**IMediaSeeking::GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-202">**IMediaSeeking::GetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-gettimeformat)
-   [<span data-ttu-id="f550d-203">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-203">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="f550d-204">**IMediaSeeking::IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-204">**IMediaSeeking::IsUsingTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-isusingtimeformat)
-   [<span data-ttu-id="f550d-205">**IMediaSeeking::SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="f550d-205">**IMediaSeeking::SetTimeFormat**</span></span>](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat)

<span data-ttu-id="f550d-206">Além disso, substitua os métodos [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) restantes para executar as conversões necessárias entre os formatos de hora.</span><span class="sxs-lookup"><span data-stu-id="f550d-206">In addition, override the remaining [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods to perform the necessary conversions between time formats.</span></span> <span data-ttu-id="f550d-207">Depois que o método [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) é chamado, todos os métodos **IMediaSeeking** devem tratar os parâmetros de hora de entrada e saída como estando no novo formato de hora.</span><span class="sxs-lookup"><span data-stu-id="f550d-207">After the [**SetTimeFormat**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-settimeformat) method is called, all **IMediaSeeking** methods must treat incoming and outgoing time parameters as being in the new time format.</span></span> <span data-ttu-id="f550d-208">Por exemplo, se a variável *m \_ rtDuration* representar a duração em unidades de tempo de referência, mas o formato de hora atual for frames, o método [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) deverá retornar o valor *m \_ rtDuration* convertido em quadros.</span><span class="sxs-lookup"><span data-stu-id="f550d-208">For example, if the *m\_rtDuration* variable represents the duration in units of reference time, but the current time format is frames, then the [**GetDuration**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-getduration) method must return the value *m\_rtDuration* converted to frames.</span></span> <span data-ttu-id="f550d-209">Por exemplo:</span><span class="sxs-lookup"><span data-stu-id="f550d-209">For example:</span></span>


```
STDMETHODIMP GetDuration(LONGLONG *pDuration)
{
    HRESULT hr = CSourceSeeking::GetDuration(pDuration);
    if (SUCCEEDED(hr))
    {
        if (m_TimeFormat == TIME_FORMAT_FRAME)
        {
            // Convert from reference time to frames.
            *pDuration = TimeToFrame(*pDuration);  // Private method.
        }
    }
    return hr
} 
```



<span data-ttu-id="f550d-210">Além disso, certifique-se de verificar o \_ \_ sinalizador retornartime de busca no método [**IMediaSeeking:: setpositiones**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) .</span><span class="sxs-lookup"><span data-stu-id="f550d-210">Also, make sure to check for the AM\_SEEKING\_ReturnTime flag in the [**IMediaSeeking::SetPositions**](/windows/desktop/api/Strmif/nf-strmif-imediaseeking-setpositions) method.</span></span> <span data-ttu-id="f550d-211">Se esse sinalizador estiver presente, converta os valores de posição em tempos de referência quando retorná-los ao chamador.</span><span class="sxs-lookup"><span data-stu-id="f550d-211">If this flag is present, convert the position values into reference times when you return them to the caller.</span></span>

## <a name="requirements"></a><span data-ttu-id="f550d-212">Requisitos</span><span class="sxs-lookup"><span data-stu-id="f550d-212">Requirements</span></span>



| <span data-ttu-id="f550d-213">Requisito</span><span class="sxs-lookup"><span data-stu-id="f550d-213">Requirement</span></span> | <span data-ttu-id="f550d-214">Valor</span><span class="sxs-lookup"><span data-stu-id="f550d-214">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="f550d-215">parâmetro</span><span class="sxs-lookup"><span data-stu-id="f550d-215">Header</span></span><br/>  | <dl> <span data-ttu-id="f550d-216"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="f550d-216"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="f550d-217">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="f550d-217">Library</span></span><br/> | <dl> <span data-ttu-id="f550d-218"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="f550d-218"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f550d-219">Confira também</span><span class="sxs-lookup"><span data-stu-id="f550d-219">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f550d-220">Dando suporte à busca em um filtro de origem</span><span class="sxs-lookup"><span data-stu-id="f550d-220">Supporting Seeking in a Source Filter</span></span>](supporting-seeking-in-a-source-filter.md)
</dt> </dl>

 

 




