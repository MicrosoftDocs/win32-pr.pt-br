---
description: Seção crítica que protege o estado de streaming. Para obter mais informações, consulte fluxo de dados para os desenvolvedores de filtro.
ms.assetid: f77c3129-ca25-47b8-8a6e-3a07169701af
title: 'Membro CTransformFilter:: m_csReceive (Transfrm. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_csReceive
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 542f108cee8dbe761040ef8474ae7cec565e0b52
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105766278"
---
# <a name="ctransformfilterm_csreceive-member"></a><span data-ttu-id="9f2c5-104">Membro de CTransformFilter:: m \_ csReceive</span><span class="sxs-lookup"><span data-stu-id="9f2c5-104">CTransformFilter::m\_csReceive member</span></span>

<span data-ttu-id="9f2c5-105">Seção crítica que protege o estado de streaming.</span><span class="sxs-lookup"><span data-stu-id="9f2c5-105">Critical section that protects the streaming state.</span></span> <span data-ttu-id="9f2c5-106">Para obter mais informações, consulte [fluxo de dados para os desenvolvedores de filtro](data-flow-for-filter-developers.md).</span><span class="sxs-lookup"><span data-stu-id="9f2c5-106">For more information, see [Data Flow for Filter Developers](data-flow-for-filter-developers.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="9f2c5-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="9f2c5-107">Syntax</span></span>


```C++
CCritSec m_csReceive;
```



## <a name="requirements"></a><span data-ttu-id="9f2c5-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f2c5-108">Requirements</span></span>



| <span data-ttu-id="9f2c5-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f2c5-109">Requirement</span></span> | <span data-ttu-id="9f2c5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="9f2c5-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f2c5-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f2c5-111">Header</span></span><br/>  | <dl> <span data-ttu-id="9f2c5-112"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f2c5-112"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="9f2c5-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f2c5-113">Library</span></span><br/> | <dl> <span data-ttu-id="9f2c5-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9f2c5-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f2c5-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f2c5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f2c5-116">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="9f2c5-116">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




