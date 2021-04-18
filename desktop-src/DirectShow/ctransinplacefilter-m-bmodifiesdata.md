---
description: A \_ variável de membro m bModifiesData indica se o filtro modifica os dados de exemplo que são recebidos. O valor é definido no Construtor CTransInPlaceFilter, mas o padrão é TRUE.
ms.assetid: 8ccdba46-315f-4519-b363-6870d1217f98
title: 'Membro CTransInPlaceFilter:: m_bModifiesData (TRANSip. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_bModifiesData
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5bc0d630fd0eda6e9915f8c11f5b15d21b725ce8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752075"
---
# <a name="ctransinplacefilterm_bmodifiesdata-member"></a><span data-ttu-id="b8548-104">Membro de CTransInPlaceFilter:: m \_ bModifiesData</span><span class="sxs-lookup"><span data-stu-id="b8548-104">CTransInPlaceFilter::m\_bModifiesData member</span></span>

<span data-ttu-id="b8548-105">A `m_bModifiesData` variável de membro indica se o filtro modifica os dados de exemplo que são recebidos.</span><span class="sxs-lookup"><span data-stu-id="b8548-105">The `m_bModifiesData` member variable indicates whether the filter modifies the sample data that is receives.</span></span> <span data-ttu-id="b8548-106">O valor é definido no construtor **CTransInPlaceFilter** , mas o padrão é **true**.</span><span class="sxs-lookup"><span data-stu-id="b8548-106">The value is set in the **CTransInPlaceFilter** constructor, but defaults to **TRUE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b8548-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b8548-107">Syntax</span></span>


```C++
bool m_bModifiesData;
```



## <a name="remarks"></a><span data-ttu-id="b8548-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="b8548-108">Remarks</span></span>

<span data-ttu-id="b8548-109">Essa variável afeta como o filtro negocia o alocador.</span><span class="sxs-lookup"><span data-stu-id="b8548-109">This variable affects how the filter negotiates the allocator.</span></span> <span data-ttu-id="b8548-110">Se o valor for **true**, o filtro não poderá usar um alocador somente leitura para ambas as conexões de PIN.</span><span class="sxs-lookup"><span data-stu-id="b8548-110">If the value is **TRUE**, the filter cannot use a read-only allocator for both pin connections.</span></span>

## <a name="requirements"></a><span data-ttu-id="b8548-111">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b8548-111">Requirements</span></span>



| <span data-ttu-id="b8548-112">Requisito</span><span class="sxs-lookup"><span data-stu-id="b8548-112">Requirement</span></span> | <span data-ttu-id="b8548-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b8548-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b8548-114">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b8548-114">Header</span></span><br/>  | <dl> <span data-ttu-id="b8548-115"><dt>TRANSip. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b8548-115"><dt>Transip.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b8548-116">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b8548-116">Library</span></span><br/> | <dl> <span data-ttu-id="b8548-117"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b8548-117"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b8548-118">Confira também</span><span class="sxs-lookup"><span data-stu-id="b8548-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8548-119">**Classe CTransInPlaceFilter**</span><span class="sxs-lookup"><span data-stu-id="b8548-119">**CTransInPlaceFilter Class**</span></span>](ctransinplacefilter.md)
</dt> </dl>

 

 




