---
description: Seção crítica que impede que o thread seja acessado por outros threads.
ms.assetid: 9bc360be-52d6-4db1-b384-8bc9e25c0914
title: 'Membro CAMThread:: m_AccessLock (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_AccessLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6edb4b58b630cfdcfd6eefc43b908cf6aeb0f084
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757899"
---
# <a name="camthreadm_accesslock-member"></a><span data-ttu-id="68b3b-103">Membro de CAMThread:: m \_ AccessLock</span><span class="sxs-lookup"><span data-stu-id="68b3b-103">CAMThread::m\_AccessLock member</span></span>

<span data-ttu-id="68b3b-104">Seção crítica que impede que o thread seja acessado por outros threads.</span><span class="sxs-lookup"><span data-stu-id="68b3b-104">Critical section that locks the thread from being accessed by other threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="68b3b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="68b3b-105">Syntax</span></span>


```C++
CCritSec m_AccessLock;
```



## <a name="remarks"></a><span data-ttu-id="68b3b-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="68b3b-106">Remarks</span></span>

<span data-ttu-id="68b3b-107">Os métodos [**CAMThread:: Create**](camthread-create.md) e [**CAMThread:: CallWorker**](camthread-callworker.md) mantêm esse bloqueio para serializar operações no thread.</span><span class="sxs-lookup"><span data-stu-id="68b3b-107">The [**CAMThread::Create**](camthread-create.md) and [**CAMThread::CallWorker**](camthread-callworker.md) methods hold this lock, to serialize operations on the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="68b3b-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="68b3b-108">Requirements</span></span>



| <span data-ttu-id="68b3b-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="68b3b-109">Requirement</span></span> | <span data-ttu-id="68b3b-110">Valor</span><span class="sxs-lookup"><span data-stu-id="68b3b-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="68b3b-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="68b3b-111">Header</span></span><br/>  | <dl> <span data-ttu-id="68b3b-112"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="68b3b-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="68b3b-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="68b3b-113">Library</span></span><br/> | <dl> <span data-ttu-id="68b3b-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="68b3b-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="68b3b-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="68b3b-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68b3b-116">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="68b3b-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




