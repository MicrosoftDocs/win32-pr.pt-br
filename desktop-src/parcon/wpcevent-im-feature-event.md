---
description: Evento por usuário gerado por um cliente de mensagens instantâneas quando recursos definidos são usados em controles dos pais.
ms.assetid: 45e80314-90b1-4fcf-9c8f-c9840ae1775b
title: WPCEVENT_IM_FEATURE evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ee28f004560ed287bc3cb94cbee1bda876355834
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "103921609"
---
# <a name="wpcevent_im_feature-event"></a>\_Evento de \_ recurso WPCEVENT im

Evento por usuário gerado por um cliente de mensagens instantâneas quando recursos definidos são usados em controles dos pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_FEATURE = {0xb, 0x0, 0x10, 0x4, 0x16, 0xb, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AppName* 
</dt> <dd>

O nome do aplicativo de mensagens instantâneas.

</dd> <dt>

*AppVersion* 
</dt> <dd>

A cadeia de caracteres da versão para o aplicativo.

</dd> <dt>

*AccountName* 
</dt> <dd>

O nome da conta de mensagens instantâneas deste usuário.

</dd> <dt>

*Convid* 
</dt> <dd>

A ID desta conversa.

</dd> <dt>

*MediaType* 
</dt> <dd>

Um valor da enumeração [**do \_ \_ recurso WPCFLAG im**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_im_feature) que indica informações sobre os recursos acessados durante uma interação de mensagens instantâneas.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

</dd> <dt>

*RecipCount* 
</dt> <dd>

A contagem de usuários de mensagens instantâneas que estão recebendo o recurso e que têm identidades definidas no campo destinatário.

</dd> <dt>

*Destinatário* 
</dt> <dd>

Uma cadeia de caracteres delimitada que contém identidades de conta de mensagens instantâneas de todos os usuários que estão recebendo o recurso.

</dd> <dt>

*Remetente* 
</dt> <dd>

O nome da conta de mensagens instantâneas para o usuário que está originando o recurso.

</dd> <dt>

*SenderIP* 
</dt> <dd>

O endereço IP do computador do remetente.

</dd> <dt>

*Dados* 
</dt> <dd>

A descrição dos dados no recurso.

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

 

 




