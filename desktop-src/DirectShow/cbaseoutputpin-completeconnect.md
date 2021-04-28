---
description: Método CBaseOutputPin. CompleteConnect – o método CompleteConnect conclui uma conexão com um PIN de entrada.
ms.assetid: 44c28c71-2c69-40ca-9bc4-c10394475a0f
title: Método CBaseOutputPin. CompleteConnect (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.CompleteConnect
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: cd4bc52db99b88c4d6f16c549fbb558bb6423730
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099534"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="66eb2-103">Método CBaseOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="66eb2-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="66eb2-104">O `CompleteConnect` método conclui uma conexão com um PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="66eb2-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="66eb2-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="66eb2-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="66eb2-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="66eb2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="66eb2-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="66eb2-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="66eb2-108">Ponteiro para o pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="66eb2-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="66eb2-109">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="66eb2-109">Return value</span></span>

<span data-ttu-id="66eb2-110">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="66eb2-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="66eb2-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="66eb2-111">Remarks</span></span>

<span data-ttu-id="66eb2-112">Esse método substitui o método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="66eb2-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="66eb2-113">Ele chama o método [**DecideAllocator**](cbaseoutputpin-decideallocator.md) , que seleciona o alocador de memória a ser usado para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="66eb2-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="66eb2-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="66eb2-114">Requirements</span></span>



| <span data-ttu-id="66eb2-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="66eb2-115">Requirement</span></span> | <span data-ttu-id="66eb2-116">Valor</span><span class="sxs-lookup"><span data-stu-id="66eb2-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66eb2-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="66eb2-117">Header</span></span><br/>  | <dl> <span data-ttu-id="66eb2-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="66eb2-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="66eb2-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="66eb2-119">Library</span></span><br/> | <dl> <span data-ttu-id="66eb2-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="66eb2-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="66eb2-121">Consulte também</span><span class="sxs-lookup"><span data-stu-id="66eb2-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="66eb2-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="66eb2-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




