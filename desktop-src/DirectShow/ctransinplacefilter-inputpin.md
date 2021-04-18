---
description: O método InputPin recupera um ponteiro para o PIN de entrada do filtro.
ms.assetid: 533a962e-225d-4f10-a9c3-1464bea512ba
title: Método CTransInPlaceFilter. InputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.InputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b92775eca87a88659326aa5b34eb0c15109ed8a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758648"
---
# <a name="ctransinplacefilterinputpin-method"></a><span data-ttu-id="c3b04-103">Método CTransInPlaceFilter. InputPin</span><span class="sxs-lookup"><span data-stu-id="c3b04-103">CTransInPlaceFilter.InputPin method</span></span>

<span data-ttu-id="c3b04-104">O `InputPin` método recupera um ponteiro para o PIN de entrada do filtro.</span><span class="sxs-lookup"><span data-stu-id="c3b04-104">The `InputPin` method retrieves a pointer to the filter's input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3b04-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3b04-105">Syntax</span></span>


```C++
CTransInPlaceInputPin* InputPin();
```



## <a name="parameters"></a><span data-ttu-id="c3b04-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3b04-106">Parameters</span></span>

<span data-ttu-id="c3b04-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3b04-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3b04-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3b04-108">Return value</span></span>

<span data-ttu-id="c3b04-109">Retorna a variável de membro [**CTransformFilter:: m \_ pInput**](ctransformfilter-m-pinput.md) .</span><span class="sxs-lookup"><span data-stu-id="c3b04-109">Returns the [**CTransformFilter::m\_pInput**](ctransformfilter-m-pinput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3b04-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3b04-110">Requirements</span></span>



| <span data-ttu-id="c3b04-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3b04-111">Requirement</span></span> | <span data-ttu-id="c3b04-112">Valor</span><span class="sxs-lookup"><span data-stu-id="c3b04-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3b04-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3b04-113">Header</span></span><br/>  | <dl> <span data-ttu-id="c3b04-114"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3b04-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3b04-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3b04-115">Library</span></span><br/> | <dl> <span data-ttu-id="c3b04-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c3b04-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3b04-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3b04-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3b04-118">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="c3b04-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




