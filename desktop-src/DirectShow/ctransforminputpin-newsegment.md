---
description: 'O método NewSegment notifica o PIN de que amostras de mídia recebidas após essa chamada são agrupadas como um segmento. Esse método implementa o método IPin:: NewSegment.'
ms.assetid: 8925b8b5-13dd-4127-82d8-96525bd4d6fc
title: Método CTransformInputPin. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformInputPin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 25c455fe5ec6ddf9157e991b70b468ace653daa9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759087"
---
# <a name="ctransforminputpinnewsegment-method"></a><span data-ttu-id="d8c76-104">Método CTransformInputPin. NewSegment</span><span class="sxs-lookup"><span data-stu-id="d8c76-104">CTransformInputPin.NewSegment method</span></span>

<span data-ttu-id="d8c76-105">O `NewSegment` método notifica o PIN de que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento.</span><span class="sxs-lookup"><span data-stu-id="d8c76-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="d8c76-106">Esse método implementa o método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="d8c76-106">This method implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="d8c76-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="d8c76-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="d8c76-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="d8c76-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d8c76-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="d8c76-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c76-110">Hora de início do segmento.</span><span class="sxs-lookup"><span data-stu-id="d8c76-110">Start time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="d8c76-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="d8c76-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c76-112">Hora de parada do segmento.</span><span class="sxs-lookup"><span data-stu-id="d8c76-112">Stop time of the segment.</span></span>

</dd> <dt>

<span data-ttu-id="d8c76-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="d8c76-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="d8c76-114">Taxa do segmento.</span><span class="sxs-lookup"><span data-stu-id="d8c76-114">Rate of the segment.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d8c76-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="d8c76-115">Return value</span></span>

<span data-ttu-id="d8c76-116">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="d8c76-116">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="d8c76-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="d8c76-117">Remarks</span></span>

<span data-ttu-id="d8c76-118">Esse método substitui o método [**CBasePin:: NewSegment**](cbasepin-newsegment.md) .</span><span class="sxs-lookup"><span data-stu-id="d8c76-118">This method overrides the [**CBasePin::NewSegment**](cbasepin-newsegment.md) method.</span></span> <span data-ttu-id="d8c76-119">Ele chama o método [**CTransformFilter:: NewSegment**](ctransformfilter-newsegment.md) do filtro para entregar a chamada downstream.</span><span class="sxs-lookup"><span data-stu-id="d8c76-119">It calls the filter's [**CTransformFilter::NewSegment**](ctransformfilter-newsegment.md) method to deliver the call downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="d8c76-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="d8c76-120">Requirements</span></span>



| <span data-ttu-id="d8c76-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="d8c76-121">Requirement</span></span> | <span data-ttu-id="d8c76-122">Valor</span><span class="sxs-lookup"><span data-stu-id="d8c76-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d8c76-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="d8c76-123">Header</span></span><br/>  | <dl> <span data-ttu-id="d8c76-124"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="d8c76-124"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="d8c76-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="d8c76-125">Library</span></span><br/> | <dl> <span data-ttu-id="d8c76-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="d8c76-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




