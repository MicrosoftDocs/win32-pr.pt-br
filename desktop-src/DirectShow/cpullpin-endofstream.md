---
description: O método EndOfStream é chamado depois que o objeto entrega a última amostra. A classe derivada deve implementar esse método.
ms.assetid: 55a32c17-9993-4ad7-8829-6aa5c1407622
title: Método CPullPin. EndOfStream (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a1df28430cdb71edd2ef9791e6c26092bbb21d0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782254"
---
# <a name="cpullpinendofstream-method"></a><span data-ttu-id="0734d-104">Método CPullPin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="0734d-104">CPullPin.EndOfStream method</span></span>

<span data-ttu-id="0734d-105">O `EndOfStream` método é chamado depois que o objeto entrega o último exemplo.</span><span class="sxs-lookup"><span data-stu-id="0734d-105">The `EndOfStream` method is called after the object delivers the last sample.</span></span> <span data-ttu-id="0734d-106">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="0734d-106">The derived class must implement this method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0734d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0734d-107">Syntax</span></span>


```C++
virtual HRESULT EndOfStream() = 0;
```



## <a name="parameters"></a><span data-ttu-id="0734d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0734d-108">Parameters</span></span>

<span data-ttu-id="0734d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="0734d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="0734d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0734d-110">Return value</span></span>

<span data-ttu-id="0734d-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0734d-111">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0734d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="0734d-112">Remarks</span></span>

<span data-ttu-id="0734d-113">Use este método para chamar [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) em cada PIN de entrada downstream que recebe dados desse objeto.</span><span class="sxs-lookup"><span data-stu-id="0734d-113">Use this method to call [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) on each downstream input pin that receives data from this object.</span></span> <span data-ttu-id="0734d-114">Se os Pins de saída do filtro derivarem de [**CBaseOutputPin**](cbaseoutputpin.md), chame o método [**CBaseOutputPin::D eliverendofstream**](cbaseoutputpin-deliverendofstream.md) .</span><span class="sxs-lookup"><span data-stu-id="0734d-114">If your filter's output pin(s) derive from [**CBaseOutputPin**](cbaseoutputpin.md), call the [**CBaseOutputPin::DeliverEndOfStream**](cbaseoutputpin-deliverendofstream.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0734d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0734d-115">Requirements</span></span>



| <span data-ttu-id="0734d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0734d-116">Requirement</span></span> | <span data-ttu-id="0734d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0734d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0734d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0734d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0734d-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="0734d-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="0734d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0734d-120">Library</span></span><br/> | <dl> <span data-ttu-id="0734d-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0734d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0734d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="0734d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0734d-123">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="0734d-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




