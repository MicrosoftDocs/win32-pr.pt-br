---
description: O método BreakConnect libera o PIN de uma conexão.
ms.assetid: a1f299e1-30bf-4d55-84cf-73acccf38151
title: Método CBasePin. BreakConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.BreakConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8964ea76e48e4753f42923663ab45962cd672e6e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770297"
---
# <a name="cbasepinbreakconnect-method"></a><span data-ttu-id="25bd1-103">Método CBasePin. BreakConnect</span><span class="sxs-lookup"><span data-stu-id="25bd1-103">CBasePin.BreakConnect method</span></span>

<span data-ttu-id="25bd1-104">O `BreakConnect` método libera o PIN de uma conexão.</span><span class="sxs-lookup"><span data-stu-id="25bd1-104">The `BreakConnect` method releases the pin from a connection.</span></span>

## <a name="syntax"></a><span data-ttu-id="25bd1-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25bd1-105">Syntax</span></span>


```C++
virtual HRESULT BreakConnect();
```



## <a name="parameters"></a><span data-ttu-id="25bd1-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25bd1-106">Parameters</span></span>

<span data-ttu-id="25bd1-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="25bd1-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25bd1-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25bd1-108">Return value</span></span>

<span data-ttu-id="25bd1-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="25bd1-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="25bd1-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="25bd1-110">Remarks</span></span>

<span data-ttu-id="25bd1-111">Esse método é chamado durante a desconexão do PIN pelo método [**CBasePin::D isconnect**](cbasepin-disconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="25bd1-111">This method is called during pin disconnection by the [**CBasePin::Disconnect**](cbasepin-disconnect.md) method.</span></span> <span data-ttu-id="25bd1-112">Ele também será chamado durante uma tentativa de conexão se o método [**CBasePin:: CheckConnect**](cbasepin-checkconnect.md) falhar.</span><span class="sxs-lookup"><span data-stu-id="25bd1-112">It is also called during a connection attempt if the [**CBasePin::CheckConnect**](cbasepin-checkconnect.md) method fails.</span></span>

<span data-ttu-id="25bd1-113">Esse método deve liberar todos os recursos que foram obtidos pelo método **CheckConnect** .</span><span class="sxs-lookup"><span data-stu-id="25bd1-113">This method must free any resources that were obtained by the **CheckConnect** method.</span></span> <span data-ttu-id="25bd1-114">Por exemplo, se **CheckConnect** alocar memória, `BreakConnect` o deve liberar a memória.</span><span class="sxs-lookup"><span data-stu-id="25bd1-114">For example, if **CheckConnect** allocates memory, `BreakConnect` should free the memory.</span></span> <span data-ttu-id="25bd1-115">Se **CheckConnect** consulta o PIN de conexão de uma interface, `BreakConnect` o deve liberar a interface.</span><span class="sxs-lookup"><span data-stu-id="25bd1-115">If **CheckConnect** queries the connecting pin for an interface, `BreakConnect` should free the interface.</span></span>

<span data-ttu-id="25bd1-116">Observe que `BreakConnect` pode ser chamado sem uma chamada correspondente para **CompleteConnect**.</span><span class="sxs-lookup"><span data-stu-id="25bd1-116">Note that `BreakConnect` can be called without a corresponding call to **CompleteConnect**.</span></span> <span data-ttu-id="25bd1-117">Portanto, você não pode supor que **CompleteConnect** foi chamado anteriormente.</span><span class="sxs-lookup"><span data-stu-id="25bd1-117">Therefore, you cannot assume that **CompleteConnect** has been called previously.</span></span>

## <a name="requirements"></a><span data-ttu-id="25bd1-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25bd1-118">Requirements</span></span>



| <span data-ttu-id="25bd1-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="25bd1-119">Requirement</span></span> | <span data-ttu-id="25bd1-120">Valor</span><span class="sxs-lookup"><span data-stu-id="25bd1-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25bd1-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25bd1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="25bd1-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25bd1-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="25bd1-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25bd1-123">Library</span></span><br/> | <dl> <span data-ttu-id="25bd1-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="25bd1-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25bd1-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="25bd1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25bd1-126">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="25bd1-126">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




