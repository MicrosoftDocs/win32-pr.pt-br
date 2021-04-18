---
description: O método EndOfStream notifica o filtro de que nenhum dado adicional é esperado do pino de entrada.
ms.assetid: b8fc3976-e3d4-4f16-82b0-3900ad6a740c
title: Método CTransformFilter. EndOfStream (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.EndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dea676a42f6df46d0035fdbb6e812b1df15fbb2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752079"
---
# <a name="ctransformfilterendofstream-method"></a><span data-ttu-id="24141-103">Método CTransformFilter. EndOfStream</span><span class="sxs-lookup"><span data-stu-id="24141-103">CTransformFilter.EndOfStream method</span></span>

<span data-ttu-id="24141-104">O `EndOfStream` método notifica o filtro de que nenhum dado adicional é esperado do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="24141-104">The `EndOfStream` method notifies the filter that no additional data is expected from the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="24141-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="24141-105">Syntax</span></span>


```C++
virtual HRESULT EndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="24141-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="24141-106">Parameters</span></span>

<span data-ttu-id="24141-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="24141-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="24141-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="24141-108">Return value</span></span>

<span data-ttu-id="24141-109">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="24141-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="24141-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="24141-110">Remarks</span></span>

<span data-ttu-id="24141-111">O método [**CTransformInputPin:: EndOfStream**](ctransforminputpin-endofstream.md) do pino de entrada chama esse método.</span><span class="sxs-lookup"><span data-stu-id="24141-111">The input pin's [**CTransformInputPin::EndOfStream**](ctransforminputpin-endofstream.md) method calls this method.</span></span> <span data-ttu-id="24141-112">Esse método entrega o downstream de notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="24141-112">This method delivers the end-of-stream notification downstream.</span></span> <span data-ttu-id="24141-113">Se a classe derivada usar um thread de trabalho para fornecer amostras de mídia, ela deverá substituir esse método e enfileirar a notificação de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="24141-113">If the derived class uses a worker thread to deliver media samples, it should override this method and queue the end-of-stream notification.</span></span>

## <a name="requirements"></a><span data-ttu-id="24141-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="24141-114">Requirements</span></span>



| <span data-ttu-id="24141-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="24141-115">Requirement</span></span> | <span data-ttu-id="24141-116">Valor</span><span class="sxs-lookup"><span data-stu-id="24141-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="24141-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="24141-117">Header</span></span><br/>  | <dl> <span data-ttu-id="24141-118"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="24141-118"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="24141-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="24141-119">Library</span></span><br/> | <dl> <span data-ttu-id="24141-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="24141-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="24141-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="24141-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="24141-122">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="24141-122">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




