---
description: O \_ método Get Event obtém um \_ descritor de evento participante do tipo de evento que ocorreu.
ms.assetid: 6b5e6358-2ba6-48b5-8d55-bc896fbb9962
title: 'Método ITParticipantEvent:: get_Event (Confpriv. h)'
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9b6cbfcf709b1f9f3f49047504bf5d9e8c02b159
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779308"
---
# <a name="itparticipanteventget_event-method"></a><span data-ttu-id="b3e91-103">Método de evento ITParticipantEvent:: get \_</span><span class="sxs-lookup"><span data-stu-id="b3e91-103">ITParticipantEvent::get\_Event method</span></span>

<span data-ttu-id="b3e91-104">\[**obter \_ O evento** não está disponível para uso no Windows Vista, no Windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="b3e91-104">\[**get\_Event** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="b3e91-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="b3e91-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="b3e91-106">O método **Get \_ Event** Obtém um descritor de [**\_ evento participante**](participant-event.md) do tipo de evento que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="b3e91-106">The **get\_Event** method gets a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the type of event that has occurred.</span></span>

## <a name="syntax"></a><span data-ttu-id="b3e91-107">Sintaxe</span><span class="sxs-lookup"><span data-stu-id="b3e91-107">Syntax</span></span>


```C++
HRESULT get_Event(
  [out] PARTICIPANT_EVENT *pParticipantEvent
);
```



## <a name="parameters"></a><span data-ttu-id="b3e91-108">Parâmetros</span><span class="sxs-lookup"><span data-stu-id="b3e91-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b3e91-109">*pParticipantEvent* \[ fora\]</span><span class="sxs-lookup"><span data-stu-id="b3e91-109">*pParticipantEvent* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b3e91-110">Ponteiro para um descritor de [**\_ evento de participante**](participant-event.md) do evento.</span><span class="sxs-lookup"><span data-stu-id="b3e91-110">Pointer to a [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b3e91-111">Retornar valor</span><span class="sxs-lookup"><span data-stu-id="b3e91-111">Return value</span></span>

<span data-ttu-id="b3e91-112">Esse método pode retornar um desses valores.</span><span class="sxs-lookup"><span data-stu-id="b3e91-112">This method can return one of these values.</span></span>



| <span data-ttu-id="b3e91-113">Valor</span><span class="sxs-lookup"><span data-stu-id="b3e91-113">Value</span></span>                                                                                         | <span data-ttu-id="b3e91-114">Significado</span><span class="sxs-lookup"><span data-stu-id="b3e91-114">Meaning</span></span>                                                              |
|-----------------------------------------------------------------------------------------------|----------------------------------------------------------------------|
| <dl> <span data-ttu-id="b3e91-115"><dt>**S \_ OK**</dt></span><span class="sxs-lookup"><span data-stu-id="b3e91-115"><dt>**S\_OK**</dt></span></span> </dl>          | <span data-ttu-id="b3e91-116">O método foi bem-sucedido.</span><span class="sxs-lookup"><span data-stu-id="b3e91-116">Method succeeded.</span></span><br/>                                         |
| <dl> <span data-ttu-id="b3e91-117"><dt>**E \_ OUTOFMEMORY**</dt></span><span class="sxs-lookup"><span data-stu-id="b3e91-117"><dt>**E\_OUTOFMEMORY**</dt></span></span> </dl> | <span data-ttu-id="b3e91-118">Há memória insuficiente para executar a operação.</span><span class="sxs-lookup"><span data-stu-id="b3e91-118">Insufficient memory exists to perform the operation.</span></span><br/>      |
| <dl> <span data-ttu-id="b3e91-119"><dt>**\_ponteiro E**</dt></span><span class="sxs-lookup"><span data-stu-id="b3e91-119"><dt>**E\_POINTER**</dt></span></span> </dl>     | <span data-ttu-id="b3e91-120">O parâmetro *pParticipantEvent* não é um ponteiro válido.</span><span class="sxs-lookup"><span data-stu-id="b3e91-120">The *pParticipantEvent* parameter is not a valid pointer.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="b3e91-121">Requisitos</span><span class="sxs-lookup"><span data-stu-id="b3e91-121">Requirements</span></span>



| <span data-ttu-id="b3e91-122">Requisito</span><span class="sxs-lookup"><span data-stu-id="b3e91-122">Requirement</span></span> | <span data-ttu-id="b3e91-123">Valor</span><span class="sxs-lookup"><span data-stu-id="b3e91-123">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="b3e91-124">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="b3e91-124">TAPI version</span></span><br/> | <span data-ttu-id="b3e91-125">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="b3e91-125">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="b3e91-126">parâmetro</span><span class="sxs-lookup"><span data-stu-id="b3e91-126">Header</span></span><br/>       | <dl> <span data-ttu-id="b3e91-127"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="b3e91-127"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="b3e91-128">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="b3e91-128">Library</span></span><br/>      | <dl> <span data-ttu-id="b3e91-129"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="b3e91-129"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="b3e91-130">DLL</span><span class="sxs-lookup"><span data-stu-id="b3e91-130">DLL</span></span><br/>          | <dl> <span data-ttu-id="b3e91-131"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="b3e91-131"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b3e91-132">Confira também</span><span class="sxs-lookup"><span data-stu-id="b3e91-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b3e91-133">**ITParticipantEvent**</span><span class="sxs-lookup"><span data-stu-id="b3e91-133">**ITParticipantEvent**</span></span>](itparticipantevent.md)
</dt> <dt>

[<span data-ttu-id="b3e91-134">**evento de participante \_**</span><span class="sxs-lookup"><span data-stu-id="b3e91-134">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> </dl>

 

 




