---
description: A classe CAutoUsingOutputPin Obtém e libera o acesso a um objeto CDynamicOutputPin.
ms.assetid: 4ded5d18-4b14-4574-ad1f-73b886a51fac
title: Classe CAutoUsingOutputPin (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAutoUsingOutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b664267ce2ff0dbbeeba8bc74708c9c67e185ae4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755368"
---
# <a name="cautousingoutputpin-class"></a><span data-ttu-id="4707a-103">Classe CAutoUsingOutputPin</span><span class="sxs-lookup"><span data-stu-id="4707a-103">CAutoUsingOutputPin class</span></span>

<span data-ttu-id="4707a-104">A classe **CAutoUsingOutputPin** Obtém e libera o acesso a um objeto [**CDynamicOutputPin**](cdynamicoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="4707a-104">The **CAutoUsingOutputPin** class obtains and releases access to a [**CDynamicOutputPin**](cdynamicoutputpin.md) object.</span></span>

<span data-ttu-id="4707a-105">**CAutoUsingOutputPin** tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="4707a-105">**CAutoUsingOutputPin** has these types of members:</span></span>



| <span data-ttu-id="4707a-106">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="4707a-106">Public Methods</span></span>                                                           | <span data-ttu-id="4707a-107">Descrição</span><span class="sxs-lookup"><span data-stu-id="4707a-107">Description</span></span>                                              |
|--------------------------------------------------------------------------|----------------------------------------------------------|
| [<span data-ttu-id="4707a-108">**CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="4707a-108">**CAutoUsingOutputPin**</span></span>](cautousingoutputpin-cautousingoutputpin.md)   | <span data-ttu-id="4707a-109">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="4707a-109">Constructor method.</span></span> <span data-ttu-id="4707a-110">Obtém acesso ao PIN especificado.</span><span class="sxs-lookup"><span data-stu-id="4707a-110">Obtains access to the specified pin.</span></span> |
| [<span data-ttu-id="4707a-111">**~ CAutoUsingOutputPin**</span><span class="sxs-lookup"><span data-stu-id="4707a-111">**~CAutoUsingOutputPin**</span></span>](cautousingoutputpin--cautousingoutputpin.md) | <span data-ttu-id="4707a-112">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="4707a-112">Destructor method.</span></span> <span data-ttu-id="4707a-113">Obtém acesso ao PIN especificado.</span><span class="sxs-lookup"><span data-stu-id="4707a-113">Obtains access to the specified pin.</span></span>  |



 

## <a name="remarks"></a><span data-ttu-id="4707a-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="4707a-114">Remarks</span></span>

<span data-ttu-id="4707a-115">Quando determinados métodos são chamados em [**CDynamicOutputPin**](cdynamicoutputpin.md), o chamador deve obter acesso ao PIN e, em seguida, liberar esse acesso.</span><span class="sxs-lookup"><span data-stu-id="4707a-115">When certain methods are called on [**CDynamicOutputPin**](cdynamicoutputpin.md), the caller must obtain access to the pin and then release that access.</span></span> <span data-ttu-id="4707a-116">Para obter acesso, o chamador usa o método [**CDynamicOutputPin:: StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="4707a-116">To obtain access, the caller uses the [**CDynamicOutputPin::StartUsingOutputPin**](cdynamicoutputpin-startusingoutputpin.md) method.</span></span> <span data-ttu-id="4707a-117">Para liberar o acesso, ele chama o método [**CDynamicOutputPin:: StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) .</span><span class="sxs-lookup"><span data-stu-id="4707a-117">To release access, it calls the [**CDynamicOutputPin::StopUsingOutputPin**](cdynamicoutputpin-stopusingoutputpin.md) method.</span></span> <span data-ttu-id="4707a-118">A classe **CAutoUsingOutputPin** é uma classe auxiliar que manipula essas tarefas em seus métodos de construtor e destruidor.</span><span class="sxs-lookup"><span data-stu-id="4707a-118">The **CAutoUsingOutputPin** class is a helper class that handles these tasks in its constructor and destructor methods.</span></span> <span data-ttu-id="4707a-119">O exemplo de código a seguir mostra como usar essa classe:</span><span class="sxs-lookup"><span data-stu-id="4707a-119">The following code example shows how to use this class:</span></span>


```
CDynamicOutputPin *pPin;
HRESULT hr = S_OK;  // Important! Initialize to S_OK.

// TODO: Obtain a pointer to the pin (not shown).

// Scope for lock.
{
    // Hold lock on pin.
    CAutoUsingOutputPin UsingPin(pPin, &hr)

    if (SUCCEEDED(hr)) 
    {

        // Safe to use the pin.
        hr = pPin->Deliver(pSample);

    }

} // Object goes out of scope here.

// No longer safe to use the pin.
```



## <a name="requirements"></a><span data-ttu-id="4707a-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4707a-120">Requirements</span></span>



| <span data-ttu-id="4707a-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="4707a-121">Requirement</span></span> | <span data-ttu-id="4707a-122">Valor</span><span class="sxs-lookup"><span data-stu-id="4707a-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4707a-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4707a-123">Header</span></span><br/>  | <dl> <span data-ttu-id="4707a-124"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4707a-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="4707a-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4707a-125">Library</span></span><br/> | <dl> <span data-ttu-id="4707a-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4707a-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4707a-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="4707a-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4707a-128">Referência de classe base</span><span class="sxs-lookup"><span data-stu-id="4707a-128">Base Class Reference</span></span>](base-class-reference.md)
</dt> </dl>

 

 




