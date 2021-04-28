---
description: Método CMemAllocator. Alloc – o método Alloc aloca memória para os buffers.
ms.assetid: 81886163-2f7d-4d4f-be90-4491f76b8514
title: Método CMemAllocator. Alloc (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7d7de755aa3b8007a122e43529d16f5e39ca0cb8
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108099034"
---
# <a name="cmemallocatoralloc-method"></a><span data-ttu-id="2f73a-103">Método CMemAllocator. Alloc</span><span class="sxs-lookup"><span data-stu-id="2f73a-103">CMemAllocator.Alloc method</span></span>

<span data-ttu-id="2f73a-104">O `Alloc` método aloca memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="2f73a-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f73a-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2f73a-105">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="2f73a-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2f73a-106">Parameters</span></span>

<span data-ttu-id="2f73a-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2f73a-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2f73a-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="2f73a-108">Return value</span></span>

<span data-ttu-id="2f73a-109">Retorna um dos valores **HRESULT** mostrados na tabela a seguir.</span><span class="sxs-lookup"><span data-stu-id="2f73a-109">Returns one of the **HRESULT** values shown in the following table.</span></span>



| <span data-ttu-id="2f73a-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="2f73a-110">Return code</span></span>                                                                                       | <span data-ttu-id="2f73a-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="2f73a-111">Description</span></span>                                  |
|---------------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <span data-ttu-id="2f73a-112"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="2f73a-112"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="2f73a-113">Sucesso.</span><span class="sxs-lookup"><span data-stu-id="2f73a-113">Success.</span></span><br/>                          |
| <dl> <span data-ttu-id="2f73a-114"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="2f73a-114"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl>     | <span data-ttu-id="2f73a-115">Memória insuficiente.</span><span class="sxs-lookup"><span data-stu-id="2f73a-115">Insufficient memory.</span></span><br/>              |
| <dl> <span data-ttu-id="2f73a-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="2f73a-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="2f73a-117">Os requisitos de buffer não foram definidos.</span><span class="sxs-lookup"><span data-stu-id="2f73a-117">Buffer requirements were not set.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="2f73a-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="2f73a-118">Remarks</span></span>

<span data-ttu-id="2f73a-119">Esse método é chamado pelo método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="2f73a-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span> <span data-ttu-id="2f73a-120">Ele aloca um bloco contíguo de memória suficiente para os requisitos de buffer fornecidos no método [**CMemAllocator:: SetProperties**](cmemallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="2f73a-120">It allocates a contiguous block of memory sufficient for the buffer requirements given in the [**CMemAllocator::SetProperties**](cmemallocator-setproperties.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f73a-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2f73a-121">Requirements</span></span>



| <span data-ttu-id="2f73a-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="2f73a-122">Requirement</span></span> | <span data-ttu-id="2f73a-123">Valor</span><span class="sxs-lookup"><span data-stu-id="2f73a-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2f73a-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2f73a-124">Header</span></span><br/>  | <dl> <span data-ttu-id="2f73a-125"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2f73a-125"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="2f73a-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2f73a-126">Library</span></span><br/> | <dl> <span data-ttu-id="2f73a-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2f73a-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2f73a-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="2f73a-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f73a-129">**Classe CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="2f73a-129">**CMemAllocator Class**</span></span>](cmemallocator.md)
</dt> </dl>

 

 




