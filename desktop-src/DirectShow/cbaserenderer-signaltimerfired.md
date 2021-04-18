---
description: O método SignalTimerFired limpa o identificador do temporizador usado para agendar a renderização.
ms.assetid: b8ae362e-fcda-4888-be32-8fb910d0f0db
title: Método CBaseRenderer. SignalTimerFired (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.SignalTimerFired
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4dd29b37869fc6f07c2d876dfa0d1d306b04b111
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105757038"
---
# <a name="cbaserenderersignaltimerfired-method"></a><span data-ttu-id="b75ed-103">Método CBaseRenderer. SignalTimerFired</span><span class="sxs-lookup"><span data-stu-id="b75ed-103">CBaseRenderer.SignalTimerFired method</span></span>

<span data-ttu-id="b75ed-104">O `SignalTimerFired` método limpa o identificador do temporizador usado para agendar a renderização.</span><span class="sxs-lookup"><span data-stu-id="b75ed-104">The `SignalTimerFired` method clears the timer identifier used to schedule rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="b75ed-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b75ed-105">Syntax</span></span>


```C++
virtual void SignalTimerFired();
```



## <a name="parameters"></a><span data-ttu-id="b75ed-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b75ed-106">Parameters</span></span>

<span data-ttu-id="b75ed-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b75ed-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b75ed-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b75ed-108">Return value</span></span>

<span data-ttu-id="b75ed-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="b75ed-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="b75ed-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b75ed-110">Remarks</span></span>

<span data-ttu-id="b75ed-111">O filtro chama esse método quando o temporizador de renderização é ativado (consulte [**CBaseRenderer:: WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) ou quando o temporizador é cancelado (consulte [**CBaseRenderer:: CancelNotification**](cbaserenderer-cancelnotification.md)).</span><span class="sxs-lookup"><span data-stu-id="b75ed-111">The filter calls this method when the rendering timer activates (see [**CBaseRenderer::WaitForRenderTime**](cbaserenderer-waitforrendertime.md)) or when the timer is canceled (see [**CBaseRenderer::CancelNotification**](cbaserenderer-cancelnotification.md)).</span></span> <span data-ttu-id="b75ed-112">O método redefine a variável de membro [**CBaseRenderer:: m \_ dwAdvise**](cbaserenderer-m-dwadvise.md) para zero.</span><span class="sxs-lookup"><span data-stu-id="b75ed-112">The method resets the [**CBaseRenderer::m\_dwAdvise**](cbaserenderer-m-dwadvise.md) member variable to zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b75ed-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b75ed-113">Requirements</span></span>



| <span data-ttu-id="b75ed-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b75ed-114">Requirement</span></span> | <span data-ttu-id="b75ed-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b75ed-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b75ed-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b75ed-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b75ed-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b75ed-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b75ed-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b75ed-118">Library</span></span><br/> | <dl> <span data-ttu-id="b75ed-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b75ed-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b75ed-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b75ed-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b75ed-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="b75ed-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




