---
description: O método de alocação aloca memória para os buffers.
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
ms.openlocfilehash: b7510a108e69eb218a894b67dd5b62d94bfdbe6c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756652"
---
# <a name="cbaseallocatoralloc-method"></a><span data-ttu-id="fefaa-103">Método CBaseAllocator. Alloc</span><span class="sxs-lookup"><span data-stu-id="fefaa-103">CBaseAllocator.Alloc method</span></span>

<span data-ttu-id="fefaa-104">O `Alloc` método aloca memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="fefaa-104">The `Alloc` method allocates memory for the buffers.</span></span>

## <a name="syntax"></a><span data-ttu-id="fefaa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fefaa-105">Syntax</span></span>


```C++
virtual HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="fefaa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fefaa-106">Parameters</span></span>

<span data-ttu-id="fefaa-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fefaa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fefaa-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fefaa-108">Return value</span></span>

<span data-ttu-id="fefaa-109">Retorna um dos valores de **HRESULT** a seguir.</span><span class="sxs-lookup"><span data-stu-id="fefaa-109">Returns one of the following **HRESULT** values.</span></span>



| <span data-ttu-id="fefaa-110">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="fefaa-110">Return code</span></span>                                                                                       | <span data-ttu-id="fefaa-111">Descrição</span><span class="sxs-lookup"><span data-stu-id="fefaa-111">Description</span></span>                                      |
|---------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="fefaa-112"><dt>**\_falso**</dt></span><span class="sxs-lookup"><span data-stu-id="fefaa-112"><dt>**S\_FALSE**</dt></span></span> </dl>           | <span data-ttu-id="fefaa-113">Os requisitos de buffer não foram alterados.</span><span class="sxs-lookup"><span data-stu-id="fefaa-113">Buffer requirements have not changed.</span></span><br/> |
| <dl> <span data-ttu-id="fefaa-114"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="fefaa-114"><dt>**S\_OK**</dt></span></span> </dl>              | <span data-ttu-id="fefaa-115">Os requisitos de buffer foram alterados.</span><span class="sxs-lookup"><span data-stu-id="fefaa-115">Buffer requirements have changed.</span></span><br/>     |
| <dl> <span data-ttu-id="fefaa-116"><dt>**VFW \_ E \_ SIZENOTSET**</dt></span><span class="sxs-lookup"><span data-stu-id="fefaa-116"><dt>**VFW\_E\_SIZENOTSET**</dt></span></span> </dl> | <span data-ttu-id="fefaa-117">Os requisitos de buffer não foram definidos.</span><span class="sxs-lookup"><span data-stu-id="fefaa-117">Buffer requirements were not set.</span></span><br/>     |



 

## <a name="remarks"></a><span data-ttu-id="fefaa-118">Comentários</span><span class="sxs-lookup"><span data-stu-id="fefaa-118">Remarks</span></span>

<span data-ttu-id="fefaa-119">Esse método é chamado pelo método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) .</span><span class="sxs-lookup"><span data-stu-id="fefaa-119">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method.</span></span>

<span data-ttu-id="fefaa-120">Na classe base, esse método não aloca nenhuma memória.</span><span class="sxs-lookup"><span data-stu-id="fefaa-120">In the base class, this method does not allocate any memory.</span></span> <span data-ttu-id="fefaa-121">Ele retornará um erro se os requisitos de buffer não tiverem sido definidos, S \_ false se os requisitos não foram alterados e s \_ OK se os requisitos foram alterados.</span><span class="sxs-lookup"><span data-stu-id="fefaa-121">It returns an error if the buffer requirements were not set, S\_FALSE if the requirements have not changed, and S\_OK if the requirements have changed.</span></span>

<span data-ttu-id="fefaa-122">Uma classe derivada deve substituir esse método para executar a alocação de memória real.</span><span class="sxs-lookup"><span data-stu-id="fefaa-122">A derived class should override this method to perform the actual memory allocation.</span></span> <span data-ttu-id="fefaa-123">Normalmente, a classe derivada executará as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="fefaa-123">Typically, the derived class will perform the following steps:</span></span>

1.  <span data-ttu-id="fefaa-124">Chame a implementação da classe base para determinar se a memória realmente precisa ser alocada.</span><span class="sxs-lookup"><span data-stu-id="fefaa-124">Call the base class implementation, to determine whether the memory truly needs allocating.</span></span>
2.  <span data-ttu-id="fefaa-125">Aloque memória.</span><span class="sxs-lookup"><span data-stu-id="fefaa-125">Allocate memory.</span></span>
3.  <span data-ttu-id="fefaa-126">Crie objetos [**CMediaSample**](cmediasample.md) que contenham partes de memória da etapa 2.</span><span class="sxs-lookup"><span data-stu-id="fefaa-126">Create [**CMediaSample**](cmediasample.md) objects that contain chunks of memory from step 2.</span></span>
4.  <span data-ttu-id="fefaa-127">Adicione cada objeto **CMediaSample** à lista de amostras gratuitas ([**CBaseAllocator:: m \_ lFree**](cbaseallocator-m-lfree.md)).</span><span class="sxs-lookup"><span data-stu-id="fefaa-127">Add each **CMediaSample** object to the list of free samples ([**CBaseAllocator::m\_lFree**](cbaseallocator-m-lfree.md)).</span></span>

<span data-ttu-id="fefaa-128">Para obter um exemplo, consulte [**CMemAllocator:: Alloc**](cmemallocator-alloc.md).</span><span class="sxs-lookup"><span data-stu-id="fefaa-128">For an example, see [**CMemAllocator::Alloc**](cmemallocator-alloc.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="fefaa-129">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fefaa-129">Requirements</span></span>



| <span data-ttu-id="fefaa-130">Requisito</span><span class="sxs-lookup"><span data-stu-id="fefaa-130">Requirement</span></span> | <span data-ttu-id="fefaa-131">Valor</span><span class="sxs-lookup"><span data-stu-id="fefaa-131">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fefaa-132">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fefaa-132">Header</span></span><br/>  | <dl> <span data-ttu-id="fefaa-133"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fefaa-133"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="fefaa-134">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fefaa-134">Library</span></span><br/> | <dl> <span data-ttu-id="fefaa-135"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fefaa-135"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fefaa-136">Confira também</span><span class="sxs-lookup"><span data-stu-id="fefaa-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fefaa-137">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="fefaa-137">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




