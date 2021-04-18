---
description: O método Create cria o thread.
ms.assetid: 453972eb-7cf6-43c6-820e-c1992675260e
title: Método CAMThread. Create (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.Create
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 0316cf053326d23d45c0d82f3c410d68d68a92dd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105761773"
---
# <a name="camthreadcreate-method"></a><span data-ttu-id="b30e7-103">Método CAMThread. Create</span><span class="sxs-lookup"><span data-stu-id="b30e7-103">CAMThread.Create method</span></span>

<span data-ttu-id="b30e7-104">O `Create` método cria o thread.</span><span class="sxs-lookup"><span data-stu-id="b30e7-104">The `Create` method creates the thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="b30e7-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b30e7-105">Syntax</span></span>


```C++
BOOL Create();
```



## <a name="parameters"></a><span data-ttu-id="b30e7-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b30e7-106">Parameters</span></span>

<span data-ttu-id="b30e7-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="b30e7-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="b30e7-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b30e7-108">Return value</span></span>

<span data-ttu-id="b30e7-109">Retorna **verdadeiro** se for bem-sucedido ou **false** caso contrário.</span><span class="sxs-lookup"><span data-stu-id="b30e7-109">Returns **TRUE** if successful, or **FALSE** otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="b30e7-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="b30e7-110">Remarks</span></span>

<span data-ttu-id="b30e7-111">Esse método cria o thread, usando o método [**CAMThread:: InitialThreadProc**](camthread-initialthreadproc.md) para o procedimento de thread e `this` para o argumento thread.</span><span class="sxs-lookup"><span data-stu-id="b30e7-111">This method creates the thread, using the [**CAMThread::InitialThreadProc**](camthread-initialthreadproc.md) method for the thread procedure and `this` for the thread argument.</span></span>

<span data-ttu-id="b30e7-112">O método falhará se o thread já existir.</span><span class="sxs-lookup"><span data-stu-id="b30e7-112">The method fails if the thread already exists.</span></span>

## <a name="requirements"></a><span data-ttu-id="b30e7-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b30e7-113">Requirements</span></span>



| <span data-ttu-id="b30e7-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="b30e7-114">Requirement</span></span> | <span data-ttu-id="b30e7-115">Valor</span><span class="sxs-lookup"><span data-stu-id="b30e7-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b30e7-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b30e7-116">Header</span></span><br/>  | <dl> <span data-ttu-id="b30e7-117"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b30e7-117"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="b30e7-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b30e7-118">Library</span></span><br/> | <dl> <span data-ttu-id="b30e7-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b30e7-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b30e7-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="b30e7-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b30e7-121">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="b30e7-121">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




