---
description: Método de construtor de Construtor CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec, \* REFCLSID, HRESULT \* ).
ms.assetid: 705a075e-3f0f-4e7d-94b6-3458f87b6718
title: Construtor CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID, HRESULT *) (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseFilter.CBaseFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: f85fc666d299d5e120f71cfeaec5fc2f88e72761
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108120104"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-hresult-constructor"></a><span data-ttu-id="6cfbd-103">Construtor CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec, \* REFCLSID, HRESULT \* )</span><span class="sxs-lookup"><span data-stu-id="6cfbd-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID, HRESULT\*) constructor</span></span>

<span data-ttu-id="6cfbd-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cfbd-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="6cfbd-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid,
         HRESULT   *phr
);
```



## <a name="parameters"></a><span data-ttu-id="6cfbd-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="6cfbd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cfbd-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="6cfbd-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="6cfbd-108">Ponteiro para uma cadeia de caracteres que contém o nome do filtro, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="6cfbd-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="6cfbd-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="6cfbd-110">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="6cfbd-111">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="6cfbd-112">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6cfbd-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="6cfbd-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="6cfbd-114">Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="6cfbd-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="6cfbd-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="6cfbd-116">Identificador de classe (CLSID) do filtro.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-116">Class identifier (CLSID) of the filter.</span></span>

</dd> <dt>

<span data-ttu-id="6cfbd-117">*phr*</span><span class="sxs-lookup"><span data-stu-id="6cfbd-117">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="6cfbd-118">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="6cfbd-118">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="6cfbd-119">O Construtor ignora esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-119">The constructor ignores this parameter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6cfbd-120">Comentários</span><span class="sxs-lookup"><span data-stu-id="6cfbd-120">Remarks</span></span>

<span data-ttu-id="6cfbd-121">Para o objeto seção crítica, você normalmente faria um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="6cfbd-121">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="6cfbd-122">Derive uma classe que herde **CBaseFilter** e **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-122">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="6cfbd-123">Para *pLock*, passe o `this` ponteiro.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-123">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="6cfbd-124">Derive uma classe que herda **CBaseFilter** e contém uma variável de membro **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="6cfbd-124">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="6cfbd-125">Para *pLock*, passe o endereço dessa variável.</span><span class="sxs-lookup"><span data-stu-id="6cfbd-125">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cfbd-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="6cfbd-126">Requirements</span></span>



| <span data-ttu-id="6cfbd-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="6cfbd-127">Requirement</span></span> | <span data-ttu-id="6cfbd-128">Valor</span><span class="sxs-lookup"><span data-stu-id="6cfbd-128">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="6cfbd-129">parâmetro</span><span class="sxs-lookup"><span data-stu-id="6cfbd-129">Header</span></span><br/>  | <dl> <span data-ttu-id="6cfbd-130"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="6cfbd-130"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="6cfbd-131">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="6cfbd-131">Library</span></span><br/> | <dl> <span data-ttu-id="6cfbd-132"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="6cfbd-132"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6cfbd-133">Consulte também</span><span class="sxs-lookup"><span data-stu-id="6cfbd-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cfbd-134">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="6cfbd-134">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




