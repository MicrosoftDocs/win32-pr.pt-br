---
description: Método CTransInPlaceInputPin. PeekAllocator – o método PeekAllocator retorna um ponteiro para o alocador do PIN. O método não incrementa a contagem de referência na interface.
ms.assetid: 67f1b872-4ae2-4fbe-9240-801ef8ae1e5b
title: Método CTransInPlaceInputPin. PeekAllocator (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceInputPin.PeekAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f7a5f7cb0fbe754890b1d7930bb54c6fca47afa5
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084664"
---
# <a name="ctransinplaceinputpinpeekallocator-method"></a><span data-ttu-id="aeaa6-104">Método CTransInPlaceInputPin. PeekAllocator</span><span class="sxs-lookup"><span data-stu-id="aeaa6-104">CTransInPlaceInputPin.PeekAllocator method</span></span>

<span data-ttu-id="aeaa6-105">O `PeekAllocator` método retorna um ponteiro para o alocador do PIN.</span><span class="sxs-lookup"><span data-stu-id="aeaa6-105">The `PeekAllocator` method returns a pointer to the pin's allocator.</span></span> <span data-ttu-id="aeaa6-106">O método não incrementa a contagem de referência na interface.</span><span class="sxs-lookup"><span data-stu-id="aeaa6-106">The method does not increment the reference count on the interface.</span></span>

## <a name="syntax"></a><span data-ttu-id="aeaa6-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aeaa6-107">Syntax</span></span>


```C++
IMemAllocator* PeekAllocator();
```



## <a name="parameters"></a><span data-ttu-id="aeaa6-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aeaa6-108">Parameters</span></span>

<span data-ttu-id="aeaa6-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="aeaa6-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aeaa6-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="aeaa6-110">Return value</span></span>

<span data-ttu-id="aeaa6-111">Retorna a variável de membro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="aeaa6-111">Returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="aeaa6-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aeaa6-112">Requirements</span></span>



| <span data-ttu-id="aeaa6-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="aeaa6-113">Requirement</span></span> | <span data-ttu-id="aeaa6-114">Valor</span><span class="sxs-lookup"><span data-stu-id="aeaa6-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aeaa6-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aeaa6-115">Header</span></span><br/>  | <dl> <span data-ttu-id="aeaa6-116"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="aeaa6-116"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="aeaa6-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aeaa6-117">Library</span></span><br/> | <dl> <span data-ttu-id="aeaa6-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="aeaa6-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aeaa6-119">Consulte também</span><span class="sxs-lookup"><span data-stu-id="aeaa6-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aeaa6-120">**Classe CTransInPlaceInputPin**</span><span class="sxs-lookup"><span data-stu-id="aeaa6-120">**CTransInPlaceInputPin Class**</span></span>](ctransinplaceinputpin.md)
</dt> </dl>

 

 




