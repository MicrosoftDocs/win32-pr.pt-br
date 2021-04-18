---
description: A classe CEnumMediaTypes implementa um enumerador para tipos de mídia preferenciais.
ms.assetid: 50a90926-0bc7-4204-8000-81894bd154ac
title: Classe CEnumMediaTypes (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CEnumMediaTypes
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ad5e1de9eb2edbdb63eb6f476391ae8387c8d01e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756631"
---
# <a name="cenummediatypes-class"></a><span data-ttu-id="d36de-103">Classe CEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="d36de-103">CEnumMediaTypes class</span></span>

![hierarquia de classe CEnumMediaTypes](images/filter04.png)

<span data-ttu-id="d36de-105">A `CEnumMediaTypes` classe implementa um enumerador para tipos de mídia preferenciais.</span><span class="sxs-lookup"><span data-stu-id="d36de-105">The `CEnumMediaTypes` class implements an enumerator for preferred media types.</span></span>

<span data-ttu-id="d36de-106">Essa classe implementa a interface [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) .</span><span class="sxs-lookup"><span data-stu-id="d36de-106">This class implements the [**IEnumMediaTypes**](/windows/desktop/api/Strmif/nn-strmif-ienummediatypes) interface.</span></span> <span data-ttu-id="d36de-107">Ele chama os seguintes métodos [**CBasePin**](cbasepin.md) :</span><span class="sxs-lookup"><span data-stu-id="d36de-107">It calls the following [**CBasePin**](cbasepin.md) methods:</span></span>

-   <span data-ttu-id="d36de-108">[**CBasePin:: GetMediaType**](cbasepin-getmediatype.md): recupera um tipo de mídia, referenciado por um índice baseado em zero.</span><span class="sxs-lookup"><span data-stu-id="d36de-108">[**CBasePin::GetMediaType**](cbasepin-getmediatype.md):Retrieves a media type, referenced by a zero-based index.</span></span>
-   <span data-ttu-id="d36de-109">[**CBasePin:: GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): determina se o conjunto de tipos preferenciais foi alterado.</span><span class="sxs-lookup"><span data-stu-id="d36de-109">[**CBasePin::GetMediaTypeVersion**](cbasepin-getmediatypeversion.md): Determines whether the set of preferred types has changed.</span></span>

<span data-ttu-id="d36de-110">Sempre que um PIN altera sua lista de tipos de mídia preferenciais, o PIN incrementa o número de versão do tipo de mídia.</span><span class="sxs-lookup"><span data-stu-id="d36de-110">Whenever a pin alters its list of preferred media types, the pin increments the media-type version number.</span></span> <span data-ttu-id="d36de-111">Quando isso acontece, o objeto enumerador não é mais sincronizado com o PIN e os métodos de classe retornam VFW \_ E \_ enum \_ fora \_ de \_ sincronia.</span><span class="sxs-lookup"><span data-stu-id="d36de-111">When this happens, the enumerator object is no longer synchronized with the pin, and the class methods return VFW\_E\_ENUM\_OUT\_OF\_SYNC.</span></span> <span data-ttu-id="d36de-112">Chame o método [**CEnumMediaTypes:: Reset**](cenummediatypes-reset.md) para ressincronizar o enumerador.</span><span class="sxs-lookup"><span data-stu-id="d36de-112">Call the [**CEnumMediaTypes::Reset**](cenummediatypes-reset.md) method to resynchronize the enumerator.</span></span>



| <span data-ttu-id="d36de-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="d36de-113">Public Methods</span></span>                                               | <span data-ttu-id="d36de-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="d36de-114">Description</span></span>                                                     |
|--------------------------------------------------------------|-----------------------------------------------------------------|
| [<span data-ttu-id="d36de-115">**CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="d36de-115">**CEnumMediaTypes**</span></span>](cenummediatypes-cenummediatypes.md)   | <span data-ttu-id="d36de-116">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="d36de-116">Constructor method.</span></span>                                             |
| [<span data-ttu-id="d36de-117">**~ CEnumMediaTypes**</span><span class="sxs-lookup"><span data-stu-id="d36de-117">**~CEnumMediaTypes**</span></span>](cenummediatypes--cenummediatypes.md) | <span data-ttu-id="d36de-118">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="d36de-118">Destructor method.</span></span> <span data-ttu-id="d36de-119">VirtuaisLUNs.</span><span class="sxs-lookup"><span data-stu-id="d36de-119">Virtual.</span></span>                                     |
| <span data-ttu-id="d36de-120">Métodos IEnumMediaTypes</span><span class="sxs-lookup"><span data-stu-id="d36de-120">IEnumMediaTypes Methods</span></span>                                      | <span data-ttu-id="d36de-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="d36de-121">Description</span></span>                                                     |
| [<span data-ttu-id="d36de-122">**8i**</span><span class="sxs-lookup"><span data-stu-id="d36de-122">**Clone**</span></span>](cenummediatypes-clone.md)                       | <span data-ttu-id="d36de-123">Faz uma cópia do enumerador com o mesmo estado de enumeração.</span><span class="sxs-lookup"><span data-stu-id="d36de-123">Makes a copy of the enumerator with the same enumeration state.</span></span> |
| [<span data-ttu-id="d36de-124">**Avançar**</span><span class="sxs-lookup"><span data-stu-id="d36de-124">**Next**</span></span>](cenummediatypes-next.md)                         | <span data-ttu-id="d36de-125">Recupera um número especificado de tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="d36de-125">Retrieves a specified number of media types.</span></span>                    |
| [<span data-ttu-id="d36de-126">**Redefinir**</span><span class="sxs-lookup"><span data-stu-id="d36de-126">**Reset**</span></span>](cenummediatypes-reset.md)                       | <span data-ttu-id="d36de-127">Redefine a sequência de enumeração para o início.</span><span class="sxs-lookup"><span data-stu-id="d36de-127">Resets the enumeration sequence to the beginning.</span></span>               |
| [<span data-ttu-id="d36de-128">**Ignorar**</span><span class="sxs-lookup"><span data-stu-id="d36de-128">**Skip**</span></span>](cenummediatypes-skip.md)                         | <span data-ttu-id="d36de-129">Ignora um número especificado de tipos de mídia.</span><span class="sxs-lookup"><span data-stu-id="d36de-129">Skips over a specified number of media types.</span></span>                   |



 

## <a name="requirements"></a><span data-ttu-id="d36de-130">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d36de-130">Requirements</span></span>



| <span data-ttu-id="d36de-131">Requisito</span><span class="sxs-lookup"><span data-stu-id="d36de-131">Requirement</span></span> | <span data-ttu-id="d36de-132">Valor</span><span class="sxs-lookup"><span data-stu-id="d36de-132">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d36de-133">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d36de-133">Header</span></span><br/>  | <dl> <span data-ttu-id="d36de-134"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d36de-134"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d36de-135">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d36de-135">Library</span></span><br/> | <dl> <span data-ttu-id="d36de-136"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d36de-136"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




