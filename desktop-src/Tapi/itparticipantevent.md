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
# <a name="itparticipantevent-interface"></a>Interface ITParticipantEvent

\[O **ITParticipantEvent** não está disponível para uso no Windows Vista, no windows Server 2008 e em versões subsequentes do sistema operacional. A API do cliente RTC fornece funcionalidade semelhante.\]

A interface **ITParticipantEvent** contém métodos que recuperam a descrição dos eventos de participante. Quando a implementação do aplicativo do método [**ITTAPIEventNotification:: Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) indica um [**\_ evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) igual a **te \_ Private**, o parâmetro *pEvent* do método é um ponteiro **IDispatch** para a interface **ITParticipantEvent** . Os métodos dessa interface podem ser usados para recuperar informações relacionadas a uma alteração de participante que ocorreu.

> [!Note]  
> Você deve chamar o método [**ITTAPI::p UT \_ EventFilter**](/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-put_eventfilter) e definir uma máscara de filtro de eventos que inclua o evento **\_ textprivate** para habilitar a recepção de eventos de participante. Se você não chamar **ITTAPI::p UT \_ EventFilter**, seu aplicativo não receberá nenhum evento. Para obter mais informações, consulte a visão geral de [eventos](events.md) .

 

## <a name="members"></a>Membros

A interface **ITParticipantEvent** herda da interface [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) . **ITParticipantEvent** também tem estes tipos de membros:

-   [Métodos](#methods)

### <a name="methods"></a>Métodos

A interface **ITParticipantEvent** tem esses métodos.



| Método                                                         | Descrição                                                                                                                                     |
|:---------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------------------------------|
| [**obter \_ evento**](itparticipantevent-get-event.md)             | Obtém o descritor de [**\_ evento do participante**](participant-event.md) do evento.<br/>                                                    |
| [**obter \_ participante**](itparticipantevent-get-participant.md) | Obtém um ponteiro para uma matriz de interfaces [**ITParticipant**](itparticipant.md) que representam os participantes envolvidos no evento.<br/> |
| [**obter \_ Subfluxo**](itparticipantevent-get-substream.md)     | Obtém um ponteiro para uma matriz de interfaces [**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream) que representam os subfluxos envolvidos no evento.<br/>       |



 

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------|---------------------------------------------------------------------------------------|
| Versão da TAPI<br/> | Requer TAPI 3,0 ou posterior<br/>                                                 |
| parâmetro<br/>       | <dl> <dt>Confpriv. h</dt> </dl> |
| Biblioteca<br/>      | <dl> <dt>UUID. lib</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl>  |



## <a name="see-also"></a>Confira também

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITSubStream**](/windows/win32/api/tapi3if/nn-tapi3if-itsubstream)
</dt> <dt>

[**ITCallInfo**](/windows/desktop/api/tapi3if/nn-tapi3if-itcallinfo)
</dt> <dt>

[**evento de participante \_**](participant-event.md)
</dt> <dt>

[**Evento ITTAPIEventNotification::**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event)
</dt> <dt>

[**\_evento TAPI**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event)
</dt> <dt>

[Trecho de código de registro de eventos](register-events.md)
</dt> </dl>

 

