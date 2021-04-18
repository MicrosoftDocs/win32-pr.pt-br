---
description: O método GetRenderEvent recupera o evento que agenda a renderização.
ms.assetid: da0272f6-6a1d-4c07-a907-822227b56305
title: Método CBaseRenderer. GetRenderEvent (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRenderEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9e2fd0b9cd98194129eccd2e24e6ee75577d1eec
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783197"
---
# <a name="cbaserenderergetrenderevent-method"></a><span data-ttu-id="067e2-103">Método CBaseRenderer. GetRenderEvent</span><span class="sxs-lookup"><span data-stu-id="067e2-103">CBaseRenderer.GetRenderEvent method</span></span>

<span data-ttu-id="067e2-104">O `GetRenderEvent` método recupera o evento que agenda a renderização.</span><span class="sxs-lookup"><span data-stu-id="067e2-104">The `GetRenderEvent` method retrieves the event that schedules rendering.</span></span>

## <a name="syntax"></a><span data-ttu-id="067e2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="067e2-105">Syntax</span></span>


```C++
CAMEvent* GetRenderEvent();
```



## <a name="parameters"></a><span data-ttu-id="067e2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="067e2-106">Parameters</span></span>

<span data-ttu-id="067e2-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="067e2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="067e2-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="067e2-108">Return value</span></span>

<span data-ttu-id="067e2-109">Retorna um ponteiro para o evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) .</span><span class="sxs-lookup"><span data-stu-id="067e2-109">Returns a pointer to the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event.</span></span>

## <a name="requirements"></a><span data-ttu-id="067e2-110">Requisitos</span><span class="sxs-lookup"><span data-stu-id="067e2-110">Requirements</span></span>



| <span data-ttu-id="067e2-111">Requisito</span><span class="sxs-lookup"><span data-stu-id="067e2-111">Requirement</span></span> | <span data-ttu-id="067e2-112">Valor</span><span class="sxs-lookup"><span data-stu-id="067e2-112">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="067e2-113">parâmetro</span><span class="sxs-lookup"><span data-stu-id="067e2-113">Header</span></span><br/>  | <dl> <span data-ttu-id="067e2-114"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="067e2-114"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="067e2-115">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="067e2-115">Library</span></span><br/> | <dl> <span data-ttu-id="067e2-116"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="067e2-116"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="067e2-117">Confira também</span><span class="sxs-lookup"><span data-stu-id="067e2-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="067e2-118">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="067e2-118">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




