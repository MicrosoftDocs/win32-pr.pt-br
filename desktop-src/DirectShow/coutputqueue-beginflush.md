---
description: O método BeginFlush inicia uma operação de liberação.
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
ms.openlocfilehash: 462c3027e38bd94f061eb927c0d52576e29c997b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753166"
---
# <a name="coutputqueuebeginflush-method"></a><span data-ttu-id="c3f1c-103">Método COutputQueue. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="c3f1c-103">COutputQueue.BeginFlush method</span></span>

<span data-ttu-id="c3f1c-104">O `BeginFlush` método inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="c3f1c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c3f1c-105">Syntax</span></span>


```C++
void BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="c3f1c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c3f1c-106">Parameters</span></span>

<span data-ttu-id="c3f1c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="c3f1c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="c3f1c-108">Return value</span></span>

<span data-ttu-id="c3f1c-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c3f1c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="c3f1c-110">Remarks</span></span>

<span data-ttu-id="c3f1c-111">Esse método define a variável de membro [**COutputQueue:: m \_ BFlushing**](coutputqueue-m-bflushing.md) como **true**.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-111">This method sets the [**COutputQueue::m\_bFlushing**](coutputqueue-m-bflushing.md) member variable to **TRUE**.</span></span> <span data-ttu-id="c3f1c-112">Se o objeto estiver usando um thread, o thread chamará o método [**COutputQueue:: FreeSamples**](coutputqueue-freesamples.md) para liberar quaisquer amostras pendentes.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-112">If the object is using a thread, the thread calls the [**COutputQueue::FreeSamples**](coutputqueue-freesamples.md) method to free any pending samples.</span></span> <span data-ttu-id="c3f1c-113">Caso contrário, o objeto chamará **FreeSamples** durante o método [**COutputQueue:: EndFlush**](coutputqueue-endflush.md) .</span><span class="sxs-lookup"><span data-stu-id="c3f1c-113">Otherwise, the object calls **FreeSamples** during the [**COutputQueue::EndFlush**](coutputqueue-endflush.md) method.</span></span> <span data-ttu-id="c3f1c-114">Esse método também define a variável de membro [**COutputQueue:: m \_ HR**](coutputqueue-m-hr.md) como S \_ false, o que faz com que o objeto descarte todas as novas amostras.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-114">This method also sets the [**COutputQueue::m\_hr**](coutputqueue-m-hr.md) member variable to S\_FALSE, which causes the object to discard all new samples.</span></span>

<span data-ttu-id="c3f1c-115">O objeto passa o downstream de notificação de liberação chamando o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="c3f1c-115">The object passes the flush notification downstream by calling the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="c3f1c-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c3f1c-116">Requirements</span></span>



| <span data-ttu-id="c3f1c-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c3f1c-117">Requirement</span></span> | <span data-ttu-id="c3f1c-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c3f1c-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c3f1c-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c3f1c-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c3f1c-120"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f1c-120"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="c3f1c-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c3f1c-121">Library</span></span><br/> | <dl> <span data-ttu-id="c3f1c-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c3f1c-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c3f1c-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="c3f1c-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c3f1c-124">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="c3f1c-124">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




