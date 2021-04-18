---
description: Evento de nível de sistema gerado em uma alteração de configuração de controles pais.
ms.assetid: 2540c3cc-96d0-4e01-a525-4da4a857cb58
title: WPCEVENT_SYS_SETTINGCHANGE evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ea0efb4d68fabcb5f9216c4ccf3bb923ee0ff54
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/08/2021
ms.locfileid: "105771381"
---
# <a name="wpcevent_sys_settingchange-event"></a>\_Evento WPCEVENT sys \_ SETTINGCHANGE

Evento de nível de sistema gerado em uma alteração de configuração de controles pais.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYS_SETTINGCHANGE = {0x1, 0x0, 0x10, 0x4, 0x15, 0x1, 0x8000000000000010};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Classe* 
</dt> <dd>

A classe que está gerando o evento.

</dd> <dt>

*Configuração* 
</dt> <dd>

Um valor da enumeração **de \_ configurações de WPC** .

</dd> <dt>

*Proprietário* 
</dt> <dd>

O identificador de segurança do usuário que está gerando o evento.

</dd> <dt>

*OldVal* 
</dt> <dd>

O valor anterior dessa configuração, se excluído ou alterado.

</dd> <dt>

*NewVal* 
</dt> <dd>

O novo valor dessa configuração, se adicionado ou alterado.

</dd> <dt>

*Motivo* 
</dt> <dd>

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

</dd> <dt>

*Opcional* 
</dt> <dd>

Um campo opcional.

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

 

 




