---
description: Sinalizador que indica se a amostra mais recente foi descartada. Se o método Receive descartar um exemplo, ele definirá o valor como TRUE.
ms.assetid: 6143f948-75b0-47c6-9951-4c18c0773857
title: 'Membro CTransformFilter:: m_bSampleSkipped (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bSampleSkipped
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 61d8ceda20fed4c8ec89538cbe9675ad1f3e4549
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747372"
---
# <a name="ctransformfilterm_bsampleskipped-member"></a><span data-ttu-id="d159d-104">Membro de CTransformFilter:: m \_ bSampleSkipped</span><span class="sxs-lookup"><span data-stu-id="d159d-104">CTransformFilter::m\_bSampleSkipped member</span></span>

<span data-ttu-id="d159d-105">Sinalizador que indica se a amostra mais recente foi descartada.</span><span class="sxs-lookup"><span data-stu-id="d159d-105">Flag that indicates whether the most recent sample was dropped.</span></span> <span data-ttu-id="d159d-106">Se o método [**Receive**](ctransformfilter-receive.md) descartar um exemplo, ele definirá o valor como **true**.</span><span class="sxs-lookup"><span data-stu-id="d159d-106">If the [**Receive**](ctransformfilter-receive.md) method drops a sample, it sets the value to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="d159d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d159d-107">Syntax</span></span>


```C++
BOOL m_bSampleSkipped;
```



## <a name="requirements"></a><span data-ttu-id="d159d-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d159d-108">Requirements</span></span>



| <span data-ttu-id="d159d-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="d159d-109">Requirement</span></span> | <span data-ttu-id="d159d-110">Valor</span><span class="sxs-lookup"><span data-stu-id="d159d-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d159d-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d159d-111">Header</span></span><br/>  | <dl> <span data-ttu-id="d159d-112"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d159d-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d159d-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d159d-113">Library</span></span><br/> | <dl> <span data-ttu-id="d159d-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d159d-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d159d-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="d159d-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d159d-116">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="d159d-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




