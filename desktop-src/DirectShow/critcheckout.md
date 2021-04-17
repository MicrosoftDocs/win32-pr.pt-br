---
description: Retornará FALSE se o thread atual for o proprietário da seção crítica especificada.
ms.assetid: 1a2cb56c-2806-4bb2-b904-985af332b290
title: Função CritCheckOut (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckOut
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ae5a888e619f6bed9cda203ccd8a197b0b25c001
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105787394"
---
# <a name="critcheckout-function"></a><span data-ttu-id="9f878-103">Função CritCheckOut</span><span class="sxs-lookup"><span data-stu-id="9f878-103">CritCheckOut function</span></span>

<span data-ttu-id="9f878-104">Retornará **false** se o thread atual for o proprietário da seção crítica especificada.</span><span class="sxs-lookup"><span data-stu-id="9f878-104">Returns **FALSE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="9f878-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="9f878-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckOut(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="9f878-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="9f878-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9f878-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="9f878-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="9f878-108">Ponteiro para uma seção crítica [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="9f878-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9f878-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="9f878-109">Return value</span></span>

<span data-ttu-id="9f878-110">Em compilações de depuração, retorna **falso** se o thread atual for o proprietário desta seção crítica ou **verdadeiro** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="9f878-110">In debug builds, returns **FALSE** if the current thread is the owner of this critical section, or **TRUE** otherwise.</span></span> <span data-ttu-id="9f878-111">Em compilações de varejo, sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="9f878-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="9f878-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="9f878-112">Remarks</span></span>

<span data-ttu-id="9f878-113">Essa função é o inverso da função [**CritCheckIn**](critcheckin.md) .</span><span class="sxs-lookup"><span data-stu-id="9f878-113">This function is the inverse of the [**CritCheckIn**](critcheckin.md) function.</span></span> <span data-ttu-id="9f878-114">Se **CritCheckIn** retornar **true**, **CritCheckOut** retornará **false** e vice-versa.</span><span class="sxs-lookup"><span data-stu-id="9f878-114">If **CritCheckIn** returns **TRUE**, **CritCheckOut** returns **FALSE**, and vice versa.</span></span>

## <a name="requirements"></a><span data-ttu-id="9f878-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="9f878-115">Requirements</span></span>



| <span data-ttu-id="9f878-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="9f878-116">Requirement</span></span> | <span data-ttu-id="9f878-117">Valor</span><span class="sxs-lookup"><span data-stu-id="9f878-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="9f878-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="9f878-118">Header</span></span><br/>  | <dl> <span data-ttu-id="9f878-119"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="9f878-119"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="9f878-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="9f878-120">Library</span></span><br/> | <dl> <span data-ttu-id="9f878-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="9f878-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9f878-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="9f878-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9f878-123">Funções de depuração de seção crítica</span><span class="sxs-lookup"><span data-stu-id="9f878-123">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




