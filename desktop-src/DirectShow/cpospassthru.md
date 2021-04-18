---
description: A classe CPosPassThru manipula comandos de busca para filtros de transformação, passando-os upstream para o próximo filtro.
ms.assetid: 14180d6e-7925-4e1a-8b16-cae9d7113468
title: Classe CPosPassThru (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 77bd8adfac5d609af356f7cef0a5da086c052b8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780862"
---
# <a name="cpospassthru-class"></a><span data-ttu-id="0b724-103">Classe CPosPassThru</span><span class="sxs-lookup"><span data-stu-id="0b724-103">CPosPassThru class</span></span>

![hierarquia de classe base CPosPassThru](images/cutil14.png)

<span data-ttu-id="0b724-105">A `CPosPassThru` classe manipula comandos de busca para filtros de transformação, passando-os upstream para o próximo filtro.</span><span class="sxs-lookup"><span data-stu-id="0b724-105">The `CPosPassThru` class handles seek commands for transform filters, by passing them upstream to the next filter.</span></span>

<span data-ttu-id="0b724-106">Quando um aplicativo busca o grafo de filtro, o Gerenciador de grafo de filtro fornece o comando de busca aos filtros de processador.</span><span class="sxs-lookup"><span data-stu-id="0b724-106">When an application seeks the filter graph, the Filter Graph Manager gives the seek command to the renderer filters.</span></span> <span data-ttu-id="0b724-107">O comando é passado para upstream, por meio do pino de saída de cada filtro, até atingir um filtro que possa executar o comando (se houver).</span><span class="sxs-lookup"><span data-stu-id="0b724-107">The command is passed upstream, through each filter's output pin, until it reaches a filter that can execute the command (if any).</span></span> <span data-ttu-id="0b724-108">Para obter detalhes, consulte [buscando](seeking.md).</span><span class="sxs-lookup"><span data-stu-id="0b724-108">For details, see [Seeking](seeking.md).</span></span> <span data-ttu-id="0b724-109">A `CPosPassThru` classe passa todos os comandos de busca para o pino de saída no filtro upstream, conforme mostrado no diagrama a seguir.</span><span class="sxs-lookup"><span data-stu-id="0b724-109">The `CPosPassThru` class passes all seek commands to the output pin on the upstream filter, as shown in the following diagram.</span></span>

![a classe CPosPassThru envia comandos de busca upstream.](images/cpospassthru.png)

<span data-ttu-id="0b724-111">Embora essa classe seja fornecida na biblioteca de classes base, o DirectShow também fornece a mesma classe em Quartz.dll.</span><span class="sxs-lookup"><span data-stu-id="0b724-111">Although this class is provided in the base class library, DirectShow also provides the same class in Quartz.dll.</span></span> <span data-ttu-id="0b724-112">O uso da versão Quartz.dll pode reduzir um pouco o tamanho do código em seu filtro, pois a classe é carregada em tempo de execução da DLL.</span><span class="sxs-lookup"><span data-stu-id="0b724-112">Using the Quartz.dll version can reduce the code size in your filter somewhat, because the class is loaded at run-time from the DLL.</span></span> <span data-ttu-id="0b724-113">Para usar essa versão, chame a função [**CreatePosPassThru**](createpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="0b724-113">To use that version, call the [**CreatePosPassThru**](createpospassthru.md) function.</span></span>

<span data-ttu-id="0b724-114">No método **NonDelegatingQueryInterface** do pino de saída, delegue ao objeto **CPosPassThru** sempre que a interface solicitada for [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) ou [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), conforme mostrado no código a seguir:</span><span class="sxs-lookup"><span data-stu-id="0b724-114">In your output pin's **NonDelegatingQueryInterface** method, delegate to the **CPosPassThru** object whenever the requested interface is [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) or [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), as shown in the following code:</span></span>


```
// The following member variables are assumed:
IPin *m_pInput;    // Pointer to the input pin on your filter.
IUnknown *m_pPos;  // Pointer to the CPosPassThru object.

STDMETHODIMP CMyPin::NonDelegatingQueryInterface(REFIID riid, void **ppv)
{
    HRESULT hr
    if (riid == IID_IMediaPosition || riid == IID_IMediaSeeking) 
    {
        if (m_pPos == NULL) 
        {
            // We have not created the CPosPassThru object yet. Do so now.
            hr = CreatePosPassThru(GetOwner(), FALSE, m_pInput, &m_pPos);
            if (FAILED(hr)) return hr;
        }
        return m_pPos->QueryInterface(riid, ppv);
    } 
    else
    {
         // Other interfaces (not shown).
    }
}

~CMyPin::CMyPin() 
{
    // Release the CPosPassThruObject.
    if (m_pPos != NULL) m_pPos->Release();
}
```



<span data-ttu-id="0b724-115">Exceto quando indicado, todos os métodos [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) e [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) nessa classe chamam o método correspondente no PIN conectado e retornam o resultado.</span><span class="sxs-lookup"><span data-stu-id="0b724-115">Except where noted, all [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) and [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) methods in this class call the corresponding method on the connected pin and return the result.</span></span>



| <span data-ttu-id="0b724-116">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="0b724-116">Public Methods</span></span>                                                    | <span data-ttu-id="0b724-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b724-117">Description</span></span>                                                                                         |
|-------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0b724-118">**CPosPassThru**</span><span class="sxs-lookup"><span data-stu-id="0b724-118">**CPosPassThru**</span></span>](cpospassthru-cpospassthru.md)                 | <span data-ttu-id="0b724-119">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="0b724-119">Constructor method.</span></span>                                                                                 |
| [<span data-ttu-id="0b724-120">**ForceRefresh**</span><span class="sxs-lookup"><span data-stu-id="0b724-120">**ForceRefresh**</span></span>](cpospassthru-forcerefresh.md)                 | <span data-ttu-id="0b724-121">Obsoleto.</span><span class="sxs-lookup"><span data-stu-id="0b724-121">Obsolete.</span></span>                                                                                           |
| [<span data-ttu-id="0b724-122">**GetMediaTime**</span><span class="sxs-lookup"><span data-stu-id="0b724-122">**GetMediaTime**</span></span>](cpospassthru-getmediatime.md)                 | <span data-ttu-id="0b724-123">Recupera os carimbos de data/hora no exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="0b724-123">Retrieves the time stamps on the current sample.</span></span> <span data-ttu-id="0b724-124">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="0b724-124">Virtual.</span></span>                                           |
| <span data-ttu-id="0b724-125">Métodos IMediaPosition</span><span class="sxs-lookup"><span data-stu-id="0b724-125">IMediaPosition Methods</span></span>                                            | <span data-ttu-id="0b724-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b724-126">Description</span></span>                                                                                         |
| [<span data-ttu-id="0b724-127">**obter \_ duração**</span><span class="sxs-lookup"><span data-stu-id="0b724-127">**get\_Duration**</span></span>](cpospassthru-get-duration.md)                | <span data-ttu-id="0b724-128">Recupera a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-128">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="0b724-129">**colocar \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="0b724-129">**put\_CurrentPosition**</span></span>](cpospassthru-put-currentposition.md)  | <span data-ttu-id="0b724-130">Define a posição atual, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-130">Sets the current position, relative to the total duration of the stream.</span></span>                            |
| [<span data-ttu-id="0b724-131">**obter \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="0b724-131">**get\_StopTime**</span></span>](cpospassthru-get-stoptime.md)                | <span data-ttu-id="0b724-132">Recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-132">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="0b724-133">**colocar \_ StopTime**</span><span class="sxs-lookup"><span data-stu-id="0b724-133">**put\_StopTime**</span></span>](cpospassthru-put-stoptime.md)                | <span data-ttu-id="0b724-134">Define a hora em que a reprodução será interrompida, em relação à duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-134">Sets the time at which the playback will stop, relative to the duration of the stream.</span></span>              |
| [<span data-ttu-id="0b724-135">**obter \_ preverttime**</span><span class="sxs-lookup"><span data-stu-id="0b724-135">**get\_PrerollTime**</span></span>](cpospassthru-get-prerolltime.md)          | <span data-ttu-id="0b724-136">Recupera a quantidade de dados que serão enfileirados antes da posição inicial.</span><span class="sxs-lookup"><span data-stu-id="0b724-136">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="0b724-137">**colocar \_ preverttime**</span><span class="sxs-lookup"><span data-stu-id="0b724-137">**put\_PrerollTime**</span></span>](cpospassthru-put-prerolltime.md)          | <span data-ttu-id="0b724-138">Define a quantidade de dados que serão enfileirados antes da posição inicial.</span><span class="sxs-lookup"><span data-stu-id="0b724-138">Sets the amount of data that will be queued before the start position.</span></span>                              |
| [<span data-ttu-id="0b724-139">**taxa de obtenção \_**</span><span class="sxs-lookup"><span data-stu-id="0b724-139">**get\_Rate**</span></span>](cpospassthru-get-rate.md)                        | <span data-ttu-id="0b724-140">Recupera a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0b724-140">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="0b724-141">**taxa de Put \_**</span><span class="sxs-lookup"><span data-stu-id="0b724-141">**put\_Rate**</span></span>](cpospassthru-put-rate.md)                        | <span data-ttu-id="0b724-142">Define a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0b724-142">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="0b724-143">**obter \_ CurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="0b724-143">**get\_CurrentPosition**</span></span>](cpospassthru-get-currentposition.md)  | <span data-ttu-id="0b724-144">Recupera a posição atual, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-144">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="0b724-145">**CanSeekForward**</span><span class="sxs-lookup"><span data-stu-id="0b724-145">**CanSeekForward**</span></span>](cpospassthru-canseekforward.md)             | <span data-ttu-id="0b724-146">Determina se o fluxo pode ser buscado retroativamente.</span><span class="sxs-lookup"><span data-stu-id="0b724-146">Determines whether the stream can be seeked backward.</span></span>                                               |
| [<span data-ttu-id="0b724-147">**CanSeekBackward**</span><span class="sxs-lookup"><span data-stu-id="0b724-147">**CanSeekBackward**</span></span>](cpospassthru-canseekbackward.md)           | <span data-ttu-id="0b724-148">Determina se o fluxo pode ser buscado em frente.</span><span class="sxs-lookup"><span data-stu-id="0b724-148">Determines whether the stream can be seeked forward.</span></span>                                                |
| <span data-ttu-id="0b724-149">Métodos IMediaSeeking</span><span class="sxs-lookup"><span data-stu-id="0b724-149">IMediaSeeking Methods</span></span>                                             | <span data-ttu-id="0b724-150">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b724-150">Description</span></span>                                                                                         |
| [<span data-ttu-id="0b724-151">**CheckCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0b724-151">**CheckCapabilities**</span></span>](cpospassthru-checkcapabilities.md)       | <span data-ttu-id="0b724-152">Consulta se um fluxo especificou recursos de busca.</span><span class="sxs-lookup"><span data-stu-id="0b724-152">Queries whether a stream has specified seeking capabilities.</span></span>                                        |
| [<span data-ttu-id="0b724-153">**ConvertTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="0b724-153">**ConvertTimeFormat**</span></span>](cpospassthru-converttimeformat.md)       | <span data-ttu-id="0b724-154">Converte de um formato de tempo para outro.</span><span class="sxs-lookup"><span data-stu-id="0b724-154">Converts from one time format to another.</span></span>                                                           |
| [<span data-ttu-id="0b724-155">**GetAvailable**</span><span class="sxs-lookup"><span data-stu-id="0b724-155">**GetAvailable**</span></span>](cpospassthru-getavailable.md)                 | <span data-ttu-id="0b724-156">Recupera o intervalo de vezes em que a busca é eficiente.</span><span class="sxs-lookup"><span data-stu-id="0b724-156">Retrieves the range of times in which seeking is efficient.</span></span>                                         |
| [<span data-ttu-id="0b724-157">**GetCapabilities**</span><span class="sxs-lookup"><span data-stu-id="0b724-157">**GetCapabilities**</span></span>](cpospassthru-getcapabilities.md)           | <span data-ttu-id="0b724-158">Recupera todos os recursos de busca do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-158">Retrieves all the seeking capabilities of the stream.</span></span>                                               |
| [<span data-ttu-id="0b724-159">**GetCurrentPosition**</span><span class="sxs-lookup"><span data-stu-id="0b724-159">**GetCurrentPosition**</span></span>](cpospassthru-getcurrentposition.md)     | <span data-ttu-id="0b724-160">Recupera a posição atual, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-160">Retrieves the current position, relative to the total duration of the stream.</span></span>                       |
| [<span data-ttu-id="0b724-161">**GetDuration**</span><span class="sxs-lookup"><span data-stu-id="0b724-161">**GetDuration**</span></span>](cpospassthru-getduration.md)                   | <span data-ttu-id="0b724-162">Recupera a duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-162">Retrieves the duration of the stream.</span></span>                                                               |
| [<span data-ttu-id="0b724-163">**Getpositiones**</span><span class="sxs-lookup"><span data-stu-id="0b724-163">**GetPositions**</span></span>](cpospassthru-getpositions.md)                 | <span data-ttu-id="0b724-164">Recupera a posição atual e a posição de parada, em relação à duração total do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-164">Retrieves the current position and the stop position, relative to the total duration of the stream.</span></span> |
| [<span data-ttu-id="0b724-165">**GetPreroll**</span><span class="sxs-lookup"><span data-stu-id="0b724-165">**GetPreroll**</span></span>](cpospassthru-getpreroll.md)                     | <span data-ttu-id="0b724-166">Recupera a quantidade de dados que serão enfileirados antes da posição inicial.</span><span class="sxs-lookup"><span data-stu-id="0b724-166">Retrieves the amount of data that will be queued before the start position.</span></span>                         |
| [<span data-ttu-id="0b724-167">**GetRate**</span><span class="sxs-lookup"><span data-stu-id="0b724-167">**GetRate**</span></span>](cpospassthru-getrate.md)                           | <span data-ttu-id="0b724-168">Recupera a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0b724-168">Retrieves the playback rate.</span></span>                                                                        |
| [<span data-ttu-id="0b724-169">**GetStopPosition**</span><span class="sxs-lookup"><span data-stu-id="0b724-169">**GetStopPosition**</span></span>](cpospassthru-getstopposition.md)           | <span data-ttu-id="0b724-170">Recupera a hora em que a reprodução será interrompida, em relação à duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-170">Retrieves the time at which the playback will stop, relative to the duration of the stream.</span></span>         |
| [<span data-ttu-id="0b724-171">**GetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="0b724-171">**GetTimeFormat**</span></span>](cpospassthru-gettimeformat.md)               | <span data-ttu-id="0b724-172">Recupera o formato de hora atual.</span><span class="sxs-lookup"><span data-stu-id="0b724-172">Retrieves the current time format.</span></span>                                                                  |
| [<span data-ttu-id="0b724-173">**IsFormatSupported**</span><span class="sxs-lookup"><span data-stu-id="0b724-173">**IsFormatSupported**</span></span>](cpospassthru-isformatsupported.md)       | <span data-ttu-id="0b724-174">Determina se há suporte para um formato de hora especificado.</span><span class="sxs-lookup"><span data-stu-id="0b724-174">Determines whether a specified time format is supported.</span></span>                                            |
| [<span data-ttu-id="0b724-175">**IsUsingTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="0b724-175">**IsUsingTimeFormat**</span></span>](cpospassthru-isusingtimeformat.md)       | <span data-ttu-id="0b724-176">Determina se um formato de hora especificado é o formato em uso no momento.</span><span class="sxs-lookup"><span data-stu-id="0b724-176">Determines whether a specified time format is the format currently in use.</span></span>                          |
| [<span data-ttu-id="0b724-177">**QueryPreferredFormat**</span><span class="sxs-lookup"><span data-stu-id="0b724-177">**QueryPreferredFormat**</span></span>](cpospassthru-querypreferredformat.md) | <span data-ttu-id="0b724-178">Recupera o formato de hora preferencial para o fluxo.</span><span class="sxs-lookup"><span data-stu-id="0b724-178">Retrieves the preferred time format for the stream.</span></span>                                                 |
| [<span data-ttu-id="0b724-179">**Setpositiones**</span><span class="sxs-lookup"><span data-stu-id="0b724-179">**SetPositions**</span></span>](cpospassthru-setpositions.md)                 | <span data-ttu-id="0b724-180">Define a posição atual e a posição de parada.</span><span class="sxs-lookup"><span data-stu-id="0b724-180">Sets the current position and the stop position.</span></span>                                                    |
| [<span data-ttu-id="0b724-181">**SetRate**</span><span class="sxs-lookup"><span data-stu-id="0b724-181">**SetRate**</span></span>](cpospassthru-setrate.md)                           | <span data-ttu-id="0b724-182">Define a taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0b724-182">Sets the playback rate.</span></span>                                                                             |
| [<span data-ttu-id="0b724-183">**SetTimeFormat**</span><span class="sxs-lookup"><span data-stu-id="0b724-183">**SetTimeFormat**</span></span>](cpospassthru-settimeformat.md)               | <span data-ttu-id="0b724-184">Define o formato de hora.</span><span class="sxs-lookup"><span data-stu-id="0b724-184">Sets the time format.</span></span>                                                                               |
| <span data-ttu-id="0b724-185">Funções auxiliares</span><span class="sxs-lookup"><span data-stu-id="0b724-185">Helper Functions</span></span>                                                  | <span data-ttu-id="0b724-186">Descrição</span><span class="sxs-lookup"><span data-stu-id="0b724-186">Description</span></span>                                                                                         |
| [<span data-ttu-id="0b724-187">**CreatePosPassThru**</span><span class="sxs-lookup"><span data-stu-id="0b724-187">**CreatePosPassThru**</span></span>](createpospassthru.md)                    | <span data-ttu-id="0b724-188">Cria um `CPosPassThru` objeto ou [**CRendererPosPassThru**](crendererpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="0b724-188">Creates a `CPosPassThru` or [**CRendererPosPassThru**](crendererpospassthru.md) object.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="0b724-189">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b724-189">Requirements</span></span>



| <span data-ttu-id="0b724-190">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b724-190">Requirement</span></span> | <span data-ttu-id="0b724-191">Valor</span><span class="sxs-lookup"><span data-stu-id="0b724-191">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b724-192">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b724-192">Header</span></span><br/>  | <dl> <span data-ttu-id="0b724-193"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b724-193"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0b724-194">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b724-194">Library</span></span><br/> | <dl> <span data-ttu-id="0b724-195"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0b724-195"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




