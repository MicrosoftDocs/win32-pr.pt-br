---
description: Ponteiro para um objeto de seção crítica que protege o estado do filtro.
ms.assetid: e733360d-ed95-493f-a85b-53d584681f60
title: 'Membro CBasePin:: m_pLock (Amfilter. h)'
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
ms.openlocfilehash: 0a18755c1ea1c5c29b9839ecaf8803a84f8c8f10
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749259"
---
# <a name="cbasepinm_plock-member"></a><span data-ttu-id="cbc1a-103">Membro de CBasePin:: m \_ pLock</span><span class="sxs-lookup"><span data-stu-id="cbc1a-103">CBasePin::m\_pLock member</span></span>

<span data-ttu-id="cbc1a-104">Ponteiro para um objeto de seção crítica que protege o estado do filtro.</span><span class="sxs-lookup"><span data-stu-id="cbc1a-104">Pointer to a critical section object that protects the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="cbc1a-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="cbc1a-105">Syntax</span></span>


```C++
CCritSec *m_pLock;
```



## <a name="requirements"></a><span data-ttu-id="cbc1a-106">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cbc1a-106">Requirements</span></span>



| <span data-ttu-id="cbc1a-107">Requisito</span><span class="sxs-lookup"><span data-stu-id="cbc1a-107">Requirement</span></span> | <span data-ttu-id="cbc1a-108">Valor</span><span class="sxs-lookup"><span data-stu-id="cbc1a-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cbc1a-109">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cbc1a-109">Header</span></span><br/>  | <dl> <span data-ttu-id="cbc1a-110"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc1a-110"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="cbc1a-111">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cbc1a-111">Library</span></span><br/> | <dl> <span data-ttu-id="cbc1a-112"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cbc1a-112"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cbc1a-113">Confira também</span><span class="sxs-lookup"><span data-stu-id="cbc1a-113">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cbc1a-114">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="cbc1a-114">**CBasePin Class**</span></span>](cbasepin.md)
</dt> <dt>

[<span data-ttu-id="cbc1a-115">Threads e seções críticas</span><span class="sxs-lookup"><span data-stu-id="cbc1a-115">Threads and Critical Sections</span></span>](threads-and-critical-sections.md)
</dt> </dl>

 

 




