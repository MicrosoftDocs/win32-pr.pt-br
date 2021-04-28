---
description: Método COutputQueue. BeginFlush-o método BeginFlush inicia uma operação de liberação.
ms.assetid: d37b611e-742f-4bdf-bd72-a91cd1c473b3
title: Método COutputQueue. BeginFlush (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e7c6168daf766ec11e18e86673d9d25542b50462
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099024"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="e1d10-103">Método COutputQueue. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="e1d10-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="e1d10-104">O `BeginFlush` método inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="e1d10-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e1d10-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e1d10-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="e1d10-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e1d10-106">Parameters</span></span>

<span data-ttu-id="e1d10-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e1d10-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e1d10-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e1d10-108">Return value</span></span>

<span data-ttu-id="e1d10-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="e1d10-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="e1d10-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e1d10-110">Remarks</span></span>

<span data-ttu-id="e1d10-111">Esse método define a variável de membro [**COutputQueue:: m \_ BFlushing**](coutputqueue-m-bflushing.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="e1d10-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="e1d10-112">Se o objeto estiver usando um thread, o thread chamará o método [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) para liberar quaisquer amostras pendentes.</span><span class="sxs-lookup"><span data-stu-id="e1d10-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="e1d10-113">Caso contrário, o objeto chamará **FreeSamples** durante o método [**COutputQueue:: EndFlush**](coutputqueue-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="e1d10-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="e1d10-114">Esse método também define a variável de membro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) como S \_ false, o que faz com que o objeto descarte todas as novas amostras.</span><span class="sxs-lookup"><span data-stu-id="e1d10-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="e1d10-115">O objeto passa o downstream de notificação de liberação chamando o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="e1d10-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="e1d10-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e1d10-116">Requirements</span></span>



| <span data-ttu-id="e1d10-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="e1d10-117">Requirement</span></span> | <span data-ttu-id="e1d10-118">Valor</span><span class="sxs-lookup"><span data-stu-id="e1d10-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e1d10-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e1d10-119">Header</span></span><br/>  | <dl> <span data-ttu-id="e1d10-120"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e1d10-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e1d10-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e1d10-121">Library</span></span><br/> | <dl> <span data-ttu-id="e1d10-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e1d10-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e1d10-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e1d10-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e1d10-124">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="e1d10-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




