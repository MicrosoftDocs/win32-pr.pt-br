---
description: O método DeliverNewSegment entrega uma notificação de novo segmento para o PIN de entrada conectado.
ms.assetid: 304f0267-88e0-4642-98a2-68ce973bdeab
title: Método CBaseOutputPin. DeliverNewSegment (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverNewSegment
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3eb6d31a50095affdf38d44b69040304674ec6fe
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758245"
---
# <a name="cbaseoutputpindelivernewsegment-method"></a><span data-ttu-id="571aa-103">Método CBaseOutputPin. DeliverNewSegment</span><span class="sxs-lookup"><span data-stu-id="571aa-103">CBaseOutputPin.DeliverNewSegment method</span></span>

<span data-ttu-id="571aa-104">O `DeliverNewSegment` método fornece uma notificação de novo segmento para o PIN de entrada conectado.</span><span class="sxs-lookup"><span data-stu-id="571aa-104">The `DeliverNewSegment` method delivers a new-segment notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="571aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="571aa-105">Syntax</span></span>


```C++
virtual HRESULT DeliverNewSegment(
   REFERENCE_TIME tStart,
   REFERENCE_TIME tStop,
   double         dRate
);
```



## <a name="parameters"></a><span data-ttu-id="571aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="571aa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="571aa-107">*tStart*</span><span class="sxs-lookup"><span data-stu-id="571aa-107">*tStart*</span></span> 
</dt> <dd>

<span data-ttu-id="571aa-108">Iniciando a posição de mídia do segmento, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="571aa-108">Starting media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="571aa-109">*tStop*</span><span class="sxs-lookup"><span data-stu-id="571aa-109">*tStop*</span></span> 
</dt> <dd>

<span data-ttu-id="571aa-110">Terminar a posição de mídia do segmento, em unidades de 100 a nanossegundos.</span><span class="sxs-lookup"><span data-stu-id="571aa-110">End media position of the segment, in 100-nanosecond units.</span></span>

</dd> <dt>

<span data-ttu-id="571aa-111">*dRate*</span><span class="sxs-lookup"><span data-stu-id="571aa-111">*dRate*</span></span> 
</dt> <dd>

<span data-ttu-id="571aa-112">Taxa na qual esse segmento deve ser processado, como uma porcentagem da taxa original.</span><span class="sxs-lookup"><span data-stu-id="571aa-112">Rate at which this segment should be processed, as a percentage of the original rate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="571aa-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="571aa-113">Return value</span></span>

<span data-ttu-id="571aa-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="571aa-114">Returns an **HRESULT** value.</span></span> <span data-ttu-id="571aa-115">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="571aa-115">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="571aa-116">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="571aa-116">Return code</span></span>                                                                                           | <span data-ttu-id="571aa-117">Descrição</span><span class="sxs-lookup"><span data-stu-id="571aa-117">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="571aa-118"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="571aa-118"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="571aa-119">Êxito.</span><span class="sxs-lookup"><span data-stu-id="571aa-119">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="571aa-120"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="571aa-120"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="571aa-121">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="571aa-121">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="571aa-122">Comentários</span><span class="sxs-lookup"><span data-stu-id="571aa-122">Remarks</span></span>

<span data-ttu-id="571aa-123">Esse método chama o método [**IPin:: NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="571aa-123">This method calls the [**IPin::NewSegment**](/windows/desktop/api/Strmif/nf-strmif-ipin-newsegment) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="571aa-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="571aa-124">Requirements</span></span>



| <span data-ttu-id="571aa-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="571aa-125">Requirement</span></span> | <span data-ttu-id="571aa-126">Valor</span><span class="sxs-lookup"><span data-stu-id="571aa-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="571aa-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="571aa-127">Header</span></span><br/>  | <dl> <span data-ttu-id="571aa-128"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="571aa-128"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="571aa-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="571aa-129">Library</span></span><br/> | <dl> <span data-ttu-id="571aa-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="571aa-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="571aa-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="571aa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="571aa-132">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="571aa-132">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




