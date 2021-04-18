---
description: Aguarda que qualquer (ou todos) os objetos especificados sejam sinalizados.
ms.assetid: e60c98b6-a4d2-40de-8297-727404e3c387
title: Função DbgWaitForMultipleObjects (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForMultipleObjects
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0e555afb4e6a82500876f11e6d1275e7de027f7e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105751672"
---
# <a name="dbgwaitformultipleobjects-function"></a><span data-ttu-id="a1801-103">Função DbgWaitForMultipleObjects</span><span class="sxs-lookup"><span data-stu-id="a1801-103">DbgWaitForMultipleObjects function</span></span>

<span data-ttu-id="a1801-104">Aguarda que qualquer (ou todos) os objetos especificados sejam sinalizados.</span><span class="sxs-lookup"><span data-stu-id="a1801-104">Waits for any (or all) of the specified objects to be signaled.</span></span>

<span data-ttu-id="a1801-105">Em uma compilação de depuração, essa função acionará uma declaração se o intervalo de tempo limite expirar antes que os objetos sejam sinalizados.</span><span class="sxs-lookup"><span data-stu-id="a1801-105">In a debug build, this function triggers an assert if the time-out interval expires before the objects are signaled.</span></span> <span data-ttu-id="a1801-106">Para definir o intervalo de tempo limite, chame a função [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="a1801-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="a1801-107">Em uma compilação de varejo, essa função é equivalente à função **WaitForMultipleObjects** com um intervalo de tempo limite de infinito.</span><span class="sxs-lookup"><span data-stu-id="a1801-107">In a retail build, this function is equivalent to the **WaitForMultipleObjects** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="a1801-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="a1801-108">Syntax</span></span>


```C++
DWORD DbgWaitForMultipleObjects(
   DWORD         nCount,
   CONST HANDLE  *lpHandles,
   BOOL          bWaitAll
);
```



## <a name="parameters"></a><span data-ttu-id="a1801-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="a1801-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1801-110">*nCount*</span><span class="sxs-lookup"><span data-stu-id="a1801-110">*nCount*</span></span> 
</dt> <dd>

<span data-ttu-id="a1801-111">Número de objetos.</span><span class="sxs-lookup"><span data-stu-id="a1801-111">Number of objects.</span></span>

</dd> <dt>

<span data-ttu-id="a1801-112">*lpHandles*</span><span class="sxs-lookup"><span data-stu-id="a1801-112">*lpHandles*</span></span> 
</dt> <dd>

<span data-ttu-id="a1801-113">Matriz de identificadores para objetos, de tamanho *nCount*.</span><span class="sxs-lookup"><span data-stu-id="a1801-113">Array of handles to objects, of size *nCount*.</span></span>

</dd> <dt>

<span data-ttu-id="a1801-114">*bWaitAll*</span><span class="sxs-lookup"><span data-stu-id="a1801-114">*bWaitAll*</span></span> 
</dt> <dd>

<span data-ttu-id="a1801-115">Valor booliano que especifica se deve aguardar todos os objetos.</span><span class="sxs-lookup"><span data-stu-id="a1801-115">Boolean value that specifies whether to wait for all of the objects.</span></span> <span data-ttu-id="a1801-116">Se **for true**, a função aguardará que todos os objetos sejam sinalizados.</span><span class="sxs-lookup"><span data-stu-id="a1801-116">If **TRUE**, the function waits for all of the objects to be signaled.</span></span> <span data-ttu-id="a1801-117">Caso contrário, ele aguarda pelo menos um objeto a ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="a1801-117">Otherwise, it waits for at least one object to be signaled.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="a1801-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="a1801-118">Requirements</span></span>



| <span data-ttu-id="a1801-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="a1801-119">Requirement</span></span> | <span data-ttu-id="a1801-120">Valor</span><span class="sxs-lookup"><span data-stu-id="a1801-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a1801-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="a1801-121">Header</span></span><br/>  | <dl> <span data-ttu-id="a1801-122"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="a1801-122"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="a1801-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="a1801-123">Library</span></span><br/> | <dl> <span data-ttu-id="a1801-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="a1801-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a1801-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="a1801-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a1801-126">Aguardar funções de depuração</span><span class="sxs-lookup"><span data-stu-id="a1801-126">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




