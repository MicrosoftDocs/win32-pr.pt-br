---
description: 'O método CompleteConnect conclui uma conexão com um pino de saída. Esse método substitui o método CBasePin:: CompleteConnect.'
ms.assetid: 32d95815-e018-4724-8cf3-8cd093ede517
title: Método CRendererInputPin. CompleteConnect (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 2e868693308d40fb786f201a9d7f056dd88326ab
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748623"
---
# <a name="crendererinputpincompleteconnect-method"></a><span data-ttu-id="6571c-104">Método CRendererInputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="6571c-104">CRendererInputPin.CompleteConnect method</span></span>

<span data-ttu-id="6571c-105">O `CompleteConnect` método conclui uma conexão com um pino de saída.</span><span class="sxs-lookup"><span data-stu-id="6571c-105">The `CompleteConnect` method completes a connection to an output pin.</span></span> <span data-ttu-id="6571c-106">Esse método substitui o método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="6571c-106">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6571c-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6571c-107">Syntax</span></span>


```C++
HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="6571c-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6571c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6571c-109">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="6571c-109">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="6571c-110">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de saída</span><span class="sxs-lookup"><span data-stu-id="6571c-110">Pointer to the output pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6571c-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6571c-111">Return value</span></span>

<span data-ttu-id="6571c-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6571c-112">Returns an **HRESULT** value.</span></span>

## <a name="requirements"></a><span data-ttu-id="6571c-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6571c-113">Requirements</span></span>



| <span data-ttu-id="6571c-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="6571c-114">Requirement</span></span> | <span data-ttu-id="6571c-115">Valor</span><span class="sxs-lookup"><span data-stu-id="6571c-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6571c-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6571c-116">Header</span></span><br/>  | <dl> <span data-ttu-id="6571c-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6571c-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6571c-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6571c-118">Library</span></span><br/> | <dl> <span data-ttu-id="6571c-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6571c-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6571c-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="6571c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6571c-121">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="6571c-121">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




