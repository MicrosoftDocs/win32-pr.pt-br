---
description: A classe CBaseOutputPin é uma classe base abstrata que implementa um pino de saída.
ms.assetid: 5279c8aa-6ec0-4a89-a1b3-6904d7b69a93
title: Classe CBaseOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 21949d772c44f02e364013dd98c905b8f59ccdc2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750067"
---
# <a name="cbaseoutputpin-class"></a><span data-ttu-id="a7ca5-103">Classe CBaseOutputPin</span><span class="sxs-lookup"><span data-stu-id="a7ca5-103">CBaseOutputPin class</span></span>

![hierarquia de classe CBaseOutputPin](images/filter06.png)

<span data-ttu-id="a7ca5-105">A `CBaseOutputPin` classe é uma classe base abstrata que implementa um pino de saída.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-105">The `CBaseOutputPin` class is an abstract base class that implements an output pin.</span></span>

<span data-ttu-id="a7ca5-106">Essa classe deriva de [**CBasePin**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="a7ca5-106">This class derives from [**CBasePin**](cbasepin.md).</span></span> <span data-ttu-id="a7ca5-107">Ele difere do **CBasePin** nos seguintes aspectos:</span><span class="sxs-lookup"><span data-stu-id="a7ca5-107">It differs from **CBasePin** in the following respects:</span></span>

-   <span data-ttu-id="a7ca5-108">Ele se conecta somente a Pins de entrada que dão suporte à interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) .</span><span class="sxs-lookup"><span data-stu-id="a7ca5-108">It connects only to input pins that support the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface.</span></span>
-   <span data-ttu-id="a7ca5-109">Ele dá suporte ao transporte de memória local por meio da interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="a7ca5-109">It supports local memory transport through the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>
-   <span data-ttu-id="a7ca5-110">Ele rejeita as notificações de fim de fluxo, liberação e novo segmento.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-110">It rejects end-of-stream, flush, and new-segment notifications.</span></span> <span data-ttu-id="a7ca5-111">(Eles não devem ser enviados a um PIN de saída.)</span><span class="sxs-lookup"><span data-stu-id="a7ca5-111">(These should not be sent to an output pin.)</span></span>
-   <span data-ttu-id="a7ca5-112">Ele fornece métodos para a distribuição de amostras downstream.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-112">It provides methods for delivering samples downstream.</span></span>

<span data-ttu-id="a7ca5-113">Quando o PIN se conecta, ele solicita um alocador de memória do PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-113">When the pin connects, it requests a memory allocator from the input pin.</span></span> <span data-ttu-id="a7ca5-114">Falhando, ele cria um novo objeto de alocador.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-114">Failing that, it creates a new allocator object.</span></span> <span data-ttu-id="a7ca5-115">O pino de saída é responsável por definir as propriedades do alocador.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-115">The output pin is responsible for setting the allocator properties.</span></span> <span data-ttu-id="a7ca5-116">Ele faz isso por meio do método virtual puro [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="a7ca5-116">It does this through the pure virtual method [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span> <span data-ttu-id="a7ca5-117">Substitua esse método em sua classe derivada.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-117">Override this method in your derived class.</span></span> <span data-ttu-id="a7ca5-118">Se o pino de entrada tiver requisitos de buffer, eles serão passados para o método **DecideBufferSize** .</span><span class="sxs-lookup"><span data-stu-id="a7ca5-118">If the input pin has any buffer requirements, they are passed to the **DecideBufferSize** method.</span></span>

<span data-ttu-id="a7ca5-119">Chame o método [**CBaseOutputPin:: GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) para obter um exemplo de mídia vazio.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-119">Call the [**CBaseOutputPin::GetDeliveryBuffer**](cbaseoutputpin-getdeliverybuffer.md) method to obtain an empty media sample.</span></span> <span data-ttu-id="a7ca5-120">Chame o método [**CBaseOutputPin::D eliver**](cbaseoutputpin-deliver.md) para entregar amostras downstream.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-120">Call the [**CBaseOutputPin::Deliver**](cbaseoutputpin-deliver.md) method to deliver samples downstream.</span></span>

<span data-ttu-id="a7ca5-121">Sua classe derivada deve substituir o método [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md) puro virtual para validar o tipo de mídia durante conexões de PIN.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-121">Your derived class must override the pure virtual [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md) method to validate the media type during pin connections.</span></span>



