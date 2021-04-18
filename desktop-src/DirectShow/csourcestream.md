---
description: A classe CSourceStream fornece um pino de saída para a classe de filtro CSource.
ms.assetid: 5ccfb129-93e2-4773-9398-5f59f2914ba7
title: Classe CSourceStream (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 36b9085df8c15e765c751be8b5fcdfd4f4a02140
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779545"
---
# <a name="csourcestream-class"></a><span data-ttu-id="1373a-103">Classe CSourceStream</span><span class="sxs-lookup"><span data-stu-id="1373a-103">CSourceStream class</span></span>

![hierarquia de classe CSourceStream](images/source02.png)

<span data-ttu-id="1373a-105">A classe **CSourceStream** fornece um pino de saída para a classe de filtro [**CSource**](csource.md) .</span><span class="sxs-lookup"><span data-stu-id="1373a-105">The **CSourceStream** class provides an output pin for the [**CSource**](csource.md) filter class.</span></span>

<span data-ttu-id="1373a-106">Para obter informações sobre como usar essa classe, consulte [**CSource**](csource.md).</span><span class="sxs-lookup"><span data-stu-id="1373a-106">For information on using this class, see [**CSource**](csource.md).</span></span> <span data-ttu-id="1373a-107">Essa classe herda a classe [**CAMThread**](camthread.md) , que fornece um thread de trabalho para streaming de dados do PIN.</span><span class="sxs-lookup"><span data-stu-id="1373a-107">This class inherits the [**CAMThread**](camthread.md) class, which provides a worker thread for streaming data from the pin.</span></span> <span data-ttu-id="1373a-108">A classe **CSourceStream** implementa os seguintes métodos auxiliares para enviar solicitações para o thread:</span><span class="sxs-lookup"><span data-stu-id="1373a-108">The **CSourceStream** class implements the following helper methods to send requests to the thread:</span></span>

-   [<span data-ttu-id="1373a-109">**CSourceStream:: sair**</span><span class="sxs-lookup"><span data-stu-id="1373a-109">**CSourceStream::Exit**</span></span>](csourcestream-exit.md)
-   [<span data-ttu-id="1373a-110">**CSourceStream:: init**</span><span class="sxs-lookup"><span data-stu-id="1373a-110">**CSourceStream::Init**</span></span>](csourcestream-init.md)
-   [<span data-ttu-id="1373a-111">**CSourceStream::P ause**</span><span class="sxs-lookup"><span data-stu-id="1373a-111">**CSourceStream::Pause**</span></span>](csourcestream-pause.md)
-   [<span data-ttu-id="1373a-112">**CSourceStream:: Run**</span><span class="sxs-lookup"><span data-stu-id="1373a-112">**CSourceStream::Run**</span></span>](csourcestream-run.md)
-   [<span data-ttu-id="1373a-113">**CSourceStream:: Stop**</span><span class="sxs-lookup"><span data-stu-id="1373a-113">**CSourceStream::Stop**</span></span>](csourcestream-stop.md)

<span data-ttu-id="1373a-114">A primeira solicitação para o thread deve ser [**init**](csourcestream-init.md).</span><span class="sxs-lookup"><span data-stu-id="1373a-114">The first request to the thread must be [**Init**](csourcestream-init.md).</span></span> <span data-ttu-id="1373a-115">A solicitação de [**saída**](csourcestream-exit.md) encerra o thread.</span><span class="sxs-lookup"><span data-stu-id="1373a-115">The [**Exit**](csourcestream-exit.md) request terminates the thread.</span></span> <span data-ttu-id="1373a-116">Na prática, não é necessário chamar qualquer um desses métodos diretamente, porque os métodos [**CSourceStream:: active**](csourcestream-active.md) e [**CSourceStream:: Inactive**](csourcestream-inactive.md) do PIN os chamam conforme necessário.</span><span class="sxs-lookup"><span data-stu-id="1373a-116">In practice, it is not necessary to call any of these methods directly, because the pin's [**CSourceStream::Active**](csourcestream-active.md) and [**CSourceStream::Inactive**](csourcestream-inactive.md) methods call them as needed.</span></span>

<span data-ttu-id="1373a-117">A classe também fornece vários métodos "Handler":</span><span class="sxs-lookup"><span data-stu-id="1373a-117">The class also provides several "handler" methods:</span></span>

-   [<span data-ttu-id="1373a-118">**CSourceStream::OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="1373a-118">**CSourceStream::OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)
-   [<span data-ttu-id="1373a-119">**CSourceStream::OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="1373a-119">**CSourceStream::OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)
-   [<span data-ttu-id="1373a-120">**CSourceStream::OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="1373a-120">**CSourceStream::OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)

<span data-ttu-id="1373a-121">Eles não fazem nada na classe base, mas a classe derivada pode substituí-los.</span><span class="sxs-lookup"><span data-stu-id="1373a-121">These do nothing in the base class, but the derived class can override them.</span></span>



| <span data-ttu-id="1373a-122">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="1373a-122">Protected Member Variables</span></span>                                             | <span data-ttu-id="1373a-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="1373a-123">Description</span></span>                                                                                                                       |
|------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="1373a-124">**\_pFilter m**</span><span class="sxs-lookup"><span data-stu-id="1373a-124">**m\_pFilter**</span></span>](csourcestream-m-pfilter.md)                          | <span data-ttu-id="1373a-125">Ponteiro para o filtro que contém este pin.</span><span class="sxs-lookup"><span data-stu-id="1373a-125">Pointer to the filter that contains this pin.</span></span>                                                                                     |
| <span data-ttu-id="1373a-126">Métodos Protegidos</span><span class="sxs-lookup"><span data-stu-id="1373a-126">Protected Methods</span></span>                                                      | <span data-ttu-id="1373a-127">Descrição</span><span class="sxs-lookup"><span data-stu-id="1373a-127">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="1373a-128">**OnThreadCreate**</span><span class="sxs-lookup"><span data-stu-id="1373a-128">**OnThreadCreate**</span></span>](csourcestream-onthreadcreate.md)                 | <span data-ttu-id="1373a-129">Chamado quando o thread de streaming é inicializado.</span><span class="sxs-lookup"><span data-stu-id="1373a-129">Called when the streaming thread is initialized.</span></span> <span data-ttu-id="1373a-130">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="1373a-130">Virtual.</span></span>                                                                         |
| [<span data-ttu-id="1373a-131">**OnThreadDestroy**</span><span class="sxs-lookup"><span data-stu-id="1373a-131">**OnThreadDestroy**</span></span>](csourcestream-onthreaddestroy.md)               | <span data-ttu-id="1373a-132">Chamado quando o thread de streaming está prestes a sair.</span><span class="sxs-lookup"><span data-stu-id="1373a-132">Called when the streaming thread is about to exit.</span></span> <span data-ttu-id="1373a-133">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="1373a-133">Virtual.</span></span>                                                                       |
| [<span data-ttu-id="1373a-134">**OnThreadStartPlay**</span><span class="sxs-lookup"><span data-stu-id="1373a-134">**OnThreadStartPlay**</span></span>](csourcestream-onthreadstartplay.md)           | <span data-ttu-id="1373a-135">Chamado no início do método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="1373a-135">Called at the start of the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span> <span data-ttu-id="1373a-136">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="1373a-136">Virtual.</span></span> |
| [<span data-ttu-id="1373a-137">**Activo**</span><span class="sxs-lookup"><span data-stu-id="1373a-137">**Active**</span></span>](csourcestream-active.md)                                 | <span data-ttu-id="1373a-138">Notifica o PIN de que o filtro está ativo agora.</span><span class="sxs-lookup"><span data-stu-id="1373a-138">Notifies the pin that the filter is now active.</span></span>                                                                                   |
| [<span data-ttu-id="1373a-139">**Inativo**</span><span class="sxs-lookup"><span data-stu-id="1373a-139">**Inactive**</span></span>](csourcestream-inactive.md)                             | <span data-ttu-id="1373a-140">Notifica o PIN de que o filtro não está mais ativo.</span><span class="sxs-lookup"><span data-stu-id="1373a-140">Notifies the pin that the filter is no longer active.</span></span>                                                                             |
| [<span data-ttu-id="1373a-141">**GetRequest**</span><span class="sxs-lookup"><span data-stu-id="1373a-141">**GetRequest**</span></span>](csourcestream-getrequest.md)                         | <span data-ttu-id="1373a-142">Aguarda a próxima solicitação de thread.</span><span class="sxs-lookup"><span data-stu-id="1373a-142">Waits for the next thread request.</span></span>                                                                                                |
| [<span data-ttu-id="1373a-143">**CheckRequest**</span><span class="sxs-lookup"><span data-stu-id="1373a-143">**CheckRequest**</span></span>](csourcestream-checkrequest.md)                     | <span data-ttu-id="1373a-144">Verifica se há uma solicitação de thread, sem bloqueio.</span><span class="sxs-lookup"><span data-stu-id="1373a-144">Checks if there is a thread request, without blocking.</span></span>                                                                            |
| [<span data-ttu-id="1373a-145">**ThreadProc**</span><span class="sxs-lookup"><span data-stu-id="1373a-145">**ThreadProc**</span></span>](csourcestream-threadproc.md)                         | <span data-ttu-id="1373a-146">Procedimento de thread.</span><span class="sxs-lookup"><span data-stu-id="1373a-146">Thread procedure.</span></span> <span data-ttu-id="1373a-147">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="1373a-147">Virtual.</span></span>                                                                                                        |
| [<span data-ttu-id="1373a-148">**DoBufferProcessingLoop**</span><span class="sxs-lookup"><span data-stu-id="1373a-148">**DoBufferProcessingLoop**</span></span>](csourcestream-dobufferprocessingloop.md) | <span data-ttu-id="1373a-149">Gera dados de mídia e os entrega para o pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="1373a-149">Generates media data and delivers it to the downstream input pin.</span></span> <span data-ttu-id="1373a-150">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="1373a-150">Virtual.</span></span>                                                        |
| [<span data-ttu-id="1373a-151">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="1373a-151">**CheckMediaType**</span></span>](csourcestream-checkmediatype.md)                 | <span data-ttu-id="1373a-152">Determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="1373a-152">Determines if the pin accepts a specific media type.</span></span> <span data-ttu-id="1373a-153">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="1373a-153">Virtual.</span></span>                                                                     |
| [<span data-ttu-id="1373a-154">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="1373a-154">**GetMediaType**</span></span>](csourcestream-getmediatype.md)                     | <span data-ttu-id="1373a-155">Recupera um tipo de mídia preferencial.</span><span class="sxs-lookup"><span data-stu-id="1373a-155">Retrieves a preferred media type.</span></span> <span data-ttu-id="1373a-156">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="1373a-156">Virtual.</span></span>                                                                                        |
| <span data-ttu-id="1373a-157">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="1373a-157">Public Methods</span></span>                                                         | <span data-ttu-id="1373a-158">Descrição</span><span class="sxs-lookup"><span data-stu-id="1373a-158">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="1373a-159">**CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="1373a-159">**CSourceStream**</span></span>](csourcestream-csourcestream.md)                   | <span data-ttu-id="1373a-160">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="1373a-160">Constructor method.</span></span>                                                                                                               |
| [<span data-ttu-id="1373a-161">**~ CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="1373a-161">**~ CSourceStream**</span></span>](csourcestream--csourcestream.md)                | <span data-ttu-id="1373a-162">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="1373a-162">Destructor method.</span></span> <span data-ttu-id="1373a-163">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="1373a-163">Virtual.</span></span>                                                                                                       |
| [<span data-ttu-id="1373a-164">**Init**</span><span class="sxs-lookup"><span data-stu-id="1373a-164">**Init**</span></span>](csourcestream-init.md)                                     | <span data-ttu-id="1373a-165">Inicializa o thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="1373a-165">Initializes the streaming thread.</span></span>                                                                                                 |
| [<span data-ttu-id="1373a-166">**Fechar**</span><span class="sxs-lookup"><span data-stu-id="1373a-166">**Exit**</span></span>](csourcestream-exit.md)                                     | <span data-ttu-id="1373a-167">Sinaliza o thread de streaming para sair.</span><span class="sxs-lookup"><span data-stu-id="1373a-167">Signals the streaming thread to exit.</span></span>                                                                                             |
| [<span data-ttu-id="1373a-168">**Executar**</span><span class="sxs-lookup"><span data-stu-id="1373a-168">**Run**</span></span>](csourcestream-run.md)                                       | <span data-ttu-id="1373a-169">Sinaliza o thread de streaming a ser executado.</span><span class="sxs-lookup"><span data-stu-id="1373a-169">Signals the streaming thread to run.</span></span>                                                                                              |
| [<span data-ttu-id="1373a-170">**Pausar**</span><span class="sxs-lookup"><span data-stu-id="1373a-170">**Pause**</span></span>](csourcestream-pause.md)                                   | <span data-ttu-id="1373a-171">Sinaliza o thread de streaming para se tornar ativo.</span><span class="sxs-lookup"><span data-stu-id="1373a-171">Signals the streaming thread to become active.</span></span>                                                                                    |
| [<span data-ttu-id="1373a-172">**Stop**</span><span class="sxs-lookup"><span data-stu-id="1373a-172">**Stop**</span></span>](csourcestream-stop.md)                                     | <span data-ttu-id="1373a-173">Sinaliza o thread de streaming para parar.</span><span class="sxs-lookup"><span data-stu-id="1373a-173">Signals the streaming thread to stop.</span></span>                                                                                             |
| <span data-ttu-id="1373a-174">Métodos virtuais puros</span><span class="sxs-lookup"><span data-stu-id="1373a-174">Pure Virtual Methods</span></span>                                                   | <span data-ttu-id="1373a-175">Descrição</span><span class="sxs-lookup"><span data-stu-id="1373a-175">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="1373a-176">**FillBuffer**</span><span class="sxs-lookup"><span data-stu-id="1373a-176">**FillBuffer**</span></span>](csourcestream-fillbuffer.md)                         | <span data-ttu-id="1373a-177">Preenche um exemplo de mídia com dados.</span><span class="sxs-lookup"><span data-stu-id="1373a-177">Fills a media sample with data.</span></span>                                                                                                   |
| <span data-ttu-id="1373a-178">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="1373a-178">IPin Methods</span></span>                                                           | <span data-ttu-id="1373a-179">Descrição</span><span class="sxs-lookup"><span data-stu-id="1373a-179">Description</span></span>                                                                                                                       |
| [<span data-ttu-id="1373a-180">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="1373a-180">**QueryId**</span></span>](/windows/desktop/api/Strmif/nf-strmif-ipin-queryid)                                        | <span data-ttu-id="1373a-181">Recupera um identificador para o PIN.</span><span class="sxs-lookup"><span data-stu-id="1373a-181">Retrieves an identifier for the pin.</span></span>                                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="1373a-182">Requisitos</span><span class="sxs-lookup"><span data-stu-id="1373a-182">Requirements</span></span>



| <span data-ttu-id="1373a-183">Requisito</span><span class="sxs-lookup"><span data-stu-id="1373a-183">Requirement</span></span> | <span data-ttu-id="1373a-184">Valor</span><span class="sxs-lookup"><span data-stu-id="1373a-184">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="1373a-185">parâmetro</span><span class="sxs-lookup"><span data-stu-id="1373a-185">Header</span></span><br/>  | <dl> <span data-ttu-id="1373a-186"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="1373a-186"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="1373a-187">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="1373a-187">Library</span></span><br/> | <dl> <span data-ttu-id="1373a-188"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="1373a-188"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1373a-189">Confira também</span><span class="sxs-lookup"><span data-stu-id="1373a-189">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1373a-190">Gravando filtros de origem</span><span class="sxs-lookup"><span data-stu-id="1373a-190">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




