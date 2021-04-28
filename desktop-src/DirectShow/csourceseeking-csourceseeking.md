---
description: Construtor de CSourceSeeking. CSourceSeeking-método de construtor.
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
ms.openlocfilehash: 7fcca70408e76466a88c620e3907271d49930973
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098814"
---
# <a name="csourceseekingcsourceseeking-constructor"></a><span data-ttu-id="4f961-103">Construtor CSourceSeeking. CSourceSeeking</span><span class="sxs-lookup"><span data-stu-id="4f961-103">CSourceSeeking.CSourceSeeking constructor</span></span>

<span data-ttu-id="4f961-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="4f961-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f961-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="4f961-105">Syntax</span></span>


```C++
CSourceSeeking(
   const TCHAR     *pName,
         LPUNKNOWN pUnk,
         HRESULT   *phr,
         CCritSec  *pLock
);
```



## <a name="parameters"></a><span data-ttu-id="4f961-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="4f961-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4f961-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="4f961-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="4f961-108">Ponteiro para uma cadeia de caracteres que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="4f961-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="4f961-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="4f961-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="4f961-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="4f961-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="4f961-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="4f961-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="4f961-112">Se o objeto for agregado, passe um ponteiro para a interface **IUnknown** do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="4f961-112">If the object is aggregated, pass a pointer to the aggregating object's **IUnknown** interface.</span></span> <span data-ttu-id="4f961-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="4f961-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="4f961-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="4f961-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="4f961-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="4f961-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="4f961-116">Ignorado.</span><span class="sxs-lookup"><span data-stu-id="4f961-116">Ignored.</span></span>

</dd> <dt>

<span data-ttu-id="4f961-117">*pLock*</span><span class="sxs-lookup"><span data-stu-id="4f961-117">*pLock*</span></span> 
</dt> <dd>

<span data-ttu-id="4f961-118">Ponteiro para um objeto [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="4f961-118">Pointer to a [**CCritSec**](ccritsec.md) object.</span></span> <span data-ttu-id="4f961-119">Na classe derivada, declare uma variável de membro **CCritSec** e use o endereço dela para esse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="4f961-119">In your derived class, declare a **CCritSec** member variable and use the address of it for this parameter.</span></span> <span data-ttu-id="4f961-120">A `CSourceSeeking` classe usa essa seção crítica para sincronizar o acesso às horas de início e parada, à duração e à taxa de reprodução.</span><span class="sxs-lookup"><span data-stu-id="4f961-120">The `CSourceSeeking` class uses this critical section to synchronize access to the start and stop times, duration, and playback rate.</span></span> <span data-ttu-id="4f961-121">Sempre que você acessar essas variáveis em sua classe derivada, mantenha esse bloqueio.</span><span class="sxs-lookup"><span data-stu-id="4f961-121">Whenever you access those variables in your derived class, hold this lock.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4f961-122">Requisitos</span><span class="sxs-lookup"><span data-stu-id="4f961-122">Requirements</span></span>



| <span data-ttu-id="4f961-123">Requisito</span><span class="sxs-lookup"><span data-stu-id="4f961-123">Requirement</span></span> | <span data-ttu-id="4f961-124">Valor</span><span class="sxs-lookup"><span data-stu-id="4f961-124">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4f961-125">parâmetro</span><span class="sxs-lookup"><span data-stu-id="4f961-125">Header</span></span><br/>  | <dl> <span data-ttu-id="4f961-126"><dt>Ctlutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="4f961-126"><dt>Ctlutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="4f961-127">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="4f961-127">Library</span></span><br/> | <dl> <span data-ttu-id="4f961-128"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="4f961-128"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4f961-129">Consulte também</span><span class="sxs-lookup"><span data-stu-id="4f961-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4f961-130">**Classe CSourceSeeking**</span><span class="sxs-lookup"><span data-stu-id="4f961-130">**CSourceSeeking Class**</span></span>](csourceseeking.md)
</dt> </dl>

 

 




