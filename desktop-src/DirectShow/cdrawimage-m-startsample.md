---
description: A \_ variável de membro m StartSample especifica a hora de início do exemplo mais recente.
ms.assetid: 2e6d6893-d57b-4009-a6ec-40dc0878d9c4
title: 'Membro CDrawImage:: m_StartSample (Winutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_StartSample
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4fd8039b1d37d0e61a150ed6c6944f0052089b0c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105782265"
---
# <a name="cdrawimagem_startsample-member"></a><span data-ttu-id="a599c-103">Membro de CDrawImage:: m \_ StartSample</span><span class="sxs-lookup"><span data-stu-id="a599c-103">CDrawImage::m\_StartSample member</span></span>

<span data-ttu-id="a599c-104">A variável de membro **m \_ StartSample** especifica a hora de início do exemplo mais recente.</span><span class="sxs-lookup"><span data-stu-id="a599c-104">The **m\_StartSample** member variable specifies the start time of the most recent sample.</span></span>

## <a name="syntax"></a><span data-ttu-id="a599c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a599c-105">Syntax</span></span>


```C++
CRefTime m_StartSample;
```



## <a name="remarks"></a><span data-ttu-id="a599c-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="a599c-106">Remarks</span></span>

<span data-ttu-id="a599c-107">O valor só é válido dentro do método [**CDrawImage::D isplaysampletimes**](cdrawimage-displaysampletimes.md) .</span><span class="sxs-lookup"><span data-stu-id="a599c-107">The value is only valid inside the [**CDrawImage::DisplaySampleTimes**](cdrawimage-displaysampletimes.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="a599c-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a599c-108">Requirements</span></span>



| <span data-ttu-id="a599c-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="a599c-109">Requirement</span></span> | <span data-ttu-id="a599c-110">Valor</span><span class="sxs-lookup"><span data-stu-id="a599c-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a599c-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a599c-111">Header</span></span><br/>  | <dl> <span data-ttu-id="a599c-112"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a599c-112"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a599c-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a599c-113">Library</span></span><br/> | <dl> <span data-ttu-id="a599c-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a599c-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a599c-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="a599c-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a599c-116">**Classe CDrawImage**</span><span class="sxs-lookup"><span data-stu-id="a599c-116">**CDrawImage Class**</span></span>](cdrawimage.md)
</dt> </dl>

 

 




