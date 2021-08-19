---
description: Evento por usuário gerado por um cliente de Mensagens Instantâneas quando um usuário deixa uma conversa em Controles Dos Pais.
ms.assetid: e6bd6bce-9eba-4192-aac8-c9e47d7180a1
title: WPCEVENT_IM_LEAVE evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f6d814f6c9d4e3ec5acd3ee3cf3a6eb6e67d315148304f2766baf45fc633fa22
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951206"
---
# <a name="wpcevent_im_leave-event"></a>Evento WPCEVENT \_ IM \_ LEAVE

Evento por usuário gerado por um cliente de Mensagens Instantâneas quando um usuário deixa uma conversa em Controles Dos Pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_LEAVE = {0x9, 0x0, 0x10, 0x4, 0x16, 0x9, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AppName* 
</dt> <dd>

O nome do aplicativo que está gerando o evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

A cadeia de caracteres de versão do aplicativo que está gerando o evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

A cadeia de caracteres de identidade da conta de mensagens instantânea para esse usuário.

</dd> <dt>

*ConvID* 
</dt> <dd>

O identificador dessa conversa.

</dd> <dt>

*LeavingIP* 
</dt> <dd>

Uma cadeia de caracteres que contém o endereço IP do computador que está deixando essa conversa.

</dd> <dt>

*LeavingUser* 
</dt> <dd>

A cadeia de caracteres de identidade da conta de mensagens instantânea para o usuário que está saindo.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da [**enumeração \_ ISBLOCKED WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são impedidos de usar e quais controles estão em uso.

</dd> <dt>

*Membercount* 
</dt> <dd>

A contagem de participantes que estão na conversa e que têm identidades definidas no campo membro.

</dd> <dt>

*Membro* 
</dt> <dd>

Uma cadeia de caracteres delimitada que contém cadeias de caracteres de identidade da conta de mensagens instantâneas para todos os membros atuais desta conversa.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Um valor da [**enumeração WPCFLAG \_ IM \_ LEAVE**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_leave) que indica informações sobre quando um participante sai da interação instantânea de mensagens.

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

 

 




