---
description: 'O método Commit aloca a memória para os buffers. Esse método implementa o método IMemAllocator:: Commit.'
ms.assetid: e8c36276-0229-428f-b030-978651ab7534
title: Método CBaseAllocator. Commit (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Commit
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b49fae72e5588105b1235c1f0c461d5cc45cfa2b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105778651"
---
# <a name="cbaseallocatorcommit-method"></a><span data-ttu-id="bebf4-104">Método CBaseAllocator. Commit</span><span class="sxs-lookup"><span data-stu-id="bebf4-104">CBaseAllocator.Commit method</span></span>

<span data-ttu-id="bebf4-105">O `Commit` método aloca a memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="bebf4-105">The `Commit` method allocates the memory for the buffers.</span></span> <span data-ttu-id="bebf4-106">Esse método implementa o método [**IMemAllocator:: Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) .</span><span class="sxs-lookup"><span data-stu-id="bebf4-106">This method implements the [**IMemAllocator::Commit**](/windows/desktop/api/Strmif/nf-strmif-imemallocator-commit) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="bebf4-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bebf4-107">Syntax</span></span>


```C++
HRESULT Commit();
```



## <a name="parameters"></a><span data-ttu-id="bebf4-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bebf4-108">Parameters</span></span>

<span data-ttu-id="bebf4-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="bebf4-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bebf4-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bebf4-110">Return value</span></span>

<span data-ttu-id="bebf4-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="bebf4-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="bebf4-112">Os valores possíveis incluem os da lista a seguir.</span><span class="sxs-lookup"><span data-stu-id="bebf4-112">Possible values include those in the following list.</span></span>



| <span data-ttu-id="bebf4-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="bebf4-113">Return code</span></span>                                                                                       | <span data-ttu-id="bebf4-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="bebf4-114">Description</span></span>                                        |
|---------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="bebf4-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="bebf4-115"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="bebf4-116">Êxito.</span><span class="sxs-lookup"><span data-stu-id="bebf4-116">Success.</span></span><br/>                                |
| <dl> <span data-ttu-id="bebf4-117"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="bebf4-117"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="bebf4-118">Os requisitos de buffer não foram especificados.</span><span class="sxs-lookup"><span data-stu-id="bebf4-118">Buffer requirements were not specified.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="bebf4-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="bebf4-119">Remarks</span></span>

<span data-ttu-id="bebf4-120">Antes de chamar esse método, chame o método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) para especificar os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="bebf4-120">Before calling this method, call the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method to specify the buffer requirements.</span></span>

<span data-ttu-id="bebf4-121">Esse método chama o método virtual [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) para alocar a memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="bebf4-121">This method calls the virtual method [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) to allocate the memory for the buffers.</span></span> <span data-ttu-id="bebf4-122">As classes derivadas podem substituir a **alocação**.</span><span class="sxs-lookup"><span data-stu-id="bebf4-122">Derived classes can override **Alloc**.</span></span> <span data-ttu-id="bebf4-123">Se uma operação de desconfirmação estiver pendente, ela será cancelada.</span><span class="sxs-lookup"><span data-stu-id="bebf4-123">If a decommit operation is pending, it is canceled.</span></span>

<span data-ttu-id="bebf4-124">Você deve chamar esse método antes de chamar o método [**CBaseAllocator:: GetBuffer**](cbaseallocator-getbuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="bebf4-124">You must call this method before calling the [**CBaseAllocator::GetBuffer**](cbaseallocator-getbuffer.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="bebf4-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bebf4-125">Requirements</span></span>



| <span data-ttu-id="bebf4-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="bebf4-126">Requirement</span></span> | <span data-ttu-id="bebf4-127">Valor</span><span class="sxs-lookup"><span data-stu-id="bebf4-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bebf4-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bebf4-128">Header</span></span><br/>  | <dl> <span data-ttu-id="bebf4-129"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bebf4-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="bebf4-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bebf4-130">Library</span></span><br/> | <dl> <span data-ttu-id="bebf4-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bebf4-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bebf4-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="bebf4-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bebf4-133">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="bebf4-133">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




