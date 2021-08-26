---
description: Evento por usuário gerado por um cliente de email quando uma recepção de mensagem é tentada em Controles Dos Pais.
ms.assetid: 3b8d9bac-16b0-49e9-b360-b2d6e82f1753
title: WPCEVENT_EMAIL_RECEIVED evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a81a51e79125403504aae2ed6e823c10044ffc35ed36ff139e8333f955338d81
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951556"
---
# <a name="wpcevent_email_received-event"></a>Evento WPCEVENT \_ EMAIL \_ RECEIVED

Evento por usuário gerado por um cliente de email quando uma recepção de mensagem é tentada em Controles Dos Pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_RECEIVED = {0x4, 0x0, 0x10, 0x4, 0x16, 0x4, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Remetente* 
</dt> <dd>

O nome da conta de email da entidade de envio.

</dd> <dt>

*AppName* 
</dt> <dd>

O nome do aplicativo de email que está gerando o evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

A versão do aplicativo de email que está gerando o evento.

</dd> <dt>

*Assunto* 
</dt> <dd>

A linha de assunto da mensagem recebida.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da [**enumeração \_ ISBLOCKED WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são impedidos de usar e quais controles estão em uso.

</dd> <dt>

*RecipCount* 
</dt> <dd>

A contagem de endereços de email que estão recebendo a mensagem e que têm identidades definidas no campo destinatário.

</dd> <dt>

*Destinatário* 
</dt> <dd>

Uma cadeia de caracteres delimitada que contém os nomes de conta de email de todos os destinatários da mensagem.

</dd> <dt>

*AttachCount* 
</dt> <dd>

A contagem de anexos para a mensagem.

</dd> <dt>

*AttachmentName* 
</dt> <dd>

Uma cadeia de caracteres delimitada que contém os nomes de todos os anexos à mensagem.

</dd> <dt>

*ReceivedTime* 
</dt> <dd>

A hora em que a mensagem foi tentada para ser recebida.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

O nome da conta de email para esse usuário.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho do Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Cabeçalho<br/>                   | <dl> <dt>Wpcevent.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando APIs de log para controles dos pais](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ ARGS \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




