---
description: 'O método EndOfStream notifica o PIN de que nenhum dado adicional é esperado. Esse método implementa o método IPin:: EndOfStream. Chame esse método somente em Pins de entrada.'
ms.assetid: 52a71c30-bd68-4152-8901-71ef2e65913a
title: Método CBasePin. EndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2324bae8ec1266dce2471049f8ba2f06b0c9e6e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769243"
---
# <a name="cbasepinendofstream-method"></a><span data-ttu-id="667e5-105">Método CBasePin. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="667e5-105">CBasePin.EndOfStream method</span></span>

<span data-ttu-id="667e5-106">O `EndOfStream` método notifica o PIN de que nenhum dado adicional é esperado.</span><span class="sxs-lookup"><span data-stu-id="667e5-106">The `EndOfStream` method notifies the pin that no additional data is expected.</span></span> <span data-ttu-id="667e5-107">Esse método implementa o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) .</span><span class="sxs-lookup"><span data-stu-id="667e5-107">This method implements the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method.</span></span> <span data-ttu-id="667e5-108">Chame esse método somente em Pins de entrada.</span><span class="sxs-lookup"><span data-stu-id="667e5-108">Call this method only on input pins.</span></span>

## <a name="syntax"></a><span data-ttu-id="667e5-109">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="667e5-109">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="667e5-110">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="667e5-110">Parameters</span></span>

<span data-ttu-id="667e5-111">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="667e5-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="667e5-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="667e5-112">Return value</span></span>

<span data-ttu-id="667e5-113">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="667e5-113">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="667e5-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="667e5-114">Remarks</span></span>

<span data-ttu-id="667e5-115">O filtro deve passar notificações de fim de fluxo downstream para os Pins de entrada dos filtros conectados.</span><span class="sxs-lookup"><span data-stu-id="667e5-115">The filter should pass end-of-stream notifications downstream, to the input pins of connected filters.</span></span> <span data-ttu-id="667e5-116">Se o filtro for um renderizador, ele deverá lançar uma notificação de evento do [**EC \_ Complete**](ec-complete.md) para o Gerenciador do grafo de filtro.</span><span class="sxs-lookup"><span data-stu-id="667e5-116">If the filter is a renderer, it should post an [**EC\_COMPLETE**](ec-complete.md) event notification to the filter graph manager.</span></span> <span data-ttu-id="667e5-117">Para obter mais informações, consulte [fluxo de dados no grafo de filtro](data-flow-in-the-filter-graph.md).</span><span class="sxs-lookup"><span data-stu-id="667e5-117">For more information, see [Data Flow in the Filter Graph](data-flow-in-the-filter-graph.md).</span></span>

<span data-ttu-id="667e5-118">Na classe base, esse método não faz nada.</span><span class="sxs-lookup"><span data-stu-id="667e5-118">In the base class, this method does nothing.</span></span> <span data-ttu-id="667e5-119">Classes derivadas devem substituir esse método.</span><span class="sxs-lookup"><span data-stu-id="667e5-119">Derived classes should override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="667e5-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="667e5-120">Requirements</span></span>



| <span data-ttu-id="667e5-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="667e5-121">Requirement</span></span> | <span data-ttu-id="667e5-122">Valor</span><span class="sxs-lookup"><span data-stu-id="667e5-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="667e5-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="667e5-123">Header</span></span><br/>  | <dl> <span data-ttu-id="667e5-124"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="667e5-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="667e5-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="667e5-125">Library</span></span><br/> | <dl> <span data-ttu-id="667e5-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="667e5-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="667e5-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="667e5-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="667e5-128">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="667e5-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




