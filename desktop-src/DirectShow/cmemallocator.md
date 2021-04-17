---
description: Implementa um alocador que dá suporte à interface IMemAllocator.
ms.assetid: c40eccef-d915-4bf3-81b2-b20e000718fb
title: Classe CMemAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMemAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5adf390b7abf8fcbdb017ecde04bde76bf4bc001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770284"
---
# <a name="cmemallocator-class"></a><span data-ttu-id="3fb89-103">Classe CMemAllocator</span><span class="sxs-lookup"><span data-stu-id="3fb89-103">CMemAllocator class</span></span>

![hierarquia de classe CMemAllocator](images/filter10.png)

<span data-ttu-id="3fb89-105">Implementa um alocador que dá suporte à interface [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) .</span><span class="sxs-lookup"><span data-stu-id="3fb89-105">Implements an allocator that supports the [**IMemAllocator**](/windows/desktop/api/Strmif/nn-strmif-imemallocator) interface.</span></span>

<span data-ttu-id="3fb89-106">Essa classe deriva de [**CBaseAllocator**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="3fb89-106">This class derives from [**CBaseAllocator**](cbaseallocator.md).</span></span> <span data-ttu-id="3fb89-107">Para obter mais informações sobre os alocadores, consulte a documentação do [**CBaseAllocator**](cbaseallocator.md).</span><span class="sxs-lookup"><span data-stu-id="3fb89-107">For more information about allocators, refer to the documentation for [**CBaseAllocator**](cbaseallocator.md).</span></span>



| <span data-ttu-id="3fb89-108">Variáveis de membro protegido</span><span class="sxs-lookup"><span data-stu-id="3fb89-108">Protected Member Variables</span></span>                              | <span data-ttu-id="3fb89-109">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fb89-109">Description</span></span>                                                              |
|---------------------------------------------------------|--------------------------------------------------------------------------|
| [<span data-ttu-id="3fb89-110">**\_pBuffer m**</span><span class="sxs-lookup"><span data-stu-id="3fb89-110">**m\_pBuffer**</span></span>](cmemallocator-m-pbuffer.md)           | <span data-ttu-id="3fb89-111">Ponteiro para o bloco de memória que contém os buffers.</span><span class="sxs-lookup"><span data-stu-id="3fb89-111">Pointer to the memory block that contains the buffers.</span></span>                   |
| <span data-ttu-id="3fb89-112">Métodos Protegidos</span><span class="sxs-lookup"><span data-stu-id="3fb89-112">Protected Methods</span></span>                                       | <span data-ttu-id="3fb89-113">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fb89-113">Description</span></span>                                                              |
| [<span data-ttu-id="3fb89-114">**Informações**</span><span class="sxs-lookup"><span data-stu-id="3fb89-114">**Free**</span></span>](cmemallocator-free.md)                      | <span data-ttu-id="3fb89-115">Método de espaço reservado; chamado durante uma operação de desconfirmação.</span><span class="sxs-lookup"><span data-stu-id="3fb89-115">Placeholder method; called during a decommit operation.</span></span>                  |
| [<span data-ttu-id="3fb89-116">**ReallyFree**</span><span class="sxs-lookup"><span data-stu-id="3fb89-116">**ReallyFree**</span></span>](cmemallocator-reallyfree.md)          | <span data-ttu-id="3fb89-117">Libera a memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="3fb89-117">Releases the memory for the buffers.</span></span>                                     |
| [<span data-ttu-id="3fb89-118">**Alocação**</span><span class="sxs-lookup"><span data-stu-id="3fb89-118">**Alloc**</span></span>](cmemallocator-alloc.md)                    | <span data-ttu-id="3fb89-119">Aloca memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="3fb89-119">Allocates memory for the buffers.</span></span>                                        |
| <span data-ttu-id="3fb89-120">Métodos públicos</span><span class="sxs-lookup"><span data-stu-id="3fb89-120">Public Methods</span></span>                                          | <span data-ttu-id="3fb89-121">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fb89-121">Description</span></span>                                                              |
| [<span data-ttu-id="3fb89-122">**CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="3fb89-122">**CMemAllocator**</span></span>](cmemallocator-cmemallocator.md)    | <span data-ttu-id="3fb89-123">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="3fb89-123">Constructor method.</span></span>                                                      |
| [<span data-ttu-id="3fb89-124">**~ CMemAllocator**</span><span class="sxs-lookup"><span data-stu-id="3fb89-124">**~ CMemAllocator**</span></span>](cmemallocator--cmemallocator.md) | <span data-ttu-id="3fb89-125">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="3fb89-125">Destructor method.</span></span>                                                       |
| [<span data-ttu-id="3fb89-126">**CreateInstance**</span><span class="sxs-lookup"><span data-stu-id="3fb89-126">**CreateInstance**</span></span>](cmemallocator-createinstance.md)  | <span data-ttu-id="3fb89-127">Cria uma nova instância da classe **CMemAllocator** .</span><span class="sxs-lookup"><span data-stu-id="3fb89-127">Creates a new instance of the **CMemAllocator** class.</span></span>                   |
| <span data-ttu-id="3fb89-128">Métodos IMemAllocator</span><span class="sxs-lookup"><span data-stu-id="3fb89-128">IMemAllocator Methods</span></span>                                   | <span data-ttu-id="3fb89-129">Descrição</span><span class="sxs-lookup"><span data-stu-id="3fb89-129">Description</span></span>                                                              |
| [<span data-ttu-id="3fb89-130">**SetProperties**</span><span class="sxs-lookup"><span data-stu-id="3fb89-130">**SetProperties**</span></span>](cmemallocator-setproperties.md)    | <span data-ttu-id="3fb89-131">Especifica o número de buffers a serem alocados e o tamanho de cada buffer.</span><span class="sxs-lookup"><span data-stu-id="3fb89-131">Specifies the number of buffers to allocate and the size of each buffer.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="3fb89-132">Requisitos</span><span class="sxs-lookup"><span data-stu-id="3fb89-132">Requirements</span></span>



| <span data-ttu-id="3fb89-133">Requisito</span><span class="sxs-lookup"><span data-stu-id="3fb89-133">Requirement</span></span> | <span data-ttu-id="3fb89-134">Valor</span><span class="sxs-lookup"><span data-stu-id="3fb89-134">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3fb89-135">parâmetro</span><span class="sxs-lookup"><span data-stu-id="3fb89-135">Header</span></span><br/>  | <dl> <span data-ttu-id="3fb89-136"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="3fb89-136"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="3fb89-137">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="3fb89-137">Library</span></span><br/> | <dl> <span data-ttu-id="3fb89-138"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="3fb89-138"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3fb89-139">Confira também</span><span class="sxs-lookup"><span data-stu-id="3fb89-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3fb89-140">Fornecendo um alocador personalizado</span><span class="sxs-lookup"><span data-stu-id="3fb89-140">Providing a Custom Allocator</span></span>](providing-a-custom-allocator.md)
</dt> </dl>

 

 




