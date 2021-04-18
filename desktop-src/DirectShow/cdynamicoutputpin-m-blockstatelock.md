---
description: Seção crítica que protege o estado de bloqueio.
ms.assetid: 6d20cf4c-2c27-41e6-8d01-6cb5e3876a38
title: 'Membro CDynamicOutputPin:: m_BlockStateLock (Amfilter. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_BlockStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 56d9175342218e8b82698fe9b89d15937d6913e1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752497"
---
# <a name="cdynamicoutputpinm_blockstatelock-member"></a><span data-ttu-id="a7d7b-103">Membro de CDynamicOutputPin:: m \_ BlockStateLock</span><span class="sxs-lookup"><span data-stu-id="a7d7b-103">CDynamicOutputPin::m\_BlockStateLock member</span></span>

<span data-ttu-id="a7d7b-104">Seção crítica que protege o estado de bloqueio.</span><span class="sxs-lookup"><span data-stu-id="a7d7b-104">Critical section that protects the blocking state.</span></span>

## <a name="syntax"></a><span data-ttu-id="a7d7b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a7d7b-105">Syntax</span></span>


```C++
CCritSec m_BlockStateLock;
```



## <a name="remarks"></a><span data-ttu-id="a7d7b-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="a7d7b-106">Remarks</span></span>

<span data-ttu-id="a7d7b-107">Mantenha esta seção crítica antes de usar qualquer uma das seguintes variáveis de membro:</span><span class="sxs-lookup"><span data-stu-id="a7d7b-107">Hold this critical section before using any of the following member variables:</span></span>

-   [<span data-ttu-id="a7d7b-108">**CDynamicOutputPin:: m \_ blockstate**</span><span class="sxs-lookup"><span data-stu-id="a7d7b-108">**CDynamicOutputPin::m\_BlockState**</span></span>](cdynamicoutputpin-m-blockstate.md)
-   [<span data-ttu-id="a7d7b-109">**CDynamicOutputPin:: m \_ dwBlockCallerThreadID**</span><span class="sxs-lookup"><span data-stu-id="a7d7b-109">**CDynamicOutputPin::m\_dwBlockCallerThreadID**</span></span>](cdynamicoutputpin-m-dwblockcallerthreadid.md)
-   [<span data-ttu-id="a7d7b-110">**CDynamicOutputPin:: m \_ dwNumOutstandingOutputPinUsers**</span><span class="sxs-lookup"><span data-stu-id="a7d7b-110">**CDynamicOutputPin::m\_dwNumOutstandingOutputPinUsers**</span></span>](cdynamicoutputpin-m-dwnumoutstandingoutputpinusers.md)
-   [<span data-ttu-id="a7d7b-111">**CDynamicOutputPin:: m \_ hNotifyCallerPinBlockedEvent**</span><span class="sxs-lookup"><span data-stu-id="a7d7b-111">**CDynamicOutputPin::m\_hNotifyCallerPinBlockedEvent**</span></span>](cdynamicoutputpin-m-hnotifycallerpinblockedevent.md)

## <a name="requirements"></a><span data-ttu-id="a7d7b-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a7d7b-112">Requirements</span></span>



| <span data-ttu-id="a7d7b-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="a7d7b-113">Requirement</span></span> | <span data-ttu-id="a7d7b-114">Valor</span><span class="sxs-lookup"><span data-stu-id="a7d7b-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a7d7b-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a7d7b-115">Header</span></span><br/>  | <dl> <span data-ttu-id="a7d7b-116"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d7b-116"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a7d7b-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a7d7b-117">Library</span></span><br/> | <dl> <span data-ttu-id="a7d7b-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a7d7b-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a7d7b-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="a7d7b-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a7d7b-120">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="a7d7b-120">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




