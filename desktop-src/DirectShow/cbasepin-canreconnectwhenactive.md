---
description: O método CanReconnectWhenActive consulta se o PIN dá suporte a reconexões dinâmicas.
ms.assetid: a2679987-7897-4b18-b06b-9ab8f2f3b9f5
title: Método CBasePin. CanReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.CanReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 89a072a26afe0087ce9adfed5b29eb1cc4280dac
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753356"
---
# <a name="cbasepincanreconnectwhenactive-method"></a><span data-ttu-id="e951c-103">Método CBasePin. CanReconnectWhenActive</span><span class="sxs-lookup"><span data-stu-id="e951c-103">CBasePin.CanReconnectWhenActive method</span></span>

<span data-ttu-id="e951c-104">O `CanReconnectWhenActive` método consulta se o PIN dá suporte a reconexões dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="e951c-104">The `CanReconnectWhenActive` method queries whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="e951c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e951c-105">Syntax</span></span>


```C++
bool CanReconnectWhenActive();
```



## <a name="parameters"></a><span data-ttu-id="e951c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e951c-106">Parameters</span></span>

<span data-ttu-id="e951c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e951c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e951c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e951c-108">Return value</span></span>

<span data-ttu-id="e951c-109">Retorna um valor booliano que especifica se o PIN pode se reconectar dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="e951c-109">Returns a Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="e951c-110">Se **for true**, o PIN poderá se reconectar dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="e951c-110">If **TRUE**, the pin can dynamically reconnect.</span></span>

## <a name="remarks"></a><span data-ttu-id="e951c-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="e951c-111">Remarks</span></span>

<span data-ttu-id="e951c-112">Por padrão, você deve interromper um filtro antes de reconectar qualquer um de seus Pins.</span><span class="sxs-lookup"><span data-stu-id="e951c-112">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="e951c-113">No entanto, se um PIN oferecer suporte à reconexão dinâmica, ele poderá se reconectar enquanto o filtro estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="e951c-113">If a pin supports dynamic reconnection, however, it can reconnect while the filter is active.</span></span> <span data-ttu-id="e951c-114">Para obter mais informações, consulte [criação de grafo dinâmico](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="e951c-114">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="e951c-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e951c-115">Requirements</span></span>



| <span data-ttu-id="e951c-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="e951c-116">Requirement</span></span> | <span data-ttu-id="e951c-117">Valor</span><span class="sxs-lookup"><span data-stu-id="e951c-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e951c-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e951c-118">Header</span></span><br/>  | <dl> <span data-ttu-id="e951c-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e951c-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e951c-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e951c-120">Library</span></span><br/> | <dl> <span data-ttu-id="e951c-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e951c-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e951c-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="e951c-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e951c-123">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="e951c-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




