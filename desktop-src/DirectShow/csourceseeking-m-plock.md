---
description: Ponteiro para um objeto de seção crítica.
ms.assetid: dc791bc4-857c-4a79-9aa8-3c5974c23483
title: 'Membro CSourceSeeking:: m_pLock (Ctlutil. h)'
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
ms.openlocfilehash: 2f8de9159e917d24701635a428e0f5e6a1b9cb55
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758070"
---
# <a name="csourceseekingm_plock-member"></a><span data-ttu-id="2e87f-103">Membro de CSourceSeeking:: m \_ pLock</span><span class="sxs-lookup"><span data-stu-id="2e87f-103">CSourceSeeking::m\_pLock member</span></span>

<span data-ttu-id="2e87f-104">Ponteiro para um objeto de seção crítica.</span><span class="sxs-lookup"><span data-stu-id="2e87f-104">Pointer to a critical section object.</span></span> <span data-ttu-id="2e87f-105">A `CSourceSeeking` classe usa essa seção crítica para sincronizar o acesso às horas de início e parada, à duração e às variáveis de taxa.</span><span class="sxs-lookup"><span data-stu-id="2e87f-105">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and rate variables.</span></span> <span data-ttu-id="2e87f-106">Essa variável é inicializada no método do Construtor; consulte [**CSourceSeeking:: CSourceSeeking**](csourceseeking-csourceseeking.md).</span><span class="sxs-lookup"><span data-stu-id="2e87f-106">This variable is initialized in the constructor method; see [**CSourceSeeking::CSourceSeeking**](csourceseeking-csourceseeking.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="2e87f-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2e87f-107">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="2e87f-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2e87f-108">Requirements</span></span>



| <span data-ttu-id="2e87f-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="2e87f-109">Requirement</span></span> | <span data-ttu-id="2e87f-110">Valor</span><span class="sxs-lookup"><span data-stu-id="2e87f-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2e87f-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2e87f-111">Header</span></span><br/>  | <dl> <span data-ttu-id="2e87f-112"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2e87f-112"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2e87f-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2e87f-113">Library</span></span><br/> | <dl> <span data-ttu-id="2e87f-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2e87f-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2e87f-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="2e87f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2e87f-116">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="2e87f-116">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




