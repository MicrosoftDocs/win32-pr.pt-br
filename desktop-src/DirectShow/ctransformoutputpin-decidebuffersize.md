---
description: Método CTransformOutputPin. DecideBufferSize – o método DecideBufferSize define os requisitos de buffer.
ms.assetid: cdf9e384-623e-46a6-b123-d881fe21fb09
title: Método CTransformOutputPin. DecideBufferSize (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1bc84eaf5e95a19436de5429ce018352cdaa286e
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108084834"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="c36da-103">Método CTransformOutputPin. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="c36da-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="c36da-104">O `DecideBufferSize` método define os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="c36da-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="c36da-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="c36da-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="c36da-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="c36da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c36da-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="c36da-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="c36da-108">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="c36da-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="c36da-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="c36da-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="c36da-110">Ponteiro de uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="c36da-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c36da-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="c36da-111">Return value</span></span>

<span data-ttu-id="c36da-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="c36da-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="c36da-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="c36da-113">Remarks</span></span>

<span data-ttu-id="c36da-114">Esse método substitui o método [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="c36da-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="c36da-115">Ele chama o método CTransformFilter virtual puro do filtro [**::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) , que a classe derivada do filtro deve implementar.</span><span class="sxs-lookup"><span data-stu-id="c36da-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="c36da-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="c36da-116">Requirements</span></span>



| <span data-ttu-id="c36da-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="c36da-117">Requirement</span></span> | <span data-ttu-id="c36da-118">Valor</span><span class="sxs-lookup"><span data-stu-id="c36da-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="c36da-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="c36da-119">Header</span></span><br/>  | <dl> <span data-ttu-id="c36da-120"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="c36da-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="c36da-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="c36da-121">Library</span></span><br/> | <dl> <span data-ttu-id="c36da-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="c36da-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




