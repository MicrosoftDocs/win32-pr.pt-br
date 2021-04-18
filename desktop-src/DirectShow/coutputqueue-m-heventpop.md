---
description: 'Evento opcional sinalizado sempre que o objeto remove um exemplo da fila. O valor é inicialmente nulo. Chame o método COutputQueue:: SetPopEvent para especificar um identificador de evento.'
ms.assetid: f2602532-b045-4384-b87c-b28cc34c81b0
title: 'Membro COutputQueue:: m_hEventPop (Outputq. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_hEventPop
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 88ab5235a3d4df5b60b53279c444ae99b12fe0c5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759308"
---
# <a name="coutputqueuem_heventpop-member"></a><span data-ttu-id="63e08-105">Membro de COutputQueue:: m \_ hEventPop</span><span class="sxs-lookup"><span data-stu-id="63e08-105">COutputQueue::m\_hEventPop member</span></span>

<span data-ttu-id="63e08-106">Evento opcional sinalizado sempre que o objeto remove um exemplo da fila.</span><span class="sxs-lookup"><span data-stu-id="63e08-106">Optional event that is signaled whenever the object removes a sample from the queue.</span></span> <span data-ttu-id="63e08-107">O valor é inicialmente **nulo**.</span><span class="sxs-lookup"><span data-stu-id="63e08-107">The value is initially **NULL**.</span></span> <span data-ttu-id="63e08-108">Chame o método [**COutputQueue:: SetPopEvent**](coutputqueue-setpopevent.md) para especificar um identificador de evento.</span><span class="sxs-lookup"><span data-stu-id="63e08-108">Call the [**COutputQueue::SetPopEvent**](coutputqueue-setpopevent.md) method to specify an event handle.</span></span>

## <a name="syntax"></a><span data-ttu-id="63e08-109">Syntax</span><span class="sxs-lookup"><span data-stu-id="63e08-109">Syntax</span></span>


```C++
HANDLE m_hEventPop;
```



## <a name="requirements"></a><span data-ttu-id="63e08-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="63e08-110">Requirements</span></span>



| <span data-ttu-id="63e08-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="63e08-111">Requirement</span></span> | <span data-ttu-id="63e08-112">Valor</span><span class="sxs-lookup"><span data-stu-id="63e08-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="63e08-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="63e08-113">Header</span></span><br/>  | <dl> <span data-ttu-id="63e08-114"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="63e08-114"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="63e08-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="63e08-115">Library</span></span><br/> | <dl> <span data-ttu-id="63e08-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="63e08-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="63e08-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="63e08-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="63e08-118">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="63e08-118">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




