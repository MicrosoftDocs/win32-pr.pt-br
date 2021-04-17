---
description: O método NewSegment notifica o filtro de que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento.
ms.assetid: 78ddaac7-9c1f-47b6-835d-dd16b1f5b01f
title: Método CTransformFilter. NewSegment (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0fd046288886d3e7619419dd591dd94310f56020
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752686"
---
# <a name="ctransformfilternewsegment-method"></a><span data-ttu-id="36a18-103">Método CTransformFilter. NewSegment</span><span class="sxs-lookup"><span data-stu-id="36a18-103">CTransformFilter.NewSegment method</span></span>

<span data-ttu-id="36a18-104">O `NewSegment` método notifica o filtro de que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento.</span><span class="sxs-lookup"><span data-stu-id="36a18-104">The `NewSegment` method notifies the filter that media samples received after this call are grouped as a segment.</span></span>

## <a name="syntax"></a><span data-ttu-id="36a18-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="36a18-105">Syntax</span></span>


```C++
virtual HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="36a18-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="36a18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="36a18-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="36a18-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="36a18-108">Hora de início do segmento, em relação à fonte original.</span><span class="sxs-lookup"><span data-stu-id="36a18-108">Start time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="36a18-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="36a18-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="36a18-110">Hora de parada do segmento, em relação à fonte original.</span><span class="sxs-lookup"><span data-stu-id="36a18-110">Stop time of the segment, relative to the original source.</span></span>

</dd> <dt>

<span data-ttu-id="36a18-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="36a18-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="36a18-112">Taxa em que o segmento deve ser processado.</span><span class="sxs-lookup"><span data-stu-id="36a18-112">Rate at which the segment should be processed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="36a18-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="36a18-113">Return value</span></span>

<span data-ttu-id="36a18-114">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="36a18-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="36a18-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="36a18-115">Remarks</span></span>

<span data-ttu-id="36a18-116">O método [**CTransformInputPin:: NewSegment**](ctransforminputpin-newsegment.md) do pino de entrada chama esse método.</span><span class="sxs-lookup"><span data-stu-id="36a18-116">The input pin's [**CTransformInputPin::NewSegment**](ctransforminputpin-newsegment.md) method calls this method.</span></span> <span data-ttu-id="36a18-117">Esse método entrega a `NewSegment` chamada para o pino de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="36a18-117">This method delivers the `NewSegment` call to the downstream input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="36a18-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="36a18-118">Requirements</span></span>



| <span data-ttu-id="36a18-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="36a18-119">Requirement</span></span> | <span data-ttu-id="36a18-120">Valor</span><span class="sxs-lookup"><span data-stu-id="36a18-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="36a18-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="36a18-121">Header</span></span><br/>  | <dl> <span data-ttu-id="36a18-122"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="36a18-122"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="36a18-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="36a18-123">Library</span></span><br/> | <dl> <span data-ttu-id="36a18-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="36a18-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="36a18-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="36a18-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="36a18-126">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="36a18-126">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




