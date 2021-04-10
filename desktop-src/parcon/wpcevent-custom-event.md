---
description: Evento por usuário que dá suporte a até três campos.
ms.assetid: e6cf8008-b896-453b-9946-a6b3d94a991a
title: WPCEVENT_CUSTOM evento (Wpcevent. h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d20cb2450cd18bb0c77993622d226cfc06dff6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 01/07/2021
ms.locfileid: "104169357"
---
# <a name="wpcevent_custom-event"></a>\_Evento personalizado WPCEVENT

Evento por usuário que dá suporte a até três campos.

Os eventos são exibidos no **Visualizador de atividades** na **outra** seção com a seguinte hierarquia:

1.  Publicador

2.  Aplicativo

3.  Evento


```C++
const EVENT_DESCRIPTOR WPCEVENT_CUSTOM = {0xd, 0x0, 0x10, 0x4, 0x17, 0xd, 0x8000000000000030};
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Publicador* 
</dt> <dd>

O editor do evento (por exemplo, um nome de empresa).

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

*Value2* 
</dt> <dd>

Campo personalizado 2.

</dd> <dt>

*Value3* 
</dt> <dd>

Campo personalizado 3.

</dd> <dt>

*Bloqueado* 
</dt> <dd>

Um valor da enumeração [**\_ IsBlocked de WPCFLAG**](/windows/win32/api/wpcevent/ne-wpcevent-wpcflag_isblocked) que indica informações sobre quais eventos são bloqueados do uso e quais controles estão em vigor.

</dd> <dt>

*Motivo* 
</dt> <dd>

Uma cadeia de caracteres personalizada que fornece informações adicionais sobre o motivo do bloqueio ou não do bloqueio.

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

 

 




