---
description: O método DecideBufferSize define os requisitos de buffer do pino de saída.
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
ms.openlocfilehash: 71a506a9c9cd16a014418b24ad3fbd1186d6f48f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752689"
---
# <a name="ctransformfilterdecidebuffersize-method"></a><span data-ttu-id="33bdc-103">Método CTransformFilter. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="33bdc-103">CTransformFilter.DecideBufferSize method</span></span>

<span data-ttu-id="33bdc-104">O `DecideBufferSize` método define os requisitos de buffer do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="33bdc-104">The `DecideBufferSize` method sets the output pin's buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="33bdc-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="33bdc-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="33bdc-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="33bdc-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="33bdc-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="33bdc-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="33bdc-108">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) no alocador do pino de saída.</span><span class="sxs-lookup"><span data-stu-id="33bdc-108">Pointer to the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface on the output pin's allocator.</span></span>

</dd> <dt>

<span data-ttu-id="33bdc-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="33bdc-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="33bdc-110">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer do PIN de entrada downstream.</span><span class="sxs-lookup"><span data-stu-id="33bdc-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains buffer requirements from the downstream input pin.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="33bdc-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="33bdc-111">Return value</span></span>

<span data-ttu-id="33bdc-112">Retorna S \_ OK ou outro valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="33bdc-112">Returns S\_OK or another **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="33bdc-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="33bdc-113">Remarks</span></span>

<span data-ttu-id="33bdc-114">O método [**CTransformOutputPin::D ecidebuffersize**](ctransformoutputpin-decidebuffersize.md) do pino de saída chama esse método.</span><span class="sxs-lookup"><span data-stu-id="33bdc-114">The output pin's [**CTransformOutputPin::DecideBufferSize**](ctransformoutputpin-decidebuffersize.md) method calls this method.</span></span> <span data-ttu-id="33bdc-115">A classe derivada deve implementar esse método.</span><span class="sxs-lookup"><span data-stu-id="33bdc-115">The derived class must implement this method.</span></span> <span data-ttu-id="33bdc-116">Para obter mais informações, consulte [**CBaseOutputPin::D ecidebuffersize**](cbaseoutputpin-decidebuffersize.md).</span><span class="sxs-lookup"><span data-stu-id="33bdc-116">For more information, see [**CBaseOutputPin::DecideBufferSize**](cbaseoutputpin-decidebuffersize.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="33bdc-117">Requisitos</span><span class="sxs-lookup"><span data-stu-id="33bdc-117">Requirements</span></span>



| <span data-ttu-id="33bdc-118">Requisito</span><span class="sxs-lookup"><span data-stu-id="33bdc-118">Requirement</span></span> | <span data-ttu-id="33bdc-119">Valor</span><span class="sxs-lookup"><span data-stu-id="33bdc-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="33bdc-120">parâmetro</span><span class="sxs-lookup"><span data-stu-id="33bdc-120">Header</span></span><br/>  | <dl> <span data-ttu-id="33bdc-121"><dt>Transfrm. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="33bdc-121"><dt>Transfrm.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="33bdc-122">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="33bdc-122">Library</span></span><br/> | <dl> <span data-ttu-id="33bdc-123"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="33bdc-123"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="33bdc-124">Confira também</span><span class="sxs-lookup"><span data-stu-id="33bdc-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="33bdc-125">**Classe CTransformFilter**</span><span class="sxs-lookup"><span data-stu-id="33bdc-125">**CTransformFilter Class**</span></span>](ctransformfilter.md)
</dt> </dl>

 

 




