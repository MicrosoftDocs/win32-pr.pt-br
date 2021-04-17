---
description: O método SetReconnectWhenActive especifica se o PIN dá suporte a reconexões dinâmicas.
ms.assetid: 64776008-5d1b-461c-a446-8cd6124276c0
title: Método CBasePin. SetReconnectWhenActive (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.SetReconnectWhenActive
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 10840ad60c858f69164b19f2460a0039cd332700
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105783203"
---
# <a name="cbasepinsetreconnectwhenactive-method"></a><span data-ttu-id="8aa8f-103">Método CBasePin. SetReconnectWhenActive</span><span class="sxs-lookup"><span data-stu-id="8aa8f-103">CBasePin.SetReconnectWhenActive method</span></span>

<span data-ttu-id="8aa8f-104">O `SetReconnectWhenActive` método especifica se o PIN dá suporte a reconexões dinâmicas.</span><span class="sxs-lookup"><span data-stu-id="8aa8f-104">The `SetReconnectWhenActive` method specifies whether the pin supports dynamic reconnections.</span></span>

## <a name="syntax"></a><span data-ttu-id="8aa8f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8aa8f-105">Syntax</span></span>


```C++
void SetReconnectWhenActive(
   bool bCanReconnect
);
```



## <a name="parameters"></a><span data-ttu-id="8aa8f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8aa8f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8aa8f-107">*bCanReconnect*</span><span class="sxs-lookup"><span data-stu-id="8aa8f-107">*bCanReconnect*</span></span> 
</dt> <dd>

<span data-ttu-id="8aa8f-108">Valor booliano que especifica se o PIN pode se reconectar dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="8aa8f-108">Boolean value that specifies whether the pin can dynamically reconnect.</span></span> <span data-ttu-id="8aa8f-109">Se **for true**, o PIN poderá se reconectar dinamicamente.</span><span class="sxs-lookup"><span data-stu-id="8aa8f-109">If **TRUE**, the pin can dynamically reconnect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8aa8f-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="8aa8f-110">Return value</span></span>

<span data-ttu-id="8aa8f-111">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="8aa8f-111">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="8aa8f-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="8aa8f-112">Remarks</span></span>

<span data-ttu-id="8aa8f-113">Por padrão, você deve interromper um filtro antes de reconectar qualquer um de seus Pins.</span><span class="sxs-lookup"><span data-stu-id="8aa8f-113">By default, you must stop a filter before reconnecting any of its pins.</span></span> <span data-ttu-id="8aa8f-114">Se o PIN puder se reconectar enquanto o filtro estiver ativo, chame esse método com um valor de **true**.</span><span class="sxs-lookup"><span data-stu-id="8aa8f-114">If the pin can reconnect while the filter is active, call this method with a value of **TRUE**.</span></span> <span data-ttu-id="8aa8f-115">Para obter mais informações, consulte [criação de grafo dinâmico](dynamic-graph-building.md).</span><span class="sxs-lookup"><span data-stu-id="8aa8f-115">For more information, see [Dynamic Graph Building](dynamic-graph-building.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8aa8f-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8aa8f-116">Requirements</span></span>



| <span data-ttu-id="8aa8f-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="8aa8f-117">Requirement</span></span> | <span data-ttu-id="8aa8f-118">Valor</span><span class="sxs-lookup"><span data-stu-id="8aa8f-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8aa8f-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8aa8f-119">Header</span></span><br/>  | <dl> <span data-ttu-id="8aa8f-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8aa8f-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8aa8f-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8aa8f-121">Library</span></span><br/> | <dl> <span data-ttu-id="8aa8f-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8aa8f-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8aa8f-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="8aa8f-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8aa8f-124">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="8aa8f-124">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




