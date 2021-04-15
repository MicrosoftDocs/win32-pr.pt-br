---
description: O método DecideBufferSize define os requisitos de buffer.
ms.assetid: 1f7a3424-18ba-4a10-b09f-947ee8585ffa
title: Método CBaseOutputPin. DecideBufferSize (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.DecideBufferSize
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dcb3328b56a7e203575a3abbaab64cda6a9b87f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747407"
---
# <a name="cbaseoutputpindecidebuffersize-method"></a><span data-ttu-id="eb07d-103">Método CBaseOutputPin. DecideBufferSize</span><span class="sxs-lookup"><span data-stu-id="eb07d-103">CBaseOutputPin.DecideBufferSize method</span></span>

<span data-ttu-id="eb07d-104">O `DecideBufferSize` método define os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="eb07d-104">The `DecideBufferSize` method sets the buffer requirements.</span></span>

## <a name="syntax"></a><span data-ttu-id="eb07d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="eb07d-105">Syntax</span></span>


```C++
virtual HRESULT DecideBufferSize(
   IMemAllocator        *pAlloc,
   ALLOCATOR_PROPERTIES *ppropInputRequest
) = 0;
```



## <a name="parameters"></a><span data-ttu-id="eb07d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="eb07d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eb07d-107">*pAlloc*</span><span class="sxs-lookup"><span data-stu-id="eb07d-107">*pAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="eb07d-108">Ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="eb07d-108">Pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> <dt>

<span data-ttu-id="eb07d-109">*ppropInputRequest*</span><span class="sxs-lookup"><span data-stu-id="eb07d-109">*ppropInputRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="eb07d-110">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer do pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="eb07d-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the input pin's buffer requirements.</span></span> <span data-ttu-id="eb07d-111">Se o pino de entrada não tiver nenhum requisito, o chamador deverá zerar os membros dessa estrutura antes de chamar o método.</span><span class="sxs-lookup"><span data-stu-id="eb07d-111">If the input pin does not have any requirements, the caller should zero out the members of this structure before calling the method.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eb07d-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="eb07d-112">Return value</span></span>

<span data-ttu-id="eb07d-113">Retorna S \_ OK se bem-sucedido ou um valor **HRESULT** que indica a causa do erro.</span><span class="sxs-lookup"><span data-stu-id="eb07d-113">Returns S\_OK if successful, or an **HRESULT** value indicating the cause of the error.</span></span>

## <a name="remarks"></a><span data-ttu-id="eb07d-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="eb07d-114">Remarks</span></span>

<span data-ttu-id="eb07d-115">Substitua esse método em sua classe derivada.</span><span class="sxs-lookup"><span data-stu-id="eb07d-115">Override this method in your derived class.</span></span> <span data-ttu-id="eb07d-116">Chame o método [**IMemAllocator:: SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) para especificar os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="eb07d-116">Call the [**IMemAllocator::SetProperties**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-setproperties) method to specify your buffer requirements.</span></span> <span data-ttu-id="eb07d-117">Normalmente, a classe derivada honrará os requisitos de buffer do pino de entrada, mas não é necessário.</span><span class="sxs-lookup"><span data-stu-id="eb07d-117">Typically, the derived class will honor the input pin's buffer requirements, but it is not required to.</span></span>

## <a name="requirements"></a><span data-ttu-id="eb07d-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="eb07d-118">Requirements</span></span>



| <span data-ttu-id="eb07d-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="eb07d-119">Requirement</span></span> | <span data-ttu-id="eb07d-120">Valor</span><span class="sxs-lookup"><span data-stu-id="eb07d-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="eb07d-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="eb07d-121">Header</span></span><br/>  | <dl> <span data-ttu-id="eb07d-122"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="eb07d-122"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="eb07d-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="eb07d-123">Library</span></span><br/> | <dl> <span data-ttu-id="eb07d-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="eb07d-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="eb07d-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="eb07d-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eb07d-126">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="eb07d-126">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




