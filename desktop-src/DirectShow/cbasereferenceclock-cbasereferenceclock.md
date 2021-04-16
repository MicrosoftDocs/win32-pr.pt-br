---
description: Método de construtor.
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
ms.openlocfilehash: 5ad593d488e367ad6e902b0c931ffbfc3f741a53
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758243"
---
# <a name="cbasereferenceclockcbasereferenceclock-constructor"></a><span data-ttu-id="e563e-103">Construtor CBaseReferenceClock. CBaseReferenceClock</span><span class="sxs-lookup"><span data-stu-id="e563e-103">CBaseReferenceClock.CBaseReferenceClock constructor</span></span>

<span data-ttu-id="e563e-104">Método de construtor.</span><span class="sxs-lookup"><span data-stu-id="e563e-104">Constructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e563e-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e563e-105">Syntax</span></span>


```C++
CBaseReferenceClock(
   TCHAR       *pName,
   LPUNKNOWN   pUnk,
   HRESULT     *phr,
   CAMSchedule *pSched = NULL
);
```



## <a name="parameters"></a><span data-ttu-id="e563e-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="e563e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e563e-107">*pName*</span><span class="sxs-lookup"><span data-stu-id="e563e-107">*pName*</span></span> 
</dt> <dd>

<span data-ttu-id="e563e-108">Ponteiro para uma cadeia de caracteres que contém o nome do objeto.</span><span class="sxs-lookup"><span data-stu-id="e563e-108">Pointer to a string containing the name of the object.</span></span> <span data-ttu-id="e563e-109">Para obter mais informações, consulte [**CBaseObject**](cbaseobject.md).</span><span class="sxs-lookup"><span data-stu-id="e563e-109">For more information, see [**CBaseObject**](cbaseobject.md).</span></span>

</dd> <dt>

<span data-ttu-id="e563e-110">*pUnk*</span><span class="sxs-lookup"><span data-stu-id="e563e-110">*pUnk*</span></span> 
</dt> <dd>

<span data-ttu-id="e563e-111">Ponteiro para o proprietário deste objeto.</span><span class="sxs-lookup"><span data-stu-id="e563e-111">Pointer to the owner of this object.</span></span> <span data-ttu-id="e563e-112">Se o objeto for agregado, passe um ponteiro para a interface IUnknown do objeto de agregação.</span><span class="sxs-lookup"><span data-stu-id="e563e-112">If the object is aggregated, pass a pointer to the aggregating object's IUnknown interface.</span></span> <span data-ttu-id="e563e-113">Caso contrário, defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e563e-113">Otherwise, set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e563e-114">*phr*</span><span class="sxs-lookup"><span data-stu-id="e563e-114">*phr*</span></span> 
</dt> <dd>

<span data-ttu-id="e563e-115">Ponteiro para um valor **HRESULT** .</span><span class="sxs-lookup"><span data-stu-id="e563e-115">Pointer to an **HRESULT** value.</span></span> <span data-ttu-id="e563e-116">Se ocorrer um erro, o método retornará um código de erro nesse parâmetro.</span><span class="sxs-lookup"><span data-stu-id="e563e-116">If an error occurs, the method returns an error code in this parameter.</span></span> <span data-ttu-id="e563e-117">Não defina esse parâmetro como **NULL**.</span><span class="sxs-lookup"><span data-stu-id="e563e-117">Do not set this parameter to **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="e563e-118">*pSched*</span><span class="sxs-lookup"><span data-stu-id="e563e-118">*pSched*</span></span> 
</dt> <dd>

<span data-ttu-id="e563e-119">Ponteiro para um objeto [**CAMSchedule**](camschedule.md) .</span><span class="sxs-lookup"><span data-stu-id="e563e-119">Pointer to a [**CAMSchedule**](camschedule.md) object.</span></span> <span data-ttu-id="e563e-120">Se for **NULL**, esse método criará um novo objeto **CAMSchedule** .</span><span class="sxs-lookup"><span data-stu-id="e563e-120">If **NULL**, this method creates a new **CAMSchedule** object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e563e-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e563e-121">Requirements</span></span>



| <span data-ttu-id="e563e-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="e563e-122">Requirement</span></span> | <span data-ttu-id="e563e-123">Valor</span><span class="sxs-lookup"><span data-stu-id="e563e-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e563e-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e563e-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e563e-125"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e563e-125"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="e563e-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e563e-126">Library</span></span><br/> | <dl> <span data-ttu-id="e563e-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e563e-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e563e-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="e563e-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e563e-129">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="e563e-129">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




