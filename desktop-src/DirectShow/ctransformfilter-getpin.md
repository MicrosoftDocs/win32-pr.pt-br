---
description: O método GetPin recupera um PIN.
ms.assetid: 5d278ef0-e5ce-439e-93b1-fec988c55854
title: Método CTransformFilter. GetPin (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 30567db84eefd5471dbbe1fbd2d2e5ed64514ba2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759089"
---
# <a name="ctransformfiltergetpin-method"></a><span data-ttu-id="8ae70-103">Método CTransformFilter. GetPin</span><span class="sxs-lookup"><span data-stu-id="8ae70-103">CTransformFilter.GetPin method</span></span>

<span data-ttu-id="8ae70-104">O `GetPin` método recupera um PIN.</span><span class="sxs-lookup"><span data-stu-id="8ae70-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ae70-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ae70-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="8ae70-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ae70-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8ae70-107">*n*</span><span class="sxs-lookup"><span data-stu-id="8ae70-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="8ae70-108">Número do PIN especificado, indexado de zero.</span><span class="sxs-lookup"><span data-stu-id="8ae70-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="8ae70-109">Nesse filtro, o pino 0 é o pino de entrada e o pino 1 é o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="8ae70-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8ae70-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8ae70-110">Return value</span></span>

<span data-ttu-id="8ae70-111">Retorna um ponteiro para o objeto [**CBasePin**](cbasepin.md) que implementa o PIN ou **NULL** se o método falhar.</span><span class="sxs-lookup"><span data-stu-id="8ae70-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ae70-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ae70-112">Remarks</span></span>

<span data-ttu-id="8ae70-113">Esse método implementa o método puramente virtual [**CBaseFilter:: GetPin**](cbasefilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="8ae70-113">This method implements the pure virtual [**CBaseFilter::GetPin**](cbasefilter-getpin.md) method.</span></span> <span data-ttu-id="8ae70-114">Na primeira vez que o método é chamado, ele cria ambos os Pins.</span><span class="sxs-lookup"><span data-stu-id="8ae70-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="8ae70-115">Esse método não incrementa a contagem de referência no PIN retornado, portanto, o PIN retornado não tem uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="8ae70-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="8ae70-116">Se o chamador precisar manter uma referência no PIN, ele deverá chamar o método **IUnknown:: AddRef** no PIN.</span><span class="sxs-lookup"><span data-stu-id="8ae70-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="8ae70-117">Se o filtro usar os Pins [**CTransformInputPin**](ctransforminputpin.md) e [**CTransformOutputPin**](ctransformoutputpin.md) padrão, você provavelmente não precisará substituir esse método.</span><span class="sxs-lookup"><span data-stu-id="8ae70-117">If the filter uses the default [**CTransformInputPin**](ctransforminputpin.md) and [**CTransformOutputPin**](ctransformoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="8ae70-118">No entanto, se o filtro usar Pins que estendam essas classes, você deverá substituir esse método para criar Pins desse tipo.</span><span class="sxs-lookup"><span data-stu-id="8ae70-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ae70-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ae70-119">Requirements</span></span>



| <span data-ttu-id="8ae70-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ae70-120">Requirement</span></span> | <span data-ttu-id="8ae70-121">Valor</span><span class="sxs-lookup"><span data-stu-id="8ae70-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ae70-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ae70-122">Header</span></span><br/>  | <dl> <span data-ttu-id="8ae70-123"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae70-123"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8ae70-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ae70-124">Library</span></span><br/> | <dl> <span data-ttu-id="8ae70-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8ae70-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ae70-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="8ae70-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ae70-127">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="8ae70-127">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




