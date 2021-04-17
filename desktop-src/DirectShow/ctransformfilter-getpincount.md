---
description: O método GetPinCount recupera o número de Pins no filtro.
ms.assetid: 29039ada-fccd-4890-b36b-3dd5c0bbdc3e
title: Método CTransformFilter. GetPinCount (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.GetPinCount
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ba1d2046bf7be31a9c0d3f3d43b13aeeffd1f76b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751481"
---
# <a name="ctransformfiltergetpincount-method"></a><span data-ttu-id="9a56b-103">Método CTransformFilter. GetPinCount</span><span class="sxs-lookup"><span data-stu-id="9a56b-103">CTransformFilter.GetPinCount method</span></span>

<span data-ttu-id="9a56b-104">O `GetPinCount` método recupera o número de Pins no filtro.</span><span class="sxs-lookup"><span data-stu-id="9a56b-104">The `GetPinCount` method retrieves the number of pins on the filter.</span></span>

## <a name="syntax"></a><span data-ttu-id="9a56b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9a56b-105">Syntax</span></span>


```C++
virtual int GetPinCount();
```



## <a name="parameters"></a><span data-ttu-id="9a56b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9a56b-106">Parameters</span></span>

<span data-ttu-id="9a56b-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9a56b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9a56b-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9a56b-108">Return value</span></span>

<span data-ttu-id="9a56b-109">Retorna 2.</span><span class="sxs-lookup"><span data-stu-id="9a56b-109">Returns 2.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a56b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9a56b-110">Remarks</span></span>

<span data-ttu-id="9a56b-111">Esse método substitui o método [**CBaseFilter:: GetPinCount**](cbasefilter-getpincount.md) .</span><span class="sxs-lookup"><span data-stu-id="9a56b-111">This method overrides the [**CBaseFilter::GetPinCount**](cbasefilter-getpincount.md) method.</span></span> <span data-ttu-id="9a56b-112">A classe **CTransformFilter** dá suporte a exatamente um PIN de entrada e um PIN de saída.</span><span class="sxs-lookup"><span data-stu-id="9a56b-112">The **CTransformFilter** class supports exactly one input pin and one output pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="9a56b-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9a56b-113">Requirements</span></span>



| <span data-ttu-id="9a56b-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9a56b-114">Requirement</span></span> | <span data-ttu-id="9a56b-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9a56b-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9a56b-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9a56b-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9a56b-117"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9a56b-117"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9a56b-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9a56b-118">Library</span></span><br/> | <dl> <span data-ttu-id="9a56b-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9a56b-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9a56b-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9a56b-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9a56b-121">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="9a56b-121">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




