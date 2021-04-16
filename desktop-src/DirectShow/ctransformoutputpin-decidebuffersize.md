---
description: O método DecideBufferSize define os requisitos de buffer.
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
ms.openlocfilehash: dc17314887094b7f62a43f38dd406d0ac9039de3
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750649"
---
# <a name="ctransformoutputpindecidebuffersize-method"></a><span data-ttu-id="ca990-103">Método CTransformOutputPin. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="ca990-103">CTransformOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="ca990-104">O `DecideBufferSize` método define os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="ca990-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="ca990-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="ca990-105">Syntax</span></span>


```C++
HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
);
```



## <a name="parameters"></a><span data-ttu-id="ca990-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="ca990-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ca990-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="ca990-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="ca990-108">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="ca990-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="ca990-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="ca990-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="ca990-110">Ponteiro de uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="ca990-110">Pointer an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ca990-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="ca990-111">Return value</span></span>

<span data-ttu-id="ca990-112">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="ca990-112">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="ca990-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="ca990-113">Remarks</span></span>

<span data-ttu-id="ca990-114">Esse método substitui o método [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md) .</span><span class="sxs-lookup"><span data-stu-id="ca990-114">This method overrides the [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md) method.</span></span> <span data-ttu-id="ca990-115">Ele chama o método CTransformFilter virtual puro do filtro [**::D ecidebuffersize**](ctransformfilter-decidebuffersize.md) , que a classe derivada do filtro deve implementar.</span><span class="sxs-lookup"><span data-stu-id="ca990-115">It calls the filter's pure virtual [**CTransformFilter::DecideBufferSize**](ctransformfilter-decidebuffersize.md) method, which the filter's derived class must implement.</span></span>

## <a name="requirements"></a><span data-ttu-id="ca990-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="ca990-116">Requirements</span></span>



| <span data-ttu-id="ca990-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="ca990-117">Requirement</span></span> | <span data-ttu-id="ca990-118">Valor</span><span class="sxs-lookup"><span data-stu-id="ca990-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca990-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="ca990-119">Header</span></span><br/>  | <dl> <span data-ttu-id="ca990-120"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="ca990-120"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="ca990-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="ca990-121">Library</span></span><br/> | <dl> <span data-ttu-id="ca990-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="ca990-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




