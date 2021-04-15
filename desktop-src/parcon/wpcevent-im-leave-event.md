---
description: Evento por usuário gerado por um cliente de mensagens instantâneas quando um usuário deixa uma conversa em controles dos pais.
ms.assetid: e6bd6bce-9eba-4192-aac8-c9e47d7180a1
title: WPCEVENT_IM_LEAVE evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 260833a30f08330da9c622faae06f76b5d79e682
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105761643"
---
# <a name="wpcevent_im_leave-event"></a>Evento de saída do WPCEVENT \_ im \_

Evento por usuário gerado por um cliente de mensagens instantâneas quando um usuário deixa uma conversa em controles dos pais.


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

A cadeia de caracteres da versão do aplicativo que está gerando o evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

A cadeia de caracteres de identidade da conta de mensagens instantâneas para este usuário.

</dd> <dt>

*Convid* 
</dt> <dd>

O identificador desta conversa.

</dd> <dt>

*LeavingIP* 
</dt> <dd>

Uma cadeia de caracteres que contém o endereço IP do computador que está saindo desta conversa.

</dd> <dt>

*LeavingUser* 
</dt> <dd>

A cadeia de caracteres de identidade da conta de mensagens instantâneas para o usuário que está saindo.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

</dd> <dt>

*MemberCount* 
</dt> <dd>

A contagem de participantes que estão na conversa e que têm identidades definidas no campo membro.

</dd> <dt>

*Membro* 
</dt> <dd>

Uma cadeia delimitada que contém cadeias de caracteres de identidade da conta de mensagens instantâneas para todos os membros atuais desta conversa.

</dd> <dt>

*Sinalizadores* 
</dt> <dd>

Um valor da enumeração [**de \_ \_ saída do WPCFLAG im**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_leave) que indica informações sobre quando um participante deixa a interação de mensagens instantâneas.

</dd> </dl>

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | \[Somente aplicativos da área de trabalho do Windows Vista\]<br/>                                        |
| Servidor mínimo com suporte<br/> | Nenhum compatível<br/>                                                             |
| parâmetro<br/>                   | <dl> <dt>Wpcevent. h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Usando APIs de log para controles dos pais](using-logging-apis-for-parental-controls.md)
</dt> <dt>

[**WPC \_ args \_ CONVERSATIONINITEVENT**](/windows/win32/api/wpcevent/ne-wpcevent-wpc_args_conversationinitevent)
</dt> </dl>

 

 




