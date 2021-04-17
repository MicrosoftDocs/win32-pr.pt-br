---
description: A classe CSource é uma classe base para implementar filtros de origem. Um filtro derivado de CSource contém um ou mais Pins de saída derivados da classe CSourceStream. Cada pino de saída cria um thread de trabalho que envia amostras de mídia por push downstream.
ms.assetid: 25bd0334-4ad1-48ed-93f9-b36c13a280a3
title: Classe CSource (Source. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSource
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a4fcecbd1973c54e30c9bf1251bed174aa4a469f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105768797"
---
# <a name="csource-class"></a><span data-ttu-id="beb4f-105">Classe CSource</span><span class="sxs-lookup"><span data-stu-id="beb4f-105">CSource class</span></span>

![hierarquia de classe CSource](images/source01.png)

<span data-ttu-id="beb4f-107">A classe **CSource** é uma classe base para implementar filtros de origem.</span><span class="sxs-lookup"><span data-stu-id="beb4f-107">The **CSource** class is a base class for implementing source filters.</span></span> <span data-ttu-id="beb4f-108">Um filtro derivado de **CSource** contém um ou mais Pins de saída derivados da classe [**CSourceStream**](csourcestream.md) .</span><span class="sxs-lookup"><span data-stu-id="beb4f-108">A filter derived from **CSource** contains one or more output pins derived from the [**CSourceStream**](csourcestream.md) class.</span></span> <span data-ttu-id="beb4f-109">Cada pino de saída cria um thread de trabalho que envia amostras de mídia por push downstream.</span><span class="sxs-lookup"><span data-stu-id="beb4f-109">Each output pin creates a worker thread that pushes media samples downstream.</span></span>

> [!Note]  
> <span data-ttu-id="beb4f-110">A classe **CSource** foi projetada para dar suporte ao modelo de push para o fluxo de dados.</span><span class="sxs-lookup"><span data-stu-id="beb4f-110">The **CSource** class is designed to support the push model for data flow.</span></span> <span data-ttu-id="beb4f-111">Essa classe não é recomendada para a criação de filtros de leitor de arquivo.</span><span class="sxs-lookup"><span data-stu-id="beb4f-111">This class is not recommended for creating file-reader filters.</span></span> <span data-ttu-id="beb4f-112">Os leitores de arquivo devem dar suporte ao modelo de pull, por meio da interface [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) .</span><span class="sxs-lookup"><span data-stu-id="beb4f-112">File readers should support the pull model, through the [**IAsyncReader**](/windows/desktop/api/Strmif/nn-strmif-iasyncreader) interface.</span></span> <span data-ttu-id="beb4f-113">Para obter mais informações, consulte [fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="beb4f-113">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

 



| <span data-ttu-id="beb4f-114">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="beb4f-114">Protected Member Variables</span></span>                     | <span data-ttu-id="beb4f-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="beb4f-115">Description</span></span>                                                  |
|------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="beb4f-116">**\_iPins m**</span><span class="sxs-lookup"><span data-stu-id="beb4f-116">**m\_iPins**</span></span>](csource-m-ipins.md)            | <span data-ttu-id="beb4f-117">Número de Pins no filtro.</span><span class="sxs-lookup"><span data-stu-id="beb4f-117">Number of pins on the filter.</span></span>                                |
| [<span data-ttu-id="beb4f-118">**\_paStreams m**</span><span class="sxs-lookup"><span data-stu-id="beb4f-118">**m\_paStreams**</span></span>](csource-m-pastreams.md)    | <span data-ttu-id="beb4f-119">Matriz de Pins.</span><span class="sxs-lookup"><span data-stu-id="beb4f-119">Array of pins.</span></span>                                               |
| [<span data-ttu-id="beb4f-120">**\_cStateLock m**</span><span class="sxs-lookup"><span data-stu-id="beb4f-120">**m\_cStateLock**</span></span>](csource-m-cstatelock.md)  | <span data-ttu-id="beb4f-121">Objeto de seção crítica que protege o estado do filtro.</span><span class="sxs-lookup"><span data-stu-id="beb4f-121">Critical section object that protects the filter state.</span></span>      |
| <span data-ttu-id="beb4f-122">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="beb4f-122">Public Methods</span></span>                                 | <span data-ttu-id="beb4f-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="beb4f-123">Description</span></span>                                                  |
| [<span data-ttu-id="beb4f-124">**CSource**</span><span class="sxs-lookup"><span data-stu-id="beb4f-124">**CSource**</span></span>](csource-csource.md)             | <span data-ttu-id="beb4f-125">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="beb4f-125">Constructor method.</span></span>                                          |
| [<span data-ttu-id="beb4f-126">**~ CSource**</span><span class="sxs-lookup"><span data-stu-id="beb4f-126">**~CSource**</span></span>](csource--csource.md)           | <span data-ttu-id="beb4f-127">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="beb4f-127">Destructor method.</span></span>                                           |
| [<span data-ttu-id="beb4f-128">**GetPinCount**</span><span class="sxs-lookup"><span data-stu-id="beb4f-128">**GetPinCount**</span></span>](csource-getpincount.md)     | <span data-ttu-id="beb4f-129">Recupera o número de Pins no filtro.</span><span class="sxs-lookup"><span data-stu-id="beb4f-129">Retrieves the number of pins on the filter.</span></span>                  |
| [<span data-ttu-id="beb4f-130">**GetPin**</span><span class="sxs-lookup"><span data-stu-id="beb4f-130">**GetPin**</span></span>](csource-getpin.md)               | <span data-ttu-id="beb4f-131">Recupera um PIN.</span><span class="sxs-lookup"><span data-stu-id="beb4f-131">Retrieves a pin.</span></span>                                             |
| [<span data-ttu-id="beb4f-132">**pStateLock**</span><span class="sxs-lookup"><span data-stu-id="beb4f-132">**pStateLock**</span></span>](csource--pstatelock.md)      | <span data-ttu-id="beb4f-133">Recupera um ponteiro para o objeto de seção crítica do filtro.</span><span class="sxs-lookup"><span data-stu-id="beb4f-133">Retrieves a pointer to the filter's critical section object.</span></span> |
| [<span data-ttu-id="beb4f-134">**AddPin**</span><span class="sxs-lookup"><span data-stu-id="beb4f-134">**AddPin**</span></span>](csource-addpin.md)               | <span data-ttu-id="beb4f-135">Adiciona um novo pino de saída ao filtro.</span><span class="sxs-lookup"><span data-stu-id="beb4f-135">Adds a new output pin to the filter.</span></span>                         |
| [<span data-ttu-id="beb4f-136">**RemovePin**</span><span class="sxs-lookup"><span data-stu-id="beb4f-136">**RemovePin**</span></span>](csource-removepin.md)         | <span data-ttu-id="beb4f-137">Remove um PIN especificado do filtro.</span><span class="sxs-lookup"><span data-stu-id="beb4f-137">Removes a specified pin from the filter.</span></span>                     |
| [<span data-ttu-id="beb4f-138">**FindPinNumber**</span><span class="sxs-lookup"><span data-stu-id="beb4f-138">**FindPinNumber**</span></span>](csource-findpinnumber.md) | <span data-ttu-id="beb4f-139">Recupera o número de um PIN especificado no filtro.</span><span class="sxs-lookup"><span data-stu-id="beb4f-139">Retrieves the number of a specified pin on the filter.</span></span>       |
| <span data-ttu-id="beb4f-140">Métodos IBaseFilter</span><span class="sxs-lookup"><span data-stu-id="beb4f-140">IBaseFilter Methods</span></span>                            | <span data-ttu-id="beb4f-141">Descrição</span><span class="sxs-lookup"><span data-stu-id="beb4f-141">Description</span></span>                                                  |
| [<span data-ttu-id="beb4f-142">**FindPin**</span><span class="sxs-lookup"><span data-stu-id="beb4f-142">**FindPin**</span></span>](csource-findpin.md)             | <span data-ttu-id="beb4f-143">Recupera o PIN com o identificador especificado.</span><span class="sxs-lookup"><span data-stu-id="beb4f-143">Retrieves the pin with the specified identifier.</span></span>             |



 

## <a name="remarks"></a><span data-ttu-id="beb4f-144">Comentários</span><span class="sxs-lookup"><span data-stu-id="beb4f-144">Remarks</span></span>

<span data-ttu-id="beb4f-145">Para implementar um PIN de saída, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="beb4f-145">To implement an output pin, do the following:</span></span>

-   <span data-ttu-id="beb4f-146">Derive uma classe de [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="beb4f-146">Derive a class from [**CSourceStream**](csourcestream.md).</span></span>
-   <span data-ttu-id="beb4f-147">Substitua o método [**CSourceStream:: GetMediaType**](csourcestream-getmediatype.md) e, possivelmente, o método [**CSourceStream:: CheckMediaType**](csourcestream-checkmediatype.md) , que valida os tipos de mídia para o PIN.</span><span class="sxs-lookup"><span data-stu-id="beb4f-147">Override the [**CSourceStream::GetMediaType**](csourcestream-getmediatype.md) method and possibly the [**CSourceStream::CheckMediaType**](csourcestream-checkmediatype.md) method, which validate media types for the pin.</span></span>
-   <span data-ttu-id="beb4f-148">Implemente o método [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) , que retorna os requisitos de buffer do PIN.</span><span class="sxs-lookup"><span data-stu-id="beb4f-148">Implement the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method, which returns the pin's buffer requirements.</span></span>
-   <span data-ttu-id="beb4f-149">Implemente o método [**CSourceStream:: FillBuffer**](csourcestream-fillbuffer.md) , que preenche um buffer de exemplo de mídia com dados.</span><span class="sxs-lookup"><span data-stu-id="beb4f-149">Implement the [**CSourceStream::FillBuffer**](csourcestream-fillbuffer.md) method, which fills a media sample buffer with data.</span></span>

<span data-ttu-id="beb4f-150">Para implementar o filtro, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="beb4f-150">To implement the filter, do the following:</span></span>

-   <span data-ttu-id="beb4f-151">Derive uma classe de **CSource**.</span><span class="sxs-lookup"><span data-stu-id="beb4f-151">Derive a class from **CSource**.</span></span>
-   <span data-ttu-id="beb4f-152">No construtor, crie um ou mais Pins de saída derivados de [**CSourceStream**](csourcestream.md).</span><span class="sxs-lookup"><span data-stu-id="beb4f-152">In the constructor, create one or more output pins derived from [**CSourceStream**](csourcestream.md).</span></span> <span data-ttu-id="beb4f-153">Os PINs se adicionam automaticamente ao filtro em seus métodos de construtor e se removem em seus métodos destruidores.</span><span class="sxs-lookup"><span data-stu-id="beb4f-153">The pins automatically add themselves to the filter in their constructor methods, and remove themselves in their destructor methods.</span></span>

<span data-ttu-id="beb4f-154">Para sincronizar o estado do filtro entre vários threads, chame o método [**CSource::P stateLock**](csource--pstatelock.md) .</span><span class="sxs-lookup"><span data-stu-id="beb4f-154">To synchronize the filter state among multiple threads, call the [**CSource::pStateLock**](csource--pstatelock.md) method.</span></span> <span data-ttu-id="beb4f-155">Esse método retorna um ponteiro para a seção crítica de estado de filtro.</span><span class="sxs-lookup"><span data-stu-id="beb4f-155">This method returns a pointer to the filter-state critical section.</span></span> <span data-ttu-id="beb4f-156">Use a classe [**CAutoLock**](cautolock.md) para manter a seção crítica.</span><span class="sxs-lookup"><span data-stu-id="beb4f-156">Use the [**CAutoLock**](cautolock.md) class to hold the critical section.</span></span> <span data-ttu-id="beb4f-157">De um PIN, você pode acessar **pStateLock** da variável de membro [**CBasePin:: m \_ pFilter**](cbasepin-m-pfilter.md) do PIN, da seguinte maneira:</span><span class="sxs-lookup"><span data-stu-id="beb4f-157">From a pin, you can access **pStateLock** from the pin's [**CBasePin::m\_pFilter**](cbasepin-m-pfilter.md) member variable, as follows:</span></span>


```
CAutoLock lock(m_pFilter->pStateLock());
```



## <a name="requirements"></a><span data-ttu-id="beb4f-158">Requisitos</span><span class="sxs-lookup"><span data-stu-id="beb4f-158">Requirements</span></span>



| <span data-ttu-id="beb4f-159">Requisito</span><span class="sxs-lookup"><span data-stu-id="beb4f-159">Requirement</span></span> | <span data-ttu-id="beb4f-160">Valor</span><span class="sxs-lookup"><span data-stu-id="beb4f-160">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="beb4f-161">parâmetro</span><span class="sxs-lookup"><span data-stu-id="beb4f-161">Header</span></span><br/>  | <dl> <span data-ttu-id="beb4f-162"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="beb4f-162"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="beb4f-163">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="beb4f-163">Library</span></span><br/> | <dl> <span data-ttu-id="beb4f-164"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="beb4f-164"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="beb4f-165">Confira também</span><span class="sxs-lookup"><span data-stu-id="beb4f-165">See also</span></span>

<dl> <dt>

[<span data-ttu-id="beb4f-166">Gravando filtros de origem</span><span class="sxs-lookup"><span data-stu-id="beb4f-166">Writing Source Filters</span></span>](writing-source-filters.md)
</dt> </dl>

 

 




