---
description: Método de construtor.
ms.assetid: a51d90c9-4046-42dc-b7cf-51b904c5f57a
title: Construtor CSourceSeeking. CSourceSeeking (Ctlutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSourceSeeking.CSourceSeeking
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 309e926ddf001cf9933b19334992f5210fc7f17b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752693"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="0b7f4-103">Construtor CSourceSeeking. CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="0b7f4-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="0b7f4-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="0b7f4-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="0b7f4-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="0b7f4-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="0b7f4-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0b7f4-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="0b7f4-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="0b7f4-108">Ponteiro para uma cadeia de caracteres que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="0b7f4-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="0b7f4-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="0b7f4-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="0b7f4-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="0b7f4-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="0b7f4-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="0b7f4-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="0b7f4-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="0b7f4-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="0b7f4-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="0b7f4-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="0b7f4-116">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="0b7f4-117">*pLock*</span><span class="sxs-lookup"><span data-stu-id="0b7f4-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="0b7f4-118">Ponteiro para um objeto [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="0b7f4-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="0b7f4-119">Na classe derivada, declare uma variável de membro **CCritSec** e use o endereço dela para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="0b7f4-120">A `CSourceSeeking` classe usa essa seção crítica para sincronizar o acesso às horas de início e parada, à duração e à taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="0b7f4-121">Sempre que você acessar essas variáveis em sua classe derivada, mantenha esse bloqueio.</span><span class="sxs-lookup"><span data-stu-id="0b7f4-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0b7f4-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="0b7f4-122">Requirements</span></span>



| <span data-ttu-id="0b7f4-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="0b7f4-123">Requirement</span></span> | <span data-ttu-id="0b7f4-124">Valor</span><span class="sxs-lookup"><span data-stu-id="0b7f4-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="0b7f4-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="0b7f4-125">Header</span></span><br/>  | <dl> <span data-ttu-id="0b7f4-126"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="0b7f4-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="0b7f4-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="0b7f4-127">Library</span></span><br/> | <dl> <span data-ttu-id="0b7f4-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="0b7f4-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0b7f4-129">Confira também</span><span class="sxs-lookup"><span data-stu-id="0b7f4-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0b7f4-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="0b7f4-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




