---
description: Evento por usuário gerado por um cliente de mensagens instantâneas quando as informações de contato são adicionadas, alteradas ou removidas nos controles dos pais.
ms.assetid: 0a016542-306e-48b4-8b0c-b9e4e915513e
title: WPCEVENT_IM_CONTACT evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: baac4bf5648b27f2e8d446a79bb2d90d52f0aac416e30d031d3b81d430a6927b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951437"
---
# <a name="wpcevent_im_contact-event"></a>Evento de contato do WPCEVENT \_ im \_

Evento por usuário gerado por um cliente de mensagens instantâneas quando as informações de contato são adicionadas, alteradas ou removidas nos controles dos pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_IM_CONTACT = {0xf, 0x0, 0x10, 0x4, 0x16, 0xf, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AppName* 
</dt> <dd>

O nome do aplicativo de mensagens instantâneas que está gerando o evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

A versão do aplicativo que está gerando o evento.

</dd> <dt>

*AccountName* 
</dt> <dd>

O nome da conta de mensagens instantâneas para este usuário.

</dd> <dt>

*OldName* 
</dt> <dd>

O nome da conta de mensagens instantâneas anterior, se excluído ou alterado.

</dd> <dt>

*OldID* 
</dt> <dd>

A ID associada ao nome da conta de mensagens instantâneas anterior.

</dd> <dt>

*NewName* 
</dt> <dd>

O novo nome da conta de mensagens instantâneas, se adicionado ou alterado.

</dd> <dt>

*NewID* 
</dt> <dd>

A ID que está associada ao novo nome da conta de mensagens instantâneas.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

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

 

 




