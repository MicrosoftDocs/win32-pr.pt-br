---
description: Evento por usuário fornecido para o log de inicialização de conversas por clientes de mensagens instantâneas.
ms.assetid: b2cd1d37-9993-4990-83b7-b147a109e4af
title: WPCEVENT_IM_INVITATION evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f29b1adc556e29e03f7c8a189567b98055187f80d1574e201c54e3af0c1c0aca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951386"
---
# <a name="wpcevent_im_invitation-event"></a>Evento de convite do WPCEVENT \_ im \_

Evento por usuário fornecido para o log de inicialização de conversas por clientes de mensagens instantâneas.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_INVITATION = {0x7, 0x0, 0x10, 0x4, 0x16, 0x7, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AppName* 
</dt> <dd>

O nome do aplicativo que está gerando o evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

A cadeia de caracteres da versão do aplicativo que está gerando o evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

A cadeia de caracteres de identidade da conta de mensagens instantâneas.

</dd> <dt>

*Convid* 
</dt> <dd>

O identificador da conversa.

</dd> <dt>

*RequestingIP* 
</dt> <dd>

Uma cadeia de caracteres que contém o endereço IP do computador que está enviando o convite.

</dd> <dt>

*Remetente* 
</dt> <dd>

A cadeia de caracteres de identidade da conta de mensagens instantâneas para a conta que está emitindo o convite.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

</dd> <dt>

*RecipCount* 
</dt> <dd>

A contagem de destinatários que estão recebendo o convite e que têm identidades definidas no campo destinatário.

</dd> <dt>

*Destinatário* 
</dt> <dd>

Uma cadeia delimitada que contém cadeias de caracteres de identidade da conta de mensagens instantâneas para os destinatários do convite.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows \[Somente aplicativos da área de trabalho do vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| Cabeçalho<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando APIs de log para controles dos pais](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




