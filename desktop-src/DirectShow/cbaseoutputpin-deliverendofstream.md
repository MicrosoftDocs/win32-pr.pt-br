---
description: O método DeliverEndOfStream entrega uma notificação de fim de fluxo para o pino de entrada conectado.
ms.assetid: 5b564675-a1e0-4010-b35d-28315c262bcc
title: Método CBaseOutputPin. DeliverEndOfStream (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DeliverEndOfStream
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 334101c9b61631a35c5da91bd398cb7742d39235
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752715"
---
# <a name="cbaseoutputpindeliverendofstream-method"></a><span data-ttu-id="5f886-103">Método CBaseOutputPin. DeliverEndOfStream</span><span class="sxs-lookup"><span data-stu-id="5f886-103">CBaseOutputPin.DeliverEndOfStream method</span></span>

<span data-ttu-id="5f886-104">O `DeliverEndOfStream` método fornece uma notificação de fim de fluxo para o PIN de entrada conectado.</span><span class="sxs-lookup"><span data-stu-id="5f886-104">The `DeliverEndOfStream` method delivers an end-of-stream notification to the connected input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="5f886-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5f886-105">Syntax</span></span>


```C++
virtual HRESULT DeliverEndOfStream();
```



## <a name="parameters"></a><span data-ttu-id="5f886-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5f886-106">Parameters</span></span>

<span data-ttu-id="5f886-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="5f886-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="5f886-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="5f886-108">Return value</span></span>

<span data-ttu-id="5f886-109">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5f886-109">Returns an **HRESULT** value.</span></span> <span data-ttu-id="5f886-110">Os valores possíveis incluem os listados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="5f886-110">Possible values include those listed in the following table.</span></span>



| <span data-ttu-id="5f886-111">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="5f886-111">Return code</span></span>                                                                                           | <span data-ttu-id="5f886-112">Descrição</span><span class="sxs-lookup"><span data-stu-id="5f886-112">Description</span></span>                      |
|-------------------------------------------------------------------------------------------------------|----------------------------------|
| <dl> <span data-ttu-id="5f886-113"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="5f886-113"><dt>**S\_OK**</dt></span></span> </dl>                  | <span data-ttu-id="5f886-114">Êxito.</span><span class="sxs-lookup"><span data-stu-id="5f886-114">Success.</span></span><br/>              |
| <dl> <span data-ttu-id="5f886-115"><dt>**VFW \_ E \_ não \_ conectado**</dt></span><span class="sxs-lookup"><span data-stu-id="5f886-115"><dt>**VFW\_E\_NOT\_CONNECTED**</dt></span></span> </dl> | <span data-ttu-id="5f886-116">O PIN não está conectado.</span><span class="sxs-lookup"><span data-stu-id="5f886-116">Pin is not connected.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="5f886-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="5f886-117">Remarks</span></span>

<span data-ttu-id="5f886-118">Esse método chama o método [**IPin:: EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) no pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="5f886-118">This method calls the [**IPin::EndOfStream**](/windows/desktop/api/Strmif/nf-strmif-ipin-endofstream) method on the input pin.</span></span>

## <a name="requirements"></a><span data-ttu-id="5f886-119">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5f886-119">Requirements</span></span>



| <span data-ttu-id="5f886-120">Requisito</span><span class="sxs-lookup"><span data-stu-id="5f886-120">Requirement</span></span> | <span data-ttu-id="5f886-121">Valor</span><span class="sxs-lookup"><span data-stu-id="5f886-121">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5f886-122">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5f886-122">Header</span></span><br/>  | <dl> <span data-ttu-id="5f886-123"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5f886-123"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5f886-124">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5f886-124">Library</span></span><br/> | <dl> <span data-ttu-id="5f886-125"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5f886-125"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5f886-126">Confira também</span><span class="sxs-lookup"><span data-stu-id="5f886-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5f886-127">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="5f886-127">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




