---
description: 'O método de alocação aloca memória para os buffers. Esse método substitui o método CBaseAllocator:: Alloc.'
ms.assetid: 4a246b4e-93b3-4adb-9f10-6b92d9f479eb
title: Método CImageAllocator. Alloc (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.Alloc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7acd13e2d2d09e6e491a2f338aef2fe7564b82b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752699"
---
# <a name="cimageallocatoralloc-method"></a><span data-ttu-id="25c19-104">Método CImageAllocator. Alloc</span><span class="sxs-lookup"><span data-stu-id="25c19-104">CImageAllocator.Alloc method</span></span>

<span data-ttu-id="25c19-105">O `Alloc` método aloca memória para os buffers.</span><span class="sxs-lookup"><span data-stu-id="25c19-105">The `Alloc` method allocates memory for the buffers.</span></span> <span data-ttu-id="25c19-106">Esse método substitui o método [**CBaseAllocator:: Alloc**](cbaseallocator-alloc.md) .</span><span class="sxs-lookup"><span data-stu-id="25c19-106">This method overrides the [**CBaseAllocator::Alloc**](cbaseallocator-alloc.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="25c19-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="25c19-107">Syntax</span></span>


```C++
HRESULT Alloc();
```



## <a name="parameters"></a><span data-ttu-id="25c19-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="25c19-108">Parameters</span></span>

<span data-ttu-id="25c19-109">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="25c19-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="25c19-110">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="25c19-110">Return value</span></span>

<span data-ttu-id="25c19-111">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="25c19-111">Returns an **HRESULT** value.</span></span> <span data-ttu-id="25c19-112">Os possíveis valores incluem os seguintes.</span><span class="sxs-lookup"><span data-stu-id="25c19-112">Possible values include the following.</span></span>



| <span data-ttu-id="25c19-113">Código de retorno</span><span class="sxs-lookup"><span data-stu-id="25c19-113">Return code</span></span>                                                                                   | <span data-ttu-id="25c19-114">Descrição</span><span class="sxs-lookup"><span data-stu-id="25c19-114">Description</span></span>                    |
|-----------------------------------------------------------------------------------------------|--------------------------------|
| <dl> <span data-ttu-id="25c19-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="25c19-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="25c19-116">Sucesso</span><span class="sxs-lookup"><span data-stu-id="25c19-116">Success</span></span><br/>             |
| <dl> <span data-ttu-id="25c19-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="25c19-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="25c19-118">Memória insuficiente</span><span class="sxs-lookup"><span data-stu-id="25c19-118">Insufficient memory</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="25c19-119">Comentários</span><span class="sxs-lookup"><span data-stu-id="25c19-119">Remarks</span></span>

<span data-ttu-id="25c19-120">Esse método é chamado pelo método [**CBaseAllocator:: Commit**](cbaseallocator-commit.md) , quando o filtro confirma o alocador.</span><span class="sxs-lookup"><span data-stu-id="25c19-120">This method is called by the [**CBaseAllocator::Commit**](cbaseallocator-commit.md) method, when the filter commits the allocator.</span></span>

<span data-ttu-id="25c19-121">Esse método cria uma lista de amostras de mídia, que são implementadas como objetos [**CImageSample**](cimagesample.md) .</span><span class="sxs-lookup"><span data-stu-id="25c19-121">This method creates a list of media samples, which are implemented as [**CImageSample**](cimagesample.md) objects.</span></span> <span data-ttu-id="25c19-122">Cada exemplo contém um bitmap independente de dispositivo GDI, usando a função **CreateDIBSection** do GDI.</span><span class="sxs-lookup"><span data-stu-id="25c19-122">Each sample contains a GDI device-independent bitmap, using the GDI **CreateDIBSection** function.</span></span>

<span data-ttu-id="25c19-123">Internamente, esse método chama [**CImageAllocator:: CreateDIB**](cimageallocator-createdib.md) para criar cada DIB e [**CImageAllocator:: CreateImageSample**](cimageallocator-createimagesample.md) para criar cada exemplo.</span><span class="sxs-lookup"><span data-stu-id="25c19-123">Internally this method calls [**CImageAllocator::CreateDIB**](cimageallocator-createdib.md) to create each DIB, and [**CImageAllocator::CreateImageSample**](cimageallocator-createimagesample.md) to create each sample.</span></span>

## <a name="requirements"></a><span data-ttu-id="25c19-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="25c19-124">Requirements</span></span>



| <span data-ttu-id="25c19-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="25c19-125">Requirement</span></span> | <span data-ttu-id="25c19-126">Valor</span><span class="sxs-lookup"><span data-stu-id="25c19-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="25c19-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="25c19-127">Header</span></span><br/>  | <dl> <span data-ttu-id="25c19-128"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="25c19-128"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="25c19-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="25c19-129">Library</span></span><br/> | <dl> <span data-ttu-id="25c19-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="25c19-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="25c19-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="25c19-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="25c19-132">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="25c19-132">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