| <span data-ttu-id="a7ca5-122">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="a7ca5-122">Protected Member Variables</span></span>                                      | <span data-ttu-id="a7ca5-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7ca5-123">Description</span></span>                                                                |
|-----------------------------------------------------------------|----------------------------------------------------------------------------|
| [<span data-ttu-id="a7ca5-124">**\_pAllocator m**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-124">**m\_pAllocator**</span></span>](cbaseoutputpin-m-pallocator.md)            | <span data-ttu-id="a7ca5-125">Ponteiro para o alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-125">Pointer to the memory allocator.</span></span>                                           |
| [<span data-ttu-id="a7ca5-126">**\_pInputPin m**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-126">**m\_pInputPin**</span></span>](cbaseoutputpin-m-pinputpin.md)              | <span data-ttu-id="a7ca5-127">Ponteiro para o pino de entrada conectado a este pin.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-127">Pointer to the input pin connected to this pin.</span></span>                            |
| <span data-ttu-id="a7ca5-128">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="a7ca5-128">Public Methods</span></span>                                                  | <span data-ttu-id="a7ca5-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7ca5-129">Description</span></span>                                                                |
| [<span data-ttu-id="a7ca5-130">**CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-130">**CBaseOutputPin**</span></span>](cbaseoutputpin-cbaseoutputpin.md)         | <span data-ttu-id="a7ca5-131">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-131">Constructor method.</span></span>                                                        |
| [<span data-ttu-id="a7ca5-132">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-132">**CompleteConnect**</span></span>](cbaseoutputpin-completeconnect.md)       | <span data-ttu-id="a7ca5-133">Conclui uma conexão com um PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-133">Completes a connection to an input pin.</span></span> <span data-ttu-id="a7ca5-134">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-134">Virtual.</span></span>                           |
| [<span data-ttu-id="a7ca5-135">**DecideAllocator**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-135">**DecideAllocator**</span></span>](cbaseoutputpin-decideallocator.md)       | <span data-ttu-id="a7ca5-136">Seleciona um alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-136">Selects a memory allocator.</span></span> <span data-ttu-id="a7ca5-137">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-137">Virtual.</span></span>                                       |
| [<span data-ttu-id="a7ca5-138">**GetDeliveryBuffer**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-138">**GetDeliveryBuffer**</span></span>](cbaseoutputpin-getdeliverybuffer.md)   | <span data-ttu-id="a7ca5-139">Recupera um exemplo de mídia que contém um buffer vazio.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-139">Retrieves a media sample that contains an empty buffer.</span></span> <span data-ttu-id="a7ca5-140">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-140">Virtual.</span></span>           |
| [<span data-ttu-id="a7ca5-141">**Fornecimento**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-141">**Deliver**</span></span>](cbaseoutputpin-deliver.md)                       | <span data-ttu-id="a7ca5-142">Entrega um exemplo de mídia para o pino de entrada conectado.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-142">Delivers a media sample to the connected input pin.</span></span> <span data-ttu-id="a7ca5-143">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-143">Virtual.</span></span>               |
| [<span data-ttu-id="a7ca5-144">**InitAllocator**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-144">**InitAllocator**</span></span>](cbaseoutputpin-initallocator.md)           | <span data-ttu-id="a7ca5-145">Cria um alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-145">Creates a memory allocator.</span></span> <span data-ttu-id="a7ca5-146">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-146">Virtual.</span></span>                                       |
| [<span data-ttu-id="a7ca5-147">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-147">**CheckConnect**</span></span>](cbaseoutputpin-checkconnect.md)             | <span data-ttu-id="a7ca5-148">Determina se uma conexão de PIN é adequada.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-148">Determines whether a pin connection is suitable.</span></span>                           |
| [<span data-ttu-id="a7ca5-149">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-149">**BreakConnect**</span></span>](cbaseoutputpin-breakconnect.md)             | <span data-ttu-id="a7ca5-150">Libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-150">Releases the pin from a connection.</span></span>                                        |
| [<span data-ttu-id="a7ca5-151">**Activo**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-151">**Active**</span></span>](cbaseoutputpin-active.md)                         | <span data-ttu-id="a7ca5-152">Notifica o PIN de que o filtro está ativo agora.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-152">Notifies the pin that the filter is now active.</span></span>                            |
| [<span data-ttu-id="a7ca5-153">**Inativo**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-153">**Inactive**</span></span>](cbaseoutputpin-inactive.md)                     | <span data-ttu-id="a7ca5-154">Notifica o PIN de que o filtro não está mais ativo.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-154">Notifies the pin that the filter is no longer active.</span></span>                      |
| [<span data-ttu-id="a7ca5-155">**DeliverEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-155">**DeliverEndOfStream**</span></span>](cbaseoutputpin-deliverendofstream.md) | <span data-ttu-id="a7ca5-156">Entrega uma notificação de fim de fluxo para o PIN de entrada conectado. VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-156">Delivers an end-of-stream notification to the connected input pin.Virtual.</span></span> |
| [<span data-ttu-id="a7ca5-157">**DeliverBeginFlush**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-157">**DeliverBeginFlush**</span></span>](cbaseoutputpin-deliverbeginflush.md)   | <span data-ttu-id="a7ca5-158">Solicita que o PIN de entrada conectado inicie uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-158">Requests the connected input pin to begin a flush operation.</span></span> <span data-ttu-id="a7ca5-159">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-159">Virtual.</span></span>      |
| [<span data-ttu-id="a7ca5-160">**DeliverEndFlush**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-160">**DeliverEndFlush**</span></span>](cbaseoutputpin-deliverendflush.md)       | <span data-ttu-id="a7ca5-161">Solicita que o PIN de entrada conectado Finalize uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-161">Requests the connected input pin to end a flush operation.</span></span> <span data-ttu-id="a7ca5-162">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-162">Virtual.</span></span>        |
| [<span data-ttu-id="a7ca5-163">**DeliverNewSegment**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-163">**DeliverNewSegment**</span></span>](cbaseoutputpin-delivernewsegment.md)   | <span data-ttu-id="a7ca5-164">Entrega uma notificação de novo segmento para o PIN de entrada conectado.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-164">Delivers a new-segment notification to the connected input pin.</span></span> <span data-ttu-id="a7ca5-165">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-165">Virtual.</span></span>   |
| <span data-ttu-id="a7ca5-166">Métodos virtuais puros</span><span class="sxs-lookup"><span data-stu-id="a7ca5-166">Pure Virtual Methods</span></span>                                            | <span data-ttu-id="a7ca5-167">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7ca5-167">Description</span></span>                                                                |
| [<span data-ttu-id="a7ca5-168">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-168">**DecideBufferSize**</span></span>](cbaseoutputpin-decidebuffersize.md)     | <span data-ttu-id="a7ca5-169">Define os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-169">Sets the buffer requirements.</span></span>                                              |
| <span data-ttu-id="a7ca5-170">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="a7ca5-170">IPin Methods</span></span>                                                    | <span data-ttu-id="a7ca5-171">Descrição</span><span class="sxs-lookup"><span data-stu-id="a7ca5-171">Description</span></span>                                                                |
| [<span data-ttu-id="a7ca5-172">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-172">**BeginFlush**</span></span>](cbaseoutputpin-beginflush.md)                 | <span data-ttu-id="a7ca5-173">Inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-173">Begins a flush operation.</span></span>                                                  |
| [<span data-ttu-id="a7ca5-174">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-174">**EndFlush**</span></span>](cbaseoutputpin-endflush.md)                     | <span data-ttu-id="a7ca5-175">Finaliza uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-175">Ends a flush operation.</span></span>                                                    |
| [<span data-ttu-id="a7ca5-176">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="a7ca5-176">**EndOfStream**</span></span>](cbaseoutputpin-endofstream.md)               | <span data-ttu-id="a7ca5-177">Notifica o PIN de que nenhum dado adicional é esperado.</span><span class="sxs-lookup"><span data-stu-id="a7ca5-177">Notifies the pin that no additional data is expected.</span></span>                      |



 

## <a name="requirements"></a><span data-ttu-id="a7ca5-178">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7ca5-178">Requirements</span></span>



| <span data-ttu-id="a7ca5-179">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7ca5-179">Requirement</span></span> | <span data-ttu-id="a7ca5-180">Valor</span><span class="sxs-lookup"><span data-stu-id="a7ca5-180">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7ca5-181">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7ca5-181">Header</span></span><br/>  | <dl> <span data-ttu-id="a7ca5-182"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7ca5-182"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a7ca5-183">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7ca5-183">Library</span></span><br/> | <dl> <span data-ttu-id="a7ca5-184"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a7ca5-184"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




