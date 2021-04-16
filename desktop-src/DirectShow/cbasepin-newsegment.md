---
description: 'O método NewSegment notifica o PIN de que amostras de mídia recebidas após essa chamada são agrupadas como um segmento. Implementa o método IPin:: NewSegment.'
ms.assetid: e334d5a7-0398-496c-882c-bf73e6545867
title: Método CBasePin. NewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBasePin.NewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f128ce8cb2fee5479efeddd5932d0392b92a6fc
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751263"
---
# <a name="cbasepinnewsegment-method"></a><span data-ttu-id="21bfc-104">Método CBasePin. NewSegment</span><span class="sxs-lookup"><span data-stu-id="21bfc-104">CBasePin.NewSegment method</span></span>

<span data-ttu-id="21bfc-105">O `NewSegment` método notifica o PIN de que as amostras de mídia recebidas após essa chamada são agrupadas como um segmento.</span><span class="sxs-lookup"><span data-stu-id="21bfc-105">The `NewSegment` method notifies the pin that media samples received after this call are grouped as a segment.</span></span> <span data-ttu-id="21bfc-106">Implementa o método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) .</span><span class="sxs-lookup"><span data-stu-id="21bfc-106">Implements the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="21bfc-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="21bfc-107">Syntax</span></span>


```C++
HRESULT NewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="21bfc-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="21bfc-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="21bfc-109">*tStart*</span><span class="sxs-lookup"><span data-stu-id="21bfc-109">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="21bfc-110">Iniciando a posição de mídia do segmento, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="21bfc-110">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="21bfc-111">*tStop*</span><span class="sxs-lookup"><span data-stu-id="21bfc-111">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="21bfc-112">Terminar a posição de mídia do segmento, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="21bfc-112">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="21bfc-113">*dRate*</span><span class="sxs-lookup"><span data-stu-id="21bfc-113">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="21bfc-114">Taxa na qual esse segmento deve ser processado, como uma porcentagem da taxa original.</span><span class="sxs-lookup"><span data-stu-id="21bfc-114">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="21bfc-115">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="21bfc-115">Return value</span></span>

<span data-ttu-id="21bfc-116">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="21bfc-116">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="21bfc-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="21bfc-117">Remarks</span></span>

<span data-ttu-id="21bfc-118">Esse método define as variáveis de membro [**CBasePin:: m \_ tStart**](cbasepin-m-tstart.md), [**CBasePin:: m \_ tStop**](cbasepin-m-tstop.md)e [**CBasePin:: m \_ drate**](cbasepin-m-drate.md) .</span><span class="sxs-lookup"><span data-stu-id="21bfc-118">This method sets the [**CBasePin::m\_tStart**](cbasepin-m-tstart.md), [**CBasePin::m\_tStop**](cbasepin-m-tstop.md), and [**CBasePin::m\_dRate**](cbasepin-m-drate.md) member variables.</span></span> <span data-ttu-id="21bfc-119">Na classe derivada, substitua esse método para passar o downstream de notificação.</span><span class="sxs-lookup"><span data-stu-id="21bfc-119">In your derived class, override this method to pass the notification downstream.</span></span>

## <a name="requirements"></a><span data-ttu-id="21bfc-120">Requisitos</span><span class="sxs-lookup"><span data-stu-id="21bfc-120">Requirements</span></span>



| <span data-ttu-id="21bfc-121">Requisito</span><span class="sxs-lookup"><span data-stu-id="21bfc-121">Requirement</span></span> | <span data-ttu-id="21bfc-122">Valor</span><span class="sxs-lookup"><span data-stu-id="21bfc-122">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="21bfc-123">parâmetro</span><span class="sxs-lookup"><span data-stu-id="21bfc-123">Header</span></span><br/>  | <dl> <span data-ttu-id="21bfc-124"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="21bfc-124"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="21bfc-125">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="21bfc-125">Library</span></span><br/> | <dl> <span data-ttu-id="21bfc-126"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="21bfc-126"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="21bfc-127">Confira também</span><span class="sxs-lookup"><span data-stu-id="21bfc-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21bfc-128">**Classe CBasePin**</span><span class="sxs-lookup"><span data-stu-id="21bfc-128">**CBasePin Class**</span></span>](cbasepin.md)
</dt> </dl>

 

 




