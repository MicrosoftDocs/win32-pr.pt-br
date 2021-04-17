---
description: 'O método SetProperties especifica o número de buffers a serem alocados e o tamanho de cada buffer. Esse método substitui o método CBaseAllocator:: SetProperties.'
ms.assetid: 8d419432-a9a7-44fb-b916-8dacd08eb6ec
title: Método CImageAllocator. SetProperties (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.SetProperties
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 6c04501fe3511d9cdd45f3513c68082d2ffece0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105747821"
---
# <a name="cimageallocatorsetproperties-method"></a><span data-ttu-id="a6cad-104">Método CImageAllocator. SetProperties</span><span class="sxs-lookup"><span data-stu-id="a6cad-104">CImageAllocator.SetProperties method</span></span>

<span data-ttu-id="a6cad-105">O `SetProperties` método especifica o número de buffers a serem alocados e o tamanho de cada buffer.</span><span class="sxs-lookup"><span data-stu-id="a6cad-105">The `SetProperties` method specifies the number of buffers to allocate and the size of each buffer.</span></span> <span data-ttu-id="a6cad-106">Esse método substitui o método [**CBaseAllocator:: SetProperties**](cbaseallocator-setproperties.md) .</span><span class="sxs-lookup"><span data-stu-id="a6cad-106">This method overrides the [**CBaseAllocator::SetProperties**](cbaseallocator-setproperties.md) method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6cad-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6cad-107">Syntax</span></span>


```C++
HRESULT SetProperties(
   ALLOCATOR_PROPERTIES *pRequest,
   ALLOCATOR_PROPERTIES *pActual
);
```



## <a name="parameters"></a><span data-ttu-id="a6cad-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6cad-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6cad-109">*pRequest*</span><span class="sxs-lookup"><span data-stu-id="a6cad-109">*pRequest*</span></span> 
</dt> <dd>

<span data-ttu-id="a6cad-110">Ponteiro para uma estrutura de [**\_ Propriedades de alocador**](/windows/win32/api/strmif/ns-strmif-allocator_properties) que contém os requisitos de buffer.</span><span class="sxs-lookup"><span data-stu-id="a6cad-110">Pointer to an [**ALLOCATOR\_PROPERTIES**](/windows/win32/api/strmif/ns-strmif-allocator_properties) structure that contains the buffer requirements.</span></span>

</dd> <dt>

<span data-ttu-id="a6cad-111">*pActual*</span><span class="sxs-lookup"><span data-stu-id="a6cad-111">*pActual*</span></span> 
</dt> <dd>

<span data-ttu-id="a6cad-112">Ponteiro para uma estrutura de **\_ Propriedades de alocador** que recebe as propriedades reais do buffer.</span><span class="sxs-lookup"><span data-stu-id="a6cad-112">Pointer to an **ALLOCATOR\_PROPERTIES** structure that receives the actual buffer properties.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6cad-113">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6cad-113">Return value</span></span>

<span data-ttu-id="a6cad-114">Retorna um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="a6cad-114">Returns an **HRESULT** value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6cad-115">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6cad-115">Remarks</span></span>

<span data-ttu-id="a6cad-116">Esse método chama [**CImageAllocator:: CheckSizes**](cimageallocator-checksizes.md) para validar o tamanho do buffer solicitado.</span><span class="sxs-lookup"><span data-stu-id="a6cad-116">This method calls [**CImageAllocator::CheckSizes**](cimageallocator-checksizes.md) to validate the requested buffer size.</span></span> <span data-ttu-id="a6cad-117">Ele também chama a versão de classe base do `SetProperties` .</span><span class="sxs-lookup"><span data-stu-id="a6cad-117">It also calls the base-class version of `SetProperties`.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6cad-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6cad-118">Requirements</span></span>



| <span data-ttu-id="a6cad-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6cad-119">Requirement</span></span> | <span data-ttu-id="a6cad-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a6cad-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6cad-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6cad-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a6cad-122"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6cad-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a6cad-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6cad-123">Library</span></span><br/> | <dl> <span data-ttu-id="a6cad-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a6cad-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6cad-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6cad-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6cad-126">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="a6cad-126">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




