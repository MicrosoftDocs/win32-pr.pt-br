---
description: A classe CTransInPlaceInputPin implementa um PIN de entrada que é usado pela classe CTransInPlaceFilter.
ms.assetid: 8cd2f17d-64b4-4ee6-b31a-e841ada03ce6
title: Classe CTransInPlaceInputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 242e3c09a3fb569036a22b515d4da9c49b6178da
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778440"
---
# <a name="ctransinplaceinputpin-class"></a><span data-ttu-id="77684-103">Classe CTransInPlaceInputPin</span><span class="sxs-lookup"><span data-stu-id="77684-103">CTransInPlaceInputPin class</span></span>

![hierarquia de classe CTransInPlaceInputPin](images/tsip01.png)

<span data-ttu-id="77684-105">A `CTransInPlaceInputPin` classe implementa um PIN de entrada que é usado pela classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="77684-105">The `CTransInPlaceInputPin` class implements an input pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="77684-106">Normalmente, você não precisa derivar dessa classe.</span><span class="sxs-lookup"><span data-stu-id="77684-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="77684-107">Se você fizer isso, deverá substituir o método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) do filtro para criar instâncias da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="77684-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="77684-108">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="77684-108">Protected Member Variables</span></span>                                                          | <span data-ttu-id="77684-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="77684-109">Description</span></span>                                                |
|-------------------------------------------------------------------------------------|------------------------------------------------------------|
| [<span data-ttu-id="77684-110">**\_bReadOnly m**</span><span class="sxs-lookup"><span data-stu-id="77684-110">**m\_bReadOnly**</span></span>](ctransinplaceinputpin-m-breadonly.md)                           | <span data-ttu-id="77684-111">Sinalizador que especifica se o fluxo de entrada é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="77684-111">Flag that specifies whether the input stream is read-only.</span></span> |
| [<span data-ttu-id="77684-112">**\_pTIPFilter m**</span><span class="sxs-lookup"><span data-stu-id="77684-112">**m\_pTIPFilter**</span></span>](ctransinplaceinputpin-m-ptipfilter.md)                         | <span data-ttu-id="77684-113">Ponteiro para o filtro que criou este pin.</span><span class="sxs-lookup"><span data-stu-id="77684-113">Pointer to the filter that created this pin.</span></span>               |
| <span data-ttu-id="77684-114">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="77684-114">Public Methods</span></span>                                                                      | <span data-ttu-id="77684-115">Descrição</span><span class="sxs-lookup"><span data-stu-id="77684-115">Description</span></span>                                                |
| [<span data-ttu-id="77684-116">**CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="77684-116">**CTransInPlaceInputPin**</span></span>](ctransinplaceinputpin-ctransinplaceinputpin.md)        | <span data-ttu-id="77684-117">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="77684-117">Constructor method.</span></span>                                        |
| [<span data-ttu-id="77684-118">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="77684-118">**CheckMediaType**</span></span>](ctransinplaceinputpin-checkmediatype.md)                      | <span data-ttu-id="77684-119">Determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="77684-119">Determines if the pin accepts a specific media type.</span></span>       |
| [<span data-ttu-id="77684-120">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="77684-120">**PeekAllocator**</span></span>](ctransinplaceinputpin-peekallocator.md)                        | <span data-ttu-id="77684-121">Recupera um ponteiro para o alocador do PIN.</span><span class="sxs-lookup"><span data-stu-id="77684-121">Retrieves a pointer to the pin's allocator.</span></span>                |
| [<span data-ttu-id="77684-122">**ReadOnly**</span><span class="sxs-lookup"><span data-stu-id="77684-122">**ReadOnly**</span></span>](ctransinplaceinputpin-readonly.md)                                  | <span data-ttu-id="77684-123">Indica se o fluxo de entrada é somente leitura.</span><span class="sxs-lookup"><span data-stu-id="77684-123">Indicates whether the input stream is read-only.</span></span>           |
| <span data-ttu-id="77684-124">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="77684-124">IPin Methods</span></span>                                                                        | <span data-ttu-id="77684-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="77684-125">Description</span></span>                                                |
| [<span data-ttu-id="77684-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="77684-126">**EnumMediaTypes**</span></span>](ctransinplaceinputpin-enummediatypes.md)                      | <span data-ttu-id="77684-127">Enumera os tipos de mídia preferenciais do PIN.</span><span class="sxs-lookup"><span data-stu-id="77684-127">Enumerates the pin's preferred media types.</span></span>                |
| <span data-ttu-id="77684-128">Métodos IMemInputPin</span><span class="sxs-lookup"><span data-stu-id="77684-128">IMemInputPin Methods</span></span>                                                                | <span data-ttu-id="77684-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="77684-129">Description</span></span>                                                |
| [<span data-ttu-id="77684-130">**Getalocador**</span><span class="sxs-lookup"><span data-stu-id="77684-130">**GetAllocator**</span></span>](ctransinplaceinputpin-getallocator.md)                          | <span data-ttu-id="77684-131">Recupera o alocador de memória proposto por este pin.</span><span class="sxs-lookup"><span data-stu-id="77684-131">Retrieves the memory allocator proposed by this pin.</span></span>       |
| [<span data-ttu-id="77684-132">**NotifyAllocator**</span><span class="sxs-lookup"><span data-stu-id="77684-132">**NotifyAllocator**</span></span>](ctransinplaceinputpin-notifyallocator.md)                    | <span data-ttu-id="77684-133">Especifica um alocador para a conexão.</span><span class="sxs-lookup"><span data-stu-id="77684-133">Specifies an allocator for the connection.</span></span>                 |
| [<span data-ttu-id="77684-134">**GetAllocatorRequirements**</span><span class="sxs-lookup"><span data-stu-id="77684-134">**GetAllocatorRequirements**</span></span>](ctransinplaceinputpin--getallocatorrequirements.md) | <span data-ttu-id="77684-135">Recupera as propriedades de alocador solicitadas pelo PIN.</span><span class="sxs-lookup"><span data-stu-id="77684-135">Retrieves the allocator properties requested by the pin.</span></span>   |



 

## <a name="requirements"></a><span data-ttu-id="77684-136">Requisitos</span><span class="sxs-lookup"><span data-stu-id="77684-136">Requirements</span></span>



| <span data-ttu-id="77684-137">Requisito</span><span class="sxs-lookup"><span data-stu-id="77684-137">Requirement</span></span> | <span data-ttu-id="77684-138">Valor</span><span class="sxs-lookup"><span data-stu-id="77684-138">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="77684-139">parâmetro</span><span class="sxs-lookup"><span data-stu-id="77684-139">Header</span></span><br/>  | <dl> <span data-ttu-id="77684-140"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="77684-140"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="77684-141">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="77684-141">Library</span></span><br/> | <dl> <span data-ttu-id="77684-142"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="77684-142"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




