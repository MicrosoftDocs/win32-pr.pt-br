---
description: O método BeginFlush informa o filtro proprietário para liberar os filtros downstream. A classe derivada deve implementar esse método.
ms.assetid: 612f230c-7f23-42cf-b565-344fae0b6f9a
title: Método CPullPin. BeginFlush (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f2e4c26b99c78794449077e73040d98b5481fb91
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757304"
---
# <a name="cpullpinbeginflush-method"></a><span data-ttu-id="01c29-104">Método CPullPin. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="01c29-104">CPullPin.BeginFlush method</span></span>

<span data-ttu-id="01c29-105">O `BeginFlush` método informa o filtro proprietário para liberar os filtros downstream.</span><span class="sxs-lookup"><span data-stu-id="01c29-105">The `BeginFlush` method informs the owning filter to flush the downstream filters.</span></span> <span data-ttu-id="01c29-106">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="01c29-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="01c29-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="01c29-107">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="01c29-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="01c29-108">Parameters</span></span>

<span data-ttu-id="01c29-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="01c29-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="01c29-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="01c29-110">Return value</span></span>

<span data-ttu-id="01c29-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="01c29-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="01c29-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="01c29-112">Remarks</span></span>

<span data-ttu-id="01c29-113">O método [**CPullPin:: Seek**](cpullpin-seek.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="01c29-113">The [**CPullPin::Seek**](cpullpin-seek.md) method calls this method.</span></span> <span data-ttu-id="01c29-114">Implemente este método para chamar o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) em cada pino de entrada downstream que recebe dados desse objeto.</span><span class="sxs-lookup"><span data-stu-id="01c29-114">Implement this method to call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="01c29-115">Se os Pins de saída do filtro derivarem de [**CBaseOutputPin**](cbaseoutputpin.md), chame o método [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="01c29-115">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>

<span data-ttu-id="01c29-116">Esse design permite que o filtro busque o fluxo simplesmente chamando **Seek** no objeto **CPullPin** .</span><span class="sxs-lookup"><span data-stu-id="01c29-116">This design enables the filter to seek the stream simply by calling **Seek** on the **CPullPin** object.</span></span>

## <a name="requirements"></a><span data-ttu-id="01c29-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="01c29-117">Requirements</span></span>



| <span data-ttu-id="01c29-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="01c29-118">Requirement</span></span> | <span data-ttu-id="01c29-119">Valor</span><span class="sxs-lookup"><span data-stu-id="01c29-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="01c29-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="01c29-120">Header</span></span><br/>  | <dl> <span data-ttu-id="01c29-121"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="01c29-121"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="01c29-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="01c29-122">Library</span></span><br/> | <dl> <span data-ttu-id="01c29-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="01c29-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="01c29-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="01c29-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="01c29-125">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="01c29-125">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




