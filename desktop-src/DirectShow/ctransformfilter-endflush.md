---
description: O método EndFlush termina uma operação de liberação.
ms.assetid: ebb6beec-84e2-49a7-9771-bbd191faada7
title: Método CTransformFilter. EndFlush (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 348675f1369ec9b0deb5415ad14a864a8befef73
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751677"
---
# <a name="ctransformfilterendflush-method"></a><span data-ttu-id="9dc8c-103">Método CTransformFilter. EndFlush</span><span class="sxs-lookup"><span data-stu-id="9dc8c-103">CTransformFilter.EndFlush method</span></span>

<span data-ttu-id="9dc8c-104">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-104">The `EndFlush` method ends a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="9dc8c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9dc8c-105">Syntax</span></span>


```C++
virtual HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="9dc8c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9dc8c-106">Parameters</span></span>

<span data-ttu-id="9dc8c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9dc8c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9dc8c-108">Return value</span></span>

<span data-ttu-id="9dc8c-109">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="9dc8c-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="9dc8c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9dc8c-110">Remarks</span></span>

<span data-ttu-id="9dc8c-111">No final de uma operação de liberação, o método [**CTransformInputPin:: EndFlush**](ctransforminputpin-endflush.md) do pino de entrada chama esse método.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-111">At the end of a flush operation, the input pin's [**CTransformInputPin::EndFlush**](ctransforminputpin-endflush.md) method calls this method.</span></span> <span data-ttu-id="9dc8c-112">Esse método passa a `EndFlush` chamada downstream.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-112">This method passes the `EndFlush` call downstream.</span></span>

<span data-ttu-id="9dc8c-113">Se a classe derivada usar um thread de trabalho para fornecer amostras, ela deverá descartar todos os dados na fila antes de enviar a `EndFlush` chamada downstream.</span><span class="sxs-lookup"><span data-stu-id="9dc8c-113">If the derived class uses a worker thread to deliver samples, it must discard any queued data before sending the `EndFlush` call downstream.</span></span> <span data-ttu-id="9dc8c-114">Para obter mais informações, consulte [fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="9dc8c-114">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="9dc8c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9dc8c-115">Requirements</span></span>



| <span data-ttu-id="9dc8c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9dc8c-116">Requirement</span></span> | <span data-ttu-id="9dc8c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9dc8c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9dc8c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9dc8c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9dc8c-119"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9dc8c-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9dc8c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9dc8c-120">Library</span></span><br/> | <dl> <span data-ttu-id="9dc8c-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9dc8c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9dc8c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9dc8c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9dc8c-123">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="9dc8c-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




