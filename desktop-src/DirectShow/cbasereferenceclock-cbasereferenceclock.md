---
description: Construtor de CBaseReferenceClock. CBaseReferenceClock-método de construtor.
ms.assetid: 0fbfdc68-e1df-449f-a7d1-739504db8a2f
title: Construtor CBaseReferenceClock. CBaseReferenceClock (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.CBaseReferenceClock
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 9840bb9d733641ada7c45b0df1470a4150b8ec85
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 04/28/2021
ms.locfileid: "108119934"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="5af34-103">Construtor CBaseReferenceClock. CBaseReferenceClock</span><span class="sxs-lookup"><span data-stu-id="5af34-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="5af34-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="5af34-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="5af34-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="5af34-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="5af34-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="5af34-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5af34-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="5af34-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="5af34-108">Ponteiro para uma cadeia de caracteres que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="5af34-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="5af34-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="5af34-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="5af34-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="5af34-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="5af34-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="5af34-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="5af34-112">Se o objeto for agregado, passe um ponteiro para a interface IUnknown do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="5af34-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="5af34-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5af34-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5af34-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="5af34-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="5af34-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="5af34-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="5af34-116">Se ocorrer um erro, o método retornará um código de erro nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="5af34-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="5af34-117">Não defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="5af34-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="5af34-118">*pSched*</span><span class="sxs-lookup"><span data-stu-id="5af34-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="5af34-119">Ponteiro para um objeto [**CAMSchedule**](camschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="5af34-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="5af34-120">Se for **NULL**, esse método criará um novo objeto **CAMSchedule** .</span><span class="sxs-lookup"><span data-stu-id="5af34-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="5af34-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="5af34-121">Requirements</span></span>



| <span data-ttu-id="5af34-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="5af34-122">Requirement</span></span> | <span data-ttu-id="5af34-123">Valor</span><span class="sxs-lookup"><span data-stu-id="5af34-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="5af34-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="5af34-124">Header</span></span><br/>  | <dl> <span data-ttu-id="5af34-125"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="5af34-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="5af34-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="5af34-126">Library</span></span><br/> | <dl> <span data-ttu-id="5af34-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="5af34-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5af34-128">Consulte também</span><span class="sxs-lookup"><span data-stu-id="5af34-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5af34-129">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="5af34-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




