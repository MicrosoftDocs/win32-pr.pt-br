---
description: O método ResetEndOfStreamTimer cancela o temporizador que agenda as \_ notificações completas do EC.
ms.assetid: 9d423241-1401-4181-8fbf-c409a1e8abdd
title: Método CBaseRenderer. ResetEndOfStreamTimer (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStreamTimer
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 734673c4e2bd6719179eca00f03a6c2f41061132
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747399"
---
# <a name="cbaserendererresetendofstreamtimer-method"></a><span data-ttu-id="ea625-103">Método CBaseRenderer. ResetEndOfStreamTimer</span><span class="sxs-lookup"><span data-stu-id="ea625-103">CBaseRenderer.ResetEndOfStreamTimer method</span></span>

<span data-ttu-id="ea625-104">O `ResetEndOfStreamTimer` método cancela o temporizador que agenda as notificações [**\_ completas do EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="ea625-104">The `ResetEndOfStreamTimer` method cancels the timer that schedules [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea625-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea625-105">Syntax</span></span>


```C++
void ResetEndOfStreamTimer();
```



## <a name="parameters"></a><span data-ttu-id="ea625-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea625-106">Parameters</span></span>

<span data-ttu-id="ea625-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ea625-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea625-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea625-108">Return value</span></span>

<span data-ttu-id="ea625-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="ea625-109">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea625-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea625-110">Requirements</span></span>



| <span data-ttu-id="ea625-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea625-111">Requirement</span></span> | <span data-ttu-id="ea625-112">Valor</span><span class="sxs-lookup"><span data-stu-id="ea625-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea625-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea625-113">Header</span></span><br/>  | <dl> <span data-ttu-id="ea625-114"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea625-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ea625-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea625-115">Library</span></span><br/> | <dl> <span data-ttu-id="ea625-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ea625-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea625-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea625-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea625-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="ea625-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> <dt>

[<span data-ttu-id="ea625-119">**CBaseRenderer::SendEndOfStream**</span><span class="sxs-lookup"><span data-stu-id="ea625-119">**CBaseRenderer::SendEndOfStream**</span></span>](cbaserenderer-sendendofstream.md)
</dt> <dt>

[<span data-ttu-id="ea625-120">**CBaseRenderer:: TimerCallback**</span><span class="sxs-lookup"><span data-stu-id="ea625-120">**CBaseRenderer::TimerCallback**</span></span>](cbaserenderer-timercallback.md)
</dt> </dl>

 

 




