---
description: 'Duração do fluxo. Por padrão, o valor é definido como o valor da variável de membro CSourceSeeking:: m \_ rtStop.'
ms.assetid: a87b321e-3179-4485-969b-bf12cb634b43
title: 'Membro CSourceSeeking:: m_rtDuration (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_rtDuration
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e188a29689a6dd1a54ef401f8bd2677e30989972
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748620"
---
# <a name="csourceseekingm_rtduration-member"></a><span data-ttu-id="814f2-104">Membro de CSourceSeeking:: m \_ rtDuration</span><span class="sxs-lookup"><span data-stu-id="814f2-104">CSourceSeeking::m\_rtDuration member</span></span>

<span data-ttu-id="814f2-105">Duração do fluxo.</span><span class="sxs-lookup"><span data-stu-id="814f2-105">Duration of the stream.</span></span> <span data-ttu-id="814f2-106">Por padrão, o valor é definido como o valor da variável de membro [**CSourceSeeking:: m \_ rtStop**](csourceseeking-m-rtstop.md) .</span><span class="sxs-lookup"><span data-stu-id="814f2-106">By default, the value is set to the value of the [**CSourceSeeking::m\_rtStop**](csourceseeking-m-rtstop.md) member variable.</span></span>

## <a name="syntax"></a><span data-ttu-id="814f2-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="814f2-107">Syntax</span></span>


```C++
CRefTime m_rtDuration;
```



## <a name="remarks"></a><span data-ttu-id="814f2-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="814f2-108">Remarks</span></span>

<span data-ttu-id="814f2-109">Mantenha a seção crítica **m \_ pLock** antes de acessar essa variável.</span><span class="sxs-lookup"><span data-stu-id="814f2-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="814f2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="814f2-110">Requirements</span></span>



| <span data-ttu-id="814f2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="814f2-111">Requirement</span></span> | <span data-ttu-id="814f2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="814f2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="814f2-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="814f2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="814f2-114"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="814f2-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="814f2-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="814f2-115">Library</span></span><br/> | <dl> <span data-ttu-id="814f2-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="814f2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="814f2-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="814f2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="814f2-118">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="814f2-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




