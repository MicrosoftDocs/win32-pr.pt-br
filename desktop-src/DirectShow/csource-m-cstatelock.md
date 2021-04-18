---
description: Objeto de seção crítica que protege o estado do filtro. O método auxiliar CSource::p StateLock retorna um ponteiro para essa variável de membro.
ms.assetid: faaf5fea-54bc-4856-9bca-3ed420c491e4
title: 'Membro CSource:: m_cStateLock (Source. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_cStateLock
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 85ff046b7e1f7a0ccfcc41f630785a3e8404e256
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787391"
---
# <a name="csourcem_cstatelock-member"></a><span data-ttu-id="3a486-104">Membro de CSource:: m \_ cStateLock</span><span class="sxs-lookup"><span data-stu-id="3a486-104">CSource::m\_cStateLock member</span></span>

<span data-ttu-id="3a486-105">Objeto de seção crítica que protege o estado do filtro.</span><span class="sxs-lookup"><span data-stu-id="3a486-105">Critical section object that protects the filter state.</span></span> <span data-ttu-id="3a486-106">O método auxiliar [**CSource::P stateLock**](csource--pstatelock.md) retorna um ponteiro para essa variável de membro.</span><span class="sxs-lookup"><span data-stu-id="3a486-106">The [**CSource::pStateLock**](csource--pstatelock.md) helper method returns a pointer to this member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="3a486-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="3a486-107">Syntax</span></span>


```C++
CCritSec m_cStateLock;
```



## <a name="requirements"></a><span data-ttu-id="3a486-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3a486-108">Requirements</span></span>



| <span data-ttu-id="3a486-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="3a486-109">Requirement</span></span> | <span data-ttu-id="3a486-110">Valor</span><span class="sxs-lookup"><span data-stu-id="3a486-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a486-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3a486-111">Header</span></span><br/>  | <dl> <span data-ttu-id="3a486-112"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3a486-112"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="3a486-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3a486-113">Library</span></span><br/> | <dl> <span data-ttu-id="3a486-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3a486-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a486-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="3a486-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a486-116">**Classe CSource**</span><span class="sxs-lookup"><span data-stu-id="3a486-116">**CSource Class**</span></span>](csource.md)
</dt> </dl>

 

 




