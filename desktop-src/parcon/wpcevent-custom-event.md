---
description: Evento por usuário que dá suporte a até três campos.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: WPCEVENT_CUSTOM evento (Wpcevent.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e8082e03aa6dfea8cd2fd461feec093de71a1ada8051b8fb88295d0bbbf570b2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119951546"
---
# <a name="wpcevent_custom-event"></a>Evento WPCEVENT \_ CUSTOM

Evento por usuário que dá suporte a até três campos.

Os eventos são exibidos no **Visualizador de Atividade** na **seção Outros** com a seguinte hierarquia:

1.  Publisher

2.  Aplicativo

3.  Evento


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Publicador* 
</dt> <dd>

O editor do evento (por exemplo, um nome da empresa).

</dd> <dt>

*AppName* 
</dt> <dd>

O nome do aplicativo que está gerando o evento.

</dd> <dt>

*AppVersion* 
</dt> <dd>

A versão do aplicativo que está gerando o evento.

</dd> <dt>

*Evento* 
</dt> <dd>

O nome do evento.

</dd> <dt>

*Value1* 
</dt> <dd>

Campo personalizado 1.

</dd> <dt>

*Valor2* 
</dt> <dd>

Campo personalizado 2.

</dd> <dt>

*Valor3* 
</dt> <dd>

Campo personalizado 3.

</dd> <dt>

*Bloqueado* 
</dt> <dd>

Um valor da [**enumeração \_ ISBLOCKED WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são impedidos de usar e quais controles estão em uso.

</dd> <dt>

*Motivo* 
</dt> <dd>

Uma cadeia de caracteres personalizada que fornece informações adicionais sobre o motivo do bloqueio ou não.

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

 

 




