---
description: Essa classe implementa a interface IAMStreamControl para Pins de entrada e saída.
ms.assetid: a0ddc2d5-8385-4209-b1c5-9822c30f8a02
title: Classe CBaseStreamControl (Strmctl. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseStreamControl
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c20a4f08040bdb2c71bdd8f09aa657719228efa5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748635"
---
# <a name="cbasestreamcontrol-class"></a><span data-ttu-id="a2586-103">Classe CBaseStreamControl</span><span class="sxs-lookup"><span data-stu-id="a2586-103">CBaseStreamControl class</span></span>

![hierarquia de classe CBaseStreamControl](images/strmctl1.png)

<span data-ttu-id="a2586-105">Essa classe implementa a interface [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) para Pins de entrada e saída.</span><span class="sxs-lookup"><span data-stu-id="a2586-105">This class implements the [**IAMStreamControl**](/windows/desktop/api/Strmif/nn-strmif-iamstreamcontrol) interface for input and output pins.</span></span> <span data-ttu-id="a2586-106">Ele fornece controle sobre como iniciar e parar um PIN individual no filtro.</span><span class="sxs-lookup"><span data-stu-id="a2586-106">It provides control over starting and stopping an individual pin on the filter.</span></span> <span data-ttu-id="a2586-107">Um PIN que dá suporte a **IAMStreamControl** deve herdar dessa classe base.</span><span class="sxs-lookup"><span data-stu-id="a2586-107">A pin that supports **IAMStreamControl** should inherit from this base class.</span></span> <span data-ttu-id="a2586-108">Veja a seguir uma declaração típica para um PIN de entrada:</span><span class="sxs-lookup"><span data-stu-id="a2586-108">The following is a typical declaration for an input pin:</span></span>

``` syntax
class CMyInputPin : public CBaseInputPin, public CBaseStreamControl
```

<span data-ttu-id="a2586-109">Certifique-se de substituir **NonDelegatingQueryInteface** para expor **IAMStreamControl**.</span><span class="sxs-lookup"><span data-stu-id="a2586-109">Be sure to override **NonDelegatingQueryInteface** to expose **IAMStreamControl**.</span></span> <span data-ttu-id="a2586-110">Para obter mais informações, consulte [como implementar IUnknown](how-to-implement-iunknown.md).</span><span class="sxs-lookup"><span data-stu-id="a2586-110">For more information, see [How to Implement IUnknown](how-to-implement-iunknown.md).</span></span>



| <span data-ttu-id="a2586-111">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="a2586-111">Public Methods</span></span>                                                        | <span data-ttu-id="a2586-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2586-112">Description</span></span>                                                                                          |
|-----------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="a2586-113">**CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="a2586-113">**CBaseStreamControl**</span></span>](cbasestreamcontrol-cbasestreamcontrol.md)   | <span data-ttu-id="a2586-114">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="a2586-114">Constructor method.</span></span>                                                                                  |
| [<span data-ttu-id="a2586-115">**~ CBaseStreamControl**</span><span class="sxs-lookup"><span data-stu-id="a2586-115">**~CBaseStreamControl**</span></span>](cbasestreamcontrol--cbasestreamcontrol.md) | <span data-ttu-id="a2586-116">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="a2586-116">Destructor method.</span></span>                                                                                   |
| [<span data-ttu-id="a2586-117">**CheckStreamState**</span><span class="sxs-lookup"><span data-stu-id="a2586-117">**CheckStreamState**</span></span>](cbasestreamcontrol-checkstreamstate.md)       | <span data-ttu-id="a2586-118">Determina se um exemplo de mídia deve ser entregue ou descartado.</span><span class="sxs-lookup"><span data-stu-id="a2586-118">Determines whether a media sample should be delivered or discarded.</span></span>                                  |
| [<span data-ttu-id="a2586-119">**Liberação**</span><span class="sxs-lookup"><span data-stu-id="a2586-119">**Flushing**</span></span>](cbasestreamcontrol-flushing.md)                       | <span data-ttu-id="a2586-120">Notifica a classe base que o PIN iniciou ou parou a liberação.</span><span class="sxs-lookup"><span data-stu-id="a2586-120">Notifies the base class that the pin has started or stopped flushing.</span></span>                                |
| [<span data-ttu-id="a2586-121">**NotifyFilterState**</span><span class="sxs-lookup"><span data-stu-id="a2586-121">**NotifyFilterState**</span></span>](cbasestreamcontrol-notifyfilterstate.md)     | <span data-ttu-id="a2586-122">Notifica o PIN quando o estado do filtro é alterado.</span><span class="sxs-lookup"><span data-stu-id="a2586-122">Notifies the pin when the filter's state changes.</span></span>                                                    |
| [<span data-ttu-id="a2586-123">**SetFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="a2586-123">**SetFilterGraph**</span></span>](cbasestreamcontrol-setfiltergraph.md)           | <span data-ttu-id="a2586-124">Especifica o coletor de eventos para eventos de controle de fluxo.</span><span class="sxs-lookup"><span data-stu-id="a2586-124">Specifies the event sink for stream control events.</span></span>                                                  |
| [<span data-ttu-id="a2586-125">**Setsynce**</span><span class="sxs-lookup"><span data-stu-id="a2586-125">**SetSyncSource**</span></span>](cbasestreamcontrol-setsyncsource.md)             | <span data-ttu-id="a2586-126">Notifica a classe base do relógio de referência atual.</span><span class="sxs-lookup"><span data-stu-id="a2586-126">Notifies the base class of the current reference clock.</span></span>                                              |
| <span data-ttu-id="a2586-127">Métodos IAMStreamControl</span><span class="sxs-lookup"><span data-stu-id="a2586-127">IAMStreamControl Methods</span></span>                                              | <span data-ttu-id="a2586-128">Descrição</span><span class="sxs-lookup"><span data-stu-id="a2586-128">Description</span></span>                                                                                          |
| [<span data-ttu-id="a2586-129">**GetInfo**</span><span class="sxs-lookup"><span data-stu-id="a2586-129">**GetInfo**</span></span>](cbasestreamcontrol-getinfo.md)                         | <span data-ttu-id="a2586-130">Recupera informações sobre as configurações de controle de fluxo atuais, incluindo os horários de início e de parada.</span><span class="sxs-lookup"><span data-stu-id="a2586-130">Retrieves information about the current stream-control settings, including the start and stop times.</span></span> |
| [<span data-ttu-id="a2586-131">**StartAt**</span><span class="sxs-lookup"><span data-stu-id="a2586-131">**StartAt**</span></span>](cbasestreamcontrol-startat.md)                         | <span data-ttu-id="a2586-132">Informa o PIN quando iniciar a entrega de dados.</span><span class="sxs-lookup"><span data-stu-id="a2586-132">Informs the pin when to start delivering data.</span></span>                                                       |
| [<span data-ttu-id="a2586-133">**StopAt**</span><span class="sxs-lookup"><span data-stu-id="a2586-133">**StopAt**</span></span>](cbasestreamcontrol-stopat.md)                           | <span data-ttu-id="a2586-134">Informa o PIN quando parar de entregar dados.</span><span class="sxs-lookup"><span data-stu-id="a2586-134">Informs the pin when to stop delivering data.</span></span>                                                        |



 

