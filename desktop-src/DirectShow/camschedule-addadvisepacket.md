---
description: O método AddAdvisePacket adiciona uma solicitação de aviso à lista de solicitações pendentes.
ms.assetid: 138d8404-7d28-47cc-91b4-4733a113ac7a
title: Método CAMSchedule. AddAdvisePacket (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.AddAdvisePacket
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 5dd9586b09586c12f1a30f45b512336831372295
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105780445"
---
# <a name="camscheduleaddadvisepacket-method"></a><span data-ttu-id="b93f6-103">Método CAMSchedule. AddAdvisePacket</span><span class="sxs-lookup"><span data-stu-id="b93f6-103">CAMSchedule.AddAdvisePacket method</span></span>

<span data-ttu-id="b93f6-104">O `AddAdvisePacket` método adiciona uma solicitação de aviso à lista de solicitações pendentes.</span><span class="sxs-lookup"><span data-stu-id="b93f6-104">The `AddAdvisePacket` method adds an advise request to the list of pending requests.</span></span>

## <a name="syntax"></a><span data-ttu-id="b93f6-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b93f6-105">Syntax</span></span>


```C++
DWORD_PTR AddAdvisePacket(
  [ref] const REFERENCE_TIME &time1,
  [ref] const REFERENCE_TIME &time2,
              HANDLE         hNotify,
              BOOL           bPeriodic
);
```



## <a name="parameters"></a><span data-ttu-id="b93f6-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b93f6-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b93f6-107">*time1* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="b93f6-107">*time1* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b93f6-108">Hora solicitada para o aviso.</span><span class="sxs-lookup"><span data-stu-id="b93f6-108">Requested time for the advise.</span></span>

</dd> <dt>

<span data-ttu-id="b93f6-109">*time2* \[ referência\]</span><span class="sxs-lookup"><span data-stu-id="b93f6-109">*time2* \[ref\]</span></span>
</dt> <dd>

<span data-ttu-id="b93f6-110">Para solicitações de aviso periódicas, o tempo entre as notificações.</span><span class="sxs-lookup"><span data-stu-id="b93f6-110">For periodic advise requests, the time between notifications.</span></span> <span data-ttu-id="b93f6-111">Esse parâmetro será ignorado se *bPeriodic* for **false**.</span><span class="sxs-lookup"><span data-stu-id="b93f6-111">This parameter is ignored if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b93f6-112">*hNotify*</span><span class="sxs-lookup"><span data-stu-id="b93f6-112">*hNotify*</span></span> 
</dt> <dd>

<span data-ttu-id="b93f6-113">Manipule um semáforo se *bPeriodic* for **verdadeiro** ou manipule um evento se *bPeriodic* for **false**.</span><span class="sxs-lookup"><span data-stu-id="b93f6-113">Handle to a semaphore if *bPeriodic* is **TRUE**, or handle to an event if *bPeriodic* is **FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="b93f6-114">*bPeriodic*</span><span class="sxs-lookup"><span data-stu-id="b93f6-114">*bPeriodic*</span></span> 
</dt> <dd>

<span data-ttu-id="b93f6-115">Valor booliano que especifica se uma notificação periódica ou uma notificação de uma imagem deve ser adicionada.</span><span class="sxs-lookup"><span data-stu-id="b93f6-115">Boolean value that specifies whether to add a periodic notification or a one-shot notification.</span></span> <span data-ttu-id="b93f6-116">Se for **true**, a notificação será periódica; o parâmetro *time2* especifica o tempo entre as notificações.</span><span class="sxs-lookup"><span data-stu-id="b93f6-116">If **TRUE**, the notification is periodic; the *time2* parameter specifies the time between notifications.</span></span> <span data-ttu-id="b93f6-117">Se **for false**, a notificação ocorrerá apenas uma vez.</span><span class="sxs-lookup"><span data-stu-id="b93f6-117">If **FALSE**, the notification occurs only once.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b93f6-118">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b93f6-118">Return value</span></span>

<span data-ttu-id="b93f6-119">Retorna um identificador para a solicitação de aviso (o "cookie").</span><span class="sxs-lookup"><span data-stu-id="b93f6-119">Returns an identifier for the advise request (the "cookie").</span></span> <span data-ttu-id="b93f6-120">Se o método falhar, o valor de retorno será zero.</span><span class="sxs-lookup"><span data-stu-id="b93f6-120">If the method fails, the return value is zero.</span></span>

## <a name="requirements"></a><span data-ttu-id="b93f6-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b93f6-121">Requirements</span></span>



| <span data-ttu-id="b93f6-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b93f6-122">Requirement</span></span> | <span data-ttu-id="b93f6-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b93f6-123">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="b93f6-124">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b93f6-124">Header</span></span><br/>  | <dl> <span data-ttu-id="b93f6-125"><dt>Dsschedule. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="b93f6-125"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="b93f6-126">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b93f6-126">Library</span></span><br/> | <dl> <span data-ttu-id="b93f6-127"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="b93f6-127"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="b93f6-128">Confira também</span><span class="sxs-lookup"><span data-stu-id="b93f6-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b93f6-129">**Classe CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="b93f6-129">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




