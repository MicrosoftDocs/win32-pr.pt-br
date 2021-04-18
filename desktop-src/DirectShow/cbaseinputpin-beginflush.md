---
description: 'O método CBaseInputPin inicia uma operação de liberação. Esse método implementa o método IPin:: BeginFlush.'
ms.assetid: 3f149d4f-765b-44c1-87e5-6313f6a4d50d
title: Método CBaseInputPin. BeginFlush (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 93c0f687daf65e91443f4f59896d641b9b0cfd43
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756200"
---
# <a name="cbaseinputpinbeginflush-method"></a><span data-ttu-id="ea0ce-104">Método CBaseInputPin. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="ea0ce-104">CBaseInputPin.BeginFlush method</span></span>

<span data-ttu-id="ea0ce-105">O `CBaseInputPin` método inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="ea0ce-105">The `CBaseInputPin` method begins a flush operation.</span></span> <span data-ttu-id="ea0ce-106">Esse método implementa o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="ea0ce-106">This method implements the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="ea0ce-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ea0ce-107">Syntax</span></span>


```C++
HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="ea0ce-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ea0ce-108">Parameters</span></span>

<span data-ttu-id="ea0ce-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="ea0ce-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="ea0ce-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ea0ce-110">Return value</span></span>

<span data-ttu-id="ea0ce-111">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="ea0ce-111">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="ea0ce-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="ea0ce-112">Remarks</span></span>

<span data-ttu-id="ea0ce-113">Esse método define o sinalizador [**CBaseInputPin:: m \_ BFlushing**](cbaseinputpin-m-bflushing.md) como **true**, o que faz com que o método [**CBaseInputPin:: Receive**](cbaseinputpin-receive.md) rejeite mais exemplos.</span><span class="sxs-lookup"><span data-stu-id="ea0ce-113">This method sets the [**CBaseInputPin::m\_bFlushing**](cbaseinputpin-m-bflushing.md) flag to **TRUE**, which causes the [**CBaseInputPin::Receive**](cbaseinputpin-receive.md) method to reject any more samples.</span></span>

<span data-ttu-id="ea0ce-114">A classe derivada deve substituir esse método e executar as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="ea0ce-114">The derived class must override this method and perform the following steps:</span></span>

1.  <span data-ttu-id="ea0ce-115">Chame o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) nos Pins de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="ea0ce-115">Call the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method on downstream input pins.</span></span> <span data-ttu-id="ea0ce-116">Se o PIN ainda não tiver entregue nenhuma amostra de mídia downstream, você poderá ignorar esta etapa.</span><span class="sxs-lookup"><span data-stu-id="ea0ce-116">If the pin has not yet delivered any media samples downstream, you can skip this step.</span></span> <span data-ttu-id="ea0ce-117">Se os Pins de saída derivarem da classe [**CBaseOutputPin**](cbaseoutputpin.md) , você poderá chamar o método [**CBaseOutputPin::D eliverbeginflush**](cbaseoutputpin-deliverbeginflush.md) .</span><span class="sxs-lookup"><span data-stu-id="ea0ce-117">If your output pins derive from the [**CBaseOutputPin**](cbaseoutputpin.md) class, you can call the [**CBaseOutputPin::DeliverBeginFlush**](cbaseoutputpin-deliverbeginflush.md) method.</span></span>
2.  <span data-ttu-id="ea0ce-118">Chame o método da classe base.</span><span class="sxs-lookup"><span data-stu-id="ea0ce-118">Call the base class method.</span></span>
3.  <span data-ttu-id="ea0ce-119">Iniciar descartar dados na fila.</span><span class="sxs-lookup"><span data-stu-id="ea0ce-119">Begin discarding queued data.</span></span>
4.  <span data-ttu-id="ea0ce-120">Retornar de todas as chamadas bloqueadas para o método **Receive** .</span><span class="sxs-lookup"><span data-stu-id="ea0ce-120">Return from any blocked calls to the **Receive** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea0ce-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ea0ce-121">Requirements</span></span>



| <span data-ttu-id="ea0ce-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="ea0ce-122">Requirement</span></span> | <span data-ttu-id="ea0ce-123">Valor</span><span class="sxs-lookup"><span data-stu-id="ea0ce-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ea0ce-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ea0ce-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ea0ce-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ea0ce-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ea0ce-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ea0ce-126">Library</span></span><br/> | <dl> <span data-ttu-id="ea0ce-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ea0ce-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ea0ce-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="ea0ce-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ea0ce-129">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="ea0ce-129">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




