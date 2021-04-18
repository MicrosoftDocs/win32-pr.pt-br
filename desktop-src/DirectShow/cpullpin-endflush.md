---
description: O método EndFlush informa o filtro proprietário para finalizar uma operação de liberação. A classe derivada deve implementar esse método.
ms.assetid: 5b178b09-019c-4b5b-9794-5176b5402e1c
title: Método CPullPin. EndFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e58cb9a903f0841de2442216fab0e360007206b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780861"
---
# <a name="cpullpinendflush-method"></a><span data-ttu-id="aa642-104">Método CPullPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="aa642-104">CPullPin.EndFlush method</span></span>

<span data-ttu-id="aa642-105">O `EndFlush` método informa o filtro proprietário para finalizar uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="aa642-105">The `EndFlush` method informs the owning filter to end a flush operation.</span></span> <span data-ttu-id="aa642-106">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="aa642-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="aa642-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="aa642-107">Syntax</span></span>


```C++
virtual HRESULT EndFlush() = 0;
```



## <a name="parameters"></a><span data-ttu-id="aa642-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="aa642-108">Parameters</span></span>

<span data-ttu-id="aa642-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="aa642-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="aa642-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="aa642-110">Return value</span></span>

<span data-ttu-id="aa642-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="aa642-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="aa642-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="aa642-112">Remarks</span></span>

<span data-ttu-id="aa642-113">O método [**CPullPin:: Seek**](cpullpin-seek.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="aa642-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="aa642-114">Implemente esse método para chamar o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) em cada pino de entrada downstream que recebe dados desse objeto.</span><span class="sxs-lookup"><span data-stu-id="aa642-114">Implement this method to call the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="aa642-115">Se os Pins de saída do filtro derivarem de **CBaseOutputPin**, chame o método **CBaseOutputPin::D eliverendflush** .</span><span class="sxs-lookup"><span data-stu-id="aa642-115">If your filter's output pin(s) derive from **CBaseOutputPin**, call the **CBaseOutputPin::DeliverEndFlush** method.</span></span>

<span data-ttu-id="aa642-116">Esse design permite que o filtro busque o fluxo simplesmente chamando **Seek** no objeto **CPullPin** .</span><span class="sxs-lookup"><span data-stu-id="aa642-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="aa642-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="aa642-117">Requirements</span></span>



| <span data-ttu-id="aa642-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="aa642-118">Requirement</span></span> | <span data-ttu-id="aa642-119">Valor</span><span class="sxs-lookup"><span data-stu-id="aa642-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="aa642-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="aa642-120">Header</span></span><br/>  | <dl> <span data-ttu-id="aa642-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="aa642-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="aa642-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="aa642-122">Library</span></span><br/> | <dl> <span data-ttu-id="aa642-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="aa642-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="aa642-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="aa642-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aa642-125">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="aa642-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




