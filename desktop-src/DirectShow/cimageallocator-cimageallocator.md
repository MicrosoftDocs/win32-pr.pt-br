---
description: Construtor de CImageAllocator. CImageAllocator-método de construtor.
ms.assetid: 8c215b16-98e5-42fb-a95b-b6df1ade180e
title: Construtor CImageAllocator. CImageAllocator (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CImageAllocator.CImageAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f17ae78b668f6cc35e454c5e4e83d38727077ef7
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108085754"
---
# <a name="cimageallocatorcimageallocator-constructor"></a><span data-ttu-id="09dd3-103">Construtor CImageAllocator. CImageAllocator</span><span class="sxs-lookup"><span data-stu-id="09dd3-103">CImageAllocator.CImageAllocator constructor</span></span>

<span data-ttu-id="09dd3-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="09dd3-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="09dd3-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="09dd3-105">Syntax</span></span>


```C++
CImageAllocator(
   CBaseFilter *pFilter,
   TCHAR       *pName,
   HRESULT     *phr
);
```



## <a name="parameters"></a><span data-ttu-id="09dd3-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="09dd3-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="09dd3-107">*pFilter*</span><span class="sxs-lookup"><span data-stu-id="09dd3-107">*pFilter*</span></span> 
</dt> <dd>

<span data-ttu-id="09dd3-108">Ponteiro para o filtro proprietário.</span><span class="sxs-lookup"><span data-stu-id="09dd3-108">Pointer to the owning filter.</span></span>

</dd> <dt>

<span data-ttu-id="09dd3-109">*pName*</span><span class="sxs-lookup"><span data-stu-id="09dd3-109">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="09dd3-110">Ponteiro para uma cadeia de caracteres que contém o nome de depuração do alocador.</span><span class="sxs-lookup"><span data-stu-id="09dd3-110">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="09dd3-111">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="09dd3-111">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="09dd3-112">*phr*</span><span class="sxs-lookup"><span data-stu-id="09dd3-112">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="09dd3-113">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="09dd3-113">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="09dd3-114">Defina o valor como S \_ OK antes de criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="09dd3-114">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="09dd3-115">Se o Construtor falhar, o valor será definido como um código de erro.</span><span class="sxs-lookup"><span data-stu-id="09dd3-115">If the constructor fails, the value is set to an error code.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="09dd3-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="09dd3-116">Requirements</span></span>



| <span data-ttu-id="09dd3-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="09dd3-117">Requirement</span></span> | <span data-ttu-id="09dd3-118">Valor</span><span class="sxs-lookup"><span data-stu-id="09dd3-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="09dd3-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="09dd3-119">Header</span></span><br/>  | <dl> <span data-ttu-id="09dd3-120"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="09dd3-120"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="09dd3-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="09dd3-121">Library</span></span><br/> | <dl> <span data-ttu-id="09dd3-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="09dd3-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="09dd3-123">Consulte também</span><span class="sxs-lookup"><span data-stu-id="09dd3-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="09dd3-124">**Classe CImageAllocator**</span><span class="sxs-lookup"><span data-stu-id="09dd3-124">**CImageAllocator Class**</span></span>](cimageallocator.md)
</dt> </dl>

 

 




