---
description: A classe CEnumPins implementa um enumerador para Pins.
ms.assetid: 8729f294-c76d-404f-9f51-7565470eced8
title: Classe CEnumPins (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumPins
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dde02c31ed0ef72e6df36a6cf0364b7f184304e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751245"
---
# <a name="cenumpins-class"></a><span data-ttu-id="75206-103">Classe CEnumPins</span><span class="sxs-lookup"><span data-stu-id="75206-103">CEnumPins class</span></span>

![hierarquia de classe CEnumPins](images/filter03.png)

<span data-ttu-id="75206-105">A `CEnumPins` classe implementa um enumerador para Pins.</span><span class="sxs-lookup"><span data-stu-id="75206-105">The `CEnumPins` class implements an enumerator for pins.</span></span>

<span data-ttu-id="75206-106">Essa classe implementa a interface [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) .</span><span class="sxs-lookup"><span data-stu-id="75206-106">This class implements the [**IEnumPins**](/windows/desktop/api/Strmif/nn-strmif-ienumpins) interface.</span></span> <span data-ttu-id="75206-107">Ele chama os seguintes métodos [**CBaseFilter**](cbasefilter.md) :</span><span class="sxs-lookup"><span data-stu-id="75206-107">It calls the following [**CBaseFilter**](cbasefilter.md) methods:</span></span>

-   <span data-ttu-id="75206-108">[**CBaseFilter:: GetPin**](cbasefilter-getpin.md): recupera um PIN no filtro, referenciado por um índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="75206-108">[**CBaseFilter::GetPin**](cbasefilter-getpin.md): Retrieves a pin on the filter, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="75206-109">[**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md): recupera o número total de Pins no filtro.</span><span class="sxs-lookup"><span data-stu-id="75206-109">[**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md): Retrieves the total number of pins on the filter.</span></span>
-   <span data-ttu-id="75206-110">[**CBaseFilter:: GetPinVersion**](cbasefilter-getpinversion.md): determina se os Pins foram alterados.</span><span class="sxs-lookup"><span data-stu-id="75206-110">[**CBaseFilter::GetPinVersion**](cbasefilter-getpinversion.md): Determines whether the pins have changed.</span></span>

<span data-ttu-id="75206-111">Se o filtro cria ou destrói Pins dinamicamente, ele incrementa a versão do PIN sempre que os Pins são alterados.</span><span class="sxs-lookup"><span data-stu-id="75206-111">If the filter dynamically creates or destroys pins, it increments the pin version whenever the pins change.</span></span> <span data-ttu-id="75206-112">Se o número de versão for alterado, o objeto enumerador não será mais sincronizado com o filtro.</span><span class="sxs-lookup"><span data-stu-id="75206-112">If the version number changes, the enumerator object is no longer synchronized with the filter.</span></span> <span data-ttu-id="75206-113">Depois que o enumerador estiver fora de sincronia, os métodos em `CEnumPins` retornarão VFW \_ E \_ enum \_ fora \_ de \_ sincronia.</span><span class="sxs-lookup"><span data-stu-id="75206-113">Once the enumerator is out of sync, the methods in `CEnumPins` return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="75206-114">Chame o método [**CEnumPins:: Reset**](cenumpins-reset.md) para ressincronizar o enumerador.</span><span class="sxs-lookup"><span data-stu-id="75206-114">Call the [**CEnumPins::Reset**](cenumpins-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="75206-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="75206-115">Public Methods</span></span>                             | <span data-ttu-id="75206-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="75206-116">Description</span></span>                                                     |
|--------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="75206-117">**CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="75206-117">**CEnumPins**</span></span>](cenumpins-cenumpins.md)   | <span data-ttu-id="75206-118">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="75206-118">Constructor method.</span></span>                                             |
| [<span data-ttu-id="75206-119">**~ CEnumPins**</span><span class="sxs-lookup"><span data-stu-id="75206-119">**~CEnumPins**</span></span>](cenumpins--cenumpins.md) | <span data-ttu-id="75206-120">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="75206-120">Destructor method.</span></span> <span data-ttu-id="75206-121">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="75206-121">Virtual.</span></span>                                     |
| <span data-ttu-id="75206-122">Métodos IEnumPins</span><span class="sxs-lookup"><span data-stu-id="75206-122">IEnumPins Methods</span></span>                          | <span data-ttu-id="75206-123">Descrição</span><span class="sxs-lookup"><span data-stu-id="75206-123">Description</span></span>                                                     |
| [<span data-ttu-id="75206-124">**8i**</span><span class="sxs-lookup"><span data-stu-id="75206-124">**Clone**</span></span>](cenumpins-clone.md)           | <span data-ttu-id="75206-125">Faz uma cópia do enumerador com o mesmo estado de enumeração.</span><span class="sxs-lookup"><span data-stu-id="75206-125">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="75206-126">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="75206-126">**Next**</span></span>](cenumpins-next.md)             | <span data-ttu-id="75206-127">Recupera um número especificado de Pins.</span><span class="sxs-lookup"><span data-stu-id="75206-127">Retrieves a specified number of pins.</span></span>                           |
| [<span data-ttu-id="75206-128">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="75206-128">**Reset**</span></span>](cenumpins-reset.md)           | <span data-ttu-id="75206-129">Redefine a sequência de enumeração para o início.</span><span class="sxs-lookup"><span data-stu-id="75206-129">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="75206-130">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="75206-130">**Skip**</span></span>](cenumpins-skip.md)             | <span data-ttu-id="75206-131">Ignora um número especificado de Pins.</span><span class="sxs-lookup"><span data-stu-id="75206-131">Skips over a specified number of pins.</span></span>                          |



 

## <a name="requirements"></a><span data-ttu-id="75206-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="75206-132">Requirements</span></span>



| <span data-ttu-id="75206-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="75206-133">Requirement</span></span> | <span data-ttu-id="75206-134">Valor</span><span class="sxs-lookup"><span data-stu-id="75206-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75206-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="75206-135">Header</span></span><br/>  | <dl> <span data-ttu-id="75206-136"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="75206-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="75206-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="75206-137">Library</span></span><br/> | <dl> <span data-ttu-id="75206-138"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="75206-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




