---
description: O método WaitForRenderTime aguarda o tempo de apresentação do exemplo atual.
ms.assetid: a6acb780-48df-4f73-adcb-cfa4e54b19ac
title: Método CBaseRenderer. WaitForRenderTime (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.WaitForRenderTime
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a537728ca0874fa1dfd69b4712bcc97cf23850
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749626"
---
# <a name="cbaserendererwaitforrendertime-method"></a><span data-ttu-id="7ac38-103">Método CBaseRenderer. WaitForRenderTime</span><span class="sxs-lookup"><span data-stu-id="7ac38-103">CBaseRenderer.WaitForRenderTime method</span></span>

<span data-ttu-id="7ac38-104">O `WaitForRenderTime` método aguarda o tempo de apresentação do exemplo atual.</span><span class="sxs-lookup"><span data-stu-id="7ac38-104">The `WaitForRenderTime` method waits for the current sample's presentation time.</span></span>

## <a name="syntax"></a><span data-ttu-id="7ac38-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7ac38-105">Syntax</span></span>


```C++
virtual HRESULT WaitForRenderTime();
```



## <a name="parameters"></a><span data-ttu-id="7ac38-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7ac38-106">Parameters</span></span>

<span data-ttu-id="7ac38-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="7ac38-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="7ac38-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7ac38-108">Return value</span></span>

<span data-ttu-id="7ac38-109">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="7ac38-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="7ac38-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="7ac38-110">Return code</span></span>                                                                                           | <span data-ttu-id="7ac38-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="7ac38-111">Description</span></span>                                                               |
|-------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7ac38-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="7ac38-112"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="7ac38-113">Êxito.</span><span class="sxs-lookup"><span data-stu-id="7ac38-113">Success.</span></span><br/>                                                       |
| <dl> <span data-ttu-id="7ac38-114"><dt>**VFW \_ E \_ estado \_ alterado**</dt></span><span class="sxs-lookup"><span data-stu-id="7ac38-114"><dt>**VFW\_E\_STATE\_CHANGED**</dt></span></span> </dl> | <span data-ttu-id="7ac38-115">O estado do filtro foi alterado antes de o tempo de apresentação chegar.</span><span class="sxs-lookup"><span data-stu-id="7ac38-115">The filter state changed before the presentation time arrived.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="7ac38-116">Comentários</span><span class="sxs-lookup"><span data-stu-id="7ac38-116">Remarks</span></span>

<span data-ttu-id="7ac38-117">Esse método aguarda até que ocorra um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="7ac38-117">This method waits until one of the following occurs:</span></span>

-   <span data-ttu-id="7ac38-118">O tempo de apresentação do exemplo chega, no ponto em que o exemplo pode ser renderizado.</span><span class="sxs-lookup"><span data-stu-id="7ac38-118">The sample's presentation time arrives, at which point the sample can be rendered.</span></span>
-   <span data-ttu-id="7ac38-119">O filtro para ou começa a liberar dados.</span><span class="sxs-lookup"><span data-stu-id="7ac38-119">The filter stops or begins flushing data.</span></span>

<span data-ttu-id="7ac38-120">Se o tempo de apresentação chegar, o evento [**CBaseRenderer:: m \_ RenderEvent**](cbaserenderer-m-renderevent.md) será sinalizado.</span><span class="sxs-lookup"><span data-stu-id="7ac38-120">If the presentation time arrives, the [**CBaseRenderer::m\_RenderEvent**](cbaserenderer-m-renderevent.md) event is signaled.</span></span> <span data-ttu-id="7ac38-121">Se o estado for alterado, o evento [**CBaseRenderer:: m \_ ThreadSignal**](cbaserenderer-m-threadsignal.md) será sinalizado.</span><span class="sxs-lookup"><span data-stu-id="7ac38-121">If the state changes, the [**CBaseRenderer::m\_ThreadSignal**](cbaserenderer-m-threadsignal.md) event is signaled.</span></span> <span data-ttu-id="7ac38-122">Esse método espera em ambos os eventos.</span><span class="sxs-lookup"><span data-stu-id="7ac38-122">This method waits on both events.</span></span> <span data-ttu-id="7ac38-123">A classe derivada pode substituir esse método para aguardar eventos adicionais, se necessário.</span><span class="sxs-lookup"><span data-stu-id="7ac38-123">The derived class can override this method to wait on additional events, if necessary.</span></span>

<span data-ttu-id="7ac38-124">Esse método chama o método [**CBaseRenderer:: OnWaitStart**](cbaserenderer-onwaitstart.md) quando a espera começa e o método [**CBaseRenderer:: OnWaitEnd**](cbaserenderer-onwaitend.md) quando a espera é concluída.</span><span class="sxs-lookup"><span data-stu-id="7ac38-124">This method calls the [**CBaseRenderer::OnWaitStart**](cbaserenderer-onwaitstart.md) method when the wait begins, and the [**CBaseRenderer::OnWaitEnd**](cbaserenderer-onwaitend.md) method when the wait is done.</span></span> <span data-ttu-id="7ac38-125">Nenhum método faz nada na classe base, mas a classe derivada pode substituí-los.</span><span class="sxs-lookup"><span data-stu-id="7ac38-125">Neither method does anything in the base class, but the derived class can override them.</span></span>

## <a name="requirements"></a><span data-ttu-id="7ac38-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7ac38-126">Requirements</span></span>



| <span data-ttu-id="7ac38-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="7ac38-127">Requirement</span></span> | <span data-ttu-id="7ac38-128">Valor</span><span class="sxs-lookup"><span data-stu-id="7ac38-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7ac38-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7ac38-129">Header</span></span><br/>  | <dl> <span data-ttu-id="7ac38-130"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7ac38-130"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="7ac38-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7ac38-131">Library</span></span><br/> | <dl> <span data-ttu-id="7ac38-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7ac38-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7ac38-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="7ac38-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7ac38-134">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="7ac38-134">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