## <a name="remarks"></a><span data-ttu-id="a2586-135">Comentários</span><span class="sxs-lookup"><span data-stu-id="a2586-135">Remarks</span></span>

<span data-ttu-id="a2586-136">Essa classe requer o PIN e o filtro proprietário para notificar a classe quando vários eventos ocorrem, como o filtro ingressando no grafo ou recebendo um novo relógio de referência.</span><span class="sxs-lookup"><span data-stu-id="a2586-136">This class requires the pin and the owning filter to notify the class when various events occur, such as the filter joining the graph or receiving a new reference clock.</span></span> <span data-ttu-id="a2586-137">Você deve chamar os seguintes métodos de classe:</span><span class="sxs-lookup"><span data-stu-id="a2586-137">You should call the following class methods:</span></span>

-   <span data-ttu-id="a2586-138">No método [**IMediaFilter:: Setsincronizate**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) do filtro, chame o método [**CBaseStreamControl:: setsincronizate**](cbasestreamcontrol-setsyncsource.md) .</span><span class="sxs-lookup"><span data-stu-id="a2586-138">In the filter's [**IMediaFilter::SetSyncSource**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-setsyncsource) method, call the [**CBaseStreamControl::SetSyncSource**](cbasestreamcontrol-setsyncsource.md) method.</span></span> <span data-ttu-id="a2586-139">Esse método notifica a classe do relógio de referência atual.</span><span class="sxs-lookup"><span data-stu-id="a2586-139">This method notifies the class of the current reference clock.</span></span>
-   <span data-ttu-id="a2586-140">No método [**CBaseFilter:: JoinFilterGraph**](cbasefilter-joinfiltergraph.md) do filtro, chame o método [**CBaseStreamControl:: SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) .</span><span class="sxs-lookup"><span data-stu-id="a2586-140">In the filter's [**CBaseFilter::JoinFilterGraph**](cbasefilter-joinfiltergraph.md) method, call the [**CBaseStreamControl::SetFilterGraph**](cbasestreamcontrol-setfiltergraph.md) method.</span></span> <span data-ttu-id="a2586-141">Esse método fornece à classe um ponteiro para o Gerenciador do grafo de filtro, para que a classe possa enviar os eventos de controle de fluxo corretos.</span><span class="sxs-lookup"><span data-stu-id="a2586-141">This method gives the class a pointer to the Filter Graph Manager, so that the class can send the right stream-control events.</span></span>
-   <span data-ttu-id="a2586-142">Sempre que o filtro muda de estado (para em execução, em pausa ou parado), chame o método [**CBaseStreamControl:: NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) .</span><span class="sxs-lookup"><span data-stu-id="a2586-142">Whenever the filter changes state (to running, paused, or stopped), call the [**CBaseStreamControl::NotifyFilterState**](cbasestreamcontrol-notifyfilterstate.md) method.</span></span>
-   <span data-ttu-id="a2586-143">Nos métodos [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) e [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) do PIN, chame o método [**CBaseStreamControl:: flush**](cbasestreamcontrol-flushing.md) .</span><span class="sxs-lookup"><span data-stu-id="a2586-143">In the pin's [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) and [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) methods, call the [**CBaseStreamControl::Flushing**](cbasestreamcontrol-flushing.md) method.</span></span>

