---
description: Recupera o identificador do thread.
ms.assetid: c2b25342-841a-46cb-862c-01761fc60363
title: Método CMsgThread. GetThreadId (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.GetThreadID
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0819810b9b7589fc5272c0e79f87fc2f34325f5e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105756813"
---
# <a name="cmsgthreadgetthreadid-method"></a><span data-ttu-id="b2f15-103">Método CMsgThread. GetThreadId</span><span class="sxs-lookup"><span data-stu-id="b2f15-103">CMsgThread.GetThreadID method</span></span>

<span data-ttu-id="b2f15-104">Recupera o identificador do thread.</span><span class="sxs-lookup"><span data-stu-id="b2f15-104">Retrieves the thread's identifier.</span></span>

## <a name="syntax"></a><span data-ttu-id="b2f15-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b2f15-105">Syntax</span></span>


```C++
DWORD GetThreadID();
```



## <a name="parameters"></a><span data-ttu-id="b2f15-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b2f15-106">Parameters</span></span>

<span data-ttu-id="b2f15-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b2f15-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b2f15-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b2f15-108">Return value</span></span>

<span data-ttu-id="b2f15-109">Retorna o membro de dados privados **m \_ ThreadID** .</span><span class="sxs-lookup"><span data-stu-id="b2f15-109">Returns the **m\_ThreadId** private data member.</span></span>

## <a name="remarks"></a><span data-ttu-id="b2f15-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b2f15-110">Remarks</span></span>

<span data-ttu-id="b2f15-111">Essa função retorna o identificador Win32 da Microsoft para o thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="b2f15-111">This function returns the Microsoft Win32 identifier for the worker thread.</span></span> <span data-ttu-id="b2f15-112">Você pode chamar essa função de membro no thread de trabalho ou em um thread de cliente.</span><span class="sxs-lookup"><span data-stu-id="b2f15-112">You can call this member function on either the worker thread or a client thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="b2f15-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b2f15-113">Requirements</span></span>



| <span data-ttu-id="b2f15-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b2f15-114">Requirement</span></span> | <span data-ttu-id="b2f15-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b2f15-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b2f15-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b2f15-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b2f15-117"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b2f15-117"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="b2f15-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b2f15-118">Library</span></span><br/> | <dl> <span data-ttu-id="b2f15-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b2f15-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b2f15-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b2f15-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b2f15-121">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="b2f15-121">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




