---
description: Método CDynamicOutputPin. CompleteConnect – o método CompleteConnect conclui uma conexão com um PIN de entrada.
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
ms.openlocfilehash: 5fa15c84b9d9e0b686e17110c656b74161687705
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095734"
---
# <a name="cdynamicoutputpincompleteconnect-method"></a><span data-ttu-id="0741e-103">Método CDynamicOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="0741e-103">CDynamicOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="0741e-104">O `CompleteConnect` método conclui uma conexão com um PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="0741e-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0741e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0741e-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="0741e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0741e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0741e-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="0741e-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="0741e-108">Ponteiro para a interface [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="0741e-108">Pointer to the input pin's [**IPin**](/windows/desktop/api/Strmif/nn-strmif-ipin) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0741e-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0741e-109">Return value</span></span>

<span data-ttu-id="0741e-110">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa da falha.</span><span class="sxs-lookup"><span data-stu-id="0741e-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="0741e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0741e-111">Remarks</span></span>

<span data-ttu-id="0741e-112">Esse método substitui o método [**CBaseOutputPin:: CompleteConnect**](cbaseoutputpin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0741e-112">This method overrides the [**CBaseOutputPin::CompleteConnect**](cbaseoutputpin-completeconnect.md) method.</span></span> <span data-ttu-id="0741e-113">Para dar suporte a reconexões dinâmicas, esse método confirma o alocador se o filtro estiver ativo.</span><span class="sxs-lookup"><span data-stu-id="0741e-113">To support dynamic reconnections, this method commits the allocator if the filter is active.</span></span> <span data-ttu-id="0741e-114">Na classe base, as conexões podem ocorrer somente quando o filtro é interrompido, portanto, o alocador sempre é confirmado no método [**CBaseOutputPin:: active**](cbaseoutputpin-active.md) .</span><span class="sxs-lookup"><span data-stu-id="0741e-114">In the base class, connections can occur only when the filter is stopped, so the allocator is always committed in the [**CBaseOutputPin::Active**](cbaseoutputpin-active.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="0741e-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0741e-115">Requirements</span></span>



| <span data-ttu-id="0741e-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="0741e-116">Requirement</span></span> | <span data-ttu-id="0741e-117">Valor</span><span class="sxs-lookup"><span data-stu-id="0741e-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0741e-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0741e-118">Header</span></span><br/>  | <dl> <span data-ttu-id="0741e-119"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0741e-119"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0741e-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0741e-120">Library</span></span><br/> | <dl> <span data-ttu-id="0741e-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0741e-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0741e-122">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0741e-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0741e-123">**Classe CDynamicOutputPin**</span><span class="sxs-lookup"><span data-stu-id="0741e-123">**CDynamicOutputPin Class**</span></span>](cdynamicoutputpin.md)
</dt> </dl>

 

 




