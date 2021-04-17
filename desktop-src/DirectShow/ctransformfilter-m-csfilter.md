---
description: Seção crítica que protege o estado do filtro. Para obter mais informações, consulte fluxo de dados para os desenvolvedores de filtro.
ms.assetid: 75b9c8b0-e911-41fd-8d07-b854dbe25551
title: 'Membro CTransformFilter:: m_csFilter (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csFilter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 991b07aa654ce42a651f4fa169e757d8380fdc8e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752687"
---
# <a name="ctransformfilterm_csfilter-member"></a><span data-ttu-id="c6f1a-104">Membro de CTransformFilter:: m \_ csFilter</span><span class="sxs-lookup"><span data-stu-id="c6f1a-104">CTransformFilter::m\_csFilter member</span></span>

<span data-ttu-id="c6f1a-105">Seção crítica que protege o estado do filtro.</span><span class="sxs-lookup"><span data-stu-id="c6f1a-105">Critical section that protects the filter state.</span></span> <span data-ttu-id="c6f1a-106">Para obter mais informações, consulte [fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="c6f1a-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="c6f1a-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6f1a-107">Syntax</span></span>


```C++
CCritSec m_csFilter;
```



## <a name="requirements"></a><span data-ttu-id="c6f1a-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c6f1a-108">Requirements</span></span>



| <span data-ttu-id="c6f1a-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="c6f1a-109">Requirement</span></span> | <span data-ttu-id="c6f1a-110">Valor</span><span class="sxs-lookup"><span data-stu-id="c6f1a-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c6f1a-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c6f1a-111">Header</span></span><br/>  | <dl> <span data-ttu-id="c6f1a-112"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c6f1a-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c6f1a-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c6f1a-113">Library</span></span><br/> | <dl> <span data-ttu-id="c6f1a-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c6f1a-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="c6f1a-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="c6f1a-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c6f1a-116">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="c6f1a-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




