---
description: O método pause pausa o filtro. Esse método implementa o método IMediaFilter::P ause.
ms.assetid: cfb7d532-6c00-49a1-a48d-4dadaca39a0f
title: Método CBaseFilter. PAUSE (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 43a90e78084f2320d0df7da806b6138571c9a5bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750899"
---
# <a name="cbasefilterpause-method"></a><span data-ttu-id="e4325-104">Método CBaseFilter. Pause</span><span class="sxs-lookup"><span data-stu-id="e4325-104">CBaseFilter.Pause method</span></span>

<span data-ttu-id="e4325-105">O `Pause` método pausa o filtro.</span><span class="sxs-lookup"><span data-stu-id="e4325-105">The `Pause` method pauses the filter.</span></span> <span data-ttu-id="e4325-106">Esse método implementa o método [**IMediaFilter::P ause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) .</span><span class="sxs-lookup"><span data-stu-id="e4325-106">This method implements the [**IMediaFilter::Pause**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-pause) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e4325-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e4325-107">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="e4325-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e4325-108">Parameters</span></span>

<span data-ttu-id="e4325-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e4325-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e4325-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e4325-110">Return value</span></span>

<span data-ttu-id="e4325-111">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="e4325-111">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="e4325-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="e4325-112">Remarks</span></span>

<span data-ttu-id="e4325-113">Esse método chama o método [**CBasePin:: active**](cbasepin-active.md) em cada um dos Pins conectados do filtro.</span><span class="sxs-lookup"><span data-stu-id="e4325-113">This method calls the [**CBasePin::Active**](cbasepin-active.md) method on each of the filter's connected pins.</span></span>

## <a name="requirements"></a><span data-ttu-id="e4325-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e4325-114">Requirements</span></span>



| <span data-ttu-id="e4325-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="e4325-115">Requirement</span></span> | <span data-ttu-id="e4325-116">Valor</span><span class="sxs-lookup"><span data-stu-id="e4325-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e4325-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e4325-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e4325-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e4325-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e4325-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e4325-119">Library</span></span><br/> | <dl> <span data-ttu-id="e4325-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e4325-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e4325-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="e4325-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e4325-122">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="e4325-122">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




