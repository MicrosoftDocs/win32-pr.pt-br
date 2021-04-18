---
description: O método de alocador recupera um ponteiro para o alocador de memória.
ms.assetid: ac262502-eadc-482c-bc58-1e942889f0a7
title: Método CRendererInputPin. alocador (Renbase. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererInputPin.Allocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: c1dc28ddae8d493f1b30234241bfc835e28e5521
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769210"
---
# <a name="crendererinputpinallocator-method"></a><span data-ttu-id="6901f-103">Método CRendererInputPin. alocador</span><span class="sxs-lookup"><span data-stu-id="6901f-103">CRendererInputPin.Allocator method</span></span>

<span data-ttu-id="6901f-104">O `Allocator` método recupera um ponteiro para o alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="6901f-104">The `Allocator` method retrieves a pointer to the memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="6901f-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6901f-105">Syntax</span></span>


```C++
IMemAllocator* Allocator() const;
```



## <a name="parameters"></a><span data-ttu-id="6901f-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6901f-106">Parameters</span></span>

<span data-ttu-id="6901f-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="6901f-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="6901f-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="6901f-108">Return value</span></span>

<span data-ttu-id="6901f-109">Retorna um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador ou **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6901f-109">Returns a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface, or **NULL**.</span></span>

## <a name="remarks"></a><span data-ttu-id="6901f-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="6901f-110">Remarks</span></span>

<span data-ttu-id="6901f-111">Esse método retorna a variável de membro [**CBaseInputPin:: m \_ pAllocator**](cbaseinputpin-m-pallocator.md) .</span><span class="sxs-lookup"><span data-stu-id="6901f-111">This method returns the [**CBaseInputPin::m\_pAllocator**](cbaseinputpin-m-pallocator.md) member variable.</span></span> <span data-ttu-id="6901f-112">O método não incrementa a contagem de referência na interface.</span><span class="sxs-lookup"><span data-stu-id="6901f-112">The method does not increment the reference count on the interface.</span></span> <span data-ttu-id="6901f-113">Esse método é estritamente um método acessador.</span><span class="sxs-lookup"><span data-stu-id="6901f-113">This method is strictly an accessor method.</span></span>

## <a name="requirements"></a><span data-ttu-id="6901f-114">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6901f-114">Requirements</span></span>



| <span data-ttu-id="6901f-115">Requisito</span><span class="sxs-lookup"><span data-stu-id="6901f-115">Requirement</span></span> | <span data-ttu-id="6901f-116">Valor</span><span class="sxs-lookup"><span data-stu-id="6901f-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6901f-117">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6901f-117">Header</span></span><br/>  | <dl> <span data-ttu-id="6901f-118"><dt>Renbase. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6901f-118"><dt>Renbase.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="6901f-119">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6901f-119">Library</span></span><br/> | <dl> <span data-ttu-id="6901f-120"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6901f-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6901f-121">Confira também</span><span class="sxs-lookup"><span data-stu-id="6901f-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6901f-122">**Classe CRendererInputPin**</span><span class="sxs-lookup"><span data-stu-id="6901f-122">**CRendererInputPin Class**</span></span>](crendererinputpin.md)
</dt> </dl>

 

 




