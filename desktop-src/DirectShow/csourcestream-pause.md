---
description: O método pause sinaliza o thread de streaming para se tornar ativo.
ms.assetid: c97da113-c5a7-422d-9215-70b556e0b8ca
title: Método CSourceStream. PAUSE (origem. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceStream.Pause
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b6f7cd3b38144edebd98ca655b32bf6092f44269
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759560"
---
# <a name="csourcestreampause-method"></a><span data-ttu-id="2ff8c-103">Método CSourceStream. Pause</span><span class="sxs-lookup"><span data-stu-id="2ff8c-103">CSourceStream.Pause method</span></span>

<span data-ttu-id="2ff8c-104">O `Pause` método sinaliza o thread de streaming para se tornar ativo.</span><span class="sxs-lookup"><span data-stu-id="2ff8c-104">The `Pause` method signals the streaming thread to become active.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff8c-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2ff8c-105">Syntax</span></span>


```C++
HRESULT Pause();
```



## <a name="parameters"></a><span data-ttu-id="2ff8c-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2ff8c-106">Parameters</span></span>

<span data-ttu-id="2ff8c-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2ff8c-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2ff8c-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2ff8c-108">Return value</span></span>

<span data-ttu-id="2ff8c-109">Retorna S \_ OK ou E \_ inesperado.</span><span class="sxs-lookup"><span data-stu-id="2ff8c-109">Returns S\_OK or E\_UNEXPECTED.</span></span>

## <a name="remarks"></a><span data-ttu-id="2ff8c-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="2ff8c-110">Remarks</span></span>

<span data-ttu-id="2ff8c-111">O método [**CSourceStream:: active**](csourcestream-active.md) chama esse método.</span><span class="sxs-lookup"><span data-stu-id="2ff8c-111">The [**CSourceStream::Active**](csourcestream-active.md) method calls this method.</span></span> <span data-ttu-id="2ff8c-112">Quando o método [**CSourceStream:: ThreadProc**](csourcestream-threadproc.md) recebe essa solicitação, ele chama o método [**CSourceStream::D obufferprocessingloop**](csourcestream-dobufferprocessingloop.md) .</span><span class="sxs-lookup"><span data-stu-id="2ff8c-112">When the [**CSourceStream::ThreadProc**](csourcestream-threadproc.md) method receives this request, it calls the [**CSourceStream::DoBufferProcessingLoop**](csourcestream-dobufferprocessingloop.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2ff8c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2ff8c-113">Requirements</span></span>



| <span data-ttu-id="2ff8c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="2ff8c-114">Requirement</span></span> | <span data-ttu-id="2ff8c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="2ff8c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2ff8c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2ff8c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="2ff8c-117"><dt>Source. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2ff8c-117"><dt>Source.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="2ff8c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2ff8c-118">Library</span></span><br/> | <dl> <span data-ttu-id="2ff8c-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2ff8c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2ff8c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="2ff8c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2ff8c-121">**Classe CSourceStream**</span><span class="sxs-lookup"><span data-stu-id="2ff8c-121">**CSourceStream Class**</span></span>](csourcestream.md)
</dt> </dl>

 

 




