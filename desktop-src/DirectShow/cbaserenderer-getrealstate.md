---
description: O método getrealstate recupera o estado do filtro.
ms.assetid: d31c5c0b-6220-4d2e-a81a-d16b7d513c87
title: Método CBaseRenderer. getrealstate (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.GetRealState
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 40f2e49137a4324b14f25e4abb9b14cb919efbb9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752507"
---
# <a name="cbaserenderergetrealstate-method"></a><span data-ttu-id="ed1d1-103">Método CBaseRenderer. getrealstate</span><span class="sxs-lookup"><span data-stu-id="ed1d1-103">CBaseRenderer.GetRealState method</span></span>

<span data-ttu-id="ed1d1-104">O `GetRealState` método recupera o estado do filtro.</span><span class="sxs-lookup"><span data-stu-id="ed1d1-104">The `GetRealState` method retrieves the filter state.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed1d1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ed1d1-105">Syntax</span></span>


```C++
FILTER_STATE GetRealState();
```



## <a name="parameters"></a><span data-ttu-id="ed1d1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ed1d1-106">Parameters</span></span>

<span data-ttu-id="ed1d1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ed1d1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ed1d1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ed1d1-108">Return value</span></span>

<span data-ttu-id="ed1d1-109">Retorna o valor do [**\_ estado CBaseFilter:: m**](cbasefilter-m-state.md).</span><span class="sxs-lookup"><span data-stu-id="ed1d1-109">Returns the value of [**CBaseFilter::m\_State**](cbasefilter-m-state.md).</span></span> <span data-ttu-id="ed1d1-110">O valor é um membro do tipo enumerado de [**\_ estado do filtro**](/windows/win32/api/strmif/ne-strmif-filter_state) .</span><span class="sxs-lookup"><span data-stu-id="ed1d1-110">The value is a member of the [**FILTER\_STATE**](/windows/win32/api/strmif/ne-strmif-filter_state) enumerated type.</span></span>

## <a name="remarks"></a><span data-ttu-id="ed1d1-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ed1d1-111">Remarks</span></span>

<span data-ttu-id="ed1d1-112">Esse método fornece uma alternativa mais simples ao método [**CBaseRenderer:: GetState**](cbaserenderer-getstate.md) , para uso interno.</span><span class="sxs-lookup"><span data-stu-id="ed1d1-112">This method provides a simpler alternative to the [**CBaseRenderer::GetState**](cbaserenderer-getstate.md) method, for internal use.</span></span>

## <a name="requirements"></a><span data-ttu-id="ed1d1-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ed1d1-113">Requirements</span></span>



| <span data-ttu-id="ed1d1-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="ed1d1-114">Requirement</span></span> | <span data-ttu-id="ed1d1-115">Valor</span><span class="sxs-lookup"><span data-stu-id="ed1d1-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ed1d1-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ed1d1-116">Header</span></span><br/>  | <dl> <span data-ttu-id="ed1d1-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ed1d1-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="ed1d1-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ed1d1-118">Library</span></span><br/> | <dl> <span data-ttu-id="ed1d1-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ed1d1-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ed1d1-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="ed1d1-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ed1d1-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="ed1d1-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




