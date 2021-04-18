---
description: Habilita ou desabilita o log de depuração de uma determinada seção crítica.
ms.assetid: 6e6e3de4-8bea-4e28-b04e-54a52226b59a
title: Função DbgLockTrace (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgLockTrace
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 8daf3c33b43bda95bb1d54145e9e5aebc6f89c2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751879"
---
# <a name="dbglocktrace-function"></a><span data-ttu-id="a6731-103">Função DbgLockTrace</span><span class="sxs-lookup"><span data-stu-id="a6731-103">DbgLockTrace function</span></span>

<span data-ttu-id="a6731-104">Habilita ou desabilita o log de depuração de uma determinada seção crítica.</span><span class="sxs-lookup"><span data-stu-id="a6731-104">Enables or disables debug logging of a given critical section.</span></span>

## <a name="syntax"></a><span data-ttu-id="a6731-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a6731-105">Syntax</span></span>


```C++
void WINAPI DbgLockTrace(
   CCritSec *pcCrit,
   BOOL     fTrace
);
```



## <a name="parameters"></a><span data-ttu-id="a6731-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a6731-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6731-107">*pcCrit*</span><span class="sxs-lookup"><span data-stu-id="a6731-107">*pcCrit*</span></span> 
</dt> <dd>

<span data-ttu-id="a6731-108">Ponteiro para uma seção crítica [**CCritSec**](ccritsec.md) .</span><span class="sxs-lookup"><span data-stu-id="a6731-108">Pointer to a [**CCritSec**](ccritsec.md) critical section.</span></span>

</dd> <dt>

<span data-ttu-id="a6731-109">*fTrace*</span><span class="sxs-lookup"><span data-stu-id="a6731-109">*fTrace*</span></span> 
</dt> <dd>

<span data-ttu-id="a6731-110">Valor que especifica se o log está habilitado.</span><span class="sxs-lookup"><span data-stu-id="a6731-110">Value specifying whether logging is enabled.</span></span> <span data-ttu-id="a6731-111">Use **true** para habilitar o registro em log ou **false** para desabilitá-lo.</span><span class="sxs-lookup"><span data-stu-id="a6731-111">Use **TRUE** to enable logging or **FALSE** to disable it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6731-112">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="a6731-112">Return value</span></span>

<span data-ttu-id="a6731-113">Essa função não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="a6731-113">This function does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="a6731-114">Comentários</span><span class="sxs-lookup"><span data-stu-id="a6731-114">Remarks</span></span>

<span data-ttu-id="a6731-115">Use essa função para rastrear uma seção crítica específica.</span><span class="sxs-lookup"><span data-stu-id="a6731-115">Use this function to trace a specific critical section.</span></span> <span data-ttu-id="a6731-116">Por padrão, o log de depuração de seções críticas está desabilitado, devido ao grande número de seções críticas.</span><span class="sxs-lookup"><span data-stu-id="a6731-116">By default, debug logging of critical sections is disabled, because of the large number of critical sections.</span></span>

<span data-ttu-id="a6731-117">Para rastrear uma seção crítica, execute as seguintes etapas:</span><span class="sxs-lookup"><span data-stu-id="a6731-117">To trace a critical section, perform the following steps:</span></span>

1.  <span data-ttu-id="a6731-118">Defina Depurar ou \_ depurar antes de incluir os cabeçalhos do DirectShow.</span><span class="sxs-lookup"><span data-stu-id="a6731-118">Define DEBUG or \_DEBUG before you include the DirectShow headers.</span></span>
2.  <span data-ttu-id="a6731-119">Habilite o log de depuração para seções críticas, chamando [**DbgSetModuleLevel**](dbgsetmodulelevel.md) com o sinalizador de bloqueio de log \_ .</span><span class="sxs-lookup"><span data-stu-id="a6731-119">Enable debug logging for critical sections, by calling [**DbgSetModuleLevel**](dbgsetmodulelevel.md) with the LOG\_LOCKING flag.</span></span>
3.  <span data-ttu-id="a6731-120">Chame **DbgLockTrace** na seção crítica que você deseja rastrear.</span><span class="sxs-lookup"><span data-stu-id="a6731-120">Call **DbgLockTrace** on the critical section you want to trace.</span></span>

<span data-ttu-id="a6731-121">Em compilações de varejo, a função **DbgLockTrace** não tem efeito.</span><span class="sxs-lookup"><span data-stu-id="a6731-121">In retail builds, the **DbgLockTrace** function has no effect.</span></span>

## <a name="examples"></a><span data-ttu-id="a6731-122">Exemplos</span><span class="sxs-lookup"><span data-stu-id="a6731-122">Examples</span></span>

<span data-ttu-id="a6731-123">O exemplo de código a seguir mostra como rastrear uma seção crítica.</span><span class="sxs-lookup"><span data-stu-id="a6731-123">The following code example shows how to trace a critical section.</span></span>


```
DbgInitialise(g_hInst);
DbgSetModuleLevel(LOG_LOCKING, 3);

{
    CCritSec MyLock;
    DbgLockTrace(&MyLock, TRUE);
    
    CAutoLock cObjectLock(&MyLock);

    // Protected section of code.    
    DbgOutString("This code is inside a critical section.\n");

} // Lock goes out of scope here.

DbgTerminate();
```



## <a name="requirements"></a><span data-ttu-id="a6731-124">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a6731-124">Requirements</span></span>



| <span data-ttu-id="a6731-125">Requisito</span><span class="sxs-lookup"><span data-stu-id="a6731-125">Requirement</span></span> | <span data-ttu-id="a6731-126">Valor</span><span class="sxs-lookup"><span data-stu-id="a6731-126">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a6731-127">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a6731-127">Header</span></span><br/>  | <dl> <span data-ttu-id="a6731-128"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a6731-128"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="a6731-129">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a6731-129">Library</span></span><br/> | <dl> <span data-ttu-id="a6731-130"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a6731-130"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a6731-131">Confira também</span><span class="sxs-lookup"><span data-stu-id="a6731-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a6731-132">Funções de depuração de seção crítica</span><span class="sxs-lookup"><span data-stu-id="a6731-132">Critical Section Debugging Functions</span></span>](critical-section-debugging-functions.md)
</dt> </dl>

 

 




