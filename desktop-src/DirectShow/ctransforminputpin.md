---
description: A classe CTransformInputPin implementa um PIN de entrada que é usado pela classe CTransformFilter.
ms.assetid: 032da1bb-448d-48ea-ab3d-f721d790637f
title: Classe CTransformInputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6cbfad0a33384249ab474d6376ffc110294bca6b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749611"
---
# <a name="ctransforminputpin-class"></a><span data-ttu-id="6d9fb-103">Classe CTransformInputPin</span><span class="sxs-lookup"><span data-stu-id="6d9fb-103">CTransformInputPin class</span></span>

![hierarquia de classe CTransformInputPin](images/tfrm01.png)

<span data-ttu-id="6d9fb-105">A `CTransformInputPin` classe implementa um PIN de entrada que é usado pela classe [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="6d9fb-105">The `CTransformInputPin` class implements an input pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="6d9fb-106">Normalmente, você não precisa derivar dessa classe.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="6d9fb-107">A maioria dos métodos nesta classe chama os métodos correspondentes na classe **CTransformFilter** , que pode ser substituída.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="6d9fb-108">Se você derivar dessa classe, deverá substituir o método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) do filtro para criar instâncias da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="6d9fb-109">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="6d9fb-109">Protected Member Variables</span></span>                                           | <span data-ttu-id="6d9fb-110">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d9fb-110">Description</span></span>                                                                            |
|----------------------------------------------------------------------|----------------------------------------------------------------------------------------|
| [<span data-ttu-id="6d9fb-111">**\_pTransformFilter m**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-111">**m\_pTransformFilter**</span></span>](ctransforminputpin-m-ptransformfilter.md) | <span data-ttu-id="6d9fb-112">Ponteiro para o filtro proprietário.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-112">Pointer to the owning filter.</span></span>                                                          |
| <span data-ttu-id="6d9fb-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="6d9fb-113">Public Methods</span></span>                                                       | <span data-ttu-id="6d9fb-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d9fb-114">Description</span></span>                                                                            |
| [<span data-ttu-id="6d9fb-115">**CTransformInputPin**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-115">**CTransformInputPin**</span></span>](ctransforminputpin-ctransforminputpin.md)  | <span data-ttu-id="6d9fb-116">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-116">Constructor method.</span></span>                                                                    |
| [<span data-ttu-id="6d9fb-117">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-117">**CheckConnect**</span></span>](ctransforminputpin-checkconnect.md)              | <span data-ttu-id="6d9fb-118">Determina se uma conexão de PIN é adequada.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-118">Determines whether a pin connection is suitable.</span></span>                                       |
| [<span data-ttu-id="6d9fb-119">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-119">**BreakConnect**</span></span>](ctransforminputpin-breakconnect.md)              | <span data-ttu-id="6d9fb-120">Libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-120">Releases the pin from a connection.</span></span>                                                    |
| [<span data-ttu-id="6d9fb-121">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-121">**CompleteConnect**</span></span>](ctransforminputpin-completeconnect.md)        | <span data-ttu-id="6d9fb-122">Conclui uma conexão com outro PIN.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-122">Completes a connection to another pin.</span></span>                                                 |
| [<span data-ttu-id="6d9fb-123">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-123">**CheckMediaType**</span></span>](ctransforminputpin-checkmediatype.md)          | <span data-ttu-id="6d9fb-124">Determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-124">Determines if the pin accepts a specific media type.</span></span>                                   |
| [<span data-ttu-id="6d9fb-125">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-125">**SetMediaType**</span></span>](ctransforminputpin-setmediatype.md)              | <span data-ttu-id="6d9fb-126">Define o tipo de mídia para a conexão.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-126">Sets the media type for the connection.</span></span>                                                |
| [<span data-ttu-id="6d9fb-127">**CheckStreaming**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-127">**CheckStreaming**</span></span>](ctransforminputpin-checkstreaming.md)          | <span data-ttu-id="6d9fb-128">Determina se o PIN pode aceitar amostras.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-128">Determines whether the pin can accept samples.</span></span> <span data-ttu-id="6d9fb-129">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-129">Virtual.</span></span>                                |
| [<span data-ttu-id="6d9fb-130">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-130">**CurrentMediaType**</span></span>](ctransforminputpin-currentmediatype.md)      | <span data-ttu-id="6d9fb-131">Recupera o tipo de mídia para a conexão do PIN atual.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-131">Retrieves the media type for the current pin connection.</span></span>                               |
| <span data-ttu-id="6d9fb-132">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="6d9fb-132">IPin Methods</span></span>                                                         | <span data-ttu-id="6d9fb-133">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d9fb-133">Description</span></span>                                                                            |
| [<span data-ttu-id="6d9fb-134">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-134">**QueryId**</span></span>](ctransforminputpin-queryid.md)                        | <span data-ttu-id="6d9fb-135">Recupera um identificador para o PIN.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-135">Retrieves an identifier for the pin.</span></span>                                                   |
| [<span data-ttu-id="6d9fb-136">**EndOfStream**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-136">**EndOfStream**</span></span>](ctransforminputpin-endofstream.md)                | <span data-ttu-id="6d9fb-137">Notifica o PIN de que nenhum dado adicional é esperado.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-137">Notifies the pin that no additional data is expected.</span></span>                                  |
| [<span data-ttu-id="6d9fb-138">**BeginFlush**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-138">**BeginFlush**</span></span>](ctransforminputpin-beginflush.md)                  | <span data-ttu-id="6d9fb-139">Inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-139">Begins a flush operation.</span></span>                                                              |
| [<span data-ttu-id="6d9fb-140">**EndFlush**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-140">**EndFlush**</span></span>](ctransforminputpin-endflush.md)                      | <span data-ttu-id="6d9fb-141">Finaliza uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-141">Ends a flush operation.</span></span>                                                                |
| [<span data-ttu-id="6d9fb-142">**NewSegment**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-142">**NewSegment**</span></span>](ctransforminputpin-newsegment.md)                  | <span data-ttu-id="6d9fb-143">Notifica o PIN que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-143">Notifies the pin that media samples received after this call are grouped as a segment.</span></span> |
| <span data-ttu-id="6d9fb-144">Métodos IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="6d9fb-144">IMemInputPin Methods</span></span>                                                 | <span data-ttu-id="6d9fb-145">Descrição</span><span class="sxs-lookup"><span data-stu-id="6d9fb-145">Description</span></span>                                                                            |
| [<span data-ttu-id="6d9fb-146">**Recebe**</span><span class="sxs-lookup"><span data-stu-id="6d9fb-146">**Receive**</span></span>](ctransforminputpin-receive.md)                        | <span data-ttu-id="6d9fb-147">Recebe o próximo exemplo de mídia no fluxo.</span><span class="sxs-lookup"><span data-stu-id="6d9fb-147">Receives the next media sample in the stream.</span></span>                                          |



 

## <a name="requirements"></a><span data-ttu-id="6d9fb-148">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6d9fb-148">Requirements</span></span>



| <span data-ttu-id="6d9fb-149">Requisito</span><span class="sxs-lookup"><span data-stu-id="6d9fb-149">Requirement</span></span> | <span data-ttu-id="6d9fb-150">Valor</span><span class="sxs-lookup"><span data-stu-id="6d9fb-150">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6d9fb-151">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6d9fb-151">Header</span></span><br/>  | <dl> <span data-ttu-id="6d9fb-152"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6d9fb-152"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6d9fb-153">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6d9fb-153">Library</span></span><br/> | <dl> <span data-ttu-id="6d9fb-154"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6d9fb-154"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




