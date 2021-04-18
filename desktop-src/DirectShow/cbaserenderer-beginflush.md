---
description: O método BeginFlush inicia uma operação de liberação.
ms.assetid: dc652394-c24e-4cea-ac28-30a1e6de205f
title: Método CBaseRenderer. BeginFlush (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseRenderer.BeginFlush
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: e218e3b2d9c0cef8ce0fe052ad1b3c4b6f786858
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105771863"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="3e9a2-103">Método CBaseRenderer. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="3e9a2-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="3e9a2-104">O `BeginFlush` método inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="3e9a2-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="3e9a2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="3e9a2-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="3e9a2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="3e9a2-106">Parameters</span></span>

<span data-ttu-id="3e9a2-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="3e9a2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3e9a2-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="3e9a2-108">Return value</span></span>

<span data-ttu-id="3e9a2-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="3e9a2-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="3e9a2-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="3e9a2-110">Remarks</span></span>

<span data-ttu-id="3e9a2-111">O pino de entrada do filtro chama esse método quando recebe uma chamada para o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="3e9a2-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="3e9a2-112">O filtro libera o thread de streaming e libera qualquer amostra que estava segurando para renderização.</span><span class="sxs-lookup"><span data-stu-id="3e9a2-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="3e9a2-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3e9a2-113">Requirements</span></span>



| <span data-ttu-id="3e9a2-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="3e9a2-114">Requirement</span></span> | <span data-ttu-id="3e9a2-115">Valor</span><span class="sxs-lookup"><span data-stu-id="3e9a2-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3e9a2-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3e9a2-116">Header</span></span><br/>  | <dl> <span data-ttu-id="3e9a2-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3e9a2-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="3e9a2-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3e9a2-118">Library</span></span><br/> | <dl> <span data-ttu-id="3e9a2-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3e9a2-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3e9a2-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="3e9a2-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3e9a2-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="3e9a2-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




