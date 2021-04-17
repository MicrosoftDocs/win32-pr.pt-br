---
description: A classe CBaseDispatch é uma classe base para implementar a interface IDispatch em um filtro do DirectShow.
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: Classe CBaseDispatch (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748833"
---
# <a name="cbasedispatch-class"></a><span data-ttu-id="6426f-103">Classe CBaseDispatch</span><span class="sxs-lookup"><span data-stu-id="6426f-103">CBaseDispatch class</span></span>

![hierarquia de classe CBaseDispatch](images/cutil01.png)

<span data-ttu-id="6426f-105">A classe **CBaseDispatch** é uma classe base para implementar a interface **IDispatch** em um filtro do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="6426f-105">The **CBaseDispatch** class is a base class for implementing the **IDispatch** interface in a DirectShow filter.</span></span>

<span data-ttu-id="6426f-106">Essa classe é limitada ao suporte às interfaces compatíveis com automação exportadas pela biblioteca de tipos do DirectShow, QuartzTypeLib.</span><span class="sxs-lookup"><span data-stu-id="6426f-106">This class is limited to supporting the Automation-compatible interfaces exported by the DirectShow type library, QuartzTypeLib.</span></span> <span data-ttu-id="6426f-107">Por exemplo, as classes [**CMediaControl**](cmediacontrol.md) e [**CMediaPosition**](cmediaposition.md) usam **CBaseDispatch** para implementar [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) e [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectivamente.</span><span class="sxs-lookup"><span data-stu-id="6426f-107">For example, the [**CMediaControl**](cmediacontrol.md) and [**CMediaPosition**](cmediaposition.md) classes use **CBaseDispatch** to implement [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) and [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition), respectively.</span></span> <span data-ttu-id="6426f-108">Devido a essa limitação, provavelmente não há motivo para usar o **CBaseDispatch** diretamente em seus próprios filtros.</span><span class="sxs-lookup"><span data-stu-id="6426f-108">Because of this limitation, there is probably no reason to use **CBaseDispatch** directly in your own filters.</span></span>

<span data-ttu-id="6426f-109">Para usar essa classe, faça o seguinte:</span><span class="sxs-lookup"><span data-stu-id="6426f-109">To use this class, do the following:</span></span>

-   <span data-ttu-id="6426f-110">Declare uma nova classe que dê suporte a **IDispatch**.</span><span class="sxs-lookup"><span data-stu-id="6426f-110">Declare a new class that supports **IDispatch**.</span></span>
-   <span data-ttu-id="6426f-111">Dê à sua nova classe uma variável de membro privado do tipo **CBaseDispatch**.</span><span class="sxs-lookup"><span data-stu-id="6426f-111">Give your new class a private member variable of type **CBaseDispatch**.</span></span>
-   <span data-ttu-id="6426f-112">Implemente os métodos **IDispatch** .</span><span class="sxs-lookup"><span data-stu-id="6426f-112">Implement the **IDispatch** methods.</span></span>
-   <span data-ttu-id="6426f-113">Em seus métodos **IDispatch** , chame os métodos **CBaseDispatch** .</span><span class="sxs-lookup"><span data-stu-id="6426f-113">In your **IDispatch** methods, call the **CBaseDispatch** methods.</span></span>

<span data-ttu-id="6426f-114">Para obter mais detalhes, consulte o código-fonte de qualquer uma das classes de exemplo declaradas em Ctlutil. h.</span><span class="sxs-lookup"><span data-stu-id="6426f-114">For more details, refer to the source code for any of the sample classes declared in Ctlutil.h.</span></span>



| <span data-ttu-id="6426f-115">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="6426f-115">Public Methods</span></span>                                             | <span data-ttu-id="6426f-116">Descrição</span><span class="sxs-lookup"><span data-stu-id="6426f-116">Description</span></span>                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="6426f-117">**CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="6426f-117">**CBaseDispatch**</span></span>](cbasedispatch-cbasedispatch.md)       | <span data-ttu-id="6426f-118">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="6426f-118">Constructor method.</span></span>                                                                                                 |
| [<span data-ttu-id="6426f-119">**~ CBaseDispatch**</span><span class="sxs-lookup"><span data-stu-id="6426f-119">**~CBaseDispatch**</span></span>](cbasedispatch--cbasedispatch.md)     | <span data-ttu-id="6426f-120">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="6426f-120">Destructor method.</span></span>                                                                                                  |
| [<span data-ttu-id="6426f-121">**GetIDsOfNames**</span><span class="sxs-lookup"><span data-stu-id="6426f-121">**GetIDsOfNames**</span></span>](cbasedispatch-getidsofnames.md)       | <span data-ttu-id="6426f-122">Mapeia um conjunto de nomes para um conjunto correspondente de DISPIDs.</span><span class="sxs-lookup"><span data-stu-id="6426f-122">Maps a set of names to a corresponding set of DISPIDs.</span></span>                                                              |
| [<span data-ttu-id="6426f-123">**GetTypeInfo**</span><span class="sxs-lookup"><span data-stu-id="6426f-123">**GetTypeInfo**</span></span>](cbasedispatch-gettypeinfo.md)           | <span data-ttu-id="6426f-124">Recupera as informações de tipo do objeto, que podem ser usadas para obter as informações de tipo de uma interface.</span><span class="sxs-lookup"><span data-stu-id="6426f-124">Retrieves the type information for the object, which can then be used to get the type information for an interface.</span></span> |
| [<span data-ttu-id="6426f-125">**GetTypeInfoCount**</span><span class="sxs-lookup"><span data-stu-id="6426f-125">**GetTypeInfoCount**</span></span>](cbasedispatch-gettypeinfocount.md) | <span data-ttu-id="6426f-126">Recupera o número de interfaces de informações de tipo que o objeto fornece.</span><span class="sxs-lookup"><span data-stu-id="6426f-126">Retrieves the number of type information interfaces the object provides.</span></span>                                            |



 

## <a name="requirements"></a><span data-ttu-id="6426f-127">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6426f-127">Requirements</span></span>



| <span data-ttu-id="6426f-128">Requisito</span><span class="sxs-lookup"><span data-stu-id="6426f-128">Requirement</span></span> | <span data-ttu-id="6426f-129">Valor</span><span class="sxs-lookup"><span data-stu-id="6426f-129">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6426f-130">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6426f-130">Header</span></span><br/>  | <dl> <span data-ttu-id="6426f-131"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6426f-131"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6426f-132">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6426f-132">Library</span></span><br/> | <dl> <span data-ttu-id="6426f-133"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6426f-133"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6426f-134">Confira também</span><span class="sxs-lookup"><span data-stu-id="6426f-134">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6426f-135">Classes base do DirectShow</span><span class="sxs-lookup"><span data-stu-id="6426f-135">DirectShow Base Classes</span></span>](directshow-base-classes.md)
</dt> </dl>

 

 




