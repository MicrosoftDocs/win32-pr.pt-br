---
description: O método ativo notifica o PIN de que o filtro está ativo agora.
ms.assetid: 1054f8cf-a5fb-4de6-abf2-c3740ce47787
title: Método CBasePin. Active (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.Active
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4a89c0c75671e6eb29b6ddb260c5f5ec0c385399
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751707"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="d7f09-103">Método CBasePin. active</span><span class="sxs-lookup"><span data-stu-id="d7f09-103">CBasePin.Active method</span></span>

<span data-ttu-id="d7f09-104">O `Active` método notifica o PIN de que o filtro está ativo agora.</span><span class="sxs-lookup"><span data-stu-id="d7f09-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7f09-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d7f09-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="d7f09-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d7f09-106">Parameters</span></span>

<span data-ttu-id="d7f09-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d7f09-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d7f09-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d7f09-108">Return value</span></span>

<span data-ttu-id="d7f09-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d7f09-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d7f09-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d7f09-110">Remarks</span></span>

<span data-ttu-id="d7f09-111">Quando o filtro vai de parado para em pausa, a classe [**CBaseFilter**](cbasefilter.md) chama esse método em todos os Pins conectados do filtro.</span><span class="sxs-lookup"><span data-stu-id="d7f09-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="d7f09-112">Esse método não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="d7f09-112">This method does nothing in the base class.</span></span> <span data-ttu-id="d7f09-113">Classes derivadas podem substituir esse método; por exemplo, um PIN pode confirmar os alocadores ou obter recursos de hardware.</span><span class="sxs-lookup"><span data-stu-id="d7f09-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="d7f09-114">O estado interno do Gerenciador de grafo de filtro não é atualizado até que essa função de membro retorne, portanto, não teste o estado desse método.</span><span class="sxs-lookup"><span data-stu-id="d7f09-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7f09-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d7f09-115">Requirements</span></span>



| <span data-ttu-id="d7f09-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="d7f09-116">Requirement</span></span> | <span data-ttu-id="d7f09-117">Valor</span><span class="sxs-lookup"><span data-stu-id="d7f09-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7f09-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d7f09-118">Header</span></span><br/>  | <dl> <span data-ttu-id="d7f09-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d7f09-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d7f09-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d7f09-120">Library</span></span><br/> | <dl> <span data-ttu-id="d7f09-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d7f09-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d7f09-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="d7f09-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7f09-123">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="d7f09-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




