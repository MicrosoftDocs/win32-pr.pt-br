---
description: 'O método InitialThreadProc chama o método COutputQueue:: ThreadProc quando o thread é criado.'
ms.assetid: 6093f0c3-ec58-418d-bb8c-618163c43ac7
title: COutputQueue.Inimétodo tialThreadProc (Outputq. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- COutputQueue.InitialThreadProc
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: dfc7b8660d838b6ad31dd298c509b6282ab61810
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105786983"
---
# <a name="coutputqueueinitialthreadproc-method"></a><span data-ttu-id="bc891-103">COutputQueue.Inimétodo tialThreadProc</span><span class="sxs-lookup"><span data-stu-id="bc891-103">COutputQueue.InitialThreadProc method</span></span>

<span data-ttu-id="bc891-104">O `InitialThreadProc` método chama o método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) quando o thread é criado.</span><span class="sxs-lookup"><span data-stu-id="bc891-104">The `InitialThreadProc` method calls the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method when the thread is created.</span></span>

## <a name="syntax"></a><span data-ttu-id="bc891-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="bc891-105">Syntax</span></span>


```C++
static DWORD WINAPI InitialThreadProc(
   LPVOID pv
);
```



## <a name="parameters"></a><span data-ttu-id="bc891-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="bc891-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="bc891-107">*PV*</span><span class="sxs-lookup"><span data-stu-id="bc891-107">*pv*</span></span> 
</dt> <dd>

<span data-ttu-id="bc891-108">`this` refere.</span><span class="sxs-lookup"><span data-stu-id="bc891-108">`this` pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="bc891-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="bc891-109">Return value</span></span>

<span data-ttu-id="bc891-110">Retorna o valor retornado pelo método [**COutputQueue:: ThreadProc**](coutputqueue-threadproc.md) .</span><span class="sxs-lookup"><span data-stu-id="bc891-110">Returns the value returned by the [**COutputQueue::ThreadProc**](coutputqueue-threadproc.md) method.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc891-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="bc891-111">Remarks</span></span>

<span data-ttu-id="bc891-112">Esse método é o procedimento de thread para o thread de trabalho do objeto.</span><span class="sxs-lookup"><span data-stu-id="bc891-112">This method is the thread procedure for the object's worker thread.</span></span> <span data-ttu-id="bc891-113">O ponteiro do objeto `this` é o parâmetro de thread.</span><span class="sxs-lookup"><span data-stu-id="bc891-113">The object's `this` pointer is the thread parameter.</span></span> <span data-ttu-id="bc891-114">O método faz referência a isso para chamar **ThreadProc**.</span><span class="sxs-lookup"><span data-stu-id="bc891-114">The method dereferences this to call **ThreadProc**.</span></span>

## <a name="requirements"></a><span data-ttu-id="bc891-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="bc891-115">Requirements</span></span>



| <span data-ttu-id="bc891-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="bc891-116">Requirement</span></span> | <span data-ttu-id="bc891-117">Valor</span><span class="sxs-lookup"><span data-stu-id="bc891-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bc891-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="bc891-118">Header</span></span><br/>  | <dl> <span data-ttu-id="bc891-119"><dt>Outputq. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="bc891-119"><dt>Outputq.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="bc891-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="bc891-120">Library</span></span><br/> | <dl> <span data-ttu-id="bc891-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="bc891-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="bc891-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="bc891-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bc891-123">**Classe COutputQueue**</span><span class="sxs-lookup"><span data-stu-id="bc891-123">**COutputQueue Class**</span></span>](coutputqueue.md)
</dt> </dl>

 

 




