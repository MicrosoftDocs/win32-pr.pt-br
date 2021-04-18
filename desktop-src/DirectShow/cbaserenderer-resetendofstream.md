---
description: O método ResetEndOfStream redefine os sinalizadores de fim de fluxo.
ms.assetid: 80f6d49b-a825-4c3c-b693-7b1d9298f541
title: Método CBaseRenderer. ResetEndOfStream (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.ResetEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0269ee2dfafea9265b5eeb82caa4c39f8d91320c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756604"
---
# <a name="cbaserendererresetendofstream-method"></a><span data-ttu-id="6492d-103">Método CBaseRenderer. ResetEndOfStream</span><span class="sxs-lookup"><span data-stu-id="6492d-103">CBaseRenderer.ResetEndOfStream method</span></span>

<span data-ttu-id="6492d-104">O `ResetEndOfStream` método redefine os sinalizadores de fim de fluxo.</span><span class="sxs-lookup"><span data-stu-id="6492d-104">The `ResetEndOfStream` method resets the end-of-stream flags.</span></span>

## <a name="syntax"></a><span data-ttu-id="6492d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6492d-105">Syntax</span></span>


```C++
virtual HRESULT ResetEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="6492d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6492d-106">Parameters</span></span>

<span data-ttu-id="6492d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6492d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6492d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6492d-108">Return value</span></span>

<span data-ttu-id="6492d-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6492d-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6492d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6492d-110">Remarks</span></span>

<span data-ttu-id="6492d-111">Esse método limpa a condição de fim de fluxo anterior.</span><span class="sxs-lookup"><span data-stu-id="6492d-111">This method clears the previous end-of-stream condition.</span></span> <span data-ttu-id="6492d-112">Nesse ponto, o filtro pode receber novos dados.</span><span class="sxs-lookup"><span data-stu-id="6492d-112">At that point, the filter can receive new data.</span></span> <span data-ttu-id="6492d-113">Os métodos [**CBaseRenderer:: Stop**](cbaserenderer-stop.md) e [**CBaseRenderer:: BeginFlush**](cbaserenderer-beginflush.md) chamam esse método.</span><span class="sxs-lookup"><span data-stu-id="6492d-113">The [**CBaseRenderer::Stop**](cbaserenderer-stop.md) and [**CBaseRenderer::BeginFlush**](cbaserenderer-beginflush.md) methods call this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6492d-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6492d-114">Requirements</span></span>



| <span data-ttu-id="6492d-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6492d-115">Requirement</span></span> | <span data-ttu-id="6492d-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6492d-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6492d-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6492d-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6492d-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6492d-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6492d-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6492d-119">Library</span></span><br/> | <dl> <span data-ttu-id="6492d-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6492d-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6492d-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6492d-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6492d-122">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="6492d-122">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




