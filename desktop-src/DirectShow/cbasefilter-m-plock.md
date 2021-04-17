---
description: Ponteiro para uma seção crítica que é usada para serializar alterações de estado.
ms.assetid: 4fecd9a6-54df-49d7-bf2f-5dcaef919ad7
title: 'Membro CBaseFilter:: m_pLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40b2f6ece048fc6463fda0a22792d57839d59e55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752910"
---
# <a name="cbasefilterm_plock-member"></a><span data-ttu-id="ca306-103">Membro de CBaseFilter:: m \_ pLock</span><span class="sxs-lookup"><span data-stu-id="ca306-103">CBaseFilter::m\_pLock member</span></span>

<span data-ttu-id="ca306-104">Ponteiro para uma seção crítica que é usada para serializar alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="ca306-104">Pointer to a critical section that is used to serialize state changes.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca306-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca306-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="remarks"></a><span data-ttu-id="ca306-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca306-106">Remarks</span></span>

<span data-ttu-id="ca306-107">Essa variável é inicializada no construtor da classe; consulte [**CBaseFilter:: CBaseFilter**](cbasefilter-cbasefilter.md).</span><span class="sxs-lookup"><span data-stu-id="ca306-107">This variable is initialized in the class constructor; see [**CBaseFilter::CBaseFilter**](cbasefilter-cbasefilter.md).</span></span>

<span data-ttu-id="ca306-108">Mantenha essa seção crítica durante as transições de estado ou quando um método acessar o estado em várias operações.</span><span class="sxs-lookup"><span data-stu-id="ca306-108">Hold this critical section during state transitions, or when a method accesses the state over several operations.</span></span> <span data-ttu-id="ca306-109">A classe base contém a seção crítica nos seguintes métodos:</span><span class="sxs-lookup"><span data-stu-id="ca306-109">The base class holds the critical section in the following methods:</span></span>

-   [<span data-ttu-id="ca306-110">**CBaseFilter::FindPin**</span><span class="sxs-lookup"><span data-stu-id="ca306-110">**CBaseFilter::FindPin**</span></span>](cbasefilter-findpin.md)
-   [<span data-ttu-id="ca306-111">**CBaseFilter:: getsync**</span><span class="sxs-lookup"><span data-stu-id="ca306-111">**CBaseFilter::GetSyncSource**</span></span>](cbasefilter-getsyncsource.md)
-   [<span data-ttu-id="ca306-112">**CBaseFilter::JoinFilterGraph**</span><span class="sxs-lookup"><span data-stu-id="ca306-112">**CBaseFilter::JoinFilterGraph**</span></span>](cbasefilter-joinfiltergraph.md)
-   [<span data-ttu-id="ca306-113">**CBaseFilter:: IsActive**</span><span class="sxs-lookup"><span data-stu-id="ca306-113">**CBaseFilter::IsActive**</span></span>](cbasefilter-isactive.md)
-   [<span data-ttu-id="ca306-114">**CBaseFilter:: setsincronizate**</span><span class="sxs-lookup"><span data-stu-id="ca306-114">**CBaseFilter::SetSyncSource**</span></span>](cbasefilter-setsyncsource.md)
-   [<span data-ttu-id="ca306-115">**CBaseFilter::P ause**</span><span class="sxs-lookup"><span data-stu-id="ca306-115">**CBaseFilter::Pause**</span></span>](cbasefilter-pause.md)
-   [<span data-ttu-id="ca306-116">**CBaseFilter:: Run**</span><span class="sxs-lookup"><span data-stu-id="ca306-116">**CBaseFilter::Run**</span></span>](cbasefilter-run.md)
-   [<span data-ttu-id="ca306-117">**CBaseFilter:: Stop**</span><span class="sxs-lookup"><span data-stu-id="ca306-117">**CBaseFilter::Stop**</span></span>](cbasefilter-stop.md)

<span data-ttu-id="ca306-118">Não mantenha esta seção crítica durante operações de streaming (isto é, ao entregar amostras a um filtro downstream).</span><span class="sxs-lookup"><span data-stu-id="ca306-118">Do not hold this critical section during streaming operations (that is, when delivering samples to a downstream filter).</span></span> <span data-ttu-id="ca306-119">Serialize operações de streaming usando uma seção crítica diferente.</span><span class="sxs-lookup"><span data-stu-id="ca306-119">Serialize streaming operations using a different critical section.</span></span> <span data-ttu-id="ca306-120">Caso contrário, isso pode causar deadlock.</span><span class="sxs-lookup"><span data-stu-id="ca306-120">Otherwise, it can cause deadlock.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca306-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca306-121">Requirements</span></span>



| <span data-ttu-id="ca306-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca306-122">Requirement</span></span> | <span data-ttu-id="ca306-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ca306-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca306-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca306-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ca306-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca306-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca306-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca306-126">Library</span></span><br/> | <dl> <span data-ttu-id="ca306-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ca306-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ca306-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ca306-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca306-129">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="ca306-129">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> <dt>

[<span data-ttu-id="ca306-130">Threads e seções críticas</span><span class="sxs-lookup"><span data-stu-id="ca306-130">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




