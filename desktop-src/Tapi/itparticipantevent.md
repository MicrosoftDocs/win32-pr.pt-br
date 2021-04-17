---
description: A interface ITParticipantEvent contém métodos que recuperam a descrição dos eventos de participante.
ms.assetid: 1199ec91-ee06-4e6c-8d8f-1585a3da3db0
title: Interface ITParticipantEvent (Confpriv. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2ac6e2b43a528bc041a71962e84b4e1be62152a4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/22/2021
ms.locfileid: "105779463"
---
# <a name="itparticipantevent-interface"></a><span data-ttu-id="94ef5-103">Interface ITParticipantEvent</span><span class="sxs-lookup"><span data-stu-id="94ef5-103">ITParticipantEvent interface</span></span>

<span data-ttu-id="94ef5-104">\[O **ITParticipantEvent** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional.</span><span class="sxs-lookup"><span data-stu-id="94ef5-104">\[**ITParticipantEvent** is not available for use in Windows Vista, Windows Server 2008, and subsequent versions of the operating system.</span></span> <span data-ttu-id="94ef5-105">A API do cliente RTC fornece funcionalidade semelhante.\]</span><span class="sxs-lookup"><span data-stu-id="94ef5-105">The RTC Client API provides similar functionality.\]</span></span>

<span data-ttu-id="94ef5-106">A interface **ITParticipantEvent** contém métodos que recuperam a descrição dos eventos de participante.</span><span class="sxs-lookup"><span data-stu-id="94ef5-106">The **ITParticipantEvent** interface contains methods that retrieve the description of participant events.</span></span> <span data-ttu-id="94ef5-107">Quando a implementação do aplicativo do método [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indica um [**\_ evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) igual a **te \_ Private**, o parâmetro *pEvent* do método é um ponteiro **IDispatch** para a interface **ITParticipantEvent** .</span><span class="sxs-lookup"><span data-stu-id="94ef5-107">When the application's implementation of the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method indicates a [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_PRIVATE**, the method's *pEvent* parameter is an **IDispatch** pointer for the **ITParticipantEvent** interface.</span></span> <span data-ttu-id="94ef5-108">Os métodos dessa interface podem ser usados para recuperar informações relacionadas a uma alteração de participante que ocorreu.</span><span class="sxs-lookup"><span data-stu-id="94ef5-108">The methods of this interface can be used to retrieve information concerning a participant change that has occurred.</span></span>

> [!Note]  
> <span data-ttu-id="94ef5-109">Você deve chamar o método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e definir uma máscara de filtro de eventos que inclua o evento **\_ textprivate** para habilitar a recepção de eventos de participante.</span><span class="sxs-lookup"><span data-stu-id="94ef5-109">You must call the [**ITTAPI::put\_EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) method and set an event filter mask that includes the **TE\_PRIVATE** event to enable reception of participant events.</span></span> <span data-ttu-id="94ef5-110">Se você não chamar **ITTAPI::p UT \_ EventFilter**, seu aplicativo não receberá nenhum evento.</span><span class="sxs-lookup"><span data-stu-id="94ef5-110">If you do not call **ITTAPI::put\_EventFilter**, your application will not receive any events.</span></span> <span data-ttu-id="94ef5-111">Para obter mais informações, consulte a visão geral de [eventos](events.md) .</span><span class="sxs-lookup"><span data-stu-id="94ef5-111">For more information, see the [Events](events.md) overview.</span></span>

 

## <a name="members"></a><span data-ttu-id="94ef5-112">Membros</span><span class="sxs-lookup"><span data-stu-id="94ef5-112">Members</span></span>

<span data-ttu-id="94ef5-113">A interface **ITParticipantEvent** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) .</span><span class="sxs-lookup"><span data-stu-id="94ef5-113">The **ITParticipantEvent** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="94ef5-114">**ITParticipantEvent** também tem estes tipos de membros:</span><span class="sxs-lookup"><span data-stu-id="94ef5-114">**ITParticipantEvent** also has these types of members:</span></span>

-   [<span data-ttu-id="94ef5-115">Métodos</span><span class="sxs-lookup"><span data-stu-id="94ef5-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="94ef5-116">Métodos</span><span class="sxs-lookup"><span data-stu-id="94ef5-116">Methods</span></span>

<span data-ttu-id="94ef5-117">A interface **ITParticipantEvent** tem esses métodos.</span><span class="sxs-lookup"><span data-stu-id="94ef5-117">The **ITParticipantEvent** interface has these methods.</span></span>



| <span data-ttu-id="94ef5-118">Método</span><span class="sxs-lookup"><span data-stu-id="94ef5-118">Method</span></span>                                                         | <span data-ttu-id="94ef5-119">Descrição</span><span class="sxs-lookup"><span data-stu-id="94ef5-119">Description</span></span>                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="94ef5-120">**obter \_ evento**</span><span class="sxs-lookup"><span data-stu-id="94ef5-120">**get\_Event**</span></span>](itparticipantevent-get-event.md)             | <span data-ttu-id="94ef5-121">Obtém o descritor de [**\_ evento do participante**](participant-event.md) do evento.</span><span class="sxs-lookup"><span data-stu-id="94ef5-121">Gets the [**PARTICIPANT\_EVENT**](participant-event.md) descriptor of the event.</span></span><br/>                                                    |
| [<span data-ttu-id="94ef5-122">**obter \_ participante**</span><span class="sxs-lookup"><span data-stu-id="94ef5-122">**get\_Participant**</span></span>](itparticipantevent-get-participant.md) | <span data-ttu-id="94ef5-123">Obtém um ponteiro para uma matriz de interfaces [**ITParticipant**](itparticipant.md) que representam os participantes envolvidos no evento.</span><span class="sxs-lookup"><span data-stu-id="94ef5-123">Gets a pointer to an array of [**ITParticipant**](itparticipant.md) interfaces representing the participants involved in the event.</span></span><br/> |
| [<span data-ttu-id="94ef5-124">**obter \_ Subfluxo**</span><span class="sxs-lookup"><span data-stu-id="94ef5-124">**get\_SubStream**</span></span>](itparticipantevent-get-substream.md)     | <span data-ttu-id="94ef5-125">Obtém um ponteiro para uma matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representam os subfluxos envolvidos no evento.</span><span class="sxs-lookup"><span data-stu-id="94ef5-125">Gets a pointer to an array of [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) interfaces representing the substreams involved in the event.</span></span><br/>       |



 

## <a name="requirements"></a><span data-ttu-id="94ef5-126">Requisitos</span><span class="sxs-lookup"><span data-stu-id="94ef5-126">Requirements</span></span>



| <span data-ttu-id="94ef5-127">Requisito</span><span class="sxs-lookup"><span data-stu-id="94ef5-127">Requirement</span></span> | <span data-ttu-id="94ef5-128">Valor</span><span class="sxs-lookup"><span data-stu-id="94ef5-128">Value</span></span> |
|-------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="94ef5-129">Versão da TAPI</span><span class="sxs-lookup"><span data-stu-id="94ef5-129">TAPI version</span></span><br/> | <span data-ttu-id="94ef5-130">Requer TAPI 3,0 ou posterior</span><span class="sxs-lookup"><span data-stu-id="94ef5-130">Requires TAPI 3.0 or later</span></span><br/>                                                 |
| <span data-ttu-id="94ef5-131">parâmetro</span><span class="sxs-lookup"><span data-stu-id="94ef5-131">Header</span></span><br/>       | <dl> <span data-ttu-id="94ef5-132"><dt>Confpriv. h</dt></span><span class="sxs-lookup"><span data-stu-id="94ef5-132"><dt>Confpriv.h</dt></span></span> </dl> |
| <span data-ttu-id="94ef5-133">Biblioteca</span><span class="sxs-lookup"><span data-stu-id="94ef5-133">Library</span></span><br/>      | <dl> <span data-ttu-id="94ef5-134"><dt>UUID. lib</dt></span><span class="sxs-lookup"><span data-stu-id="94ef5-134"><dt>Uuid.lib</dt></span></span> </dl>   |
| <span data-ttu-id="94ef5-135">DLL</span><span class="sxs-lookup"><span data-stu-id="94ef5-135">DLL</span></span><br/>          | <dl> <span data-ttu-id="94ef5-136"><dt>Tapi3.dll</dt></span><span class="sxs-lookup"><span data-stu-id="94ef5-136"><dt>Tapi3.dll</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="94ef5-137">Confira também</span><span class="sxs-lookup"><span data-stu-id="94ef5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94ef5-138">**ITParticipant**</span><span class="sxs-lookup"><span data-stu-id="94ef5-138">**ITParticipant**</span></span>](itparticipant.md)
</dt> <dt>

[<span data-ttu-id="94ef5-139">**ITSubStream**</span><span class="sxs-lookup"><span data-stu-id="94ef5-139">**ITSubStream**</span></span>](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[<span data-ttu-id="94ef5-140">**ITCallInfo**</span><span class="sxs-lookup"><span data-stu-id="94ef5-140">**ITCallInfo**</span></span>](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[<span data-ttu-id="94ef5-141">**evento de participante \_**</span><span class="sxs-lookup"><span data-stu-id="94ef5-141">**PARTICIPANT\_EVENT**</span></span>](participant-event.md)
</dt> <dt>

[<span data-ttu-id="94ef5-142">**Evento ITTAPIEventNotification::**</span><span class="sxs-lookup"><span data-stu-id="94ef5-142">**ITTAPIEventNotification::Event**</span></span>](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[<span data-ttu-id="94ef5-143">**\_evento TAPI**</span><span class="sxs-lookup"><span data-stu-id="94ef5-143">**TAPI\_EVENT**</span></span>](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[<span data-ttu-id="94ef5-144">Trecho de código de registro de eventos</span><span class="sxs-lookup"><span data-stu-id="94ef5-144">Register Events code snippet</span></span>](register-events.md)
</dt> </dl>

 

