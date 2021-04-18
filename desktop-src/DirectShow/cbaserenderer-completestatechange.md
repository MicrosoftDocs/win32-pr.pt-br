---
description: O método CompleteStateChange determina se uma transição para o estado em pausa está concluída.
ms.assetid: 505a0b31-deaa-46be-91e6-f9bc8e47dd3a
title: Método CBaseRenderer. CompleteStateChange (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.CompleteStateChange
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d2465aeed3347f6ebc592dbe01bc3580a30983e0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753347"
---
# <a name="cbaserenderercompletestatechange-method"></a><span data-ttu-id="17ffa-103">Método CBaseRenderer. CompleteStateChange</span><span class="sxs-lookup"><span data-stu-id="17ffa-103">CBaseRenderer.CompleteStateChange method</span></span>

<span data-ttu-id="17ffa-104">O `CompleteStateChange` método determina se uma transição para o estado em pausa está concluída.</span><span class="sxs-lookup"><span data-stu-id="17ffa-104">The `CompleteStateChange` method determines whether a transition to the paused state is complete.</span></span>

## <a name="syntax"></a><span data-ttu-id="17ffa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="17ffa-105">Syntax</span></span>


```C++
virtual HRESULT CompleteStateChange(
   FILTER_STATE OldState
);
```



## <a name="parameters"></a><span data-ttu-id="17ffa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="17ffa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="17ffa-107">*OldState*</span><span class="sxs-lookup"><span data-stu-id="17ffa-107">*OldState*</span></span> 
</dt> <dd>

<span data-ttu-id="17ffa-108">Estado anterior à transição.</span><span class="sxs-lookup"><span data-stu-id="17ffa-108">State prior to the transition.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="17ffa-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="17ffa-109">Return value</span></span>

<span data-ttu-id="17ffa-110">Retornará S \_ OK se a transição for concluída.</span><span class="sxs-lookup"><span data-stu-id="17ffa-110">Returns S\_OK if the transition is complete.</span></span> <span data-ttu-id="17ffa-111">Caso contrário, retornará S \_ false.</span><span class="sxs-lookup"><span data-stu-id="17ffa-111">Otherwise, returns S\_FALSE.</span></span>

## <a name="remarks"></a><span data-ttu-id="17ffa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="17ffa-112">Remarks</span></span>

<span data-ttu-id="17ffa-113">O método [**CBaseRenderer::P ause**](cbaserenderer-pause.md) chama esse método para atualizar o status de transição de estado.</span><span class="sxs-lookup"><span data-stu-id="17ffa-113">The [**CBaseRenderer::Pause**](cbaserenderer-pause.md) method calls this method to update the state-transition status.</span></span> <span data-ttu-id="17ffa-114">Em geral, a transição para pausada não é concluída até que o filtro receba um exemplo.</span><span class="sxs-lookup"><span data-stu-id="17ffa-114">In general, the transition to paused does not finish until the filter receives a sample.</span></span> <span data-ttu-id="17ffa-115">No entanto, em algumas situações a transição é concluída imediatamente: por exemplo, se o filtro estiver desconectado ou se o final do fluxo foi atingido.</span><span class="sxs-lookup"><span data-stu-id="17ffa-115">However, in some situations the transition completes immediately: for example, if the filter is unconnected, or if the end of the stream was reached.</span></span> <span data-ttu-id="17ffa-116">Esse método verifica os vários critérios e, em seguida, chama o método [**CBaseRenderer:: Ready**](cbaserenderer-ready.md) ou o método [**CBaseRenderer:: não Ready**](cbaserenderer-notready.md) para atualizar o status da transição.</span><span class="sxs-lookup"><span data-stu-id="17ffa-116">This method checks the various criteria and then calls the [**CBaseRenderer::Ready**](cbaserenderer-ready.md) method or the [**CBaseRenderer::NotReady**](cbaserenderer-notready.md) method to update the transition status.</span></span>

## <a name="requirements"></a><span data-ttu-id="17ffa-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="17ffa-117">Requirements</span></span>



| <span data-ttu-id="17ffa-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="17ffa-118">Requirement</span></span> | <span data-ttu-id="17ffa-119">Valor</span><span class="sxs-lookup"><span data-stu-id="17ffa-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17ffa-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="17ffa-120">Header</span></span><br/>  | <dl> <span data-ttu-id="17ffa-121"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="17ffa-121"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="17ffa-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="17ffa-122">Library</span></span><br/> | <dl> <span data-ttu-id="17ffa-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="17ffa-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="17ffa-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="17ffa-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="17ffa-125">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="17ffa-125">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




