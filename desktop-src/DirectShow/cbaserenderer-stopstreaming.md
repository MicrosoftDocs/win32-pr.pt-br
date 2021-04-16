---
description: O método StopStreaming interrompe o streaming quando o filtro sai do estado de execução.
ms.assetid: 465dde15-adec-46da-b8c8-56743e0cbd29
title: Método CBaseRenderer. StopStreaming (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.StopStreaming
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfd943de6a53383d7505fa9e884dcc152da6e5f4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750695"
---
# <a name="cbaserendererstopstreaming-method"></a><span data-ttu-id="9906a-103">Método CBaseRenderer. StopStreaming</span><span class="sxs-lookup"><span data-stu-id="9906a-103">CBaseRenderer.StopStreaming method</span></span>

<span data-ttu-id="9906a-104">O `StopStreaming` método interrompe o streaming quando o filtro sai do estado de execução.</span><span class="sxs-lookup"><span data-stu-id="9906a-104">The `StopStreaming` method halts streaming when the filter switches out of the running state.</span></span>

## <a name="syntax"></a><span data-ttu-id="9906a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9906a-105">Syntax</span></span>


```C++
virtual HRESULT StopStreaming();
```



## <a name="parameters"></a><span data-ttu-id="9906a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9906a-106">Parameters</span></span>

<span data-ttu-id="9906a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="9906a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="9906a-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9906a-108">Return value</span></span>

<span data-ttu-id="9906a-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="9906a-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9906a-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="9906a-110">Remarks</span></span>

<span data-ttu-id="9906a-111">Esse método chama o método [**CBaseRenderer:: OnStopStreaming**](cbaserenderer-onstopstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="9906a-111">This method calls the [**CBaseRenderer::OnStopStreaming**](cbaserenderer-onstopstreaming.md) method.</span></span> <span data-ttu-id="9906a-112">Esse método não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="9906a-112">That method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="9906a-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9906a-113">Requirements</span></span>



| <span data-ttu-id="9906a-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="9906a-114">Requirement</span></span> | <span data-ttu-id="9906a-115">Valor</span><span class="sxs-lookup"><span data-stu-id="9906a-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9906a-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9906a-116">Header</span></span><br/>  | <dl> <span data-ttu-id="9906a-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9906a-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="9906a-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9906a-118">Library</span></span><br/> | <dl> <span data-ttu-id="9906a-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9906a-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9906a-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="9906a-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9906a-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="9906a-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




