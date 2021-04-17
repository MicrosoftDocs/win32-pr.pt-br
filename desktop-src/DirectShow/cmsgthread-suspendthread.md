---
description: Usa a função SuspendThread do Microsoft Win32 para suspender a operação de um thread em execução.
ms.assetid: 07d919a2-797d-47c3-83e3-c8e2d2b2cddd
title: Método CMsgThread. SuspendThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.SuspendThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 69190015104d712864965e757d82afbdcc852884
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105770281"
---
# <a name="cmsgthreadsuspendthread-method"></a><span data-ttu-id="672aa-103">Método CMsgThread. SuspendThread</span><span class="sxs-lookup"><span data-stu-id="672aa-103">CMsgThread.SuspendThread method</span></span>

<span data-ttu-id="672aa-104">Usa a função **SuspendThread** do Microsoft Win32 para suspender a operação de um thread em execução.</span><span class="sxs-lookup"><span data-stu-id="672aa-104">Uses the Microsoft Win32 **SuspendThread** function to suspend the operation of a running thread.</span></span>

## <a name="syntax"></a><span data-ttu-id="672aa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="672aa-105">Syntax</span></span>


```C++
DWORD SuspendThread();
```



## <a name="parameters"></a><span data-ttu-id="672aa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="672aa-106">Parameters</span></span>

<span data-ttu-id="672aa-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="672aa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="672aa-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="672aa-108">Return value</span></span>

<span data-ttu-id="672aa-109">Se a função de membro for realizada com sucesso, o valor de retorno será a contagem de suspensão anterior do thread.</span><span class="sxs-lookup"><span data-stu-id="672aa-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="672aa-110">Se a função de membro falhar, o valor de retorno será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="672aa-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="672aa-111">Para obter informações de erro estendidas, chame a função **GetLastError** do Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="672aa-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="remarks"></a><span data-ttu-id="672aa-112">Comentários</span><span class="sxs-lookup"><span data-stu-id="672aa-112">Remarks</span></span>

<span data-ttu-id="672aa-113">O thread do cliente chama essa função de membro para suspender a operação do thread de trabalho.</span><span class="sxs-lookup"><span data-stu-id="672aa-113">The client thread calls this member function to suspend the operation of the worker thread.</span></span> <span data-ttu-id="672aa-114">O thread de trabalho permanece suspenso e não será executado até que uma chamada adicional para a função de membro [**CMsgThread:: ResumeThread**](cmsgthread-resumethread.md) seja feita.</span><span class="sxs-lookup"><span data-stu-id="672aa-114">The worker thread remains suspended and will not execute until an additional call to the [**CMsgThread::ResumeThread**](cmsgthread-resumethread.md) member function is made.</span></span>

## <a name="requirements"></a><span data-ttu-id="672aa-115">Requisitos</span><span class="sxs-lookup"><span data-stu-id="672aa-115">Requirements</span></span>



| <span data-ttu-id="672aa-116">Requisito</span><span class="sxs-lookup"><span data-stu-id="672aa-116">Requirement</span></span> | <span data-ttu-id="672aa-117">Valor</span><span class="sxs-lookup"><span data-stu-id="672aa-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="672aa-118">parâmetro</span><span class="sxs-lookup"><span data-stu-id="672aa-118">Header</span></span><br/>  | <dl> <span data-ttu-id="672aa-119"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="672aa-119"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="672aa-120">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="672aa-120">Library</span></span><br/> | <dl> <span data-ttu-id="672aa-121"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="672aa-121"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="672aa-122">Confira também</span><span class="sxs-lookup"><span data-stu-id="672aa-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="672aa-123">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="672aa-123">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




