---
description: Retornará TRUE se o thread atual for o proprietário da seção crítica especificada.
ms.assetid: 96158f08-07a0-42a9-b173-0a05456a5f3a
title: Função CritCheckIn (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CritCheckIn
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: ff31707dc409db1e72c36866150c5a0b24c53f9a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752890"
---
# <a name="critcheckin-function"></a><span data-ttu-id="7df85-103">Função CritCheckIn</span><span class="sxs-lookup"><span data-stu-id="7df85-103">CritCheckIn function</span></span>

<span data-ttu-id="7df85-104">Retornará **true** se o thread atual for o proprietário da seção crítica especificada.</span><span class="sxs-lookup"><span data-stu-id="7df85-104">Returns **TRUE** if the current thread is the owner of the specified critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="7df85-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="7df85-105">Syntax</span></span>


```C++
BOOL WINAPI CritCheckIn(
   CCritSec *pcCrit
);
```



## <a name="parameters"></a><span data-ttu-id="7df85-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="7df85-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7df85-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="7df85-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="7df85-108">Ponteiro para uma seção crítica [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="7df85-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7df85-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="7df85-109">Return value</span></span>

<span data-ttu-id="7df85-110">Em builds de depuração, retornará **true** se o thread atual for o proprietário desta seção crítica ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="7df85-110">In debug builds, returns **TRUE** if the current thread is the owner of this critical section, or **FALSE** otherwise.</span></span> <span data-ttu-id="7df85-111">Em compilações de varejo, sempre retorna **true**.</span><span class="sxs-lookup"><span data-stu-id="7df85-111">In retail builds, always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="7df85-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="7df85-112">Remarks</span></span>

<span data-ttu-id="7df85-113">Essa função é especialmente útil na macro [**Assert**](assert.md) , para testar se um thread possui um determinado bloqueio.</span><span class="sxs-lookup"><span data-stu-id="7df85-113">This function is especially useful within the [**ASSERT**](assert.md) macro, to test whether a thread owns a given lock.</span></span>

## <a name="examples"></a><span data-ttu-id="7df85-114">Exemplos</span><span class="sxs-lookup"><span data-stu-id="7df85-114">Examples</span></span>

<span data-ttu-id="7df85-115">O exemplo de código a seguir mostra como usar essa função:</span><span class="sxs-lookup"><span data-stu-id="7df85-115">The following code example shows how to use this function:</span></span>


```
{
    CCritSec MyLock;  // Critical section is not locked yet.
    
    ASSERT(CritCheckIn(&MyLock)); // This assert will fire.

    // Lock the critical section.    
    CAutoLock cObjectLock(&MyLock);
     
    ASSERT(CritCheckIn(&MyLock)); // This assert will not fire.

} // Lock goes out of scope here.
```



## <a name="requirements"></a><span data-ttu-id="7df85-116">Requisitos</span><span class="sxs-lookup"><span data-stu-id="7df85-116">Requirements</span></span>



| <span data-ttu-id="7df85-117">Requisito</span><span class="sxs-lookup"><span data-stu-id="7df85-117">Requirement</span></span> | <span data-ttu-id="7df85-118">Valor</span><span class="sxs-lookup"><span data-stu-id="7df85-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df85-119">parâmetro</span><span class="sxs-lookup"><span data-stu-id="7df85-119">Header</span></span><br/>  | <dl> <span data-ttu-id="7df85-120"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="7df85-120"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7df85-121">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="7df85-121">Library</span></span><br/> | <dl> <span data-ttu-id="7df85-122"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="7df85-122"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7df85-123">Confira também</span><span class="sxs-lookup"><span data-stu-id="7df85-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7df85-124">Funções de depuração de seção crítica</span><span class="sxs-lookup"><span data-stu-id="7df85-124">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




