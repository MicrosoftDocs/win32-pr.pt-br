---
description: O método InitAllocator cria um alocador de memória.
ms.assetid: a1fa0ffb-ed43-446d-811e-6c3594743592
title: CBaseOutputPin.Inimétodo tAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseOutputPin.InitAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7e5385671ba4c7fdf1b719f83aafba7d84421bce
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105769245"
---
# <a name="cbaseoutputpininitallocator-method"></a><span data-ttu-id="b5ea9-103">CBaseOutputPin.Inimétodo tAllocator</span><span class="sxs-lookup"><span data-stu-id="b5ea9-103">CBaseOutputPin.InitAllocator method</span></span>

<span data-ttu-id="b5ea9-104">O `InitAllocator` método cria um alocador de memória.</span><span class="sxs-lookup"><span data-stu-id="b5ea9-104">The `InitAllocator` method creates a memory allocator.</span></span>

## <a name="syntax"></a><span data-ttu-id="b5ea9-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b5ea9-105">Syntax</span></span>


```C++
virtual HRESULT InitAllocator(
   IMemAllocator **ppAlloc
);
```



## <a name="parameters"></a><span data-ttu-id="b5ea9-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b5ea9-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b5ea9-107">*ppAlloc*</span><span class="sxs-lookup"><span data-stu-id="b5ea9-107">*ppAlloc*</span></span> 
</dt> <dd>

<span data-ttu-id="b5ea9-108">Endereço de uma variável que recebe um ponteiro para a interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) do alocador.</span><span class="sxs-lookup"><span data-stu-id="b5ea9-108">Address of a variable that receives a pointer to the allocator's [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b5ea9-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b5ea9-109">Return value</span></span>

<span data-ttu-id="b5ea9-110">Retorna S \_ OK se for bem-sucedido ou um código de erro da função **CoCreateInstance** .</span><span class="sxs-lookup"><span data-stu-id="b5ea9-110">Returns S\_OK if successful, or an error code from the **CoCreateInstance** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="b5ea9-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="b5ea9-111">Remarks</span></span>

<span data-ttu-id="b5ea9-112">Se o pino de entrada não fornecer um alocador de memória, o método [**CBaseOutputPin::D ecideallocator**](cbaseoutputpin-decideallocator.md) chamará esse método para criar um alocador.</span><span class="sxs-lookup"><span data-stu-id="b5ea9-112">If the input pin does not provide a memory allocator, the [**CBaseOutputPin::DecideAllocator**](cbaseoutputpin-decideallocator.md) method calls this method to create an allocator.</span></span>

## <a name="requirements"></a><span data-ttu-id="b5ea9-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b5ea9-113">Requirements</span></span>



| <span data-ttu-id="b5ea9-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b5ea9-114">Requirement</span></span> | <span data-ttu-id="b5ea9-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b5ea9-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b5ea9-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b5ea9-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b5ea9-117"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b5ea9-117"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="b5ea9-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b5ea9-118">Library</span></span><br/> | <dl> <span data-ttu-id="b5ea9-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b5ea9-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b5ea9-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b5ea9-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b5ea9-121">**Classe CBaseOutputPin**</span><span class="sxs-lookup"><span data-stu-id="b5ea9-121">**CBaseOutputPin Class**</span></span>](cbaseoutputpin.md)
</dt> </dl>

 

 




