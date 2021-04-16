---
description: 'Matriz de amostras de tamanho COutputQueue:: m \_ lBatchSize.'
ms.assetid: 5c4b904d-480b-4393-a799-63989669ea1c
title: 'Membro COutputQueue:: m_ppSamples (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_ppSamples
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3659c4a71cacb839caaa1b6ac89e46cd4e42a249
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754150"
---
# <a name="coutputqueuem_ppsamples-member"></a><span data-ttu-id="96e67-103">Membro de COutputQueue:: m \_ ppSamples</span><span class="sxs-lookup"><span data-stu-id="96e67-103">COutputQueue::m\_ppSamples member</span></span>

<span data-ttu-id="96e67-104">Matriz de amostras de tamanho [**COutputQueue:: m \_ lBatchSize**](coutputqueue-m-lbatchsize.md).</span><span class="sxs-lookup"><span data-stu-id="96e67-104">Array of samples of size [**COutputQueue::m\_lBatchSize**](coutputqueue-m-lbatchsize.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="96e67-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="96e67-105">Syntax</span></span>


```C++
IMediaSample **m_ppSamples;
```



## <a name="remarks"></a><span data-ttu-id="96e67-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="96e67-106">Remarks</span></span>

<span data-ttu-id="96e67-107">O thread de trabalho extrai amostras da fila e as coloca nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="96e67-107">The worker thread pulls samples from the queue and places them in this array.</span></span> <span data-ttu-id="96e67-108">Ele passa a matriz para o método [**IMemInputPin:: ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) .</span><span class="sxs-lookup"><span data-stu-id="96e67-108">It passes the array to the [**IMemInputPin::ReceiveMultiple**](/windows/desktop/api/Strmif/nf-strmif-imeminputpin-receivemultiple) method.</span></span> <span data-ttu-id="96e67-109">Se o objeto não estiver usando um thread de trabalho, o objeto colocará amostras diretamente nessa matriz.</span><span class="sxs-lookup"><span data-stu-id="96e67-109">If the object is not using a worker thread, the object places samples directly into this array.</span></span> <span data-ttu-id="96e67-110">A variável de membro da [**\_ lista COutputQueue:: m**](coutputqueue-m-list.md) contém a fila.</span><span class="sxs-lookup"><span data-stu-id="96e67-110">The [**COutputQueue::m\_List**](coutputqueue-m-list.md) member variable holds the queue.</span></span>

## <a name="requirements"></a><span data-ttu-id="96e67-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="96e67-111">Requirements</span></span>



| <span data-ttu-id="96e67-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="96e67-112">Requirement</span></span> | <span data-ttu-id="96e67-113">Valor</span><span class="sxs-lookup"><span data-stu-id="96e67-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="96e67-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="96e67-114">Header</span></span><br/>  | <dl> <span data-ttu-id="96e67-115"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="96e67-115"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="96e67-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="96e67-116">Library</span></span><br/> | <dl> <span data-ttu-id="96e67-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="96e67-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="96e67-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="96e67-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="96e67-119">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="96e67-119">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




