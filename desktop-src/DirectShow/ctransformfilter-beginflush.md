---
description: Método CTransformFilter. BeginFlush-o método BeginFlush inicia uma operação de liberação.
ms.assetid: 15bea993-f862-4791-b784-0d0468c6c05c
title: Método CTransformFilter. BeginFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3bd7735726d7e7d21bc16e8a811947b954ffaac4
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085154"
---
# <a name="ctransformfilterbeginflush-method"></a><span data-ttu-id="eb3f7-103">Método CTransformFilter. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="eb3f7-103">CTransformFilter.BeginFlush method</span></span>

<span data-ttu-id="eb3f7-104">O `BeginFlush` método inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb3f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb3f7-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="eb3f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb3f7-106">Parameters</span></span>

<span data-ttu-id="eb3f7-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="eb3f7-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="eb3f7-108">Return value</span></span>

<span data-ttu-id="eb3f7-109">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb3f7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb3f7-110">Remarks</span></span>

<span data-ttu-id="eb3f7-111">No início de uma operação de liberação, o método [**CTransformInputPin:: BeginFlush**](ctransforminputpin-beginflush.md) do pino de entrada chama esse método.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-111">At the start of a flush operation, the input pin's [**CTransformInputPin::BeginFlush**](ctransforminputpin-beginflush.md) method calls this method.</span></span> <span data-ttu-id="eb3f7-112">Esse método passa a `BeginFlush` chamada downstream.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-112">This method passes the `BeginFlush` call downstream.</span></span>

<span data-ttu-id="eb3f7-113">Se a classe derivada usar um thread de trabalho para fornecer amostras, ela deverá descartar todos os dados na fila durante uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-113">If the derived class uses a worker thread to deliver samples, it should discard any queued data during a flush operation.</span></span> <span data-ttu-id="eb3f7-114">Isso pode ser feito no `BeginFlush` método ou no método [**EndFlush**](ctransformfilter-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-114">That can be done either in the `BeginFlush` method, or in the [**EndFlush**](ctransformfilter-endflush.md) method.</span></span> <span data-ttu-id="eb3f7-115">No entanto, observe que `BeginFlush` as chamadas para não estão sincronizadas com o thread de streaming.</span><span class="sxs-lookup"><span data-stu-id="eb3f7-115">However, note that calls to `BeginFlush` are not synchronized with the streaming thread.</span></span> <span data-ttu-id="eb3f7-116">Se o `BeginFlush` método descartar os dados na fila, o filtro deverá ter cuidado para não processar mais dados entre as `BeginFlush` chamadas e **EndFlush** .</span><span class="sxs-lookup"><span data-stu-id="eb3f7-116">If the `BeginFlush` method discards the queued data, the filter must be careful not to process any more data between the `BeginFlush` and **EndFlush** calls.</span></span> <span data-ttu-id="eb3f7-117">Para obter mais informações, consulte [fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="eb3f7-117">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="eb3f7-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb3f7-118">Requirements</span></span>



| <span data-ttu-id="eb3f7-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb3f7-119">Requirement</span></span> | <span data-ttu-id="eb3f7-120">Valor</span><span class="sxs-lookup"><span data-stu-id="eb3f7-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb3f7-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb3f7-121">Header</span></span><br/>  | <dl> <span data-ttu-id="eb3f7-122"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb3f7-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb3f7-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb3f7-123">Library</span></span><br/> | <dl> <span data-ttu-id="eb3f7-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eb3f7-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb3f7-125">Consulte também</span><span class="sxs-lookup"><span data-stu-id="eb3f7-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb3f7-126">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="eb3f7-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




