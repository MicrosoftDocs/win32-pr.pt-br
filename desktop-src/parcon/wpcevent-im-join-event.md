---
description: Evento por usuário gerado por um aplicativo de mensagens instantâneas quando uma entidade tenta ingressar em uma conversa em andamento em controles dos pais.
ms.assetid: 5251234b-0280-4d5d-80f5-295d720a89d1
title: WPCEVENT_IM_JOIN evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 181bc849cf89e8a78a7a5aaad97463baf0c611d99ca0dc05caf9bfaf879eb804
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951286"
---
# <a name="wpcevent_im_join-event"></a>Evento de junção de \_ im WPCEVENT \_

Evento por usuário gerado por um aplicativo de mensagens instantâneas quando uma entidade tenta ingressar em uma conversa em andamento em controles dos pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_JOIN = {0x8, 0x0, 0x10, 0x4, 0x16, 0x8, 0x8000000000000030};
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

*JoiningIP* 
</dt> <dd>

Uma cadeia de caracteres que contém o endereço IP do computador que está ingressando nesta conversa.

</dd> <dt>

*JoiningUser* 
</dt> <dd>

A cadeia de caracteres de identidade da conta de mensagens instantâneas para o usuário que está ingressando.

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

*Remetente* 
</dt> <dd>

A cadeia de caracteres de identidade da conta de mensagens instantâneas para o usuário que está fazendo a solicitação para ingressar na conversa.

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

 

 




