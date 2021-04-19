---
description: A \_ variável de membro da exsample m especifica a hora de parada do exemplo mais recente.
ms.assetid: 694815b6-8da5-4174-b2c7-7d686a557c6c
title: 'Membro CDrawImage:: m_EndSample (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_EndSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 78268e8335d6dd8c24497a9e4d74b0caab205a99
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780878"
---
# <a name="cdrawimagem_endsample-member"></a><span data-ttu-id="a73d5-103">Membro de exemplo endCDrawImage:: m \_</span><span class="sxs-lookup"><span data-stu-id="a73d5-103">CDrawImage::m\_EndSample member</span></span>

<span data-ttu-id="a73d5-104">A `m_EndSample` variável de membro especifica a hora de parada do exemplo mais recente.</span><span class="sxs-lookup"><span data-stu-id="a73d5-104">The `m_EndSample` member variable specifies the stop time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a73d5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a73d5-105">Syntax</span></span>


```C++
CRefTime m_EndSample;
```



## <a name="remarks"></a><span data-ttu-id="a73d5-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="a73d5-106">Remarks</span></span>

<span data-ttu-id="a73d5-107">O valor só é válido dentro do método [**CDrawImage::D isplaysampletimes**](cdrawimage-displaysampletimes.md) .</span><span class="sxs-lookup"><span data-stu-id="a73d5-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a73d5-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a73d5-108">Requirements</span></span>



| <span data-ttu-id="a73d5-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a73d5-109">Requirement</span></span> | <span data-ttu-id="a73d5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a73d5-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a73d5-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a73d5-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a73d5-112"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a73d5-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a73d5-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a73d5-113">Library</span></span><br/> | <dl> <span data-ttu-id="a73d5-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a73d5-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a73d5-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="a73d5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a73d5-116">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="a73d5-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




