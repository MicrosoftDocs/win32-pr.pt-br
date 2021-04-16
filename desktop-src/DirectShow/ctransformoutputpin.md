---
description: A classe CTransformOutputPin implementa um pino de saída que é usado pela classe CTransformFilter.
ms.assetid: 76f9a981-8f0d-45d4-b901-c5ec5b5ac9ee
title: Classe CTransformOutputPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c55c57fbec0a8441b80398370542d94b2b70c1ce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758650"
---
# <a name="ctransformoutputpin-class"></a><span data-ttu-id="51131-103">Classe CTransformOutputPin</span><span class="sxs-lookup"><span data-stu-id="51131-103">CTransformOutputPin class</span></span>

![hierarquia de classe CTransformOutputPin](images/tfrm02.png)

<span data-ttu-id="51131-105">A `CTransformOutputPin` classe implementa um pino de saída que é usado pela classe [**CTransformFilter**](ctransformfilter.md) .</span><span class="sxs-lookup"><span data-stu-id="51131-105">The `CTransformOutputPin` class implements an output pin that is used by the [**CTransformFilter**](ctransformfilter.md) class.</span></span>

<span data-ttu-id="51131-106">Normalmente, você não precisa derivar dessa classe.</span><span class="sxs-lookup"><span data-stu-id="51131-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="51131-107">A maioria dos métodos nesta classe chama os métodos correspondentes na classe **CTransformFilter** , que pode ser substituída.</span><span class="sxs-lookup"><span data-stu-id="51131-107">Most of the methods in this class call corresponding methods on the **CTransformFilter** class, which you can override.</span></span> <span data-ttu-id="51131-108">Se você derivar dessa classe, deverá substituir o método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) do filtro para criar instâncias da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="51131-108">If you derive from this class, you must override the filter's [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method to create instances of your derived class.</span></span>

<span data-ttu-id="51131-109">Essa classe expõe as interfaces **IMediaSeeking** e **IMediaPosition** por meio do objeto [**CPosPassThru**](cpospassthru.md) .</span><span class="sxs-lookup"><span data-stu-id="51131-109">This class exposes the **IMediaSeeking** and **IMediaPosition** interfaces through the [**CPosPassThru**](cpospassthru.md) object.</span></span> <span data-ttu-id="51131-110">Ele passa todas as solicitações de busca para o próximo filtro upstream.</span><span class="sxs-lookup"><span data-stu-id="51131-110">It passes all seek requests to the next filter upstream.</span></span>



