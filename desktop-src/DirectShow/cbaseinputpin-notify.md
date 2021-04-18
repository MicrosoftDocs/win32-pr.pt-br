---
description: 'O método Notify notifica o PIN de que uma alteração de qualidade é solicitada. Esse método implementa o método IQualityControl:: Notify.'
ms.assetid: 76124321-0d2d-4fee-a08a-4db23078e8df
title: Método CBaseInputPin. Notify (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.Notify
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: a5ae7ca47c5adc11c87a739e8736ba327dc0b65f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105764583"
---
# <a name="cbaseinputpinnotify-method"></a><span data-ttu-id="e2fe4-104">Método CBaseInputPin. Notify</span><span class="sxs-lookup"><span data-stu-id="e2fe4-104">CBaseInputPin.Notify method</span></span>

<span data-ttu-id="e2fe4-105">O `Notify` método notifica o PIN de que uma alteração de qualidade é solicitada.</span><span class="sxs-lookup"><span data-stu-id="e2fe4-105">The `Notify` method notifies the pin that a quality change is requested.</span></span> <span data-ttu-id="e2fe4-106">Esse método implementa o método [**IQualityControl:: Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) .</span><span class="sxs-lookup"><span data-stu-id="e2fe4-106">This method implements the [**IQualityControl::Notify**](/windows/desktop/api/Strmif/nf-strmif-iqualitycontrol-notify) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2fe4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e2fe4-107">Syntax</span></span>


```C++
HRESULT Notify(
   IBaseFilter *pSelf,
   Quality     q
);
```



## <a name="parameters"></a><span data-ttu-id="e2fe4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e2fe4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2fe4-109">*pSelf*</span><span class="sxs-lookup"><span data-stu-id="e2fe4-109">*pSelf*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fe4-110">Ponteiro para o filtro que está enviando a mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e2fe4-110">Pointer to the filter that is sending the quality-control message.</span></span>

</dd> <dt>

<span data-ttu-id="e2fe4-111">*perguntas*</span><span class="sxs-lookup"><span data-stu-id="e2fe4-111">*q*</span></span> 
</dt> <dd>

<span data-ttu-id="e2fe4-112">Estrutura de [**qualidade**](/windows/win32/api/strmif/ns-strmif-quality) que contém a mensagem de controle de qualidade.</span><span class="sxs-lookup"><span data-stu-id="e2fe4-112">[**Quality**](/windows/win32/api/strmif/ns-strmif-quality) structure that contains the quality-control message.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2fe4-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="e2fe4-113">Return value</span></span>

<span data-ttu-id="e2fe4-114">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e2fe4-114">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e2fe4-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="e2fe4-115">Remarks</span></span>

<span data-ttu-id="e2fe4-116">Os filtros normalmente passam mensagens de controle de qualidade para um pino de saída upstream, não para um pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="e2fe4-116">Filters usually pass quality-control messages to an upstream output pin, not to an input pin.</span></span> <span data-ttu-id="e2fe4-117">Portanto, esse método retorna S \_ OK sem fazer nada.</span><span class="sxs-lookup"><span data-stu-id="e2fe4-117">Therefore, this method returns S\_OK without doing anything.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2fe4-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e2fe4-118">Requirements</span></span>



| <span data-ttu-id="e2fe4-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="e2fe4-119">Requirement</span></span> | <span data-ttu-id="e2fe4-120">Valor</span><span class="sxs-lookup"><span data-stu-id="e2fe4-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2fe4-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e2fe4-121">Header</span></span><br/>  | <dl> <span data-ttu-id="e2fe4-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e2fe4-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e2fe4-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e2fe4-123">Library</span></span><br/> | <dl> <span data-ttu-id="e2fe4-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e2fe4-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e2fe4-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="e2fe4-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2fe4-126">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="e2fe4-126">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> <dt>

[<span data-ttu-id="e2fe4-127">Gerenciamento de controle de qualidade</span><span class="sxs-lookup"><span data-stu-id="e2fe4-127">Quality-Control Management</span></span>](quality-control-management.md)
</dt> </dl>

 

 




