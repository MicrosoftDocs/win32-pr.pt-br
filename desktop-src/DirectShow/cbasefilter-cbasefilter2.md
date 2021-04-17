---
description: Método de construtor.
ms.assetid: b6433ec9-6710-4c2f-968f-00e0d9f8c7a5
title: Construtor CBaseFilter. CBaseFilter (const TCHAR *, LPUNKNOWN, CCritSec*, REFCLSID) (Amfilter. h)
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
ms.openlocfilehash: 40ac48a1fd28b9b50a8f1fa9c698ea5db49d97b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105748832"
---
# <a name="cbasefiltercbasefilterconst-tchar-lpunknown-ccritsec-refclsid-constructor"></a><span data-ttu-id="effd4-103">Construtor CBaseFilter. CBaseFilter (const TCHAR \* , LPUNKNOWN, CCritSec \* , REFCLSID)</span><span class="sxs-lookup"><span data-stu-id="effd4-103">CBaseFilter.CBaseFilter(const TCHAR\*, LPUNKNOWN, CCritSec\*, REFCLSID) constructor</span></span>

<span data-ttu-id="effd4-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="effd4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="effd4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="effd4-105">Syntax</span></span>


```C++
CBaseFilter(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         CCritSec  *pLock,
         REFCLSID  clsid
);
```



## <a name="parameters"></a><span data-ttu-id="effd4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="effd4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="effd4-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="effd4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="effd4-108">Ponteiro para uma cadeia de caracteres que contém o nome do filtro, para fins de depuração.</span><span class="sxs-lookup"><span data-stu-id="effd4-108">Pointer to a string containing the name of the filter, for debugging purposes.</span></span>

</dd> <dt>

<span data-ttu-id="effd4-109">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="effd4-109">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="effd4-110">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="effd4-110">Pointer to the owner of this object.</span></span> <span data-ttu-id="effd4-111">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="effd4-111">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="effd4-112">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="effd4-112">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="effd4-113">*pLock*</span><span class="sxs-lookup"><span data-stu-id="effd4-113">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="effd4-114">Ponteiro para um bloqueio de [**CCritSec**](ccritsec.md) , usado para serializar alterações de estado.</span><span class="sxs-lookup"><span data-stu-id="effd4-114">Pointer to a [**CCritSec**](ccritsec.md) lock, used to serialize state changes.</span></span>

</dd> <dt>

<span data-ttu-id="effd4-115">*CLSID*</span><span class="sxs-lookup"><span data-stu-id="effd4-115">*clsid*</span></span> 
</dt> <dd>

<span data-ttu-id="effd4-116">Identificador de classe (CLSID) do filtro.</span><span class="sxs-lookup"><span data-stu-id="effd4-116">Class identifier (CLSID) of the filter.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="effd4-117">Comentários</span><span class="sxs-lookup"><span data-stu-id="effd4-117">Remarks</span></span>

<span data-ttu-id="effd4-118">Para o objeto seção crítica, você normalmente faria um dos seguintes:</span><span class="sxs-lookup"><span data-stu-id="effd4-118">For the critical section object, you would typically do one of the following:</span></span>

-   <span data-ttu-id="effd4-119">Derive uma classe que herde **CBaseFilter** e **CCritSec**.</span><span class="sxs-lookup"><span data-stu-id="effd4-119">Derive a class that inherits both **CBaseFilter** and **CCritSec**.</span></span> <span data-ttu-id="effd4-120">Para *pLock*, passe o `this` ponteiro.</span><span class="sxs-lookup"><span data-stu-id="effd4-120">For *pLock*, pass the `this` pointer.</span></span>
-   <span data-ttu-id="effd4-121">Derive uma classe que herda **CBaseFilter** e contém uma variável de membro **CCritSec** .</span><span class="sxs-lookup"><span data-stu-id="effd4-121">Derive a class that inherits **CBaseFilter** and contains a **CCritSec** member variable.</span></span> <span data-ttu-id="effd4-122">Para *pLock*, passe o endereço dessa variável.</span><span class="sxs-lookup"><span data-stu-id="effd4-122">For *pLock*, pass the address of that variable.</span></span>

## <a name="requirements"></a><span data-ttu-id="effd4-123">Requisitos</span><span class="sxs-lookup"><span data-stu-id="effd4-123">Requirements</span></span>



| <span data-ttu-id="effd4-124">Requisito</span><span class="sxs-lookup"><span data-stu-id="effd4-124">Requirement</span></span> | <span data-ttu-id="effd4-125">Valor</span><span class="sxs-lookup"><span data-stu-id="effd4-125">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="effd4-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="effd4-126">Header</span></span><br/>  | <dl> <span data-ttu-id="effd4-127"><dt>Amfilter. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="effd4-127"><dt>Amfilter.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="effd4-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="effd4-128">Library</span></span><br/> | <dl> <span data-ttu-id="effd4-129"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="effd4-129"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="effd4-130">Confira também</span><span class="sxs-lookup"><span data-stu-id="effd4-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="effd4-131">**Classe CBaseFilter**</span><span class="sxs-lookup"><span data-stu-id="effd4-131">**CBaseFilter Class**</span></span>](cbasefilter.md)
</dt> </dl>

 

 




