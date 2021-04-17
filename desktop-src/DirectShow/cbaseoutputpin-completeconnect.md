---
description: O método CompleteConnect conclui uma conexão com um PIN de entrada.
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
ms.openlocfilehash: 4614e8531a21d88a1c2f4cfd75fcbe05a9210f13
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787424"
---
# <a name="cbaseoutputpincompleteconnect-method"></a><span data-ttu-id="0845b-103">Método CBaseOutputPin. CompleteConnect</span><span class="sxs-lookup"><span data-stu-id="0845b-103">CBaseOutputPin.CompleteConnect method</span></span>

<span data-ttu-id="0845b-104">O `CompleteConnect` método conclui uma conexão com um PIN de entrada.</span><span class="sxs-lookup"><span data-stu-id="0845b-104">The `CompleteConnect` method completes a connection to an input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="0845b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0845b-105">Syntax</span></span>


```C++
virtual HRESULT CompleteConnect(
   IPin *pReceivePin
);
```



## <a name="parameters"></a><span data-ttu-id="0845b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0845b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0845b-107">*pReceivePin*</span><span class="sxs-lookup"><span data-stu-id="0845b-107">*pReceivePin*</span></span> 
</dt> <dd>

<span data-ttu-id="0845b-108">Ponteiro para o pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="0845b-108">Pointer to the input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0845b-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="0845b-109">Return value</span></span>

<span data-ttu-id="0845b-110">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="0845b-110">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="0845b-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="0845b-111">Remarks</span></span>

<span data-ttu-id="0845b-112">Esse método substitui o método [**CBasePin:: CompleteConnect**](cbasepin-completeconnect.md) .</span><span class="sxs-lookup"><span data-stu-id="0845b-112">This method overrides the [**CBasePin::CompleteConnect**](cbasepin-completeconnect.md) method.</span></span> <span data-ttu-id="0845b-113">Ele chama o método [**DecideAllocator**](cbaseoutputpin-decideallocator.md) , que seleciona o alocador de memória a ser usado para essa conexão.</span><span class="sxs-lookup"><span data-stu-id="0845b-113">It calls the [**DecideAllocator**](cbaseoutputpin-decideallocator.md) method, which selects the memory allocator to use for this connection.</span></span>

## <a name="requirements"></a><span data-ttu-id="0845b-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0845b-114">Requirements</span></span>



| <span data-ttu-id="0845b-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="0845b-115">Requirement</span></span> | <span data-ttu-id="0845b-116">Valor</span><span class="sxs-lookup"><span data-stu-id="0845b-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0845b-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0845b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="0845b-118"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0845b-118"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0845b-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0845b-119">Library</span></span><br/> | <dl> <span data-ttu-id="0845b-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0845b-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0845b-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="0845b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0845b-122">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="0845b-122">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




