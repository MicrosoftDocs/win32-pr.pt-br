---
description: Taxa de reprodução. Por padrão, o valor é definido como 1,0.
ms.assetid: 835ddbe8-2017-4a4a-8f10-b3f33a8215a7
title: 'Membro CSourceSeeking:: m_dRateSeeking (Ctlutil. h)'
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- m_dRateSeeking
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1055a420316868db6374798c0295339dd74ac172
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105784030"
---
# <a name="csourceseekingm_drateseeking-member"></a><span data-ttu-id="df19f-104">Membro de CSourceSeeking:: m \_ dRateSeeking</span><span class="sxs-lookup"><span data-stu-id="df19f-104">CSourceSeeking::m\_dRateSeeking member</span></span>

<span data-ttu-id="df19f-105">Taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="df19f-105">Playback rate.</span></span> <span data-ttu-id="df19f-106">Por padrão, o valor é definido como 1,0.</span><span class="sxs-lookup"><span data-stu-id="df19f-106">By default, the value is set to 1.0.</span></span>

## <a name="syntax"></a><span data-ttu-id="df19f-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="df19f-107">Syntax</span></span>


```C++
double m_dRateSeeking;
```



## <a name="remarks"></a><span data-ttu-id="df19f-108">Comentários</span><span class="sxs-lookup"><span data-stu-id="df19f-108">Remarks</span></span>

<span data-ttu-id="df19f-109">Mantenha a seção crítica **m \_ pLock** antes de acessar essa variável.</span><span class="sxs-lookup"><span data-stu-id="df19f-109">Hold the **m\_pLock** critical section before accessing this variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="df19f-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="df19f-110">Requirements</span></span>



| <span data-ttu-id="df19f-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="df19f-111">Requirement</span></span> | <span data-ttu-id="df19f-112">Valor</span><span class="sxs-lookup"><span data-stu-id="df19f-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="df19f-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="df19f-113">Header</span></span><br/>  | <dl> <span data-ttu-id="df19f-114"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="df19f-114"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="df19f-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="df19f-115">Library</span></span><br/> | <dl> <span data-ttu-id="df19f-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="df19f-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="df19f-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="df19f-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="df19f-118">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="df19f-118">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




