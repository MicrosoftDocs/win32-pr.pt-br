---
description: O método StartStreaming inicia o streaming quando o filtro alterna para um estado de execução.
ms.assetid: 198e9c1b-be69-4ba6-aa67-9f24ed080ab6
title: Método CBaseRenderer. StartStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StartStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7bf1fcb1cbfb651221296054493688b2d9f33bd3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771859"
---
# <a name="cbaserendererstartstreaming-method"></a><span data-ttu-id="089f7-103">Método CBaseRenderer. StartStreaming</span><span class="sxs-lookup"><span data-stu-id="089f7-103">CBaseRenderer.StartStreaming method</span></span>

<span data-ttu-id="089f7-104">O `StartStreaming` método inicia o streaming quando o filtro alterna para um estado de execução.</span><span class="sxs-lookup"><span data-stu-id="089f7-104">The `StartStreaming` method initiates streaming when the filter switches to a running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="089f7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="089f7-105">Syntax</span></span>


```C++
virtual HRESULT StartStreaming();
```



## <a name="parameters"></a><span data-ttu-id="089f7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="089f7-106">Parameters</span></span>

<span data-ttu-id="089f7-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="089f7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="089f7-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="089f7-108">Return value</span></span>

<span data-ttu-id="089f7-109">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="089f7-109">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="089f7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="089f7-110">Remarks</span></span>

<span data-ttu-id="089f7-111">Se o filtro tiver um exemplo, ele agendará o exemplo para renderização.</span><span class="sxs-lookup"><span data-stu-id="089f7-111">If the filter has a sample, it schedules the sample for rendering.</span></span> <span data-ttu-id="089f7-112">Caso contrário, se houver uma notificação de fim de fluxo pendente, o filtro enviará um evento de [**\_ conclusão de EC**](ec-complete.md) para o Gerenciador de gráfico de filtro.</span><span class="sxs-lookup"><span data-stu-id="089f7-112">Otherwise, if there is a pending end-of-stream notification, the filter sends an [**EC\_COMPLETE**](ec-complete.md) event to the filter graph manager.</span></span>

<span data-ttu-id="089f7-113">Esse método chama o método [**CBaseRenderer:: OnStartStreaming**](cbaserenderer-onstartstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="089f7-113">This method calls the [**CBaseRenderer::OnStartStreaming**](cbaserenderer-onstartstreaming.md) method.</span></span> <span data-ttu-id="089f7-114">Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="089f7-114">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="089f7-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="089f7-115">Requirements</span></span>



| <span data-ttu-id="089f7-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="089f7-116">Requirement</span></span> | <span data-ttu-id="089f7-117">Valor</span><span class="sxs-lookup"><span data-stu-id="089f7-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="089f7-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="089f7-118">Header</span></span><br/>  | <dl> <span data-ttu-id="089f7-119"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="089f7-119"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="089f7-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="089f7-120">Library</span></span><br/> | <dl> <span data-ttu-id="089f7-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="089f7-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="089f7-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="089f7-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="089f7-123">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="089f7-123">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




