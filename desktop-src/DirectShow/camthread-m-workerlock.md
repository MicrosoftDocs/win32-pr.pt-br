---
description: Seção crítica que bloqueia os dados compartilhados entre threads.
ms.assetid: 87966d7d-6677-462f-93bc-fedda7f0bdcf
title: 'Membro CAMThread:: m_WorkerLock (Wxutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_WorkerLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fce6c2ff2a7857f6cb69ce3bb92fe2b6f24bcbf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779858"
---
# <a name="camthreadm_workerlock-member"></a><span data-ttu-id="e9007-103">Membro de CAMThread:: m \_ WorkerLock</span><span class="sxs-lookup"><span data-stu-id="e9007-103">CAMThread::m\_WorkerLock member</span></span>

<span data-ttu-id="e9007-104">Seção crítica que bloqueia os dados compartilhados entre threads.</span><span class="sxs-lookup"><span data-stu-id="e9007-104">Critical section that locks data shared among threads.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9007-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="e9007-105">Syntax</span></span>


```C++
CCritSec m_WorkerLock;
```



## <a name="requirements"></a><span data-ttu-id="e9007-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e9007-106">Requirements</span></span>



| <span data-ttu-id="e9007-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="e9007-107">Requirement</span></span> | <span data-ttu-id="e9007-108">Valor</span><span class="sxs-lookup"><span data-stu-id="e9007-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9007-109">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e9007-109">Header</span></span><br/>  | <dl> <span data-ttu-id="e9007-110"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e9007-110"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e9007-111">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e9007-111">Library</span></span><br/> | <dl> <span data-ttu-id="e9007-112"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e9007-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e9007-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="e9007-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9007-114">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="e9007-114">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




