---
description: Método de construtor.
ms.assetid: 91290f58-a77b-447f-aa2a-bbee067f5a98
title: Construtor CBaseMediaFilter. CBaseMediaFilter (Amfilter. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseMediaFilter.CBaseMediaFilter
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8498e9da88804291fc5cdb900ff1dbda212e8b0f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105753362"
---
# <a name="cbasemediafiltercbasemediafilter-constructor"></a><span data-ttu-id="a0e3b-103">Construtor CBaseMediaFilter. CBaseMediaFilter</span><span class="sxs-lookup"><span data-stu-id="a0e3b-103">CBaseMediaFilter.CBaseMediaFilter constructor</span></span>

<span data-ttu-id="a0e3b-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="a0e3b-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a0e3b-105">Syntax</span></span>


```C++
CBaseMediaFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="a0e3b-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a0e3b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a0e3b-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="a0e3b-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="a0e3b-108">Ponteiro para uma cadeia de caracteres que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-108">Pointer to a string containing the name of the object.</span></span>

</dd> <dt>

<span data-ttu-id="a0e3b-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="a0e3b-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="a0e3b-110">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="a0e3b-111">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="a0e3b-112">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="a0e3b-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="a0e3b-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="a0e3b-114">Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="a0e3b-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="a0e3b-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="a0e3b-116">Identificador de classe do objeto.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-116">Class identifier of the object.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="a0e3b-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="a0e3b-117">Remarks</span></span>

<span data-ttu-id="a0e3b-118">Se outro objeto contiver ou agregar o `CBaseMediaFilter` objeto, o bloqueio **CCritSec** poderá ser externo ao `CBaseMediaFilter` objeto.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-118">If another object contains or aggregates the `CBaseMediaFilter` object, the **CCritSec** lock might be external to the `CBaseMediaFilter` object.</span></span> <span data-ttu-id="a0e3b-119">Nesse caso, passe um ponteiro para o bloqueio em *pLock*.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-119">In that case, pass a pointer to the lock in *pLock*.</span></span>

<span data-ttu-id="a0e3b-120">Caso contrário, você pode:</span><span class="sxs-lookup"><span data-stu-id="a0e3b-120">Otherwise, you can:</span></span>

-   <span data-ttu-id="a0e3b-121">Derive uma classe que herda `CBaseMediaFilter` e **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-121">Derive a class that inherits both `CBaseMediaFilter` and **CCritSec**.</span></span> <span data-ttu-id="a0e3b-122">Para *pLock*, passe o ponteiro.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-122">For *pLock*, pass the this pointer.</span></span>
-   <span data-ttu-id="a0e3b-123">Derive uma classe que herda `CBaseMediaFilter` e contém uma variável de membro **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="a0e3b-123">Derive a class that inherits `CBaseMediaFilter` and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="a0e3b-124">Para *pLock*, passe o endereço dessa variável.</span><span class="sxs-lookup"><span data-stu-id="a0e3b-124">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="a0e3b-125">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a0e3b-125">Requirements</span></span>



| <span data-ttu-id="a0e3b-126">Requisito</span><span class="sxs-lookup"><span data-stu-id="a0e3b-126">Requirement</span></span> | <span data-ttu-id="a0e3b-127">Valor</span><span class="sxs-lookup"><span data-stu-id="a0e3b-127">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a0e3b-128">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a0e3b-128">Header</span></span><br/>  | <dl> <span data-ttu-id="a0e3b-129"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a0e3b-129"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="a0e3b-130">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a0e3b-130">Library</span></span><br/> | <dl> <span data-ttu-id="a0e3b-131"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a0e3b-131"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a0e3b-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="a0e3b-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a0e3b-133">**Classe CBaseMediaFilter**</span><span class="sxs-lookup"><span data-stu-id="a0e3b-133">**CBaseMediaFilter Class**</span></span>](cbasemediafilter.md)
</dt> </dl>

 

 




