---
description: O método OutputPin recupera um ponteiro para o pino de saída do filtro.
ms.assetid: 8c8c125e-553d-43c5-bc63-a0c7d5b01260
title: Método CTransInPlaceFilter. OutputPin (TRANSip. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransInPlaceFilter.OutputPin
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d4e74708062d66c8678af9541df762103ae36537
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778442"
---
# <a name="ctransinplacefilteroutputpin-method"></a><span data-ttu-id="374be-103">Método CTransInPlaceFilter. OutputPin</span><span class="sxs-lookup"><span data-stu-id="374be-103">CTransInPlaceFilter.OutputPin method</span></span>

<span data-ttu-id="374be-104">O `OutputPin` método recupera um ponteiro para o pino de saída do filtro.</span><span class="sxs-lookup"><span data-stu-id="374be-104">The `OutputPin` method retrieves a pointer to the filter's output pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="374be-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="374be-105">Syntax</span></span>


```C++
CTransInPlaceOutputPin* OutputPin();
```



## <a name="parameters"></a><span data-ttu-id="374be-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="374be-106">Parameters</span></span>

<span data-ttu-id="374be-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="374be-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="374be-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="374be-108">Return value</span></span>

<span data-ttu-id="374be-109">Retorna a variável de membro [**CTransformFilter:: m \_ pOutput**](ctransformfilter-m-poutput.md) .</span><span class="sxs-lookup"><span data-stu-id="374be-109">Returns the [**CTransformFilter::m\_pOutput**](ctransformfilter-m-poutput.md) member variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="374be-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="374be-110">Requirements</span></span>



| <span data-ttu-id="374be-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="374be-111">Requirement</span></span> | <span data-ttu-id="374be-112">Valor</span><span class="sxs-lookup"><span data-stu-id="374be-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="374be-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="374be-113">Header</span></span><br/>  | <dl> <span data-ttu-id="374be-114"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="374be-114"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="374be-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="374be-115">Library</span></span><br/> | <dl> <span data-ttu-id="374be-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="374be-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="374be-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="374be-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="374be-118">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="374be-118">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




