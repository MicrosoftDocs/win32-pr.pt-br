---
description: A classe CMediaPosition manipula os métodos IDispatch da interface dupla IMediaPosition.
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: Classe CMediaPosition (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 60d06a08badf3302ef4ddb352d840842a2605600
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105789973"
---
# <a name="cmediaposition-class"></a><span data-ttu-id="2a79c-103">Classe CMediaPosition</span><span class="sxs-lookup"><span data-stu-id="2a79c-103">CMediaPosition class</span></span>

![hierarquia de classe CMediaPosition](images/cutil14.png)

<span data-ttu-id="2a79c-105">A classe **CMediaPosition** manipula os métodos **IDispatch** da interface dupla [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) .</span><span class="sxs-lookup"><span data-stu-id="2a79c-105">The **CMediaPosition** class handles the **IDispatch** methods of the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) dual interface.</span></span>

<span data-ttu-id="2a79c-106">Essa classe herda a interface [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) , mas não a implementa.</span><span class="sxs-lookup"><span data-stu-id="2a79c-106">This class inherits the [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) interface but does not implement it.</span></span> <span data-ttu-id="2a79c-107">Ele implementa o **IDispatch** por meio da classe [**CBaseDispatch**](cbasedispatch.md) e da biblioteca de tipos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="2a79c-107">It implements **IDispatch** through the [**CBaseDispatch**](cbasedispatch.md) class and the DirectShow type library.</span></span> <span data-ttu-id="2a79c-108">Não use essa classe diretamente.</span><span class="sxs-lookup"><span data-stu-id="2a79c-108">Do not use this class directly.</span></span> <span data-ttu-id="2a79c-109">Em vez disso, use uma das seguintes classes:</span><span class="sxs-lookup"><span data-stu-id="2a79c-109">Instead, use one of the following classes:</span></span>

-   <span data-ttu-id="2a79c-110">Filtros de origem: Use a classe base [**CSourceSeeking**](csourceseeking.md) para implementar a busca.</span><span class="sxs-lookup"><span data-stu-id="2a79c-110">Source filters: Use the [**CSourceSeeking**](csourceseeking.md) base class to implement seeking.</span></span>
-   <span data-ttu-id="2a79c-111">Filtros de transformação: Use a classe [**CPosPassThru**](cpospassthru.md) para passar comandos de busca ascendentes.</span><span class="sxs-lookup"><span data-stu-id="2a79c-111">Transform filters: Use the [**CPosPassThru**](cpospassthru.md) class to pass seeking commands upstream.</span></span>
-   <span data-ttu-id="2a79c-112">Renderizadores: Use a classe [**CRendererPosPassThru**](crendererpospassthru.md) para passar comandos de busca ascendentes.</span><span class="sxs-lookup"><span data-stu-id="2a79c-112">Renderers: Use the [**CRendererPosPassThru**](crendererpospassthru.md) class to pass seeking commands upstream.</span></span>



| <span data-ttu-id="2a79c-113">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="2a79c-113">Public Methods</span></span>                                              | <span data-ttu-id="2a79c-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a79c-114">Description</span></span>                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="2a79c-115">**CMediaPosition**</span><span class="sxs-lookup"><span data-stu-id="2a79c-115">**CMediaPosition**</span></span>](cmediaposition-cmediaposition.md)     | <span data-ttu-id="2a79c-116">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="2a79c-116">Constructor method.</span></span>                                                                                                 |
| <span data-ttu-id="2a79c-117">Métodos IDispatch</span><span class="sxs-lookup"><span data-stu-id="2a79c-117">IDispatch Methods</span></span>                                           | <span data-ttu-id="2a79c-118">Descrição</span><span class="sxs-lookup"><span data-stu-id="2a79c-118">Description</span></span>                                                                                                         |
| [<span data-ttu-id="2a79c-119">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="2a79c-119">**GetIDsOfNames**</span></span>](cmediaposition-getidsofnames.md)       | <span data-ttu-id="2a79c-120">Mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="2a79c-120">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="2a79c-121">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="2a79c-121">**GetTypeInfo**</span></span>](cmediaposition-gettypeinfo.md)           | <span data-ttu-id="2a79c-122">Recupera as informações de tipo do objeto, que podem ser usadas para obter as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="2a79c-122">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="2a79c-123">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="2a79c-123">**GetTypeInfoCount**</span></span>](cmediaposition-gettypeinfocount.md) | <span data-ttu-id="2a79c-124">Recupera o número de interfaces de informações de tipo que o objeto fornece.</span><span class="sxs-lookup"><span data-stu-id="2a79c-124">Retrieves the number of type information interfaces the object provides.</span></span>                                            |
| [<span data-ttu-id="2a79c-125">**Chame**</span><span class="sxs-lookup"><span data-stu-id="2a79c-125">**Invoke**</span></span>](cmediaposition-invoke.md)                     | <span data-ttu-id="2a79c-126">Fornece acesso a propriedades e métodos expostos pelo objeto.</span><span class="sxs-lookup"><span data-stu-id="2a79c-126">Provides access to properties and methods exposed by the object.</span></span>                                                    |



 

## <a name="requirements"></a><span data-ttu-id="2a79c-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2a79c-127">Requirements</span></span>



| <span data-ttu-id="2a79c-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="2a79c-128">Requirement</span></span> | <span data-ttu-id="2a79c-129">Valor</span><span class="sxs-lookup"><span data-stu-id="2a79c-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a79c-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2a79c-130">Header</span></span><br/>  | <dl> <span data-ttu-id="2a79c-131"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2a79c-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2a79c-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2a79c-132">Library</span></span><br/> | <dl> <span data-ttu-id="2a79c-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2a79c-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2a79c-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="2a79c-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a79c-135">Classes base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="2a79c-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




