---
description: Evento por usuário gerado por um cliente de email que registra quando um contato é adicionado, alterado ou excluído nos controles dos pais.
ms.assetid: 9d1f52ef-ff49-4c0d-a48a-93aeccbe7f2b
title: WPCEVENT_EMAIL_CONTACT evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8d84a450c53705dae2db777081f7177f43505e0481ae38a67c1b90e507fa4a5d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951566"
---
# <a name="wpcevent_email_contact-event"></a>Evento de contato de \_ email do WPCEVENT \_

Evento por usuário gerado por um cliente de email que registra quando um contato é adicionado, alterado ou excluído nos controles dos pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_EMAIL_CONTACT = {0xe, 0x0, 0x10, 0x4, 0x16, 0xe, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*AppName* 
</dt> <dd>

O nome do aplicativo de email que está gerando o evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

A versão do aplicativo de email que está gerando o evento.

</dd> <dt>

*OldName* 
</dt> <dd>

O nome da conta de email anterior, se excluído ou alterado.

</dd> <dt>

*OldID* 
</dt> <dd>

A ID associada ao nome da conta de email anterior.

</dd> <dt>

*NewName* 
</dt> <dd>

O novo nome da conta de email, se adicionado ou alterado.

</dd> <dt>

*NewID* 
</dt> <dd>

A ID associada ao novo nome de conta de email.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

</dd> <dt>

*EmailAccount* 
</dt> <dd>

O nome da conta de email para este usuário.

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

 

 




