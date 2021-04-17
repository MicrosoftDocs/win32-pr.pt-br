---
description: O método TimerCallback é um método de retorno de chamada para o evento de timer de fim de fluxo.
ms.assetid: ed43d07a-1ece-43ab-8753-ab14fa388946
title: Método CBaseRenderer. TimerCallback (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.TimerCallback
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cfa59ca6bed0539caa7eb650458c168999b0de5a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749627"
---
# <a name="cbaserenderertimercallback-method"></a><span data-ttu-id="5acfd-103">Método CBaseRenderer. TimerCallback</span><span class="sxs-lookup"><span data-stu-id="5acfd-103">CBaseRenderer.TimerCallback method</span></span>

<span data-ttu-id="5acfd-104">O `TimerCallback` método é um método de retorno de chamada para o evento de timer de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="5acfd-104">The `TimerCallback` method is a callback method for the end-of-stream timer event.</span></span>

## <a name="syntax"></a><span data-ttu-id="5acfd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5acfd-105">Syntax</span></span>


```C++
void TimerCallback();
```



## <a name="parameters"></a><span data-ttu-id="5acfd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5acfd-106">Parameters</span></span>

<span data-ttu-id="5acfd-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5acfd-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5acfd-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5acfd-108">Return value</span></span>

<span data-ttu-id="5acfd-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="5acfd-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5acfd-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="5acfd-110">Remarks</span></span>

<span data-ttu-id="5acfd-111">O método [**CBaseRenderer:: SendEndOfStream**](cbaserenderer-sendendofstream.md) usa um evento de timer para agendar \_ notificações completas do EC.</span><span class="sxs-lookup"><span data-stu-id="5acfd-111">The [**CBaseRenderer::SendEndOfStream**](cbaserenderer-sendendofstream.md) method uses a timer event to schedule EC\_COMPLETE notifications.</span></span> <span data-ttu-id="5acfd-112">O método **CBaseRenderer:: TimerCallback** é a função de retorno de chamada para o evento timer.</span><span class="sxs-lookup"><span data-stu-id="5acfd-112">The **CBaseRenderer::TimerCallback** method is the callback function for the timer event.</span></span> <span data-ttu-id="5acfd-113">O `TimerCallback` método chama **SendEndOfStream** novamente e **SendEndOfStream** determina se a notificação completa do EC deve ser enviada \_ ou definida outro temporizador.</span><span class="sxs-lookup"><span data-stu-id="5acfd-113">The `TimerCallback` method calls **SendEndOfStream** again, and **SendEndOfStream** determines whether to send the EC\_COMPLETE notification or set another timer.</span></span>

<span data-ttu-id="5acfd-114">O método [**CBaseRenderer:: ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) cancela o evento timer.</span><span class="sxs-lookup"><span data-stu-id="5acfd-114">The [**CBaseRenderer::ResetEndOfStreamTimer**](cbaserenderer-resetendofstreamtimer.md) method cancels the timer event.</span></span>

## <a name="requirements"></a><span data-ttu-id="5acfd-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5acfd-115">Requirements</span></span>



| <span data-ttu-id="5acfd-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5acfd-116">Requirement</span></span> | <span data-ttu-id="5acfd-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5acfd-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5acfd-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5acfd-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5acfd-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5acfd-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="5acfd-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5acfd-120">Library</span></span><br/> | <dl> <span data-ttu-id="5acfd-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5acfd-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5acfd-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5acfd-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5acfd-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="5acfd-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




