---
description: O método GetEvent recupera um identificador de evento, que é usado para sinalizar uma alteração no próximo horário de aviso.
ms.assetid: 2548a321-df65-4a5b-9e6a-8bbc031254c7
title: Método CAMSchedule. GetEvent (Dsschedule. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMSchedule.GetEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 360a4b88c8c03d2f04ad55bc65eebf6be3797c92
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105752312"
---
# <a name="camschedulegetevent-method"></a><span data-ttu-id="fe4db-103">Método CAMSchedule. GetEvent</span><span class="sxs-lookup"><span data-stu-id="fe4db-103">CAMSchedule.GetEvent method</span></span>

<span data-ttu-id="fe4db-104">O `GetEvent` método recupera um identificador de evento, que é usado para sinalizar uma alteração no próximo horário de aviso.</span><span class="sxs-lookup"><span data-stu-id="fe4db-104">The `GetEvent` method retrieves an event handle, which is used to signal a change in the next advise time.</span></span>

## <a name="syntax"></a><span data-ttu-id="fe4db-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="fe4db-105">Syntax</span></span>


```C++
HANDLE GetEvent();
```



## <a name="parameters"></a><span data-ttu-id="fe4db-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="fe4db-106">Parameters</span></span>

<span data-ttu-id="fe4db-107">Esse método não tem parâmetros.</span><span class="sxs-lookup"><span data-stu-id="fe4db-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="fe4db-108">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="fe4db-108">Return value</span></span>

<span data-ttu-id="fe4db-109">Retorna um identificador para um evento.</span><span class="sxs-lookup"><span data-stu-id="fe4db-109">Returns a handle to an event.</span></span>

## <a name="remarks"></a><span data-ttu-id="fe4db-110">Comentários</span><span class="sxs-lookup"><span data-stu-id="fe4db-110">Remarks</span></span>

<span data-ttu-id="fe4db-111">Se a próxima hora do aviso for alterada em outras palavras, se uma nova solicitação de aviso for adicionada à frente da lista, o Agendador sinalizará esse evento.</span><span class="sxs-lookup"><span data-stu-id="fe4db-111">If the next advise time changes in other words, if a new advise request is added to the front of the list the scheduler signals this event.</span></span> <span data-ttu-id="fe4db-112">O relógio deve chamar o método [**CAMSchedule:: Advise**](camschedule-advise.md) para determinar o próximo horário de aviso.</span><span class="sxs-lookup"><span data-stu-id="fe4db-112">The clock should call the [**CAMSchedule::Advise**](camschedule-advise.md) method to determine the next advise time.</span></span>

## <a name="requirements"></a><span data-ttu-id="fe4db-113">Requisitos</span><span class="sxs-lookup"><span data-stu-id="fe4db-113">Requirements</span></span>



| <span data-ttu-id="fe4db-114">Requisito</span><span class="sxs-lookup"><span data-stu-id="fe4db-114">Requirement</span></span> | <span data-ttu-id="fe4db-115">Valor</span><span class="sxs-lookup"><span data-stu-id="fe4db-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fe4db-116">parâmetro</span><span class="sxs-lookup"><span data-stu-id="fe4db-116">Header</span></span><br/>  | <dl> <span data-ttu-id="fe4db-117"><dt>Dsschedule. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="fe4db-117"><dt>Dsschedule.h (include Streams.h)</dt></span></span> </dl>                                                                                |
| <span data-ttu-id="fe4db-118">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="fe4db-118">Library</span></span><br/> | <dl> <span data-ttu-id="fe4db-119"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="fe4db-119"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="fe4db-120">Confira também</span><span class="sxs-lookup"><span data-stu-id="fe4db-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fe4db-121">**Classe CAMSchedule**</span><span class="sxs-lookup"><span data-stu-id="fe4db-121">**CAMSchedule Class**</span></span>](camschedule.md)
</dt> </dl>

 

 




