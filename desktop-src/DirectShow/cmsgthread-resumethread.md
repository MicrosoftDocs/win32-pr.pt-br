---
description: 'Usa a função ResumeThread do Microsoft Win32 para continuar a operação do thread de trabalho após uma chamada anterior para a função de membro CMsgThread:: SuspendThread.'
ms.assetid: 5c94a079-5c74-4024-8fb0-71c7ef9c7e73
title: Método CMsgThread. ResumeThread (Msgthrd. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsgThread.ResumeThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 3e0a20bb60f4a10a06ef50f58c449496cae8050d
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105759312"
---
# <a name="cmsgthreadresumethread-method"></a><span data-ttu-id="2b175-103">Método CMsgThread. ResumeThread</span><span class="sxs-lookup"><span data-stu-id="2b175-103">CMsgThread.ResumeThread method</span></span>

<span data-ttu-id="2b175-104">Usa a função **ResumeThread** do Microsoft Win32 para continuar a operação do thread de trabalho após uma chamada anterior para a função de membro [**CMsgThread:: SuspendThread**](cmsgthread-suspendthread.md) .</span><span class="sxs-lookup"><span data-stu-id="2b175-104">Uses the Microsoft Win32 **ResumeThread** function to continue the operation of the worker thread after a previous call to the [**CMsgThread::SuspendThread**](cmsgthread-suspendthread.md) member function.</span></span>

## <a name="syntax"></a><span data-ttu-id="2b175-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="2b175-105">Syntax</span></span>


```C++
DWORD ResumeThread();
```



## <a name="parameters"></a><span data-ttu-id="2b175-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="2b175-106">Parameters</span></span>

<span data-ttu-id="2b175-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="2b175-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="2b175-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="2b175-108">Return value</span></span>

<span data-ttu-id="2b175-109">Se a função de membro for realizada com sucesso, o valor de retorno será a contagem de suspensão anterior do thread.</span><span class="sxs-lookup"><span data-stu-id="2b175-109">If the member function succeeds, the return value is the previous suspend count of the thread.</span></span> <span data-ttu-id="2b175-110">Se a função de membro falhar, o valor de retorno será 0xFFFFFFFF.</span><span class="sxs-lookup"><span data-stu-id="2b175-110">If the member function fails, the return value is 0xFFFFFFFF.</span></span> <span data-ttu-id="2b175-111">Para obter informações de erro estendidas, chame a função **GetLastError** do Microsoft Win32.</span><span class="sxs-lookup"><span data-stu-id="2b175-111">To obtain extended error information, call the Microsoft Win32 **GetLastError** function.</span></span>

## <a name="requirements"></a><span data-ttu-id="2b175-112">Requisitos</span><span class="sxs-lookup"><span data-stu-id="2b175-112">Requirements</span></span>



| <span data-ttu-id="2b175-113">Requisito</span><span class="sxs-lookup"><span data-stu-id="2b175-113">Requirement</span></span> | <span data-ttu-id="2b175-114">Valor</span><span class="sxs-lookup"><span data-stu-id="2b175-114">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="2b175-115">parâmetro</span><span class="sxs-lookup"><span data-stu-id="2b175-115">Header</span></span><br/>  | <dl> <span data-ttu-id="2b175-116"><dt>Msgthrd. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="2b175-116"><dt>Msgthrd.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="2b175-117">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="2b175-117">Library</span></span><br/> | <dl> <span data-ttu-id="2b175-118"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="2b175-118"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="2b175-119">Confira também</span><span class="sxs-lookup"><span data-stu-id="2b175-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2b175-120">**Classe CMsgThread**</span><span class="sxs-lookup"><span data-stu-id="2b175-120">**CMsgThread Class**</span></span>](cmsgthread.md)
</dt> </dl>

 

 




