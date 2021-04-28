---
description: Método CBasePin. active – o método ativo notifica o PIN de que o filtro está ativo agora.
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
ms.openlocfilehash: 8ccee76dbf89cf82abcd8d4758305ddec91f1afa
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096096"
---
# <a name="cbasepinactive-method"></a><span data-ttu-id="8ca4b-103">Método CBasePin. active</span><span class="sxs-lookup"><span data-stu-id="8ca4b-103">CBasePin.Active method</span></span>

<span data-ttu-id="8ca4b-104">O `Active` método notifica o PIN de que o filtro está ativo agora.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-104">The `Active` method notifies the pin that the filter is now active.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ca4b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="8ca4b-105">Syntax</span></span>


```C++
virtual HRESULT Active();
```



## <a name="parameters"></a><span data-ttu-id="8ca4b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="8ca4b-106">Parameters</span></span>

<span data-ttu-id="8ca4b-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="8ca4b-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="8ca4b-108">Return value</span></span>

<span data-ttu-id="8ca4b-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="8ca4b-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="8ca4b-110">Remarks</span></span>

<span data-ttu-id="8ca4b-111">Quando o filtro vai de parado para em pausa, a classe [**CBaseFilter**](cbasefilter.md) chama esse método em todos os Pins conectados do filtro.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-111">When the filter goes from stopped to paused, the [**CBaseFilter**](cbasefilter.md) class calls this method on all of the filter's connected pins.</span></span>

<span data-ttu-id="8ca4b-112">Esse método não faz nada na classe base.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-112">This method does nothing in the base class.</span></span> <span data-ttu-id="8ca4b-113">Classes derivadas podem substituir esse método; por exemplo, um PIN pode confirmar os alocadores ou obter recursos de hardware.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-113">Derived classes can override this method; for example, a pin might commit allocators or obtain hardware resources.</span></span>

<span data-ttu-id="8ca4b-114">O estado interno do Gerenciador de grafo de filtro não é atualizado até que essa função de membro retorne, portanto, não teste o estado desse método.</span><span class="sxs-lookup"><span data-stu-id="8ca4b-114">The filter graph manager's internal state is not updated until after this member function returns, so do not test the state from this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="8ca4b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="8ca4b-115">Requirements</span></span>



| <span data-ttu-id="8ca4b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="8ca4b-116">Requirement</span></span> | <span data-ttu-id="8ca4b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="8ca4b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8ca4b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="8ca4b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="8ca4b-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="8ca4b-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="8ca4b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="8ca4b-120">Library</span></span><br/> | <dl> <span data-ttu-id="8ca4b-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="8ca4b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8ca4b-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="8ca4b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8ca4b-123">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="8ca4b-123">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




