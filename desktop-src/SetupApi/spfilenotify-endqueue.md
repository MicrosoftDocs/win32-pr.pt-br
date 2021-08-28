---
description: A notificação SPFILENOTIFY ENDQUEUE é enviada para a rotina de retorno de chamada quando todas as operações na fila \_ foram concluídas.
ms.assetid: f4540ab6-edea-4f84-b7eb-4ab3f774068b
title: SPFILENOTIFY_ENDQUEUE mensagem (Setupapi.h)
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6192ac867b47b3e5cf9d06806bfb6eb42743aee4d97a935035fd7b44ea0e79b8
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: pt-BR
ms.lasthandoff: 08/11/2021
ms.locfileid: "119665136"
---
# <a name="spfilenotify_endqueue-message"></a>Mensagem SPFILENOTIFY \_ ENDQUEUE

A **notificação SPFILENOTIFY \_ ENDQUEUE** é enviada para a rotina de retorno de chamada quando todas as operações na fila foram concluídas.


```C++
SPFILENOTIFY_ENDQUEUE
  Param1 = (UINT) Result;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a>Parâmetros

<dl> <dt>

*Param1* 
</dt> <dd>

**TRUE** se a fila foi processada com êxito; caso **contrário, FALSE.**

</dd> <dt>

*Param2* 
</dt> <dd>

Não utilizado.

</dd> </dl>

## <a name="return-value"></a>Valor retornado

O valor de retorno é ignorado.

## <a name="requirements"></a>Requisitos



| Requisito | Valor |
|-------------------------------------|---------------------------------------------------------------------------------------|
| Cliente mínimo com suporte<br/> | Windows Somente \[ aplicativos da área de trabalho XP\]<br/>                                           |
| Servidor mínimo com suporte<br/> | Windows Somente aplicativos da área de trabalho server 2003 \[\]<br/>                                  |
| Cabeçalho<br/>                   | <dl> <dt>Setupapi.h</dt> </dl> |



## <a name="see-also"></a>Confira também

<dl> <dt>

[Visão geral](overview.md)
</dt> <dt>

[Notificações](notifications.md)
</dt> <dt>

[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[**SetupDefaultQueueCallback**](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

 




