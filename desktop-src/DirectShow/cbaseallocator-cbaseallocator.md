---
description: Método de construtor.
ms.assetid: e697e377-6407-4316-9f04-fe3bdb814175
title: Construtor CBaseAllocator. CBaseAllocator (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseAllocator.CBaseAllocator
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 98a1ba1163058f92fba666177d0ff82331dd528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105750910"
---
# <a name="cbaseallocatorcbaseallocator-constructor"></a><span data-ttu-id="94e2b-103">Construtor CBaseAllocator. CBaseAllocator</span><span class="sxs-lookup"><span data-stu-id="94e2b-103">CBaseAllocator.CBaseAllocator constructor</span></span>

<span data-ttu-id="94e2b-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="94e2b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="94e2b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="94e2b-105">Syntax</span></span>


```C++
CBaseAllocator(
   TCHAR     *pName,
   LPUNKNOWN pUnk,
   HRESULT   *phr,
   BOOL      bEvent = TRUE,
   BOOL      fEnableReleaseCallback = FALSE
);
```



## <a name="parameters"></a><span data-ttu-id="94e2b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="94e2b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="94e2b-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="94e2b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="94e2b-108">Ponteiro para uma cadeia de caracteres que contém o nome de depuração do alocador.</span><span class="sxs-lookup"><span data-stu-id="94e2b-108">Pointer to a string containing the debug name of the allocator.</span></span> <span data-ttu-id="94e2b-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="94e2b-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="94e2b-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="94e2b-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="94e2b-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="94e2b-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="94e2b-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="94e2b-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="94e2b-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="94e2b-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="94e2b-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="94e2b-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="94e2b-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="94e2b-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="94e2b-116">Defina o valor como S \_ OK antes de criar o objeto.</span><span class="sxs-lookup"><span data-stu-id="94e2b-116">Set the value to S\_OK before creating the object.</span></span> <span data-ttu-id="94e2b-117">Se o Construtor falhar, o valor será definido como um código de erro.</span><span class="sxs-lookup"><span data-stu-id="94e2b-117">If the constructor fails, the value is set to an error code.</span></span>

</dd> <dt>

<span data-ttu-id="94e2b-118">*beventilação*</span><span class="sxs-lookup"><span data-stu-id="94e2b-118">*bEvent*</span></span> 
</dt> <dd>

<span data-ttu-id="94e2b-119">Valor booliano que indica se um semáforo deve ser criado.</span><span class="sxs-lookup"><span data-stu-id="94e2b-119">Boolean value indicating whether to create a semaphore.</span></span> <span data-ttu-id="94e2b-120">Se **for true**, o alocador criará um semáforo ([**CBaseAllocator:: m \_ hSem**](cbaseallocator-m-hsem.md)), que é sinalizado sempre que um exemplo se tornar disponível.</span><span class="sxs-lookup"><span data-stu-id="94e2b-120">If **TRUE**, the allocator creates a semaphore ([**CBaseAllocator::m\_hSem**](cbaseallocator-m-hsem.md)), which is signaled whenever a sample becomes available.</span></span> <span data-ttu-id="94e2b-121">Defina o valor como **false** se você estiver implementando uma classe derivada que não requer um semáforo.</span><span class="sxs-lookup"><span data-stu-id="94e2b-121">Set the value to **FALSE** if you are implementing a derived class that does not require a semaphore.</span></span>

</dd> <dt>

<span data-ttu-id="94e2b-122">*fEnableReleaseCallback*</span><span class="sxs-lookup"><span data-stu-id="94e2b-122">*fEnableReleaseCallback*</span></span> 
</dt> <dd>

<span data-ttu-id="94e2b-123">Valor booliano que indica se o mecanismo de retorno de chamada da versão está habilitado.</span><span class="sxs-lookup"><span data-stu-id="94e2b-123">Boolean value indicating whether the release callback mechanism is enabled.</span></span> <span data-ttu-id="94e2b-124">Defina o valor como **true** se desejar fornecer uma interface de retorno de chamada, que é chamada quando os buffers são liberados.</span><span class="sxs-lookup"><span data-stu-id="94e2b-124">Set the value to **TRUE** if you want to supply a callback interface, which is called when buffers are released.</span></span> <span data-ttu-id="94e2b-125">Especifique o retorno de chamada chamando o método [**CBaseAllocator:: Setnotificar**](cbaseallocator-setnotify.md) .</span><span class="sxs-lookup"><span data-stu-id="94e2b-125">Specify the callback by calling the [**CBaseAllocator::SetNotify**](cbaseallocator-setnotify.md) method.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="94e2b-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94e2b-126">Requirements</span></span>



| <span data-ttu-id="94e2b-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="94e2b-127">Requirement</span></span> | <span data-ttu-id="94e2b-128">Valor</span><span class="sxs-lookup"><span data-stu-id="94e2b-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94e2b-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94e2b-129">Header</span></span><br/>  | <dl> <span data-ttu-id="94e2b-130"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="94e2b-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="94e2b-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94e2b-131">Library</span></span><br/> | <dl> <span data-ttu-id="94e2b-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="94e2b-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="94e2b-133">Confira também</span><span class="sxs-lookup"><span data-stu-id="94e2b-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94e2b-134">**Classe CBaseAllocator**</span><span class="sxs-lookup"><span data-stu-id="94e2b-134">**CBaseAllocator Class**</span></span>](cbaseallocator.md)
</dt> </dl>

 

 




