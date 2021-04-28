---
description: Método CBaseRenderer. BeginFlush-o método BeginFlush inicia uma operação de liberação.
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
ms.openlocfilehash: 76dfd77a5170a83813871143781868cae55c45ba
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095934"
---
# <a name="cbaserendererbeginflush-method"></a><span data-ttu-id="e091f-103">Método CBaseRenderer. BeginFlush</span><span class="sxs-lookup"><span data-stu-id="e091f-103">CBaseRenderer.BeginFlush method</span></span>

<span data-ttu-id="e091f-104">O `BeginFlush` método inicia uma operação de liberação.</span><span class="sxs-lookup"><span data-stu-id="e091f-104">The `BeginFlush` method begins a flush operation.</span></span>

## <a name="syntax"></a><span data-ttu-id="e091f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e091f-105">Syntax</span></span>


```C++
virtual HRESULT BeginFlush();
```



## <a name="parameters"></a><span data-ttu-id="e091f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e091f-106">Parameters</span></span>

<span data-ttu-id="e091f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="e091f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="e091f-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="e091f-108">Return value</span></span>

<span data-ttu-id="e091f-109">Retorna S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="e091f-109">Returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="e091f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="e091f-110">Remarks</span></span>

<span data-ttu-id="e091f-111">O pino de entrada do filtro chama esse método quando recebe uma chamada para o método [**IPin:: BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) .</span><span class="sxs-lookup"><span data-stu-id="e091f-111">The filter's input pin calls this method when it receives a call to the [**IPin::BeginFlush**](/windows/desktop/api/Strmif/nf-strmif-ipin-beginflush) method.</span></span> <span data-ttu-id="e091f-112">O filtro libera o thread de streaming e libera qualquer amostra que estava segurando para renderização.</span><span class="sxs-lookup"><span data-stu-id="e091f-112">The filter releases the streaming thread, and releases any sample that it was holding for rendering.</span></span>

## <a name="requirements"></a><span data-ttu-id="e091f-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e091f-113">Requirements</span></span>



| <span data-ttu-id="e091f-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="e091f-114">Requirement</span></span> | <span data-ttu-id="e091f-115">Valor</span><span class="sxs-lookup"><span data-stu-id="e091f-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e091f-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e091f-116">Header</span></span><br/>  | <dl> <span data-ttu-id="e091f-117"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e091f-117"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="e091f-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e091f-118">Library</span></span><br/> | <dl> <span data-ttu-id="e091f-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e091f-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e091f-120">Consulte também</span><span class="sxs-lookup"><span data-stu-id="e091f-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e091f-121">**Classe CBaseRenderer**</span><span class="sxs-lookup"><span data-stu-id="e091f-121">**CBaseRenderer Class**</span></span>](cbaserenderer.md)
</dt> </dl>

 

 




