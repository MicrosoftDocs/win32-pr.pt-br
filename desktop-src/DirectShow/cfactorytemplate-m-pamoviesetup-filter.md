---
description: Ponteiro para uma \_ estrutura de filtro AMOVIESETUP.
ms.assetid: 72db601b-78a3-484a-a27f-147ec36022ab
title: 'Membro CFactoryTemplate:: m_pAMovieSetup_Filter (combase. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_pAMovieSetup_Filter
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 087612acf99a41966ccd98d3b41d2b83255a86f9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769219"
---
# <a name="cfactorytemplatem_pamoviesetup_filter-member"></a><span data-ttu-id="72a51-103">Membro de filtro CFactoryTemplate:: m \_ pAMovieSetup \_</span><span class="sxs-lookup"><span data-stu-id="72a51-103">CFactoryTemplate::m\_pAMovieSetup\_Filter member</span></span>

<span data-ttu-id="72a51-104">Ponteiro para uma estrutura de [**\_ filtro AMOVIESETUP**](amoviesetup-filter.md) .</span><span class="sxs-lookup"><span data-stu-id="72a51-104">Pointer to an [**AMOVIESETUP\_FILTER**](amoviesetup-filter.md) structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="72a51-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="72a51-105">Syntax</span></span>


```C++
const AMOVIESETUP_FILTER *m_pAMovieSetup_Filter;
```



## <a name="remarks"></a><span data-ttu-id="72a51-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="72a51-106">Remarks</span></span>

<span data-ttu-id="72a51-107">Use essa estrutura para fazer um filtro se registrar automaticamente.</span><span class="sxs-lookup"><span data-stu-id="72a51-107">Use this structure to make a filter self-registering.</span></span> <span data-ttu-id="72a51-108">Se o componente não for um filtro, essa variável de membro poderá ser **nula**.</span><span class="sxs-lookup"><span data-stu-id="72a51-108">If your component is not a filter, this member variable can be **NULL**.</span></span> <span data-ttu-id="72a51-109">Para obter mais informações, consulte como registrar filtros do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="72a51-109">For more information, see How to Register DirectShow Filters.</span></span>

## <a name="requirements"></a><span data-ttu-id="72a51-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="72a51-110">Requirements</span></span>



| <span data-ttu-id="72a51-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="72a51-111">Requirement</span></span> | <span data-ttu-id="72a51-112">Valor</span><span class="sxs-lookup"><span data-stu-id="72a51-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="72a51-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="72a51-113">Header</span></span><br/>  | <dl> <span data-ttu-id="72a51-114"><dt>Combase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="72a51-114"><dt>Combase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="72a51-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="72a51-115">Library</span></span><br/> | <dl> <span data-ttu-id="72a51-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="72a51-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72a51-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="72a51-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72a51-118">**Classe CFactoryTemplate**</span><span class="sxs-lookup"><span data-stu-id="72a51-118">**CFactoryTemplate Class**</span></span>](cfactorytemplate.md)
</dt> </dl>

 

 




