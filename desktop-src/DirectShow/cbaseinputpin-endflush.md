---
description: 'O método EndFlush termina uma operação de liberação. Implementa o método IPin:: EndFlush.'
ms.assetid: d4110eb4-26c5-4312-b33f-4af31e1bf2ae
title: Método CBaseInputPin. EndFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.EndFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 403ee5aa100309084090dc241724067f9dd3aa5c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751915"
---
# <a name="cbaseinputpinendflush-method"></a><span data-ttu-id="32045-104">Método CBaseInputPin. EndFlush</span><span class="sxs-lookup"><span data-stu-id="32045-104">CBaseInputPin.EndFlush method</span></span>

<span data-ttu-id="32045-105">O `EndFlush` método encerra uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="32045-105">The `EndFlush` method ends a flush operation.</span></span> <span data-ttu-id="32045-106">Implementa o método [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) .</span><span class="sxs-lookup"><span data-stu-id="32045-106">Implements the [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="32045-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="32045-107">Syntax</span></span>


```C++
HRESULT EndFlush();
```



## <a name="parameters"></a><span data-ttu-id="32045-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="32045-108">Parameters</span></span>

<span data-ttu-id="32045-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="32045-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="32045-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="32045-110">Return value</span></span>

<span data-ttu-id="32045-111">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="32045-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="32045-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="32045-112">Remarks</span></span>

<span data-ttu-id="32045-113">Esse método define o sinalizador [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) como **true**, o que permite que o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) aceite amostras.</span><span class="sxs-lookup"><span data-stu-id="32045-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which enables the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to accept samples.</span></span>

<span data-ttu-id="32045-114">A classe derivada deve substituir esse método e executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="32045-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="32045-115">Libere todos os dados armazenados em buffer e aguarde a descartação de todas as amostras em fila.</span><span class="sxs-lookup"><span data-stu-id="32045-115">Free any buffered data and wait for all queued samples to be discarded.</span></span>
2.  <span data-ttu-id="32045-116">Desmarque todas as notificações pendentes do [**EC \_ Complete**](ec-complete.md) .</span><span class="sxs-lookup"><span data-stu-id="32045-116">Clear any pending [**EC\_COMPLETE**](ec-complete.md) notifications.</span></span>
3.  <span data-ttu-id="32045-117">Chame o método da classe base.</span><span class="sxs-lookup"><span data-stu-id="32045-117">Call the base class method.</span></span>
4.  <span data-ttu-id="32045-118">Chame [**IPin:: EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) em Pins de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="32045-118">Call [**IPin::EndFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-endflush) on downstream input pins.</span></span> <span data-ttu-id="32045-119">Se o PIN ainda não tiver entregue nenhuma amostra de mídia downstream, você poderá ignorar esta etapa.</span><span class="sxs-lookup"><span data-stu-id="32045-119">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="32045-120">Se os Pins de saída derivarem da classe [**CBaseOutputPin**](cbaseoutputpin.md) , você poderá chamar o método [**CBaseOutputPin::D eliverendflush**](cbaseoutputpin-deliverendflush.md) .</span><span class="sxs-lookup"><span data-stu-id="32045-120">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverEndFlush**](cbaseoutputpin-deliverendflush.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="32045-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="32045-121">Requirements</span></span>



| <span data-ttu-id="32045-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="32045-122">Requirement</span></span> | <span data-ttu-id="32045-123">Valor</span><span class="sxs-lookup"><span data-stu-id="32045-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="32045-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="32045-124">Header</span></span><br/>  | <dl> <span data-ttu-id="32045-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="32045-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="32045-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="32045-126">Library</span></span><br/> | <dl> <span data-ttu-id="32045-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="32045-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="32045-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="32045-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="32045-129">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="32045-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




