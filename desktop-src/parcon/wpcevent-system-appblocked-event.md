---
description: Evento no nível do sistema gerado por políticas de restrições de software (SRP) quando um aplicativo é bloqueado por regras mais seguras.
ms.assetid: 6772a2c9-35c1-4b75-94e4-baa84af7c0ed
title: WPCEVENT_SYSTEM_APPBLOCKED evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e0444cee0a2844ae868923b5cf51923e0024c9de9a2a12ad51e20d8db9fa3b60
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "120112716"
---
# <a name="wpcevent_system_appblocked-event"></a>\_Evento WPCEVENT System \_ APPBLOCKED

Evento no nível do sistema gerado por políticas de restrições de software (SRP) quando um aplicativo é bloqueado por regras mais seguras.


```C++
const EVENT_DESCRIPTOR WPCEVENT_SYSTEM_APPBLOCKED = {0x10, 0x0, 0x10, 0x4, 0x16, 0x10, 0x8000000000000010};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Estampa* 
</dt> <dd>

A hora em que o bloco ocorreu.

</dd> <dt>

*UserID* 
</dt> <dd>

O identificador de segurança do usuário que está tentando iniciar o aplicativo.

</dd> <dt>

*Caminho* 
</dt> <dd>

O caminho para o aplicativo que o usuário está tentando iniciar.

</dd> <dt>

*RuleID* 
</dt> <dd>

A ID da regra no conjunto de regras mais seguras de controles dos pais que está bloqueando a execução.

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

 

 




