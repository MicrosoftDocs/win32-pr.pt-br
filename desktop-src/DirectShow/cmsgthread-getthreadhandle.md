---
description: Recupera o identificador para o thread no objeto CMsgThread.
ms.assetid: dacbdc68-91a0-46d4-805f-fe51cb047e19
title: Método CMsgThread. GetThreadHandle (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadHandle
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b61d7bfb11f78be3c1d23275589c8cb1c62259bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759135"
---
# <a name="cmsgthreadgetthreadhandle-method"></a><span data-ttu-id="57a5d-103">Método CMsgThread. GetThreadHandle</span><span class="sxs-lookup"><span data-stu-id="57a5d-103">CMsgThread.GetThreadHandle method</span></span>

<span data-ttu-id="57a5d-104">Recupera o identificador para o thread no objeto [**CMsgThread**](cmsgthread.md) .</span><span class="sxs-lookup"><span data-stu-id="57a5d-104">Retrieves the handle to the thread in the [**CMsgThread**](cmsgthread.md) object.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a5d-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="57a5d-105">Syntax</span></span>


```C++
HANDLE GetThreadHandle();
```



## <a name="parameters"></a><span data-ttu-id="57a5d-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="57a5d-106">Parameters</span></span>

<span data-ttu-id="57a5d-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="57a5d-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="57a5d-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="57a5d-108">Return value</span></span>

<span data-ttu-id="57a5d-109">Retorna o identificador de thread.</span><span class="sxs-lookup"><span data-stu-id="57a5d-109">Returns the thread handle.</span></span>

## <a name="remarks"></a><span data-ttu-id="57a5d-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="57a5d-110">Remarks</span></span>

<span data-ttu-id="57a5d-111">O identificador de thread pode ser passado para funções de espera, como [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span><span class="sxs-lookup"><span data-stu-id="57a5d-111">The thread handle can be passed to wait functions, such as [**WaitForMultipleObjects**](/windows/desktop/api/synchapi/nf-synchapi-waitformultipleobjects).</span></span> <span data-ttu-id="57a5d-112">O identificador de thread é sinalizado quando o thread foi encerrado.</span><span class="sxs-lookup"><span data-stu-id="57a5d-112">The thread handle is signaled when the thread has exited.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a5d-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="57a5d-113">Requirements</span></span>



| <span data-ttu-id="57a5d-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="57a5d-114">Requirement</span></span> | <span data-ttu-id="57a5d-115">Valor</span><span class="sxs-lookup"><span data-stu-id="57a5d-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="57a5d-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="57a5d-116">Header</span></span><br/>  | <dl> <span data-ttu-id="57a5d-117"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="57a5d-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="57a5d-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="57a5d-118">Library</span></span><br/> | <dl> <span data-ttu-id="57a5d-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="57a5d-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="57a5d-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="57a5d-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a5d-121">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="57a5d-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

