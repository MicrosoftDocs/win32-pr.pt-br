---
description: O método EndOfStream notifica o filtro de que o PIN de entrada recebeu uma notificação de fim de fluxo.
ms.assetid: bdfd03f9-81e0-4d52-959e-82fd1a67e1c3
title: Método CBaseRenderer. EndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6e12da02ffbce99b29d324c1166b3d4cdf2265c6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752899"
---
# <a name="cbaserendererendofstream-method"></a><span data-ttu-id="d075a-103">Método CBaseRenderer. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="d075a-103">CBaseRenderer.EndOfStream method</span></span>

<span data-ttu-id="d075a-104">O `EndOfStream` método notifica o filtro de que o PIN de entrada recebeu uma notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d075a-104">The `EndOfStream` method notifies the filter that the input pin received an end-of-stream notification.</span></span>

## <a name="syntax"></a><span data-ttu-id="d075a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d075a-105">Syntax</span></span>


```C++
HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="d075a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d075a-106">Parameters</span></span>

<span data-ttu-id="d075a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="d075a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d075a-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d075a-108">Return value</span></span>

<span data-ttu-id="d075a-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="d075a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="d075a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="d075a-110">Remarks</span></span>

<span data-ttu-id="d075a-111">O pino de entrada do filtro chama esse método quando recebe uma notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="d075a-111">The filter's input pin calls this method when it receives an end-of-stream notification.</span></span>

<span data-ttu-id="d075a-112">Esse método define o [**sinalizador CBaseRenderer:: m \_ BeOS**](cbaserenderer-m-beos.md) como **true** e chama o método [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) para agendar um evento de [**\_ conclusão de EC**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="d075a-112">This method sets the [**CBaseRenderer::m\_bEOS**](cbaserenderer-m-beos.md) flag to **TRUE** and calls the [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method to schedule an [**EC\_COMPLETE**](ec-complete.md) event.</span></span> <span data-ttu-id="d075a-113">Se o filtro estiver em pausa e aguardando um exemplo, esse método concluirá a transição de estado.</span><span class="sxs-lookup"><span data-stu-id="d075a-113">If the filter is paused and waiting for a sample, this method completes the state transition.</span></span>

## <a name="requirements"></a><span data-ttu-id="d075a-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d075a-114">Requirements</span></span>



| <span data-ttu-id="d075a-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="d075a-115">Requirement</span></span> | <span data-ttu-id="d075a-116">Valor</span><span class="sxs-lookup"><span data-stu-id="d075a-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d075a-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d075a-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d075a-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d075a-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="d075a-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d075a-119">Library</span></span><br/> | <dl> <span data-ttu-id="d075a-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d075a-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d075a-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="d075a-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d075a-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="d075a-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




