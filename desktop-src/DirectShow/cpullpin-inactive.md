---
description: O método inativo desliga o thread de trabalho que efetua pull dos dados do pino de saída. Esse método também desconfirma o alocador.
ms.assetid: 90b91686-b9a8-4196-b559-de924334f11c
title: Método CPullPin. Inactive (Pullpin. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CPullPin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4f32084428a36032152d3c3297b1fc9419e51cb3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754977"
---
# <a name="cpullpininactive-method"></a><span data-ttu-id="c882b-104">Método CPullPin. Inactive</span><span class="sxs-lookup"><span data-stu-id="c882b-104">CPullPin.Inactive method</span></span>

<span data-ttu-id="c882b-105">O `Inactive` método desliga o thread de trabalho que efetua pull dos dados do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="c882b-105">The `Inactive` method shuts down the worker thread that pulls data from the output pin.</span></span> <span data-ttu-id="c882b-106">Esse método também desconfirma o alocador.</span><span class="sxs-lookup"><span data-stu-id="c882b-106">This method also decommits the allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="c882b-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c882b-107">Syntax</span></span>


```C++
HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="c882b-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c882b-108">Parameters</span></span>

<span data-ttu-id="c882b-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c882b-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c882b-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c882b-110">Return value</span></span>

<span data-ttu-id="c882b-111">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="c882b-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="c882b-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="c882b-112">Remarks</span></span>

<span data-ttu-id="c882b-113">Chame esse método quando o filtro proprietário se tornar inativo.</span><span class="sxs-lookup"><span data-stu-id="c882b-113">Call this method when the owning filter becomes inactive.</span></span> <span data-ttu-id="c882b-114">(Se o PIN de entrada deriva de [**CBasePin**](cbasepin.md), substitua o método [**CBasePin:: Inactive**](cbasepin-inactive.md) .)</span><span class="sxs-lookup"><span data-stu-id="c882b-114">(If your input pin derives from [**CBasePin**](cbasepin.md), override the [**CBasePin::Inactive**](cbasepin-inactive.md) method.)</span></span>

## <a name="requirements"></a><span data-ttu-id="c882b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c882b-115">Requirements</span></span>



| <span data-ttu-id="c882b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="c882b-116">Requirement</span></span> | <span data-ttu-id="c882b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="c882b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c882b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c882b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="c882b-119"><dt>Pullpin. h</dt></span><span class="sxs-lookup"><span data-stu-id="c882b-119"><dt>Pullpin.h</dt></span></span> </dl>                                                                                                       |
| <span data-ttu-id="c882b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c882b-120">Library</span></span><br/> | <dl> <span data-ttu-id="c882b-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c882b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c882b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="c882b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c882b-123">**Classe CPullPin**</span><span class="sxs-lookup"><span data-stu-id="c882b-123">**CPullPin Class**</span></span>](cpullpin.md)
</dt> </dl>

 

 




