---
description: A classe CBaseInputPin é uma classe base abstrata para implementar Pins de entrada. Essa classe adiciona suporte para a interface IMemInputPin, além do suporte de interface IPin fornecido pelo CBasePin.
ms.assetid: 5a2b7f09-8c8b-45da-a4b7-afeb8d5548c1
title: Classe CBaseInputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba55006438a8484b0bf10b95ac8b9d8bbdb56e0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756828"
---
# <a name="cbaseinputpin-class"></a><span data-ttu-id="61e9c-104">Classe CBaseInputPin</span><span class="sxs-lookup"><span data-stu-id="61e9c-104">CBaseInputPin class</span></span>

![hierarquia de classe CBaseInputPin](images/filter07.png)

<span data-ttu-id="61e9c-106">A `CBaseInputPin` classe é uma classe base abstrata para implementar Pins de entrada.</span><span class="sxs-lookup"><span data-stu-id="61e9c-106">The `CBaseInputPin` class is an abstract base class for implementing input pins.</span></span> <span data-ttu-id="61e9c-107">Essa classe adiciona suporte para a interface [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) , além do suporte de interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) fornecido pelo [**CBasePin**](cbasepin.md).</span><span class="sxs-lookup"><span data-stu-id="61e9c-107">This class adds support for the [**IMemInputPin**](/windows/desktop/api/Strmif/nn-strmif-imeminputpin) interface, in addition to the [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface support provided by [**CBasePin**](cbasepin.md).</span></span>

<span data-ttu-id="61e9c-108">Para usar essa classe, derive uma nova classe e substitua pelo menos os seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="61e9c-108">To use this class, derive a new class and override at least the following methods:</span></span>

-   [<span data-ttu-id="61e9c-109">**CBaseInputPin::BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="61e9c-109">**CBaseInputPin::BeginFlush**</span></span>](cbaseinputpin-beginflush.md)
-   [<span data-ttu-id="61e9c-110">**CBaseInputPin:: EndFlush**</span><span class="sxs-lookup"><span data-stu-id="61e9c-110">**CBaseInputPin::EndFlush**</span></span>](cbaseinputpin-endflush.md)
-   [<span data-ttu-id="61e9c-111">**CBaseInputPin:: receber**</span><span class="sxs-lookup"><span data-stu-id="61e9c-111">**CBaseInputPin::Receive**</span></span>](cbaseinputpin-receive.md)
-   [<span data-ttu-id="61e9c-112">**CBasePin::CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="61e9c-112">**CBasePin::CheckMediaType**</span></span>](cbasepin-checkmediatype.md)
-   [<span data-ttu-id="61e9c-113">**CBasePin:: GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="61e9c-113">**CBasePin::GetMediaType**</span></span>](cbasepin-getmediatype.md)

<span data-ttu-id="61e9c-114">Dependendo da função do PIN, talvez seja necessário substituir métodos adicionais no `CBaseInputPin` ou **CBasePin**.</span><span class="sxs-lookup"><span data-stu-id="61e9c-114">Depending on the function of the pin, you might need to override additional methods in `CBaseInputPin` or **CBasePin**.</span></span>



| <span data-ttu-id="61e9c-115">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="61e9c-115">Protected Member Variables</span></span>                                                 | <span data-ttu-id="61e9c-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="61e9c-116">Description</span></span>                                                                                                 |
|----------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="61e9c-117">**\_pAllocator m**</span><span class="sxs-lookup"><span data-stu-id="61e9c-117">**m\_pAllocator**</span></span>](cbaseinputpin-m-pallocator.md)                        | <span data-ttu-id="61e9c-118">Ponteiro para o alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="61e9c-118">Pointer to the memory allocator.</span></span>                                                                            |
| [<span data-ttu-id="61e9c-119">**\_bReadOnly m**</span><span class="sxs-lookup"><span data-stu-id="61e9c-119">**m\_bReadOnly**</span></span>](cbaseinputpin-m-breadonly.md)                          | <span data-ttu-id="61e9c-120">Sinalizador que indica se o alocador produz amostras de mídia somente leitura.</span><span class="sxs-lookup"><span data-stu-id="61e9c-120">Flag that indicates whether the allocator produces read-only media samples.</span></span>                                 |
| [<span data-ttu-id="61e9c-121">**\_bFlushing m**</span><span class="sxs-lookup"><span data-stu-id="61e9c-121">**m\_bFlushing**</span></span>](cbaseinputpin-m-bflushing.md)                          | <span data-ttu-id="61e9c-122">Sinalizador que indica se o PIN está sendo liberado no momento.</span><span class="sxs-lookup"><span data-stu-id="61e9c-122">Flag that indicates whether the pin is currently flushing.</span></span>                                                  |
| [<span data-ttu-id="61e9c-123">**\_SampleProps m**</span><span class="sxs-lookup"><span data-stu-id="61e9c-123">**m\_SampleProps**</span></span>](cbaseinputpin-m-sampleprops.md)                      | <span data-ttu-id="61e9c-124">Propriedades da amostra mais recente.</span><span class="sxs-lookup"><span data-stu-id="61e9c-124">Properties of the most recent sample.</span></span>                                                                       |
| <span data-ttu-id="61e9c-125">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="61e9c-125">Public Methods</span></span>                                                             | <span data-ttu-id="61e9c-126">Descrição</span><span class="sxs-lookup"><span data-stu-id="61e9c-126">Description</span></span>                                                                                                 |
| [<span data-ttu-id="61e9c-127">**CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="61e9c-127">**CBaseInputPin**</span></span>](cbaseinputpin-cbaseinputpin.md)                       | <span data-ttu-id="61e9c-128">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="61e9c-128">Constructor method.</span></span>                                                                                         |
| [<span data-ttu-id="61e9c-129">**~ CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="61e9c-129">**~CBaseInputPin**</span></span>](cbaseinputpin--cbaseinputpin.md)                     | <span data-ttu-id="61e9c-130">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="61e9c-130">Destructor method.</span></span>                                                                                          |
| [<span data-ttu-id="61e9c-131">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="61e9c-131">**BreakConnect**</span></span>](cbaseinputpin-breakconnect.md)                         | <span data-ttu-id="61e9c-132">Libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="61e9c-132">Releases the pin from a connection.</span></span>                                                                         |
| [<span data-ttu-id="61e9c-133">**IsReadOnly**</span><span class="sxs-lookup"><span data-stu-id="61e9c-133">**IsReadOnly**</span></span>](cbaseinputpin-isreadonly.md)                             | <span data-ttu-id="61e9c-134">Consulta se o alocador usa amostras de mídia somente leitura.</span><span class="sxs-lookup"><span data-stu-id="61e9c-134">Queries whether the allocator uses read-only media samples.</span></span>                                                 |
| [<span data-ttu-id="61e9c-135">**Islibere**</span><span class="sxs-lookup"><span data-stu-id="61e9c-135">**IsFlushing**</span></span>](cbaseinputpin-isflushing.md)                             | <span data-ttu-id="61e9c-136">Consulta se o filtro está sendo liberado no momento.</span><span class="sxs-lookup"><span data-stu-id="61e9c-136">Queries whether the filter is currently flushing.</span></span>                                                           |
| [<span data-ttu-id="61e9c-137">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="61e9c-137">**CheckStreaming**</span></span>](cbaseinputpin-checkstreaming.md)                     | <span data-ttu-id="61e9c-138">Determina se o PIN pode aceitar amostras.</span><span class="sxs-lookup"><span data-stu-id="61e9c-138">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="61e9c-139">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="61e9c-139">Virtual.</span></span>                                                     |
| [<span data-ttu-id="61e9c-140">**PassNotify**</span><span class="sxs-lookup"><span data-stu-id="61e9c-140">**PassNotify**</span></span>](cbaseinputpin-passnotify.md)                             | <span data-ttu-id="61e9c-141">Passa uma mensagem de controle de qualidade para o objeto apropriado.</span><span class="sxs-lookup"><span data-stu-id="61e9c-141">Passes a quality-control message to the appropriate object.</span></span>                                                 |
| [<span data-ttu-id="61e9c-142">**Inativo**</span><span class="sxs-lookup"><span data-stu-id="61e9c-142">**Inactive**</span></span>](cbaseinputpin-inactive.md)                                 | <span data-ttu-id="61e9c-143">Notifica o PIN de que o filtro não está mais ativo.</span><span class="sxs-lookup"><span data-stu-id="61e9c-143">Notifies the pin that the filter is no longer active.</span></span> <span data-ttu-id="61e9c-144">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="61e9c-144">Virtual.</span></span>                                              |
| [<span data-ttu-id="61e9c-145">**SampleProps**</span><span class="sxs-lookup"><span data-stu-id="61e9c-145">**SampleProps**</span></span>](cbaseinputpin-sampleprops.md)                           | <span data-ttu-id="61e9c-146">Recupera as propriedades do exemplo mais recente.</span><span class="sxs-lookup"><span data-stu-id="61e9c-146">Retrieves the properties of the most recent sample.</span></span>                                                         |
| <span data-ttu-id="61e9c-147">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="61e9c-147">IPin Methods</span></span>                                                               | <span data-ttu-id="61e9c-148">Descrição</span><span class="sxs-lookup"><span data-stu-id="61e9c-148">Description</span></span>                                                                                                 |
| [<span data-ttu-id="61e9c-149">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="61e9c-149">**BeginFlush**</span></span>](cbaseinputpin-beginflush.md)                             | <span data-ttu-id="61e9c-150">Inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="61e9c-150">Begins a flush operation.</span></span>                                                                                   |
| [<span data-ttu-id="61e9c-151">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="61e9c-151">**EndFlush**</span></span>](cbaseinputpin-endflush.md)                                 | <span data-ttu-id="61e9c-152">Finaliza uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="61e9c-152">Ends a flush operation.</span></span>                                                                                     |
| <span data-ttu-id="61e9c-153">Métodos IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="61e9c-153">IMemInputPin Methods</span></span>                                                       | <span data-ttu-id="61e9c-154">Descrição</span><span class="sxs-lookup"><span data-stu-id="61e9c-154">Description</span></span>                                                                                                 |
| [<span data-ttu-id="61e9c-155">**Getalocador**</span><span class="sxs-lookup"><span data-stu-id="61e9c-155">**GetAllocator**</span></span>](cbaseinputpin-getallocator.md)                         | <span data-ttu-id="61e9c-156">Recupera o alocador de memória proposto por este pin.</span><span class="sxs-lookup"><span data-stu-id="61e9c-156">Retrieves the memory allocator proposed by this pin.</span></span>                                                        |
| [<span data-ttu-id="61e9c-157">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="61e9c-157">**NotifyAllocator**</span></span>](cbaseinputpin-notifyallocator.md)                   | <span data-ttu-id="61e9c-158">Especifica um alocador para a conexão.</span><span class="sxs-lookup"><span data-stu-id="61e9c-158">Specifies an allocator for the connection.</span></span>                                                                  |
| [<span data-ttu-id="61e9c-159">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="61e9c-159">**GetAllocatorRequirements**</span></span>](cbaseinputpin-getallocatorrequirements.md) | <span data-ttu-id="61e9c-160">Recupera as propriedades de alocador solicitadas pelo pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="61e9c-160">Retrieves the allocator properties requested by the input pin.</span></span>                                              |
| [<span data-ttu-id="61e9c-161">**Recebe**</span><span class="sxs-lookup"><span data-stu-id="61e9c-161">**Receive**</span></span>](cbaseinputpin-receive.md)                                   | <span data-ttu-id="61e9c-162">Recebe o próximo exemplo de mídia no fluxo.</span><span class="sxs-lookup"><span data-stu-id="61e9c-162">Receives the next media sample in the stream.</span></span>                                                               |
| [<span data-ttu-id="61e9c-163">**ReceiveMultiple**</span><span class="sxs-lookup"><span data-stu-id="61e9c-163">**ReceiveMultiple**</span></span>](cbaseinputpin-receivemultiple.md)                   | <span data-ttu-id="61e9c-164">Recebe vários exemplos no fluxo.</span><span class="sxs-lookup"><span data-stu-id="61e9c-164">Receives multiple samples in the stream.</span></span>                                                                    |
| [<span data-ttu-id="61e9c-165">**ReceiveCanBlock**</span><span class="sxs-lookup"><span data-stu-id="61e9c-165">**ReceiveCanBlock**</span></span>](cbaseinputpin-receivecanblock.md)                   | <span data-ttu-id="61e9c-166">Determina se as chamadas para o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) podem ser bloqueadas.</span><span class="sxs-lookup"><span data-stu-id="61e9c-166">Determines whether calls to the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method might block.</span></span> |
| <span data-ttu-id="61e9c-167">Métodos IQualityControl</span><span class="sxs-lookup"><span data-stu-id="61e9c-167">IQualityControl Methods</span></span>                                                    | <span data-ttu-id="61e9c-168">Descrição</span><span class="sxs-lookup"><span data-stu-id="61e9c-168">Description</span></span>                                                                                                 |
| [<span data-ttu-id="61e9c-169">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="61e9c-169">**Notify**</span></span>](cbaseinputpin-notify.md)                                     | <span data-ttu-id="61e9c-170">Recebe uma mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="61e9c-170">Receives a quality-control message.</span></span>                                                                         |



 

## <a name="requirements"></a><span data-ttu-id="61e9c-171">Requisitos</span><span class="sxs-lookup"><span data-stu-id="61e9c-171">Requirements</span></span>



| <span data-ttu-id="61e9c-172">Requisito</span><span class="sxs-lookup"><span data-stu-id="61e9c-172">Requirement</span></span> | <span data-ttu-id="61e9c-173">Valor</span><span class="sxs-lookup"><span data-stu-id="61e9c-173">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="61e9c-174">parâmetro</span><span class="sxs-lookup"><span data-stu-id="61e9c-174">Header</span></span><br/>  | <dl> <span data-ttu-id="61e9c-175"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="61e9c-175"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="61e9c-176">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="61e9c-176">Library</span></span><br/> | <dl> <span data-ttu-id="61e9c-177"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="61e9c-177"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




