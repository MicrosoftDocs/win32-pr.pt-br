---
description: O método GetAllocatorRequirements recupera as propriedades de alocador solicitadas pelo PIN de entrada.
ms.assetid: 81564924-6d5b-4b2a-b549-e3f358f18371
title: Método CBaseInputPin. GetAllocatorRequirements (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseInputPin.GetAllocatorRequirements
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f0239d226ea57ed5953fa65b925eeffaa0b13df1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747412"
---
# <a name="cbaseinputpingetallocatorrequirements-method"></a><span data-ttu-id="bf72e-103">Método CBaseInputPin. GetAllocatorRequirements</span><span class="sxs-lookup"><span data-stu-id="bf72e-103">CBaseInputPin.GetAllocatorRequirements method</span></span>

<span data-ttu-id="bf72e-104">O `GetAllocatorRequirements` método recupera as propriedades de alocador solicitadas pelo pino de entrada.</span><span class="sxs-lookup"><span data-stu-id="bf72e-104">The `GetAllocatorRequirements` method retrieves the allocator properties requested by the input pin.</span></span>

## <a name="syntax"></a><span data-ttu-id="bf72e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bf72e-105">Syntax</span></span>


```C++
HRESULT GetAllocatorRequirements(
   ALLOCATOR_PROPERTIES *pProps
);
```



## <a name="parameters"></a><span data-ttu-id="bf72e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bf72e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bf72e-107">*pProps*</span><span class="sxs-lookup"><span data-stu-id="bf72e-107">*pProps*</span></span> 
</dt> <dd>

<span data-ttu-id="bf72e-108">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) , que é preenchida com os requisitos.</span><span class="sxs-lookup"><span data-stu-id="bf72e-108">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure, which is filled in with the requirements.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bf72e-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bf72e-109">Return value</span></span>

<span data-ttu-id="bf72e-110">Retorna E \_ NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="bf72e-110">Returns E\_NOTIMPL.</span></span>

## <a name="remarks"></a><span data-ttu-id="bf72e-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bf72e-111">Remarks</span></span>

<span data-ttu-id="bf72e-112">Quando um pino de saída Inicializa um alocador de memória, ele pode chamar esse método para determinar se o PIN de entrada tem requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="bf72e-112">When an output pin initializes a memory allocator, it can call this method to determine whether the input pin has any buffer requirements.</span></span> <span data-ttu-id="bf72e-113">Para obter mais informações, consulte [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md).</span><span class="sxs-lookup"><span data-stu-id="bf72e-113">For more information, see [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md).</span></span>

<span data-ttu-id="bf72e-114">A implementação desse método é opcional.</span><span class="sxs-lookup"><span data-stu-id="bf72e-114">Implementing this method is optional.</span></span> <span data-ttu-id="bf72e-115">Se o filtro tiver requisitos específicos de alinhamento ou prefixo, substitua esse método.</span><span class="sxs-lookup"><span data-stu-id="bf72e-115">If the filter has specific alignment or prefix requirements, override this method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bf72e-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bf72e-116">Requirements</span></span>



| <span data-ttu-id="bf72e-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="bf72e-117">Requirement</span></span> | <span data-ttu-id="bf72e-118">Valor</span><span class="sxs-lookup"><span data-stu-id="bf72e-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bf72e-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bf72e-119">Header</span></span><br/>  | <dl> <span data-ttu-id="bf72e-120"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bf72e-120"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bf72e-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bf72e-121">Library</span></span><br/> | <dl> <span data-ttu-id="bf72e-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bf72e-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bf72e-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="bf72e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bf72e-124">**Classe CBaseInputPin**</span><span class="sxs-lookup"><span data-stu-id="bf72e-124">**CBaseInputPin Class**</span></span>](cbaseinputpin.md)
</dt> </dl>

 

 




