---
description: A classe CRenderedInputPin é uma classe base para implementar um PIN de entrada em um processador.
ms.assetid: 644dc6ef-eefa-4dfa-a27e-cab690b6e1db
title: Classe CRenderedInputPin (Amextra. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRenderedInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3fc00b4aa0ce1fc6c8a93fb2fbda2118ad6bb40e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756187"
---
# <a name="crenderedinputpin-class"></a><span data-ttu-id="032fe-103">Classe CRenderedInputPin</span><span class="sxs-lookup"><span data-stu-id="032fe-103">CRenderedInputPin class</span></span>

![hierarquia de classe crenderedinputpin](images/rbase04.png)

<span data-ttu-id="032fe-105">A classe **CRenderedInputPin** é uma classe base para implementar um PIN de entrada em um processador.</span><span class="sxs-lookup"><span data-stu-id="032fe-105">The **CRenderedInputPin** class is a base class for implementing an input pin on a renderer.</span></span> <span data-ttu-id="032fe-106">Essa classe é projetada para filtros de processador que não derivam da classe [**CBaseRenderer**](cbaserenderer.md) .</span><span class="sxs-lookup"><span data-stu-id="032fe-106">This class is designed for renderer filters that do not derive from the [**CBaseRenderer**](cbaserenderer.md) class.</span></span> <span data-ttu-id="032fe-107">(Os filtros que derivam de **CBaseRenderer** devem usar a classe [**CRendererInputPin**](crendererinputpin.md) para o pino de entrada.)</span><span class="sxs-lookup"><span data-stu-id="032fe-107">(Filters that derive from **CBaseRenderer** should use the [**CRendererInputPin**](crendererinputpin.md) class for the input pin.)</span></span>

<span data-ttu-id="032fe-108">Para usar essa classe, você deve fazer pelo menos o seguinte:</span><span class="sxs-lookup"><span data-stu-id="032fe-108">To use this class, you must do at least the following:</span></span>

-   <span data-ttu-id="032fe-109">Declare uma nova classe de PIN que herde **CRenderedInputPin**.</span><span class="sxs-lookup"><span data-stu-id="032fe-109">Declare a new pin class that inherits **CRenderedInputPin**.</span></span>
-   <span data-ttu-id="032fe-110">Na sua classe PIN, declare um objeto de seção crítica para manter o bloqueio de streaming.</span><span class="sxs-lookup"><span data-stu-id="032fe-110">In your pin class, declare a critical section object to hold the streaming lock.</span></span> <span data-ttu-id="032fe-111">Você pode usar a classe [**CCritSec**](ccritsec.md) para essa finalidade.</span><span class="sxs-lookup"><span data-stu-id="032fe-111">You can use the [**CCritSec**](ccritsec.md) class for this purpose.</span></span> <span data-ttu-id="032fe-112">Para obter mais informações, consulte [threads and Critical Sections](threads-and-critical-sections.md).</span><span class="sxs-lookup"><span data-stu-id="032fe-112">For more information, see [Threads and Critical Sections](threads-and-critical-sections.md).</span></span>
-   <span data-ttu-id="032fe-113">Substitua [**CRenderedInputPin:: EndOfStream**](crenderedinputpin-endofstream.md) para manter o bloqueio de streaming.</span><span class="sxs-lookup"><span data-stu-id="032fe-113">Override [**CRenderedInputPin::EndOfStream**](crenderedinputpin-endofstream.md) to hold the streaming lock.</span></span>
-   <span data-ttu-id="032fe-114">Implemente os métodos [**IMemInputPin:: Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin:: CheckMediaType**](cbasepin-checkmediatype.md)e [**CBasePin:: GetMediaType**](cbasepin-getmediatype.md) .</span><span class="sxs-lookup"><span data-stu-id="032fe-114">Implement the [**IMemInputPin::Receive**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receive), [**CBasePin::CheckMediaType**](cbasepin-checkmediatype.md), and [**CBasePin::GetMediaType**](cbasepin-getmediatype.md) methods.</span></span>
-   <span data-ttu-id="032fe-115">Em seu filtro, implemente [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) para retornar uma instância da sua classe PIN.</span><span class="sxs-lookup"><span data-stu-id="032fe-115">In your filter, implement [**CBaseFilter::GetPin**](cbasefilter-getpin.md) to return an instance of your pin class.</span></span>

<span data-ttu-id="032fe-116">Você pode usar essa classe em um processador que tem mais de um PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="032fe-116">You can use this class in a renderer that has more than one input pin.</span></span> <span data-ttu-id="032fe-117">Essa classe herda a classe [**CBaseInputPin**](cbaseinputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="032fe-117">This class inherits the [**CBaseInputPin**](cbaseinputpin.md) class.</span></span>



| <span data-ttu-id="032fe-118">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="032fe-118">Protected Member Variables</span></span>                                            | <span data-ttu-id="032fe-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="032fe-119">Description</span></span>                                                                                                  |
|-----------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="032fe-120">**\_bAtEndOfStream m**</span><span class="sxs-lookup"><span data-stu-id="032fe-120">**m\_bAtEndOfStream**</span></span>](crenderedinputpin-m-batendofstream.md)       | <span data-ttu-id="032fe-121">Indica se o fim do fluxo foi atingido.</span><span class="sxs-lookup"><span data-stu-id="032fe-121">Indicates whether the end of the stream was reached.</span></span>                                                         |
| [<span data-ttu-id="032fe-122">**\_bCompleteNotified m**</span><span class="sxs-lookup"><span data-stu-id="032fe-122">**m\_bCompleteNotified**</span></span>](crenderedinputpin-m-bcompletenotified.md) | <span data-ttu-id="032fe-123">Indica se o PIN enviou um evento do [**EC \_ Complete**](ec-complete.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="032fe-123">Indicates whether the pin has sent an [**EC\_COMPLETE**](ec-complete.md) event to the Filter Graph Manager.</span></span> |
| <span data-ttu-id="032fe-124">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="032fe-124">Public Methods</span></span>                                                        | <span data-ttu-id="032fe-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="032fe-125">Description</span></span>                                                                                                  |
| [<span data-ttu-id="032fe-126">**Ativo**</span><span class="sxs-lookup"><span data-stu-id="032fe-126">**Active**</span></span>](crenderedinputpin-active.md)                            | <span data-ttu-id="032fe-127">Notifica o PIN de que o filtro está ativo agora.</span><span class="sxs-lookup"><span data-stu-id="032fe-127">Notifies the pin that the filter is now active.</span></span>                                                              |
| [<span data-ttu-id="032fe-128">**CRenderedInputPin**</span><span class="sxs-lookup"><span data-stu-id="032fe-128">**CRenderedInputPin**</span></span>](crenderedinputpin-crenderedinputpin.md)      | <span data-ttu-id="032fe-129">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="032fe-129">Constructor method.</span></span>                                                                                          |
| [<span data-ttu-id="032fe-130">**Executar**</span><span class="sxs-lookup"><span data-stu-id="032fe-130">**Run**</span></span>](crenderedinputpin-run.md)                                  | <span data-ttu-id="032fe-131">Notifica o PIN de que o filtro agora está em execução.</span><span class="sxs-lookup"><span data-stu-id="032fe-131">Notifies the pin that the filter is now running.</span></span>                                                             |
| <span data-ttu-id="032fe-132">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="032fe-132">IPin Methods</span></span>                                                          | <span data-ttu-id="032fe-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="032fe-133">Description</span></span>                                                                                                  |
| [<span data-ttu-id="032fe-134">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="032fe-134">**EndFlush**</span></span>](crenderedinputpin-endflush.md)                        | <span data-ttu-id="032fe-135">Finaliza uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="032fe-135">Ends a flush operation.</span></span>                                                                                      |
| [<span data-ttu-id="032fe-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="032fe-136">**EndOfStream**</span></span>](crenderedinputpin-endofstream.md)                  | <span data-ttu-id="032fe-137">Notifica o PIN de que nenhum dado adicional é esperado até que o filtro receba um novo comando de execução.</span><span class="sxs-lookup"><span data-stu-id="032fe-137">Notifies the pin that no additional data is expected until the filter receives a new run command.</span></span>            |



 

## <a name="requirements"></a><span data-ttu-id="032fe-138">Requisitos</span><span class="sxs-lookup"><span data-stu-id="032fe-138">Requirements</span></span>



| <span data-ttu-id="032fe-139">Requisito</span><span class="sxs-lookup"><span data-stu-id="032fe-139">Requirement</span></span> | <span data-ttu-id="032fe-140">Valor</span><span class="sxs-lookup"><span data-stu-id="032fe-140">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="032fe-141">parâmetro</span><span class="sxs-lookup"><span data-stu-id="032fe-141">Header</span></span><br/>  | <dl> <span data-ttu-id="032fe-142"><dt>Amextra. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="032fe-142"><dt>Amextra.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="032fe-143">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="032fe-143">Library</span></span><br/> | <dl> <span data-ttu-id="032fe-144"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="032fe-144"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




