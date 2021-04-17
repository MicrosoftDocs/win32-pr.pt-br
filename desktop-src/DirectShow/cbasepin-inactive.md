---
description: O método inativo notifica o PIN de que o filtro não está mais ativo.
ms.assetid: 71847578-2271-4243-87c4-9f14b33f770c
title: Método CBasePin. Inactive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Inactive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 431b243107c365b5d9fda729fff2de80d9193c7c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105755362"
---
# <a name="cbasepininactive-method"></a><span data-ttu-id="51d8f-103">Método CBasePin. Inactive</span><span class="sxs-lookup"><span data-stu-id="51d8f-103">CBasePin.Inactive method</span></span>

<span data-ttu-id="51d8f-104">O `Inactive` método notifica o PIN de que o filtro não está mais ativo.</span><span class="sxs-lookup"><span data-stu-id="51d8f-104">The `Inactive` method notifies the pin that the filter is no longer active.</span></span>

## <a name="syntax"></a><span data-ttu-id="51d8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="51d8f-105">Syntax</span></span>


```C++
virtual HRESULT Inactive();
```



## <a name="parameters"></a><span data-ttu-id="51d8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="51d8f-106">Parameters</span></span>

<span data-ttu-id="51d8f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="51d8f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51d8f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="51d8f-108">Return value</span></span>

<span data-ttu-id="51d8f-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="51d8f-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="51d8f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="51d8f-110">Remarks</span></span>

<span data-ttu-id="51d8f-111">Quando o filtro é interrompido, a classe [**CBaseFilter**](cbasefilter.md) chama esse método em todos os Pins conectados do filtro.</span><span class="sxs-lookup"><span data-stu-id="51d8f-111">When the filter stops, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="51d8f-112">Esse método não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="51d8f-112">This method does nothing in the base class.</span></span> <span data-ttu-id="51d8f-113">Classes derivadas devem substituir esse método para liberar todos os recursos obtidos pelo método [**CBasePin:: active**](cbasepin-active.md) ; por exemplo, para desconfirmar os alocadores do PIN.</span><span class="sxs-lookup"><span data-stu-id="51d8f-113">Derived classes should override this method to free any resources obtained by the [**CBasePin::Active**](cbasepin-active.md) method; for example, to decommit the pin's allocators.</span></span>

<span data-ttu-id="51d8f-114">O estado interno do Gerenciador de grafo de filtro não é atualizado até que esse método retorne, portanto, não teste o estado desse método.</span><span class="sxs-lookup"><span data-stu-id="51d8f-114">The filter graph manager's internal state is not updated until after this method returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="51d8f-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="51d8f-115">Requirements</span></span>



| <span data-ttu-id="51d8f-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="51d8f-116">Requirement</span></span> | <span data-ttu-id="51d8f-117">Valor</span><span class="sxs-lookup"><span data-stu-id="51d8f-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="51d8f-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="51d8f-118">Header</span></span><br/>  | <dl> <span data-ttu-id="51d8f-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="51d8f-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="51d8f-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="51d8f-120">Library</span></span><br/> | <dl> <span data-ttu-id="51d8f-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="51d8f-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="51d8f-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="51d8f-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="51d8f-123">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="51d8f-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




