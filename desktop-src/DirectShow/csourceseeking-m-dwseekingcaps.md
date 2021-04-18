---
description: Buscando recursos.
ms.assetid: c849db20-7567-41e0-9a57-85070a6e6a3a
title: 'Membro CSourceSeeking:: m_dwSeekingCaps (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dwSeekingCaps
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e4addb06b120801b0d5e697c7df93ab8ba620bbd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751485"
---
# <a name="csourceseekingm_dwseekingcaps-member"></a><span data-ttu-id="d6984-103">Membro de CSourceSeeking:: m \_ dwSeekingCaps</span><span class="sxs-lookup"><span data-stu-id="d6984-103">CSourceSeeking::m\_dwSeekingCaps member</span></span>

<span data-ttu-id="d6984-104">Buscando recursos.</span><span class="sxs-lookup"><span data-stu-id="d6984-104">Seeking capabilities.</span></span>

## <a name="syntax"></a><span data-ttu-id="d6984-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d6984-105">Syntax</span></span>


```C++
DWORD m_dwSeekingCaps;
```



## <a name="remarks"></a><span data-ttu-id="d6984-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="d6984-106">Remarks</span></span>

<span data-ttu-id="d6984-107">Por padrão, o valor é definido como a combinação bit-a-bit dos seguintes sinalizadores:</span><span class="sxs-lookup"><span data-stu-id="d6984-107">By default, the value is set to the bitwise combination of the following flags:</span></span>

-   <span data-ttu-id="d6984-108">Estou \_ procurando \_ CanSeekForwards</span><span class="sxs-lookup"><span data-stu-id="d6984-108">AM\_SEEKING\_CanSeekForwards</span></span>
-   <span data-ttu-id="d6984-109">Estou \_ procurando \_ CanSeekBackwards</span><span class="sxs-lookup"><span data-stu-id="d6984-109">AM\_SEEKING\_CanSeekBackwards</span></span>
-   <span data-ttu-id="d6984-110">Estou \_ procurando \_ CanSeekAbsolute</span><span class="sxs-lookup"><span data-stu-id="d6984-110">AM\_SEEKING\_CanSeekAbsolute</span></span>
-   <span data-ttu-id="d6984-111">Estou \_ procurando \_ CanGetStopPos</span><span class="sxs-lookup"><span data-stu-id="d6984-111">AM\_SEEKING\_CanGetStopPos</span></span>
-   <span data-ttu-id="d6984-112">Estou \_ procurando \_ CanGetDuration</span><span class="sxs-lookup"><span data-stu-id="d6984-112">AM\_SEEKING\_CanGetDuration</span></span>

<span data-ttu-id="d6984-113">Se o filtro oferecer suporte a um conjunto diferente de recursos, substitua esse valor.</span><span class="sxs-lookup"><span data-stu-id="d6984-113">If the filter supports a different set of capabilities, override this value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d6984-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d6984-114">Requirements</span></span>



| <span data-ttu-id="d6984-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d6984-115">Requirement</span></span> | <span data-ttu-id="d6984-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d6984-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d6984-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d6984-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d6984-118"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d6984-118"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d6984-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d6984-119">Library</span></span><br/> | <dl> <span data-ttu-id="d6984-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d6984-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d6984-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d6984-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d6984-122">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="d6984-122">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




