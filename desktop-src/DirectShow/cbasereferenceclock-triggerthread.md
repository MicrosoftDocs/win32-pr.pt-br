---
description: O método TriggerThread ativa o thread de trabalho que lida com o agendamento.
ms.assetid: 296a6b59-fc52-4f5e-8a19-6b534a253a6e
title: Método CBaseReferenceClock. TriggerThread (Refclock. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseReferenceClock.TriggerThread
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 1f18b4f7dee15ea95046091da006f537830fcbb7
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105754554"
---
# <a name="cbasereferenceclocktriggerthread-method"></a><span data-ttu-id="55bfa-103">Método CBaseReferenceClock. TriggerThread</span><span class="sxs-lookup"><span data-stu-id="55bfa-103">CBaseReferenceClock.TriggerThread method</span></span>

<span data-ttu-id="55bfa-104">O `TriggerThread` método ativa o thread de trabalho que lida com o agendamento.</span><span class="sxs-lookup"><span data-stu-id="55bfa-104">The `TriggerThread` method wakes up the worker thread that handles scheduling.</span></span>

## <a name="syntax"></a><span data-ttu-id="55bfa-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="55bfa-105">Syntax</span></span>


```C++
void TriggerThread();
```



## <a name="parameters"></a><span data-ttu-id="55bfa-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="55bfa-106">Parameters</span></span>

<span data-ttu-id="55bfa-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="55bfa-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="55bfa-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="55bfa-108">Return value</span></span>

<span data-ttu-id="55bfa-109">Esse método não retorna um valor.</span><span class="sxs-lookup"><span data-stu-id="55bfa-109">This method does not return a value.</span></span>

## <a name="remarks"></a><span data-ttu-id="55bfa-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="55bfa-110">Remarks</span></span>

<span data-ttu-id="55bfa-111">O relógio usa um thread de trabalho que chama o método [**CAMSchedule:: Advise**](camschedule-advise.md) em momentos apropriados.</span><span class="sxs-lookup"><span data-stu-id="55bfa-111">The clock uses a worker thread that calls the [**CAMSchedule::Advise**](camschedule-advise.md) method at appropriate times.</span></span> <span data-ttu-id="55bfa-112">A classe derivada pode chamar `TriggerThread` para ativar o thread.</span><span class="sxs-lookup"><span data-stu-id="55bfa-112">The derived class can call `TriggerThread` to wake up the thread.</span></span>

## <a name="requirements"></a><span data-ttu-id="55bfa-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="55bfa-113">Requirements</span></span>



| <span data-ttu-id="55bfa-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="55bfa-114">Requirement</span></span> | <span data-ttu-id="55bfa-115">Valor</span><span class="sxs-lookup"><span data-stu-id="55bfa-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="55bfa-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="55bfa-116">Header</span></span><br/>  | <dl> <span data-ttu-id="55bfa-117"><dt>Refclock. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="55bfa-117"><dt>Refclock.h (include Streams.h)</dt></span></span> </dl>                                                                                  |
| <span data-ttu-id="55bfa-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="55bfa-118">Library</span></span><br/> | <dl> <span data-ttu-id="55bfa-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="55bfa-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="55bfa-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="55bfa-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="55bfa-121">**Classe CBaseReferenceClock**</span><span class="sxs-lookup"><span data-stu-id="55bfa-121">**CBaseReferenceClock Class**</span></span>](cbasereferenceclock.md)
</dt> </dl>

 

 




