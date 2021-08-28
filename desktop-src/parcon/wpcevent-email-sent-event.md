---
description: Evento por usuário gerado por um cliente de email quando uma mensagem é tentada para ser enviada em Controles Dos Pais.
ms.assetid: c49919a2-2a03-475d-9cfa-20a960184202
title: WPCEVENT_EMAIL_SENT evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bfe3d5fb08764aa83677fcca66af7f1e3b868f2b1bdf393741865bf64fd23049
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112726"
---
# <a name="wpcevent_email_sent-event"></a>Evento WPCEVENT \_ EMAIL \_ SENT

Evento por usuário gerado por um cliente de email quando uma mensagem é tentada para ser enviada em Controles Dos Pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_SENT = {0x5, 0x0, 0x10, 0x4, 0x16, 0x5, 0x8000000000000030};
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

 

 




