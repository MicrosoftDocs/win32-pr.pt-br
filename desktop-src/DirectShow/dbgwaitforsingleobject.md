---
description: Aguarda a um objeto ser sinalizado.
ms.assetid: 5fbcccd9-9db7-4834-852a-86f28218e92e
title: Função DbgWaitForSingleObject (Wxdebug. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DbgWaitForSingleObject
api_type:
- LibDef
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 99d0058a60b5cf5b362adb80855a788d9a597af6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105812784"
---
# <a name="dbgwaitforsingleobject-function"></a><span data-ttu-id="65e3a-103">Função DbgWaitForSingleObject</span><span class="sxs-lookup"><span data-stu-id="65e3a-103">DbgWaitForSingleObject function</span></span>

<span data-ttu-id="65e3a-104">Aguarda a um objeto ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="65e3a-104">Waits for an object to become signaled.</span></span>

<span data-ttu-id="65e3a-105">Em uma compilação de depuração, essa função acionará uma declaração se o intervalo de tempo limite expirar antes de o objeto ser sinalizado.</span><span class="sxs-lookup"><span data-stu-id="65e3a-105">In a debug build, this function triggers an assert if the time-out interval expires before the object is signaled.</span></span> <span data-ttu-id="65e3a-106">Para definir o intervalo de tempo limite, chame a função [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) .</span><span class="sxs-lookup"><span data-stu-id="65e3a-106">To set the time-out interval, call the [**DbgSetWaitTimeout**](dbgsetwaittimeout.md) function.</span></span>

<span data-ttu-id="65e3a-107">Em uma compilação de varejo, essa função é equivalente à função **WaitForSingleObject** com um intervalo de tempo limite de infinito.</span><span class="sxs-lookup"><span data-stu-id="65e3a-107">In a retail build, this function is equivalent to the **WaitForSingleObject** function with a time-out interval of INFINITE.</span></span>

## <a name="syntax"></a><span data-ttu-id="65e3a-108">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="65e3a-108">Syntax</span></span>


```C++
DWORD DbgWaitForSingleObject(
   HANDLE h
);
```



## <a name="parameters"></a><span data-ttu-id="65e3a-109">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="65e3a-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="65e3a-110">*h*</span><span class="sxs-lookup"><span data-stu-id="65e3a-110">*h*</span></span> 
</dt> <dd>

<span data-ttu-id="65e3a-111">Identificador para o objeto.</span><span class="sxs-lookup"><span data-stu-id="65e3a-111">Handle to the object.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="65e3a-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="65e3a-112">Requirements</span></span>



| <span data-ttu-id="65e3a-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="65e3a-113">Requirement</span></span> | <span data-ttu-id="65e3a-114">Valor</span><span class="sxs-lookup"><span data-stu-id="65e3a-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="65e3a-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="65e3a-115">Header</span></span><br/>  | <dl> <span data-ttu-id="65e3a-116"><dt>Wxdebug. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="65e3a-116"><dt>Wxdebug.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="65e3a-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="65e3a-117">Library</span></span><br/> | <dl> <span data-ttu-id="65e3a-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="65e3a-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65e3a-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="65e3a-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65e3a-120">Aguardar funções de depuração</span><span class="sxs-lookup"><span data-stu-id="65e3a-120">Wait Debugging Functions</span></span>](wait-debugging-functions.md)
</dt> </dl>

 

 




