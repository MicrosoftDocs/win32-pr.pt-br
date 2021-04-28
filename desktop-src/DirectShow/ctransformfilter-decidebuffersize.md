---
description: Método CTransformFilter. DecideBufferSize – o método DecideBufferSize define os requisitos de buffer do pino de saída.
ms.assetid: 33e41668-b4f6-4142-b22e-2ddfb96332df
title: Método CTransformFilter. DecideBufferSize (Transfrm. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CTransformFilter.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f3276170f1256bba41aa075b0e5f06fb7becbcd2
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108095144"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="0d5e7-103">Método CTransformFilter. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="0d5e7-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="0d5e7-104">O `DecideBufferSize` método define os requisitos de buffer do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="0d5e7-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="0d5e7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0d5e7-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="0d5e7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0d5e7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0d5e7-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="0d5e7-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="0d5e7-108">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) no alocador do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="0d5e7-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="0d5e7-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="0d5e7-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="0d5e7-110">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer do PIN de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="0d5e7-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0d5e7-111">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="0d5e7-111">Return value</span></span>

<span data-ttu-id="0d5e7-112">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0d5e7-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d5e7-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="0d5e7-113">Remarks</span></span>

<span data-ttu-id="0d5e7-114">O método [**CTransformOutputPin::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) do pino de saída chama esse método.</span><span class="sxs-lookup"><span data-stu-id="0d5e7-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="0d5e7-115">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="0d5e7-115">The derived class must implement this method.</span></span> <span data-ttu-id="0d5e7-116">Para obter mais informações, consulte [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="0d5e7-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0d5e7-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0d5e7-117">Requirements</span></span>



| <span data-ttu-id="0d5e7-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="0d5e7-118">Requirement</span></span> | <span data-ttu-id="0d5e7-119">Valor</span><span class="sxs-lookup"><span data-stu-id="0d5e7-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0d5e7-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0d5e7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="0d5e7-121"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5e7-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="0d5e7-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0d5e7-122">Library</span></span><br/> | <dl> <span data-ttu-id="0d5e7-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0d5e7-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0d5e7-124">Consulte também</span><span class="sxs-lookup"><span data-stu-id="0d5e7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d5e7-125">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="0d5e7-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




