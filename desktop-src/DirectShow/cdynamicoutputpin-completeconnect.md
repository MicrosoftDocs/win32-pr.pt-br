---
description: O método CompleteConnect conclui uma conexão com um PIN de entrada.
ms.assetid: c23195e7-8d66-4217-bd59-8889459ce4f1
title: Método CDynamicOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CDynamicOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 31afa592701b881d39ab4948514aacfe50b345b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752496"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="ba14b-103">Método CDynamicOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="ba14b-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="ba14b-104">O `CompleteConnect` método conclui uma conexão com um PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="ba14b-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="ba14b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ba14b-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="ba14b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ba14b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ba14b-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="ba14b-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="ba14b-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="ba14b-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ba14b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ba14b-109">Return value</span></span>

<span data-ttu-id="ba14b-110">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="ba14b-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="ba14b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="ba14b-111">Remarks</span></span>

<span data-ttu-id="ba14b-112">Esse método substitui o método [**CBaseOutputPin:: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="ba14b-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="ba14b-113">Para dar suporte a reconexões dinâmicas, esse método confirma o alocador se o filtro estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="ba14b-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="ba14b-114">Na classe base, as conexões podem ocorrer somente quando o filtro é interrompido, portanto, o alocador sempre é confirmado no método [**CBaseOutputPin:: active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="ba14b-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ba14b-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ba14b-115">Requirements</span></span>



| <span data-ttu-id="ba14b-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="ba14b-116">Requirement</span></span> | <span data-ttu-id="ba14b-117">Valor</span><span class="sxs-lookup"><span data-stu-id="ba14b-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ba14b-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ba14b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="ba14b-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ba14b-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ba14b-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ba14b-120">Library</span></span><br/> | <dl> <span data-ttu-id="ba14b-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ba14b-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ba14b-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="ba14b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ba14b-123">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="ba14b-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




