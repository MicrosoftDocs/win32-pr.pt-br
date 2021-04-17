---
description: 'Interrompe o filtro. Esse método implementa o método IMediaFilter:: Stop.'
ms.assetid: e95537d6-b3ec-49a4-aa28-333d69eff3bb
title: Método CTransformFilter. Stop (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.Stop
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2a7f7ea0f80095cd63f9708f12a42146260f2f8f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812789"
---
# <a name="ctransformfilterstop-method"></a><span data-ttu-id="5668d-104">Método CTransformFilter. Stop</span><span class="sxs-lookup"><span data-stu-id="5668d-104">CTransformFilter.Stop method</span></span>

<span data-ttu-id="5668d-105">Interrompe o filtro.</span><span class="sxs-lookup"><span data-stu-id="5668d-105">Stops the filter.</span></span> <span data-ttu-id="5668d-106">Esse método implementa o método [**IMediaFilter:: Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) .</span><span class="sxs-lookup"><span data-stu-id="5668d-106">This method implements the [**IMediaFilter::Stop**](/windows/desktop/api/Strmif/nf-strmif-imediafilter-stop) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5668d-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5668d-107">Syntax</span></span>


```C++
HRESULT Stop();
```



## <a name="parameters"></a><span data-ttu-id="5668d-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5668d-108">Parameters</span></span>

<span data-ttu-id="5668d-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5668d-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5668d-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5668d-110">Return value</span></span>

<span data-ttu-id="5668d-111">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5668d-111">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="5668d-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="5668d-112">Remarks</span></span>

<span data-ttu-id="5668d-113">Depois que esse método desconfirma ambos os alocadores, ele chama o método [**StopStreaming**](ctransformfilter-stopstreaming.md) .</span><span class="sxs-lookup"><span data-stu-id="5668d-113">After this method decommits both allocators, it calls the [**StopStreaming**](ctransformfilter-stopstreaming.md) method.</span></span> <span data-ttu-id="5668d-114">O método **StopStreaming** não faz nada na classe base, mas a classe derivada pode substituí-la.</span><span class="sxs-lookup"><span data-stu-id="5668d-114">The **StopStreaming** method does nothing in the base class, but the derived class can override it.</span></span>

## <a name="requirements"></a><span data-ttu-id="5668d-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5668d-115">Requirements</span></span>



| <span data-ttu-id="5668d-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="5668d-116">Requirement</span></span> | <span data-ttu-id="5668d-117">Valor</span><span class="sxs-lookup"><span data-stu-id="5668d-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5668d-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5668d-118">Header</span></span><br/>  | <dl> <span data-ttu-id="5668d-119"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5668d-119"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5668d-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5668d-120">Library</span></span><br/> | <dl> <span data-ttu-id="5668d-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5668d-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5668d-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="5668d-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5668d-123">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="5668d-123">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




