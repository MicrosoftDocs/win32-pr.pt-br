---
description: Método CBaseAllocator. Alloc – o método Alloc aloca memória para os buffers.
ms.assetid: a22c97ef-6a8d-4cad-b5a5-3e6b225f5c81
title: Método CBaseAllocator. Alloc (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b53dc461a520b4e8c890a36fca6d73c2c836499f
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108096356"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="30da3-103">Método CBaseAllocator. Alloc</span><span class="sxs-lookup"><span data-stu-id="30da3-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="30da3-104">O `Alloc` método aloca memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="30da3-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="30da3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="30da3-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="30da3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="30da3-106">Parameters</span></span>

<span data-ttu-id="30da3-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="30da3-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="30da3-108">Valor retornado</span><span class="sxs-lookup"><span data-stu-id="30da3-108">Return value</span></span>

<span data-ttu-id="30da3-109">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="30da3-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="30da3-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="30da3-110">Return code</span></span>                                                                                       | <span data-ttu-id="30da3-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="30da3-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="30da3-112"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="30da3-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="30da3-113">Os requisitos de buffer não foram alterados.</span><span class="sxs-lookup"><span data-stu-id="30da3-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="30da3-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="30da3-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="30da3-115">Os requisitos de buffer foram alterados.</span><span class="sxs-lookup"><span data-stu-id="30da3-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="30da3-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="30da3-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="30da3-117">Os requisitos de buffer não foram definidos.</span><span class="sxs-lookup"><span data-stu-id="30da3-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="30da3-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="30da3-118">Remarks</span></span>

<span data-ttu-id="30da3-119">Esse método é chamado pelo método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="30da3-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="30da3-120">Na classe base, esse método não aloca nenhuma memória.</span><span class="sxs-lookup"><span data-stu-id="30da3-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="30da3-121">Ele retornará um erro se os requisitos de buffer não tiverem sido definidos, S \_ false se os requisitos não foram alterados e s \_ OK se os requisitos foram alterados.</span><span class="sxs-lookup"><span data-stu-id="30da3-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="30da3-122">Uma classe derivada deve substituir esse método para executar a alocação de memória real.</span><span class="sxs-lookup"><span data-stu-id="30da3-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="30da3-123">Normalmente, a classe derivada executará as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="30da3-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="30da3-124">Chame a implementação da classe base para determinar se a memória realmente precisa ser alocada.</span><span class="sxs-lookup"><span data-stu-id="30da3-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="30da3-125">Aloque memória.</span><span class="sxs-lookup"><span data-stu-id="30da3-125">Allocate memory.</span></span>
3.  <span data-ttu-id="30da3-126">Crie objetos [**CMediaSample**](cmediasample.md) que contenham partes de memória da etapa 2.</span><span class="sxs-lookup"><span data-stu-id="30da3-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="30da3-127">Adicione cada objeto **CMediaSample** à lista de amostras gratuitas ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="30da3-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="30da3-128">Para obter um exemplo, consulte [**CMemAllocator:: Alloc**](cmemallocator-alloc.md).</span><span class="sxs-lookup"><span data-stu-id="30da3-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="30da3-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="30da3-129">Requirements</span></span>



| <span data-ttu-id="30da3-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="30da3-130">Requirement</span></span> | <span data-ttu-id="30da3-131">Valor</span><span class="sxs-lookup"><span data-stu-id="30da3-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="30da3-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="30da3-132">Header</span></span><br/>  | <dl> <span data-ttu-id="30da3-133"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="30da3-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="30da3-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="30da3-134">Library</span></span><br/> | <dl> <span data-ttu-id="30da3-135"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="30da3-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="30da3-136">Consulte também</span><span class="sxs-lookup"><span data-stu-id="30da3-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="30da3-137">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="30da3-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




