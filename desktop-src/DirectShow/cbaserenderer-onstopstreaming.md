---
description: O método OnStopStreaming é chamado quando o filtro para de streaming.
ms.assetid: d882fec8-09e1-4d36-a09c-44568e743da3
title: Método CBaseRenderer. OnStopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.OnStopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 417a18ca53240dce0e4ed6d40f551c45c24b0f1c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764572"
---
# <a name="cbaserendereronstopstreaming-method"></a><span data-ttu-id="6986a-103">Método CBaseRenderer. OnStopStreaming</span><span class="sxs-lookup"><span data-stu-id="6986a-103">CBaseRenderer.OnStopStreaming method</span></span>

<span data-ttu-id="6986a-104">O `OnStopStreaming` método é chamado quando o filtro para de streaming.</span><span class="sxs-lookup"><span data-stu-id="6986a-104">The `OnStopStreaming` method is called when the filter stops streaming.</span></span>

## <a name="syntax"></a><span data-ttu-id="6986a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6986a-105">Syntax</span></span>


```C++
virtual HRESULT OnStopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="6986a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6986a-106">Parameters</span></span>

<span data-ttu-id="6986a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6986a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6986a-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6986a-108">Return value</span></span>

<span data-ttu-id="6986a-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="6986a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="6986a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6986a-110">Remarks</span></span>

<span data-ttu-id="6986a-111">O método [**CBaseRenderer:: StopStreaming**](cbaserenderer-stopstreaming.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="6986a-111">The [**CBaseRenderer::StopStreaming**](cbaserenderer-stopstreaming.md) method calls this method.</span></span> <span data-ttu-id="6986a-112">Ele não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="6986a-112">It does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="6986a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6986a-113">Requirements</span></span>



| <span data-ttu-id="6986a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6986a-114">Requirement</span></span> | <span data-ttu-id="6986a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6986a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6986a-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6986a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6986a-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6986a-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6986a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6986a-118">Library</span></span><br/> | <dl> <span data-ttu-id="6986a-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6986a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6986a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6986a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6986a-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="6986a-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