| <span data-ttu-id="51131-111">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="51131-111">Protected Member Variables</span></span>                                               | <span data-ttu-id="51131-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="51131-112">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="51131-113">**\_pTransformFilter m**</span><span class="sxs-lookup"><span data-stu-id="51131-113">**m\_pTransformFilter**</span></span>](ctransformoutputpin-m-ptransformfilter.md)    | <span data-ttu-id="51131-114">Ponteiro para o filtro proprietário.</span><span class="sxs-lookup"><span data-stu-id="51131-114">Pointer to the owning filter.</span></span>                            |
| <span data-ttu-id="51131-115">Variáveis de membro público</span><span class="sxs-lookup"><span data-stu-id="51131-115">Public Member Variables</span></span>                                                  | <span data-ttu-id="51131-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="51131-116">Description</span></span>                                              |
| [<span data-ttu-id="51131-117">**\_pPosition m**</span><span class="sxs-lookup"><span data-stu-id="51131-117">**m\_pPosition**</span></span>](ctransformoutputpin-m-pposition.md)                  | <span data-ttu-id="51131-118">Objeto auxiliar para passar comandos de busca upstream.</span><span class="sxs-lookup"><span data-stu-id="51131-118">Helper object to pass seek commands upstream.</span></span>            |
| <span data-ttu-id="51131-119">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="51131-119">Public Methods</span></span>                                                           | <span data-ttu-id="51131-120">Descrição</span><span class="sxs-lookup"><span data-stu-id="51131-120">Description</span></span>                                              |
| [<span data-ttu-id="51131-121">**CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="51131-121">**CTransformOutputPin**</span></span>](ctransformoutputpin-ctransformoutputpin.md)   | <span data-ttu-id="51131-122">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="51131-122">Constructor method.</span></span>                                      |
| [<span data-ttu-id="51131-123">**~ CTransformOutputPin**</span><span class="sxs-lookup"><span data-stu-id="51131-123">**~CTransformOutputPin**</span></span>](ctransformoutputpin--ctransformoutputpin.md) | <span data-ttu-id="51131-124">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="51131-124">Destructor method.</span></span>                                       |
| [<span data-ttu-id="51131-125">**CheckConnect**</span><span class="sxs-lookup"><span data-stu-id="51131-125">**CheckConnect**</span></span>](ctransformoutputpin-checkconnect.md)                 | <span data-ttu-id="51131-126">Determina se uma conexão de PIN é adequada.</span><span class="sxs-lookup"><span data-stu-id="51131-126">Determines whether a pin connection is suitable.</span></span>         |
| [<span data-ttu-id="51131-127">**BreakConnect**</span><span class="sxs-lookup"><span data-stu-id="51131-127">**BreakConnect**</span></span>](ctransformoutputpin-breakconnect.md)                 | <span data-ttu-id="51131-128">Libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="51131-128">Releases the pin from a connection.</span></span>                      |
| [<span data-ttu-id="51131-129">**CompleteConnect**</span><span class="sxs-lookup"><span data-stu-id="51131-129">**CompleteConnect**</span></span>](ctransformoutputpin-completeconnect.md)           | <span data-ttu-id="51131-130">Conclui uma conexão com outro PIN.</span><span class="sxs-lookup"><span data-stu-id="51131-130">Completes a connection to another pin.</span></span>                   |
| [<span data-ttu-id="51131-131">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="51131-131">**CheckMediaType**</span></span>](ctransformoutputpin-checkmediatype.md)             | <span data-ttu-id="51131-132">Determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="51131-132">Determines if the pin accepts a specific media type.</span></span>     |
| [<span data-ttu-id="51131-133">**SetMediaType**</span><span class="sxs-lookup"><span data-stu-id="51131-133">**SetMediaType**</span></span>](ctransformoutputpin-setmediatype.md)                 | <span data-ttu-id="51131-134">Define o tipo de mídia para a conexão.</span><span class="sxs-lookup"><span data-stu-id="51131-134">Sets the media type for the connection.</span></span>                  |
| [<span data-ttu-id="51131-135">**DecideBufferSize**</span><span class="sxs-lookup"><span data-stu-id="51131-135">**DecideBufferSize**</span></span>](ctransformoutputpin-decidebuffersize.md)         | <span data-ttu-id="51131-136">Define os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="51131-136">Sets the buffer requirements.</span></span>                            |
| [<span data-ttu-id="51131-137">**GetMediaType**</span><span class="sxs-lookup"><span data-stu-id="51131-137">**GetMediaType**</span></span>](ctransformoutputpin-getmediatype.md)                 | <span data-ttu-id="51131-138">Recupera um tipo de mídia preferencial, por valor de índice.</span><span class="sxs-lookup"><span data-stu-id="51131-138">Retrieves a preferred media type, by index value.</span></span>        |
| [<span data-ttu-id="51131-139">**CurrentMediaType**</span><span class="sxs-lookup"><span data-stu-id="51131-139">**CurrentMediaType**</span></span>](ctransformoutputpin-currentmediatype.md)         | <span data-ttu-id="51131-140">Recupera o tipo de mídia para a conexão do PIN atual.</span><span class="sxs-lookup"><span data-stu-id="51131-140">Retrieves the media type for the current pin connection.</span></span> |
| <span data-ttu-id="51131-141">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="51131-141">IPin Methods</span></span>                                                             | <span data-ttu-id="51131-142">Descrição</span><span class="sxs-lookup"><span data-stu-id="51131-142">Description</span></span>                                              |
| [<span data-ttu-id="51131-143">**QueryId**</span><span class="sxs-lookup"><span data-stu-id="51131-143">**QueryId**</span></span>](ctransformoutputpin-queryid.md)                           | <span data-ttu-id="51131-144">Recupera um identificador para o PIN.</span><span class="sxs-lookup"><span data-stu-id="51131-144">Retrieves an identifier for the pin.</span></span>                     |
| <span data-ttu-id="51131-145">Métodos IQualityControl</span><span class="sxs-lookup"><span data-stu-id="51131-145">IQualityControl Methods</span></span>                                                  | <span data-ttu-id="51131-146">Descrição</span><span class="sxs-lookup"><span data-stu-id="51131-146">Description</span></span>                                              |
| [<span data-ttu-id="51131-147">**Notificar**</span><span class="sxs-lookup"><span data-stu-id="51131-147">**Notify**</span></span>](ctransformoutputpin-notify.md)                             | <span data-ttu-id="51131-148">Notifica o PIN de que uma alteração de qualidade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="51131-148">Notifies the pin that a quality change is requested.</span></span>     |



 

## <a name="requirements"></a><span data-ttu-id="51131-149">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51131-149">Requirements</span></span>



| <span data-ttu-id="51131-150">Requisito</span><span class="sxs-lookup"><span data-stu-id="51131-150">Requirement</span></span> | <span data-ttu-id="51131-151">Valor</span><span class="sxs-lookup"><span data-stu-id="51131-151">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51131-152">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51131-152">Header</span></span><br/>  | <dl> <span data-ttu-id="51131-153"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51131-153"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51131-154">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51131-154">Library</span></span><br/> | <dl> <span data-ttu-id="51131-155"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="51131-155"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




