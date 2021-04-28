---
description: Método CTransInPlaceFilter. GetPin – o método GetPin recupera um PIN.
ms.assetid: d8e4973b-2af4-4141-ab2e-ea2159cd51be
title: Método CTransInPlaceFilter. GetPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.GetPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1075f2a14c58b085b73f2e4283458286c118a7ae
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084764"
---
# <a name="ctransinplacefiltergetpin-method"></a><span data-ttu-id="21f8b-103">Método CTransInPlaceFilter. GetPin</span><span class="sxs-lookup"><span data-stu-id="21f8b-103">CTransInPlaceFilter.GetPin method</span></span>

<span data-ttu-id="21f8b-104">O `GetPin` método recupera um PIN.</span><span class="sxs-lookup"><span data-stu-id="21f8b-104">The `GetPin` method retrieves a pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="21f8b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21f8b-105">Syntax</span></span>


```C++
virtual CBasePin* GetPin(
   int n
);
```



## <a name="parameters"></a><span data-ttu-id="21f8b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21f8b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21f8b-107">*n*</span><span class="sxs-lookup"><span data-stu-id="21f8b-107">*n*</span></span> 
</dt> <dd>

<span data-ttu-id="21f8b-108">Número do PIN especificado, indexado de zero.</span><span class="sxs-lookup"><span data-stu-id="21f8b-108">Number of the specified pin, indexed from zero.</span></span> <span data-ttu-id="21f8b-109">Nesse filtro, o pino 0 é o pino de entrada e o pino 1 é o pino de saída.</span><span class="sxs-lookup"><span data-stu-id="21f8b-109">On this filter, pin 0 is the input pin, and pin 1 is the output pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21f8b-110">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="21f8b-110">Return value</span></span>

<span data-ttu-id="21f8b-111">Retorna um ponteiro para o objeto [**CBasePin**](cbasepin.md) que implementa o PIN ou **NULL** se o método falhar.</span><span class="sxs-lookup"><span data-stu-id="21f8b-111">Returns a pointer to the [**CBasePin**](cbasepin.md) object that implements the pin, or **NULL** if the method fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="21f8b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="21f8b-112">Remarks</span></span>

<span data-ttu-id="21f8b-113">Esse método substitui o método [**CTransformFilter:: GetPin**](ctransformfilter-getpin.md) .</span><span class="sxs-lookup"><span data-stu-id="21f8b-113">This method overrides the [**CTransformFilter::GetPin**](ctransformfilter-getpin.md) method.</span></span> <span data-ttu-id="21f8b-114">Na primeira vez que o método é chamado, ele cria ambos os Pins.</span><span class="sxs-lookup"><span data-stu-id="21f8b-114">The first time the method is called, it creates both pins.</span></span>

<span data-ttu-id="21f8b-115">Esse método não incrementa a contagem de referência no PIN retornado, portanto, o PIN retornado não tem uma contagem de referência pendente.</span><span class="sxs-lookup"><span data-stu-id="21f8b-115">This method does not increment the reference count on the returned pin, so the returned pin does not have an outstanding reference count.</span></span> <span data-ttu-id="21f8b-116">Se o chamador precisar manter uma referência no PIN, ele deverá chamar o método **IUnknown:: AddRef** no PIN.</span><span class="sxs-lookup"><span data-stu-id="21f8b-116">If the caller needs to keep a reference on the pin, it should call the **IUnknown::AddRef** method on the pin.</span></span>

<span data-ttu-id="21f8b-117">Se o filtro usar os Pins [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) e [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) padrão, você provavelmente não precisará substituir esse método.</span><span class="sxs-lookup"><span data-stu-id="21f8b-117">If the filter uses the default [**CTransInPlaceInputPin**](ctransinplaceinputpin.md) and [**CTransInPlaceOutputPin**](ctransinplaceoutputpin.md) pins, you probably do not need to override this method.</span></span> <span data-ttu-id="21f8b-118">No entanto, se o filtro usar Pins que estendam essas classes, você deverá substituir esse método para criar Pins desse tipo.</span><span class="sxs-lookup"><span data-stu-id="21f8b-118">If the filter uses pins that extend those classes, however, you must override this method to create pins of that type.</span></span>

## <a name="requirements"></a><span data-ttu-id="21f8b-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21f8b-119">Requirements</span></span>



| <span data-ttu-id="21f8b-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="21f8b-120">Requirement</span></span> | <span data-ttu-id="21f8b-121">Valor</span><span class="sxs-lookup"><span data-stu-id="21f8b-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21f8b-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21f8b-122">Header</span></span><br/>  | <dl> <span data-ttu-id="21f8b-123"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21f8b-123"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="21f8b-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21f8b-124">Library</span></span><br/> | <dl> <span data-ttu-id="21f8b-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="21f8b-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21f8b-126">Consulte também</span><span class="sxs-lookup"><span data-stu-id="21f8b-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21f8b-127">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="21f8b-127">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




