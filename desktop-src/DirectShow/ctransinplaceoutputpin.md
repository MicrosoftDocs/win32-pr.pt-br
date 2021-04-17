---
description: A classe CTransInPlaceOutputPin implementa um pino de saída que é usado pela classe CTransInPlaceFilter.
ms.assetid: 90d54807-85c1-43b9-8998-e1bcf7b54725
title: Classe CTransInPlaceOutputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e41fbff07a9bdeb8990bbf3ddba6d9f7455d1bad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105775565"
---
# <a name="ctransinplaceoutputpin-class"></a><span data-ttu-id="bf4ae-103">Classe CTransInPlaceOutputPin</span><span class="sxs-lookup"><span data-stu-id="bf4ae-103">CTransInPlaceOutputPin class</span></span>

![hierarquia de classe CTransInPlaceOutputPin](images/tsip02.png)

<span data-ttu-id="bf4ae-105">A `CTransInPlaceOutputPin` classe implementa um pino de saída que é usado pela classe [**CTransInPlaceFilter**](ctransinplacefilter.md) .</span><span class="sxs-lookup"><span data-stu-id="bf4ae-105">The `CTransInPlaceOutputPin` class implements an output pin that is used by the [**CTransInPlaceFilter**](ctransinplacefilter.md) class.</span></span>

<span data-ttu-id="bf4ae-106">Normalmente, você não precisa derivar dessa classe.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-106">Typically, you do not need to derive from this class.</span></span> <span data-ttu-id="bf4ae-107">Se você fizer isso, deverá substituir o método [**CTransInPlaceFilter:: GetPin**](ctransinplacefilter-getpin.md) do filtro para criar instâncias da classe derivada.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-107">If you do, you must override the filter's [**CTransInPlaceFilter::GetPin**](ctransinplacefilter-getpin.md) method to create instances of your derived class.</span></span>



| <span data-ttu-id="bf4ae-108">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="bf4ae-108">Protected Member Variables</span></span>                                                      | <span data-ttu-id="bf4ae-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf4ae-109">Description</span></span>                                          |
|---------------------------------------------------------------------------------|------------------------------------------------------|
| [<span data-ttu-id="bf4ae-110">**\_pTIPFilter m**</span><span class="sxs-lookup"><span data-stu-id="bf4ae-110">**m\_pTIPFilter**</span></span>](ctransinplaceoutputpin-m-ptipfilter.md)                    | <span data-ttu-id="bf4ae-111">Ponteiro para o filtro que criou este pin.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-111">Pointer to the filter that created this pin.</span></span>         |
| <span data-ttu-id="bf4ae-112">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="bf4ae-112">Public Methods</span></span>                                                                  | <span data-ttu-id="bf4ae-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf4ae-113">Description</span></span>                                          |
| [<span data-ttu-id="bf4ae-114">**CTransInPlaceOutputPin**</span><span class="sxs-lookup"><span data-stu-id="bf4ae-114">**CTransInPlaceOutputPin**</span></span>](ctransinplaceoutputpin-ctransinplaceoutputpin.md) | <span data-ttu-id="bf4ae-115">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-115">Constructor method.</span></span>                                  |
| [<span data-ttu-id="bf4ae-116">**CheckMediaType**</span><span class="sxs-lookup"><span data-stu-id="bf4ae-116">**CheckMediaType**</span></span>](ctransinplaceoutputpin-checkmediatype.md)                 | <span data-ttu-id="bf4ae-117">Determina se o PIN aceita um tipo de mídia específico.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-117">Determines if the pin accepts a specific media type.</span></span> |
| [<span data-ttu-id="bf4ae-118">**Setalocador**</span><span class="sxs-lookup"><span data-stu-id="bf4ae-118">**SetAllocator**</span></span>](ctransinplaceoutputpin-setallocator.md)                     | <span data-ttu-id="bf4ae-119">Especifica um alocador para a conexão.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-119">Specifies an allocator for the connection.</span></span>           |
| [<span data-ttu-id="bf4ae-120">**ConnectedIMemInputPin**</span><span class="sxs-lookup"><span data-stu-id="bf4ae-120">**ConnectedIMemInputPin**</span></span>](ctransinplaceoutputpin-connectedimeminputpin.md)   | <span data-ttu-id="bf4ae-121">Recupera um ponteiro para o pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-121">Retrieves a pointer to the downstream input pin.</span></span>     |
| [<span data-ttu-id="bf4ae-122">**PeekAllocator**</span><span class="sxs-lookup"><span data-stu-id="bf4ae-122">**PeekAllocator**</span></span>](ctransinplaceoutputpin-peekallocator.md)                   | <span data-ttu-id="bf4ae-123">Recupera um ponteiro para o alocador do PIN.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-123">Retrieves a pointer to the pin's allocator.</span></span>          |
| <span data-ttu-id="bf4ae-124">Métodos IPin</span><span class="sxs-lookup"><span data-stu-id="bf4ae-124">IPin Methods</span></span>                                                                    | <span data-ttu-id="bf4ae-125">Descrição</span><span class="sxs-lookup"><span data-stu-id="bf4ae-125">Description</span></span>                                          |
| [<span data-ttu-id="bf4ae-126">**EnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="bf4ae-126">**EnumMediaTypes**</span></span>](ctransinplaceoutputpin-enummediatypes.md)                 | <span data-ttu-id="bf4ae-127">Enumera os tipos de mídia preferenciais do PIN.</span><span class="sxs-lookup"><span data-stu-id="bf4ae-127">Enumerates the pin's preferred media types.</span></span>          |



 

## <a name="requirements"></a><span data-ttu-id="bf4ae-128">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf4ae-128">Requirements</span></span>



| <span data-ttu-id="bf4ae-129">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf4ae-129">Requirement</span></span> | <span data-ttu-id="bf4ae-130">Valor</span><span class="sxs-lookup"><span data-stu-id="bf4ae-130">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf4ae-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf4ae-131">Header</span></span><br/>  | <dl> <span data-ttu-id="bf4ae-132"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf4ae-132"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bf4ae-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf4ae-133">Library</span></span><br/> | <dl> <span data-ttu-id="bf4ae-134"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bf4ae-134"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