<span data-ttu-id="a2586-144">A `CBaseStreamControl` classe usa o relógio de referência do grafo de filtro para determinar quais exemplos o filtro deve ser entregue e qual deve descartar.</span><span class="sxs-lookup"><span data-stu-id="a2586-144">The `CBaseStreamControl` class uses the filter graph's reference clock to determine which samples the filter should be deliver, and which it should discard.</span></span> <span data-ttu-id="a2586-145">No método [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) do PIN, chame o método [**CBaseStreamControl:: CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) com um ponteiro para o exemplo de mídia de entrada.</span><span class="sxs-lookup"><span data-stu-id="a2586-145">In your pin's [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive) method, call the [**CBaseStreamControl::CheckStreamState**](cbasestreamcontrol-checkstreamstate.md) method with a pointer to the incoming media sample.</span></span> <span data-ttu-id="a2586-146">Se o método retornar o fluxo de valores \_ fluindo, entregue o downstream de exemplo.</span><span class="sxs-lookup"><span data-stu-id="a2586-146">If the method returns the value STREAM\_FLOWING, deliver the sample downstream.</span></span> <span data-ttu-id="a2586-147">Caso contrário, descarte-o.</span><span class="sxs-lookup"><span data-stu-id="a2586-147">Otherwise, discard it.</span></span>

## <a name="requirements"></a><span data-ttu-id="a2586-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a2586-148">Requirements</span></span>



| <span data-ttu-id="a2586-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="a2586-149">Requirement</span></span> | <span data-ttu-id="a2586-150">Valor</span><span class="sxs-lookup"><span data-stu-id="a2586-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a2586-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a2586-151">Header</span></span><br/>  | <dl> <span data-ttu-id="a2586-152"><dt>Strmctl. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a2586-152"><dt>Strmctl.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a2586-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a2586-153">Library</span></span><br/> | <dl> <span data-ttu-id="a2586-154"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a2586-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




