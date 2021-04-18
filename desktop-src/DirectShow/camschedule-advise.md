---
description: O método Advise despacha todas as solicitações agendadas para um período especificado ou anterior.
ms.assetid: 09ea84b7-517a-4ea6-9e03-0d9cd8f72e1f
title: Método CAMSchedule. Advise (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.Advise
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 70880243cef294ebe747463cd11737027faf9277
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105758884"
---
# <a name="camscheduleadvise-method"></a><span data-ttu-id="508ee-103">Método CAMSchedule. Advise</span><span class="sxs-lookup"><span data-stu-id="508ee-103">CAMSchedule.Advise method</span></span>

<span data-ttu-id="508ee-104">O `Advise` método despacha todas as solicitações agendadas para um período especificado ou anterior.</span><span class="sxs-lookup"><span data-stu-id="508ee-104">The `Advise` method dispatches all requests that are scheduled for a specified time or earlier.</span></span>

## <a name="syntax"></a><span data-ttu-id="508ee-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="508ee-105">Syntax</span></span>


```C++
REFERENCE_TIME Advise(
  [ref] const REFERENCE_TIME &rtTime
);
```



## <a name="parameters"></a><span data-ttu-id="508ee-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="508ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="508ee-107">*rtTime* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="508ee-107">*rtTime* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="508ee-108">Valor que especifica o tempo de referência atual.</span><span class="sxs-lookup"><span data-stu-id="508ee-108">Value that specifies the current reference time.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="508ee-109">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="508ee-109">Return value</span></span>

<span data-ttu-id="508ee-110">Retorna o tempo de referência da próxima solicitação de aviso agendada ou o \_ tempo máximo se não houver nenhum restante.</span><span class="sxs-lookup"><span data-stu-id="508ee-110">Returns the reference time of the next scheduled advise request, or MAX\_TIME if there are none left.</span></span>

## <a name="remarks"></a><span data-ttu-id="508ee-111">Comentários</span><span class="sxs-lookup"><span data-stu-id="508ee-111">Remarks</span></span>

<span data-ttu-id="508ee-112">Quando o relógio chama esse método, ele especifica o tempo de referência atual.</span><span class="sxs-lookup"><span data-stu-id="508ee-112">When the clock calls this method, it specifies the current reference time.</span></span> <span data-ttu-id="508ee-113">O Agendador determina quais solicitações de aviso expiraram, se houver, e as expedem.</span><span class="sxs-lookup"><span data-stu-id="508ee-113">The scheduler determines which advise requests have expired, if any, and dispatches them.</span></span> <span data-ttu-id="508ee-114">Se uma solicitação de uma única expirar, o Agendador a excluirá.</span><span class="sxs-lookup"><span data-stu-id="508ee-114">If a one-shot request expires, the scheduler deletes it.</span></span> <span data-ttu-id="508ee-115">Se uma solicitação periódica expirar, o Agendador o agendará novamente para o próximo horário de aviso.</span><span class="sxs-lookup"><span data-stu-id="508ee-115">If a periodic request expires, the scheduler re-schedules it for the next advise time.</span></span> <span data-ttu-id="508ee-116">O método retorna a hora da próxima solicitação pendente.</span><span class="sxs-lookup"><span data-stu-id="508ee-116">The method returns the time of the next pending request.</span></span>

<span data-ttu-id="508ee-117">Para distribuir uma solicitação de aviso, o Agendador sinaliza o evento ou o semáforo fornecido no parâmetro *hNotify* do método [**CAMSchedule:: AddAdvisePacket**](camschedule-addadvisepacket.md) .</span><span class="sxs-lookup"><span data-stu-id="508ee-117">To dispatch an advise request, the scheduler signals the event or semaphore given in the *hNotify* parameter of the [**CAMSchedule::AddAdvisePacket**](camschedule-addadvisepacket.md) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="508ee-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="508ee-118">Requirements</span></span>



| <span data-ttu-id="508ee-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="508ee-119">Requirement</span></span> | <span data-ttu-id="508ee-120">Valor</span><span class="sxs-lookup"><span data-stu-id="508ee-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="508ee-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="508ee-121">Header</span></span><br/>  | <dl> <span data-ttu-id="508ee-122"><dt>Dsschedule. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="508ee-122"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="508ee-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="508ee-123">Library</span></span><br/> | <dl> <span data-ttu-id="508ee-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="508ee-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="508ee-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="508ee-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="508ee-126">**Classe CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="508ee-126">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




