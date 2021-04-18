---
description: Método destruidor.
ms.assetid: eed6c566-8a03-4a97-9d99-8e500ce2954c
title: CAMThread. ~ CAMThread Destruitor (Wxutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMThread.~CAMThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: b0b0a4dde858811a75347105b9fccd2f499c4faa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105749273"
---
# <a name="camthreadcamthread-destructor"></a><span data-ttu-id="e6de5-103">Destruidor CAMThread. ~ CAMThread</span><span class="sxs-lookup"><span data-stu-id="e6de5-103">CAMThread.~CAMThread destructor</span></span>

<span data-ttu-id="e6de5-104">Método destruidor.</span><span class="sxs-lookup"><span data-stu-id="e6de5-104">Destructor method.</span></span>

## <a name="syntax"></a><span data-ttu-id="e6de5-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="e6de5-105">Syntax</span></span>


```C++
virtual ~CAMThread();
```



## <a name="remarks"></a><span data-ttu-id="e6de5-106">Comentários</span><span class="sxs-lookup"><span data-stu-id="e6de5-106">Remarks</span></span>

<span data-ttu-id="e6de5-107">O destruidor chama o método [**CAMThread:: Close**](camthread-close.md) , que aguarda a saída do thread.</span><span class="sxs-lookup"><span data-stu-id="e6de5-107">The destructor calls the [**CAMThread::Close**](camthread-close.md) method, which waits for the thread to exit.</span></span>

## <a name="requirements"></a><span data-ttu-id="e6de5-108">Requisitos</span><span class="sxs-lookup"><span data-stu-id="e6de5-108">Requirements</span></span>



| <span data-ttu-id="e6de5-109">Requisito</span><span class="sxs-lookup"><span data-stu-id="e6de5-109">Requirement</span></span> | <span data-ttu-id="e6de5-110">Valor</span><span class="sxs-lookup"><span data-stu-id="e6de5-110">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e6de5-111">parâmetro</span><span class="sxs-lookup"><span data-stu-id="e6de5-111">Header</span></span><br/>  | <dl> <span data-ttu-id="e6de5-112"><dt>Wxutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="e6de5-112"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="e6de5-113">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="e6de5-113">Library</span></span><br/> | <dl> <span data-ttu-id="e6de5-114"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="e6de5-114"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e6de5-115">Confira também</span><span class="sxs-lookup"><span data-stu-id="e6de5-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e6de5-116">**Classe CAMThread**</span><span class="sxs-lookup"><span data-stu-id="e6de5-116">**CAMThread Class**</span></span>](camthread.md)
</dt> </dl>

 

 




