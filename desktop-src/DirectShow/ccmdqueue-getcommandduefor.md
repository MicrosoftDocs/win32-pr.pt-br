---
description: O método GetCommandDueFor recupera um comando adiado que é agendado em um horário especificado.
ms.assetid: f8a2f9ae-f359-4429-aca5-021b6fe2aa93
title: Método CCmdQueue. GetCommandDueFor (Winutil. h)
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCmdQueue.GetCommandDueFor
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 48a01436a68a5b98d08880c1516bbf4576d10be2
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105785369"
---
# <a name="ccmdqueuegetcommandduefor-method"></a><span data-ttu-id="cfbe8-103">Método CCmdQueue. GetCommandDueFor</span><span class="sxs-lookup"><span data-stu-id="cfbe8-103">CCmdQueue.GetCommandDueFor method</span></span>

<span data-ttu-id="cfbe8-104">O `GetCommandDueFor` método recupera um comando adiado que é agendado em um horário especificado.</span><span class="sxs-lookup"><span data-stu-id="cfbe8-104">The `GetCommandDueFor` method retrieves a deferred command that is scheduled at a specified time.</span></span>

## <a name="syntax"></a><span data-ttu-id="cfbe8-105">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="cfbe8-105">Syntax</span></span>


```C++
virtual HRESULT GetCommandDueFor(
   REFERENCE_TIME   tStream,
   CDeferredCommand **ppCmd
);
```



## <a name="parameters"></a><span data-ttu-id="cfbe8-106">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="cfbe8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="cfbe8-107">*tStream*</span><span class="sxs-lookup"><span data-stu-id="cfbe8-107">*tStream*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbe8-108">Hora em que o comando está agendado.</span><span class="sxs-lookup"><span data-stu-id="cfbe8-108">Time for which the command is scheduled.</span></span>

</dd> <dt>

<span data-ttu-id="cfbe8-109">*ppCmd*</span><span class="sxs-lookup"><span data-stu-id="cfbe8-109">*ppCmd*</span></span> 
</dt> <dd>

<span data-ttu-id="cfbe8-110">Endereço de um ponteiro para o comando adiado a ser executado no momento especificado no parâmetro *tStream* .</span><span class="sxs-lookup"><span data-stu-id="cfbe8-110">Address of a pointer to the deferred command to be carried out at the time specified in the *tStream* parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="cfbe8-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="cfbe8-111">Return value</span></span>

<span data-ttu-id="cfbe8-112">Retorna VFW \_ E \_ não \_ encontrado se nenhum comando for devido; caso contrário, retornará S \_ OK.</span><span class="sxs-lookup"><span data-stu-id="cfbe8-112">Returns VFW\_E\_NOT\_FOUND if no commands are due; otherwise, returns S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="cfbe8-113">Comentários</span><span class="sxs-lookup"><span data-stu-id="cfbe8-113">Remarks</span></span>

<span data-ttu-id="cfbe8-114">Essa função de membro usa um fluxo de tempo e retorna o comando adiado agendado nesse momento.</span><span class="sxs-lookup"><span data-stu-id="cfbe8-114">This member function takes a stream time and returns the deferred command scheduled at that time.</span></span> <span data-ttu-id="cfbe8-115">O deslocamento real do tempo de transmissão é calculado quando a fila de comandos é executada.</span><span class="sxs-lookup"><span data-stu-id="cfbe8-115">The actual stream-time offset is calculated when the command queue is run.</span></span> <span data-ttu-id="cfbe8-116">Os comandos permanecem na fila até serem executados ou cancelados.</span><span class="sxs-lookup"><span data-stu-id="cfbe8-116">Commands remain queued until run or canceled.</span></span> <span data-ttu-id="cfbe8-117">Esta função de membro não será bloqueada.</span><span class="sxs-lookup"><span data-stu-id="cfbe8-117">This member function will not block.</span></span>

## <a name="requirements"></a><span data-ttu-id="cfbe8-118">Requisitos</span><span class="sxs-lookup"><span data-stu-id="cfbe8-118">Requirements</span></span>



| <span data-ttu-id="cfbe8-119">Requisito</span><span class="sxs-lookup"><span data-stu-id="cfbe8-119">Requirement</span></span> | <span data-ttu-id="cfbe8-120">Valor</span><span class="sxs-lookup"><span data-stu-id="cfbe8-120">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cfbe8-121">parâmetro</span><span class="sxs-lookup"><span data-stu-id="cfbe8-121">Header</span></span><br/>  | <dl> <span data-ttu-id="cfbe8-122"><dt>Winutil. h (incluir fluxos. h)</dt></span><span class="sxs-lookup"><span data-stu-id="cfbe8-122"><dt>Winutil.h (include Streams.h)</dt></span></span> </dl>                                                                                   |
| <span data-ttu-id="cfbe8-123">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="cfbe8-123">Library</span></span><br/> | <dl> <span data-ttu-id="cfbe8-124"><dt>Strmbase. lib (compilações de varejo); </dt> <dt>Strmbasd. lib (compilações de depuração)</dt></span><span class="sxs-lookup"><span data-stu-id="cfbe8-124"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfbe8-125">Confira também</span><span class="sxs-lookup"><span data-stu-id="cfbe8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfbe8-126">**Classe CCmdQueue**</span><span class="sxs-lookup"><span data-stu-id="cfbe8-126">**CCmdQueue Class**</span></span>](ccmdqueue.md)
</dt> </dl>

 

 




